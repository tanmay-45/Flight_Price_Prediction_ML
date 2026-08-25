# Flight Price Prediction using Machine Learning

## Overview

This project develops a machine learning regression model to predict flight ticket prices from flight-related attributes such as airline, journey date, source, destination, route, departure time, arrival time, duration, and number of stops.

The project follows an end-to-end workflow covering data loading, exploratory data analysis, feature engineering, categorical encoding, model training, model comparison, and Random Forest hyperparameter tuning.

## Business Problem

Flight prices vary based on multiple factors including airline, travel date, route, duration, and number of stops. The objective of this project is to build a machine learning model that can learn these relationships and estimate flight ticket prices.

## Objectives

- Explore the flight-fare dataset and identify important patterns.
- Clean and preprocess date, time, categorical, and numerical features.
- Perform feature engineering on journey and time-related variables.
- Encode categorical variables for machine learning.
- Train and compare multiple regression algorithms.
- Tune the Random Forest model.
- Select the best-performing model using R² score.

## Dataset

The notebook uses a flight-fare dataset containing fields including:

- Airline
- Date of Journey
- Source
- Destination
- Route
- Departure Time
- Arrival Time
- Duration
- Total Stops
- Additional Information
- Price (target)

The original notebook loads the dataset from an Excel file. For GitHub, the expected repository path is:

`data/Flight_Fare.xlsx`

The dataset itself is not included in this package because only the notebook was provided.

## Feature Engineering

The project transforms date and time information into machine-learning-friendly features. The notebook extracts components such as:

- Journey day
- Journey month
- Departure hour
- Departure minute
- Arrival hour
- Arrival minute
- Duration-related information

Categorical variables are encoded before model training.

## Models

Three regression models are compared:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor

### Model Comparison

| Model | R² Score |
|---|---:|
| Linear Regression | 0.759502 |
| Decision Tree | 0.872371 |
| Random Forest | **0.920877** |

Random Forest performed best among the models evaluated, achieving an R² score of approximately **0.921** on the test set.

## Hyperparameter Tuning

After comparing the baseline models, Random Forest hyperparameter tuning is performed to search for improved model settings.

The tuned Random Forest is treated as the final model in the GitHub-ready notebook.

## Key Findings

- Random Forest outperformed Linear Regression and Decision Tree on the test-set R² comparison.
- Flight price prediction benefits from combining airline, route, duration, source/destination, and time-related features.
- Feature engineering from date and time variables is an important part of the modeling workflow.
- Comparing multiple algorithms provides a stronger basis for model selection than relying on a single model.

## Repository Structure

```text
Flight_Price_Prediction_ML/
│
├── notebook/
│   └── Flight_Price_Prediction.ipynb
│
├── README.md
├── requirements.txt
├── .gitignore
└── .gitattributes
```

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/flight-price-prediction-ml.git
cd flight-price-prediction-ml
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add the dataset

Place `Flight_Fare.xlsx` inside:

```text
data/
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook inside the `notebook/` directory and run the cells.

## Limitations

- The model performance is based on the dataset used in the notebook.
- Flight prices can change because of factors that may not be represented in the available features.
- The project is a predictive modeling exercise and should not be interpreted as a live airline pricing system.
- Reproducibility requires access to the original dataset.

## Future Improvements

- Add a stronger cross-validation strategy for model comparison.
- Compare additional boosting algorithms.
- Build a reusable prediction pipeline.
- Add a Streamlit or Flask interface for interactive predictions.
- Add model monitoring and retraining workflows for changing flight-price patterns.

## Author

**Tanmay Hanmant Kanase**

This project is part of a machine learning portfolio focused on practical predictive modeling, exploratory data analysis, feature engineering, and model evaluation.
