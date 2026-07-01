---
title: "OpenDigitizer - Open Chart/Plot Data Extraction with a Pluggable CV/AI Framework"
excerpt: "Browser-based tool for extracting numerical data from images of charts and plots, with an open, pluggable computer-vision/AI extraction layer and a keyboard-first digitizing workflow"
poster: "/images/opendigitizer.png"
advisor: ""
video: ""
video_show: false
video_thumbnail: ""
slides: ""
slide_show: false
slide_thumbnail: ""
publication: ""
github: "https://github.com/bankh/OpenDigitizer"
project_link: "https://bankh.github.io/OpenDigitizer/"
scholarurl: ""
selected: false
collection: portfolio
date: 2026-06-30
keyword: "Software Engineering, Research Tools"
---

## Project Overview

**OpenDigitizer** is a browser-based tool for extracting numerical data from images of charts and plots. It is an open fork of [WebPlotDigitizer](https://github.com/automeris-io/WebPlotDigitizer) by Ankit Rohatgi, distributed under **AGPL-3.0** (independent project, not affiliated with or endorsed by Automeris LLC). The fork adds an **open, pluggable computer-vision / AI extraction framework** and a **keyboard-first digitizing workflow**, and was built to support figure-based data recovery for the residual-stress visual data extraction work.

## Highlights

- **Open CV/AI extraction framework.** New detectors register themselves and appear in the *Automatic Extraction → Algorithm* dropdown. Detection can run in **pure JS**, **in-browser WASM** (e.g. ONNX Runtime / TensorFlow.js), or your **own remote Python service** — no closed cloud dependency.
- **Keyboard-first digitizing.** Press **`K`**, then arrow keys move a crosshair (**Shift** = faster), **`A`** adds, **`D`** deletes, **`S`** grabs & moves a point, and **`Z`/`C`** jump between points. The magnifier and live coordinate readout follow the crosshair.
- **Multi-select & one-shot delete** with additive selection (Shift/Ctrl-click, Shift-drag), plus **point-level Undo/Redo** (`Ctrl+Z` / `Ctrl+Y`).
- **Folder / thumbnail browser.** Open a whole folder of images; hover a thumbnail for a large preview, click to switch.
- **Flexible masking.** Freehand Pen/Erase, a keyboard brush, and click-to-click polygon/polyline masks with numeric brush width.

## Core Capabilities

- **Chart / axis types:** XY, polar, ternary, bar, map, image, and circular chart recorder.
- **Extraction:** manual point placement and automatic color-mask + algorithm detection.
- **Measurements:** distance, angle, area / perimeter.
- **Export:** CSV, clipboard, and Plotly, with save/resume of projects.

## Notes

The fork preserves the original AGPL-3.0 license and Ankit Rohatgi's copyright; all additions are marked with `OpenDigitizer:` comments in the source. The new detector interface and data contract — with JS, WASM, and Python recipes plus a reference FastAPI server — are documented in `docs/EXTENDING-CV-AI.md`.
