# Explainable Robo-Advisor with XAI and RAG

## Overview
This repository contains the system code developed as part of a bachelor thesis project focused on enhancing transparency and interpretability in robo-advisory systems. The project combines traditional machine learning, explainable artificial intelligence (XAI), and retrieval-augmented generation (RAG) to explain why an investor is classified into a specific risk profile and how such decisions can be communicated in a clear, user-oriented manner.

The system is designed as an educational prototype that demonstrates how modern AI techniques can improve trust and interpretability in automated financial decision-support systems.

---

## Research Motivation
Robo-advisors frequently rely on complex machine-learning models that function as black boxes for end users. While these systems may deliver strong predictive performance, they often fail to provide transparent explanations that justify their outputs.

This project addresses the following challenges:

- Lack of interpretability in automated risk-profiling models  
- Limited user trust due to opaque decision logic  
- Difficulty explaining model decisions in natural, non-technical language  

By integrating Explainable AI techniques with a Retrieval-Augmented Generation explanation layer, the system aims to bridge the gap between technical model outputs and human-understandable explanations.

---

## System Architecture (High-Level)
The system follows a modular and sequential pipeline:

1. **Synthetic Investor Data Generation**  
   Investor attributes such as age, income, financial knowledge, investment experience, risk preference, loss aversion, investment horizon, and primary investment goal are generated to mimic realistic investor profiles.

2. **Risk Profile Classification**  
   A Random Forest–based classification pipeline assigns investors to one of three risk categories:
   - Conservative  
   - Moderate  
   - Aggressive  

3. **Explainable AI (XAI) with SHAP**  
   SHAP (SHapley Additive exPlanations) values are used to provide local explanations for individual predictions. Feature-level contributions quantify how each input variable influences the final classification.

4. **Retrieval-Augmented Generation (RAG)**  
   A curated domain-specific knowledge base is queried to retrieve relevant contextual information. Retrieved context is combined with model explanations to generate structured, natural-language justifications.

---

## Repository Structure
explainable_robo_advisor/
│
├── data_generation.ipynb
│ Synthetic investor data creation and preprocessing
│
├── data_exploration.ipynb
│ Exploratory data analysis and feature inspection
│
├── model_training.ipynb
│ Model training, evaluation, and probability outputs
│
├── explainability_shap.ipynb
│ SHAP-based explainability and feature contribution analysis
│
├── rag/
│ ├── knowledge_base/
│ │ └── base_knowledge.md
│ │ Curated financial explanation content
│ │
│ └── rag_explainer.ipynb
│ Retrieval-augmented explanation generation
│
├── .gitignore
│ Git ignore rules (models, data, environments, secrets)
│
└── README.md

---

## How to Run the Project

## 1. Environment Setup
Create a virtual environment (recommended):

python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
Install required dependencies (example):

pip install numpy pandas scikit-learn shap matplotlib seaborn jupyter
Note: Exact dependency versions may vary depending on the local setup.

---

## 2. Execution Order
For a clean and logical execution, notebooks should be run in the following order:

data_generation.ipynb

data_exploration.ipynb

model_training.ipynb

explainability_shap.ipynb

rag/rag_explainer.ipynb

Each notebook is self-contained and includes explanatory comments describing its purpose and outputs.

---

## Model Files and Data Handling
Trained models and large datasets are not included in this repository due to size constraints and best practices for version control.

Model artifacts (e.g. .joblib, .pkl) are generated locally when running the training notebook.

Large data files are intentionally excluded and regenerated when required.

This approach ensures:

A clean and lightweight repository

Full reproducibility through code rather than stored binaries

---

## Explainability Strategy
The project uses SHAP (SHapley Additive exPlanations) to:

Quantify individual feature contributions

Explain predictions at the level of a single investor

Support transparency and auditability

SHAP-based explanations are combined with domain-specific contextual information retrieved via RAG to produce explanations that are understandable by non-technical users.

---

## Disclaimer
This project is an educational prototype only.

It does not provide financial advice.

It does not make real investment decisions.

Outputs should not be interpreted as personalized investment recommendations.

The system is intended solely for academic, illustrative, and research purposes.

---

Author
Treva Antony Ogwang
Bachelor Thesis – Data Science, AI & Digital Business

---

License
This project is provided for academic and educational use.
All rights reserved unless stated otherwise.
