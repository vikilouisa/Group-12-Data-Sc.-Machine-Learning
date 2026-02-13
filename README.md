# Time-Series Sales Forecasting for a Bakery Using Linear Regression and Neural Networks

## Repository Link

https://github.com/vikilouisa/Group-12-Data-Sc.-Machine-Learning

## Description

This project aims to predict daily sales (Umsatz) of a bakery using machine learning methods. 
The dataset includes historical sales data across multiple product groups (Warengruppe), enriched with weather data and calendar-based features.

The prediction task is a supervised regression problem with a strict time-based train/validation/test split:

- Train: 01.07.2013 – 31.07.2017  
- Validation: 01.08.2017 – 31.07.2018  
- Test: 01.08.2018 – 31.07.2019  

The goal is to forecast sales values for the test period where the target variable is not provided.

Two modeling approaches were implemented:

1. Linear Regression (baseline model)
2. Feedforward Neural Networks (per product group)

Feature engineering plays a central role in the modeling process, including lag features, rolling statistics, seasonal transformations, and holiday indicators.


### Task Type

[For the Baseline Model we used linear regression For the Neural Net we used the model of a feedforward neural net.]

### Results Summary

#### Best Model Performance
- **Best Model:** [Name and type of the best-performing model"]
- **Evaluation Metric:** [Primary metric used, e.g., Accuracy, F1-Score, MSE, MAE]
- **Final Performance:** [Best score achieved, e.g., 95% accuracy, F1-score of 0.87, MSE of 0.12]

#### Model Comparison
- **Baseline Performance:** [Baseline model performance for comparison]
- **Improvement Over Baseline:** [Quantitative improvement, e.g., "+12% accuracy", "25% reduction in MSE"]
- **Best Alternative Model:** [Second-best model and its performance]

#### Key Insights
- **Most Important Features:** [Top 3-5 features that drive model performance]
- **Model Strengths:** [What the model does well]
- **Model Limitations:** [Known limitations and failure cases]
- **Business Impact:** [Practical implications of the model performance]

## Documentation

1. **[Literature Review](0_LiteratureReview/README.md)**
2. **[Dataset Characteristics](1_DatasetCharacteristics/exploratory_data_analysis.ipynb)**
3. **[Baseline Model](2_BaselineModel/baseline_model.ipynb)**
4. **[Model Definition and Evaluation](3_Model/model_definition_evaluation)**
5. **[Presentation](4_Presentation/README.md)**

## Cover Image

![Project Cover Image](CoverImage/Cover_Alle_Folien_1920x1080.png)
