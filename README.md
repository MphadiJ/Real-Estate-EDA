# Housing Price Exploratory Data Analysis (EDA)

This repository contains the Exploratory Data Analysis (EDA) framework for analyzing housing market factors. The goal of this analysis is to profile structural features, utilities, and geographic indicator variables to isolate the primary macro cost drivers that influence real estate pricing valuation models.

## Dataset Profile & Dictionary

The dataset consists of target financial transaction entries mapping structural features and binary categorical utility attributes.

| Feature Column | Data Type | Description |
| :--- | :--- | :--- |
| **price** | Numerical (Target) | The transaction price of the house. |
| **area** | Numerical | Total square footage footprint of the property. |
| **bedrooms** | Numerical | Total count of bedroom units. |
| **bathrooms** | Numerical | Total count of bathroom units. |
| **stories** | Numerical | Number of floor levels/stories. |
| **mainroad** | Categorical (Yes/No) | Access indicator to a primary main road asset. |
| **guestroom** | Categorical (Yes/No) | Presence of a dedicated guestroom unit. |
| **basement** | Categorical (Yes/No) | Presence of a structural basement foundation. |
| **hotwaterheating**| Categorical (Yes/No) | Dedicated gas/electric hot water heating utility. |
| **airconditioning**| Categorical (Yes/No) | Presence of central or localized air conditioning. |
| **parking** | Numerical | Count of dedicated vehicle parking garage bays. |
| **prefarea** | Categorical (Yes/No) | Indicator if the property is located in a preferred urban sector. |
| **furnishingstatus**| Categorical (String) | Structural furnishing state (`furnished`, `semi-furnished`, `unfurnished`). |

## EDA Execution Map

The diagnostic codebase evaluates features across four execution steps:

1. **Structural Metadata & Quality Audit:**
   * Evaluation of missing structural loops (`df.info()`, `df.isna().sum()`).
   * Identification of target distribution skewness in property pricing parameters.
2. **Univariate Assessment:**
   * Target variable variance analysis utilizing density plots and box plots to isolate pricing outliers.
   * Distribution count tracking across structural variables (`stories`, `parking`, `bedrooms`).
3. **Multivariate & Correlation Matrices:**
   * Encoding categorical text variables to compute a clean Pearson Correlation Matrix.
   * Scatter plots tracking target `price` behaviors relative to continuous spatial parameters (`area`).
4. **Categorical Feature Segregation:**
   * Categorical box-plot segmentation comparing value distributions across high-impact flags like `airconditioning`, `prefarea`, and `furnishingstatus`.

## Project Directory
```text
├── data/
│   └── housing_dataset.csv     # Raw housing entry rows
├── notebooks/
│   └── housing_eda_sandbox.ipynb # Interactive exploration workspace


├── requirements.txt            # Dependency configuration manifest
└── README.md
