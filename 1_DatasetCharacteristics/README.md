# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**

## Dataset Information

### Dataset Source
- **Dataset Link:** https://github.com/vikilouisa/Group-12-Data-Sc.-Machine-Learning/tree/main/1_DatasetCharacteristics/Dataset_Sources

### Dataset Characteristics
- **Number of Observations:** 9,334 entries in the primary sales data; after full calendar merge 14,277 rows; daily resolution.
- **Number of Features:** 4 raw features in the original sales data (id, date, product group, revenue); after merging with weather and calendar data a total of 11 features.

### Target Variable/Label
- **Label Name:** Umsatz
- **Label Type:** Regression
- **Label Description:** Daily sales (revenue in €) of a bakery, broken down by product group. The goal is to predict future sales per day and product group.
- **Label Values:** Continuous positive decimals (float); range from 7.05 (in product group 6) to 1,879.46 (in product group 5).
- **Label Distribution:** Sales vary significantly between product groups. Product group 6 is structurally underrepresented, as it is only available in November and December.

### Feature Description
[Provide a brief description of each feature or group of features in your dataset. If you have many features, group them logically and describe each group. Include information about data types, ranges, and what each feature represents.]

- **Feature 1 (id):** Unique numerical ID for each record, composed of date (YYMMDD) and product group.
- **Feature 2 (date):** Date of sale, type datetime, daily resolution. Period: 01.07.2013 – 31.07.2019.
- **Feature 3 (Warengruppe):** Product group as an integer category (1–6). Group 6 is only available in Nov./Dec., which represents a structural class imbalance.
- **Weather Feature Group (Bewoelkung, Temperatur, Windgeschwindigkeit, Wettercode):** Daily weather data. Missing values ​​were imputed via time-based interpolation (linear interpolation for Temperatur and Windgeschwindigkeit, rounded interpolation for Bewoelkung, forward/backward filling for the categorical Wettercode).
- **Calendar Feature Group (KielerWoche, school_holiday, public_holiday):** Binary indicator variables (0/1) that indicate whether a day falls within Kieler Woche, school holidays (Schleswig-Holstein), or a public holiday. Missing values ​​were filled with 0.

## Exploratory Data Analysis

The exploratory data analysis is conducted in the [exploratory_data_analysis.ipynb](exploratory_data_analysis.ipynb) notebook, which includes:

- Data loading and initial inspection
- Statistical summaries and distributions
- Missing value analysis
- Feature correlation analysis
- Data visualization and insights
- Data quality assessment
