# PLC-Spec-Syn: Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)

This repository contains the official dataset and resources for the ICLR 2026 submission, "**Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale**."

[cite_start]Our work introduces `PLC-Spec-Syn`, a novel framework for generating high-fidelity instruction-code pairs for Programmable Logic Controller (PLC) programming[cite: 213]. [cite_start]To address the critical scarcity of verified data in the industrial control domain, we employ a principled evolutionary process guided by real-world engineering standards[cite: 215]. [cite_start]This process has produced `PLC-Spec-Code`, the first large-scale, formally verified corpus of its kind, containing **11,669** verified specification-code pairs[cite: 217, 314].

<p align="center">
  <img src="https://i.imgur.com/your-workflow-image-url.png" width="800" alt="PLC-Spec-Syn Workflow">
</p>
## Key Contributions

* [cite_start]**A Principled Evolutionary Framework (`PLC-Spec-Syn`):** We systematically generate complex and realistic control tasks by evolving them along six orthogonal industrial axes: Functionality, Safety, Performance, Maintenance, Interoperability, and Contextual Complication[cite: 215].
* [cite_start]**A Large-Scale, Verified Corpus (`PLC-Spec-Code`):** We are releasing our full dataset of **11,669** instruction-code pairs in IEC 61131-3 Structured Text (ST)[cite: 217]. [cite_start]Each program in the dataset has been **formally verified** for semantic equivalence against its corresponding natural language instruction[cite: 216].
* [cite_start]**State-of-the-Art Performance:** We demonstrate that fine-tuning language models on `PLC-Spec-Code` significantly improves performance on verifiable PLC code generation by an average of 16.4% over base models[cite: 219].

## The `PLC-Spec-Code` Corpus

The `PLC-Spec-Code` corpus is the primary contribution of this work. It is designed to serve as a high-quality resource for training and evaluating language models on industrial code generation tasks.

### Dataset Format

The dataset is provided in JSON format. Each entry has the following structure:

```json
{
  "instruction": "Generate IEC 61131-3 Structured Text (ST) code for the given industrial control specification...",
  "output": "PROGRAM BIO_React_01_Control\\nVAR_INPUT...",
  "metadata": {
    "spec_id": "gen8_seed_69_variant_0_safety...",
    "matiec_passed": true,
    "generation_attempts": 1
  }
}
