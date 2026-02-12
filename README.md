**Project Title
**Ensemble Docking and Molecular Dynamics Reveal Allosteric Stabilization of hnRNPA1 UP1 Interdomain Dynamics by a Small-Molecule Natural Product

**Overview**
This repository contains the complete computational workflow used in the study investigating small-molecule modulation of the hnRNPA1 UP1 interdomain interface.

The workflow integrates:

High-throughput virtual screening (HTVS)

Composite ligand scoring

Molecular dynamics simulations

Ensemble docking

Structural and dynamic analyses

The repository is provided to ensure full transparency and reproducibility of ligand prioritization and mechanistic analysis.
Repository Structure
1. Ligand Ranking Workflow

Ligand_ranking.ipynb

Implements composite scoring:

Z-normalized docking energy

Pose stability metric

ADMET proxy score

Weighted scoring formula:

CS = 0.5 × Z(|E_dock|)
+ 0.2 × Z(Pose Stability)
+ 0.3 × Z(ADMET proxy)

Performs ligand-level ranking (best pose per PubChem CID)



2. Ranked Dataset

Top100_Ligands_Composite_OptionA.csv

Contains:

Compound Name

PubChem CID

Docking Energy

Pose Stability Score

ADMET Proxy

Composite Score

Rank Position

This dataset represents the objectively filtered top 100 ligands from the screened library of 2,847 phytochemicals.



Selection of Withanolide D

Withanolide D was selected from the top-ranked ligands based on:

Objective composite ranking

Balanced scoring profile (no extreme bias toward single metric)

Chemical tractability

Favorable physicochemical properties

Literature-supported neurobiological relevance

The complete ranked dataset allows independent verification of this prioritization.



**Reproducibility
**
All analyses were performed using:

Python 3.10

NumPy

pandas

scikit-learn

SciPy

matplotlib

The ranking workflow can be executed directly in Google Colab or locally using Jupyter Notebook.



**Citation**

If using this workflow or dataset, please cite:

Meitei RL et al., "Ensemble Docking and Molecular Dynamics Reveal Allosteric Stabilization of hnRNPA1 UP1 Interdomain Dynamics by a Small-Molecule Natural Product."
