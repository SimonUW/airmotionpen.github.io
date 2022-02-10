---
layout: post
title:  "Model Training"
date:   2022-02-02 13:00:00 -0500
categories: design
---

## The work so far
We have been placing orders for components such as touch tensors, pressure sensors, and a bluetooth module to update our prototype. Testing is being done for these components along with the previously purchased parts with the MCU. The tests have shown there are a couple issues with the z-axis rotation detection and are currently being fixed.

The gesture recognition model has been trained with 70 sets of IMU data so far without dynamic time wrapping. The model has achieved 90.9% test accuracy to this date.


## Next steps
* Continue data collection
* Update the motion history images (MHI) algorithm
* Train the gesture recognition model with a more diverse dataset and implement dynamic time wrapping (DTW) to measure the similarity between temporal sequences.
