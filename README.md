# Undergraduate Projects

This repository contains a collection of projects completed during my undergrad years, primarily focused on data analysis, visualization, and machine learning. Below is a brief summary of what each project folder includes and the tools used.


## Python 1: Global Coral Bleaching Analysis
This was my final project for my Python 1 class. The topic was open to our choice, and my teammates, Mariah Cornelio and Saige Young, and I chose to investigate global coral bleaching using a [dataset](https://www.bco-dmo.org/dataset/773466) compiled by Robert van Woesik and his research team. We carried out the full workflow in Jupyter Notebook: understanding the raw data, cleaning and preprocessing it, and building visualizations to communicate our findings.

We set out to answer three questions: where in the world bleaching events were concentrated, which environmental factors (sea temperature, wind patterns, water turbidity) best explained why they occurred, and when bleaching first started showing up at the most-affected sites.

**Included in this project:**
- Data cleaning, preprocessing, and visualization pipeline (Jupyter Notebook)
- Interactive map of global bleaching event locations (HTML)
- Project presentation summarizing our findings (PDF)



## Python 2: Tabular Kaggle Project: Predicting Cirrhosis Outcomes
This was my project for DATA 3402, the challenge from Kaggle's [Playground Series S3E26](https://www.kaggle.com/competitions/playground-series-s3e26/overview), was to build a multi-class model predicting patient outcomes for cirrhosis. More specifically whether a patient was alive (`C`), alive after a liver transplant (`CL`), or deceased (`D`) by a given number of days. I worked through the full pipeline in Jupyter Notebook: exploring the data, cleaning and transforming it, and training and evaluating multiple models.

The training set contained 7,905 patient records across 20 columns of numerical and categorical clinical features (drug type, sex, presence of ascites/hepatomegaly/spiders/edema, bilirubin, cholesterol, albumin, and more), with no missing values or duplicates. Using the IQR method, I found that over half the numerical columns contained outliers — Alk_Phos alone had 792. During preprocessing, I converted the Age column from days to years and applied log transformation to correct the right skewed distributions found across most numerical features, then used KDE plots to compare feature distributions across the three outcome classes.

For modeling, I trained and compared Random Forest and XGBoost classifiers, evaluating both on logarithmic loss and classification metrics (precision, recall, F1). XGBoost came out ahead overall, with a lower log loss (0.51 vs. 0.52) and modestly better recall and macro-averaged F1, indicating more confident and accurate probability predictions than Random Forest.

**Included in this project:**
- Full pipeline notebook: data understanding, preprocessing, transformation, training, and model evaluation (`cirrhosis_project.ipynb`)
- Submission file with predicted probabilities for all three outcome classes (`cirrhosis_submission.csv`)
- Provided training and test data (`cirrhosis_train`, `cirrhosis_test`)

**Tools:** Python 3.11, Jupyter Notebook, NumPy, Pandas, Matplotlib, Seaborn, SciPy, scikit-learn, XGBoost

---
