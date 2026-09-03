# GreenRoute Intelligence

### Machine Learning for High-Carbon Business Travel Prediction

GreenRoute Intelligence is an end-to-end machine learning project developed for the **GreenRoute Intelligence Challenge** to predict the probability of business trips being classified as **high-carbon**.

The solution uses travel, cost, location, accommodation, and trip-context features with **XGBoost**.

---

## Objective

Predict the probability that a business trip is `HighCarbon` before the trip occurs.

The model outputs a probability between **0 and 1**, with **ROC-AUC** as the primary evaluation metric.

---

## Approach

- Exploratory Data Analysis
- Feature Engineering
- Categorical Encoding with One-Hot Encoding
- XGBoost Classification
- Probability Prediction
- ROC-AUC, Precision, Recall & F1 evaluation

### Engineered Features

- `CostPerNight`
- `CityPair`
- `CountryPair`
- `DomesticTrip`
- `International`

---

## Leakage Prevention

The following carbon-emission outcome variables are excluded from training:

```text
Departure_CO2e
Return_CO2e
Hotel_CO2e
Spend_CO2e
TotalCO2e
HighCarbon
```

---

## Tech Stack

`Python` · `Pandas` · `Scikit-learn` · `XGBoost` · `Matplotlib` · `Seaborn` · `Jupyter`

---

## Project Structure

```text
greentravel-intelligence/
│
├── data/                 # Challenge datasets (not tracked)
├── notebooks/
│   └── notebook.ipynb
├── results/
│   └── submission.csv
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

> **Note:** Challenge datasets are not included in this repository and must be obtained through the official challenge distribution.

---

## Future Improvements

- Use additional permitted event-log and attribute-table features
- Hyperparameter optimization
- Cross-validation
- Model comparison and ensembling
- SHAP-based explainability

---

## License

This project is licensed under the **MIT License**.

Challenge datasets and materials are not included.