---
layout: post
title: Rubik's Cube Solver
description:  Created a high‑speed Rubik's Cube Solving Robot capable of automatically scanning and solving a Rubik's Cube in under 4 seconds
skills: 
  - ESP32
  - C++
  - Python
  - Computer Vision
  - PCB Design
  - KiCad
  - Fusion 360
  - 3D Printing

main-image: /CS_main.png
---

---
# Aim
- To build a robot capable of beating of breaking the Human Rubik's Cube average World Record (3.84 seconds)
- The robot should be able to scan a Rubik's Cube in any configuration and come up with a near-optimal solution

# Result
- The robot can solve the Rubik's Cube in an average of 3.6 seconds, achieving the target goal
- The color scanning algorithm yields a 95% success rate in differing light conditions
{% include youtube-video.html id="dNQgs1O4uOM" autoplay= "false" width= "900px" %}

# How?
## 1. Electronics
{% include image-gallery.html images="CS_pcb.jpg" height="400" %}
Final PCB

- Precision stepper motor control was achieved through the implementation of A4988 drivers, with an ESP32 microcontroller serving as the central control unit to manage all driver operations
- A seperate ESP32 CAM was used to scan the Rubik’s Cube’s faces
- Power distribution was segmented to ensure optimal performance; the control circuitry was supplied by an HW-131 breadboard power supply, while a dedicated 24V power supply was employed to drive the stepper motors
- The control system's development followed an iterative approach, commencing with breadboard prototyping for initial validation, and culminating in the design and fabrication of a custom printed circuit board to enhance reliability and integration

{% include image-gallery.html images="CS_schematic.png" height="400" %}
PCB Schematic

## 2. Software
{% include image-gallery.html images="CS_hsv_1color.png" height="400" %}
HSV Filter to determine range for HSV values

- The ESP32-CAM continuously sends images to a laptop via a webserver for analysis
- This image is then analyzed with computer vision, using HSV analysis with OpenCV in Python for color recognition, averaging the color values of the squares in a 3x3 grid to read the colors from nine facelets at once while minimizing the impact of noise from different lighting conditions
- The scramble of the cube is then put through Kociemba’s Two Phase Five Face algorithm to determine a near-optimal solution in 3 seconds
- This solution is sent to the control ESP32 to be executed via the stepper motors, taking into account backlash caused by the imperfect connections between the 3d printed adapters and the Rubik’s Cube for precise turning

{% include image-gallery.html images="CS_hsv_6color.png" height="400" %}
Color Detection Algorithm Result




