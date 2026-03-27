---
title: Short Film Pyrotechnics
description: A film project requires real engineering to produce safe, practical pyrotechnics.
date: 2026-01-01 00:00:00 -0600
image:
  path: /assets/img/posts/2026-01-01-short-film-pyrotechnics/pyro-front.jpg
tags: [mechanical, hardware]
---

For an unreleased short film set in a Monty Python-esque Soviet-era backdrop, I was tasked with creating a practical effect for a malfunctioning computer terminal. The scene called for a convincing electrical short—liquid spills across the machine, followed by sparks, smoke, and visible component failure. With a limited budget and no access to licensed pyrotechnics, the challenge became: how do you safely recreate that effect using real, controllable hardware?

The core idea came from an earlier lab experience where an overvolted component failed dramatically. That failure mode—heat, smoke, and a sharp pop—felt like a close analog to what we needed on screen. From there, I experimented with deliberately overdriving resistors using standard 120V AC. Through testing, I found that 1kΩ resistors consistently produced the most visually convincing results: glowing, arcing, smoking, and occasionally popping in a way that reads well on camera.

To make this usable on set, I designed a dedicated switching system to control and distribute the effect safely. The device takes a standard AC input and routes it through a two-stage activation system: a master enable toggle and a momentary push-button trigger. This ensures the system can never be left energized unintentionally. The output is distributed across four independent channels, each capable of driving a resistor “effect node” placed throughout the prop—keyboard, monitor, and internal chassis.

![](/assets/img/posts/2026-01-01-short-film-pyrotechnics/pyro-back.jpg)
_The backside of the detonator box, showing the inputs and outputs._

Each node is designed to be quickly reloadable. Resistors are mounted into compact connectors that minimize exposed conductors while allowing rapid replacement between takes. Wiring is routed through the prop itself, with connectors selected and insulated to prevent accidental contact. The system is intentionally designed so that activation requires deliberate input, and any energized components are either enclosed or momentary by design.

A significant portion of development went into tuning the effect. Resistor values that were too large would fail slowly with little visual payoff, while smaller values would burn out instantly with no visible arc. Hitting the right balance was critical to achieving a repeatable, camera-friendly effect. Bench testing confirmed consistent performance, and early camera tests showed a convincing simulation of electrical failure.

This project sits at the intersection of electronics, safety engineering, and practical effects—taking a real physical phenomenon and shaping it into something controllable, repeatable, and visually compelling for film.

{% include embed/youtube.html id='d_7fyoGsmfk' %}

{% include embed/youtube.html id='ZjGhcyicB04' %}
