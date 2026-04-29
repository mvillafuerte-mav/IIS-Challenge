# IIS-Challenge
Fuel Optimization for Transportation Fleets

## Overview

A major Mexican transportation company operating **1,000+ trucks** and **4,100+ trailers** nationwide presented us with a challenge: **fuel represents 30% of their total operating costs**, and there is significant variability in consumption between trips under similar conditions.

Our goal is to identify the root causes of this variability, build a predictive model for expected fuel consumption, and propose actionable strategies to reduce waste - translating every insight into measurable economic impact.

## Problem Statement

Trips on the same route (**Puebla → Cuautitlán Izcalli**, ~165 km) with comparable loads show inconsistent fuel efficiency (km/L). This variability leads to unpredictable costs and missed optimization opportunities across the fleet.

**Key question:** *What factors drive fuel consumption differences between similar trips, and how can we standardize performance to the most efficient levels?*

## Dataset

| Attribute | Detail |
|-----------|--------|
| Records | 76 trips |
| Route | Puebla – Cuautitlán Izcalli |
| Period | *(to be confirmed from data)* |

### Variables

| Variable | Description | Type |
|----------|-------------|------|
| `Remision` | Trip ID / shipment reference | Categorical |
| `Unidad` | Truck unit identifier | Categorical |
| `Operador` | Driver identifier | Categorical |
| `Ruta` | Route name | Categorical (single value) |
| `Fecha_Inicio` | Trip start date | Date |
| `Fecha_Fin` | Trip end date | Date |
| `Inicio_Hora` | Departure time | Time |
| `Fin_Hora` | Arrival time | Time |
| `km` | Distance traveled | Numeric (continuous) |
| `Litros` | Fuel consumed | Numeric (continuous) |
| `Rend` | Fuel efficiency (km/L) | Numeric (continuous) |
| `peso` | Load weight | Numeric (continuous) |

## Project Structure

```
├── data/
│   ├── raw/                    # Original dataset (not tracked)
│   ├── processed/              # Cleaned and enriched data
│   └── external/               # Diesel prices, weather data
│
├── notebooks/
│   ├── 01_business_understanding.md
│   ├── 02_data_understanding.ipynb
│   ├── 03_data_preparation.ipynb
│   ├── 04_modeling.ipynb
│   └── 05_evaluation.ipynb
│
├── src/
│   ├── data_processing.py      # Cleaning and feature engineering
│   ├── modeling.py             # Model training and evaluation
│   └── utils.py                # Helper functions
│
├── reports/
│   ├── figures/                # Charts and visualizations
│   └── final_presentation.pptx
│
├── .gitignore
├── requirements.txt
└── README.md
```

### Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
scikit-learn>=1.3
scipy>=1.11
openpyxl>=3.1
```