---
title: Sweden
country_code: SE
contributors:
  [Anna Asklöf, Katarina Öjefors Stark, Liane Hughes, Elisabeth Sundström]
coordinators: [Liane Hughes]
# Link to other pages in the showcase section on the IDTk by listing the page_id.
# More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website-overview
related_pages:
  showcase: []

# List the training resources produced by the  specific country in the following spreadsheet:
training:
  - name: The Mathematics and Statistics of Infectious Disease Outbreaks
    registry: GitHub
    url: https://github.com/mhoehle/mt3002-summer2020

# Refer to entries of the "main_tool_and_resource_table" if institutions, organizations and projects from the country contribute to the development of international tools and resources.

national_resources:
  - name: COVID-19 & Pandemic Preparedness Data Portal Sweden
    description: The Swedish COVID-19 & Pandemic Preparedness Data Portal is a hub for data, tools, services, and other resources centred around COVID-19 and pandemic preparedness in Sweden.
    how_to_access:
    instance_of:
    related_pages:
      # More information on which page_id you can use can be found at https://www.infectious-diseases-toolkit.org/contribute/website_overview
      human_biomolecular_data: []
      human_clinical_and_health_data: []
      socioeconomic_data: []
      pathogen_characterisation: []
      showcase: []
    url: http://pandemicpreparednessportal.se/
    registry:
      biotools:
      fairsharing:
      tess:
---

## Introduction

<!---General Infectious diseases data considerations for your country--->

This page provides a general overview of resources, tools, and data related to infectious disease data management in Sweden. The practices, regulations, and other resources listed here may have originally been developed for use with a specific pathogen, but can be repurposed for more general use.

Support for research data management (RDM), both for infectious disease data and more generally, can be obtained from [National Bioinformatics Infrastructure Sweden (NBIS)](https://nbis.se/) and [Science for Life Laboratory (SciLifeLab) Data Centre](https://www.scilifelab.se/data/). The two have a [shared data management helpdesk](mailto:data-management@scilifelab.se) for providing direct support. In addition, [research data offices (RDO) or Data Access Unit (DAU)](https://data-guidelines.scilifelab.se/topics/university-rdm-resources/) situated at most Swedish universities offer general RDM support.

## Health authorities

<!--- A section to list and provide context to agencies/authorities/institutions which define public health measures and policies --->

There are multiple authorities in Sweden that determine public health policy and the measures that should be taken to protect public health. All are government authorities with different responsibilities.

- **[The Swedish Medical Products Agency (Läkemedelsverket)](https://www.lakemedelsverket.se/en)** is responsible for the approval of prescription medications and vaccinations, as well as for monitoring their efficacy and safety after approval. It also approves and controls clinical trials.
- **[The Public Health Agency of Sweden (Folkhälsomyndigheten, FoHM)](https://www.folkhalsomyndigheten.se/the-public-health-agency-of-sweden/)** is responsible for monitoring public health issues in Sweden. It collects and aggregates statistics related to the effect of infectious diseases on public health (e.g. the number of cases and hospitalisations related to infection with a given pathogen). It is possible to search for statistics on many diseases by locating the pathogen in their [statistics directory](https://www.folkhalsomyndigheten.se/folkhalsorapportering-statistik/statistik-a-o/sjukdomsstatistik/).
- **[The National Board for Health and Welfare (Socialstyrelsen)](https://www.socialstyrelsen.se/en/)** is responsible for issuing guidelines and regulations related to public health. It also maintains multiple [clinical registers](https://www.socialstyrelsen.se/en/statistics-and-data/registers/) and [statistics on health and medical care](https://www.socialstyrelsen.se/en/statistics-and-data/statistics/), including COVID-19.

## Disease surveillance initiatives

Multiple initiatives have been established for disease surveillance in Sweden. Below we give examples of ongoing initiatives, which generally monitor a broad range of pathogens.

### Wastewater surveillance

Wastewater surveillance has proven to be an effective means of predicting outbreaks, with peaks in viral genome content shown to precede increases in cases and hospitalisations. This is also true of Swedish wastewater surveillance efforts, with e.g. [Wang _et al._ (2022)](https://pubmed.ncbi.nlm.nih.gov/36035197/) showing that peaks in viral genome content preceded increases in cases by two weeks.

Multiple research groups across Sweden have monitored viral genome content in wastewater, including groups at the [University of Gothenburg (GU)](https://www.gu.se/en), [KTH Royal Institute of Technology (KTH)](https://www.kth.se/en), and [Swedish University of Agricultural Sciences (SLU)](https://www.slu.se/en/). More information on the work by these groups, including the data collected, is on the [Swedish Pathogens Portal](https://www.pathogens.se/dashboards/wastewater/). Throughout the COVID-19 pandemic, each of these groups quantified the levels of SARS-CoV-2 in wastewater (see SARS-CoV-2 data from [GU](https://www.pathogens.se/dashboards/wastewater/covid_quantification/covid_quant_gu/), [KTH](https://www.pathogens.se/dashboards/wastewater/covid_quantification/covid_quant_kth/), and [SLU](https://www.pathogens.se/dashboards/wastewater/covid_quantification/covid_quant_slu/)). The groups also monitor other pathogens in wastewater, and share this data on the Swedish Pathogens Portal. For example, see the dashboards related to [monitoring enteric viruses by GU](https://www.pathogens.se/dashboards/wastewater/enteric_quantification/), or [monitoring influenza by SLU](https://www.pathogens.se/dashboards/wastewater/influenza_quantification/).

### Sentinel monitoring in healthcare

The [Swedish Public Health Agency](https://www.folkhalsomyndigheten.se/the-public-health-agency-of-sweden/) coordinates [sentinel monitoring (information only available in Swedish)](https://www.folkhalsomyndigheten.se/mikrobiologi-laboratorieanalyser/mikrobiella-och-immunologiska-overvakningsprogram/sentinelovervakning/) for COVID-19 and influenza. In sentinel monitoring, samples are taken from patients with symptoms of influenza or acute respiratory infections. These samples are analysed by The Swedish Public Health Agency. The data is then used to inform national policy decisions, and is presented to the public in regular reports (see the 'Hur presenteras data?' (In English: 'How is the data presented?') section of the [sentinel monitoring page (information only available in Swedish)](https://www.folkhalsomyndigheten.se/mikrobiologi-laboratorieanalyser/mikrobiella-och-immunologiska-overvakningsprogram/sentinelovervakning/) to access the public reports). The data is subsequently reported to the [European Centre for Disease Prevention and Control (ECDC)](https://www.ecdc.europa.eu/en), who then reports the data to the [World Health Organisation (WHO)](https://www.who.int/).

## Dashboards and visualisation platforms

- [SARS-CoV-2 antibody tests conducted by the SciLifeLab Autoimmunity and Serology profiling facility](https://www.pathogens.se/dashboards/serology-statistics/): shows the total number of tests conducted, as well as the number of positive and negative tests over time.
- [Wastewater monitoring by research groups in Sweden](https://www.pathogens.se/dashboards/wastewater/): shows data about the levels of viral genomes (e.g. SARS-CoV-2, influenza, enteric viruses) in wastewater in multiple Swedish cities over time.
- [Administration of COVID-19 vaccinations in Sweden](https://www.pathogens.se/dashboards/vaccines/): shows vaccine coverage in terms of different doses, different regions, and different age groups.
- [Register-based large-scale national population study to monitor COVID-19 vaccination effectiveness and safety](https://www.pathogens.se/dashboards/recovac/): uses registry based data to examine how the number of vaccine doses differs across age ranges and how this relates to ICU admissions for the general population. The resource also examines dose level among people in specific risk categories, both in general and when infected with COVID-19.
- [Post COVID-19 condition/long COVID in Sweden](https://www.pathogens.se/dashboards/post_covid/): shows the distribution of patients diagnosed with post COVID-19 condition in Sweden, in terms of age, sex, geography, as well as contacts with healthcare and secondary diagnoses.
- [Swedish COVID-19 Publications](https://www.pathogens.se/dashboards/covid_publications/): shows information about publications related to COVID-19/SARS-CoV-2 that involve at least one person affiliated with a Swedish institution.
- [CRUSH Covid project dashboard](https://www.pathogens.se/dashboards/crush_covid/): a compilation of resources related to the outcomes of the CRUSH Covid project, which mapped outbreaks of COVID-19 in Uppsala and issued reports targeted at minimising the impact on public health (no longer updated as of September 2022).
- [COVID symptom study Sweden](https://www.pathogens.se/dashboards/symptom_study_sweden/): a compilation of resources related to the COVID symptom study Sweden project, which monitored the occurrence of COVID-19 symptoms across different regions of Sweden to estimate the prevalence and distribution of symptomatic cases (no longer updated as of July 2022).
- [COVID-19 test statistics from the National Pandemic Centre](https://www.pathogens.se/dashboards/npc-statistics/): shows the number of tests conducted each week, and the relative proportions of positive, negative, and inconclusive results over time (no longer updated as of December 2020).
- [The Swedish Public Health Agency’s COVID-19 statistics](https://experience.arcgis.com/experience/09f821667ce64bf7be6f9f87457ed9aa): shows data on the number of cases, admissions to intensive care, and mortality related to COVID-19 over time (only available in Swedish).
- [The Swedish Public Health Agency’s information on COVID-19 PCR tests ](https://www.folkhalsomyndigheten.se/PCR-covid-19/): shows the number of PCR tests performed over time in Sweden (only available in Swedish).
- [The National Board for Health and Welfare’s dashboard on COVID-19 statistics](https://www.socialstyrelsen.se/statistik-och-data/statistik/statistik-om-covid-19/): shows information on the number of COVID-19 cases, and survival rates, as well as information on post COVID-19 condition/longcovid both for different regions and over time (only available in Swedish).
- [The National Board for Health and Welfare’s dashboard on data indirectly related to COVID-19](https://www.socialstyrelsen.se/statistik-och-data/statistik/statistik-om-covid-19/statistik-relaterad-till-covid-19/): shows information related to the number of influenza cases over time, as well as general mortality rates in Sweden (only available in Swedish and no longer updated as of January 2022).
- [The Swedish Public Health Agency’s information on influenza and RS virus](https://www.folkhalsomyndigheten.se/folkhalsorapportering-statistik/statistik-a-o/sjukdomsstatistik/influensa-veckorapporter/aktuell-veckorapport-om-influensa/): shows the number of cases in Sweden during the winter season (only available in Swedish).

## National data sources

<!--- A section to list and provide context to national data sources. Data source as defined in BY-COVID - those are online resources in which data can be obtained. --->

- [Database of Swedish COVID-19 publications that make data available](https://www.pathogens.se/datasets/all/) (data is openly available). This resource lists all publications on COVID-19 that involve at least one researcher affiliated with a Swedish research institution and make their data openly available. The data has been categorised according to data type (e.g. social and humanities data, genomics data) to aid users.
- [Data on infectious diseases from The Public Health Agency of Sweden](https://www.folkhalsomyndigheten.se/folkhalsorapportering-statistik/statistik-a-o/sjukdomsstatistik/) (data is openly available). This resource is a directory of statistics (e.g. the number of cases detected, and the number of resulting hospitalisations) collected by the Public Health Agency of Sweden on multiple diseases. The statistics for each pathogen/disease can be accessed by locating a given pathogen in the directory (sorted alphabetically).
- [COVID-19 data sources from The National Board for Health and Welfare](https://www.socialstyrelsen.se/statistik-och-data/statistik/statistik-om-covid-19/) (data is openly available). This resource includes data on post COVID-19 condition (or long COVID), as well as other information on the length of care required after infection with COVID-19.
- [Infectious diseases data sources published on the SciLifeLab Data Repository](https://figshare.scilifelab.se/categories/Biomedical_and_clinical_sciences/24457?categories=24508) (some data is openly available, otherwise access to data is restricted). The SciLifeLab Data Repository includes multiple different types of data (e.g. image data), the information found at the link shows only the data related to infectious disease, regardless of data type.
- [National Patient Register](https://www.socialstyrelsen.se/en/statistics-and-data/registers/national-patient-register/) (access to data is restricted). This resource includes four different types of data about patients; basic patient data (e.g. age), geographic data (e.g. hospital department), administrative data (e.g. data of inpatient check in), and medical data (e.g. main diagnosis).
- [National Prescribed Drug Register](https://www.socialstyrelsen.se/en/statistics-and-data/registers/national-prescribed-drug-register/) (access to data is restricted). This resource provides official statistics related to drugs prescribed in Sweden. It is used to increase patient safety in relation to prescribed drugs.
- [Quality Registry for SARS-CoV-2 data](https://covid19register.se/) (only available in Swedish) (access to data is restricted). This resource provides quality indicators related to SARS-CoV-2 (e.g. the number or PCR tests done overall, and percentage of the population tested).

## Regulations

<!--- Ethical and legal regulations in the country, committees etc --->

In Sweden, ethical reviews, biobanks and the processing of patient data within the healthcare system data is regulated by law. The [Swedish Ethical Review Authority](https://etikprovningsmyndigheten.se/en/) is the Swedish authority performing ethical reviews. Sweden follows European [General Data Protection Regulations (GDPR)](https://eur-lex.europa.eu/legal-content/SV/TXT/?uri=celex%3A32016R0679).

- [The Ethics Review Act](https://www.riksdagen.se/sv/dokument-lagar/dokument/svensk-forfattningssamling/lag-2003460-om-etikprovning-av-forskning-som_sfs-2003-460) (only available in Swedish)
- [The Patient Data Act](https://www.riksdagen.se/sv/dokument-lagar/dokument/svensk-forfattningssamling/patientdatalag-2008355_sfs-2008-355) (only available in Swedish)
- [The Biobank Act](https://www.riksdagen.se/sv/dokument-lagar/dokument/svensk-forfattningssamling/biobankslag-202338_sfs-2023-38) (only available in Swedish)

## Domain-specific infrastructures or resources

<!--- e.g. human data, covid-19. Please, only add domain-specific resources that you think don't fit in the table at the bottom. 3-5 sentences long for each resource--->

Below is a list of national infrastructures and resources that are associated with infectious disease data. They are involved in different stages of the data life cycle.

### National Pandemic Centre

The [National Pandemic Centre (NPC)](https://ki.se/en/mtc/national-pandemic-centre-npc) is a research facility located at [Karolinska Institutet](https://ki.se/en)/[SciLifeLab](https://www.scilifelab.se/). It is responsible for sequencing SARS-CoV-2 variants in Sweden, and collaborates with multiple Swedish regional health agencies and the Swedish Public Health Agency to collect samples and distribute data accordingly.

### Biobank Sweden

[Biobank Sweden](https://biobanksverige.se/en/home/) is the Swedish node of the European biobanking research infrastructure [BBMRI-ERIC](https://www.bbmri-eric.eu/). It facilitates, and promotes collaborations between healthcare, academia, industry, and patient organisations. It develops and maintains the [COVID-19 sample collections database](https://www.pathogens.se/biobanks/) in collaboration with the Swedish Pathogens Portal. The database shows which biobanks collections are available across Sweden, and provides details about the collections (e.g. the size of the collection and conditions for access).

### Genomic Medicine Sweden

[Genomic Medicine Sweden (GMS)](https://genomicmedicine.se/), is a collaboration founded in 2018. It aims to enable genomic innovation to be translated into clinical practice, and to provide a sustainable precision medicine infrastructure. [Infectious disease](https://genomicmedicine.se/en/infectious-diseases/) is one of the seven disease areas covered by GMS. In late 2022 the fourteen partners involved in GMS signed an [agreement for data sharing](https://genomicmedicine.se/en/2022/12/07/national-it-infrastructure-in-operation-to-share-genomics-data-across-healthcare-regions-in-sweden/). It represents the first agreement enabling healthcare data, including genomics data, to be shared throughout Sweden.

### Pandemic Laboratory Preparedness Program

The [Pandemic Laboratory Preparedness (PLP) program](https://www.scilifelab.se/capabilities/pandemic-laboratory-preparedness/) is a SciLifeLab research program commissioned by the Swedish government. It aims to build laboratory capacity to ensure future laboratory preparedness through the development of research, competence, and technology. Information about the projects (including research and development projects), and collaborations with infrastructure and government agencies can be found on the [Swedish Pathogens Portal](https://www.pathogens.se).

### Chemical Biology Consortium Sweden

[Chemical Biology Consortium Sweden (CBCS)](http://www.cbcs.se/) is a SciLifeLab national research infrastructure (i.e. a national infrastructure unit that is funded by SciLifelab). The CBCS enables researchers to find and develop small molecules to understand and decipher the function of biological pathways, including those associated with infectious disease.

### Data-driven Life Science Data Science Nodes

Four national Data Science Nodes (DSNs) have been established as part of the [SciLifeLab and Wallenberg Program for Data-Driven Life Science (DDLS)](https://scilifelab.se/data-driven) initiative. The DSN for the [Epidemiology and Biology of Infection](https://www.scilifelab.se/data-driven/ddls-research/ddls-epidemiology-and-biology-of-infection-ra/), hosted at Umeå University, will coordinate and develop national services for databases and data support as well as bioinformatics support to the Swedish research community focused on infectious diseases. The node will work closely with the [Swedish Pathogens Portal](https://www.pathogens.se).

### Centre for Health Crisis

[The Centre for Health Crisis](https://ki.se/en/collaboration/centre-for-health-crises) has been established at Karolinska Institutet and aims to contribute to building better preparedness for health crises in society, through research, education, and interdisciplinary collaboration.

### Laboratory for Molecular Infection Medicine Sweden

The [Laboratory for Molecular Infection Medicine Sweden (MIMS)](https://www.umu.se/en/mims/) in Umeå is the Nordic EMBL Partnership, a major strategic player in Europe’s molecular understanding of disease mechanisms. MIMS is the focus for basic and translational research in molecular infection medicine.
