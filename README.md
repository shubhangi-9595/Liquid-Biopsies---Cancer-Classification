Step 1 -  Download the file “GSE68086_TEP_data_matrix.txt“ from
NCBI GEO Data: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE68086

Step 2 - Unzip the file and get the text file

Step 3 - Run the RMD file "project_8_preprocessing.rmd" from the source folder in R Studio. The text file from Step 2 will be used here.

Step 4 - Using the  ipynb file "project_8_report.ipynb" from the source folder. The output file from the Step 3 will be used here.



## Overview  
This project develops a machine learning model to classify healthy and cancer samples using RNA-sequencing data from blood platelet (TEP) samples. The study uses transcriptomics data from 283 platelet samples (228 cancer, 55 healthy) and preprocesses it using DESeq2 and feature filtering. Class imbalance is handled with SMOTE, and the final dataset is split into training and testing sets for model evaluation.  

## Data  
- Source: GEO database, accession ID **GSE68086**  
- Preprocessing:  
  - Remove unknown sample types  
  - Filter low-expression genes (values ≤ 5)  
  - DESeq2 analysis for differential expression  
  - Label encoding: `1` = Cancer, `0` = Non-Cancer  
  - Oversampling minority class using SMOTE  
  - Scaling features  

## Machine Learning Methods  
- **Random Forest (RF):**  
  - Hyperparameter tuning for number of trees (optimized at 150)  
  - Bagging ensemble using decision trees  
- **Evaluation Metrics:**  
  - Confusion Matrix (TP, TN, FP, FN)  
  - ROC Curve  
  - Feature size vs. Accuracy analysis (1–90 features)  
- **Cross-Validation:** 10-fold  

## Results  
Results including model performance, important features, and comparisons with previous studies can be found in the project report.  
