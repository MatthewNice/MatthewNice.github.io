---
layout: page
title: Research Projects
image:
  feature: 1.png
comments: false
modified: 2019-07-17
---
# Vanderbilt
## Decoding Vehicle Messages, ACC Transportation Research
In the Work Laboratory I inherited the beginnings of a project working on reading out and analyzing car sensor data.  The figure shows the cord connected from behind the rear-view mirror that was used to record CAN messages. I created a data analysis toolset for the CAN messages being recorded off of vehicles. Using it, 50+ signals can be interpreted and analyzed in depth after a drive. Importantly, signals from the Automated Cruise Control, radar systems, and spedometer (among others) relate to ongoing research on the calibration of car following.

The ability to record the actions of the car opens the door for understanding the currently implemented following algorithms from manufacturers. It also is a big step closer toward testing an optimized car following algorithm from the lab, fingerprinting drivers, and more.


<figure>
	<a href="{{ site.url }}/images/panda.jpeg"><img src="{{ site.url }}/images/panda.jpeg" alt=""></a>
</figure>


Tools:
* Python 3
* pandas data analysis library
* cantools library
* Comma.ai Panda and Giraffe
* Toyota Camry, Toyota Rav4 2019

## Reverse engineering vehicle messages and signals
