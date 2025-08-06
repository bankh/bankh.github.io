---
title: "Temporal Logic (TL)-Based Autonomy for Smart Manufacturing Systems"
collection: publications
permalink: /publication/2018-Procedia-TL-Autonomy
excerpt: 'This paper is about an implementation of temporal logic planner for smart manufacturing system.'
date: 2018-05-10
type: 'Conference'
venue: '46th NAMRC'
month: 'August'
publisher: 'SME'
location: 'College Station, TX, USA'
video: ''
paperurl: 'http://bankh.github.io/files/SME_NAMRC_46_Paper_140.pdf'
authors: Bank, H.S., Dsouza, S., & Rasam A
citation: '@article{bank2018temporal,
  title={Temporal logic (TL)-based autonomy for smart manufacturing systems},
  author={Bank, Hasan Sinan and Dsouza, Sandeep and Rasam, Aditya},
  journal={Procedia Manufacturing},
  volume={26},
  pages={1221--1229},
  year={2018},
  publisher={Elsevier}
}
'
---

## 📌 Overview

Bank, D'souza, and Rasam (2018) propose a **Linear Temporal Logic (LTL)**‑based autonomy framework for smart manufacturing systems. The framework enables intuitive, constraint‑aware task planning in automated systems without hard‑coded rules, offering flexibility and assured safety ([Procedia Manufacturing][1]).

---

## Why It Matters

Smart manufacturing systems typically rely on hard‑coded rules for task execution, making them inflexible and difficult to redeploy for different scenarios. This research addresses the need for **flexible autonomy** that can adapt to changing manufacturing requirements while maintaining formal safety guarantees.

---

## Core Innovations

* **Problem formulation via LTL**: Users express manufacturing tasks (e.g. assembly), safety rules, and resource constraints in LTL. A SAT solver synthesizes plans that satisfy all specified conditions ([Procedia Manufacturing][1]).

* **Divide‑and‑conquer in receding horizon**: To manage exponential solving times, the planning horizon is broken into smaller segments, improving scalability and enabling real‑world deployment ([Procedia Manufacturing][1]).

* **Integration with industrial tools**: The framework was validated via simulated Gantry robot tasks in Siemens NX Mechatronics Concept Designer and TIA Portal with S7‑1500 PLCs ([Procedia Manufacturing][1]).

---

## Core Value

This framework democratizes **formal methods in manufacturing** by enabling engineers to specify complex task requirements using intuitive logical specifications rather than complex programming. It provides mathematical safety guarantees while maintaining computational feasibility for industrial applications.

---

## Benefits & Applications

* **Flexible autonomy**: The system adapts to changing tasks via logical specifications instead of fixed programming, supporting swift redeployment across scenarios.
* **Scalable planning**: The receding horizon method demonstrates near-linear scaling with task size, making it computationally feasible for industrial settings.
* **Formal safety guarantees**: LTL ensures that safety constraints are mathematically enforced in generated plans.
* **Industrial validation**: Demonstrated on Siemens-connected gantry robot setup, bridging academic methods with manufacturing execution.

---

### 🔍 TL;DP Summary

| Element        | Description                                                                    |
| -------------- | ------------------------------------------------------------------------------ |
| **Goal**       | Enable flexible, automated planning in smart manufacturing using formal logic  |
| **Approach**   | LTL‑based task specification + receding‑horizon solver                         |
| **Validation** | Gantry robot simulation and Siemens PLC testbed                                |
| **Benefits**   | Flexible deployment, scalable execution, formal safety, real‑world integration |

---

Would you like to explore how this LTL-based planning compares to classical scheduling or motion planning under uncertainty?

[1]: https://bankh.github.io/files/SME_NAMRC_46_Paper_140.pdf.com "[PDF] Based Autonomy for Smart Manufacturing Systems"
