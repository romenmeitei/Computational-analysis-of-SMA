# Ensemble Docking and Molecular Dynamics Reveal Allosteric Stabilization of hnRNPA1 UP1 Interdomain Dynamics by a Small-Molecule Natural Product

![Python](https://img.shields.io/badge/python-3.10-blue)
![Platform](https://img.shields.io/badge/platform-Google%20Colab-orange)
![License](https://img.shields.io/badge/license-MIT-green)

---

# Overview

This repository contains the **complete computational workflow** used to investigate small-molecule modulation of the **hnRNPA1 UP1 interdomain interface**.

The workflow integrates:

- High-Throughput Virtual Screening (HTVS)
- Composite ligand prioritization
- Ensemble docking
- Molecular dynamics simulations
- Structural and dynamic trajectory analysis

The repository is provided to ensure **full transparency, reproducibility, and traceability** of ligand prioritization and mechanistic analysis.

---

## Computational Workflow

```mermaid
flowchart TD

A[Phytochemical Library 2847 KEGG compounds] --> B[PubChem Descriptor Retrieval]

B --> C[High Throughput Virtual Screening using AutoDock Vina]

C --> D[Docking Output Processing]

D --> E[Feature Extraction]

E --> E1[Docking Energy]
E --> E2[Pose Stability Metric]
E --> E3[Physicochemical Descriptors]

E1 --> F[Z Score Normalization]
E2 --> F
E3 --> F

F --> G[Composite Scoring]

G --> H[Weighted Scoring Function]

H --> I[Ligand Level Ranking Best Pose per PubChem CID]

I --> J[Top 100 Ligands]

J --> K[Selection of Withanolide D]

K --> L[Molecular Dynamics Simulations]

L --> M[Trajectory Analysis]

M --> M1[RMSD RMSF]
M --> M2[Radius of Gyration]
M --> M3[Interdomain Distance]
M --> M4[Protein Ligand Contacts]

M1 --> N[Mechanistic Interpretation]
M2 --> N
M3 --> N
M4 --> N

N --> O[Allosteric Stabilization of hnRNPA1 UP1]
