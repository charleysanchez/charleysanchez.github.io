---
layout: demo
title: PAVAC demo
permalink: /demos/pavac/
mp4: /assets/video/PAVAC_example.mp4
poster: /assets/img/thumbs/pavac.jpg
repo: https://github.com/charleysanchez/AVPrivacy-Jetson
paper: /assets/docs/AVPrivacy_report.pdf
description: Real-time face anonymization on a Jetson Orin Nano mounted on a small rover.
---

Real-time face detection and anonymization on a Jetson Orin Nano mounted on a small rover. Faces are detected with SCRFD running under TensorRT and pixelated on the vehicle itself, and the navigation stack works from the anonymized frames. We compared the output against masks from Meta's Segment Anything Model (Dice 0.83).
