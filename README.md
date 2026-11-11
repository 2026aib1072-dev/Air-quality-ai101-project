# AQI Hazardous Prediction
### Air Quality Prediction & Hazardous Day Classification

**Mini Project – Indian Institute of Technology Ropar**  
**Academic Year:** 2026–27

**GitHub Repository:** [Air-quality-ai101-project](https://github.com/2026aib1072-dev/Air-quality-ai101-project)

---

## 1. Project Overview

This project develops a Machine Learning-based system to classify potentially hazardous air quality conditions using historical Air Quality Index (AQI) data.

The project uses pollutant-related features to classify air quality into two categories:

- **0 – Non-Hazardous:** AQI ≤ 200
- **1 – Hazardous:** AQI > 200

The objective is to understand how machine learning can be used to analyse air pollution data and identify potentially hazardous air quality days.

**Note:** AQI > 200 is the threshold selected for this project.

## 2. Problem Statement and Motivation

Air pollution is a major environmental concern that affects human health and the environment.

Identifying days with potentially hazardous air quality can help in understanding pollution patterns and assessing environmental conditions.

The objective of this project is to develop and evaluate a binary classification model using historical air quality measurements and pollutant concentrations.

## 3. Dataset Description

- **Dataset Name:** City Day AQI Dataset
- **File Used:** `city_day.csv`
- **Source:** Kaggle
- **Dataset Link:** [Air Quality Data in India – Kaggle](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)

The dataset contains historical city-wise air quality measurements and pollutant information.

It includes parameters such as:

- PM2.5
- PM10
- NO
- NO2
- NOx
- NH3
- CO
- SO2
- O3
- AQI

The original dataset contains 29,531 rows and 16 columns.

## 4. Technologies and Libraries Used

The project uses the following technologies and Python libraries:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## 5. Software and Library Versions

| Software / Library | Version |
|---|---|
| Python | 3.13.18 |
| Pandas | 2.2.3 |
| NumPy | 2.4.6 |
| Scikit-learn | 1.6.1 |
| Matplotlib | 3.10.0 |
| Seaborn | 0.13.2 |

## 6. Project Workflow

The project is divided into the following stages:

1. Data loading and cleaning
2. Exploratory Data Analysis (EDA)
3. AQI-based binary target creation
4. Feature selection and preparation
5. Train-test splitting
6. Missing-value handling through median imputation
7. Feature scaling
8. Logistic Regression model training
9. Model evaluation and visualization
10. Odds ratio analysis
11. Borderline prediction analysis

## 7. Data Preprocessing

**Implemented by:** Vineet Shekhar  
**GitHub Username:** `vin-it-1501`

The preprocessing stage includes:

1. Loading the dataset using Pandas.
2. Removing rows with missing AQI or AQI category values.
3. Creating a binary target variable named `Is_Hazardous`.
4. Removing unnecessary columns such as City, Date, AQI and AQI_Bucket from the input features.
5. Splitting the dataset into 80% training data and 20% testing data.
6. Using stratified sampling to maintain class proportions in both sets.
7. Handling missing feature values using median imputation calculated from training data only.

**Notebook:** `01_data_preprocessing_vineet_updated.ipynb`

## 8. Exploratory Data Analysis and Model Development

**Implemented by:** Rishabh Vishnoi  
**GitHub Username:** `2026aib1072-dev`

This stage focuses on understanding the dataset and developing the initial machine learning pipeline.

The work includes:

1. Exploratory Data Analysis.
2. Descriptive statistical analysis.
3. Visualizing target class distribution.
4. Analysing relationships between pollutant features using correlation.
5. Preparing data for model development.
6. Initial model development and related analysis.

**Notebook:** `02_eda_and_modeling_rishabh.ipynb`

## 9. Model Evaluation and Visualizations

**Implemented by:** Divya Godara  
**GitHub Username:** `Divyaa73`

This stage focuses on evaluating model performance and presenting the results through visualizations.

The work includes:

1. Feature scaling using StandardScaler.
2. Model evaluation on training and testing data.
3. Calculation of classification performance metrics.
4. Generating confusion matrix and classification reports.
5. Visualizing important model evaluation results.

The evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-score
- Log Loss
- Confusion Matrix

**Notebook:** `04_Model_evaluation_and_visualizations.ipynb`

## 10. Odds Ratio and Borderline Analysis

**Implemented by:** Sandeep Kumar  
**GitHub Username:** `Sandeepkumar2008`

This stage focuses on interpreting model behaviour and understanding predictions.

The work includes:

1. Calculating odds ratios from Logistic Regression coefficients.
2. Analysing the influence of different pollutant features.
3. Identifying borderline predictions using predicted probabilities.
4. Studying observations with hazardous prediction probabilities between 40% and 60%.
5. Visualizing pollutant patterns in borderline cases.

**Notebook:** `5_odds_ratios_and_borderline_analysis_sandeep.ipynb`

## 11. Model and Evaluation Results

The project uses **Logistic Regression** for binary classification.

The model is trained using the training dataset and evaluated using the testing dataset.

Recorded evaluation results:

| Metric | Result |
|---|---:|
| Training Accuracy | 94.36% |
| Testing Accuracy | 94.45% |
| Training F1-score | 0.8871 |
| Testing F1-score | 0.8888 |
| Training Log Loss | 0.1611 |
| Testing Log Loss | 0.1486 |

The close training and testing performance indicates consistent results on the two datasets.

The confusion matrix, classification report, odds ratios and borderline analysis provide additional insight into model performance and prediction behaviour.

## 12. Repository Structure

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
├── air_quality_master_pipeline.ipynb
├── merge_script.ipynb
│
├── Mini_Project_Presentation.pdf
└── video_link.txt
```

*The presentation PDF and video link files should be added to the repository before final submission.*

## 13. Installation and Execution

### Step 1: Clone the repository

```bash
git clone https://github.com/2026aib1072-dev/Air-quality-ai101-project.git
```

### Step 2: Navigate to the project directory

```bash
cd Air-quality-ai101-project
```

### Step 3: Install required libraries

```bash
pip install -r requirements.txt
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

### Step 5: Run the project

Open `air_quality_master_pipeline.ipynb` to view the integrated project workflow.

The individual notebooks are also available for understanding the contributions of each team member.

Run the notebook cells sequentially from top to bottom.

## 14. Team Members and Contributions

| S. No. | Name | GitHub Username | Contribution |
|---|---|---|---|
| 1 | Vineet Shekhar | `vin-it-1501` | Data Loading, Cleaning, Stratified Split and Documentation |
| 2 | Rishabh Vishnoi | `2026aib1072-dev` | Exploratory Data Analysis and Initial Model Development |
| 3 | Sandeep Kumar | `Sandeepkumar2008` | Odds Ratio and Borderline Analysis |
| 4 | Divya Godara | `Divyaa73` | Model Evaluation and Visualizations |

## 15. Project Presentation and Video Demonstration

**Presentation:** `Mini_Project_Presentation.pdf`

**Project Video:** [YouTube Video Link – To Be Added]

The project demonstration covers:

- Team member introductions and contributions
- Problem statement and motivation
- Dataset description
- Data preprocessing and exploratory analysis
- Training and testing data split
- Machine learning model development
- Model evaluation and visualizations
- Interpretation of results
- Odds ratio and borderline analysis

## 16. Project Status

The project implementation has been completed, including data preprocessing, exploratory data analysis, model development, evaluation, visualization, odds ratio analysis and borderline prediction analysis.

The integrated master pipeline and individual notebooks are included in the repository.

---

**Developed as an AI101 Mini Project at Indian Institute of Technology Ropar.**
