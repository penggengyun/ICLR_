# PLC-InstrSyn: Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale

[![Paper](https://img.shields.io/badge/Paper-ICLR%202026%20(Under%20Review)-blue)](https://openreview.net/forum?id=XXXX)
[![Dataset](https://img.shields.io/badge/Dataset-Download-green)](https://anonymous.4open.science/r/PLC-InstrSyn-XXXX)
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

* **A Large-Scale, Verified Corpus (`PLC-Instr-Code`):** We release a new dataset of **11,669 instruction-code pairs** in IEC 61131-3 Structured Text (ST). Each program in the corpus has been **formally verified** for semantic equivalence against its corresponding natural language instruction.

* **State-of-the-Art Performance:** We demonstrate that fine-tuning language models on `PLC-Instr-Code` significantly improves performance on verifiable PLC code generation, outperforming models trained on existing public data or with generic data synthesis methods.

## 📊 The `PLC-Instr-Code` Corpus

The `PLC-Instr-Code` corpus is the primary contribution of this work. It is designed to serve as a high-quality resource for training and evaluating language models on industrial code generation tasks.

### Dataset Format

The dataset is provided in JSONL format. Each line in the file is a JSON object with the following structure:

```json
{
  "instruction": "A detailed natural language specification for an industrial control task, including I/O requirements, control logic, safety constraints, and performance targets...",
  "code": "PROGRAM Main\nVAR_INPUT\n    ...\nEND_VAR\nVAR_OUTPUT\n    ...\nEND_VAR\n\n(* Verified Structured Text (ST) code that implements the instruction *)\n\nEND_PROGRAM"
}
````

### Accessing the Data

The full, formally verified corpus can be found in the `data/` directory of this repository or downloaded from the anonymous link above.

```bash
/data
└── plc_instr_code_verified.jsonl  # The complete 11,669-pair dataset
```

## 🛠️ Usage

This dataset can be directly used for supervised fine-tuning of code generation models.

### Fine-Tuning Example

We provide example scripts for fine-tuning popular open-source models (e.g., Qwen, Llama) on our corpus in the `finetuning/` directory.

```bash
# Example fine-tuning command (see scripts for details)
python finetuning/run_sft.py \
    --model_name_or_path "path/to/base_model" \
    --train_file "data/plc_instr_code_verified.jsonl" \
    --output_dir "output/my_finetuned_plc_model"
```

### Evaluation

Scripts and benchmarks used for evaluating model performance can be found in the `evaluation/` directory. This allows for the reproduction of the results presented in our paper.

## Citing Our Work

If you use our framework or dataset in your research, please cite our paper. For the purpose of anonymous review, please use the following placeholder.

```bibtex
@inproceedings{anonymous2026plc,
  title={Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale},
  author={Anonymous Author(s)},
  booktitle={International Conference on Learning Representations (ICLR)},
  year={2026},
  url={[https://openreview.net/forum?id=XXXX](https://openreview.net/forum?id=XXXX)}
}
```

## 📜 License

This project is licensed under the Apache 2.0 License. See the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

```
```
