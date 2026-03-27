---
title: Mobile Optical System (Skypad)
description: Virtual cockpit, simulator, and real-time sharing for any vehicle.
date: 2025-12-01 00:00:00 -0600
image:
  path: /assets/img/posts/2025-12-01-skypad-mos/mos-moab.png
tags: [software, aviation, unreal, graphics]
---

MOS (Mobile Optical System) is a virtual cockpit platform designed for operating and understanding remote vehicles. Originally envisioned for defense applications but inherently dual-use, it combines live video, telemetry, simulation, and AI assistance into a single operator interface. The goal is straightforward: make controlling a remote system feel less like configuring a tool and more like inhabiting the vehicle itself.

I was one of the founding engineers and primary owner of MOS, responsible for taking the concept from early-stage prototypes into a deployable system used in real-world demonstrations, including multiple military environments. That meant building not just the front-end experience, but the underlying systems required to reliably ingest telemetry, stream video, and synchronize data across distributed components.

{% include embed/youtube.html id='3HwLJ5OV-TQ' %}
_MOS demonstrated on cars, boats, drones, and a manned paramotor during the 2024 solar eclipse in Austin, TX._

At its core, MOS presents a real-time video feed from a vehicle alongside a fully customizable interface of telemetry—altitude, airspeed, heading, battery state, and more. Operators can configure layouts and roles, including a “Wingman” mode that allows additional users to join a live session, observe, and assist. This proved especially valuable for remote training, where one operator can guide another in real time while sharing the same situational awareness.

MOS also includes an integrated simulation environment (SkySim), built on global 3D terrain data, allowing operators to train anywhere in the world using the same interface they would use in the field. A feature called “Hyperdrive” enables instant relocation to any environment, making it possible to rehearse missions or simply build piloting proficiency without needing physical hardware.

A built-in AI assistant, MOSES, provides contextual guidance based on live telemetry, flight history, and regulatory knowledge. It can answer operational questions, analyze behavior, and surface insights both during and after flights. This extends into a backend system that records sessions—video and telemetry alike—and makes them accessible for replay, analysis, and aggregation through a web portal.

{% include embed/youtube.html id='Ii3fK_KHXpo' %}
_MOS demonstrated at the Northern Strike exercise, hosted at Camp Grayling military training facility._

From a technical standpoint, MOS is built on Unreal Engine to leverage its real-time rendering capabilities and extensibility. The system integrates multiple data pathways: MQTT for telemetry, WebRTC for low-latency streaming, FFmpeg for video encoding/decoding, and MAVSDK for vehicle communication. Significant effort went into minimizing latency and ensuring synchronization across these channels, including custom tuning of video pipelines and distributed networking strategies.

The primary challenge has been managing complexity—both in terms of Unreal Engine itself and the fragmented nature of vehicle communication systems. Different platforms expose telemetry and video in inconsistent ways, requiring adaptable integration strategies. Despite this, MOS has proven capable of interfacing with a wide range of systems, from drones to ground vehicles and even experimental platforms.

![](/assets/img/posts/2025-12-01-skypad-mos/iron-man-selfie.jpg)
_My "Iron Man selfie", featuring Skypad's MOS._

What differentiates MOS is its perspective. Traditional ground control software focuses on configuration and command. MOS focuses on experience—creating a unified, immersive interface that scales across vehicle types and use cases. Whether operating a drone, a ground vehicle, or something entirely custom, the system treats them all as extensions of the same core idea: a cockpit without a physical frame.

Looking forward, MOS represents a step toward more intuitive human-machine interaction, where the boundary between operator and system becomes increasingly thin.