---
title: "CatalogBank: A Structured and Interoperable Catalog Dataset with a Semi-Automatic Annotation Tool DocumentLabeler for Engineering System Design"
collection: publications
permalink: /publication/2024-Conference-ACM-CatalogBank
excerpt: 'This paper presents CatalogBank, a structured dataset and annotation tool for engineering system design, nominated for Best Paper Award.'
date: 2024-08-01
type: 'Conference'
venue: 'Proceedings of the ACM Symposium on Document Engineering 2024'
location: 'San Jose, CA'
pages: '1-9'
month: 'August'
publisher: 'ACM'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3685650.3685665'
data: 'https://github.com/bankh/catalogbank'
github: 'https://github.com/bankh/DocumentLabeler'
presentation: ''
video: 'https://www.youtube.com/watch?v=d5_FFa2ElMo'
note: 'Nominated for Best Paper Award'
authors: 'Bank, H. S., & Herber, D. R'
citation: '@inproceedings{bank2024catalogbank,
  title={CatalogBank: A Structured and Interoperable Catalog Dataset with a Semi-Automatic Annotation Tool (DocumentLabeler) for Engineering System Design},
  author={Bank, Hasan Sinan and Herber, Daniel R},
  booktitle={Proceedings of the ACM Symposium on Document Engineering 2024},
  pages={1--9},
  year={2024}
}'
---

## 📌 Overview

**CatalogBank: A Structured and Interoperable Catalog Dataset with a Semi‑Automatic Annotation Tool (DocumentLabeler) for Engineering System Design** was presented at **DocEng ’24** (ACM Symposium on Document Engineering) in **August 2024**. Authored by **Hasan Sinan Bank** (Craftnetics Inc.) and **Daniel R. Herber** (Colorado State University) ([ResearchGate][1]). It was nominated for Best Paper Award ([Colorado State University Engineering][2]).

---

## Objective

This work introduces **CatalogBank**, a dataset designed to connect **textual engineering catalogs** with structured, interoperable metadata. It targets improved automation in engineering workflows and downstream NLP tasks like layout analysis and knowledge extraction ([GitHub][3]).

---

## Core Contributions

### 1. **CatalogBank Dataset**

* A collection of diverse **PDF-based catalogs** from engineering vendors (e.g. Thorlabs, McMaster‑Carr).
* Extracts structured information from catalogs such as product specifications, images, tables, and layout elements ([GitHub][3], [ResearchGate][1]).
* Facilitates bridging of modalities: text, geometry, images, and graph-format data.

### 2. **DocumentLabeler Tool**

* An open‑source, semi‑automatic annotation tool tailored for engineering documents.
* Speeds annotation by combining automation and human review to generate structured labels from PDF layout ([GitHub][3]).

### 3. **Interoperability & Standardization**

* Creates unified schema and metadata model to enable consistent extraction and downstream integration.
* Helps overcome challenges posed by non‑standard PDF catalog formats and manual entry bottlenecks.

---

## Significance & Benefits

* **Enables automation** in engineering design workflows by providing structured, labeled data from catalogs.
* Supports **layout analysis** and **information extraction** in Document Engineering and NLP pipelines.
* Contributes a **robust benchmark dataset** for training and evaluating models on catalog-style documents ([ResearchGate][1]).

---

## TL;DP Summary Table

| Element       | Description                                                             |
| ------------- | ----------------------------------------------------------------------- |
| **Title**     | CatalogBank dataset with DocumentLabeler tool                           |
| **Event**     | ACM DocEng ’24 (August 2024)                                            |
| **Authors**   | Hasan Sinan Bank & Daniel R. Herber                                     |
| **Goal**      | Structure textual catalogs into interoperable data formats              |
| **Mechanism** | PDF parsing, semi-automated annotation, metadata schema standardization |
| **Tools**     | CatalogBank dataset + DocumentLabeler annotation tool                   |
| **Use Cases** | NLP layout analysis, engineering design automation, dataset benchmarks  |

[1]: https://www.researchgate.net/publication/384113961_CatalogBank_A_Structured_and_Interoperable_Catalog_Dataset_with_a_Semi-Automatic_Annotation_Tool_DocumentLabeler_for_Engineering_System_Design.com "CatalogBank: A Structured and Interoperable Catalog Dataset with a ..."
[2]: https://www.engr.colostate.edu/~drherber/publications.php.com "Publications - Herber@CSU"
[3]: https://github.com/bankh/CatalogBank.com "Part I- CatalogBank: A Structured and Interoperable Catalog Dataset ..."
