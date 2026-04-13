# 🧬 Genetic Ensemble Feature Selection (GEFS)
----

<br />
This project explores a hybrid approach to feature selection and model ensembling using a genetic algorithm framework. The goal is to jointly optimize feature subsets and model diversity under constraints.

## 📌 Overview
----

Traditional pipelines separate:

- feature selection
- model training
- ensembling

GEFS integrates these into a single evolutionary process, where each candidate represents:

- a subset of features
- an assigned model type

The system evolves populations of such candidates based on predictive performance and diversity.

## ⚙️ Implementations
----

<br />
The repository includes two versions:

1. **Baseline (Submitted Version)**
   - Fitness: F1 score + diversity
   - Homogeneous & heterogeneous ensembles
   - Majority voting or stacking
   - Designed for academic clarity and reproducibility

2. **Extended Version (Exploratory)**
   - Evaluation-aware fitness (F1 + PR-AUC)
   - Feature importance–guided search (ANOVA F-score)
   - Controlled feature pool for stability
   - Structural diversity via feature-mask novelty
   - Improved validation split for more reliable selection

This version reflects iterative improvements beyond the academic baseline.

## 🧠 Models Used
----

<br />
Base learners include:

- Decision Tree (DT)
- K-Nearest Neighbors (KNN)
- Logistic Regression (LR)
- Support Vector Machine (SVM)
- Multi-layer Perceptron (MLP)

These are used both as standalone baselines and within ensemble configurations.

## 🔬 Problem Setting
----

- **Dataset:** Online Shoppers Intention
- **Task:** Binary classification (imbalanced)
- **Focus:**
  - F1-score
  - PR-AUC (precision-recall sensitivity)
  - Ensemble diversity

## 🏗️ Pipeline
----

1. Data preprocessing & feature engineering
2. Candidate generation (feature masks + model types)
3. Genetic evolution (selection, crossover, mutation)
4. Fitness evaluation (performance + diversity)
5. Final ensemble construction (voting / stacking)

## 📊 Key Idea
----

Rather than searching for a single optimal model, GEFS searches for a set of complementary models, each operating on different feature subsets, improving robustness under limited or noisy features.

## 🚧 Notes
----

<br />
- The baseline version corresponds to the submitted academic project
- The extended version explores practical improvements and design trade-offs
- The project emphasizes system-level thinking over isolated model performance

## 🔗 Repository Structure
----
/baseline        # submitted academic version
/extended        # improved experimental version
/data            # dataset
/notebooks       # experiments and analysis
