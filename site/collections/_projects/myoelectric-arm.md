---
date: 2021-01-05 05:20:35 +0300
title: Myoelectric Arm
subtitle: Mechanical, Electrical
image: "/images/myoelectricarm.jpg"
---

8/3/24

I sought to create a myoelectric bionic arm that was cost-effective (comparable to its expensive counterparts on the market) and capable of performing basic gestures.

## Objectives

- EMG controllers
- Perform basic gestures including fist, pencil, pinch, peace, thumbs up/down
- Less than $500
- Wrist rotation
- Pressure feedback?
- Custom design PCB

## Materials

- [ ] 6 MG995 servo motors
- [ ] Fishing Line
- [ ] Arduino Nano
- [ ] Myoware 2.0 Muscle Sensor
- [ ] 6 Linear Hall Effect Sensors
- [ ] Magnet
- [ ] Breadboard
- [ ] Bolts
- [ ] Screws
- [ ] Springs
- [ ] Ribbon wire

## Research

I began by first researching the design of prosthetic arms. I stumbled upon this thesis, which directed me towards InMoov. InMoov is an open-source library with 3D printed files for a life-size robot. I decided to use the design of Handi2 for my project but incorporated additional electronics to make the arm myoelectric.

## Build

I 3D printed InMoov Handi2 parts on Prusa and Bambu with White ABS. Some of the forearm components were accidentally printed with glow-in-the-dark ABS—truly a happy accident :). I then followed InMoov Handi2 assembly instructions and made several modifications to ensure everything fit together.

On the first test of the finger movements, I realized the fishing line attached to the servo was not tensioned enough, causing the fingers not to display their full range of motion when the servo was written to 180 degrees. So, I redid each pulley’s wiring, making sure they were taut.

![Palm trees](/images/image-example-3.jpg){: width="1200" height="900"}

## Electronics

Unloaded and loaded servos draw too much current to be sufficiently powered by a USB cable connected to a laptop. The stall current of an MG995 servo is 1.5 Amps. I quickly realized this after observing the servo's twitching and creating a humming noise. In these cases, when the servo and processor are running off the same power supply, the servos can draw so much current that it causes the processor to reset.

I custom-designed a PCB using Kicad that contained a servo power distribution board along with areas to mount the hall effect and EMG sensor.

![Sea](/images/image-example-4.jpg){: width="1200" height="900"}

## Results

Coming soon!
