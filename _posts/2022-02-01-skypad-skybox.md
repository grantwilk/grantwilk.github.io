---
title: Skypad: Skybox
description: An embedded telemetry device designed to capture real-world data from any vehicle.
date: 2025-02-01 00:00:00 -0600
image:
  path: /assets/img/posts/2022-02-01-skypad-skybox/skybox-in-housing.jpg
tags: [hardware, firmware, esp32, jetson, team]
---

Skybox is an embedded telemetry device designed to capture real-world data from vehicles and stream it directly into MOS. It acts as an ingestion point at the edge—bridging physical systems and the software platform by collecting, standardizing, and transmitting telemetry in real time.

I led the development of Skybox, focusing primarily on system architecture and firmware while my close 
friend Jack took on hardware design and manufacturing. This was my first professional embedded system, and it required translating high-level product goals into a reliable, deployable device. The platform was built around an ESP32 microcontroller and integrated a wide range of sensors, including GPS, a 9-axis IMU, and a barometer, along with CAN bus support for interfacing directly with vehicles.

![](/assets/img/posts/2022-02-01-skypad-skybox/skybox-bags.jpg)
_Skybox units in electrostatic bags, ready to be shipped to customers._

The firmware was responsible for aggregating telemetry from all onboard and external sources, normalizing it into a unified format, and transmitting it over Wi-Fi using a custom UDP-based protocol to MOS. The device also hosted a lightweight web interface for configuration and logged all telemetry locally to an SD card for redundancy. Expandability was a key design goal—exposed GPIO and communication interfaces (UART, SPI, I2C) allowed Skybox to integrate with additional sensors or systems as needed.

One of the more challenging aspects was dealing with real-world variability. GPS signal quality varied significantly depending on mounting location, which led to support for external antennas. CAN bus integration was equally complex—different vehicle manufacturers expose different parameters, requiring extensive research and adaptation to extract meaningful telemetry across platforms.

![](/assets/img/posts/2022-02-01-skypad-skybox/skybox-jack-working.jpg)
_Jack troubleshooting a hardware bug on the first batch of Skybox units._

Skybox was deployed across a variety of systems, including cars, bicycles, and go-karts, proving its ability to serve as a universal telemetry layer. It enabled MOS to operate beyond drones, extending into ground-based and experimental platforms by providing a consistent data pipeline from the physical world.

This concept later evolved into an expanded version of the platform—an upgraded “Super” Skybox built around an NVIDIA Jetson. This iteration added onboard video capture and streaming alongside telemetry, effectively turning the device into a self-contained MOS integration module. With a single unit, any vehicle could be equipped with both real-time video and telemetry, dramatically lowering the barrier to integrating new platforms into the ecosystem.

![](/assets/img/posts/2022-02-01-skypad-skybox/super-skybox-chessboard.jpg)
_An early prototype of the Super Skybox system, mounted to a chessboard as a chassis._

Skybox represents the foundation of the broader system architecture: a modular, extensible edge device that transforms raw sensor data into actionable insight within a unified virtual cockpit.
