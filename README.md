Extracting OUD Patient Characteristics from Clinical Notes Using NLP

This repository contains the code and project report for analyzing Opioid Use Disorder (OUD) patients using Natural Language Processing (NLP) techniques applied to clinical notes.

The project was completed as part of CS-670: Natural Language Processing (Spring 2024).

📖 Project Overview

Opioid Use Disorder (OUD) is a major public health crisis, with overdose deaths in the U.S. rising dramatically in recent decades. To better understand OUD, this project applies NLP methods to clinical notes from the MIMIC database (anonymized electronic health records).

The project aims to:

Extract key patient characteristics (feelings, comorbidities, medications).

Compare patients with and without OUD.

Build machine learning classifiers to predict OUD from clinical notes.

⚙️ Methodology

Data Extraction

Queried the MIMIC-III/IV database using SQL.

Selected patients with and without OUD based on ICD codes.

Preprocessing

Removed noise (extra spaces, underscores, etc.).

Tokenized and lemmatized text using NLTK.

Filtered stopwords.

Extracted keywords for:

Patient feelings

Comorbid disorders

Analgesic, psychiatric, withdrawal management, and adjunctive medications

Analysis

Identified differences in symptoms and prescriptions between OUD and non-OUD patients.

Key findings include higher prevalence of:

Comorbidities: HIV, hepatitis, anxiety, bipolar disorder, cirrhosis.

Medications: methadone, clonidine, diazepam, suboxone, gabapentin.

Predictive Modeling

Classifiers tested: Naïve Bayes, Logistic Regression, Random Forest.

Random Forest achieved best performance:

Accuracy: 89.8%

Precision: 86%

Recall: 88.2%

F1 Score: 87.1%

Naïve Bayes provided interpretability, showing methadone, clonidine, and PTSD as key predictors.

📂 Repository Contents

OUD Patient Characteristics Using NLP- Python Code.ipynb → Jupyter Notebook with preprocessing, analysis, and modeling.

Extracting OUD Patient Characteristics from Clinical Notes Using NLP.pdf → Full project report with results, figures, and discussion.

🚀 How to Run

Clone this repository:

git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>


Install dependencies (Python ≥3.8 recommended):

pip install -r requirements.txt


Open the Jupyter Notebook:

jupyter notebook "OUD Patient Characteristics Using NLP- Python Code.ipynb"

📊 Results Highlights

OUD patients show distinct emotional, medical, and prescription patterns.

Methadone, clonidine, and psychiatric medications play a dual role in both treatment and withdrawal.

Random Forest performed best for prediction, while Naïve Bayes provided the most interpretability.

🔍 Limitations & Future Work

Models not fully tailored to medical notes (need domain-specific NLP models).

Data limited to one hospital (BIDMC, Boston).

Future steps:

Incorporate more variables (e.g., vitals, lab results).

Use data from multiple hospitals.

Apply advanced models (e.g., transformers for clinical NLP).

👩‍⚕️ Authors

Khashayar Eshtiaghi

Alex Vajiac

📑 References

NIH: Drug Overdose Death Rates

CDC: Understanding the Epidemic

Texas HHS: Fentanyl: One Pill Kills
