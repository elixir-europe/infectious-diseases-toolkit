---
title: Estonia
search_exclude: true #leave as “true” until the page is complete and ready to be made public
country_code: EE
contributors: [hedi-ee,diana-pilvar]

# Link to other pages in showcase section on the IDTk by listing the page_id.
# More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website_overview 
related_pages:
  showcase: [korogenoest]

training:
  - name: 
    registry: <!---choose between YouTube, Zenodo, Carpentries, GitHub, TeSS, Other--->
    url:

# Refer to entries of the "main_tool_and_resource_table" if institutions, organizations and projects from the country contribute to the development of international tools and resources. 
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
This page gathers COVID-19 disease data initiatives, dashboards, and datasets that were developed and published during 2020-2024 in Estonia. It also provides information on health authorities and local regulations for data handling and disease control. The primary target audience is the wider scientific community.

## Health authorities
<!--- A section to list and provide context to agencies/authorities/institutions which define public health measures and policies --->
In Estonia, the infectious disease data is mostly collected by [The Estonian Health Board](https://www.terviseamet.ee/en) (HB) and made publicly available as open data. The Health Board also provides guidelines:
* for the health authorities (all guidelines in Estonian)
  * [Monkeypox guidelines for healthcare workers](https://www.terviseamet.ee/et/ahvirougete-juhised-tervishoiutootajatele)
  * [Hospital infections](https://www.terviseamet.ee/et/nakkushaigused-menuu/tervishoiutootajale/haiglanakkus)
* and general public
  * [Monkeypox guidelines](https://www.terviseamet.ee/et/ahvirouged)
  * [COVID-19](https://www.terviseamet.ee/et/nakkus-haigused/covid-19-infoleht)


## Disease surveillance initiatives
The state needed additional surveillance data, and scientists were able to ensure the rapid development and implementation of new methodologies. During the COVID-19 pandemic, in cooperation with the University of Tartu, the following initiatives were implemented:

* __Wastewater surveillance__ was set up in August 2020 [by the researchers of the University of Tartu](https://ut.ee/en/node/113141) (prof Tanel Tenson and Veljo Kisand) and taken over [by the Health Board](https://www.terviseamet.ee/et/reoveeseire-kaardirakendus) by 2022. Based on data from Estonia, the viral load in wastewater increased before a rise in the number of infected people was observed. Furthermore, in certain places such as dormitories and prisons, it can predict outbreaks. In conclusion, wastewater studies have additional value when infection rates are on the rise or decline, but not during a plateau.
* __Prevalence of SARS-CoV-2 IgG antibodies.__ The determination of antibodies allowed for a retrospective assessment of the outbreak's extent and is an important tool for assessing the extent of population immunity. In Estonia, two seroepidemiological studies were conducted in the spring and late summer of 2020 (Koro-Sero-EST 1 ja 2). Moving forward, the determination of antibodies was incorporated into the prevalence study.
* __Prevalence study.__ The primary objectives of active surveillance were to evaluate the widespread presence of SARS-CoV-2 and the prevalence of antibodies. The first stage of the surveillance study took place from April 22nd to 29th, 2020. Adults from all over Estonia were invited to participate in the study based on a random sampling. In total, 33 stages were carried out, with each stage involving 2000 - 2500 participants. The percentage of infected individuals fluctuated from less than 1% during the first wave to over 10% during the fourth wave. Active surveillance provided the most objective overview of the extent of virus presence in Estonia. First stages of prevalence study have been published by [Uusküla et al 2022](https://doi.org/10.1016%2Fj.puhe.2022.02.004).
* __SARS-CoV-2 sequencing__ was started at the University of Tartu in 2020. The KoroGenoEst projects 1-3, also described as a [Showcase](https://www.infectious-diseases-toolkit.org/showcase/korogenoest), led by the University of Tartu, continued their operations up until January 2023. Over three years, a total of 8,990 samples were analyzed. From 2023 onwards, the Health Board assumed responsibility for the sequencing analysis of SARS-CoV-2.
* In August 2020, a COVID-tracking app called Hoia was launched. The app tracked contacts by capturing Bluetooth signals from nearby phones, and if the signal was close and frequent enough, anonymous codes were collected and stored on the phone. If a person with the HOIA app becomes infected, they could alert the app, and those who were considered to have been in close contact with that person were immediately notified. The app was used by 300 000 people but was decommissioned in May 2022.

## Dashboards and visualization platforms

* [koroona.ut.ee](https://koroona.ut.ee/) Multiple dashboards using opendata provided by the Health Board. 
* [Wastewater map](https://www.terviseamet.ee/et/reoveeseire-kaardirakendus). Weekly updated wastewater surveillance data since August 2021. 
* [SARS-CoV-2 sequencing results from Health Boaard](https://www.terviseamet.ee/et/koroonaviirus/sekveneerimine). Since January 2023, the Health Board has taken over the coronavirus sequencing from the University of Tartu and developed the accompanying interactive dashboards. 
* [Health Board coronavirus dashboards](https://www.terviseamet.ee/en/coronavirus-dataset). Official dashboards of the Health Board. The page includes several visualisations using infection, infected individual profiles, hospital treatment and vaccination data.
* [Corona map](https://koroonakaart.ee/en). An interactive dashboard for SARS-CoV-2 testing and vaccination data. Last data update: 02.05.2023
* [Corona statistics at the Postimees news site](https://www.postimees.ee/6931752/graafikud-nadalaga-lisandus-140-gripi-ja-1445-koroonajuhtu). The major newspaper Postimees updated daily the SARS-CoV-2 statistics using the open data from the Health Board. Last data update: 01.05.2023
[Public dashboard on SARS-CoV-2 sequencing results for 2021-2022](https://covid19dataportal.ee/genomics_transcriptomics/) Last data update: 20.03.2023
*[Infectious analysis by Krista Fischer](https://www-1.ms.ut.ee/krista/covid/covid_pildid.html) using open data from the Health Board. Last updated on 14.09.2022
*[Model predictions by Mario Kadastik](https://covid.hep.kbfi.ee/) Using model forecasts, predictive calculations were performed to find the hospitalisation, the intensive care unit and the death toll predictions. All the values are estimated, and if the actual reproduction number (R value) and the model forecast differ, it was expected that the forecast would also be different from reality. The page was last updated on 17.04.2023



## National data sources
<!--- A section to list and provide context to national data sources.  In the context of BY-COVID, a data source can be a repository which should include at least the metadata and ideally the data, that might not be directly available when considering sensitive data. Also, repositories should have the capacity to share this data and therefore have a governance model in place on how to do it. It can also include registries of data sources important for the field, with a direct link to the original data sources to be able to request access to the data. --->
Estonia started to share SARS-CoV-2 testing data openly from the beginning of the pandemic in Estonia in March 2020. The first tests were conducted in February 2020, and as of January 2024, the test statistics are still regularly published on the dedicated Health and Welfare Information Systems Centre of Estonia [opendata page](https://opendata.digilugu.ee/docs/#/). The files need to be downloaded for further usage and should not be directly integrated into websites. The files contain data on:
* [Covid-19 vaccination files](https://opendata.digilugu.ee/docs/#/en/opendata/covid19/vaccination/readme) (updated once per day):
  - Nationwide data
  - Coverage by age groups
  -  Coverage by county
  -  Coverage by age group and county
  -  Coverage by age group by municipality
  -  Coverage by age group by administrative unit
  -  Statistics about institutions which carry out vaccinations
* [SARS-CoV-2 testing files](https://opendata.digilugu.ee/docs/#/en/opendata/covid19/test/readme) (updated once per day):
  - Nationwide positive cases
  - Testresults
  - Average age of cases
  - Location-based statistics
  - County total statistics
* [Covid-19 hospitalisations files](https://opendata.digilugu.ee/docs/#/en/opendata/covid19/hospitalization/readme) (last data shared on 02.05.2023).
  - Average age of patients
  - Time of patients hospitalisation
  - Age and gender profile of patients
  - Timeline of hospitalisation statistics.

All the data above is shared both in json and csv formats.

## Regulations
<!--- Ethical and legal regulations in the country, committees etc --->
In Estonia, a research plan that involves human subjects needs to be approved by an ethics board. The two general ethics boards that researchers can apply to are [(Research Ethics Committee of the University of Tartu](https://ut.ee/en/node/113848) and [Research Ethics Committee of the National Institute for Health Development](https://en.tai.ee/en/about-us/tallinn-medical-research-ethics-commitee).

## Domain-specific infrastructures or resources 
<!--- e.g. human data, covid-19. Please, only add domain-specific resources that you think don't fit in the table at the bottom--->

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->
