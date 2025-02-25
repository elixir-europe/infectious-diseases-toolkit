---
title: Socioeconomic data
description: Tools and methods to assess quality of socio-economics data.
contributors: [Eva Garcia Alvarez, Andreas Scherer, Dilza Campos, Abeer Fadda, Marjan Meurisse, Isabel Cuesta, Sarai Varona]
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

Socioeconomic data play an important role in infectious diseases research by providing insights into how socioeconomic factors such as income, education, and occupation impact the spread, prevention, and treatment of diseases. Socioeconomic data can help identify vulnerable populations, understand patterns of disease transmission, and the effectiveness of interventions, as outlined in this publication ([Khalatbari-Soltani et al., 2020](https://doi.org/10.1136%2Fjech-2020-214297)).

The quality control of socioeconomic data in the context of infectious diseases is crucial for ensuring that such data can be reliably used for research and to generate evidence that can feed into policymaking. Quality control measures should be implemented throughout the entire data lifecycle, from data collection (or generation) to storage, analysis, sharing, and re-use. This requires that a comprehensive and systematic approach is applied throughout the data lifecycle. The approach must focus on, among other things, representativeness, clarity, timeliness, error detection, interoperability, and continuous monitoring.

## Quality dimensions

| **Quality Dimension**       | **Description** |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **Accuracy**       | The extent to which data accurately reflect the real world, the extent to which data are affected by observational biases and measurement errors. |
| **Completeness**   | The extent to which missing or incomplete data occur. |
| **Timeliness**     | The extent to which data are collected in (near) real-time and available in a timely manner for its use, the degree to which data are up-to-date. |
| **Validity**       | The extent to which data meet pre-set criteria (~ validation rules). |
| **Relevance**      | The extent to which data satisfy users’ needs. |
| **Integrity**      | The extent to which data can be traced and connected to other data. |
| **Consistency**    | The extent to which a dataset aligns or is uniform with other datasets. |
| **Representativeness** | The extent to which data reflect real-world population characteristics, extent to which data can be generalized to a target population. |
| **Clarity**        | The ease with which data consumers can understand the metadata. |
| **Currency**       | The extent to which data have real-time value. |
| **Uniqueness**     | The extent to which a dataset is free from duplicate data. |

A review on data quality dimensions for Big Data can be found in this publication ([Ridzuan et al., 2024](https://doi.org/10.1016/j.procs.2024.03.008)).

## Considerations

Below are considerations that must be taken into account when working with socioeconomics data, along with the quality dimensions that they are related to.

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

## Key factors impacting data quality

### Technical aspects

* Lack of standardized data and metadata formats
* Absence of technical solutions
* Lack of detailed information for specific searches
* Semantics: terminology variations
* Unstructured data
* Challenges with patient identification and linkage with other data sources

### Motivation

* Lack of stimulants to use evidence in public health decision-making
* Lack of communication of benefits

### Economic aspects, resources

* “Lack of investments in people, infrastructure, and organizational processes for collecting, storing, analyzing, and sharing data”
* Human resources
  * Insufficient qualified and motivated workforce
  * High workload
  * Lack of supervision

### Political aspects

* Lack of clear policies/regulations
* Uncertainty about the role of data owners
* Conflicts of interests

### Legal, ethical barriers

* Privacy and data protection
* Data minimization

A review of data quality measures in health research is provided in this publication ([Andrade et al., 2023](https://doi.org/10.2196%2F41446)).

## Approaches to assess and improve data quality

### Pilot tests

Conduct pilot tests or preliminary surveys with a subset of the target population to ensure that the survey design works effectively. This helps to identify potential issues with the clarity, relevance, and understanding of the questions before full-scale data collection.

When the data are harvested from existing databases, conduct pilot extractions to verify the data retrieval process. This involves testing the extraction protocols on a small scale to ensure that the data pulled from databases are accurate, relevant, and compatible with the study’s objectives. Pilot testing the data extraction helps to identify and address any discrepancies or issues in data format, completeness, and alignment with the research questions.

Ensuring that you extract the correct data from the database(s) in question helps with representativeness, as you can assess whether data collection methods effectively reach all segments of the population. Examining population coverage helps to identify under-served or marginalised groups whose experiences may be underrepresented in the data, thus enabling more equitable decision-making.

### Timeliness

Implement efficient data collection protocols that ensure rapid access to, and sharing of data. Real-time or near-real-time data collection and processing systems are critical for monitoring the socioeconomic impacts of infectious diseases and for timely decision making.

### Error and inconsistency detection

Perform regular error detection and data cleaning processes. This includes identifying outliers, inconsistencies, and missing data, and then applying corrections accordingly, to improve the overall quality and reliability of the data.

Outliers (i.e. data points that significantly differ from other observations) must be identified. It is key to make a distinction between outliers caused by erroneous data (e.g. due to errors in data entry or measurement), and those caused by real, but perhaps rare, events, as they must be handled differently. Tests like the Z-score and interquartile range (IQR) can be used for outlier detection, but these methods assume normally distributed data, so normalization (such as log transformation) is often necessary. To ensure that outliers are not true rare events, it's important to check related variables from the same samples (multivariate outlier detection). Additionally, consulting domain experts and cross-referencing with other datasets can help validate the outlier's authenticity. This publication ([Boukerche et al., 2020](https://dl.acm.org/doi/abs/10.1145/3381028)) provides an overview of outlier detection methods.

Some methods/tools for detecting errors and inconsistencies are:

* Data Visualisation Tools:
  * Missing data visualization: R package {% tool "naniar" %}
  * Python libraries: {% tool "matplotlib" %}, {% tool "seaborn" %}, {% tool "missingno" %}
* Statistical Analysis Software:
  * Data diagnosis:
    * R package {% tool "dlookr" %}
  * Data validation:
    * R package {% tool "validate-r-package" %}
    * R package {% tool "data-validator-r-package" %}
  * Identify duplicates:
    * R package {% tool "dplyr" %}
    * Python library {% tool "pandas" %}
  * Test missingness patterns:
    * R package {% tool "naniar" %}
  * Outlier detection:
    * R package {% tool "outliers" %}
    * Python library {% tool "pyod" %}
  * Python libraries: {% tool "pandas" %}, {% tool "numpy" %}
* Develop Data Quality Assessment Framework (DQAF) or implement already existing ones
* Cross-Validation Techniques:
  * {% tool "scikit-learn" %} - Cross-validation (python)

An overview of R packages on quality assessment is provided in this publication ([Mariño et al.,2022](https://www.mdpi.com/2076-3417/12/9/4238)).

### Data cleaning

Data cleaning procedures are essential for ensuring the accuracy and reliability of socioeconomic data. This involves identifying and rectifying errors, inconsistencies, missing data, and outliers that may arise during data collection or entry. Cleaning procedures may include de-duplication to remove redundant entries, standardisation of formats to ensure uniformity, and imputation techniques to address missing values. Existing software, such as python libraries (e.g., pandas or dedupe), can be used for data cleaning. Existing software, such as python libraries (e.g., {% tool "pandas" %} or {% tool "dedupe" %}), can be used for data cleaning.

Some tools for data cleaning:

* Statistical Analysis Software:
  * Remove duplicates:
    * R package {% tool "dplyr" %}
    * Python library {% tool "pandas" %}, {% tool "dedupe" %}
  * Handling missing data:
    * Multiple imputation: R package {% tool "mice" %} (Multivariate Imputation by Chained Equations)
    * R package {% tool "missmethods" %}

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

### Quality labels

[QUANTUM project](https://quantumproject.eu/)) is a EU-funded project that aims to create a common label system for Europe that guarantees the quality and utility of datasets for scientific and health innovation purposes. The [repository](https://www.healthinformationportal.eu/data-services/data-quality) will include the compilation of data quality management and quality assurance methods, pipelines, tools (open-source) and experiences (including case studies), initially from QUANTUM and QUANTUM consortium partners but also from the wider community, and other related relevant initiatives. Feel free to provide any comment and/or relevant content to be added there! QUANTUM is an EU-funded project (2024-2026) that aims to create a common label system for Europe that guarantees the quality and utility of datasets for scientific and health innovation purposes. This label system will enable researchers, policymakers, and healthcare professionals to identify high-quality data for research and decision making.
