---
title: Manned/Unmanned eVTOL Aircraft (Skypad)
description: DARPA-funded project to develop a dual-purpose, optionally-manned, eVTOL aircraft.
date: 2025-12-01 00:00:00 -0600
image:
  path: /assets/img/posts/2025-12-01-skypad-project-v/project-v-hexacopter.png
tags: [mechanical, hardware, firmware, software, aviation]
---

Skypad's manned/unmanned eVTOL aircraft is an initiative to develop a dual-purpose electric vertical takeoff and landing (eVTOL) system capable of operating with or without a human pilot onboard. Backed by DARPA funding during its active phase, the project explored how a single platform could bridge the gap between traditional drones and fully manned aircraft—unlocking new capabilities in mobility, logistics, and mission flexibility.

{% include embed/youtube.html id='CD70HsTUur8' %}

My role focused on system integration and early-stage flight development. I contributed to assembling multiple prototypes, integrating MOS hardware directly into the vehicle, and working on the flight control and electronics stack. This included hands-on involvement with flight controllers, ESCs, battery management systems, telemetry pipelines, and pilot control interfaces. I also participated in initial tuning and tethered flight tests as the system matured.

The project evolved through several airframe designs. Early prototypes included an experimental jetpack-style configuration, followed by a ducted bicopter that became our first manned test platform. That system successfully achieved controlled, tethered liftoff with a pilot onboard. The final iteration moved toward a more stable quadcopter configuration, where the pilot sits within a central frame supported by four large motors. This design ultimately enabled repeated manned flight demonstrations under controlled conditions.

![](/assets/img/posts/2025-12-01-skypad-project-v/project-v-bicopter.jpg)
_Prototype 2: Ducted bicopter._

Development was highly iterative and grounded in safety. Initial testing took place in a constrained environment—a tethered rig inside a reinforced enclosure—to build confidence in the system before introducing human pilots. Even during manned operation, strict limits were enforced, including low-altitude flight and active safety crews on standby. Redundancy and failure mitigation were constant considerations, particularly given the risks inherent in human-carrying electric propulsion systems.

Power delivery and reliability proved to be some of the most challenging aspects. High-current battery systems, BMS behavior under load, and ESC reliability all introduced failure modes that required careful testing and mitigation. These constraints shaped both the hardware architecture and operational procedures, reinforcing the importance of robust electrical design in addition to flight control stability.

Although the project is currently paused following the conclusion of its initial funding phase, it established a viable foundation for future development. The long-term vision is a flexible platform that can transition seamlessly between autonomous and piloted operation. This opens the door to applications ranging from search and rescue to logistics—imagine deploying the vehicle autonomously to a location, then piloting it manually for extraction or transport.

This project represents an exploration into a new class of vehicles: systems that are not strictly drones or aircraft, but something in between—designed to extend human capability while maintaining the option for full autonomy.

{% include embed/youtube.html id='AQwCscMUL2Y' %}
