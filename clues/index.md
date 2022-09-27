---
layout: page
title: TREASURE HUNT
image:
  feature: dubs/cap_hill.jpg
comments: false
modified: 2019-07-17
---
# Welcome to the Treasure Hunt!
## That's right -- I made an interactive website custom for this treasure hunt.

<figure class = "half">
  <a href="{{ site.url }}/images/dubs/pinkys.jpg"><img src="{{ site.url }}/images/dubs/pinkys.jpg" alt=""></a>
  <a href="{{ site.url }}/images/steer_angle.png"><img src="{{ site.url }}/images/steer_angle.png" alt=""></a>
</figure>

Initially, decoding the radar was confounding. Radar data collection didn't follow the pattern of the rest of the CAN messages and signals from before. Looking at just one signal is quite the mess:

<figure class = "half">
<a href="{{ site.url }}/images/radar_all_track.png"><img src="{{ site.url }}/images/radar_all_track.png" alt=""></a>
<a href="{{ site.url }}/images/all_track.png"><img src="{{ site.url }}/images/all_track.png" alt=""></a>
</figure>

 Eventually, by understanding the physics of the radar system, we figured out how to filter the data and understand what the radar was recording. I used these methods to keep track of the leading vehicle and vehicles in other lanes the two images below show. You will notice the longitudinal distance and relative velocity of two different cars the ego car is tracking. They align exactly with video recordings of the drive, and redundant GPS sensor data collected.

<figure class = "half">
  <a href="{{ site.url }}/images/relVel2.png"><img src="{{ site.url }}/images/relVel2.png" alt=""></a>
  <a href="{{ site.url }}/images/longdist2.png"><img src="{{ site.url }}/images/longdist2.png" alt=""></a>
</figure>

Tools:
* Python 3
* pandas library
* numpy library
* cantools library

# Undergraduate Research at Tulane
## Effects of Different Stem Cells in Rat Microvasculature Model
Stem cells derived from different sources are thought to have different effects when interacting with microvascular networks. For this project, we harvested the thin mesenteric tissue from rats and cultured them for 5 days while they were still viable. Differing experimental groups had adult, aged, adipose-derived, and bone marrow-derived stem cells embedded into them. By highlighting the cells and the blood vessels of the tissue with immunohistochemistry, we could track the changes in the microvasculature of the tissue over time.

<figure>
	<a href="{{ site.url }}/images/1.png"><img src="{{ site.url }}/images/1.png" alt=""></a>
</figure>

Above is a sample montage image of a couple centimeter wide harvested tissue. Originally it was over a GB in size (very hi-res microscopy). The blood vessels are in green, the stem cells are in red. The essential measurements were A) what is the change in the blood vessels over time, and B) are the cells migrating and showing pericyte behavior. Pericytes are a specific state of the stem cells that is known to facilitate blood flow and angiogenesis.

## Taking the Model from Rat to Mouse

The above model had been established in rats, but doing the same in mouse would make it more powerful. Instead of two markers to track cell types in rats (as seen in the image above), mice could easily have 4+. This is because genetic engineering is much more advanced in mice. Instead of using immunohistochemistry, we could use CRISPR or other genetic tech to make the cells trackable over time. Another feature is that the tissue culture could stay in ideal conditions longer because there would be no need for the laborious 2-4 hour immunohistochemical procedures to be performed. The most exciting aspect of the genetically engineered mouse model is that temporal and chemical genetic triggers can be put in place. This means a lot for understanding the timing of cell movement for angiogenesis. If we can track 4+ cell types simultaneously and their reactions to specific triggers as manipulated by researchers, that would be really cool. The major hiccup in mimicking the rat model in mice is that mouse mesentery isn't vascularized like rat mesentery.

My contribution to this line of thought was my Tulane Honors Thesis. I showed that angiogenesis could be induced in mouse mesentery after being harvested. This initial step sets the stage for future research in my lab and others for exploring the possibilities of angiogenesis studied the mouse mesentery culture model.