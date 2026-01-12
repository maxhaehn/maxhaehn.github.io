# Demand Forecasting

## Summary

Developed a demand forecasting solution for a pharmaceutical client, combining univariate and multivariate time-series approaches in a nested cross-validation with external data integration. Applied SHAP for model explainability and achieved significant accuracy improvements compared to baseline methods. The solution supported inventory planning and supply chain optimization.

## My Role and Scope

- Designed and implemented univariate and multivariate time-series forecasting models
- Integrated external time-series data sources to improve forecast accuracy
- Applied SHAP (SHapley Additive exPlanations) for model explainability and stakeholder communication
- Evaluated multiple hyperparameter settings and selected optimal model for deployment

## Problem Framing

The client needed accurate demand forecasts to optimize inventory levels and reduce stockouts while minimizing excess inventory costs. Historical demand patterns were influenced by external factors (e.g., market trends, seasonal events) that were not captured in internal data alone. The solution needed to be both accurate and explainable to gain stakeholder trust.

## Approach

The solution combined multiple forecasting approaches with external data integration:

```
Historical Demand Data
    ↓
[Univariate Forecasting]
    ├── ARIMA
    ├── Exponential Smoothing
    └── Prophet
    ↓
[External Data Integration]
    ├── Market Indicators
    ├── Seasonal Events
    └── Economic Factors
    ↓
[Multivariate Forecasting]
    ├── Feature Engineering
    ├── Model Selection
    └── Ensemble Methods
    ↓
[Explainability & Validation]
    ├── SHAP Analysis
    ├── Forecast Intervals
    └── Backtesting
    ↓
Production Forecasts
```

External data sources were carefully selected and validated to ensure they added predictive value without introducing noise.

## Modeling

**Univariate Models**: ARIMA, Exponential Smoothing, and Prophet for baseline forecasts. Used AIC/BIC and cross-validation for model selection.

**Multivariate Models**: Gradient Boosting and LSTM networks that incorporated external features. Compared performance across multiple architectures.

**Evaluation**: Nested cross-validation, measuring accuracy using SMAPE and compared against baseline methods.

**Explainability**: SHAP values to quantify contribution of each feature (including external data) to forecast predictions. This enabled stakeholders to understand model drivers and validate business logic.

## Engineering

- **Pipeline**: Automated forecasting pipeline with retraining and forecast generation
- **Reproducibility**: Version-controlled model parameters, feature definitions, and external data sources

## Outcomes

- Achieved accuracy improvements up to ~50% compared to baseline forecasting methods
- Enabled more accurate inventory planning, reducing stockouts and excess inventory 
- Provided explainable forecasts that gained stakeholder trust and enabled data-driven decision-making
- Integrated external data sources that captured previously unmodeled demand drivers


## Confidentiality Note

This case study has been sanitized to protect client confidentiality. Client names, proprietary data schemas, internal system names, specific KPIs, and identifying business metrics have been removed or generalized. All technical approaches and methodologies are presented at an architecture level without revealing proprietary implementations. The accuracy improvement metric ("up to ~50%") is client-specific and should be interpreted relative to the client's baseline methods.

