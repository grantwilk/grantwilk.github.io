---
title: Wearable LED Displays
description: A flexible, programmable, and animatable LED display technology for clothing.
date: 2021-05-01 00:00:00 +0600
image:
  path: /assets/img/posts/2021-05-01-wearable-led-displays/firmwear-paper-pcb-illuminated.jpg
---

An idea born out of the COVID-19 pandemic.

I thought it would be a novel idea to attempt to integrate a dot-matrix LED display into facemasks, so they would be customizable, flashy (literally), and more fun to wear. After some consideration though, I realized this idea had more potential than just facemasks; imagine hats, tube socks, bracelets, and more! Thus, the goal of developing an all-in-one, wearable, shapeable dot-matrix LED display technology came about.

Allow me to break that list of adjectives down a little bit:

- **All-In-One:** images and video can be stored and displayed on the device without the help of an external driver or controller
- **Wearable:** the display is flexible, lightweight, and comfortable against the skin
- **Shapeable:** displays of different shapes and sizes (even non-rectangular) can be created and supported under a universal set of firmware

I dubbed the project FIRMWEAR (get it?) and began constructing a prototype. Below is a gallery containing some images and videos from early development.

![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-paper-pcb-blank.jpg)
_The blank paper PCB layout._

![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-paper-pcb-populated.jpg)
_The paper PCB after it was populated with LEDs._


![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-paper-pcb-illuminated.jpg)
_The paper PCB after being illuminated with an RGB wave pattern._

As I worked, I quickly realized that there was a lot of work involved with this project. So, I decided to recruit some of my fellow computer engineering friends to help. I held a short pitch meeting at my apartment with some pizza and landed two extra pairs of hands to help bring my idea to fruition.

Because collaborative work requires effective communication, a lot of documentation had to be created in order to effectively communicate our ideas. It was a unique challenge trying to come up with sensical diagrams for some of the content we had to communicate, but I think we did a great job. Below are some of our diagrams, explaining the basic functionality of the devices.

![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-system-architecture.jpg)
![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-media-class-diagram.jpg)
![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-nucleo-schematic.jpg)
![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-render-pipeline.jpg)
![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-rom-structure.jpg)
![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-system-component-diagram.jpg)

Eventually, our ideas and work began to come together. My friend Austin played a crucial role in the design and implementation of the device's external control interface (ECI), which can be used to communicate with a host device like a computer or smartphone over USB or Bluetooth. My other friend, Colton, helped with the design and implementation of the device's ROM memory manager.

![](/assets/img/posts/2021-05-01-wearable-led-displays/firmwear-breadboard.jpg)
_The completed prototype hardware, sporting an EEPROM, a USB interface, and a serially driven dot-matrix LED display._

Unfortunately, due to increasing workloads with school and a general lack of interest in continuing from all team members, the concept of FIRMWEAR displays never made it past the prototype phase. It's a bummer, but at the same time, we all have much more exciting ideas in mind as we head into the summer following our third year of studies.

Perhaps we'll return to FIRMWEAR in the future... only time will tell. Until then, check out these awesome demonstrations of the prototype technology in action!

![https://grantwilk.com/wp-content/uploads/2021/05/Vid-20200817-225103-1.mp4](Default rainbow-cycle demonstration)
![https://grantwilk.com/wp-content/uploads/2021/05/Pxl-20210311-040749764-1.mp4](Pac-Man multi-frame animation demonstration)
![https://grantwilk.com/wp-content/uploads/2021/05/Pxl-20210321-181605460-1.mp4](Saint Patrick's Day multi-profile demonstration)
![https://grantwilk.com/wp-content/uploads/2021/05/Pxl-20210205-200745627-1.mp4](Display programming via command-line application demonstration)