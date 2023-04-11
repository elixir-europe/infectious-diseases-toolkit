---
title: Belgium 
country_code: BE 
contributors: [Koen Blot, Ruben Brondeel, Shona Cosgrove, Miriam Saso, Nina Van Goethem]

# Link to other pages in showcase section on the IDTk by listing the page_id.
# More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website_overview 
related_pages:
  showcase: [<!---REPLACE THIS with the page IDs of the showcase pages that you want to list here as related pages--->]

training:
  - name: 
    registry: <!---choose between YouTube, Zenodo, Carpentries, GitHub, TeSS, Other--->
    url:

# Refer to entries of the "main_tool_ and_resource_table" if institutions, organizations and projects from the country contribute to the development of international tools and resources. 
ref_to_main_resources: 
  -  <!---REPLACE THIS with the tool name--->

# List here tools and resources mainly relevant for the specific country
national_resources: 
  - name: <!---REPLACE THIS with the national resources about RDM in life sciences such as local instances of tools, guidelines or regulations--->
    description:
    how_to_access: <!--- REPLACE THIS free text to explain if credentials, login, specific affiliations etc., are needed to access the resource or tool--->
    instance_of: <!--- REPLACE THIS with the tool name of which this resource is an instance of, taken from the all tools and resources page --->
    related_pages:
        # More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website_overview 
        human_biomolecular_data: [<!---REPLACE THIS with the page IDs of the human_biomolecular_data pages that you want to list here as related pages--->]
        human_clinical_and_health_data: [<!---REPLACE THIS with the page IDs of the human_clinical_and_health_data pages that you want to list here as related pages--->]
        socioeconomic_data: [<!---REPLACE THIS with the page IDs of the socioeconomic_data pages that you want to list here as related pages--->]
        pathogen_characterisation: [<!---REPLACE THIS with the page IDs of the pathogen_characterisation pages that you want to list here as related pages--->]
        showcase: [<!---REPLACE THIS with the page IDs of the showcase pages that you want to list here as related pages--->]
    url:
    registry:
      biotools: <!--- DELETE ME if not needed --->
      fairsharing: <!--- DELETE ME if not needed --->
      tess: <!--- DELETE ME if not needed --->
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

## Dashboards and visualization platforms

## National data sources
<!--- A section to list and provide context to national data sources.  In the context of BY-COVID, a data source can be a repository which should include at least the metadata and ideally the data, that might not be directly available when considering sensitive data. Also, repositories should have the capacity to share this data and therefore have a governance model in place on how to do it. It can also include registries of data sources important for the field, with a direct link to the original data sources to be able to request access to the data. --->

## Regulations
<!--- Ethical and legal regulations in the country, committees etc --->

## Domain-specific infrastructures or resources 
<!--- e.g. human data, covid-19. Please, only add domain-specific resources that you think don't fit in the table at the bottom--->

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->
