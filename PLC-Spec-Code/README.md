# PLC-Spec-Code Corpus

This directory contains the `PLC-Spec-Code` dataset, the primary contribution of our ICLR 2026 submission, "**Boosting Verifiable Industrial Code Generation by Reliable Task Generation at Scale**."

## About the Corpus

`PLC-Spec-Code` is the first large-scale, formally verified corpus of instruction-code pairs specifically designed for the industrial control domain. Each entry in this dataset consists of:

1.  A detailed, structured **Specification** in natural language that describes a realistic industrial control task.
2.  The corresponding IEC 61131-3 **Structured Text (ST) Code** that correctly implements the specification.

Every code sample in this corpus has been formally verified for semantic equivalence against its specification, ensuring a high-quality and reliable resource for training and evaluating large language models.

## Progressive Release Schedule

To foster community engagement and ensure a high standard of quality, the full `PLC-Spec-Code` corpus of 11,669 pairs will be **released to the research community in stages**.

This initial release contains a significant subset of the data. We will be updating this repository with additional data progressively. Please "watch" this repository to be notified of future updates and the release of the complete dataset.

