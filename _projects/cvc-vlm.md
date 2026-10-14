---
layout: research-project
title: Egocentric VLMs for surgical feedback
description: Evidence-grounded assessment and corrective feedback for central venous catheterization.
importance: 1
category: research
# img: assets/img/research-cvc.jpg

period: "September 2026–present"
institution: "Carnegie Mellon University"
people: "Advisor: Justin Chan"
contribution: "Developing video-analysis pipelines and evaluating vision-language models for procedural understanding, performance assessment, and corrective feedback."
---
<div class="project-context">
  September 2026–present · Independent Research<br>
  Carnegie Mellon University<br>
  Advisor: Justin Chan
</div>

## Overview

This ongoing project investigates whether vision-language models can interpret head-mounted video of central venous catheterization (CVC) to support procedural understanding, performance assessment, and corrective feedback.

We are beginning with simulated procedures performed on mannequins, examining how models interpret tools, actions, and procedural transitions from the operator’s perspective.

## Inspiration and research direction

The project draws inspiration from LabOS and its vision of AI assistance grounded in observations of physical workflows. This motivates our exploration of how visual observations can be connected to procedural knowledge to support a person carrying out a complex task.

Our focus is on clinical skills training: recognizing the current step is useful, but meaningful assistance also requires understanding how an action is performed, what evidence supports an assessment, and when the model lacks enough information to judge.

## Research questions

- How accurately can general-purpose VLMs identify procedural steps, active tools, and visible actions in egocentric CVC videos?
- Can procedural references improve recognition of step transitions and interpretation of performance?
- How can assessments and corrective feedback be tied to specific video evidence?
- When should a model express uncertainty or defer to expert review?

## Current approach

I am evaluating zero-shot and reference-guided VLM prompting on simulated CVC videos. The tasks range from scene description and step-boundary identification to identifying observable issues and explaining their supporting evidence.

The evaluation compares predictions with expert annotations and assessment criteria, with particular attention to temporal precision, visibility limitations, and consistency across operators.

A longer-term direction is to combine fine-grained visual evidence with a structured representation of the procedure, helping distinguish expected variation from deviations that warrant review.

## My contribution

- Reviewing related work on AI task assistance, surgical workflow recognition, and clinical performance assessment.
- Building video-processing and VLM inference pipelines for egocentric procedure footage.
- Designing prompts and comparisons across procedural-understanding and assessment tasks.
- Investigating expert annotation schemes for step boundaries, performance criteria, and supporting events.

## Why egocentric video?

Head-mounted cameras capture the procedure from the operator’s viewpoint, offering a potential route to assistance without a fixed external camera setup.

This perspective also introduces motion blur, occlusion, changing tool distance, and limited views of anatomy. The project examines what can be assessed reliably from these observations and what requires additional evidence.

## Status

This work is ongoing. Current efforts focus on baseline evaluation and expert-grounded annotation; performance-assessment and corrective-feedback capabilities remain research goals.