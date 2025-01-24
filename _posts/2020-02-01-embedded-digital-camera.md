---
title: Embedded Digital Camera
description: A small digital camera that takes photos and saves them to an SD card.
date: 2020-02-01 00:00:00 -0600
image:
  path: /assets/img/posts/2020-02-01-embedded-digital-camera/digital-camera.jpg
---

For our final project in Embedded Systems II, we were given free reign to create just about anything we'd like, as long as it was related to what we were working on in class. I decided it would be a fun challenge to try and interface an OV7670 camera module and a microSD card with our provided microcontroller to try and create an embedded digital camera.

Here's the full list of materials I used:

- ST NUCLEO-F446RE Development Board
- OV7670 Camera Module
- MicroSD Breakout Board with SPI interface
- Misc. breadboards, wires, buttons, etc.

![](/assets/img/posts/2020-02-01-embedded-digital-camera/digital-camera-test.jpg)
_Digital camera testing apparatus._

## Results

The project was a great learning experience for me. I had the opportunity to experiment with our microcontroller's digital camera media interface, build an understanding of ST's HAL, practice working with SPI peripherals, learn how DMA controllers work, and even explore FAT file systems from an embedded perspective.

While I wasn't able to get flawless results out of the camera due to awkward timing and buffering issues with the DCMI that I was unable to debug in time, I did manage to take a pretty artsy selfie!

![](/assets/img/posts/2020-02-01-embedded-digital-camera/digital-camera-photo.jpg)
_My gorgeous face, duplicated four times due to timing and buffering issues._