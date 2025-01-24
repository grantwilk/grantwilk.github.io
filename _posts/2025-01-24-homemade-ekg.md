---
title: Homemade EKG
description: A surprise trip to the ER turns into a mission to capture heart arrhythmias at home.
date: 2025-01-24 00:00:00 -0600
image:
  path: /assets/img/posts/2025-01-24-homemade-ekg/homemade-ekg.jpg
tags: [hardware, signal processing, team]
---

I had open-heart surgery at the age of two, so heart health has always been a significant part of my life. Recently, a sudden heart arrhythmia led me to the ER, only for my heart to revert to a normal sinus rhythm the moment I was hooked up to an EKG, which was both frustrating and expensive. This experience sparked my curiosity and inspired me to create a homemade EKG.

The journey began with a USB oscilloscope and EKG pads from Amazon. With my friend Michael's help, we experimented with different electrode placements, trying to find the optimal configuration to detect a clear signal. The breakthrough came when we placed electrodes on the chest and foot, creating the highest potential difference we were capable of capturing while still using the body as a ground reference.

{% include embed/youtube.html id='09inn7hn8KQ' %}

However, the raw signals were incredibly noisy. Through research and experimentation, we implemented a fourth-order software bandpass filter between 300 mHz and 20 Hz, which drastically improved the clarity of the heartbeats. We also tried averaging multiple leads to further refine the signal, and while this provided a moderate improvement, it was the fine-tuned filter that truly made the difference.

Once we perfected our filtration process, we were able to capture clear EKG footage for each of the standard 5-lead cardiac views. When I showed this data to my girlfriend, a cardiac RN, she was able to identify the PQRST waves, confirming the accuracy of our readings.

{% include embed/youtube.html id='xNw-femFH9Q' %}

The highlight of this project was capturing my arrhythmia, a set of Premature Atrial Contractions (PACs), which was confirmed a few days later by a medical-grade Holter monitor. This means that my crazy engineering endeavors were able to not only capture a moment that a hospital-grade machine missed, but also beat the medical system as a whole to an accurate diagnosis.

Of course, my knowledge ends there, so I'm back in the hands of the American healthcare system. Lets hope I don't have to build any more DIY medical equipment!

![](/assets/img/posts/2025-01-24-homemade-ekg/homemade-ekg-wave.jpg)
_The PQRST waves labeled on our EKG reading._

{% include embed/youtube.html id='NOFYVN09Ew8' %}

![](/assets/img/posts/2025-01-24-homemade-ekg/homemade-ekg-hardware.jpg)
_The EKG hardware consists of an Analog Discovery 2, EKG pads, and tin-foil shielded alligator clips!_