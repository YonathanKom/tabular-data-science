# Song Popularity Prediction

This project is part of my **Tabular Data Science** class and focuses on predicting the popularity of songs using their audio features. The project explores the relationships between features such as danceability, tempo, energy, acousticness, and popularity while leveraging machine learning techniques to develop a robust model.  

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [File Structure](#file-structure)
3. [Usage](#usage)
4. [Approach](#approach)
5. [Results](#results)
6. [Acknowledgements](#acknowledgements)

---

## Project Overview

The goal of this project is to predict the `song_popularity` score (ranging from 0 to 100) based on a dataset of audio features. Two Jupyter notebooks form the core of this project:

- **TDS_project.ipynb**: Focuses on initial data exploration, visualization, and building a basic machine learning model. It also visualizes the performance of the baseline model.
- **Part_2.ipynb**: Refines the baseline model, introduces advanced techniques (outlier handling, data balancing, and hyperparameter tuning), and analyzes feature importance.

This project uses an `XGBoost` regressor as the primary machine learning model, supported by preprocessing, feature engineering, and visualization.

---

## File Structure

The project contains the following files:

- **TDS_project.ipynb**: Handles data visualization, preprocessing, and building a baseline model.
- **Part_2.ipynb**: Improves upon the baseline by implementing advanced modeling techniques.
- **requirements.txt**: Lists all dependencies needed to run the project.
- **README.md**: Documentation for the project.

---

## Usage

1. **TDS_project.ipynb**:
   - Visualizes the dataset.
   - Performs basic preprocessing, feature engineering, and builds a baseline model.
   - Evaluates the model with simple metrics and visualizations.

2. **Part_2.ipynb**:
   - Implements advanced techniques:
     - Handles outliers.
     - Balances the target variable using `SMOTE`.
     - Optimizes hyperparameters using `RandomizedSearchCV`.
   - Evaluates model performance with improved metrics.
   - Explores feature importance using SHAP values and permutation importance.

---

## Approach

### TDS_project.ipynb: 
- **Data Exploration & Visualization**: 
  - Explores distributions of features like `tempo`, `danceability`, and `energy`.
  - Visualizes correlations between features and song popularity.
  
- **Baseline Model**:
  - Builds an `XGBoost` regressor with default parameters.
  - Evaluates performance using RMSE, MAE, and R².

### Part_2.ipynb: 
- **Advanced Techniques**:
  - **Outlier Handling**: Caps extreme values in numerical features to reduce noise.
  - **Data Balancing**: Uses `SMOTE` to balance the target variable by oversampling underrepresented categories.
  - **Hyperparameter Tuning**: Optimizes model parameters using `RandomizedSearchCV`.

- **Feature Importance Analysis**:
  - SHAP values highlight the contribution of each feature to predictions.
  - Permutation importance confirms the impact of key features.

---

## Results

1. **Baseline Model**:
   - RMSE: *18.6121*
   - R²: *0.2814*
   
2. **Improved Model**:
   - RMSE: *17.7321*
   - R²: *0.3478*

The improved model outperforms the baseline by effectively leveraging feature engineering, data balancing, and hyperparameter tuning.

---

## Acknowledgements

This project is part of my **Tabular Data Science** class. A special thanks to **ChatGPT**, which was instrumental in guiding me through the process, refining code, and ensuring quality documentation.

This project uses the following libraries and tools:
- **Data Analysis**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`, `shap`
- **Machine Learning**: `scikit-learn`, `xgboost`, `imblearn`

Inspired by the intersection of music and data science to uncover the secrets behind popular songs. Feel free to contribute or open issues for improvements!
