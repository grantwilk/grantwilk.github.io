---
title: Bus Route Editor App
description: A GUI application for creating and editing public transportation routes.
date: 2020-05-01 00:00:00 -0600
image:
  path: /assets/img/posts/2020-05-01-bus-route-editor\bus-route-editor-screenshot.jpg
tags: [software]
---

### Software Tools and Practices Project

In my Software Tools and Practices course, I formed a team with a few other students to implement a Java-based application used to view and edit General Transit Feed Specification (GTFS) files, a file standard used by Google for logging transportation information.

Personally, I took a lead in data structure design, class organization, GUI design, and GUI implementation.

![](/assets/img/posts/2020-05-01-bus-route-editor/bus-route-editor-architecture.jpg)
_The software architecture of the editor._

![](/assets/img/posts/2020-05-01-bus-route-editor/bus-route-editor-gui-design.jpg)
_Our group's approach to UI/UX design for the application._

![](/assets/img/posts/2020-05-01-bus-route-editor/bus-route-editor-modular-ui.jpg)
_The modular UI system I created._

### Results

Using assorted software tools, including diagramming software, version control, and IDEs combined with strategic planning activities like diagramming, developing user stories, and taking time to experiment with GUI design, we were able to complete the project.

My favorite part of working on this project was using JavaFX to make modular GUI components. This was key in maintaining a clean-looking GUI while also being able to scale to the magnitude of the GTFS files we were working with.

The final application can be downloaded [here](https://github.com/grantwilk/se2030_gtfs_editor/releases/download/final/se2030_gtfs_editor_final.jar), and some sample GTFS files can be found [here](https://github.com/grantwilk/se2030_gtfs_editor/tree/final/samples/full-samples).