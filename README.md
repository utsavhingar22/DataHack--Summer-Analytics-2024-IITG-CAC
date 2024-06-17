# DataHack-Summer-Analytics-2024-IITG-CAC

# Vaccine Prediction Project- Summer Analytics 2024

This project aims to predict the likelihood of individuals receiving their XYZ and seasonal flu vaccines. Specifically, we predict two probabilities: one for `xyz_vaccine` and one for `seasonal_vaccine`. The predictions are made using a machine learning model trained on the provided dataset.

## Problem Description

The goal is to predict the probabilities for two target variables:
- `xyz_vaccine`: Whether the respondent received the XYZ flu vaccine.
- `seasonal_vaccine`: Whether the respondent received the seasonal flu vaccine.

Both target variables are binary:
- 0 = No
- 1 = Yes

## Dataset

The dataset contains 36 columns:
- `respondent_id`: A unique and random identifier for each respondent.
- 35 features describing various behavioral, opinion-based, and demographic information.

### Features

- `xyz_concern`: Level of concern about the XYZ flu.
- `xyz_knowledge`: Level of knowledge about XYZ flu.
- `behavioral_antiviral_meds`: Has taken antiviral medications. (binary)
- `behavioral_avoidance`: Has avoided close contact with others with flu-like symptoms. (binary)
- `behavioral_face_mask`: Has bought a face mask. (binary)
- `behavioral_wash_hands`: Has frequently washed hands or used hand sanitizer. (binary)
- `behavioral_large_gatherings`: Has reduced time at large gatherings. (binary)
- `behavioral_outside_home`: Has reduced contact with people outside of own household. (binary)
- `behavioral_touch_face`: Has avoided touching eyes, nose, or mouth. (binary)
- `doctor_recc_xyz`: XYZ flu vaccine was recommended by doctor. (binary)
- `doctor_recc_seasonal`: Seasonal flu vaccine was recommended by doctor. (binary)
- `chronic_med_condition`: Has any of the following chronic medical conditions. (binary)
- `child_under_6_months`: Has regular close contact with a child under six months. (binary)
- `health_worker`: Is a healthcare worker. (binary)
- `health_insurance`: Has health insurance. (binary)
- `opinion_xyz_vacc_effective`: Respondent's opinion about XYZ vaccine effectiveness.
- `opinion_xyz_risk`: Respondent's opinion about risk of getting sick with XYZ flu without vaccine.
- `opinion_xyz_sick_from_vacc`: Respondent's worry of getting sick from taking XYZ vaccine.
- `opinion_seas_vacc_effective`: Respondent's opinion about seasonal flu vaccine effectiveness.
- `opinion_seas_risk`: Respondent's opinion about risk of getting sick with seasonal flu without vaccine.
- `opinion_seas_sick_from_vacc`: Respondent's worry of getting sick from taking seasonal flu vaccine.
- `age_group`: Age group of respondent.
- `education`: Self-reported education level.
- `race`: Race of respondent.
- `sex`: Sex of respondent.
- `income_poverty`: Household annual income of respondent.
- `marital_status`: Marital status of respondent.
- `rent_or_own`: Housing situation of respondent.
- `employment_status`: Employment status of respondent.
- `hhs_geo_region`: Respondent's residence using a 10-region geographic classification.
- `census_msa`: Respondent's residence within metropolitan statistical areas (MSA).
- `household_adults`: Number of other adults in household.
- `household_children`: Number of children in household.
- `employment_industry`: Type of industry respondent is employed in.
- `employment_occupation`: Type of occupation of respondent.

## Files in Repository

- `submission.csv`: The submission file with predicted probabilities.
- `DataHack By IITG- Utsav Hingar.ipynb`: The Jupyter Notebook containing the code for data preprocessing, model training, and prediction.

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Libraries: pandas, numpy, sklearn, matplotlib, seaborn

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/utsavhingar22/DataHack--Summer-Analytics-2024-IITG-CAC.git
    ```

2. Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```

3. Open the Jupyter Notebook:
    ```bash
    jupyter notebook DataHack By IITG- Utsav Hingar.ipynb
    ```

### Running the Notebook

1. Load the datasets and merge training features and labels.
2. Fill missing values in both training and test datasets.
3. Perform exploratory data analysis (EDA) including plotting correlation matrix and histograms.
4. Encode non-numeric features.
5. Add new features to both training and test datasets.
6. Separate features and labels for the training data.
7. Standardize the features using `StandardScaler`.
8. Train and evaluate models for `xyz_vaccine` and `seasonal_vaccine`.
9. Make probability predictions on the test set.
10. Prepare and save the submission file as `submission.csv`.

### Evaluation

The performance of the model is evaluated based on the area under the receiver operating characteristic curve (ROC AUC) for each of the two target variables. The mean of these two scores is the overall score.

## Results

The `submission.csv` file contains the predicted probabilities for `xyz_vaccine` and `seasonal_vaccine` for each respondent in the test set.

## Acknowledgements

Special thanks to the data providers and contributors to this project.

---

Feel free to customize this README file as needed.
