---
title: Wearable LED Displays
description: A flexible, programmable, and animatable LED display technology for clothing.
date: 2021-05-01 00:00:00 +0600
image:
  path: /assets/img/avatar.jpg
---

An idea born out of the COVID-19 pandemic.

I thought it would be a novel idea to attempt to integrate a dot-matrix LED display into facemasks, so they would be customizable, flashy (literally), and more fun to wear. After some consideration though, I realized this idea had more potential than just facemasks; imagine hats, tube socks, bracelets, and more! Thus, the goal of developing an all-in-one, wearable, shapeable dot-matrix LED display technology came about.

Allow me to break that list of adjectives down a little bit:

- **All-In-One:** images and video can be stored and displayed on the device without the help of an external driver or controller
- **Wearable:** the display is flexible, lightweight, and comfortable against the skin
- **Shapeable:** displays of different shapes and sizes (even non-rectangular) can be created and supported under a universal set of firmware

I dubbed the project FIRMWEAR (get it?) and began constructing a prototype. Below is a gallery containing some images and videos from early development.

![https://grantwilk.com/wp-content/uploads/2021/05/PXL_20200926_225132727-min-1024x566.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/PXL_20201015_174237249-min-1024x768.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/PXL_20200926_223033250-01-min-1024x654.jpeg]()
![https://grantwilk.com/wp-content/uploads/2021/05/PXL_20201113_152801364-min-1024x768.jpg]()

As I worked, I quickly realized that there was a lot of work involved with this project. So, I decided to recruit some of my fellow computer engineering friends to help. I held a short pitch meeting at my apartment with some pizza and landed two extra pairs of hands to help bring my idea to fruition.

Because collaborative work requires effective communication, a lot of documentation had to be created in order to effectively communicate our ideas. It was a unique challenge trying to come up with sensical diagrams for some of the content we had to communicate, but I think we did a great job. Below are some of our diagrams, explaining the basic functionality of the devices.

![https://grantwilk.com/wp-content/uploads/2021/05/dp-00-00-high-level-hardware-diagram-page-001.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/dp-00-00-media-class-diagram-page-001-696x1024.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/dp-00-00-nucleo-schematic-page-001-1024x904.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/dp-00-00-render-pipeline-data-flow-page-001-1024x245.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/dp-00-00-rom-memory-structure-page-001-1024x617.jpg]()
![https://grantwilk.com/wp-content/uploads/2021/05/dp-00-00-system-component-diagram-page-001-1024x301.jpg]()

Eventually, our ideas and work began to come together. My friend Austin played a crucial role in the design and implementation of the device's external control interface (ECI), which can be used to communicate with a host device like a computer or smartphone over USB or Bluetooth. My other friend, Colton, helped with the design and implementation of the device's ROM memory manager.

Below is the completed prototype hardware, sporting an EEPROM, a USB interface, and a serially driven dot-matrix LED display.

![https://grantwilk.com/wp-content/uploads/2021/05/PXL_20210309_212311918-min-1024x797.jpg]()

Unfortunately, due to increasing workloads with school and a general lack of interest in continuing from all team members, the concept of FIRMWEAR displays never made it past the prototype phase. It's a bummer, but at the same time, we all have much more exciting ideas in mind as we head into the summer following our third year of studies.

Perhaps we'll return to FIRMWEAR in the future... only time will tell. Until then, check out these awesome demonstrations of the prototype technology in action!

![https://grantwilk.com/wp-content/uploads/2021/05/Vid-20200817-225103-1.mp4](Default rainbow-cycle demonstration)
![https://grantwilk.com/wp-content/uploads/2021/05/Pxl-20210311-040749764-1.mp4](Pac-Man multi-frame animation demonstration)
![https://grantwilk.com/wp-content/uploads/2021/05/Pxl-20210321-181605460-1.mp4](Saint Patrick's Day multi-profile demonstration)
![https://grantwilk.com/wp-content/uploads/2021/05/Pxl-20210205-200745627-1.mp4](Display programming via command-line application demonstration)