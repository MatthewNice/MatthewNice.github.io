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
In the Work Laboratory I inherited the beginnings of a project working on reading out and analyzing car sensor data.  The figure shows the cord connected from behind the rear-view mirror that was used to record CAN messages. I created a data analysis toolset for the CAN messages being recorded off of vehicles. Using it, 50+ signals can be interpreted and analyzed in depth after a drive. Importantly, signals from the Automated Cruise Control, radar systems, and speedometer (among others) relate to ongoing research on the calibration of car following.

The ability to record the actions of the car opens the door for understanding the currently implemented following algorithms from manufacturers. It also is a big step closer toward testing an optimized car following algorithm from the lab, fingerprinting drivers, and more.


<figure>
	<a href="{{ site.url }}/images/panda.jpeg"><img src="{{ site.url }}/images/panda.jpeg" alt=""></a>
</figure>


Tools:
* Python 3
* pandas data analysis library
* cantools library

## Reverse engineering vehicle messages and signals

# Undergraduate Research at Tulane
## Angiogenesis in Stem Cells
Stem cells derived from different sources are thought to have different results when interacting with microvascular networks. For this project, we harvested the thin mesenteric tissue from rats and cultured them for 5 days while they were still viable. Differing groups had adult, aged, adipose-derived, and bone marrow-derived stem cells embedded into them. By highlighting the cells and the blood vessels of the tissue with immunohistochemistry, we could track the changes in the microvasculature of the tissue over time.

<figure>
	<a href="{{ site.url }}/images/1.png"><img src="{{ site.url }}/images/1.png" alt=""></a>
</figure>

Above is a sample montage image of a harvested tissue. The blood vessels are in green, the stem cells are in red. The essential measurements were A) what is the change in the blood vessels over time, and B) are the cells migrating and showing pericyte behavior. Pericytes are a specific state of the stem cells that is known to facilitate blood flow and angiogenesis.

## Taking the Model from Rat to Mouse

The above model had been established in rats, but doing the same in mouse would make it more powerful. Instead of two markers to track cell types in rats (as seen in the image above), mice could easily have 4+. This is because genetic engineering is much more advanced in mice. Instead of using immunohistochemistry, we could use CRISPR or other genetic tech to make the cells trackable over time. Another feature is that the tissue culture could stay in ideal conditions longer because there would be no need for the laborious 2-4 hour immunohistochemical procedures to be performed. The most exciting aspect of the genetically engineered mouse model is that temporal and chemical genetic triggers can be put in place. This means a lot for understanding the timing of cell movement for angiogenesis. If we can track 4+ cell types simultaneously and their reactions to specific triggers as manipulated by researchers, that would be really cool. The major hiccup in mimicking the rat model in mice is that mouse mesentery isn't vascularized like rat mesentery.

My contribution to this line of thought was my Tulane Honors Thesis. I showed that angiogenesis could be induced in mouse mesentery after being harvested. This initial step sets the stage for future research in my lab and others for exploring the possibilities of angiogenesis studied the mouse mesentery culture model.
