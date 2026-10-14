---
layout: research-project
title: VoiceMorph
description: A real-time voice transformation system for studying auditory self-recognition.
importance: 3
category: research
# img: assets/img/research-voicemorph.png

period: "May–September 2025"
institution: "MIT Media Lab · Fluid Interfaces"
people: "Advisor: Pattie Maes"
contribution: "Built the real-time experimental interface in TouchDesigner and analyzed participants’ perceptions of transformed voice identity."
paper_url: "https://arxiv.org/abs/2510.16192"
---

<div class="project-context">
  May–September 2025 · Research Intern<br>
  MIT Media Lab · Fluid Interfaces<br>
  With Professor Pattie Maes and master student Kye Shimizu
</div>

## Overview

How much can a voice change before it stops feeling like your own? VoiceMorph investigated auditory self-recognition by gradually blending participants’ cloned voices with another speaker’s voice.

## Research question

We examined where self-recognition breaks down, how acoustic differences relate to recognition judgments and response times, and which cues people use to identify their own voice.

## System and study

Using Cartesia, we interpolated voice embeddings at 1% increments between each participant and a demographically matched target speaker.

In an in-person study with 21 participants, listeners rated how much each voice sounded like themselves. We recorded response times and conducted follow-up interviews about recognition strategies and reactions to voice manipulation.

## My contribution

- Built the real-time experimental interface in TouchDesigner around the voice-morphing model.
- Automated stimulus presentation and response capture across more than 2,000 trials.
- Analyzed recognition ratings, response times, and individual differences.
- Led acoustic quality control using UTMOSv2 and supported demographic matching of target voices.
- Synthesized quantitative results and qualitative findings.

## Key findings

- The estimated group-level recognition boundary was 35.2% morphing, with substantial individual variation.
- Larger embedding distances were associated with slower judgments, but did not reliably predict recognition thresholds.
- Participants described intonation, rhythm, and word emphasis as important identity cues.

## Design implications

Personalized synthetic voices need to preserve recognizable speaking patterns as well as vocal similarity. These preliminary findings inform voice customization and assistive communication; broader validation requires larger, more diverse studies.

## Publication

**VoiceMorph: How AI Voice Morphing Reveals the Boundaries of Auditory Self-Recognition**

Kye Shimizu, Minghan Gao, Ananya Ganesh, and Pattie Maes.

[Read the preprint](https://arxiv.org/abs/2510.16192)