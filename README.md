# AI-Based Crop Yield Prediction

An end-to-end machine learning pipeline for predicting crop yields across multiple countries using agronomic and environmental data. Built as part of an MSc Artificial Intelligence dissertation at Nottingham Trent University.

## Results

| Model | R² | RMSE | MAE |
|---|---|---|---|
| Random Forest | **0.989** | — | — |
| MLP Neural Network | competitive | — | — |
| LSTM (time-series) | competitive | — | — |
| Linear Regression | baseline | — | — |

> Random Forest achieved R² = 0.989 on the test set, with cross-validation confirming robust, generalisable performance.

## Project Overview

Crop yield prediction is a critical challenge for food security, agricultural planning, and climate adaptation. This project builds a reproducible, production-aligned ML pipeline that:

- Ingests and cleans a multi-country agricultural dataset (28,000+ records)
- Engineers meaningful features from raw agronomic and environmental inputs
- Trains and evaluates multiple ML algorithms head-to-head
- Applies SHAP explainability to identify the key drivers of yield outcomes
- Produces fully documented, auditable outputs suitable for real-world decision support

## Pipeline Architecture
Raw Data (28K+ records, multiple countries)
|
v
Data Ingestion & Validation
|
v
Cleaning & Preprocessing
(missing values, outliers, normalisation)
|
v
Feature Engineering
(derived features, encoding, selection)
|
v
Model Training
(Linear Regression, Random Forest, MLP, LSTM)
|
v
Evaluation
(RMSE, MAE, R², cross-validation)
|
v
SHAP Explainability
(feature importance, decision transparency)
|
v
Results & Documentation

## Tech Stack

- **Language:** Python 3.x
- **ML Frameworks:** scikit-learn, TensorFlow/Keras
- **Data:** Pandas, NumPy
- **Visualisation:** Matplotlib, Seaborn
- **Explainability:** SHAP
- **Experiment Tracking:** structured logs and modular code

## Key Features

### End-to-End Pipeline
Every stage from raw data to final model output is implemented in modular, reusable Python code. The pipeline is fully reproducible — run it from scratch and get the same results every time.

### Multi-Model Comparison
Four algorithms are trained and evaluated on identical data splits, enabling a rigorous head-to-head comparison. Random Forest emerged as the strongest performer with R² = 0.989.

### SHAP Explainability
SHAP (SHapley Additive exPlanations) values are computed for the best-performing model, revealing which features drive yield predictions. This makes the model's decisions transparent and interpretable for non-technical stakeholders.

### Ethical AI Assessment
The project includes a comprehensive ethical assessment covering:
- Bias and fairness across country and crop type distributions
- Data privacy and minimisation principles
- Transparency and auditability of model outputs
- Environmental considerations of model training

## Repository Structure
crop-yield-prediction/
│
├── crop_yield_prediction.ipynb   # Main notebook — full pipeline
├── requirements.txt              # Python dependencies
└── README.md

## Getting Started

### Prerequisites

```bash
pip install -r requirements.txt
```

### Run the notebook

```bash
# Clone the repo
git clone https://github.com/Pranit3434/crop-yield-prediction.git
cd crop-yield-prediction

# Install dependencies
pip install -r requirements.txt

# Open notebook
jupyter notebook crop_yield_prediction.ipynb
```

## Dataset

This project uses a publicly available multi-country agricultural dataset. Due to file size, the raw data is not included in this repository.

To reproduce results, download the dataset and place it in the same directory as the notebook, then update the file path in the data loading cell.

## Ethical Considerations

This model is intended as a decision-support tool, not a replacement for expert agronomic judgement. Key considerations:

- **Bias:** Performance may vary across countries and crop types. Always evaluate on locally representative data before deployment.
- **Transparency:** SHAP values are provided for all predictions to support human oversight.
- **Privacy:** No personally identifiable information is used or stored.
- **Environmental:** Model training is computationally lightweight and designed to minimise unnecessary compute.

## Author

**Pranit Devendra Salvi**
MSc Artificial Intelligence, Nottingham Trent University (2025)

[LinkedIn](https://linkedin.com/in/pranit-salvi-a3860b276) | salvipranit13@gmail.com
