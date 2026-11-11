# 🌫️ AQI Hazardous Prediction Using Machine Learning

## 1. Project Overview

This project focuses on predicting hazardous air quality conditions using Machine Learning.

It uses historical air quality data from Indian cities and applies Data Preprocessing, Exploratory Data Analysis (EDA), Feature Scaling, Logistic Regression, and Model Evaluation to classify air quality into two categories:

- **Non-Hazardous (0):** AQI ≤ 200
- **Hazardous (1):** AQI > 200

The AQI threshold of 200 is selected for this project.

## 2. Problem Statement

Air pollution is a major environmental concern in India. High concentrations of pollutants such as PM2.5, PM10, CO, and SO2 can negatively affect human health.

The objective of this project is to develop a Machine Learning classification model that predicts whether air quality is hazardous based on pollutant concentration data.

## 3. Dataset Description

- **Dataset:** Air Quality Data in India
- **Dataset File:** `city_day.csv`
- **Source:** Kaggle – Air Quality Data in India

The dataset contains historical air quality measurements from different Indian cities.

### Features Used

The model uses the following 12 pollutant-related features:

1. PM2.5
2. PM10
3. NO
4. NO2
5. NOx
6. NH3
7. CO
8. SO2
9. O3
10. Benzene
11. Toluene
12. Xylene

### Target Variable

`Is_Hazardous`

- `0` – Non-Hazardous
- `1` – Hazardous

## 4. Technologies and Libraries

| Technology | Version |
|---|---|
| Python | 3.13.18 |
| Pandas | 2.2.3 |
| NumPy | 2.4.6 |
| Scikit-learn | 1.6.1 |
| Matplotlib | 3.10.0 |
| Seaborn | 0.13.2 |

Other tools: Jupyter Notebook and Git/GitHub.

## 5. Project Workflow

1. **Data Loading:** Loading the air quality dataset.
2. **Data Cleaning:** Handling missing values and preparing the dataset.
3. **Target Creation:** Creating the binary `Is_Hazardous` variable using the AQI threshold.
4. **Exploratory Data Analysis:** Studying pollutant distributions and relationships through visualizations.
5. **Train-Test Split:** Splitting the dataset into training and testing sets using stratified sampling (80:20).
6. **Feature Scaling:** Standardizing pollutant features using StandardScaler.
7. **Model Training:** Training a Logistic Regression classifier.
8. **Model Evaluation:** Evaluating the model using classification metrics and visualizations.
9. **Odds Ratio Analysis:** Understanding the influence of pollutant features.
10. **Borderline Analysis:** Examining predictions around the classification boundary.

## 6. Machine Learning Model

The project uses **Logistic Regression**, a supervised Machine Learning algorithm for binary classification.

### Data Preprocessing

- Missing values are handled using median imputation.
- The dataset is divided into training and testing sets in an 80:20 ratio.
- Stratified sampling preserves the class distribution.
- StandardScaler is fitted on training data and then applied to testing data to prevent data leakage.

### Model Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Log Loss
- Confusion Matrix

## 7. Model Performance

The following results were recorded during project development:

| Metric | Training | Testing |
|---|---:|---:|
| Accuracy | 94.36% | 94.45% |
| F1-score | 0.8871 | 0.8888 |
| Log Loss | 0.1611 | 0.1486 |

*These values should be verified against the final executed notebook before submission.*

## 8. Odds Ratio Analysis

Odds ratios help interpret the influence of different pollutant features on hazardous classification.

Some recorded odds ratios are:

| Feature | Odds Ratio |
|---|---:|
| PM2.5 | 73.5339 |
| CO | 22.0709 |
| PM10 | 2.6723 |
| SO2 | 1.3147 |
| NOx | 1.2826 |

Since the features are standardized, these values represent the change in odds associated with a one-standard-deviation increase in the corresponding feature, holding other features constant.

## 9. Team Contributions

| Team Member | Contribution |
|---|---|
| Vineet Shekhar (`vin-it-1501`) | Data Loading, Cleaning, Stratified Train-Test Split and Documentation |
| Rishabh Vishnoi (`2026aib1072-dev`) | Exploratory Data Analysis and Initial Model Development |
| Divya Godara (`Divyaa73`) | Model Evaluation and Visualizations |
| Sandeep Kumar (`Sandeepkumar2008`) | Odds Ratio and Borderline Analysis |

## 10. Installation and Execution

Follow these steps to clone the repository, install dependencies, and execute the master pipeline.

### Step 1. Clone the repository from GitHub

<text>Time: Approximately 10 seconds</text>

**PowerShell:**

```powershell
git clone https://github.com/2026aib1072-dev/Air-quality-ai101-project.git
```

### Step 2. Navigate into the project directory

<text>Time: Approximately 5 seconds</text>

**PowerShell:**

```powershell
cd Air-quality-ai101-project
```

### Step 3. Pull latest changes from main branch

<text>Time: Approximately 10 seconds</text>

**PowerShell:**

```powershell
git pull origin main
```

### Step 4. Install all dependencies from requirements.txt

<text>Time: Approximately 30 seconds</text>

**PowerShell:**

```powershell
python -m pip install -r requirements.txt
```

### Step 5. Execute the master pipeline headlessly

<text>Time: Approximately 1 minute</text>

**PowerShell:**

```powershell
python -m nbconvert --to notebook --execute air_quality_master_pipeline.ipynb
```

This command executes the master notebook from top to bottom without requiring manual interaction with the Jupyter interface.

**Note:** Execution time may vary depending on system specifications and internet speed. Python 3.13 is recommended for the listed library versions.

## 11. Project Structure

```text
Air-quality-ai101-project/
│
├── README.md
├── requirements.txt
├── city_day.csv
│
├── 01_data_preprocessing_vineet_updated.ipynb
├── 02_eda_and_modeling_rishabh.ipynb
├── 04_Model_evaluation_and_visualizations.ipynb
├── 5_odds_ratios_and_borderline_analysis_sandeep.ipynb
│
├── merge_script.ipynb
└── air_quality_master_pipeline.ipynb
```

## 12. Project Demonstration

**Video Demonstration:** Add the YouTube video link after uploading the final project presentation.

## 13. Conclusion

This project demonstrates the application of Machine Learning techniques to classify hazardous air quality conditions using pollutant concentration data.

It combines data preprocessing, exploratory analysis, Logistic Regression, model evaluation, and odds ratio interpretation to study the relationship between air pollutants and hazardous air quality.

## 14. Project Information

- **Course:** AI101
- **Project Title:** AQI Hazardous Prediction Using Machine Learning
- **GitHub Repository:** https://github.com/2026aib1072-dev/Air-quality-ai101-project
