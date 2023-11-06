---
title: "So you think you can track?"
collection: publications
excerpt: 'This work introduces a multi-camera tracking dataset consisting of 234 hours of video data recorded concurrently from 234 overlapping HD cameras covering a 4.2 mile stretch of 8-10 lane interstate highway near Nashville, TN. GPS trajectories from 270 vehicle passes through the scene are manually corrected in the video data to provide a set of ground-truth trajectories for recall-oriented tracking metrics, and object detections are provided for each camera in the scene (159 million total before cross-camera fusion).'
date: 2023-09-15
venue: 'Winter Conference on the Application of Computer Vision (WACV)'
paper_url: 'https://arXiv.org/abs/2309.07268'
authors: 'Gloudemans, Derek and Zachar, Gergely and Wang, Yanbing and Ji, Junyi and **Nice, Matthew W.** and Bunting, Matt and Barbour, William and Sprinkle, Jonathan and Piccoli, Benedetto and Monache, Maria Laura Delle and others'
citation:
cover_image: MattHAT.jpeg

---

This work introduces a multi-camera tracking dataset consisting of 234 hours of video data recorded concurrently from 234 overlapping HD cameras covering a 4.2 mile stretch of 8-10 lane interstate highway near Nashville, TN. The video is recorded during a period of high traffic density with 500+ objects typically visible within the scene and typical object longevities of 3-15 minutes. GPS trajectories from 270 vehicle passes through the scene are manually corrected in the video data to provide a set of ground-truth trajectories for recall-oriented tracking metrics, and object detections are provided for each camera in the scene (159 million total before cross-camera fusion). Initial benchmarking of tracking-by-detection algorithms is performed against the GPS trajectories, and a best HOTA of only 9.5% is obtained (best recall 75.9% at IOU 0.1, 47.9 average IDs per ground truth object), indicating the benchmarked trackers do not perform sufficiently well at the long temporal and spatial durations required for traffic scene understanding.
