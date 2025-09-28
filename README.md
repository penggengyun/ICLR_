# PLC-InstrSyn: Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale

[![License](https://img.shields.io/badge/License-Apache%202.0-orange.svg)](LICENSE)

This repository contains the official dataset and resources for the ICLR 2026 submission, "**Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale**".

Our work introduces **`PLC-InstrSyn`**, a novel framework for generating high-fidelity instruction-code pairs for Programmable Logic Controller (PLC) programming. To address the critical scarcity of verified data in the industrial control domain, we employ a principled evolutionary process guided by real-world engineering standards. This process has produced **`PLC-Instr-Code`**, the first large-scale, formally verified corpus of its kind.

## 🚀 Key Contributions

* **A Principled Evolutionary Framework (`PLC-InstrSyn`):** We systematically generate complex and realistic control tasks by evolving them along six orthogonal industrial axes:
    1.  Functionality
    2.  Safety
    3.  Performance
    4.  Maintenance
    5.  Interoperability
    6.  Contextual Complication

* **A Large-Scale, Verified Corpus (`PLC-Instr-Code`):** We are releasing an initial set of **1000 instruction-code pairs** in IEC 61131-3 Structured Text (ST), with the full corpus to be made available progressively. Each program in the dataset has been formally verified for semantic equivalence against its corresponding natural language instruction.

* **State-of-the-Art Performance:** We demonstrate that fine-tuning language models on `PLC-Instr-Code` significantly improves performance on verifiable PLC code generation, outperforming models trained on existing public data or with generic data synthesis methods.

## 📊 The `PLC-Instr-Code` Corpus

The `PLC-Instr-Code` corpus is the primary contribution of this work. It is designed to serve as a high-quality resource for training and evaluating language models on industrial code generation tasks.

### Dataset Format

The dataset is provided in JSON format. 



### Accessing the Data



### Evaluation

Scripts and benchmarks used for evaluating model performance can be found in the `evaluation/` directory. This allows for the reproduction of the results presented in our paper.



## 📜 License

This project is licensed under the Apache 2.0 License. See the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

```
```
