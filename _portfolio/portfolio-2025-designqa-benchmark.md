---
title: "ASME IDETC Hackathon 2025 - DesignQA: Multimodal Benchmark for Engineering Documentation Understanding"
excerpt: "A comprehensive benchmark for evaluating Large Language Models' understanding of engineering documentation through rule extraction, comprehension, and compliance tasks"
advisor: ""
video: ""
video_show: false
video_thumbnail: ""
slides: "https://github.com/bankh/design_qa_IDETC2025/blob/main/docs/bankh/slide_deck/IDETC_2025.pdf"
slide_show: false
slide_thumbnail: ""
poster: "academicpages.github.io/files/teaser.png"
publication: "2025-DesignQA-Benchmark"
github: "https://github.com/bankh/design_qa_IDETC2025"
project_link: ""
selected: true
collection: portfolio
date: 2025-08-17
keyword: "Artificial Intelligence, Benchmarking, Engineering Documentation"
---

DesignQA is a multimodal benchmark designed to evaluate Large Language Models' (LLMs) understanding of engineering documentation, specifically focusing on Formula SAE (FSAE) competition rules. This benchmark addresses the critical need for AI systems to comprehend complex technical specifications and regulatory requirements in engineering contexts.

## Problem Statement

Engineering documentation presents unique challenges for AI systems:
- Complex technical terminology and domain-specific language
- Multi-modal content combining text, diagrams, and CAD models
- Hierarchical rule structures with interdependencies
- Need for precise compliance verification
- Limited existing benchmarks for engineering documentation understanding

## Solution

The DesignQA benchmark provides a comprehensive evaluation framework with three main categories:

### Rule Extraction
- **Retrieval QAs**: Extract specific rules from documentation
- **Compilation QAs**: Identify all rules relevant to specific terms or concepts

### Rule Comprehension  
- **Definition QAs**: Identify components highlighted in multi-view CAD images
- **Presence QAs**: Determine component presence in detailed CAD views

### Rule Compliance
- **Dimension QAs**: Verify dimensional constraint compliance
- **Functional Performance QAs**: Assess functional performance requirements

## Technical Implementation

The benchmark includes:
- **Multimodal Dataset**: Text-based rules combined with CAD images and diagrams
- **Structured Evaluation**: Automated metrics for each benchmark category
- **Comprehensive Coverage**: 1,000+ question-answer pairs across all categories
- **Real-world Context**: Based on actual FSAE competition rules and vehicle designs

## Impact

DesignQA serves as:
- **Research Tool**: Enables evaluation of LLM capabilities in engineering domains
- **Development Guide**: Provides insights for improving AI systems' technical comprehension
- **Industry Benchmark**: Establishes standards for engineering documentation AI
- **Educational Resource**: Supports AI education in engineering contexts

The benchmark has been accepted as an IDETC 2025 hackathon problem, demonstrating its relevance to the engineering design community and potential for advancing AI capabilities in technical documentation understanding.
