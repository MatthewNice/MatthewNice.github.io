---
title: "Online parameter estimation methods for adaptive cruise control systems"
collection: publications
excerpt: 'Two online methods are introduced to estimate model parameters of Adaptive Cruise Control enabled vehicles. The first technique is a recursive least squares approach, while the second method solves a nonlinear joint state and parameter estimation problem via particle filtering. All methods are tested both on synthetic data created using known model parameters, as well as on empirical data collected directly from a 2019 model year ACC vehicle using data from sensors that are part of the stock ACC system.'
date: 2020-09-15
venue: 'IEEE Transactions on Intelligent Vehicles (IEEE T-IV)'
paper_url: 'https://doi.org/10.1109/TIV.2020.3023674'
authors: 'Wang, Yanbing and Gunter, George and **Nice, Matthew W.** and Delle Monache, Maria Laura and Work, Daniel B'
citation:
cover_image: radar_car4.png

---

Two online methods are introduced to estimate model parameters of  \textit{Adaptive Cruise Control} (ACC) enabled vehicles. The first technique is a recursive least squares approach, while the second method solves a nonlinear joint state and parameter estimation problem via particle filtering. The accuracy and computational runtime of the online proposed methods are compared to a commonly used offline simulation-based optimization approach. All methods are tested both on synthetic data created using known model parameters, as well as on empirical data collected directly from a 2019 model year ACC vehicle using data from sensors that are part of the stock ACC system. The online methods (recursive least-squares and the particle filter) are scalable, faster than the batch optimization method, and provide comparable accuracy to the batch method. The recursive least-squares method is two orders of magnitude faster than the batch method for modest sized (e.g., 15 min) datasets, and is the fastest overall. The particle filter also runs in real-time, and is also suitable in streaming applications in which the datasets can grow arbitrarily large.
