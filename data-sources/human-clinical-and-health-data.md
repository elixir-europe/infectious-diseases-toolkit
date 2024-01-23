---
title: Human clinical and health data
description: Finding and sharing data from human clinical and health data related data sources.
contributors: [Iris Van Dam, Shona Cosgrove, Marcos Casado Barbero, Laura Portell Silva]
page_id: hchd_data_sources
rdmkit:
  - name:
    url:
training:
- name:
  registry:
  url:
rdmkit:
- name: Why are the FAIR principles needed?
  url: https://rdmkit.elixir-europe.org/about#why-are-the-fair-principles-needed
- name: Sharing and reusing of human data
  url: https://rdmkit.elixir-europe.org/human_data#sharing-and-reusing-of-human-data
- name: Identifiers
  url: https://rdmkit.elixir-europe.org/identifiers
- name: GDPR compliance
  url: https://rdmkit.elixir-europe.org/gdpr_compliance
faircookbook:
- name:
  url:

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page_metadata
---

## Introduction

This page is dedicated to human clinical and health data, what they are and where to find them. It details how health data are organised across Europe, how to discover existing data and what to consider when you want to access the data. Last but not least, the page shares some existing approaches to get you started.
So, if this is what you are looking for, look no further! 

### What is considered as human clinical and health data and why is it important for infectious diseases research?

Human clinical and health data are personal data related to the health status of a natural person (Figure 1). In the context of infectious diseases, human clinical and health data are often collected in the context of surveillance or through the provision of health care services. This data is indispensable to make decisions regarding health and management of infectious diseases. As such, it is crucial to know where to find and access it in order to eventually transform the data into usable information and knowledge.

{% include image.html file="Different_health_data_sources.png" alt="Health data types" caption="Figure 1. Data types related to the health status of a natural person (e.g., diagnosis, treatment, laboratory test results)" %}

## Data organisation

The organisation of human clinical and health data can vary across European member states due to differences in national laws, regulations, and healthcare systems. For example, there are differences in the level of:
* **Digitalisation**: in some countries the health information has been fully digitalised. In other countries digitalisation is in progress and yet in others the initial data is still being collected on paper and later digitalised. Nonetheless, COVID-19 has been a major driver for digitalisation, especially for specific data types such as mortality and vaccination data.  
* **Data centralisation**: in some countries the health information has been stored in a more centralised manner (e.g. Estonia, Finland, Hungary, Portugal and Slovenia). In most member states of the European Union the information however remains fragmented across a range of national and regional data holders with decentralised data management (e.g. Belgium, Czech Republic, Germany, Ireland, Netherlands and Sweden). Some examples of different health data management systems across Europe can be found in the report on [Mapping health data management systems through country visits](https://tehdas.eu/results/member-states-readiness-to-benefit-from-the-ehds-regulation-varies/).
* **Private healthcare providers**: in some countries there is limited data sharing from private healthcare providers (e.g. private hospitals, private health insurance or private laboratories). As a consequence this data is often unfindable and thus inaccessible. For example, during the sequence of COVID outbreaks of 2021, private companies often did not report on the number of COVID tests analysed per day.
* **Data protection laws**: all countries within the European Union are subject to the [General Data Protection Regulation (GDPR)](https://eur-lex.europa.eu/eli/reg/2016/679/oj), which establishes strict standards for data privacy and protection. However, European member states have different interpretations of the GDPR and different national regulations on health and research data, adding complexity on how health data can be collected, stored, and shared. For example, European member states have a different legal basis that they rely upon for the secondary use of health data for research by third-party public-sector researchers (e.g. Explicit Consent; Broad consent as defined in national legislation or no specific legislation). Even within a country the different GDPR definitions and interpretations can form a barrier. For example, in Germany there are Data Protection Authorities (DPAs) in each region as well as at a national level which have different definitions of the secondary use of health data. An in-depth overview of the country differences can be found in the report on [‘Assessment of the EU Member States’ rules on health data in the light of GDPR’](https://op.europa.eu/s/yLde).

### Considerations
The above can make it challenging to find and access human clinical and health data. Nonetheless, there are also commonalities in how data is organised and managed across Europe, which might help as a starting point to find and access the data:
* **Electronic health records**: most European countries have implemented some form of electronic health records to store patient health data. These typically include patient demographics and medical information such as diagnoses, medications, treatment plans, immunisation dates, allergies, radiology images, and laboratory and test results. Electronic health records can be accessed by authorised healthcare professionals and are used to support clinical decision-making and continuity of care. For researchers outside of the health system it can be challenging to find and gain access to these records.
* **Health data repositories**: in some countries, national or regional health data repositories have been established to aggregate electronic health records across multiple sources. For example, in Sweden, [the National Patient Register](https://www.socialstyrelsen.se/en/statistics-and-data/registers/national-patient-register/) collects data from all healthcare providers in the country; while in the UK, [the National Health Service (NHS) Digital](https://digital.nhs.uk/) collects data from various healthcare settings. However, in many countries these types of registries are not yet in place.
* **Cross-border health data exchange**: the European Union is working to establish a common framework for cross-border exchange of health data: {% tool "ehds" %}. This initiative aims to facilitate the exchange of health data across borders while ensuring data protection and privacy. The EHDS will include a set of technical standards and protocols to enable interoperability of health data across Europe. Currently the European Genome-phenome Archive (EGA) is expanding into a federation of nodes through the {% tool "fega" %}. FEGA enables deposition and distribution of health data that cannot be stored outside of the country of origin.

## Search and discoverability

As human clinical and health data encompasses sensitive personal data, it requires stringent security measures for its storage, access and distribution. These are often put in place by dedicated controlled access data (CAD) repositories. In many cases, the data cannot leave the original facilities (e.g. hospitals or national institutes of health) due to national requirements that guarantee privacy and security.

### Considerations

* When selecting data sources for your research, it is important to consider their **reliability, relevance**, and **completeness**. Are the data sources trustworthy and up-to-date? Are they relevant to the infectious disease in question and do they have the right data to answer your research question? Are the data sources complete, or are there gaps that need to be taken into account?
* Human clinical and health data can be collected in the form of:
    * electronic health records
    * hospital data
    * pharmacy data
    * laboratory and test result data
    * disease registries
    * insurance claim data
    * mortality data
    * survey data
    * consumer data
* Depending on how the data is collected, the data can be found across different sources and data holders, for example:
    * National Institutes of Public Health;
    * Electronic health records at hospitals or other healthcare providers;
    * International organisations (e.g., ECDC, WHO);
    * Research data networks and consortia.

* **Metadata catalogues:**
As human clinical and health data are organised differently across countries and controlled by different institutes, they can be difficult to find if good metadata are not published. Publicly available metadata catalogues can provide a solution by providing a central place where data users can see what data is available, where it is available, and how they can access it.

### Existing approaches

Data repositories and catalogues are important tools for promoting data sharing and reuse in research. They can help researchers and other users discover (and access) data that might otherwise be difficult to find. Here are some resources that can be useful for you when looking for a place to deposit your data or looking for data for your researcher.
* {% tool "ega" %}: The European Genome-phenome Archive (EGA) is a service for permanent archiving and sharing of personally identifiable genetic, phenotypic, and clinical data generated for the purposes of biomedical research projects or in the context of research-focused healthcare systems. It provides access to a variety of datasets from Europe and beyond.
* {% tool "ema" %}: EMA is a regulatory agency responsible for evaluating and approving medicines for use in Europe. It provides access to various databases and reports on clinical trials, adverse drug reactions, and other aspects of drug safety and efficacy.
* {% tool "ecdc" %}: ECDC collects and analyses data on infectious diseases across Europe. It provides access to various databases and reports on disease outbreaks, surveillance data, and risk assessments.
* {% tool "info-gateway" %}: The European Health Information Gateway is a platform that provides access to various health information resources and datasets from across Europe, including data on health systems, health determinants, and health outcomes.
* {% tool "ecrin-tools" %}: ECRIN is a non-profit organisation that aims to support multinational clinical trials in Europe. ECRIN provides a range of tools and services to help researchers design, conduct, and manage clinical trials across multiple countries. 
* {% tool "health-portal" %}: The aim of the Health Information Portal is to provide access to population health and healthcare data across Europe. The portal is a gateway for researchers and policy makers to make use of the services of the {% tool "phiri" %}. The portal provides access to various resources and datasets, such as data on health determinants, health outcomes and health systems
* {% tool "beacon" %}: An API (usually extended with a user interface) that allows for data discovery of phenoclinic and biomolecular data. .
* {% tool "covid-19-data-portal" %}: Tool that facilitates data sharing and analysis in order to accelerate coronavirus research and acts as a Data sharing platform.

In addition to the European resources, there are many resources available at a national level that are very useful as well, for example:
* {% tool "data-bfarm" %} in Germany;
* {% tool "danish-gateway" %} in Denmark; 
* {% tool "irish-catalogue" %} in Ireland;
* {% tool "portugal-catalogue" %} in Portugal;
* {% tool "findata" %} in Finland;
* {% tool "french-hub" %} in France;
* {% tool "hdr-uk" %} in the UK. 

An overview of additional existing international approaches (not necessarily applicable to Europe) for the sharing and reusing of human data can be found at the [RDMkit](https://rdmkit.elixir-europe.org/human_data#sharing-and-reusing-of-human-data).

## Data access

As human clinical and health data contain sensitive personal information, they are protected under the GDPR within the European Union, as well as national data protection and ethical legislation in different countries. This means that health data are protected by certain legal rules and requirements. 

### Considerations

#### Access procedures

The first step to access data is figuring out the access procedures. Generally, access to sensitive data is granted on a request basis, that is linked to the secondary purposes (a purpose that is different from the original for which the data were collected) of a specific research project. The research protocol of the research project that is requesting data access is generally evaluated by a research ethics committee (REC) and/or a Data Protection Agency (DPA).

Currently, the process for accessing human clinical and health data varies widely between countries, and even between data holders within countries, as health data are often fragmented between many data controllers. Nonetheless, some countries have moved towards centralised data access bodies (i.e., a single point of entry for health data). This is important as it can reduce the burden on users to get access to sensitive data by having less heterogeneous procedures. Examples include:
* {% tool "findata" %} in Finland;
* {% tool "french-hub" %} in France;
* {% tool "hdr-uk" %} in the UK. 
  
#### How access is provided

Across the European Union, three main data access procedures were identified for the secondary use of health data, as described in the [‘Assessment of the EU Member States’ rules on health data in the light of GDPR’](https://op.europa.eu/s/yLde).
* Access is granted after authorisation by research ethics committee (REC) or data protection agency (DPA).
* The data controller provides direct access without engagement of an ethics committee or DPA being required.
* Centralised governance body exists in some form
Nonetheless, the exact procedure will depend on the nature of the research, on how the data are organised within a country  and on the institute that is doing the research. The personal and sensitive nature of health data in turn can impose further requirements when data are reused for research. For example, to ensure that an individual is not re-identified, data are usually pseudonymised (identifiers are replaced with a pseudonym) or anonymised (removing all identifiers so the individual can no longer be identified). Another method to protect sensitive health data is to only allow processing and analysing data within secure processing environments (SPEs), also known as Trusted Research Environments (TREs).

#### Fees

Sometimes fees are charged to access data. Generally, these fees are charged to cover work required for any necessary data processing prior to providing access to data users (e.g., if data needs to be pseudonymised or aggregated). In addition, if data are provided within a secure processing environment (SPE) or trusted research environment (TRE), fees may be charged to support the running of the environment. 

### Existing approaches

#### Research infrastructures

Several health-related research infrastructures (RIs) have been established in Europe, the objective of which is to support researchers by providing resources and services for the research community in their field. One of the ways RIs provide support to researchers is in facilitating access to data. 
Some examples are:
* [Health-RI](https://www.health-ri.nl/), which is a Dutch national initiative to facilitate and stimulate an integrated health data infrastructure accessible for researchers, citizens, care providers and industry.
* [CESSDA](https://www.cessda.eu/), which provides large-scale, integrated and sustainable data services for the social sciences.
* [ELIXIR](https://elixir-europe.org/), which coordinates and develops life science services across Europe within a single infrastructure.
* [ECRIN](https://ecrin.org/), which facilitates researchers to set up and conduct multinational clinical trials in Europe.
  
#### European Health Data Space (EHDS)

In May 2022, the European Commission published a legislative proposal on the {% tool "ehds" %}, with the aim of facilitating the use and re-use of health data in Europe, to improve patient care as well as research and policymaking. One of the objectives of the EHDS is to facilitate access to health data within and across countries, by streamlining access processes. The EHDS proposal states that data holders have the duty to make certain categories of personal health data available for secondary use.
There is currently no standard procedure for the data access application process. This is why the EHDS legislation aims to have a coordinated application procedure across the EU to reduce the complexity and as such facilitate data access and research.