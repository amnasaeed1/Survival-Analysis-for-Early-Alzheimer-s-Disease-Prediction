# Survival-Analysis-for-Early-Alzheimer-s-Disease-Prediction

This repository contains the code for the proeject which focuses on using survival analysis for the early prediction of Alzheimer's Disease (AD) progression in individuals with Mild Cognitive Impairment (MCI). 

Survival analysis is a statistical approach used to predict the time until an event of interest occurs, such as disease onset or progression. In the context of this project, the 'event' is the conversion from MCI to Alzheimer's Disease.

The project uses machine learning techniques, Random Survival Forest, Extra Survival Trees, Coxnet, CoxPH, Gradient Boosting Survival, Survival Tree; to estimate the risk of conversion over time. These model generate individualized survival curves for each patient, allowing for a more personalized prediction of when the conversion from MCI to AD is likely to occur. The ultimate goal is to aid in clinical decision-making by identifying high-risk patients at an earlier stage, potentially leading to more timely interventions.

- Data Source:
The data was obtained from the Alzheimer's Disease Neuroimaging Initiative (ADNI) database, which includes comprehensive datasets for individuals at various stages of cognitive decline.

- Datasets Used:
Cognitive Tests, MRI, and PET Data: The primary dataset contained features from cognitive tests, MRI, and PET scans, along with diagnostic information at baseline and at the end of the study. This helped evaluate whether individuals converted from MCI to Alzheimer's Disease (AD). The cognitive test features included:
Age
Education
CDRSB (Clinical Dementia Rating - Sum of Boxes)
ADAS13 (Alzheimer's Disease Assessment Scale)
ADAS11
MMSE (Mini-Mental State Examination)
RAVLT.immediate (Rey Auditory Verbal Learning Test)
RAVLT.learning
RAVLT.forgetting
RAVLT.perc.forgetting
FAQ (Functional Activities Questionnaire)

The imaging test features included:
FDG-PET (Fluorodeoxyglucose-Positron Emission Tomography)
Ventricles
Hippocampus
Whole Brain
Entorhinal
Fusiform
Mid Temporal

CSF Biomarkers: An additional dataset contained cerebrospinal fluid (CSF) biomarker levels for the same patients, including:
ABETA (Amyloid Beta)
TAU
PTAU (Phosphorylated Tau)
This dataset was merged with the primary dataset to enhance predictive accuracy.

- Data Preprocessing:
1. Data Cleaning: Initial data cleaning involved removing any inconsistencies or irrelevant entries from the datasets.
2. Imputation for Missing Values: Missing values were handled using imputation techniques to ensure that the dataset was complete and usable for model training.
3. Standardization: Feature standardization was performed to ensure that all variables were on a comparable scale.
4. Handling Class Imbalance: Techniques were applied to manage class imbalance, ensuring that the model was not biased toward the more frequent class.

- Training and Testing:
Train-Test Split: The dataset was split into training and testing sets to validate the models' performance.
Model Training and Evaluation: Six different models were trained and tested to predict the time to conversion from MCI to AD. These models were evaluated using the Concordance Index (CI) and Integrated Brier Score (IBS) to assess their predictive performance.

- Feature Importance:
Permutation Feature Importance: To identify the most significant predictors of AD conversion, permutation feature importance was applied, revealing which features contributed most to the model's predictions.
