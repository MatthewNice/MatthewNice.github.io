---
title: "CAN coach: Vehicular control through human cyber-physical systems"
collection: publications
excerpt: 'This work addresses whether a human-in-the-loop cyber-physical system (HCPS) can be effective in improving the longitudinal control of an individual vehicle in a traffic flow. We introduce the CAN Coach, which is a system that gives feedback to the human-in-the-loop using radar data (relative speed and position information to objects ahead) that is available on the controller area network (CAN). Conclusions include that it is possible to coach drivers to improve performance on driving tasks using CAN data.'
date: 2021-09-15
venue: 'Proceedings of the ACM/IEEE 12th International Conference on Cyber-Physical Systems (ICCPS)'
paper_url: 'https://arxiv.org/abs/2104.06264'
authors: '**Nice, Matthew W.** and Elmadani, Safwan and Bhadani, Rahul and Bunting, Matt and Sprinkle, Jonathan and Work, Dan'
citation:
cover_image: stack_alt2.png

---

This work addresses whether a human-in-the-loop cyber-physical system (HCPS) can be effective in improving the longitudinal control of an individual vehicle in a traffic flow. We introduce the CAN Coach, which is a system that gives feedback to the human-in-the-loop using radar data (relative speed and position information to objects ahead) that is available on the controller area network (CAN). Using a cohort of six human subjects driving an instrumented vehicle, we compare the ability of the human-in-the-loop driver to achieve a constant time-gap control policy using only human-based visual perception to the car ahead, and by augmenting human perception with audible feedback from CAN sensor data. The addition of CAN-based feedback reduces the mean time-gap error by an average of 73%, and also improves the consistency of the human by reducing the standard deviation of the time-gap error by 53%. We remove human perception from the loop using a ghost mode in which the human-in-the-loop is coached to track a virtual vehicle on the road, rather than a physical one. The loss of visual perception of the vehicle ahead degrades the performance for most drivers, but by varying amounts. We show that human subjects can match the velocity of the lead vehicle ahead with and without CAN-based feedback, but velocity matching does not offer regulation of vehicle spacing. The viability of dynamic time-gap control is also demonstrated. We conclude that (1) it is possible to coach drivers to improve performance on driving tasks using CAN data, and (2) it is a true HCPS, since removing human perception from the control loop reduces performance at the given control objective.
