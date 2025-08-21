# Extracting OUD Patient Characteristics from Clinical Notes Using NLP

This repository contains the code and project report for analyzing **Opioid Use Disorder (OUD)** patients using **Natural Language Processing (NLP)** techniques applied to clinical notes.  

The project was completed as part of **CS-670: Natural Language Processing (Spring 2024)**.  

---

##  Project Overview
Opioid Use Disorder (OUD) is a major public health crisis, with overdose deaths in the U.S. rising dramatically in recent decades. To better understand OUD, this project applies **NLP methods** to clinical notes from the **MIMIC database** (anonymized electronic health records).  

**Goals:**
- Extract key patient characteristics (feelings, comorbidities, medications).  
- Compare patients with and without OUD.  
- Build machine learning classifiers to predict OUD from clinical notes.  

---

##  Methodology
1. **Data Extraction**
   - Queried the MIMIC database using SQL.  
   - Selected patients with and without OUD based on ICD codes.  

2. **Preprocessing**
   - Removed noise and standardized text.  
   - Tokenized and lemmatized with **NLTK**.  
   - Filtered stopwords.  
   - Extracted keywords for:
     - Patient feelings  
     - Comorbid disorders  
     - Analgesic, psychiatric, withdrawal management, and adjunctive medications  

3. **Analysis**
   - Found significant differences in emotions, disorders, and prescriptions.  
   - Example findings:
     - Comorbidities: HIV, hepatitis, anxiety, bipolar disorder, cirrhosis.  
     - Medications: methadone, clonidine, diazepam, suboxone, gabapentin.  

4. **Predictive Modeling**
   - Classifiers: Naïve Bayes, Logistic Regression, Random Forest.  
   - **Random Forest** performed best:  
     - Accuracy: **89.8%**  
     - Precision: **86%**  
     - Recall: **88.2%**  
     - F1 Score: **87.1%**  

---

##  Repository Contents
- `OUD Patient Characteristics Using NLP- Python Code.ipynb` → Jupyter Notebook (code for preprocessing, analysis, and modeling).  
- `Extracting OUD Patient Characteristics from Clinical Notes Using NLP.pdf` → Full project report with results, figures, and discussion.  

---

##  How to Run
```bash
# Clone this repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install -r requirements.txt

# Open the Jupyter Notebook
jupyter notebook "OUD Patient Characteristics Using NLP- Python Code.ipynb"
