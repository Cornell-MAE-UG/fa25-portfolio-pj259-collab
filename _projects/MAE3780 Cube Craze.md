---
layout: project
title: MAE3780 Cube Craze
description: Class project
technologies: [Arduino, C++, 3D Printing]
image: /assets/images/MAE3780_robot.jpg
---
In this project, we designed and built an autonomous robot for the Cube Craze competition in MAE3780. The robot uses a wide U-shaped 3D-printed plow with a servo-driven pipe cleaner brush to capture and retain 1-inch wooden cubes, pushing them across the midline onto the opponent's side. A TCS3200 color sensor reads the floor color to navigate—driving straight to the midline, then sweeping laterally back and forth until the match ends. Our robot went 5-1-1 in competition.

The biggest technical challenge was getting reliable color sensing. We learned that pulseIn() fails for signals at the extremes of its timing range, and that counting pulse edges in a fixed window is far more robust. We also learned the value of keeping control logic simple—our best-performing code was a basic two-phase state machine, and every attempt to add complexity introduced more failure modes than it solved. On the mechanical side, the plow and brush won us more matches than any software ever could have, reinforcing that good hardware design is just as important as good code.

[Read the full report]({{ "/assets/MAE3780_Final_Report.pdf" | relative_url }}) in PDF format.
