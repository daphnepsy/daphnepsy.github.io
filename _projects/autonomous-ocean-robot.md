---
title: Autonomous Ocean Robot
period: Spring 2019
order: 2
image: assets/images/weatherstation.JPG
summary: For an engineering class, my team and I built a robot that could navigate autonomously to gather data about wind speed and current speed near-shore, in order to quantify the effects of one on the other.
---
<p align="center">
  <img height="300" src="{{ '/assets/images/weatherstation.JPG' | relative_url }}" alt="Weather station on the ocean robot">
  <img height="300" src="{{ '/assets/images/aor_overhead.JPG' | relative_url }}" alt="Ocean robot from above">
</p>

For an experimental engineering class, my team of 4 built an autonomous ocean robot to determine the wind-current relationship near shore. We implemented PD control to have robot navigate autonomously to different waypoints and hold its position within a 1m radius of a waypoint, while gathering data in turbulent conditions. We also designed sensor mounts that could rotate to track the heading of a weather vane using Python and Arduino.

{% include pdf.html file="assets/files/e80report.pdf" width="600" height="600" %}
