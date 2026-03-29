# MedShow - Clinical Attendance Prediction System

A machine learning project that predicts whether a patient will attend 
their scheduled medical appointment, built using Python and Scikit-learn.

---

## Problem Statement

Hospital no-shows are a major operational challenge — empty appointment 
slots waste doctor time and cause revenue loss. This project builds a 
prediction model to identify patients who are likely to miss their 
appointments, enabling hospitals to take proactive action.

---

## Dataset

- Source: Kaggle — Medical Appointment No-Shows (Brazil)
- Records: 110,527 patients
- Features: Age, Gender, SMS Received, Waiting Days, Medical Conditions
- Target: Whether the patient showed up or not (0 = Showed Up, 1 = No Show)

---

## Project Structure
```
MedShow/
├── data/
│   └── KaggleV2-May-2016.csv       <- Original dataset
├── notebook/
│   └── MedShow_Pred.ipynb          <- Main Jupyter notebook
├── output/
│   ├── cleaned_data.csv            <- Cleaned dataset
│   ├── noshow_by_age.png           <- Visualization 1
│   ├── noshow_by_waitingdays.png   <- Visualization 2
│   ├── noshow_by_dayofweek.png     <- Visualization 3
│   ├── confusion_matrix.png        <- Model output
│   ├── feature_importance.png      <- Feature importance
│   └── data_summary_dashboard.png  <- Dashboard
└── README.md

```

---

## Steps Performed

1. Loaded dataset and explored structure
2. Handled missing values using Median and Mode imputation
3. Performed data cleaning — fixed column names, removed invalid records
4. Created new features — WaitingDays, TotalDiseases, AppointmentDayOfWeek
5. Performed data analysis and created visualizations
6. Trained two ML models — Random Forest and XGBoost
7. Compared model performance and selected best model

---

## Models and Results

| Model | Accuracy |
|---|---|
| Random Forest | 65.22% |
| XGBoost | 71.35% |

Best Model : XGBoost Classifier

---

## Key Findings

- Younger patients (under 35) miss appointments more than older patients
- Longer waiting days increase the likelihood of no-shows
- Alcoholism is the strongest predictor of no-show behaviour
- Patients on scholarship have a higher no-show rate (34.9% vs 27.8%)

---

## Technologies Used

- Python 3.10
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## How to Run

1. Clone this repository
2. Install dependencies
3. Open the notebook
```
jupyter notebook notebook/MedShow_Pred.ipynb
```
4. Run all cells in order

---

## Business Impact

This model can be integrated into healthcare applications to flag 
high-risk patients and trigger automated reminders — directly reducing 
revenue loss from empty appointment slots and improving hospital efficiency.

---

## Author

Praneeth N R  
M.Sc Data Science  
Coimbatore Institute of Technology
