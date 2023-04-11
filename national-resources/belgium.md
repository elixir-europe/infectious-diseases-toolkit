---
title: Belgium 
country_code: BE 
contributors: [Koen Blot, Ruben Brondeel, Shona Cosgrove, Miriam Saso, Nina Van Goethem]

# Link to other pages in showcase section on the IDTk by listing the page_id.
# More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website_overview 
related_pages:
  showcase: []

training:
  - name: "Master of Biomedical Sciences: Infectious and Tropical Diseases"
    registry: Other
    url: https://www.uantwerpen.be/en/study/programmes/all-programmes/master-infectious-diseases-research/
    
  - name: "Valentine Vaccine Symposium - University of Antwerp"
    registry: Other 
    url: https://www.uantwerpen.be/nl/congressen/valentijn-vaccinatie-symposium/programma-2023/
    
  - name: "SIMID Annual Course - University of Antwerp"
    registry: Other
    url: https://www.uantwerpen.be/en/research-groups/chermid/education/simid-course/

# Refer to entries of the "main_tool_ and_resource_table" if institutions, organizations and projects from the country contribute to the development of international tools and resources. 
ref_to_main_resources: 
  -  

# List here tools and resources mainly relevant for the specific country
national_resources: 
  - name: Epidemiology of Infectious Diseases (Epistat)
    description: A web based application for visualising and exploring data on infectious diseases monitored by Sciensano.
    how_to_access: Open access
    url: https://epistat.sciensano.be/
  
  - name: COVID Epistat
    description: Dashboard for COVID-19 epidemiological data (vaccination, laboratory testing, wastewater, variants, hospitalised patients, mortality, nursing home patients, mental health indicators, seroprevalence).
    how_to_access: Open access
    url: https://lookerstudio.google.com/embed/u/0/reporting/c14a5cfc-cab7-4812-848c-0369173148ab/page/ZwmOB
      
  - name: Sciensano R Shiny Apps
    description: Shiny is an R package that makes it easy to build interactive web apps straight from R. At Sciensano, several Shiny Apps have been developed to process, analyse and visualise data during the COVID-19 crisis. These include the Surge App (monitoring and data quality of COVID-19 hospitalisations), Indicator App (COVID-19 indicators based on test positivity rates per province), Coverage App (coverage of clinical database on hospitalised patients), Hospital Indicators (forecasting and profile of hospitalised patients), and Quality of reporting (quality indicators of reporting by individual hospitals).
    how_to_access: Restricted access to the specific Shiny Apps developed by Sciensano. Sciensano affiliation needed and added permission (login). 
    instance_of: R Shiny
    url: http://rshiny.sciensano.be/shiny/
    
  - name: R Markdown
    description: Tool at Sciensano for generating weekly and daily reports. 
    how_to_access: Restricted access to specific Sciensano affiliated people 
      
  - name: Sciensano LimeSurvey
    description: Tool for online surveys. 
    how_to_access: Sciensano affiliation needed. 
    instance_of: LimeSurvey
    url: https://surveys.sciensano.be/
      
  - name: DMPonline.be
    description: Tool that provides templates for data management plans.
    how_to_access: Affiliation to one of the listed institutions needed. 
    instance_of: DMP online
    url: https://dmponline.be/
      
  - name: Figures on notifiable infectious diseases
    description: Dashboard for notifiable infectious diseases in Flanders. 
    how_to_access: Open access
    url: https://www.zorg-en-gezondheid.be/cijfers-over-meldingsplichtige-infectieziekten-0
    
  - name: Galaxy Belgium
    description: Belgian Galaxy instance.
    how_to_access: Open access or registered access through LifeScience Login
    instance_of: Galaxy
    url: https://usegalaxy.be/
      
  - name: ELIXIR Belgium ENA upload tool
    description: Belgium Galaxy instance
    how_to_access: Open access or registered access through LifeScience Login
    instance_of: Galaxy
    url: https://www.elixir-belgium.org/services/ena-data-submission-toolbox
      
      
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style_guide when writing the content of this page. -->

<!---All the resources added above will appear on the table at the bottom of the page--->

<!---Following information for the page text--->
<!---If the information is already in another resource, please include the link instead of duplicating information--->
<!---Please focus on resources that are relevant for the whole country for infectious diseases--->

## Introduction 
The responsibility for infectious disease data collection and management in Belgium is divided between several institutes and organizational layers. Belgium is a federated country, with both national and subnational health authorities which have separate responsibilities for infectious diseases. 

The **National Public Health Institute (Sciensano)** is responsible for epidemiology and surveillance of infectious diseases at the national level and transmission of data to the international level (ECDC, WHO). Sciensano coordinates national epidemiological surveillance in collaboration with the **subnational Health Authorities** for Flanders, Brussels, Wallonia and the German-speaking community (see Health Authorities infra). At the subnational level, the federated health authorities are responsible for infection prevention and control. This includes the maintenance of data registries for 1) vaccination and 2) mandatory notification of infectious diseases. This leads to a fragmented system across different communities (Flanders, Wallonia, French-speakers in Brussels, and Dutch-speakers in Brussels), as described below in section ‘National data sources’.

## Health authorities
* **Sciensano (National Public Health Institute)** has several responsibilities for infectious diseases, split between epidemiological and microbiology directions:
  * In terms of [epidemiology of infectious disease](https://www.sciensano.be/en/about-sciensano/sciensanos-organogram/epidemiology-infectious-diseases), Sciensano is responsible for the evaluation of epidemiology and public health impact of all infectious diseases in Belgium, including:
    * Providing support to federal entities in case of outbreaks
    * Transmitting infectious disease epidemiology to international institutes (e.g., ECDC, WHO) 
    * Performing health threat detection through the risk assessment group (RAG)
    * Making recommendations to the health authorities regarding the implementation of measures to combat and prevent infectious diseases
  * The microbiology directions (human and veterinary) are responsible for the  development of expertise in diagnosis and sub-analyses of infectious diseases
  * Also within Sciensano, [healthdata.be](https://healthdata.sciensano.be/) provides a technical infrastructure for the collection of registries, using a pseudonymised national registry number. The platform also facilitates automated data extraction (e.g., from clinical laboratories) and the linkage of registries. 

* The **Federal Service for Public Health** maintains a registry of [minimal hospital dataset](https://www.health.belgium.be/fr/sante/organisation-des-soins-de-sante/hopitaux/systemes-denregistrement/rhm) for reimbursement of hospitals. It was also responsible for the hospital surge capacity management plan during the COVID-19 pandemic. The High Council of Health is a group of experts that provide advice (e.g., on vaccination and other health measures such as masks). 

*  The [Risk Assessment Group (RAG)](https://covid-19.sciensano.be/fr/covid-19-informations-scientifiques) is a group with members from different disease units in Sciensano. It is responsible for continuous health threat detection and assessment in order to provide general management advice to the risk management group. Sciensano coordinates the group and invites external experts to provide input when developing risk assessments. 

* The [Risk Management Group (RMG)](https://www.health.belgium.be/nl/node/37374) decides, in the event of a public health threat, the measures to reduce the risk to the Belgian population. It is composed of representatives of Belgium’s health authorities and coordinated by the National Focal Point for the International Health Regulations of the Federal Public Health Service.

* **Sub-national health authorities** are responsible for infectious disease prevention and control (including vaccination):
  * Flanders: [Vlaams Agentschap Zorg en Gezondheid](https://www.zorg-en-gezondheid.be/) (Flemish Agency for Care and Health)
  * Brussels: [Gemeenschappelijke Gemeenschapcommissie](https://www.ccc-ggc.brussels/nl) (Common Community Commission) 
  * Wallonia: [Agence pour une Vie de Qualité](https://plasma.aviq.be/Home/Index?ReturnUrl=PLASMA) (Agency for a Life of Quality) 
  * German-speaking community: [Hygieneinspektion van Ministerium der Deutschspraghigen Gemeinschaft](https://ostbelgienlive.be/desktopdefault.aspx/tabid-219/753_read-968/) (Hygiene Inspection of the Ministry of the German-speaking Community) 

* [RIZIV-INAMI (Institute for Disease and Disability Insurance)](https://www.riziv.fgov.be/fr/Pages/default.aspx) collects reimbursement data on treatments and diagnostics (e.g., Hep C, HIV). This data can be used for epidemiological purposes. 

* The Interministerial Conference (IMC) brings together 9 Ministers of Health and has the final political decision on proposals given by health authorities. A fragmented public health mandate and policy decision-making process undermines collaborative crisis management and long-term action plans for eradication of infectious diseases. 

* The [Health Care Knowledge Centre (KCE)](https://www.kce.fgov.be/en) provides scientific advice on topics related to healthcare. Topics are generally asked for by public authorities, universities etc. 

* There are approximately 40 [National Reference Centres for Human Microbiology (NRCHMs)](https://www.sciensano.be/nl/nationale-referentiecentra-voor-humane-microbiologie#nrc_nrl-block_1-0) across Belgium, which are reference laboratories with increased expertise and capacity for testing of different pathogens. They usually perform secondary analyses. The network is coordinated by Sciensano. 

* The [Information Security Committee](https://www.ksz-bcss.fgov.be/nl/gegevensbescherming/informatieveiligheidscomite-ivc) has specific tasks in the field of information security, including deliberations for certain types of personal data collection or use. However the ISC is not a supervisory authority under the GDPR (this role is taken by the Data Protection Authority).

* A law to establish a [Health Data Agency (HDA)](https://www.lachambre.be/FLWB/PDF/55/3065/55K3065001.pdf) was approved in March 2023 by the Chamber of Representatives. The aim of the HDA is to facilitate access to health data, in particular for secondary use. 

## Disease surveillance initiatives
**Sciensano** is responsible for the national coordination, analysis and interpretation of multiple [surveillance systems for infectious diseases](https://www.sciensano.be/en/data-collection): 

* **Sentinel network of clinical laboratories (Epilabo)**: collects diagnostic data as well as basic demographic patient information, date, and type of test for 40+ pathogens across Belgium. 

* **Sentinel network of general practitioners (GP)**: collects clinical and microbiological data among patients presenting with acute respiratory infection or influenza-like illness (ILI) presenting at the GP. Microbiological samples are taken among a subset of patients for multiplex PCR testing (16 respiratory pathogens) at the National Reference Centre for Influenza. These results are coupled with the clinical data. 

* **Sentinel network of hospitals for severe acute respiratory infection (SARI)**: collects clinical and microbiological data among all SARI patients admitted among the six participating hospitals. Microbiological samples are taken among a subset of patients for multiplex PCR testing (16 respiratory pathogens) at the National Reference Centre for Influenza. These results are coupled with the clinical data. 

* **General Practitioner (GP) Barometer**: collects data (semi-automatically) on the number of weekly GP consultations for influenza-like illness. 

* Sciensano collects information from subnational health authorities to develop a national registry of [notifiable infectious diseases (MATRA)](https://www.sciensano.be/en/projects/notifiable-infectious-diseases). The health authorities at the subnational level are responsible for identifying which pathogens are mandatory to report and the collection of the data. See the different lists of notifiable diseases:
  * [Flemish community](https://www.zorg-en-gezondheid.be/een-meldingsplichtige-infectieziekte-aangeven) 
  * [French-speaking community](https://matra.sciensano.be/) 
  * [Brussels](https://matra.sciensano.be/bru/)
  * [German-speaking community](https://matra.sciensano.be/) 

* Sciensano coordinates a **network of National Reference Centres (NRCs)** for 40+ infectious diseases. Each NRC reports basic demographic patient information and specific microbiological results (antigen, PCR, sequencing, etc) for their respective pathogen. 

* The **HIV-AIDS Reference Laboratories** report all new HIV diagnoses and the clinical results of their medical follow-ups. 

* PediSurv has a **network of pediatricians and general practitioners** that register clinical cases of six pediatric (vaccine-preventable) infectious diseases: acute flaccid paralysis (including poliomyelitis), measles, mumps, rubella, invasive pneumococcal infection, and hospitalized pertussis cases. 

* **TekenNet/TiqueNet** is a national citizen science platform for the surveillance of tick-bites and erythema migrans in the general population. 

* MEMO+ is a national **citizen science platform for monitoring the presence of the exotic tiger mosquito (Aedes albopictus)**. Photos can be uploaded by citizens to be analyzed by experts at the Institute of Tropical Medicine to assess whether the photo is concordant with a tiger mosquito. If positive, further terrain investigations are performed to confirm its presence with mosquito traps. 

* **Belgian mortality monitoring (Be-MOMO)** collects weekly information on all-cause mortality from an external national data source Statbel (statistics institute). Using mathematical modeling, it monitors periods of excess mortality during the winter (flu) and summer (heat wave) season. 

* A **national surveillance of healthcare-associated infections** monitors bloodstream infections, Clostridiodes difficile, and surgical site infections in the hospital setting. 

* A **sentinel nursing home network for influenza-like illness** is in the process of being developed for the monitoring of clinical and microbiological cases of ILI. 

* During the COVID-19 pandemic, several new surveillance platforms were established to follow the **epidemiology of SARS-CoV-2**. These include: 
    * SARS-CoV-2 laboratory test results (including negative test results, genomic variants)
    * Pharmacy test results
    * Prescription data
    * Wastewater surveillance
    * Clinical surveillance of hospitalized COVID-19 patients
    * Surge capacity surveillance of hospitalized COVID-19 patients
    * National nursing home surveillance of COVID-19 cases
    * Vaccination registry [Vaccinnet+](https://www.vaccinnet.be/Vaccinnet/welkom.do) 
    * Contact tracing 

* Within the healthdata.be infrastructure, it was possible to link these datasets to other national registries.
    * COBHRA - Common Base Registry for HealthCare Actor. This database provides data on healthcare workers and their healthcare organization, to follow up incidence rates per type of healthcare worker.
    * StatBel: national individual-level data on socio-economic status, mortality and cause of death (e.g. infections)
    * IMA-AIM: reimbursement data, allowing to calculate incidence rates among people with comorbidities

## Dashboards and visualization platforms
With the available surveillance systems described above, Sciensano provides both regular reports and, for select pathogens, data visualisation through use of online interactive dashboards:

* [Epistat](https://epistat.sciensano.be/home/) is Sciensano’s data visualisation dashboard, allowing data explorations and visualisations for different infectious diseases
* [COVID Epistat](https://lookerstudio.google.com/embed/u/0/reporting/c14a5cfc-cab7-4812-848c-0369173148ab/page/ZwmOB) is Sciensano’s data visualisation dashboard, specific for COVID-19 related data. It includes the following sub-topics: vaccination, cases, hospitalisation, deaths, tests, municipalities, nursing homes, seroprevalence, mental health, wastewater, variants 
* There are also university or media dashboards, which use Sciensano open data. For example: [University of Hasselt COVID-19 Data Dashboard](https://gjbex.github.io/DSI_UHasselt_covid_dashboard/), [VRT news coronavirus figures](https://www.vrt.be/vrtnws/nl/2021/10/23/coronacijfers/) 

## National data sources
The [surveillance systems](https://www.sciensano.be/en/data-collection) at Sciensano described above are available as data sources, for instance:
* Epilabo 
* Sentinel network of general practitioners (GPs)
* Sentinel network of hospitals for severe acute respiratory infections (SARI): in case of data request, Sciensano has to obtain permission from all six participating hospitals
* General Practitioner (GP) barometer
* Regional registries of notifiable diseases
* Network of National Reference Centres (NRCs)
* HIV-AIDS Reference 
* TekenNet/TiqueNet
* MEMO+
* National surveillance of healthcare-associated infections 
* Sentinel nursing home network for influenza-like illness is in the process of being developed for the monitoring of clinical and microbiological cases of ILI. 
* COVID-19 registries 

[FAIR.healthdata.be](https://fair.healthdata.be/) is a FAIR portal that provides an overview of existing databases with health and health care related data. It aims to steadily make this data discoverable and available to the public to increase public health knowledge. 

Other national data sources can also be reused for monitoring of infectious diseases, or describing the participants in the above registries by linking data at the individual level. These include the following: 

* Socio-demographic data by [Statbel](https://statbel.fgov.be/en) (Belgian statistical office): national individual-level data on socio-economic status, mortality and cause of death (e.g. infections)
* [Minimal hospital dataset (RHM/MZG)](https://www.health.belgium.be/fr/sante/organisation-des-soins-de-sante/hopitaux/systemes-denregistrement/rhm) by Federal Service for Public Health: all non-psychiatric hospitals are obligated to report administrative and medical information, related to the reimbursement of hospitals for the care provided to admitted patients
* Vaccination datasets (Regional level, see below for more information):
    * Federal level: SARS-CoV-2 vaccination
    * Federated health authority  level: vaccination against other infectious diseases
* [RIZIV-INAMI](https://www.riziv.fgov.be/nl/Paginas/default.aspx): national database on diagnostics and treatment reimbursement data
* [IMA-AIM](https://ima-aim.be/): national database on reimbursement data collected by the agency ‘InterMutualistisch Agentschap (IMA) - Agence InterMutualiste (AIM)’ among all Belgian mutuality health insurance funds.
* [Common Base Registry for HealthCare Actor (COBHRA)](https://www.ehealth.fgov.be/ehealthplatform/nl/service-cobrha-common-base-registry-for-healthcare-actor)	: national database by Federal Service for Public Health combining the data of all institutes responsible with the recognition of healthcare actors in Belgium. 
* [Absenteeism registry MEDEX](https://www.health.belgium.be/nl/wie-zijn-wij-0#missie): national database  by Federal Service for Public Health on the declared absenteeism

Most above-mentioned data sources are collected by national institutes. However, the federated health authorities (Flanders, Wallonia, French-speakers in Brussels, and Dutch-speakers in Brussels) are responsible for infection prevention and control. The vaccination registries and mandatory notifiable diseases registries are therefore fragmented. This leads to extra complications in using the registries, as described here. 

**Vaccination registry**:  During the crisis phase, the SARS-CoV-2 vaccination campaign was a combined federal and federated competency. The vaccination registry was collected at the federal level and was the first example of a uniform vaccine registry in Belgium, using the existing Flemish infrastructure [VaccinNet+](https://www.vaccinnet.be/Vaccinnet/welkom.do). Outside of the crisis phase, each federated health authority is responsible for their own vaccine registry. This leads to a fragmented system across different communities and lack of an interoperable vaccine registry. On top of this, it is unclear how representative some vaccine registries are, as not all health-care practitioners may fill in the registry - or it is only filled in for vaccines that are reimbursed. 

This limited usability was highlighted during the monkeypox epidemic. Belgium was not able to proactively follow the number of available and administered vaccinations. The exhaustive SARS-CoV-2 vaccination registry could be linked with individual patient-level infections, hospitalisations and deaths to assess vaccine effectiveness. In theory, this infrastructure with linkages between infection and vaccination data could be developed for non-COVID-19 pathogens. However, due to the fragmented infrastructure across federated health authorities and unclear data quality, this will not be achieved in the short-term period. A concerted effort among all health authorities is primordial to achieve this essential public health goal. 

**Mandatory notifiable infectious diseases**: Each federated health authority is responsible for the monitoring of 40+ notifiable infectious diseases. Although the list of notifiable diseases and specific collected data may vary across the different health authorities, in general the same pathogens are collected with a general template including at a minimum the date of sampling, results, contact details of the treating physician, along with patient age, gender and post code. 

## Regulations
* The [law establishing Sciensano](https://etaamb.openjustice.be/nl/wet-van-25-februari-2018_n2018011241.html) was approved in 2018. Article 4 defines the assignments of Sciensano, including to provide advice to the authorities responsible for health, perform scientific research, certify laboratories, and perform risk assessment, among others. Sciensano is responsible for processing personal data in the context of public health research to support health policy and has a legal mandate for surveillance activities related to public health in Belgium.  

* For access to Sciensano data sources, external investigators with a request for selected data should fill in the [data request form](https://epistat.wiv-isp.be/datarequest). Depending on the type of desired data (anonymized or pseudonymized), the provision of data can be assessed by Sciensano or has to be assessed by the Belgian Information Security Committee based on legal and ethical regulations.

* The [Information Security Committee (ISC)](https://www.ksz-bcss.fgov.be/nl/gegevensbescherming/informatieveiligheidscomite-ivc) was established by [law in September 2018](https://www.ksz-bcss.fgov.be/sites/default/files/assets/veiligheid_en_privacy/ivc_huishoudelijk_reglement.pdf) with the responsibility to protect the privacy of personal data.

* There are four Royal Decrees establishing the mandatory reporting of notifiable infectious diseases at the regional level. 

* A [Royal Decree](https://etaamb.openjustice.be/fr/arrete-royal-du-30-avril-2020_n2021032850.html) defining mandatory reporting of hospital bed occupancy in the context of COVID-19 (Surge Capacity Survey) was adopted in April 2020. 

* A [Royal Decree](https://etaamb.openjustice.be/nl/koninklijk-besluit-van-09-februari-2011_n2011022071.html) setting up the National Reference Centres and their financing was adopted in 2011. 

* In general, Belgium uses consent as the legal basis for secondary use of health data. Ethical committee approval is generally required for processing of personal data. 

## Domain-specific infrastructures or resources 
* The [Belgian SARS-CoV-2 sequencing consortium](https://www.uzleuven.be/nl/laboratoriumgeneeskunde/genomic-surveillance-sars-cov-2-belgium) is coordinated by the national reference centre of KU Leuven. Based on Belgian sequencing data generated on a weekly basis, the overall frequency of SARS-CoV-2 variants is plotted over time, providing a general overview of the variants that have been and are circulating in Belgium. Data is submitted to Sciensano and GISAID.

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->
