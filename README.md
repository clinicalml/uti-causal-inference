# uti-causal-inference

Code for "Reassessing the management of uncomplicated urinary tract infection: A retrospective analysis

Preface: Important Note on Replication
The data used in this study is not publicly available. 

Repository Overview
Setup

Src/Notebooks/Cohort Generation

-	Feature Generation 1-Final.ipynb: 
  	Generates Treatment History Confounders
-	Feature Generation 2-Final.ipynb: 
  	Generates Provider Features using NPI Database
-	Feature Generation 3-Final.ipynb: 
    Generates Condition 2 year history Features
-	Feature Generation 4-Final.ipynb: 
     Generates additional condition history covariates using concept ancestors for following condition categories
-	Feature Generation 5-Final.ipynb: 
      Generates lab, lab existence features, censor and outcome variables
  -	Cohort_Generation.ipynb:
    Generates the cohort based on defined inclusion/exclusion criteria


Src/Notebooks/Covariate Tables
-	Antibiotic prevalence analysis.ipynb:
  	Creates supplementary table 5
-	Table 1.ipynb:
  	Creates table 1
  
Src/Notebooks/ATE Tables and Plots
The causal analysis notebooks utilize either the omop or domain-knowledge derived features and second line or alternatives treatment to do cross-validated grid search for propensity/censorship models. These notebooks also contain the code to use the model to generate boostrap ATEs, shapley value plots and the calibration plots.
-	Grid Search and Causal Analysis (final) – alternatives
  o	The notebook used to perform the causal analysis on first line vs alternatives
-	Grid Search and Causal Analysis (final) – second line
  o	The notebook used to perform the causal analysis on first line vs second-line
