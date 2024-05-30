---
title: Socioeconomic data
description: Tools and methods to assess quality of socio-economics data.
contributors: [Eva Garcia Alvarez]
page_id: sed_quality_control
redirect_from: /socioeconomic-data/quality-control
rdmkit:
  - name:
    url:
training:
  - name:
    registry:
    url:
---

## Introduction
The quality control of socioeconomic data in the context of infectious diseases is crucial for ensuring that such data can be reliably used for research and policymaking. Quality control measures should be implemented throughout the entire data lifecycle, from data collection (or generation) to storage. This requires that a comprehensive and systematic approach is applied throughout the data lifecycle. The approach must focus on, among other things, representativeness, clarity, timeliness, error detection, interoperability, and continuous monitoring.

Below are considerations that must be taken into account when working with socioeconomics data, along with the quality dimensions that they are related to.

## Considerations

### Define the target population
* **Quality dimension**: Representativeness
* It is essential that the sampling population accurately represents the demographics most affected by the disease. This includes accounting for age, gender, socioeconomic status, geographical location, and other relevant factors, to ensure that the findings can be generalised to the wider population at risk.

### Define the collection strategy
* **Quality dimension**: Clarity and Relevance
* When data are collected using surveys, it is vital to design questions that are relevant and easily understood by participants. The questions should be straightforward, culturally appropriate, and tailored to capture the necessary socioeconomic variables that impact, or are impacted by, the infectious disease in question. Additionally, when harvesting data from existing databases, it is crucial to ensure that the data extracted are pertinent and clearly defined. This involves understanding the database schema, ensuring compatibility with the research objectives, and verifying the accuracy and relevance of the socioeconomic variables included. The data extraction process should be well-documented and consistent, ensuring that the harvested data maintain their integrity and usefulness for the intended analysis.

### Timeliness
* **Quality dimension**: Currency and Relevance
* Socio-economic data related to infectious diseases must be current and collected promptly to reflect the rapidly changing dynamics of disease spread and its socioeconomic impacts, especially during an outbreak. Timely data collection enables timely intervention and policy response.

### Missing values
* **Quality dimension**: Completeness and population coverage
* Strategies should be applied to address any gaps in data, and to ensure coverage of all relevant sub-populations.

## Existing approaches

### Pilot tests
Conduct pilot tests or preliminary surveys with a subset of the target population to ensure that the survey design works effectively. This helps to identify potential issues with the clarity, relevance, and understanding of the questions before full-scale data collection.

When the data are harvested from existing databases, conduct pilot extractions to verify the data retrieval process. This involves testing the extraction protocols on a small scale to ensure that the data pulled from databases are accurate, relevant, and compatible with the study’s objectives. Pilot testing the data extraction helps identify and address any discrepancies or issues in data format, completeness, and alignment with the research questions.

This helps with representativeness, assessing whether data collection methods effectively reach all segments of the population. Examining population coverage helps identify underserved or marginalized groups whose experiences may be underrepresented in the data, thus enabling more equitable decision-making.

### Timeliness
Implement efficient data collection protocols that ensure rapid access to and sharing of data. Real-time or near-real-time data collection and processing systems are critical for monitoring the socio-economic impacts of infectious diseases and for timely decision-making.

### Error and inconsistency detection
Perform regular error detection and data cleaning processes. This includes identifying and correcting outliers, inconsistencies, and missing data to improve the overall quality and reliability of the data.

Outliers (i.e., data points that significantly differ from other observations) must be identified. It is key to make a distinction between these actual but rare events that need careful consideration and errors in data entry or measurement anomalies.

Some methods for detecting errors and inconsistencies are:
* Data Visualization Tools:
  * Python libraries: {% tool "matplotlib" %}, {% tool "seaborn" %}
* Statistical Analysis Software:
  * {% tool "r" %}
  * Python libraries: {% tool "pandas" %}, {% tool "numpy" %}
* Develop Data Quality Assessment Framework (DQAF) or implement already existing ones
* Cross-Validation Techniques:
  * {% tool "scikit-learn" %} - Cross-validation (python)

### Data cleaning
Data cleaning procedures are essential for ensuring the accuracy and reliability of socioeconomic data. This involves identifying and rectifying errors, inconsistencies, and outliers that may arise during data collection or entry. Cleaning procedures may include de-duplication to remove redundant entries, standardisation of formats to ensure uniformity, and imputation techniques to address missing values.
Existing software, such as python libraries (e.g., {% tool "pandas" %} or {% tool "dedupe" %}), can be used for data cleaning.

### Interoperability
* Semantic harmonisation: Use standard codes and terminologies for variables to ensure consistency across different data sources and studies.
* Syntactic harmonisation: Adopt standardised data formats to facilitate data integration and comparability across various datasets.

### Statistical tests for data quality
Conduct statistical tests to assess data reliability and validity. Reliability tests assess the consistency of the data over time, ensuring that data trends are dependable and not subject to random fluctuations. Validity tests, on the other hand, examine the accuracy of the data in measuring what they are intended to measure. For instance, in the context of infectious diseases, validity tests might assess whether socio-economic variables accurately reflect the true impact of the disease on different demographics.

### Check completeness
Completeness is the dimension that takes into account the number of variables in a given data model that have actual values. This involves scrutinising datasets for missing values, ensuring that all relevant variables are captured.

### Continuous monitoring
Implement ongoing monitoring mechanisms to continuously assess data quality. This includes tracking data collection processes, identifying and addressing data quality issues promptly, and updating data collection protocols as needed. This entails establishing protocols for ongoing assessment of data collection processes, automated checks for anomalies or inconsistencies, and regular audits to verify adherence to quality control procedures.

### Regular communication with data sources
Establishing regular communication channels with data sources fosters a collaborative approach to quality control. This enables swift resolution of any issues or discrepancies identified during quality checks, as stakeholders can promptly provide clarification or rectify errors. Additionally, ongoing dialogue with data sources facilitates mutual understanding of data requirements and collection methodologies, allowing for adjustments to be made in real-time to improve data quality.
