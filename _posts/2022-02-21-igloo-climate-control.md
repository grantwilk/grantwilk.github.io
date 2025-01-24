---
title: Paper Igloo Climate Control
description: A simple programmable climate control system for a paper igloo
date: 2022-02-21 00:00:00 -0600
image:
  path: /assets/img/posts/2022-02-21-igloo-climate-control/igloo-climate-control.jpg
tags: [hardware, firmware]
---

For my advanced embedded systems class, I designed the Digital Paper Igloo Climate Control System, a compact and interactive project that demonstrates temperature regulation using an embedded controller. The system features a TMP36 thermometer, a heating element, and a fan housed inside a small "igloo." An LCD screen displays the current temperature and user-defined setpoint, with real-time updates smoothed by a 100-sample moving average for improved readability. LEDs provide visual feedback, with one indicating power to the heating element and the other representing the PWM signal controlling the fan.

Using simple buttons, users can adjust the setpoint, activating the heating and cooling components when needed. While the design works, I realized an oversight in placing the heating element outside the airflow, unintentionally creating an air conditioner effect instead of a heater. Future iterations would improve mechanical integration by placing the heating element closer to the thermometer for better thermal diffusion.

Watch the system in action here:

{% include embed/youtube.html id='QCMUzJWZC0E' %}