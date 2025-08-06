---
title: "SimpleFOC: A Field Oriented Control (FOC) Library for Controlling Brushless Direct Current (BLDC) and Stepper Motors"
collection: publications
permalink: /publication/2022-JOSS-SimpleFOC
excerpt: 'This paper presents SimpleFOC, an open-source library for field oriented control of BLDC and stepper motors.'
date: 2022-06-01
type: 'Journal'
venue: 'Journal of Open Source Software'
volume: '7'
number: '74'
pages: '4232'
github: 'https://github.com/simplefoc'
video: 'https://www.youtube.com/@theskura/videos'
authors: 'Skuric, A., Bank, H. S., Unger, R., Williams, O., & González-Reyes, D.'
paperurl: 'https://joss.theoj.org/papers/10.21105/joss.04232'
citation: '@article{skuric2022simplefoc,
  title={SimpleFOC: a field oriented control (FOC) library for controlling brushless direct current (BLDC) and stepper motors},
  author={Skuric, Antun and Bank, Hasan Sinan and Unger, Richard and Williams, Owen and Gonzalez-Reyes, David},
  journal={Journal of Open Source Software},
  volume={7},
  number={74},
  pages={4232},
  year={2022}
}'
---

## 📌 Overview

We present **SimpleFOC**, a C++ library implementing **Field‑Oriented Control (FOC)** for brushless DC (BLDC) and stepper motors, aiming to be both **generic** and **cross‑platform** ([Open Journals][1]).

---

## Why It Matters

FOC is highly efficient for controlling electrically commutated motors but demands complex computations. Most existing implementations are tightly coupled to specific microcontrollers or hardware stacks ([Open Journals][1]). SimpleFOC fills that gap by offering a flexible, modular, platform‑agnostic approach.

---

## Key Features

* **Portable across hardware**: supports Atmega, STM32, ESP32, RP2040, Teensy, Portenta, and platforms like Arduino UNO, Nucleo, etc. ([Open Journals][1]).
* **Logical architecture**: divides the system into modular blocks—motor, driver, sensors, microcontroller, UI—enabling easier swapping and reconfiguration ([Open Journals][1]).
* **C++ object‑oriented design**: encapsulates FOC routines, motion control, hardware interfaces, and configurations with intuitive APIs ([Open Journals][1]).
* **Community‑driven**: >250 GitHub forks, 600+ members engaged in discussions, and 10,000+ posts in its community platform as of mid‑2022 ([Open Journals][1]).

---

## Core Value

SimpleFOC aims to **democratize advanced motor control**. It removes hardware vendor lock‑in, facilitating rapid experimentation and teaching in robotics, dynamic control systems, and embedded motion applications.

---

### 🔍 TL;DP Summary

| Aspect                 | Detail                                                                        |
| ---------------------- | ----------------------------------------------------------------------------- |
| **Purpose**            | Provide a cross‑platform FOC library usable across many MCU boards            |
| **Technical design**   | Modular C++ architecture with abstracted motor, driver, and sensor interfaces |
| **Supported hardware** | Arduino, ESP32, STM32, RP2040, Teensy, Nucleo, Atmega and more                |
| **Community standing** | Active development and adoption in academic and hobbyist projects             |
| **Publication**        | Published June 25, 2022 in JOSS (DOI: 10.21105/joss.04232)                    |

---

[1]: https://www.theoj.org/joss-papers/joss.04232/10.21105.joss.04232.pdf?utm_source=chatgpt.com "[PDF] SimpleFOC: A Field Oriented Control (FOC) Library ... - Open Journals"
