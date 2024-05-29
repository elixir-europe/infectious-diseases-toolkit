---
title: Socioeconomic data
description: Tools and methods to assess quality.
contributors: []
no_robots: true
search_exclude: true
sitemap: false
page_id: sed_quality_control
redirect_from: /socioeconomic-data/quality-control
rdmkit:
  - name:
    url:
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction
Quality control of socio-economic data in the context of infectious diseases is crucial for ensuring that such data can be reliably used for research and policymaking. Quality control measures should be implemented throughout the entire data lifecycle, from data collection (or generation) to their final use. This requires a comprehensive and systematic approach throughout the data lifecycle focusing, among others, on representativeness, clarity, timeliness, error detection, interoperability and continuous monitoring.

In the following section considerations that have to be taken into account when working with socioeconomics data are gathered, along with the quality dimensions they are related to.

## Considerations

### Define the target population
* **Quality dimension**: Representativeness
* It is essential that the sampling population accurately represents the demographics most affected by the disease. This includes considerations of age, gender, socioeconomic status, geographical location, and other relevant factors to ensure that the findings can be generalized to the entire population at risk.

### Define the collection strategy
*	**Quality dimension**: Clarity and Relevance
*	When data are collected through surveys, it is vital to design questions that are relevant and clearly understood by participants. The questions should be straightforward, culturally appropriate, and tailored to capture the necessary socio-economic variables that impact or are impacted by the infectious disease in question. Additionally, when harvesting data from existing databases, it is crucial to ensure that the data extracted are pertinent and clearly defined. This involves understanding the database schema, ensuring compatibility with the research objectives, and verifying the accuracy and relevance of the socio-economic variables included. The data extraction process should be well-documented and consistent, ensuring that the harvested data maintain their integrity and usefulness for the intended analysis.

### Timeliness
* **Quality dimension**: Currency and Relevance
* Socio-economic data related to infectious diseases must be current and promptly collected to reflect the rapidly changing dynamics of disease spread and its socio-economic impacts, especially during an outbreak. Timely data enables timely intervention and policy response.

### Missing values
* **Quality dimension**: Completeness and population coverage
* Strategies should be applied to address gaps and ensure coverage of all relevant sub-populations.

## Existing Approaches

### Pilot Tests
Conduct pilot tests or preliminary surveys with a subset of the target population to ensure the survey design works effectively. This helps in identifying potential issues with question clarity, relevance, and respondent understanding before full-scale data collection.

When the data is harvested from existing databases, conduct pilot extractions to verify the data retrieval process. This involves testing the extraction protocols on a small scale to ensure that the data pulled from databases are accurate, relevant, and compatible with the study’s objectives. Pilot testing the data extraction helps identify and address any discrepancies or issues in data format, completeness, and alignment with the research questions.

This helps with representativeness, assessing whether data collection methods effectively reach all segments of the population. Examining population coverage helps identify underserved or marginalized groups whose experiences may be underrepresented in the data, thus enabling more equitable decision-making.

### Timeliness
Implement efficient data collection protocols that ensure rapid access to and sharing of data. Real-time or near-real-time data collection and processing systems are critical for monitoring the socio-economic impacts of infectious diseases and for timely decision-making.

### Error and inconsistency detection
Perform regular error detection and data cleaning processes. This includes identifying and correcting outliers, inconsistencies, and missing data to improve the overall quality and reliability of the data.

Outliers (i.e., data points that significantly differ from other observations) must be identified. It is key to make a distinction between these actual but rare events that need careful consideration and errors in data entry or measurement anomalies.

Some methods for detecting errors and inconsistencies are **TODO CHECK LINKS!**:
* Data Visualization Tools:
  * [Tableau](https://www.tableau.com/)
  * [Microsoft Power BI](https://powerbi.microsoft.com/)
  * Python libraries: [matplotlib](https://matplotlib.org/), [seaborn](https://seaborn.pydata.org/)
* Statistical Analysis Software:
  * [R](https://www.r-project.org/)
  * Python libraries: [pandas](https://pandas.pydata.org/), [numPy](https://numpy.org/)
* Develop Data Quality Assessment Framework (DQAF) or implement already existing ones
* Cross-Validation Techniques:
  * [Scikit-learn - Cross-validation](https://scikit-learn.org/stable/modules/cross_validation.ht)

### Data Cleaning
Data cleaning procedures are essential for ensuring the accuracy and reliability of socio-economic data. This involves identifying and rectifying errors, inconsistencies, and outliers that may arise during data collection or entry. Cleaning procedures may include deduplication to remove redundant entries, standardization of formats to ensure uniformity, and imputation techniques to address missing values.
Existing software can be used for data cleaning, such as python libraries (e.g., pandas or [dedupe]( https://dedupe.readthedocs.io/en/latest/)).

### Interoperability
* Semantic Harmonization: Use standard codes and terminologies for variables to ensure consistency across different data sources and studies.
* Syntactic Harmonization: Adopt standardized data formats to facilitate data integration and comparison across various datasets.

### Statistical Tests for Data Quality
Conduct statistical tests to assess data reliability (e.g., consistency of responses over time) and validity (e.g., the accuracy of the data in measuring what it is intended to measure). Reliability tests assess the consistency of responses over time, ensuring that data trends are dependable and not subject to random fluctuations. Validity tests, on the other hand, examine the accuracy of the data in measuring what they are intended to measure. For instance, in the context of infectious diseases, validity tests might assess whether socio-economic variables accurately reflect the true impact of the disease on different demographics.

### Check Completeness
o	Completeness is the dimension that takes into account the number of variables in a given data model that have actual values. This involves scrutinizing datasets for missing values, ensuring that all relevant variables are captured

### Continuous Monitoring
Implement ongoing monitoring mechanisms to continuously assess data quality. This includes tracking data collection processes, identifying and addressing data quality issues promptly, and updating data collection protocols as needed. This entails establishing protocols for ongoing assessment of data collection processes, automated checks for anomalies or inconsistencies, and regular audits to verify adherence to quality control procedures.

### Regular Communication with Data Sources
Establishing regular communication channels with data sources fosters a collaborative approach to quality control. Maintaining open lines of communication enables swift resolution of any issues or discrepancies identified during quality checks, as stakeholders can promptly provide clarification or rectify errors. Additionally, ongoing dialogue with data sources facilitates mutual understanding of data requirements and collection methodologies, allowing for adjustments to be made in real-time to improve data quality.
