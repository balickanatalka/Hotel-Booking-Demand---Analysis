# Hotel Booking Demand – Data Science Project

Analysis of hotel booking data using exploratory data analysis, statistical testing, predictive modeling, decision trees and clustering.


Data analysis and machine learning project based on the **Hotel Booking Demand** dataset.

The project covers the complete analytical workflow: data preprocessing, exploratory data analysis, statistical inference, regression, classification and clustering.

## Dataset

Dataset source:

[Hotel Booking Demand – Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand?resource=download)

The original dataset contains over **119,000 hotel reservations** and 32 variables describing bookings for City Hotel and Resort Hotel.

Approximately **37% of reservations were cancelled**, therefore cancellation behaviour became one of the main areas investigated in the project.

## Project Structure

### 1. Data Preprocessing and Exploratory Data Analysis

- missing-value analysis and data cleaning
- outlier analysis
- feature engineering
- exploratory data analysis
- cancellation patterns and correlations

The cleaned dataset contains **119,205 observations**.

Key findings:
- City Hotel cancellation rate: ~41.8%
- Resort Hotel cancellation rate: ~27.8%
- cancelled bookings had a considerably longer average lead time
- lead time showed the strongest positive numerical correlation with cancellation

### 2. Hypothesis Testing and Statistical Inference

Three statistical tests were performed:

- one-sample proportion z-test
- Welch's independent samples t-test
- Chi-square test of independence

All three tests produced statistically significant results at `α = 0.05`.

### 3. Predictive Modelling and Regression Analysis

Two regression approaches were analysed:

- **Multiple Linear Regression** for predicting ADR
- **Binary Logistic Regression** for predicting booking cancellation

Selected results:

- Linear Regression R²: **0.187**
- Logistic Regression Accuracy: **~81%**
- Logistic Regression ROC-AUC: **~0.889**

### 4. Decision Tree Classification

A Decision Tree Classifier was developed for booking cancellation prediction.

The notebook includes:

- preprocessing of numerical and categorical features
- train/test split
- cross-validation and hyperparameter tuning
- classification metrics
- confusion matrix
- feature importance
- decision tree visualization
- extraction and evaluation of decision rules

### 5. K-means Clustering

K-means clustering was used to discover different booking profiles.

Features used:

- `lead_time`
- `adr`
- `total_nights`
- `total_guests`
- `total_of_special_requests`

Solutions from **K = 2 to K = 7** were evaluated using the Elbow Method and Silhouette Score.

Final solution:

- **K = 5**
- Silhouette Score: **0.2523**

The analysis identified several interpretable booking profiles, including higher-priced group bookings, bookings with many special requests, very early bookings, long stays and shorter bookings made closer to arrival.

Cancellation status was analysed only after clustering and was not used to create the clusters.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Scikit-learn
- Google Colab / Jupyter Notebook


## Repository Contents

- `01_...ipynb` – Data Preprocessing and EDA
- `02_...ipynb` – Hypothesis Testing and Statistical Inference
- `03_...ipynb` – Regression Analysis
- `04_...ipynb` – Decision Tree Classification
- `05_...ipynb` – K-means Clustering

## Authors

Natalia Balicka  
Kęstutis Juodis
