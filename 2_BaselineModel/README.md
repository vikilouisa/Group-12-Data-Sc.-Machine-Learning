# Baseline Model

**[Notebook](baseline_model.ipynb)**

## Baseline Model Results

### Model Selection
- **Baseline Model Type:** Linear Regression
- **Rationale:** Linear regression was selected as the baseline model because it provides a transparent and interpretable framework for evaluating the predictive power of engineered time-series features. As a regression-based forecasting approach, it allows us to assess whether sales patterns can be sufficiently explained through linear relationships between lag variables, seasonal indicators, and calendar-based features. Establishing this benchmark enables a structured comparison with more complex models in later stages of the project.

### Model Performance
- **Evaluation Metric:** R² and Adjusted R² 
- **Performance Score:** Validation R² per Warengruppe:
   - WG1: 0.476  
  - WG2: 0.862  
  - WG3: 0.848  
  - WG4: 0.182  
  - WG5: 0.248  
  - WG6: 0.552
- **Cross-Validation Score:** was not applied

### Evaluation Methodology
- **Data Split:** Train/Validation/Test split ratio 67,2/16,4/16,4
- **Evaluation Metrics:**
  - **R² (Coefficient of Determination):** Measures the proportion of variance in daily sales explained by the model.  
  - **Adjusted R²:** Accounts for the number of predictors and penalizes unnecessary complexity.
  - A time-based split ensures that future information is not used in training, thereby preventing data leakage and maintaining realistic forecasting conditions.

### Metric Practical Relevance
R² values provide insight into how reliably demand patterns can be modeled for each product group.

- High explanatory power in WG2 and WG3 indicates stable and predictable demand behavior.
- Moderate results in WG1 and WG6 suggest partially structured but more volatile demand.
- Lower values in WG4 and WG5 point to higher noise levels or irregular purchasing patterns.

From a business perspective, higher predictive accuracy improves planning reliability for inventory management and staffing decisions, while lower performance highlights areas where more advanced modeling techniques may be necessary.

## Next Steps
The linear regression model establishes a performance benchmark. In the next phase, more advanced machine learning approaches will be evaluated to determine whether nonlinear modeling can capture additional structure in the data and improve forecasting accuracy beyond this baseline. Further info can be found in the [Model Definition and Evaluation](../3_Model/README.md) phase.

