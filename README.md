Repository Contents
This repository contains the complete analytical pipeline for our systematic review and meta-analysis of machine learning models predicting all-cause mortality.
Included Scripts and Data:
1. Data Extraction and Preprocessing

data_extraction.py: Systematic extraction of AUC values, confidence intervals, and study characteristics from included studies
data_cleaning.py: Quality control, missing data handling, and standardization of extracted variables
tripod_scoring.py: Automated TRIPOD+AI quality assessment scoring system

2. Meta-Analysis Pipeline

meta_analysis_main.py: Core random-effects meta-analysis using Python (numpy, pandas, statsmodels)
subgroup_analysis.py: Stratified analyses by population type, country income, sample size, and model categories
meta_regression.py: Weighted least squares meta-regression examining study-level moderators
heterogeneity_analysis.py: I² calculation and heterogeneity assessment

3. Visualization and Reporting

forest_plots.py: Generation of forest plots for overall and subgroup analyses using matplotlib/seaborn
violin_plots.py: AUC distribution visualizations by study characteristics
world_map.py: Geographic distribution of included studies
quality_assessment_plots.py: TRIPOD+AI score distributions and item-level analysis

4. Reproducibility Tools

requirements.txt: Complete Python environment specifications
config.yaml: Analysis parameters and settings
validation_checks.py: Internal validation and sensitivity analyses

Data Files:

extracted_data.csv: Complete dataset of 88 studies with AUC values and covariates
tripod_scores.csv: Detailed TRIPOD+AI assessments for all included studies
country_classifications.csv: World Bank income classifications used in analyses

Usage:
Run python meta_analysis_main.py to reproduce all primary analyses. Individual scripts can be executed independently for specific components.
