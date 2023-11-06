---
title: "Deploying traffic smoothing cruise controllers learned from trajectory data"
collection: publications
excerpt: 'Autonomous vehicle-based traffic smoothing con-trollers are often not transferred to real-world use due to challenges in calibrating many-agent traffic simulators. We show a pipeline to sidestep such calibration issues by collecting trajectory data and learning controllers directly from trajectory data that are then deployed zero-shot onto the highway. We construct a dataset of 772.3 kilometers of recorded drives on the I–24. We then construct a simple simulator using the recorded drives as the lead vehicle in front of a simulated platoon consisting of one autonomous vehicle and five human followers. Using policy-gradient methods with an asymmetric critic to learn the controller, we show that we are able to improve average MPG by 11% in simulation on congested trajectories. We deploy this controller to a mixed platoon of 4 autonomous Toyota RAV-4's in a validation experiment.'
date: 2022-09-15
venue: '2022 International Conference on Robotics and Automation (ICRA)'
paper_url: ''
authors: '**Nice, Matthew W. \*** and Lichtle , Nathan\* and Vinitsky, Eugene\* and Seibold, Benjamin and Work, Dan and Bayen, Alexandre M'
citation:
cover_image: 11_cars.png

---

Autonomous vehicle-based traffic smoothing con-trollers are often not transferred to real-world use due to challenges in calibrating many-agent traffic simulators. We show a pipeline to sidestep such calibration issues by collecting trajectory data and learning controllers directly from trajectory data that are then deployed zero-shot onto the highway. We construct a dataset of 772.3 kilometers of recorded drives on the I–24. We then construct a simple simulator using the recorded drives as the lead vehicle in front of a simulated platoon consisting of one autonomous vehicle and five human followers. Using policy-gradient methods with an asymmetric critic to learn the controller, we show that we are able to improve average MPG by 11% in simulation on congested trajectories. We deploy this controller to a mixed platoon of 4 autonomous Toyota RAV-4's in a validation experiment.
