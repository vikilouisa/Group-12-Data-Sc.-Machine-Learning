# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**

## Dataset Information

### Dataset Source

- **Dataset Link:** https://github.com/vikilouisa/Group-12-Data-Sc.-Machine-Learning/tree/main/1_DatasetCharacteristics/Dataset_Sources

### Dataset Characteristics

- **Number of Observations:** 9,334 entries in the primary sales dataset; after merging with a full daily calendar, the dataset contains 14,277 rows at daily resolution.
- **Number of Features:** 4 raw features in the original sales data (id, date, product group, revenue). After merging with weather and calendar data, the dataset contains a total of 11 variables.

### Target Variable/Label

- **Label Name:** Umsatz
- **Label Type:** Regression
- **Label Description:** Daily sales revenue (in €) of a bakery, disaggregated by product group. The objective is to predict future daily sales per product group.
- **Label Values:** Continuous positive numerical values (float), ranging from 7.05 (product group 6) to 1,879.46 (product group 5).
- **Label Distribution:** Sales levels vary substantially across product groups. Product group 6 is only observed in November and December, representing a structural class imbalance within the dataset.
  
### Feature Description

- **Feature 1 (id):** Unique numerical ID for each record, composed of date (YYMMDD) and product group.
- **Feature 2 (date):** Date of sale (datetime format), recorded at daily resolution. Observation period: 01.07.2013 – 31.07.2019.
- **Feature 3 (Warengruppe):** Product group encoded as an integer category (1–6). Group 6 is only available in November and December, which introduces structural imbalance.
- **Weather Feature Group (Bewoelkung, Temperatur, Windgeschwindigkeit, Wettercode):** Daily weather variables. Missing values were imputed using time-based methods: linear interpolation for Temperatur and Windgeschwindigkeit, rounded interpolation for Bewoelkung, and forward/backward filling for the categorical Wettercode.
- **Calendar Feature Group (KielerWoche, school_holiday, public_holiday):** Binary indicator variables (0/1) representing whether a day falls within Kieler Woche, school holidays (Schleswig-Holstein), or a public holiday. Missing values were set to 0.

## Exploratory Data Analysis

The exploratory data analysis is conducted in the [exploratory_data_analysis.ipynb](exploratory_data_analysis.ipynb) notebook and includes:

- Data loading and initial inspection
- Statistical summaries and distribution analysis
- Missing value analysis
- Variable correlation analysis
- Data visualization and insights
- Data quality assessment
