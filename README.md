# Water Quality Monitoring using IoT, Edge AI & Water Quality Index

> **An intelligent water-quality monitoring framework combining IoT sensing, edge-compatible data processing, Water Quality Index (WQI) assessment, machine learning, and explainable AI.**

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![IoT](https://img.shields.io/badge/IoT-Enabled-orange)](#system-overview)
[![Edge AI](https://img.shields.io/badge/Edge-AI-green)](#machine-learning)
[![Research](https://img.shields.io/badge/Project-Research-purple)](#research-scope)

---
This project paper work is submitted to Discover Internet of things and is in review.
##  Overview

Water quality monitoring traditionally relies on periodic sampling and laboratory-based analysis. Although these approaches can provide accurate measurements, they may be time-consuming, expensive, and unsuitable for continuous monitoring.

This project presents an **IoT-enabled intelligent water-quality monitoring framework** designed to combine sensor measurements with computational intelligence for faster and more accessible assessment.

The framework focuses on three measured water-quality parameters:

- **pH**
- **Turbidity**
- **Total Dissolved Solids (TDS)**

The measurements are processed to support **Water Quality Index (WQI)** assessment and machine-learning-based water-quality classification. The overall approach is designed with **edge-compatible processing** in mind, allowing analysis to be performed closer to the sensing layer rather than depending entirely on remote/cloud computation.

### Main Goal

> **To develop a practical intelligent monitoring framework that can sense, process, assess, and interpret water-quality information using IoT and AI techniques.**

---

##  System at a Glance

```text
┌──────────────────────┐
│   Water Environment  │
│  Pond / Water Source │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────────────┐
│       IoT Sensor Layer       │
│                              │
│  • pH Sensor                 │
│  • Turbidity Sensor          │
│  • TDS Sensor                │
└──────────┬───────────────────┘
           │ Sensor Readings
           ▼
┌──────────────────────────────┐
│     Data Processing Layer    │
│                              │
│  • Data preprocessing        │
│  • Feature preparation       │
│  • Outlier / anomaly checks  │
└──────────┬───────────────────┘
           │
           ├──────────────────────┐
           ▼                      ▼
┌──────────────────────┐  ┌──────────────────────┐
│    WQI Assessment    │  │   Machine Learning   │
│                      │  │                      │
│  Water-quality       │  │  Classification      │
│  score calculation   │  │  using ML model      │
└──────────┬───────────┘  └──────────┬───────────┘
           │                         │
           └────────────┬────────────┘
                        ▼
              ┌────────────────────┐
              │ Intelligent Water  │
              │ Quality Assessment │
              └─────────┬──────────┘
                        │
                        ▼
              ┌────────────────────┐
              │ Decision / Alert / │
              │ Monitoring Output  │
              └────────────────────┘
```

---

##  System Overview

The proposed framework consists of several interconnected stages.

### 1. Water-quality sensing

The sensing layer collects measurements from the water source using sensors for:

| Parameter | Purpose |
|---|---|
| **pH** | Indicates the acidity/alkalinity of water |
| **Turbidity** | Indicates the presence of suspended particles |
| **TDS** | Provides an indication of dissolved substances |

These parameters provide the primary inputs for subsequent processing.

### 2. Data processing

Sensor observations are prepared before being used for assessment and machine learning.

The processing stage includes:

- Data collection
- Data cleaning
- Feature preparation
- Anomaly/outlier consideration
- Water-quality score calculation
- ML feature preparation

### 3. WQI assessment

The measured parameters are used to derive a **Water Quality Index (WQI)** representing water quality through a numerical score.

WQI provides a compact representation of multiple water-quality measurements and can be used to support categorical interpretation.

### 4. Machine-learning classification

Machine learning is used to classify water-quality observations based on the prepared features.

The manuscript reports **Logistic Regression** as the evaluated classification model, with the reported performance of:

- **Accuracy:** 95.83%
- **Weighted F1-score:** 0.96

These values are presented here as the results reported in the associated research work.

### 5. Edge-compatible intelligence

The framework is designed around the idea of performing computational processing closer to the sensing/edge layer. This can reduce dependence on continuous cloud-side analysis and support faster local interpretation.

---

## Architecture

The conceptual architecture can be divided into five layers:

### Layer 1 — Sensing Layer

Collects physical measurements from the water source.

**Inputs:**
- pH
- Turbidity
- TDS

### Layer 2 — IoT / Communication Layer

Transfers sensor observations from the monitoring device to the processing environment.

### Layer 3 — Data Processing Layer

Performs data preparation and converts raw measurements into usable analytical features.

### Layer 4 — Intelligence Layer

Contains:

- WQI computation
- Machine-learning classification
- Explainable AI / interpretation components

### Layer 5 — Monitoring & Decision Layer

Provides an interpretable water-quality assessment that can support monitoring and potential alert generation.

---

##  Machine Learning

The machine-learning component treats water-quality assessment as a classification problem using processed water-quality features.

### Evaluated Model

**Logistic Regression**

The reported model performance in the research work is:

| Metric | Reported Value |
|---|---:|
| Accuracy | **95.83%** |
| Weighted F1-score | **0.96** |

> **Important:** These metrics are reported from the research manuscript. The original training code, model artifact, raw prediction files, and complete experiment logs are not included in this repository.

This distinction is intentional so that the repository does not claim to reproduce experiments for which the original implementation/data are unavailable.

---

##  Water Quality Index (WQI)

WQI combines multiple water-quality measurements into a single numerical indicator.

The framework uses measured parameters to derive an overall water-quality assessment.

Conceptually:

```text
Individual Water Parameters
          │
          ▼
   Parameter Evaluation
          │
          ▼
   Quality / Weight Terms
          │
          ▼
      WQI Calculation
          │
          ▼
   Water Quality Category
```

The exact parameter weights, permissible/reference values, and category thresholds should be interpreted according to the methodology defined in the associated research work.

---

##  Research Evaluation

The research work reported observations from:

- **120 pond-water readings**
- **6 tap-water readings**
- **126 total observations**

The pond-water observations were used for the reported machine-learning analysis.

The repository intentionally does **not** include fabricated records, synthetic copies of the original dataset, or reconstructed predictions.

### Reported ML Result

```text
Logistic Regression
        │
        ├── Accuracy      → 95.83%
        │
        └── Weighted F1   → 0.96
```

---

##  Explainable AI

Explainability is included as part of the broader intelligent-monitoring framework to improve the interpretability of machine-learning decisions.

The purpose of the XAI component is to help understand:

- Which input parameters influence predictions
- How individual water-quality features contribute to decisions
- Why an observation receives a particular classification

However, **detailed quantitative XAI analysis is not included in this repository**, because the original implementation and complete experiment outputs are unavailable.

---

##  Technology Stack

| Category | Technologies / Components |
|---|---|
| Sensing | pH, Turbidity, TDS sensors |
| IoT | IoT-enabled monitoring architecture |
| Processing | Python-based analytical workflow |
| Machine Learning | Logistic Regression |
| Water Assessment | WQI |
| Explainability | XAI-oriented analysis |
| Visualization | Python visualization ecosystem |
| Deployment Concept | Edge-compatible processing |

---


### Directory purpose

**`docs/`**  
Contains detailed project documentation covering the methodology, architecture, WQI approach, and limitations.

**`data/`**  
Documents the dataset scope and availability. Raw research observations are not included.

**`src/`**  
Describes the intended implementation scope. The original project source code is not available.

**`results/`**  
Documents the results reported in the research work without presenting reconstructed or fabricated experimental outputs.

**`figures/`**  
Reserved for project/system figures that are appropriate for public release.

---

##  Reproducibility & Research Scope

This repository is intended as a **research/project documentation and portfolio repository** associated with the water-quality monitoring work.

It is important to distinguish between:

### What is documented

- System concept
- IoT sensing approach
- pH, turbidity, and TDS parameters
- WQI-based assessment
- Machine-learning methodology
- Edge-AI concept
- Reported ML performance
- Research limitations

### What is not included

- Original source code
- Original raw sensor dataset
- Original trained model
- Complete training logs
- Original prediction files
- Full experimental environment
- Unpublished manuscript
- Reviewer correspondence

This avoids presenting reconstructed material as the original research implementation.

---

##  Limitations

The research work has several limitations that should be considered when interpreting the reported results:

1. **Limited sample size**  
   The reported dataset contains 126 observations, including 120 pond-water and 6 tap-water readings.

2. **Limited water-quality parameters**  
   The framework focuses primarily on pH, turbidity, and TDS.

3. **Limited geographical/temporal coverage**  
   The available observations do not establish long-term or large-scale environmental generalization.

4. **Limited experimental benchmarking**  
   The reported work does not provide a complete large-scale comparison across many machine-learning algorithms.

5. **Limited quantitative XAI evaluation**  
   The interpretability component requires more detailed quantitative validation.

6. **Need for laboratory validation**  
   Future studies should compare sensor-based measurements against established laboratory measurements.

7. **Sensor calibration and uncertainty**  
   More detailed calibration, uncertainty analysis, and sensor-specific validation would strengthen reproducibility.

These limitations are important for future extension of the framework.

---

##  Future Work

Possible future improvements include:

- Larger and more diverse water-quality datasets
- Long-term continuous monitoring
- Multiple geographical locations
- Additional water-quality parameters
- Laboratory-validated ground truth
- Sensor calibration and uncertainty analysis
- More rigorous model comparison
- Cross-validation and statistical significance testing
- Regression-based prediction of continuous water-quality scores
- Quantitative explainable-AI analysis
- Improved edge deployment and resource benchmarking
- Real-time alert and dashboard integration
- Hardware-level optimization for low-power deployment

---

##  Potential Applications

The framework can be extended toward applications such as:

- 🏞️ Pond and lake monitoring
- 🚰 Drinking-water monitoring
- 🌱 Agricultural water assessment
- 🏭 Industrial water monitoring
- 🌊 Environmental monitoring
- 🏘️ Community-level water-quality monitoring
- 📡 Remote IoT-based sensing systems

---

##  Research Context

This repository accompanies research on an **IoT-based intelligent water-quality monitoring framework** integrating sensing, WQI assessment, machine learning, and edge-oriented processing.

The repository is maintained as a public project showcase while the associated manuscript remains under review.

> **The unpublished manuscript and reviewer correspondence are intentionally not included in this public repository.**

---

##  Author

**Rishitha Chappidi**

B.Tech — Artificial Intelligence & Data Science  
Amrita Vishwa Vidyapeetham, Coimbatore

GitHub: **[@Rishithachappidi](https://github.com/Rishithachappidi)**

---

##  Disclaimer

This repository is provided for **research documentation, educational purposes, and project showcasing**.

Reported performance values are reproduced from the associated research work and should not be interpreted as independently reproducible benchmark results from this repository.

The repository does not claim to contain the original implementation or complete experimental dataset.

---

##  Project Status

**Status: Research / Documentation Showcase**

The project documentation reflects the current research framework and reported findings. Further experimental validation and implementation release may be added when the corresponding materials become available.

---

### Keywords

`IoT` · `Water Quality` · `WQI` · `Edge AI` · `Machine Learning` · `pH` · `Turbidity` · `TDS` · `Environmental Monitoring`
