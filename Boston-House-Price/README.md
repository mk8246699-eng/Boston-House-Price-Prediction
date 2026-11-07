# Boston House Price Prediction

## Project Overview

This project focuses on predicting Boston house prices using Machine Learning regression models. The dataset contains different features related to housing, such as the number of rooms, crime rate, and other factors that may affect house prices.

The main objective is to preprocess the data, train regression models, evaluate their performance, and identify the best-performing model.

## Dataset

- **File:** `HousingData.csv`
- **Target variable:** `MEDV`
- **Features:** 13 input features related to housing and neighbourhood conditions.
- **Dataset size:** 506 rows and 14 columns.

## Steps Performed

### 1. Data Preprocessing
- Loaded the dataset using Pandas.
- Checked the dataset for missing values.
- Handled missing numerical values using median imputation.
- Handled missing values in the `CHAS` column using most frequent value imputation.
- Split the data into training and testing sets.

### 2. Exploratory Data Analysis (EDA)
- Examined the dataset using descriptive statistics.
- Studied the distribution of house prices.
- Created visualizations to understand feature relationships and correlations.
- Explored the relationship between important features and house prices.

### 3. Model Training

The following regression models were implemented:

- Linear Regression
- Decision Tree Regressor
- Gradient Boosting Regressor

### 4. Model Evaluation

The models were evaluated using Mean Squared Error (MSE) and R² Score.

| Model | MSE | R² Score |
|---|---:|---:|
| Linear Regression | 24.9834 | 0.6593 |
| Decision Tree Regressor | 23.8863 | 0.6743 |
| Gradient Boosting Regressor | 7.2950 | 0.9005 |

Gradient Boosting Regressor achieved the lowest MSE and highest R² Score among the three models on the test set.

### 5. Model Saving and Testing

The best-performing model was saved using Joblib.

**Saved model path:** `models/best_house_price_model.pkl`

The saved model was loaded again and tested with a sample from the test dataset to verify that it could generate predictions.

## Technologies and Libraries Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

## Project Structure

```text
Boston-House-Price-Prediction/
│
├── datasets/
│   └── HousingData.csv
│
├── notebooks/
│   └── 01_boston_house_price.ipynb
│
├── models/
│   └── best_house_price_model.pkl
│
├── images/
│
└── README.md
```

## How to Run the Project

1. Clone or download this repository.
2. Open the project folder in VS Code.
3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

4. Open `notebooks/01_boston_house_price.ipynb`.
5. Run the notebook cells in order.

## Conclusion

This project demonstrates the use of regression techniques for Boston house price prediction. After preprocessing the dataset, performing exploratory data analysis, and comparing three regression models, Gradient Boosting Regressor gave the best results.

The final model was saved and successfully tested by loading it again and generating a sample prediction.