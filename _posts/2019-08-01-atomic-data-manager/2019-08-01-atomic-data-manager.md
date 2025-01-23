---
title: Atomic Data Manager
description: An enhanced data management plugin for managing Blender 3D assets more efficiently.
date: 2019-08-01 00:00:00 +0600
image:
  path: /assets/img/avatar.jpg
---

### The Problem

Blender is an open-source 3D creation suite used by artists around the world. While it accomplishes many tasks exceptionally well, its data management features desperately need an upgrade.

### The Plan

Use Blender's Python API to implement a laundry-list of new data management tools, and package them into a compact but feature-packed Blender add-on.

The Atomic Data Manager add-on should accomplish the following goals:

1. Automatically detect and remove unused data from project files with one click
2. Allow users to manually remove data via an easily navigable GUI
3. Give users the ability to see exactly where their data is being used
4. Provide detailed statistics about the data in the project files
5. Detect missing dependencies and propose solutions to replace/reload them
6. Fit everything into one compact GUI with popup GUIs for more complex tools

![](https://i0.wp.com/grantwilk.com/wp-content/uploads/2020/01/spring_panel-min.jpg?fit=880%2C1002&ssl=1)

### The Result

From the first prototype to the final release, the development of Atomic Data Manager took 22 weeks. The add-on was exclusively developed with Blender's Python API using JetBrain's PyCharm as a development environment.

All six key features were successfully implemented, and a few more minor features were added along the way.

Since its release on September 1st, 2019, Atomic has accumulated more than 1,600 downloads from Blender artists around the world.

![](https://grantwilk.com/wp-content/uploads/2019/08/spring_window_shaded-min-1024x576.jpg)

### The Future

In future versions of Atomic, I plan on implementing new features and improving existing ones. Below is the list of improvements I plan on making:

- Add support for managing camera data
- Add support for managing mesh data
- Implement functionality for searching for missing files
- Add more project data statistics

If you would like to learn more about Atomic Data Manager or try it for yourself, consider visiting Atomic's [official product page](https://remington.pro/software/blender/atomic/).