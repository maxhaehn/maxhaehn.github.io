# Customer Segmentation

## Summary

Developed a customer segmentation solution for a retail healthcare client to identify distinct customer groups based on behavior. Built a modular preprocessing pipeline, applied K-means clustering, and used Gradient Boosting to extract key drivers of purchase patterns. The solution enabled targeted marketing strategies and improved customer engagement.

## My Role and Scope

- Designed and implemented a modular data preprocessing pipeline for customer data
- Applied K-means clustering to identify distinct customer segments
- Developed Gradient Boosting models to extract purchase-behavior drivers
- Collaborated with client stakeholders to validate segment interpretations
- Delivered actionable insights for marketing and product teams

## Problem Framing

The client needed to understand their customer base beyond aggregate metrics. Traditional demographic segmentation was insufficient for predicting purchase behavior. The goal was to identify homogeneous customer groups based on actual behavioral patterns and understand what drives purchases within each segment.

## Approach

The solution followed a three-stage pipeline:

```
Raw Data
    ↓
[Modular Preprocessing]
    ├── Data Merge
    ├── Feature Engineering
    ├── Aggregation
    └── Normalization
    ↓
[K-means Clustering]
    ├── Elbow Method (k selection)
    └── Segment Profiles
    ↓
[Gradient Boosting Analysis]
    ├── Feature Importance
    ├── Purchase Drivers
    └── Segment Characteristics
    ↓
Business Insights & Recommendations
```

The modular preprocessing pipeline ensured reproducibility and allowed for easy iteration on feature engineering and re-scoring of customers.

## Modeling

**Clustering**: K-means with multiple distance metrics and validation via elbow method. Selected optimal number of clusters based on business interpretability and statistical metrics.

**Driver Analysis**: Gradient Boosting (XGBoost) models trained to predict purchase behavior within each segment. Feature importance analysis revealed key drivers such as product categories, purchase frequency, and seasonal patterns.

**Evaluation**: Validated segments through business stakeholder review, ensuring each segment had distinct and actionable characteristics.

## Engineering

- **Pipeline**: Automated Python pipelines in Kedro with clear separation between preprocessing, modeling, and analysis stages
- **Reproducibility**: Version-controlled and documented feature engineering steps and model parameters

## Outcomes

- Identified distinct customer segments with clear behavioral differences
- Extracted actionable purchase-behavior drivers for each segment
- Enabled targeted marketing campaigns with improved engagement metrics
- Delivered a reusable pipeline for ongoing segmentation analysis


## Confidentiality Note

This case study has been sanitized to protect client confidentiality. Client names, proprietary data schemas, internal system names, specific KPIs, and identifying business metrics have been removed or generalized. All technical approaches and methodologies are presented at an architecture level without revealing proprietary implementations.

