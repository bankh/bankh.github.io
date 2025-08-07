---
title: "Method for dynamic multi-dimensional spatio-temporal human-machine interaction and feedback"
collection: publications
permalink: /publication/2024-Patent-Spatial-Interaction
excerpt: 'U.S. Patent for spatio-temporal human-machine interaction by Bank and Little, granted December 2024.'
date: 2024-12-03
type: 'Patent'
venue: 'USPTO'
patent_number: 'US12157235B2'
application_number: 'US17/606,535'
filing_date: '2019-05-31'
priority_date: '2019-05-31'
inventors: 'Bank, H. S., & Little, M'
assignee: 'Siemens AG'
paperurl: 'https://patents.google.com/patent/US12157235B2/en'
scholarurl: 'https://scholar.google.com/citations?view_op=view_citation&hl=en&user=vU6oBhwAAAAJ&citation_for_view=vU6oBhwAAAAJ:zA6iFVUQeVQC'
citation: '@misc{bank2024method,
  title={Method for dynamic multi-dimensional spatio-temporal human machine interaction and feedback},
  author={Bank, Hasan Sinan and Little, Michael},
  year={2024},
  month=dec # "~3",
  publisher={Google Patents},
  note={US Patent 12,157,235}
}'
---

## 📌 Overview

This patent, filed by Siemens and granted on **December 3, 2024**, describes a system and method enabling **bi‑directional communication** between industrial machines and humans in automated manufacturing environments. It projects real-time interaction intent and future motion cues using visual, audio, thermal, or haptic carriers to enhance safety and clarity during collaboration ([European Publication Server][1]).

---

## Core Innovation

1. **Interaction Reasoning Layer**

   * Combines perception of human presence with machine task and state information to reason about imminent and near-future interactions.
   * Generates two types of “images”: an **interaction image** for the immediate machine action zone and a **foreshadowing image** for upcoming actions ([European Publication Server][1]).

2. **Multi‑Domain Projection System**

   * Visual, audible, tactile, or temperature-based projections convey real‑time machine intent.
   * Projectors or wearable devices display distinct interaction and foreshadowing cues with differentiating attributes (e.g., color, intensity, timing) ([European Publication Server][1]).

3. **Programmable Output Detector**

   * Captures encoded data embedded in projected images.
   * Translates that into machine-readable messages, optionally delivering via networks or wearable devices to guide human response ([European Publication Server][1]).

---

## Technical Highlights

* **System Components**:

  * Cyber‑mechanical system with machine, controller, task planner, perception sensors, and projection hardware.
  * Interaction reasoner that fuses human proximity, environment, and task context to generate guidance outputs ([European Publication Server][1]).

* **Method Flow**:

  1. Define high-level goals and split into tasks.
  2. Sense environment and human presence.
  3. Identify imminent interactions.
  4. Create interaction and foreshadowing projections.
  5. Detect outputs with programmable devices and relay encoded information to humans via communication channels ([European Publication Server][1]).

* **Customization**:

  * Visual cues tailored by human identity or skill level.
  * Adjustable output modalities for accessibility (e.g. colorblind-friendly alternatives, stronger signals for novices) ([European Publication Server][1]).

---

## Benefits & Use Cases

* **Enhanced Safety**: Humans receive cues before hazardous motion, reducing reliance solely on machine-side avoidance or proximity detection.
* **Improved Collaboration**: Transparent machine intent fosters trust and smoother hand‑offs in tasks like shared assembly or material transfer.
* **Psychological Comfort**: Workers feel informed and anticipatory about machine actions, reducing stress and ambiguity.
* **Adaptive Display**: Scalable for multi-robot settings, overlapping projections, and personalized human-machine pairing ([European Publication Server][1]).

---

## TL;DP Summary Table

| Element                  | Description                                                                    |
| ------------------------ | ------------------------------------------------------------------------------ |
| **Goal**                 | Enable **machine‑to‑human feedback** in industrial HRI \\                      |
| **Mechanism**            | Interaction + foreshadowing “images” in visual/audio/haptic/thermal domains \\ |
| **Detection & Encoding** | Embedded info captured by detectors, delivered via network or wearables \\     |
| **Adaptability**         | Contextual, personalized to user skill and identity \\                         |
| **Outcome**              | Safer, more coordinated human‑machine workflows                                |

---

[1]: https://data.epo.org/publication-server/rest/v1.2/publication-dates/2024-08-21/patents/EP3959045NWB1/document.pdf.com "[PDF] EP003959045B1* - EP 3 959 045 B1 - European Patent Office"
