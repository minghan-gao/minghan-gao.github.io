---
layout: page
title: Low-voice recognition on a smartwatch
description: A wrist-worn ultrasonic sensing prototype for recognizing whispered commands.
importance: 2
category: project
# img: assets/img/research-voicemorph.png
---

**Role:** Hardware prototyping, data collection, and machine learning · **Period:** January–May 2025

## System

I designed a smartwatch-style whisper interface that uses active ultrasonic sensing to capture subtle articulatory motion without relying on conventional audio alone.

## What I built

- Prototyped a custom 3D-printed wrist device with dual ultrasonic speakers and microphones controlled by a Teensy 4.1.
- Collected 6,380 labeled whispered utterances from four participants across 29 command classes.
- Developed a modified four-channel ResNet-18 pipeline with transfer learning, random cropping, time-frequency masking, and Gaussian-noise augmentation.
- Achieved 55% classification accuracy with a macro F1 score of 0.56.

This project connected sensing-hardware design, signal processing, and empirical model evaluation in one end-to-end system.
