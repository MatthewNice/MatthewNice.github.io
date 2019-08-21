---
layout: post
title: "CAN Data Collection and Cleaning"
description:
modified: 2019-08-21
tags: [research, cleaning data]
image:
  feature: code_in_car.jpg
  credit: MatthewNice
  creditlink:
---

## Notes on My Data Collection

See **PandaCANAnalysis.ipynb** on my GitHub for comments and notes on code. Here I have some freeform comments on the data analysis process.

### Standard Row of Data Collected From a Vehicle

| Index| Time | Bus |Addr | Message |MessageLength |
|:--------|:-------:|--------:|:--------|:-------:|--------:|
| 0   | 3.048295   |0 | 170  | 1e5c1e741e5d1e6c   | 8   |
|=====
{: rules="groups"}

### Breaking Down the Table
Messages are sent in batches of up to 256 bytes, with tens of batches per second. For each message, we record many attributes so we can make sense of what happened in the car later. Index and time are pretty trivial, we know what those mean without explanation. Message Length is the number of bytes the message is long. Bus refers to the controller area network (CAN) bus the message was sent on. Different vehicles have different numbers of buses, often reserved for macro level grouping of ‘critical’ or ‘secondary’ messages to be sent. In this case, the message sent was from bus 0.

### Addr and Message
The last two pieces of data convey a lot of information. The addr and message are a pair of sorts. Addr is the numerical address that identifies the category of information in the message. An address has a group of signals that go together, i.e. all the signals for wheel speeds go together at one address. Generally speaking the closer the address of the message is to 0, the more critical it is to the core function of the car. Lower addresses include the brakes and speed, while higher addresses include the turn signal and the door sensors.

The car’s electronic control units (ECUs) and sensors are all connected to the CAN bus, and filter out only the messages sent on the address(es) relevant to them. The address gives the context to decipher the information embedded in the hexadecimal message string. Each message contains 8 bytes of information which can be broken down into a set of signals. Address 170 is a message on wheel speeds. A message sent with the address 170 contains four signals of 16 bits: front right wheel, front left wheel, rear right wheel, and rear left wheel. Each signal is the same size and has the same characteristics. In contrast, something like the Brake Module message contains ‘brake pressure’ and ‘brake position’ signals that are 9 bits each, and a ‘brake pressed' signal that is one bit (since it is binary, it only needs one bit).

### DBC Breakdown
Each message is different, and is decoded with a DBC file. The DBC has stringent formatting rules that convey the messages, the signals subset of the message, the start, size, scale, offset, min, max, unites, endian-ness, and signed-ness of the message. This system is used for all sorts of vehicles (yachts, riding lawn mowers, trucks, etc.) There are also multiplexed messages, which,  “can be used (indirectly) to send more than 8 bytes using a single message ID." For example, if we use a 2-bit MUX, we can send 62-bits of data with four multiplexers (M0, M1, M2, M3). In other words, your message could state that:\n
If first 2-bits are 0 (M0), then 62-bits of data is for the car's front sensors
If first 2-bits are 1 (M1), then 62-bits of data is for the car's rear sensors”
See the SJSU article referenced for more details. Anyway, here is an example of the front right wheel speed signal in my DBC file:

> SG_ WHEEL_SPEED_FR : 7,16@0+ (0.01,-67.67) [0,250] "kph" XXX

Follow the components of the line from left to right. Wheel speed, front right. Start at bit 7, 16 bits long, big-endian, unsigned, scale 0.01, offset -67.67, min value 0, maximum value 250, units kph. We can now take the bits from 7 to 16 in the messages, and transform them from hexadecimal to a value that is the speed of the front right wheel.

![Wheel Speeds Image]({{ site.url }}/images/wheel speed.png)

You might have thought to yourself, “for the wheel speeds message there were four messages of 16 bits, adding up to the 64 bits (8 bytes) that is the size of the message. In contrast, the brake module message has three signals adding up to 19 bits, well short of the size of the message. Surely, there is more information in that message!” If you are thinking that, then congratulations on your knowledge of unit conversion. I always forget how many bits to a byte. I have no idea what the other information is on these Brake Module kind of messages. A few signals have been deciphered but not the whole thing. Manufacturers are definitely sometimes using the space that isn't deciphered for sending signals, and other times that space is just left reserved for future use. Almost all of the DBC information I have is from others’ work online (comma.ai github, car hacker forums); since manufacturers don’t publish their DBC files online they have to get reverse engineered to make sense of them. It makes sense to me that for the hundreds of signals send on the car that not all of them fit nicely into 8 byte groupings, so some space is kind of wasted. As the computing power of cars expands, the inefficiencies of bit packing are probably more and more irrelevant.

Eight key parts of a CAN message:

	* SOF: start of frame dominant 0
	* CANID: Address of message.
	* RTR: remote transmission request ECU requests data from another ECU
	* Message Length: length of message in bytes
	* Message: Signals
	* CRC: cyclic redundancy check, checks message integrity
	* ACK: indicates if CRC process is ok
	* EOF: Marks the end of CAN message

References:
[DBC_Format](http://socialledge.com/sjsu/index.php/DBC_Format)
