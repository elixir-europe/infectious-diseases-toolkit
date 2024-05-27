---
title: Human clinical and health data
description: General considerations for human clinical and health data quality control.
contributors: [Vladimira Koudelakova, Eva Garcia Alvarez, Maria A. Rujano, Maria Panagiotopoulou, Bert Droesbeke]
page_id: hchd_quality_control
redirect_from: /human-clinical-and-health-data/quality-control
---

## Introduction
Human clinical and health data are collected at health information systems. Therefore, quality measures are needed in order to avoid as many errors as possible when collecting and processing these data, keeping it reliable. In addition, different information collection systems are used in different health centres, so quality measures should also take interoperability into account. Here we present several considerations, existing approaches, and frameworks for managing quality in clinical and health data.

## Quality assurance of clinical and health data
### Considerations
The management of human clinical and health data entails several steps that are relevant for ensuring their quality:
* Clinical data collection: It is essential to establish and follow standard operating procedures (SOPs) when collecting this type of data to maintain data quality dimensions such as completeness, accuracy, or consistency.
* Data linkage: The basic data collected during the step above might not be enough for a given purpose or study. Thus, it is key to link those data to other relevant records. The quality assurance of this process is key to create the dataset needed, without harming the quality dimensions.
* Sample related data: In many cases clinical data are collected as part of a testing procedure (such as antigen detection or PCR tests). Thus, in these cases it is equally important to take care of the quality of the data linked to the samples. Again, among other quality dimensions, completeness is key so all features related to the sample and its collection need to be present and well documented. 

### Existing approaches
* Clinical data collection: When collecting samples and data for an infectious disease, especially in the case of an outbreak, there are usually some established collection points. In these points, the identity of each tested individual is usually verified using an identification document (e.g., their ID). This allows the registration of their data in a platform used for data collection purposes. As one of the first quality assurance measures, it is important to double check the ID registered in the platform, one approach is comparing it with an existing database. In addition to the personal ID, a unique identifier should be created for each test performed, making it possible to distinguish among them, even if they are related to the same person ID.

  Taking the example from the Czech Republic during the COVID-19 pandemic, the quality of COVID-19 connected clinical data is controlled by several systems. Firstly, all persons tested for the presence of SARS-CoV-2 virus by antigen or PCR tests were controlled on the collection points. The employees of the collection point controlled the IDs of the tested people and registered them to the Information system of infectious diseases (ISIN) of the Czech Republic. The correctness of the personal identification number was controlled against the population register of the Czech Republic during the registration of the person in the ISIN system. The unique personal identification number was generated for foreigners without a valid Czech personal identification number. Moreover, a unique ISIN request number was generated for all registered samples. This number served as a unique identifier of the test.

  To ensure quality assurance of the clinical as well as biomolecular data and proper labelling and sample identification, CovIT software was developed by the Institute of Molecular and Translational Medicine (IMTM), Palacky University in Olomouc, Czech Republic. CovIT system has several modules. First module is designed for collection points. It controls the personal identification number, contact address, correct format of the phone number of the tested person and communicates with the ISIN register.  

* Data linkage: Ensuring data quality is again key in this step, especially paying attention to data quality dimensions such as completeness, accuracy, timeliness or consistency among the different datasets to be linked. One approach is to use standards, specifically on the semantic and syntactic levels, as they facilitate the linkage of databases, especially if they come from different sources.

  Continuing with the example above, the ISIN register is used in the Czech Republic to obtain epidemiological data on the occurrence of patients with infectious diseases (including patients with COVID-19).  It is a universal system whose purpose is to obtain information on the occurrence of infectious diseases to assess the development of the epidemiological situation in the Czech Republic, to monitor the health status of the population and to manage the provision of health care. Data from regional hygiene stations, laboratories and hospitals caring for hospitalised patients were centralised in the ISIN during the SARS-CoV-2 pandemic. The ISIN system is managed by The Institute of Health Information and Statistics of the Czech Republic, an organisational unit of the state and has been established by the Ministry of Health of the Czech Republic.

* Sample related data: Each sample should have a unique ID for its identification. Similarly, this ID would be the one used to link the sample data to the human clinical data. Thus, it is important to control this process to make sure the linkage is accurate. In addition, the quality dimensions mentioned before should be controlled also for these data.

  In the collection point module of the CovIT from the Czech Republic, the unique ISIN request number is generated using online communication with ISIN and a unique barcode containing the ISIN request number is generated and can be printed on the label together with name, surname, and personal identification number and the date and time of sampling. This labelling ensures the correct identification and processing of the sample in the laboratory. The second module of CovIT software is a module for SARS-CoV-2 testing laboratories. After delivery of the sample to the laboratory, it can be registered through barcode scanning and a unique ISIN request number or personal ID filling. All data are transferred from the collection point module, which ensures data accuracy. All important parameters related to the sample identification, storage (ID and plate position) and results are collected in the laboratory module.

  In addition, the IMTM developed a registration portal for the samples that were not collected at the collection points and self-sampled by gargling using a Gargtest self-sampling device. The unique collection tube barcode, personal data and sampling date were registered through a web portal, a unique ISIN request number was generated, and all data were automatically transferred to CovIT software. The same portal was also used to retrieve the results of SARS-CoV-2 testing and self-reporting of risky contacts (based on unique code generated by CovIT and obtained by SMS).

## Data quality frameworks and guidelines
### Considerations
Data quality frameworks and guidelines provide instructions for assessing, improving and maintaining the quality of the data during the different steps of their lifecycle. Usually they include key aspects such as data quality definition, relevant data quality dimensions, data governance and data quality assessment, control and improvement procedures. 

### Existing approaches
This section provides a comprehensive overview and pointers to several frameworks and guidelines aimed at ensuring the quality of human health and clinical research data. These resources cover diverse aspects, ranging from foundational principles to specific methodologies and standards.

* [EMA Data Quality Framework for EU Medicines Regulation](https://www.ema.europa.eu/en/documents/regulatory-procedural-guideline/data-quality-framework-eu-medicines-regulation_en.pdf):
This framework classifies data quality determinants into three categories: foundational (external factors affecting data quality), intrinsic (quality derived from the dataset itself), and question-specific (assessment based on the dataset's intended usage).

* [Data Quality Dimensions](https://ec.europa.eu/eurostat/documents/64157/4392716/ESS-QAF-V1-2final.pdf/bbf5970c-1adf-46c8-afc3-58ce177a0646):
The five dimensions (extensiveness, coherence, timeliness, relevance, and reliability) are crucial for assessing different aspects of data quality. Extensiveness focuses on the amount of available data, coherence on consistency, timeliness on the availability of data at the right time, relevance on data elements useful for specific research questions, and reliability on the overall dependability of data.

* Quality Management System (QMS):
Implementing a QMS, such as those based on ISO standards (e.g., [ISO 14155](https://www.iso.org/standard/71690.html) for clinical trial data, [ISO 13485](https://www.iso.org/standard/59752.html) for medical devices), and [EU Directive 2001/20/EC for GCP](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02001L0020-20090807#:~:text=This%20Directive%20establishes%20specific%20provisions,implementation%20of%20good%20clinical%20practice.) (clinical trial data), is vital. A QMS formalizes processes and responsibilities to achieve quality objectives through planning, assurance, control, and improvement.
 
* Software Development Life Cycle:
Following a software development life cycle, including quality assurance systems, is crucial. Adhering to ISO [250xx](https://iso25000.com/index.php/en/iso-25000-standards) standards ensures appropriate design, development, and testing of software. Additionally, guidelines like the [EMA/226170/2021](https://www.ema.europa.eu/en/documents/regulatory-procedural-guideline/draft-guideline-computerised-systems-and-electronic-data-clinical-trials_en.pdf) provide direction for implementing computerized systems and electronic data in clinical trials.

* International Organization for Standardization (ISO) Standards:
ISO has produced various standards offering frameworks for different data management aspects. [ISO 9000](https://www.iso.org/standard/45481.html) focuses on quality management systems, [ISO 8000](https://www.iso.org/standard/81745.html) on Master Data quality and exchange, and [ISO 25012](https://www.iso.org/standard/35736.html) provides a general data quality model applicable across the data life cycle.
 
* [Semantic Web Principles](https://ieeexplore.ieee.org/document/6337108):
Applying semantic web principles is essential, emphasizing factors such as the availability, accessibility, and reliability of data sources, absence of noise and inconsistencies in raw data, and the use of high-quality validated vocabularies for semantic conversion.
 
* [World Health Organization (WHO) Data Quality Principles](https://cdn.who.int/media/docs/default-source/data-quality-pages/2021_dqa_module-1-framework-and-metrics-19-04-21.pdf?sfvrsn=13c95fb1_3&sequence=1&isAllowed=y):
WHO outlines principles such as accuracy, validity, reliability, completeness, readability, timeliness, punctuality, accessibility, usefulness, confidentiality, and security for ensuring data quality. WHO has produced the [Data Quality Assurance (DQA)](https://www.who.int/data/data-collection-tools/health-service-data/data-quality-assurance-dqa) toolkit to support countries in assessing and improving the quality of Routine Health Information Systems (RHIS) data.

* [Standardization in Digital Health Europe](https://digitalhealtheurope.eu/results-and-publications/digital-health-standards/):
Digital Health Europe defines four categories for standardizing health data: information model, vocabulary/terminology standards, content standards, and communication standards. Standardization is considered fundamental for creating high-quality data.

* [Clinical Trial Registration](https://www.jmir.org/2023/1/e41446):
Clinical trial registration ensures accountability and transparency in clinical research. Timely and accurate data on trial registries are crucial for evaluating reported studies. 

* [TEHDAS Data Quality Framework](https://tehdas.eu/results/tehdas-proposals-for-data-quality-and-utility-in-ehds/):
TEHDAS provides a comprehensive data quality framework covering elements like relevance, accuracy, reliability, coherence, coverage, completeness, and timeliness. Their 13 recommendations address key activities throughout the data life cycle.

* Best Practices and Methodologies:
Several best practices and methodologies from organizations like [OHDSI](https://ohdsi.github.io/TheBookOfOhdsi/DataQuality.html), [BBMRI](https://www.bbmri-eric.eu/services/quality-management/), [ECRIN](https://zenodo.org/records/1240941#.X0UJoMgzY2y), [Health Data Research UK](https://www.hdruk.ac.uk/wp-content/uploads/2020/11/201105-Updates-to-the-Data-Utility-Framework-v2-002.pdf), and [Health Information and Quality Authority in Ireland](https://www.hiqa.ie/areas-we-work/health-information) offer specific approaches to quality assurance and quality control in health data. A recent LinkedIn article entitled [“How can you assess and improve data quality in healthcare?”](https://www.linkedin.com/advice/0/how-can-you-assess-improve-data-quality-healthcare) provides a short expert overview on main points to consider.

* [Porto Declaration](https://www.i-hd.eu/health-data-forum-2022/ihd-porto-declaration-on-health-data-quality-2022/#:~:text=This%20Declaration%20calls%20on%20all%20stakeholders%20to%20urgently%20collaborate%20on,the%20personnel%20needed%20to%20ensure):
The Porto Declaration calls for collaboration to establish standards for data quality assessment and labeling. It urges the development and certification of digital health products with data quality by design and emphasizes the need for educational and organizational changes to improve data quality.

In conclusion, these frameworks and guidelines collectively provide a comprehensive approach to ensuring the quality of health and clinical research data. Researchers and stakeholders are encouraged to leverage these resources to enhance the reliability, accuracy, and usefulness of data, ultimately contributing to improved healthcare outcomes and advancements in medical research.
