---
title: Pathogen characterisation
description: Generic workflows for different data types.
contributors: [Francesco Messina, Rafael Andrade Buono]
page_id: pc_data_analysis
redirect_from: /pathogen-characterisation/data-analysis
related_pages:
  showcase: [covid19_galaxy_project]
training:
  - name: SARS-CoV-2 data analysis
    registry: Carpentries
    url: https://gallantries.github.io/video-library/modules/covid-analysis
  - name: SARS-CoV-2, viruses and bacteria data analysis
    registry: Carpentries
    url: https://gallantries.github.io/video-library/modules/one-health 
  - name: Pathway analysis with the MINERVA Platform
    registry: Other
    url: https://gxy.io/GTN:T00437
rdmkit:
  - name: “Your tasks: Data Analysis”
    url: https://rdmkit.elixir-europe.org/data_analysis
faircookbook:
  - name: <!---the title of the FAIR Cookbook recipe--->
    url: <!---the full URL of the FAIR Cookbook recipe using following structure, https://w3id.org/faircookbook/XXXXX--->
fairsharing:
  - name: <!---the title of the FAIR Sharing entry--->
    url: <!---the full URL of the FAIR Sharing entry--->

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style-guide when writing the content of this page. -->

## Introduction 

Data analysis for pathogen characterization allows us to understand the evolution of pathogens, and the relationship among different strains and provides insights on host-pathogen interactions and drug resistance. The tasks can involve processing data collected from a diverse spectrum of sources, from both clinical and environmental samples. As in every data analysis procedure, the general workflow involves:

- Preprocessing: Includes the initial steps required to prepare data, genomics and not, for further analysis. 

- Analysis: Is the core stage where the actual detection and characterization of pathogens occur. This stage employs many techniques for pathogen characterization, such as Next-Generation Sequencing (NGS).

- Postprocessing: Includes interpreting and validating the data obtained from the analysis stage, as well as integrating it into broader contexts. Moreover, this is often followed by reporting and communication, and archiving and data management. 


Each stage is crucial for the accurate and comprehensive characterisation of pathogens, from the initial handling of samples to the final reporting and data management, and will be detailed below. 
Scalable and reproducible data analysis activities enable rapid surveillance of infectious epidemics of emerging and re-emerging pathogens in foodborne, hospital settings, and local community outbreaks. Ensuring reproducibility is critical for the usability of the analysis results. Following community-recognised best practices and the FAIR principles (Findability, Accessibility, Interoperability, and Reusability) is fundamental for guaranteeing the trustworthiness of the results and enabling collaboration and sharing of information. 


### General considerations

When analysing pathogen data involved in a health emergency or epidemic outbreak are:
- Define the pathogen and specific aspects to be investigated, e.g. genomic features of interest
- Collect the suitable reference data about the pathogen of interest, preferentially from community-accepted repositories, e.g. ENA, GISAID. It is worth noting that the right reference should be chosen taking into account mutation features, time of isolation, classification, phenotype, and genomic structure.
- Before analysing the data, define which specific aspect of the pathogen’s variability will be investigated. For example, if your aim is to describe the whole variability along the genome, the data should be compared with the whole reference genome.  
- Define the type of data you are using, e.g. DNA or RNAseq for viral genome characterisation
- Select the tools best suited for the analysis of your data
- Estimate the computing resources needed
- Define which computing infrastructure is most suitable, e.g. cluster or cloud
- Ensure to follow the FAIR principles when handling data
- Guarantee findability of the data and tools for all collaborators for reproducibility by providing your:
  - Code
  - Execution environment
  - Workflows
  - Data analysis execution, including parameters used
  - Accompanied by documentation that lists all parameters and other relevant information to reproduce the findings


## Concrete topic 1 <!---REPLACE THIS with the name of the topic. Example: Metadata harmonisation--->

Short explanation of what this topic is about and why it is important, with an emphasis on infectious diseases and the category that you selected e.g. pathogen characterisation.

### Considerations <!---This should not be replaced as these are considerations about concrete topic 1--->

Using a bullet point style list format as much as possible, describe what should be taken into account (i.e. what considerations you should have) for the topic being covered on this page, specifically with regard to infectious diseases in the broader category selected (e.g. pathogen characterisation). This could be, for example; which features are important to consider when selecting data sources?  What capabilities are important when defining tools to be used for quality control? What are general characteristics that you should look for in data standards for human biomolecular data. The considerations provided here should help to justify the existing approaches/solutions described in the next section. 

Please avoid replicating 'generic' guidelines, i.e. those not specific to infectious diseases, here. Add links to RDMkit in the metadata above, if any are needed. Links to other sources can also be provided in text as needed.

### Existing approaches <!---This should not be replaced as these are existing approaches for concrete topic 1--->

Using a bullet point list style as much as possible, describe when, why and for what purpose a specific tool or resource should be used.

Please avoid replicating 'generic' guidelines, i.e. those not specific to infectious diseases.

Avoid making long lists of links to tools and resources. The IDTk does not aim to list all possible approaches and solutions. The focus is on contextualised best practices approaches.

The tools or resources inserted in this section do not have to be considered a 'final' or 'perfect' solution, but should be something that is used by the wider community working in this area or topic. The existing approaches should also reflect the considerations mentioned in the “Considerations” subheading.

Make sure to add to the Tools and resources list table all of the tools and resources mentioned in the text

## Concrete topic 2 <!---REPLACE THIS with the name of the topic. Example: Metadata harmonisation--->

Follow the same guidelines as in Concrete topic 1

### Considerations <!---This should not be replaced as these are considerations about concrete topic 1--->

Follow the same guidelines as in Concrete topic 1

### Existing approaches <!---This should not be replaced as these are existing approaches for concrete topic 1--->

Follow the same guidelines as in Concrete topic 1

<!---add as many topics as need, following the same structure of topic title, Considerations, Existing approaches--->

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->

