# Defect Forecasting

## Summary

Developed a classification model for time-series defect prediction at a manufacturing client. Built evaluation frameworks with explainability features, conducted AWS-based experimentation, and delivered a Dockerized pipeline for production deployment. The solution enabled proactive quality control and reduced defect-related costs.

## My Role and Scope

- Developed classification models for predicting defects in manufacturing time-series data
- Designed evaluation frameworks with multiple metrics and explainability analysis
- Conducted cloud-based experimentation on AWS to test different hyperparameter settings
- Containerized the solution using Docker for retraining routines

## Problem Framing

The client experienced quality issues that led to costly rework and production delays. The main problem was that operators, in order to avoid defects, produced at too high quality standards, resulting in unnecessarily expensive production. Defects were often detected only after production, making it difficult to intervene proactively. Historical sensor and process data contained patterns that could predict defects, but existing quality control processes were reactive rather than predictive.

## Approach

The solution transformed time-series manufacturing data into a classification problem. Initially, we ingested image sensor output to identify defective parts and computed image features for predictions:

```
Image Sensor Output
    ↓
[Image Feature Extraction]
    ├── Defect Identification
    └── Image Feature Computation
    ↓
Manufacturing Sensor Data
    ↓
[Time-Series Feature Engineering]
    ├── Rolling Statistics
    ├── Trend Features
    └── Frequency Domain Features
    ↓
[Classification Model Development]
    ├── AWS Experimentation
    └── Hyperparameter Tuning
    ↓
[Evaluation & Explainability]
    ├── Precision/Recall Analysis
    ├── Feature Importance
    └── SHAP Explanations
    ↓
[Dockerized Pipeline]
    ├── Model Serving
    ├── Batch Prediction
    └── Monitoring
    ↓
Production Deployment
```

Time-series sensor data and image features were transformed into fixed-length feature vectors using rolling windows and statistical aggregations, enabling standard classification algorithms to capture temporal patterns and visual defect indicators.

## Modeling

**Algorithm**: LightGBM classifier, selected for its ability to handle mixed feature types and provide feature importance.

**Features**: Engineered from sensor readings, process parameters, image sensor output, and historical defect patterns. Included image features, rolling means, standard deviations, trends, and frequency domain features.

**Evaluation**: Stratified cross-validation with focus on precision (to minimize false alarms) and recall (to catch true defects).

**Explainability**: Feature importance analysis and SHAP values to identify which process parameters and sensor readings were most predictive of defects. This enabled root cause analysis and process improvements.

**AWS Experimentation**: Used AWS SageMaker to run parallel experiments across different hyperparameters, enabling client-specific model selection.

## Engineering

- **Dockerization**: Containerized the entire pipeline for retraining and consistent deployment across environments
- **Reproducibility**: Version-controlled pipeline, feature definitions, and Docker configurations

## Outcomes

- Deployment-ready defect prediction model with improved early detection capabilities
- Enabled defect-related cost reduction through proactive quality control interventions (client-specific improvements)
- Supported root cause analysis through explainable model outputs for process improvements
- Delivered production-ready Dockerized pipeline that could be deployed across manufacturing sites


## Confidentiality Note

This case study has been sanitized to protect client confidentiality. Client names, proprietary data schemas, internal system names, specific KPIs, and identifying business metrics have been removed or generalized. All technical approaches and methodologies are presented at an architecture level without revealing proprietary implementations.

