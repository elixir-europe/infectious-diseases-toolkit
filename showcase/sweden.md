---
title: Sweden
search_exclude: true <!---leave as “true” until page is ready to be made public--->
country_code: SE
contributors: [Anna Asklöf, Katarina Öjefors Stark, Liane Hughes] 
coordinators: [Liane Hughes]
# Link to other pages in the showcase section on the IDTk by listing the page_id.
# More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website-overview 
related_pages:
  showcase: [<!---REPLACE THIS with the page_id of the showcase pages that you want to list here as related pages--->]

# List the training resources produced by the  specific country in the following spreadsheet: National_training_resources

# Refer to entries of the "main_tool_ and_resource_table" if institutions, organizations and projects from the country contribute to the development of international tools and resources. 
ref_to_main_resources: 
  -  <!---REPLACE THIS with the tool name as it appears in the tools and resources list at Tools and resources list   --->

# List tools and resources mainly relevant for the specific country in the following spreadsheet.
National_tools_and_resources
---

---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style_guide when writing the content of this page. -->

<!--- Showcase pages should detail a particular combination of standards and tools from an infrastructural or domain perspective to tackle infectious diseases related data challenges. --->

This page provides a general overview of resources, tools and data related to the management of infectious disease data in Sweden. Given the recent COVID-19 pandemic, many of the resources featured here are centered around COVID-19. However, the practices, regulations, and other resources on this page can be repurposed for use with other pathogens.

Support for research data management (RDM) both for infectious disease data, and more generally, can be obtained from National Bioinformatics Infrastructure Sweden (NBIS) and the Data Centre at Science for Life Laboratory (SciLifeLab). The two have a [shared data management helpdesk](data-management@scilifelab.se) for providing direct support. In addition, research data offices (RDOs) or Data Access Unit (DAU)(https://data-guidelines.scilifelab.se/topics/university-rdm-resources/) situated at most Swedish universities offer general RDM support. 

## Health authorities
<!--- A section to list and provide context to agencies/authorities/institutions which define public health measures and policies --->

There are three main health authorities in Sweden that determine public health policy, and the measures that should be taken to protect public health. All are government authorities with different responsibilities. 

- **The [Swedish Medical Products Agency (Läkemedelsverket)] (https://www.lakemedelsverket.se/en)** is responsible for the approval of prescription medications and vaccinations, as well as for monitoring their efficacy and safety after approval. It also approves and controls clinical trials. 
 
- **The [Public Health Agency of Sweden (Folkhälsomyndigheten, FoHM)](https://www.folkhalsomyndigheten.se/the-public-health-agency-of-sweden/)** is responsible for monitoring public health issues in Sweden. It collects and aggregates [statistics related to the effect of infectious diseases on public health](https://www.folkhalsomyndigheten.se/folkhalsorapportering-statistik/statistik-a-o/sjukdomsstatistik/) (e.g. the number of cases and hospitalisations resulting from a given pathogen). 

- [**The National Board for Health and  Welfare (Socialstyrelsen)**](https://www.socialstyrelsen.se/en/) is responsible for issuing guidelines and regulations related to public health. It also maintains multiple [clinical registers](https://www.socialstyrelsen.se/en/statistics-and-data/registers/) and [statistics on COVID-19](https://www.socialstyrelsen.se/en/statistics-and-data/statistics/statistics-on-covid-19/).

## Disease surveillance initiatives

Multiple initiatives have been established for disease surveillance in Sweden. Below we give examples of ongoing initiatives. These initiatives generally monitor a broad range of pathogens.

### Wastewater surveillance

Wastewater surveillance has proven to be an effective means of predicting outbreaks, with peaks in viral genome content shown to precede increases in cases and hopitalisations (see e.g. [Wang *et al.* (2022)](https://pubmed.ncbi.nlm.nih.gov/36035197/)
) .

Multiple research groups across Sweden have undertaken surveillance including groups at the [University of Gothenburg](https://www.gu.se/en), [KTH Royal Institute of Technology](https://www.kth.se/en), and [Swedish University of Agricultural Sciences (SLU)](https://www.slu.se/en/). These efforts largely focused on monitoring SARS-CoV-2 throughout the COVID-19 pandemic, but have since expanded to include other pathogens. More information on the work by these groups is on the [Swedish COVID-19 and Pandemic Preparedness Portal](https://www.covid19dataportal.se/dashboards/wastewater/).

### Sentinel monitoring in healthcare

The Swedish Public Health Agency coordinates [sentinel monitoring](https://www.folkhalsomyndigheten.se/mikrobiologi-laboratorieanalyser/mikrobiella-och-immunologiska-overvakningsprogram/sentinelovervakning/) for COVID-19 and influenza. In sentinel monitoring, samples are taken from patients with symptoms of influenza or acute respiratory infections. These samples are analysed by [the Swedish Public Health Agency](https://www.folkhalsomyndigheten.se/the-public-health-agency-of-sweden/). 

The data is then used to inform national policy decisions, and is reported to the public, before being subsequently reported to the [European Centre for Disease Prevention and Control (ECDC)](https://www.ecdc.europa.eu/en). ECDC then reports the date to the [World Health Organisation (WHO)](https://www.who.int/). 

## Dashboards and visualisation platforms

[SARS-CoV-2 antibody tests conducted by the SciLifeLab Autoimmunity and Serology profiling facility]( https://www.covid19dataportal.se/dashboards/serology-statistics/): The dashboard shows the total number of tests conducted, as well as the number of positive and negative tests over time.

[Wastewater monitoring by research groups in Sweden](https://www.covid19dataportal.se/dashboards/wastewater/): The dashboard shows data about the levels of viral genome in wastewater in multiple Swedish cities over time.
[Administration of COVID-19 vaccinations in Sweden](https://www.covid19dataportal.se/dashboards/vaccines/): The dashboard shows vaccine coverage in terms of different doses, different regions, and different age groups.
[Register-based large-scale national population study to monitor COVID-19 vaccination effectiveness and safety](https://www.covid19dataportal.se/dashboards/recovac/): The dashboard shows registry based data related to how vaccination coverage with different doses related to the number of cases and admissions to intensive care units (ICU). It examines different age groups within the whole Swedish population, and different risk categories.
LIANE FROM HERE DOWN! 
https://www.covid19dataportal.se/dashboards/post_covid/, https://www.covid19dataportal.se/dashboards/covid_publications/, https://www.covid19dataportal.se/dashboards/crush_covid/, https://www.covid19dataportal.se/dashboards/symptom_study_sweden/ 
https://experience.arcgis.com/experience/09f821667ce64bf7be6f9f87457ed9aa (FoHM’s dashboard on basic descriptive stats on COVID-19)
https://www.folkhalsomyndigheten.se/PCR-covid-19/ FOHM PCR tests 
https://www.socialstyrelsen.se/statistik-och-data/statistik/statistik-om-covid-19/ Socialstyrelsen - dashboard includes e.g. survival rates, number of patients, postcovid.
https://www.socialstyrelsen.se/statistik-och-data/statistik/statistik-om-covid-19/statistik-relaterad-till-covid-19/ some info on influenza here 

{% include image.html file="" caption="Figure 1. " alt="" %}


## Who is the SHOWCASE intended for?

<!--- In this section you should provide a brief account of the target audience or intended users for the showcase --->

## What can you use the SHOWCASE for?
 
<!--- In this section you should provide a brief summary of the uses of the showcase, i.e. when you would use this showcase resource ---> 

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->


<!---Information about affiliations below will be added to the affiliations.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-an-institution-infrastructure-project-or-funder  --->
