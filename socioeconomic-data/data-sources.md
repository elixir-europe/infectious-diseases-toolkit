---
title: Data sources
description: Finding and sharing data for socioeconomic related data sources.
contributors: [Simon Saldner, Laura Portell Silva]
page_id: sed_data_sources
rdmkit:
  - name: Data sensitivity
    url: https://rdmkit.elixir-europe.org/sensitive_data
related_pages: 
  showcase: []
  human_biomolecular_data: [hbd_data_sources]
  human_clinical_and_health_data: [hchd_data_sources]
  socioeconomic_data: [sed_data_description]
  pathogen_characterisation: []
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction

This page provides an introduction to socioeconomic data for infectious disease research. It details the relevance and use cases of such data, provides an overview of important sources of socioeconomic data, as well as how it can complement other data sources such as human clinical and health data.

## What is socioeconomics data, and why is it important for infectious diseases research?

Social science research is devoted to studying societal phenomena, social changes and the impact on the individuals. The discipline includes branches such as political science, psychology, economics, and sociology, among several others. All disciplines of social sciences have a common ground of producing knowledge around the study of various aspects of human action and cultural interaction.

Social science data can provide important insights for infectious diseases research, as well as policy for disease preparedness and mitigation. For example, social sciences can help understand how infectious diseases spread among and impact different segments of society such as different socioeconomic groups or economic sectors; how effective different government strategies are at combating the spread of a virus; or how political and psychological factors can affect vaccine uptake; provide the socioeconomic elements on which policies and communication actions should focus and/or adapt in order to be more efficient.

For these reasons, the social sciences are considered an integral part of the BY-COVID project. The project aims to mobilize social science data via the {% tool "covid-19-data-portal" %}; to connect it with other sources of data such as clinical or virological data; to standardize social science data; and provide methods and protocols for exposing and analysing it. 

### Considerations

- **Methodologies**: Social sciences methodologies are quite diverse and complex as they try to investigate complex, changeable, and often intangible social phenomena such as trust, ideology, or socioeconomic status. Thus, social sciences use both quantitative and qualitative research methods, often in combination, ranging from large scale quantitative surveys, to interviews or ethnographic research. As such, socioeconomic research methodologies and data often differs significantly from the those typically used in the life sciences. 
- **Sensitive data and privacy**: due to the prevalence of sensitive and personal data in the domain of socioeconomic research, access to such data is often limited by serious data protection and privacy concerns, often making the use and sharing of such data difficult. Solutions such as pseudonymising data, or providing access via secure environments such as the {% tool "oddisei-secure-analysis-environment" %} can often provide some level of access to sensitive data, yet much of this data is only available on request, or as aggregated data. 

### Existing approaches

The pandemic of COVID-19 has shown the impact of socioeconomic factors in terms of governance and state-citizens relations when it comes to an efficient response of science (to deal with infectious diseases) for the benefit of the society. 

Indicatively, there has been a considerable number of social  surveys dealing with the pandemic and its consequences in several aspects of the everyday life of citizens at global and EU level. There has been, compared to previous pandemics, a major difference, meaning that the progress of information, digitisation, statistics included, citizens were aware of the extent, the seriousness of the various whilst at the same time citizens received information about scientific efforts and achievements to deal with diseases. 

From the demography perspective, there have been surveys and related publications proving the relation of household structures, housing conditions ([Giorgi & Boertien 2021](https://doi.org/10.1186/s41118-021-00124-8)), the role of nursing homes, especially during the first wave ([Bernandi et al. 2021](https://doi.org/10.1186/s41118-021-00119-5)), the role of gender or socioeconomic status ([Horton 2020](https://pubmed.ncbi.nlm.nih.gov/32979964/)) etc. From the perspective of political science, psychology or sociology sciences’  perspective, surveys that studied the effect of conspiracy theories regarding vaccines, propagation of virus and others, have show clusters of people that relate resistance to vaccines with respect to personal ideology , adherence to conspiracy theories or that lower level of education, religiosity, conspiracy thinking can be an indicator for vaccine resistance (Haaksonen & Furman 2022). 
 
Even industrial advanced societies proved that they were not well-prepared to combat the devastated pandemic. Lessons learnt should focus on how to adjust health systems responses but also to find ways to strengthen trust among citizens building on resilience, access to information and services for all. 

## Relevant data sources

<!--- Subsection related to a specific topic related to the data sources of the category that you selected.--->

Currently, the COVID-19 Data Portal contains over 537 metadata records from the [Consortium of European Social Science Data Archives' (CESSDA)](https://www.cessda.eu/) {% tool "cessda-data-catalogue" %}, which will soon be joined by data from the [European University Institute's (EUI)](https://www.eui.eu/en/home) {% tool "eui-covid-19-ssh-data-portal" %}. BY-COVID also aims to add additional data sources over time. 

The relevant work in the BY-COVID project is performed in the context of activities related to relevant socio-economics data sources for infectious disease outbreaks led by KNAW-DANS and with the participation and expertise of TAU-FSD, EKKE, and EUI. KNAW-DANS, TAU-FSD and EKKE participate in the project as affiliated entities of CESSDA. 

BY-COVID uses two primary, and multiple secondary data sources for socioeconomic data, which will be outlined in this section. Both primary and secondary data sources provide data that relate to or are relevant for COVID-19 and other infectious disease outbreaks, and therefore the BY-COVID project. The two primary data were determined early on the project, while the list of secondary sources will be progressively identified throughout the course of the project. These data sources are filtered for data relevant to the project, and the resulting metadata is prepared and harmonized via a [harvesting tool](https://t2-4.by-covid.bsc.es/jspui/) before being added to the COVID-19 Data Platform (for more details, see project deliverable [D2.1](https://zenodo.org/record/7017728)).


### Considerations

- **Licenses**: Socio-economic data sources are generally public and accessible, but authorization or licensing agreements may be required to access some datasets. While the complete datasets may not always be openly available, the metadata is typically freely accessible. Socio-economic data sources in the BY-COVID project also offer programmatic access to their metadata using standards like the Open Archives Initiative Protocol for Metadata Harvesting (OAI-PMH). This enables the automated harvesting, harmonisation, and transformation of metadata into the OmicsDI format, which can then be used by the COVID-19 Data Portal.

### Existing approaches

- {% tool "cessda-data-catalogue" %}: As a consortium of Social Science Data Archives with Service Providers (SPs) from [22 member states](https://www.cessda.eu/About/Consortium), CESSDA contains a wealth of social science data from throughout Europe. This data is aggregated through the CDC, which contains descriptors of over 40,000 data collections from CESSDA's SPs.  
- {% tool "eui-covid-19-ssh-data-portal" %}: This portal "*provides integrated search, discovery, and linking to datasets published on the web relevant for COVID-19-related research in the Social Sciences and Humanities.*" The metadata provided by the platform comes from data sources selected by academic staff at EUI through a thorough curation process, and the platform will develop bespoke services such as the ability to merge data from multiple data sources. 
