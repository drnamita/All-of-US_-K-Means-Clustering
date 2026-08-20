# All-of-US-K-Means-Clustering
# Identification of Distinct Mental Health–Metabolic Clusters in Female Breast Cancer Patients Using All of Us Real-World Data

## Overview

This repository contains the analytical code, data-processing workflow, and supporting materials for a study identifying distinct phenotypic subgroups among female breast cancer patients using real-world data from the **All of Us Research Program**.

The study applies an **unsupervised K-means clustering approach** to characterize multidimensional patterns of:

- Mental health disorders
- Metabolic comorbidities
- Cancer treatment exposure
- Selected sociodemographic characteristics

The objective was to identify data-driven phenotypic profiles that may capture combinations of clinical characteristics not readily apparent when individual conditions are examined separately.

---

## Study Objective

To identify distinct phenotypic subgroups of female breast cancer patients based on co-occurring mental health disorders, metabolic conditions, treatment burden, and selected sociodemographic characteristics using unsupervised clustering techniques.

---

## Data Source

Data were obtained from the **All of Us Research Program Curated Data Repository, version 8 (CTv8)**.

The initial breast cancer cohort included:

- **12,542** breast cancer participants
- **11,972** female breast cancer participants included in the analytic cohort

Data extraction and analysis were conducted using the All of Us Research Program's approved research environment.

Because All of Us data are subject to controlled-access and data-use requirements, participant-level data are **not included in this repository**.

Researchers interested in accessing All of Us data should apply through the official All of Us Research Program.

---

## Study Cohort

The cohort was constructed by identifying participants with breast cancer and subsequently restricting the population to female participants.
### Cohort flow

```text
Initial breast cancer cohort
N = 12,542
        │
        ▼
Female breast cancer participants
N = 11,972
        │
        ▼
Final clustering cohort
N = 11,972
        │
        ▼
15 clustering features
Mental health + metabolic +
treatment + sociodemographic characteristics
        │
        ▼
K-means clustering (k = 4)
        │
        ├───────────────┬────────────────┬────────────────┐
        ▼               ▼                ▼                ▼
   Cluster 1        Cluster 2         Cluster 3        Cluster 4
   Treatment-       Severe            High metabolic   Low treatment-
   exposed         psychiatric       burden with      exposure /
   phenotype       phenotype         mental health   lower metabolic
                                      burden          burden
