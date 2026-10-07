# IoT-Based Water Quality Monitoring Using Edge AI

This repository is a documentation and research showcase repository based on the
water-quality monitoring manuscript.

## Scope

The repository documents the system and methodology described in the paper.
The original source-code project and raw experimental dataset were not available
when this repository was prepared. Therefore, no fabricated implementation,
dataset, or experimental result has been added.

## System Overview

The proposed framework combines:

- IoT-based water-quality sensing
- pH measurement
- Turbidity measurement
- Total Dissolved Solids (TDS) measurement
- Edge-compatible processing
- Water Quality Index (WQI) assessment
- Machine-learning-based water-quality classification
- Explainable AI (XAI)
- Real-time monitoring

## Experimental Data Reported in the Paper

The manuscript reports:

- 120 pond-water readings
- 6 tap-water readings
- Total reported observations: 126
- Pond observations were used for the machine-learning evaluation.

The repository does not contain the original raw observations because they were
not supplied with the paper.

## Machine Learning

The manuscript reports Logistic Regression as achieving an accuracy of 95.83%
and a weighted F1 score of 0.96.

The repository does not claim to reproduce this result because the original
training data and complete experimental implementation were not supplied.

## Repository Structure

```text
water-quality-edge-ai/
├── README.md
├── .gitignore
├── requirements.txt
├── paper/
│   └── README.md
├── docs/
│   ├── methodology.md
│   ├── system-architecture.md
│   ├── wqi-methodology.md
│   └── limitations.md
├── figures/
│   └── README.md
├── data/
│   └── README.md
├── src/
│   └── README.md
└── results/
    └── README.md
```

## Reproducibility Note

This repository is intentionally transparent about what is and is not available.
It should not be interpreted as a full code-reproduction package for the paper.

For a complete reproducibility release, the original authors would need to add
the source implementation, raw/processed dataset, model configuration,
preprocessing procedure, and complete experimental outputs.

## Citation

Please cite the associated manuscript when using material from this repository.
