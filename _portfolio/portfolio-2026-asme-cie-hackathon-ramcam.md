---
title: "ASME IDETC/CIE 2026 Hackathon 1st Place - From CAD to Automated CNC Programming: Five Methods on MachinePlan-10K"
excerpt: "Team RamCAM's entry to the Siemens Foundational Technologies problem: five methods that go from a design B-Rep to a machining program - three developed for this work (MixMash, a diffusion-based method, and CAMCorrector) and two re-implemented from the literature (DeepMS, MP-GFormer) - plus a generator for a new dataset of end-to-end 2.5-axis and 5-axis (2.5+2) CAM programs and two software stacks for inspecting the data and the pipeline"
advisor: ""
video: "https://youtu.be/afMHvAYO5ms"
video_show: false
video_thumbnail: ""
slides: ""
slide_show: false
slide_thumbnail: ""
poster: "/images/ASME_IDETC_2026_Hackathon.png"
publication: ""
github: ""
project_link: "https://event.asme.org/IDETC-CIE"
scholarurl: ""
selected: true
collection: portfolio
date: 2026-08-23
keyword: "Artificial Intelligence, Advanced Manufacturing, CAD/CAM"
---

Team **RamCAM** (H. Sinan Bank, Colorado State University) won **1st Place** at the [ASME IDETC/CIE 2026 Hackathon](https://event.asme.org/IDETC-CIE), *AI for Integrated Design-to-Manufacturing*, hosted by the Computer and Information in Engineering Division of ASME, with this entry to the **Siemens Foundational Technologies** problem. The hackathon ran virtually from **August 13-22, 2026**, with the in-person closing event on **August 23, 2026** at the Hilton Houston, alongside **IDETC/CIE 2026 (August 23-26, 2026)**. A three-minute summary of the entry is on [YouTube](https://youtu.be/afMHvAYO5ms).

## The Problem

The Siemens track asked for AI-driven workflows for **automated CNC machining planning**: operation sequencing, tool selection, cutting parameters, toolpath generation, and reasoning about evolving part geometry. Solutions were evaluated on [MachinePlan-10K](https://doi.org/10.5281/zenodo.21653081) - 10,000 milled parts, each with a design B-Rep, the blank, and, per operation, an NX report, an in-process workpiece (IPW) mesh, and NC code. All five methods below share one dataset parser, one 8,000/2,000 train-test split, and the organizers' scorer, so the tiers (Easy, Medium, Hard A, Hard B) are directly comparable across methods.

## Five Methods, One Harness

Three methods were developed for this work and two published architectures were re-implemented on the same B-Rep input:

- **MixMash** *(this work)* - instances before sequence. A face-instance segmentation over the B-Rep adjacency graph feeds an autoregressive transformer decoder with an instance pointer, predicting the operation sequence and the tool per operation.
- **Diffusion-based method** *(this work)* - a latent model of the plan: a plan autoencoder with a part-conditioned latent and a count head, with a guided latent prior as a second arm.
- **CAMCorrector** *(this work)* - a geometry-only, STEP-only rule-based planner with no learning: delta-volume decomposition, tool rules over the 431-tool deck, and cutter-location toolpaths that emit an IPW chain and NC code.
- **DeepMS** *(re-implemented)* - unordered B-Rep face tokens through a set transformer to a single latent, decoded non-autoregressively into slots.
- **MP-GFormer** *(re-implemented)* - design graph plus process graphs with graph attention, temporal encoding, and cross-attention into a transformer decoder.

Each method is scored on the same held-out parts and on the organizers' released test set, from the STEP alone, with refused parts scoring zero.

## Additional Contributions

- **A dataset generation method.** A procedure for producing a new dataset of **end-to-end 2.5-axis and 5-axis (2.5+2) CAM programs**, to test the methods beyond the generated blocks of MachinePlan-10K.
- **Two software stacks.** One for **inspecting the dataset** - a part browser with renders, operations, and tools, an NC-code simulation view on the IPW, and a sequence analyzer - and one for **running and inspecting the pipeline**, which walks a single part through every stage of a method.

## Release

The five methods, the dataset generator, and both software stacks will be released with the associated papers, in preparation with N. Bircan Bugdayci (Michigan State University, College of Engineering) and, we hope, together with the Siemens organizers.

## Acknowledgments

Thanks to the organizers and judges - **Gaurav Ameta** (Siemens), **Hyunwoong Ko** (Arizona State University), and **Athul Chakkithara Dharmarajan** (Purdue University) - for the problem, the data, and the feedback, and to the other finalist teams in this track, Lakefront Trail (Hyunwoo Kwon, Northwestern University) and MSUME (Charlie LaBelle and Kaeden Palmitier, Michigan State University). MachinePlan-10K is by A. C. Dharmarajan, K. Arvanitis, and G. Ameta (Zenodo [10.5281/zenodo.21653081](https://doi.org/10.5281/zenodo.21653081), CC BY 4.0, NSF 2229260). Compute was provided by the CSU Walter Scott, Jr. College of Engineering SAIDIE cluster alongside our [GPU Workstations](https://github.com/bankh/GPU_Compute).

## References

- J. Maqueda, D. W. Rosen, S. N. Melkote. *DeepMS: A data-driven approach to machining process sequencing using transformers.* Journal of Manufacturing Systems 82 (2025) 947-963. [doi:10.1016/j.jmsy.2025.07.022](https://doi.org/10.1016/j.jmsy.2025.07.022)
- F. Elhambakhsh, G. Ameta, A. Roy, H. Ko. *MP-GFormer: A 3D-geometry-aware dynamic graph transformer approach for machining process planning.* [arXiv:2511.11837](https://arxiv.org/abs/2511.11837) (2025)
- A. C. Dharmarajan, K. Arvanitis, G. Ameta. *MachinePlan-10K.* Zenodo, [doi:10.5281/zenodo.21653081](https://doi.org/10.5281/zenodo.21653081) (2026), CC BY 4.0
