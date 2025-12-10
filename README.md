# 🧬 Designing Better Cancer Vaccines --- UCL-CCC Hackathon 2025

This repository contains our project developed for the **UCL Cancer
Collaborative Centre Hackathon 2025**, where our team designed an
end-to-end computational pipeline to improve personalised cancer vaccine
development. Our aim is to identify *high-value neoantigen targets* that
a patient's immune system has not already failed to recognise.

------------------------------------------------------------------------

## 🚀 Project Overview

Cancer vaccines provide a powerful therapeutic avenue, but high
non-response rates remain a key challenge. The main bottleneck is the
identification and prioritisation of effective neoantigen targets from
an enormous search space (≈10¹⁷ peptides). Our solution integrates
tumour genomics, patient HLA typing, and TCR repertoire data to generate
a **ranked list of optimal vaccine candidates**.

### Key Innovation

We exclude peptides already recognised by exhausted or ineffective
T-cell responses, increasing the likelihood of inducing a strong and
durable vaccine response.

------------------------------------------------------------------------

## 🧠 High-Level Pipeline

1.  **Neoantigen Identification**\
    Extract mutated peptides (9-mers) present in cancer cells but not in
    normal tissue.

2.  **MHC Binding Prediction**\
    Predict HLA-specific binding affinities to determine
    surface-presentable peptides.

3.  **TCR Binding Prediction**\
    Identify and remove peptides already targeted unsuccessfully by the
    patient's TCRs.

4.  **Ranking & Output**\
    Score the remaining peptides using immunogenicity, presentation
    likelihood, clonality, conservation, and safety metrics.

------------------------------------------------------------------------

## 🧬 Data Requirements

### Training Data

-   Cancer genomes with validated neoantigens\
-   HLA--peptide binding datasets (IEDB)\
-   TCR--peptide binding datasets

### Patient-Specific Inputs

-   Tumour genome sequencing\
-   Patient HLA genotype\
-   TCR repertoire sequencing

------------------------------------------------------------------------

## 🧩 Model Architecture

Our architecture incorporates:\
- Neoantigen identification module\
- Transformer-based MHC binding prediction\
- Structural TCR--peptide interaction modelling (AlphaFold-based)

------------------------------------------------------------------------

## 📊 Ranking Metrics

-   MHC binding affinity\
-   TCR engagement strength\
-   Surface presentation probability\
-   Peptide abundance\
-   Conservation across cancer subclones\
-   Phylogenetic clonality\
-   Cross-reactivity and safety assessment

------------------------------------------------------------------------

## 📁 Repository Structure

    .
    ├── data/
    ├── models/
    ├── pipeline/
    ├── notebooks/
    ├── results/
    └── README.md

------------------------------------------------------------------------

## 🧑‍🔬 Team TC-AWARE

-   Matthew Cowley\
-   Zhen Wei Yap\
-   Mohammad Alawwami\
-   Zarif Shafiei\
-   Linh Hoang\
-   Julia Sala-Bayo\
-   Graham Bonomo-Jackson\
-   Gleb Gmyzov\
-   Nick Keatley
