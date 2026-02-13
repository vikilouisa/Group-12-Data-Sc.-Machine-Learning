# Literature Review

This section reviews academic and practical literature related to retail sales forecasting, time-series regression, and neural-network-based demand prediction. The objective is to contextualize the methodological choices made in this project and relate them to established forecasting approaches.

---

## Source 1: Da Veiga et al. (2014)  
**“Demand forecasting in food retail: A comparison between the Holt-Winters and ARIMA models.”:**

- **Objective:**  
  The study compares two classical time-series forecasting methods — ARIMA and Holt-Winters — for predicting demand of perishable food products in retail.

- **Methods:**  
  The authors apply ARIMA(p,d,q) and multiplicative Holt-Winters models to historical sales data and evaluate performance using MAPE and U-Theil metrics.

- **Outcomes:**  
  The Holt-Winters model slightly outperformed ARIMA in this specific retail setting, but both models achieved high forecasting accuracy. The study confirms that no forecasting method is universally superior and that performance depends on data characteristics such as seasonality and volatility.

- **Relation to the Project:**  
  This paper provides a strong classical baseline for retail demand forecasting and supports the importance of seasonality modeling and evaluation via MAPE. It justifies our time-series-aware feature engineering approach and highlights the importance of empirical model comparison.

---

## Source 2: Huber & Stuckenschmidt (2020)  
**“Daily retail demand forecasting using machine learning with emphasis on calendric special days.”:**

- **Objective:**  
  The study investigates machine learning approaches for daily retail demand forecasting, with particular focus on calendric special days and event-based predictors.

- **Methods:**  
  Various machine learning models are trained on retail sales data enriched with calendric features such as holidays and special events. The performance of these models is compared to traditional statistical forecasting approaches.

- **Outcomes:**  
  The results show that incorporating special-day indicators significantly improves forecasting accuracy. Machine learning models outperform classical models when relevant temporal and event-based features are included.

- **Relation to the Project:**  
  This study directly supports our inclusion of public holidays, school holidays, and Kieler Woche as explanatory variables. It provides academic justification for our feature-engineering strategy and the use of machine learning models in retail forecasting.

---

## Source 3: Albon (2019)  
**“Machine Learning Kochbuch – praktische Lösungen mit Python.”:**

- **Objective:**  
  To provide practical guidance for implementing machine learning techniques, particularly data preprocessing and baseline modeling.

- **Methods:**  
  The KNN chapter was used to implement KNN-based missing-data imputation and establish a baseline comparison model. Neural network chapters were reviewed to consolidate understanding of architecture and training principles.

- **Outcomes:**  
  The source enabled the successful implementation of imputation strategies and reinforced understanding of activation functions and training mechanisms.

- **Relation to the Project:**  
  This source supported the early methodological setup by providing concrete procedures for preprocessing and baseline modeling.

---

## Source 4: Scarpino (2018)  
**“TensorFlow für Dummies.”:**

- **Objective:**  
  To provide an accessible introduction to TensorFlow workflows and neural network training processes.

- **Methods:**  
  Chapters on optimizers, dropout, and regularization were consulted to structure the neural network training process and parameter selection.

- **Outcomes:**  
  The source supported systematic implementation of the feedforward neural network and improved understanding of training dynamics.

- **Relation to the Project:**  
  This source contributed to the practical realization of the neural-network workflow, particularly regarding optimizer choice and regularization techniques.

---

## Source 5: Raschka & Mirjalili (2018)  
**“Machine Learning with Python and Scikit-Learn and TensorFlow.”:**

- **Objective:**  
  To provide a theoretically grounded overview of machine-learning algorithms and neural-network architectures.

- **Methods:**  
  Chapters on linear regression and neural networks were used to understand regression assumptions, activation functions such as ReLU, and regularization strategies.

- **Outcomes:**  
  The source provided conceptual understanding of bias–variance trade-offs and supported informed architectural decisions.

- **Relation to the Project:**  
  This source supports the theoretical justification of our modeling choices, including:
  - Use of linear regression as a baseline  
  - Selection of ReLU activation  
  - Application of dropout and regularization to prevent overfitting  

---

## Overall Synthesis

Across the reviewed literature, three key insights emerge:

1. **Retail demand forecasting is highly data-dependent**, and no single method consistently outperforms others.  
2. **Seasonality, lag structures, and calendric features are essential components** in time-series-based sales prediction.  
3. **Machine learning models can outperform classical models** when nonlinear relationships and special-day effects are properly captured.

These findings directly informed our project design:

- Implementation of lag and rolling-window features  
- Inclusion of holiday and event indicators  
- Separate modeling per product group  
- Comparison between linear regression and neural networks  
- Validation using R² and error-based metrics  

By combining classical time-series foundations with machine-learning approaches, this project aligns with established research while exploring modern forecasting techniques.
