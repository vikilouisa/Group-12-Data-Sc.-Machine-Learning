# Literature Review

This section reviews academic and practical literature related to retail sales forecasting, time-series regression, and neural-network-based demand prediction. The objective is to contextualize the methodological choices made in this project and relate them to established forecasting approaches.

---

## Source 1: Da Veiga et al. (2014)  
**Da Veiga, L., Amaral, R., & Faria, F. (2014). Demand forecasting in food retail: A comparison between the Holt–Winters and ARIMA models. WSEAS Transactions on Business and Economics, 11, 608–614**

- **Objective:**  
  The study compares two classical time-series forecasting methods — ARIMA and Holt-Winters — for predicting demand of perishable food products in retail environments, where short product life cycles and volatile demand patterns make accurate forecasting critical for operational decisions.

- **Methods:**  
  Da Veiga et al. apply ARIMA(p,d,q) and multiplicative Holt-Winters models to historical sales data and evaluate performance using Mean Absolute Percentage Error (MAPE) and the Theil inequality index (U-Theil metrics), enabling a quantitative comparison of model performance.

- **Outcomes:**  
  The Holt-Winters model slightly outperformed ARIMA in this specific retail setting, but both models achieved high forecasting accuracy. The study confirms that no forecasting method is universally superior and that performance depends on data characteristics such as seasonality and volatility.

- **Relation to the Project:**  
  This paper provides a strong classical baseline for retail demand forecasting and supports the importance of seasonality modeling and evaluation via MAPE. It justifies our time-series-aware feature-engineering approach and highlights the importance of empirical model comparison.

---

## Source 2: Huber & Stuckenschmidt (2020)  
**Huber, J., & Stuckenschmidt, H. (2020). Daily retail demand forecasting using machine learning with emphasis on calendric special days. International Journal of Forecasting, 36, 1420-1438**

- **Objective:**  
  The study investigates machine learning approaches for daily retail demand forecasting, with particular focus on calendric special days and event-based predictors on sales patterns.

- **Methods:**  
  Different model families, including artificial neural networks and gradient-boosted decision trees, are evaluated using retail sales data enriched with calendric features such as public holidays and special events. The performance of these models is compared to traditional statistical forecasting approaches and to conventional regression-based approaches.

- **Outcomes:**  
  The results show that incorporating special-day indicators significantly improves forecasting accuracy. Machine learning models outperform classical models when relevant temporal and event-based features are included - especially for large-scale retail forecasting scenarios.

- **Relation to the Project:**  
  This study directly supports our inclusion of public holidays, school holidays, and Kieler Woche as explanatory variables. It provides academic justification for our feature-engineering strategy and the use of machine learning models in retail forecasting.

---

## Source 3: Albon (2019)  
**Albon, C. (2019). Machine Learning Kochbuch – praktische Lösungen mit Python: Von der Vorverarbeitung der Daten bis zum Deep Learning (Frank Langenau, Trans.). Heidelberg: O’Reilly & dpunkt.verlag.**

- **Objective:**  
  To provide practical guidance for implementing common machine learning techniques, particularly data preprocessing and baseline modeling.

- **Methods:**  
  The KNN chapter (pp. 245-252) was used to implement KNN-based missing-data imputation and establish a baseline comparison model. Selected parts of the neural network chapter (pp. 291-296, 299-312) were reviewed to consolidate understanding of architecture and training principles.

- **Outcomes:**  
  The source enabled the successful implementation of imputation strategies and reinforced understanding of activation functions and training mechanisms.

- **Relation to the Project:**  
  Albon (2019) supported the early methodological setup by providing concrete procedures for preprocessing and baseline modeling. It enriched the theoretical background needed to interpret course materials and external resources, ensuring that the project’s methodological choices were grounded in a broader understanding of machine‑learning techniques.

---

## Source 4: Scarpino (2018)  
**Scarpino, M. (2018). TensorFlow für Dummies. Weinheim: Wiley-VCH Verlag**

- **Objective:**  
  To provide an accessible introduction to TensorFlow workflows and neural network training processes and to establish a coherent understanding of standard training workflows, optimization strategies, and model configuration principles.

- **Methods:**  
  Chapter 5 was used to clarify core training parameters such as epochs, steps, learning rates, and optimizers, with particular emphasis on the Adam optimizer. Chapter 7 informed the use of regularization and dropout techniques to improve model generalization. Chapter 15 provided a structured overview of a typical TensorFlow training pipeline, which guided the overall implementation process.

- **Outcomes:**  
  The source enabled systematic interpretation of training dynamics, supported deliberate selection of optimizers and regularization methods, and facilitated tuning of training parameters. Its accessible explanations also aided error diagnosis and debugging during implementation.

- **Relation to the Project:**  
  Scarpino (2018) contributed to the practical realization of the neural-network workflow, particularly regarding optimizer choice and regularization techniques. It served as a methodological complement to course materials by explaining the reasoning behind common design and training choices.

---

## Source 5: Raschka & Mirjalili (2018)  
**Raschka, S. & Mirjalili, V. (2018, 2nd ed.). Machine Learning mit Python und Scikit‑Learn und TensorFlow – Das umfassende Praxis‑Handbuch für Data Science, Deep Learning und Predictive Analytics (Knut Lorenzen, Trans.). Frechen: mitp‑Verlag.**

- **Objective:**  
  To provide a theoretically grounded overview of machine-learning algorithms and neural-network architectures, with emphasis on regression techniques, activation functions, and model regularization.

- **Methods:**  
  Chapter 10 was used as guidance on linear regression techniques, while Chapters 12 and 13 informed the understanding of neural-network architectures and TensorFlow-based training workflows. In particular, the overview of activation functions in Chapter 13.4 (p. 450) was used to evaluate and compare common activation functions, supporting the selection of ReLU as an appropriate activation function for the project’s model.

- **Outcomes:**  
  The activation-function comparison supported a well-reasoned selection of ReLU and deepened understanding of how different functions affect learning behavior and convergence. The source also provided conceptual clarity on bias–variance trade-offs and regularization strategies. Additional case studies illustrated advanced optimization and tuning approaches; however, these were reviewed but not adopted due to the project’s scope (e.g., the breast-cancer case study in Chapter 6 demonstrating extensive optimization possibilities).

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
