# Behaviour-Analysis-in-a-Gamified-Python-Learning-System-dissertation
Behaviour-Analysis-in-a-Gamified-Python-Learning-System-My dissertation 
# Learning Progression and Player Behaviour Analysis in a Gamified Python Learning System

## MSc Data Science Dissertation
**Student:** Sayud Meharaj (250153631)  
**Supervisor:** Dr. Joe Yuen  
**University:** Aston University, Birmingham  
**Module:** AM41PR Research Project  
**Date:** May 2024  

---

## Project Overview
This dissertation analyses learning progressions and player behaviour 
in a gamified Python learning system using the CodeWorkout Fall 2019 
dataset (494 students, 360,000 programming interactions).

---

## Notebooks — Run in this order

| Notebook | Description |
|---|---|
| 01_EDA.ipynb | Exploratory data analysis (7 visualisations) |
| 02_Feature_Engineering.ipynb | Behavioural feature extraction (16 features) |
| 03_Clustering.ipynb | K-means clustering and validation |
| 04_Temporal_Analysis.ipynb | Temporal transition analysis |
| 05_Prediction.ipynb | Random Forest prediction modelling |

> **Important:** Run 04_Temporal_Analysis.ipynb before 05_Prediction.ipynb  
> (04 generates data/late_labels.csv which 05 requires)

---

## Data Files

### Raw data (download from source)
The raw CodeWorkout Fall 2019 dataset is publicly available at:  
**https://csedm-dc.github.io/**

Download and place these files in the same folder as the notebooks:
- `MainTable.csv`
- `Subject.csv`
- `early.csv`
- `late.csv`

### Generated data (included in this repository)
- `feature_matrix.csv` — 494 students × 16 behavioural features
- `feature_matrix_with_clusters.csv` — features + cluster assignments
- `cluster_profiles.csv` — aggregate statistics per cluster
- `cluster_information.csv` — cluster metadata
- `transition_matrix.csv` — 4×4 temporal transition matrix
- `late_labels.csv` — late phase cluster labels per student

---

## Installation

```bash
pip install -r requirements.txt
```

## Requirements
- Python 3.8+
- See requirements.txt for full package list

---

## Key Findings
- Four distinct learner profiles identified: Deep, Steady, Surface, Struggling
- Deep Learners (avg 10.5 attempts) outperform Surface Learners (avg 2.0 attempts)
- 60% behavioural stability across semester phases
- Random Forest R²=0.44 — behavioural features outperform demographic predictors
