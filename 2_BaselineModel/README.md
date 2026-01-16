# Baseline Model

**[Notebook](baseline_model.ipynb)**

## Baseline Model Results

### Model Selection
- **Baseline Model Type:** Linear Regression
- **Rationale:** [Before building a neural net, it is useful to start with a simple Baseline Model first – like the linear regression – to check the plausibility and to have an understanding of the data, also to initialize and scale the data, so it is possible to check the quality of the (implemented) features. Maybe the data is linear so there wouldn’t be a use of the Neural Net (resource-efficiency). The optimization used in the Baseline Model is also helpful to improve the Neural Net if the Neural Net doesn’t have any hidden layers. Furthermore, the linear regression in the Baseline Model can be used as helpful debugging tool.]

### Model Performance
- **Evaluation Metric:** [e.g., Accuracy, F1-Score, Precision, Recall, MSE, MAE, R², etc.]
- **Performance Score:** [e.g., 85% accuracy, F1-score of 0.78, MSE of 0.15]
- **Cross-Validation Score:** [Mean and standard deviation of CV scores, e.g., 0.82 ± 0.03]

### Evaluation Methodology
- **Data Split:** Train/Validation/Test split ratio 67,2/16,4/16,4
- **Evaluation Metrics:** [List all metrics used and justify why they are appropriate for this problem]

### Metric Practical Relevance
[Explain the practical relevance and business impact of each chosen evaluation metric. How do these metrics translate to real-world performance and decision-making? What do the metric values mean in the context of your specific problem domain?]

## Next Steps
This baseline model serves as a reference point for evaluating more sophisticated models in the [Model Definition and Evaluation](../3_Model/README.md) phase.
