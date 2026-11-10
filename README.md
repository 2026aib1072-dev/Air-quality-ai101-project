# Air-quality-ai101-project
# AQI Hazardous Prediction

**Mini Project – Indian Institute of Technology Ropar**  
**Academic Year:** 2026–27

**GitHub Repository:** [Repository Link](https://github.com/2026aib1072-dev/Air-quality-ai101-project)

---

## 1. Project Overview

This project aims to develop a Machine Learning-based system to identify potentially hazardous air quality conditions using historical Air Quality Index (AQI) data.

The project focuses on classifying air quality into two categories based on AQI values.

## 2. Problem Statement

Air pollution is a major environmental concern that affects human health. The objective of this project is to prepare air quality data for predicting hazardous conditions.

The project uses the following binary classification:

- **0 – Non-Hazardous:** AQI ≤ 200
- **1 – Hazardous:** AQI > 200

*Note: AQI > 200 is the threshold selected for this project.*

## 3. Dataset Description

- **Dataset Name:** City Day AQI Dataset
- **File Used:** `city_day.csv`
- **Source:** Kaggle
- **Dataset Link:** [Kaggle Dataset](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india
)

The dataset contains historical city-wise air quality measurements and pollutant information.

## 4. Technologies and Libraries Used

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

## 6. Data Preprocessing

**Implemented by:** Vineet Shekhar  
**GitHub Username:** `vin-it-1501`

The preprocessing stage includes:

1. Loading the dataset using Pandas.
2. Removing rows with missing AQI or AQI category values.
3. Creating a binary target variable named `Is_Hazardous`.
4. Removing unnecessary columns such as City, Date, AQI and AQI_Bucket from input features.
5. Splitting the dataset into 80% training data and 20% testing data.
6. Using stratified sampling to maintain class proportions in both sets.
7. Handling missing feature values using median imputation calculated from training data only.

**Notebook:** `01_data_preprocessing_vineet.ipynb`

## 7. Team Members and Contributions

| S. No. | Name | GitHub Username | Contribution |
|---|---|---|---|
| 1 | Vineet Shekhar | `vin-it-1501` | Data Loading, Cleaning, Stratified Split & Documentation |
| 2 | Rishabh Vishnoi | `2026aib1072-dev` | To be updated |
| 3 | Sandeep Kumar | `Sandeepkumar2008` | To be updated |
| 4 | Divya Godara | `Divyaa73` | To be updated |

## 8. Repository Structure

```text
AQI-Hazardous-Prediction/
│
├── README.md
├── requirements.txt
├── city_day.csv
└── 01_data_preprocessing_vineet.ipynb
```

## 9. Installation and Execution

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate to the project directory:

```bash
cd AQI-Hazardous-Prediction
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open and run `01_data_preprocessing_vineet.ipynb`.

## 10. Current Project Status

The initial data preprocessing stage has been completed, including data loading, cleaning, AQI binarization, stratified train-test splitting and median imputation.

Further stages of the project will be added as development progresses.

---

**Developed as a Mini Project at IIT Ropar.**
