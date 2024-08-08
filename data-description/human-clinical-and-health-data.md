---
title: Human clinical and health data
description: Guidance in describing human clinical and health data.
contributors: [Miriam Saso, Pierluca Piselli, Shona Cosgrove, Iris Van Dam, Romain David, Hedi Peterson, Diana Pilvar]
page_id: hchd_data_description
redirect_from: /human-clinical-and-health-data/data-description
rdmkit:
  - name: Human Data
    url: https://rdmkit.elixir-europe.org/human_data
faircookbook: 
  - name: Selecting an ontology lookup service
    url: https://w3id.org/faircookbook.elixir-europe.org/content/recipes/infrastructure/vocabularies/Selecting_and_using_ontology_lookup_services.html 
  - name: Deploying EBI Ontology Lookup Service
    url: https://w3id.org/faircookbook.elixir-europe.org/content/recipes/infrastructure/vocabularies/UC3_R13_local_ontology_services.html
  - name: Introducing vocabulary portals and lookup services
    url: https://w3id.org/faircookbook.elixir-europe.org/content/recipes/infrastructure/vocabularies/technical-and-architectural-selection-criteria-of-ontology-lookup-services.html 
  - name: Selecting terminologies and ontologies
    url: https://w3id.org/faircookbook.elixir-europe.org/content/recipes/interoperability/selecting-ontologies.html

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction 

Human clinical and health data are personal data related to the health status of a natural person (e.g. diagnosis, treatment, laboratory test results [(glossary)](https://doi.org/10.5281/zenodo.6787119)). As this includes a wide variety of data, it is essential to precisely describe which type of data researchers use in their work and for which purpose.

In this regard, a data management plan and metadata records play a key role. Data description is also key to helping one find the data needed, for instance, in metadata catalogues.

Human clinical and health data can be generated through research, be it through cohort studies, population studies, or health interview surveys. General information about health data can be found on the [RDMkit website](https://rdmkit.elixir-europe.org/human_data).

Health data can also be generated when an individual interacts with the health care system by going to the doctor, being hospitalised or buying medication at the pharmacy. In more detail, this is described below and on the [Data Sources page](/data-sources/human-clinical-and-health-data).

When this data is used for a different purpose than its initial goal, it is referred to as “secondary use.” This is, among others, important to ensure adequate policy responses during (future) infectious disease outbreaks and to take well-informed public health measures where necessary.


## Health (meta)data

Human health metadata refers to information that describes the content, context, quality, and structure of health-related data. This metadata is crucial for ensuring that clinical and health data can be accurately interpreted, shared, and reused across different systems and studies. Proper metadata enhances data interoperability, facilitates comprehensive data analysis, and supports the reproducibility of research findings.

### Metadata
Metadata is information about data, which allows researchers to make their data findable, accessible, interoperable, and reusable. Data value drastically increases when that data can then be collected once and reused many times.

In general, [four main types of metadata can be encountered](https://faircookbook.elixir-europe.org/content/recipes/introduction/metadata-fair.html):

 1. **Descriptive metadata** in human health data includes patient demographic information such as name, age, gender, and medical history. This helps in identifying and discovering data.
 2. **Structural metadata** refers to the organisation of a patient's electronic health record (EHR), detailing how different data fields, such as lab results, medications, and visit notes, are interrelated.
 3. **Administrative metadata** covers data access controls, data ownership, and the timing of data collection, all of which facilitate data management.
 4. **Quality metadata** includes indicators such as the accuracy, completeness, reliability, and validity of lab test results. This ensures data reliability for analysis and decision-making.

Metadata in health data is essential for:

 * Data integration: Facilitates combining data from diverse sources.
 * Data quality: Ensures accuracy and consistency in data recording.
 * Data discovery: Helps researchers locate and understand datasets.
 * Regulatory compliance: Ensures adherence to privacy and security standards.

To achieve greater results, metadata standards have been developed across different domains, increasing metadata records' interoperability. Such standards can have different functions and therefore, have a complementary role to each other.

It is important that one’s study is planned with [data sharing](https://rdmkit.elixir-europe.org/data_publication) in mind when applicable. This will help identify the information necessary to share data effectively and make it easier to generate well-structured and complete documentation.

#### Relevance of metadata in Infectious Disease Data

Metadata is essential in infectious disease settings for:

 * Tracking and surveillance: enables effective monitoring of disease incidence and spread.
 * Data integration: facilitates combining data from various healthcare systems for comprehensive analysis.
 * Research and Public Health: supports epidemiological studies and public health interventions.
 * Regulatory compliance: ensures data privacy and security standards are met.

#### Considerations 

 * The infectious disease field is rather new to the concept of metadata, so cataloguing information about datasets is implemented less systematically than in other fields. However, with the new [European Health Data Space](https://health.ec.europa.eu/ehealth-digital-health-and-care/european-health-data-space_en#:~:text=The%20European%20Health%20Data%20Space%20will%20provide%20a%20trustworthy%20setting,Network%20and%20Information%20Systems%20Directive.) legislation, this is likely to change soon. One of the key action points of the legislation includes the development of national metadata catalogues for promoting the reusability of data. Front runners such as Finland ([Findata](https://findata.fi/en/)) will have little to do. Most other European countries, though, have started discussions on how to begin or continue developing a metadata catalogue for health data. 
 * Given the diverse types and sources of human clinical and health data, it is crucial to provide detailed information about study and data collection methods. This allows researchers to assess the reliability of the data and how competently it was generated. The information is usually organised following research community guidelines, and then structured as metadata to make the data FAIR. In a registered study, it is important to give information that helps people retrieve more information on the study itself (e.g. external links and published material).
 * It is crucial and mandatory to describe how the privacy of human research subjects and patients was guaranteed. Whilst providing complete data descriptions is advisable, some data will need to be anonymised before it can be shared. You should describe how and why sensitive data were masked or removed (see [Handling of health data](#handling-of-health-data) below)

#### Existing approaches 
 * **Generic metadata standards**
    * {% tool "dcat"%} is a metadata standard for publishing data catalogues on the web. It facilitates sharing of data and the interoperability between data catalogues. Furthermore, it allows for federated searches of datasets across catalogues on multiple sites. This further increases the findability of data.
    * DCAT extension: One of the European Commission’s key priorities for 2019-2025 has been the creation of a {% tool "ehds" %} to promote digital transformation, and to optimise and widen the use of health data. In this regard, The [EHDS-2 Pilot](https://www.ehds2pilot.eu/) is developing a DCAT extension capable of capturing key information that should be available on a metadata record related to health data. 
    * {% tool "schema-org" %} is a metadata standard that helps search engines index web pages. It improves the machine-readability of the pages and so increases the discoverability of datasets. Schema.org tags also add semantics, and allow search engines to understand the type of content available on the web page.
 * Standards such as HL7 and OMOP provide consistent frameworks for data representation. These standards ensure that health data is formatted and structured in a way that allows for seamless sharing and integration across different healthcare systems and studies.
    * HL7 (Health Level Seven International): HL7 is a set of international standards for the exchange, integration, sharing, and retrieval of electronic health information. It provides a framework for managing clinical and administrative data. While HL7 includes some ontological components, it is primarily a set of standards rather than a pure ontology.
    * [OMOP (Observational Medical Outcomes Partnership)](https://ohdsi.github.io/CommonDataModel/): OMOP is a standardised data model and common data vocabulary. It is designed to facilitate the analysis of disparate observational healthcare databases, to improve the assessment of healthcare outcomes and safety. It goes beyond an ontological component (the OMOP Common Data Model and Vocabulary), and encompasses data standardisation and analytics frameworks.

### Ontologies
An ontology is a formal description of knowledge as a set of concepts within a domain, and the relationships that exist between them. It ensures a common understanding of information and makes explicit domain assumptions, thus allowing organisations to make better sense of their data ([Fundamentals, O. (2022, December 16)](https://www.ontotext.com/knowledgehub/fundamentals/what-are-ontologies/#:~:text=An%20ontology%20is%20a%20formal,better%20sense%20of%20their%20data)). 

An ontology, on its own, allows researchers to be specific about describing the phenomena they work with, such as in the annotations of datasets. This facilitates the identification and retrieval of relevant information. More information at the [RDMkit](https://rdmkit.elixir-europe.org/metadata_management#how-do-you-find-appropriate-vocabularies-or-ontologies).

#### Considerations

When developing and using health data ontologies, consider the following: 

 * **Interoperability** is crucial to ensure that ontologies are compatible with various healthcare systems and data standards, such as HL7 and OMOP. This interoperability will facilitate data exchange and integration.
 * **Scalability** is another key factor, as ontologies must be designed to accommodate the growing volume and complexity of health data, including new diseases and treatments. 
 * **Usability** of ontologies is vital, ensuring they are user-friendly for healthcare providers and researchers, and supported by clear documentation and tools like the Ontology Lookup Service (OLS) and NCBO BioPortal.
 * **Data quality** considerations involve ensuring that ontologies contribute to the accuracy, reliability, and completeness of health data. This is fundamental for high-quality data analysis and decision-making. 
 * **Privacy and ethics** are paramount, addressing concerns related to data confidentiality and ethical use, which should be incorporated into the ontology design to guide responsible data handling practices.

#### Existing Approaches

 * For interoperability, standardisation is essential for maintaining consistency and accuracy in data representation, which can be achieved by utilising widely accepted vocabularies like ICD-10 and SNOMED CT.
 * Tools like the Ontology Lookup Service (OLS) and NCBO BioPortal provide access to various biomedical ontologies, supporting standardisation efforts and improving data quality and utility. These resources help researchers and healthcare providers ensure that their data adheres to the highest standards of accuracy and consistency.
    * {% tool "bioportal" %}: NCBO BioPortal is an extensive repository and web-based platform that provides access to a wide array of biomedical ontologies and terminologies, enabling users to search, browse, and utilise these resources for research and data annotation purposes.
    * {% tool "ols" %}: The Ontology Lookup Service (OLS) is a web-based tool that provides a single point of access to multiple ontologies, enabling users to search and browse a wide range of biomedical and health-related terminologies and ontologies.
    * {% tool "the-open-biological-and-biomedical-ontology-foundry" %}: The OBO Foundry is a collaborative initiative that aims to develop a family of interoperable ontologies designed for biomedical science. It provides principles and best practices for ontology development. These ensure that ontologies are logically well-formed, scientifically accurate, and useful for data integration across different biological and medical domains.
    * ICD-10 is a medical classification system maintained by the World Health Organization (WHO). It provides codes for diseases, signs and symptoms, abnormal findings, complaints, social circumstances, and external causes of injury or diseases. It serves as a comprehensive ontology for clinical diagnoses and health conditions, enabling standardised recording and reporting of health information across different healthcare systems.

By adhering to these standards and ontologies, healthcare providers and researchers can improve data management, leading to better disease tracking, treatment outcomes, and public health responses.

## Handling of health data

Human clinical and health data can contain personal information about individuals, therefore it is considered sensitive. To protect the privacy of those to whom the data belong, the [General Data Protection Regulation](https://gdpr.eu/what-is-gdpr/#:~:text=The%20General%20Data%20Protection%20Regulation,to%20people%20in%20the%20EU.) is in place at the European level to safeguard the privacy of European citizens. 

### Considerations 
Handling health data, especially in the context of infectious diseases, requires careful consideration due to the sensitive nature of the information and the potential for widespread public health implications. Here are the main considerations to keep in mind:


 * **Privacy and confidentiality:** ensuring the privacy and confidentiality of patient data is paramount. This involves complying with legal and ethical standards.
 * **Data security:** implement robust security measures to protect health data from unauthorised access, breaches, and other cybersecurity threats. This includes using encryption, secure data storage solutions, and secure communication channels for transmitting data.
 * **Data accuracy and integrity:** accurate data is crucial in managing infectious diseases. Errors in data can lead to incorrect assessments and interventions.
 * **Data sharing and accessibility:** facilitating the appropriate sharing of health data among healthcare providers, researchers, and public health officials is essential for effective infectious disease management and research. However, it must be balanced with privacy concerns. Agreements and protocols should be in place to guide safe and ethical data sharing.
 * **Compliance with regulations:** adhering to national and international laws and guidelines concerning the handling of health data is crucial. Different countries may have different regulations and understanding these is necessary to ensure compliance.
 * **Ethical considerations:** ethical issues must be considered, especially when handling data related to infectious diseases, which can often lead to stigma and discrimination against certain populations. Ethical use of data should promote fairness, respect, and justice.
 * **Data minimisation:** collect only the data that is necessary for health purposes to minimise potential harm. This practice helps in reducing the risk of unnecessary exposure of sensitive information.
 * **Public trust and transparency:** maintaining public trust in how health data is handled is vital, especially during outbreaks. Transparent practices about what data is collected, how it is used, and who it is shared with can help in maintaining public trust.
 * **Interoperability:** ensuring that systems used for recording and storing health data are interoperable can greatly enhance the efficiency and effectiveness of disease surveillance and management. This means systems should be able to exchange data seamlessly and use shared standards.
 * **Real-time surveillance and reporting:** for infectious diseases, the ability to monitor and report data in real-time can be essential in controlling outbreaks. Systems should be designed to support timely and accurate reporting.

### Existing approaches 

 * During the COVID-19 pandemic, many countries implemented [contact tracing apps](https://commission.europa.eu/strategy-and-policy/coronavirus-response/travel-during-coronavirus-pandemic/contact-tracing-and-warning-apps-during-covid-19_en ) that anonymised user data to protect individual privacy. 
 * The use of [blockchain technology in Estonia’s digital healthcare](https://e-estonia.com/blockchain-healthcare-estonian-experience/) system enhances the security of health data by creating tamper-proof records for every patient encounter.
 * [The WHO’s Global Influenza Surveillance and Response System (GISRS)](https://www.who.int/initiatives/global-influenza-surveillance-and-response-system) provides standardised testing procedures and reagents to laboratories worldwide, ensuring the accuracy and reliability of influenza data globally.
 * Data should be shared as openly and as rapidly as possible, for example by uploading SARS-CoV-2 sequence to {% tool "european-nucleotide-archive" %}. ENA  is an open, supported platform for the management, sharing, integration, archiving and dissemination of sequence data. 
 * {% tool "gisaid"%} Data Science Initiative platform promotes the rapid sharing of data, from priority pathogens including influenza, hCoV-19, respiratory syncytial virus (RSV), hMpxV as well as arboviruses including chikungunya, dengue and zika. It includes genetic sequence and related clinical and epidemiological data associated with human viruses, and geographical as well as species-specific data associated with avian and other animal viruses. However, GISAID is much more restrictive on data reuse compared to ENA, for example. 
 * The European Union’s General Data Protection Regulation (GDPR) includes specific provisions for processing health data, such as requiring explicit consent from individuals and allowing data processing when necessary for reasons of public interest. Please also take into account local laws and regulations.
 * During the Ebola outbreak in West Africa, [ethical guidelines](https://bioethics.jhu.edu/wp-content/uploads/2019/03/Ethics20Guidance20for20Public20Health20Containment20Lessons20from20Ebola_April2019.pdf ) for data sharing were established that balanced the need for rapid data sharing with the need to protect communities and individuals from harm, addressing issues like consent and the potential for stigmatization.
 * [European Centre for Disease Prevention and Control (CDC)](https://www.ecdc.europa.eu/en) regularly publishes detailed reports and datasets on its website regarding disease outbreaks and surveillance data, improving transparency and helping to maintain public trust.
 * [Health Level Seven International (HL7)](https://www.hl7.org/) and Fast Healthcare Interoperability Resources (FHIR) are standards that facilitate the exchange of healthcare information electronically, allowing different health information systems to work together more effectively.
 * The use of Electronic Health Records (EHRs) integrated with real-time alerting systems has been implemented in hospitals to flag potential infectious disease cases based on symptoms and travel history, enabling prompt isolation and treatment.

