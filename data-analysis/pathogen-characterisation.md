---
title: Pathogen characterisation
description: Generic workflows for different data types.
contributors: [Eva Garcia Alvarez, Francesco Messina, Fotis Psomopoulos, Rafael Andrade Buono]
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
  - name: Data Analysis
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


### Existing approaches
- **Container and environments**: Consider using containers and environments to collect and isolate dependencies for tools and pipelines. Environment management systems, such as Conda, help with reproducibility but are not inherently portable across platforms. Containers provide a higher level of portability, being able to encapsulate both the software and its dependencies.
- **Web-based code collaboration platform**: Consider using a centralised location for software developers to store, manage, collaborate, and share their code. For instance, {% tool "github" %}, {% tool "gitlab" %}, or {% tool "bitbucket" %}.
- **Workflow management systems**: Allow you to formalise your workflows in a standardised format and execute them locally or on a remote computer infrastructure. Popular systems are {% tool "nextflow" %} and {% tool "snakemake" %}.
- **Workflow platforms**: Allow users to manage data, run formalised workflows, and review their results. Platforms, such as {% tool "galaxy" %}, may offer multiple interfaces, e.g. web, GUI, and APIs.
- **Reference databases**: Collect the suitable reference data about pathogens to be investigated. {% tool "european-nucleotide-archive" %} and {% tool "gisaid" %} are examples of genomic databases to which researchers share their data. In this context, the European Pathogens Portal aggregates databases relating to pathogens, as well as hosts and their vectors. Other countries host their own instance of the {% tool "pathogens-portal" %}, e.g. see the {% tool "swedish-pathogens-portal" %}Swedish Pathogens Portal [showcase](https://www.infectious-diseases-toolkit.org/showcase/swedish-pathogens-portal).
- **Workflow registries**: Register workflows in platforms, such as {% tool "workflowhub" %}, that facilitate sharing, versioning, and authorship attribution of the pipelines.   


For more general information and solutions on data analysis, you may have a look at the content available on the [RDMkit data analysis page]
(https://rdmkit.elixir-europe.org/data_analysis#what-are-the-best-practices-for-data-analysis). 
While the examples on this page focus on the genomic characterisation of pathogens, similar principles apply to other data types.

## Preprocessing

Data preprocessing is an initial step in data analysis involving the preparation of raw data for the main analysis. It is an important factor in quality control, and involves steps for the cleaning of the data, with the identification of inconsistencies, errors, and missing values. Preprocessing may also include data conversion and transformation steps to get the data in a format compatible with the expected inputs of the chosen analysis pipelines.

### Considerations

Some typical considerations involved in this step:
- **Data cleaning**: Finds and corrects errors in the data. For example,  eliminating duplicates, removing too short genomic reads, and trimming not useful information such as contaminating host data.
- **Quality control checks**: Should be conducted at each step to ensure that the data is suitable for the intended analysis.     	
- **Exclusion of low-quality samples**: Samples with low-quality scores should be marked and removed. In genomics studies, samples with missing values, low sequencing depth, and contaminations might be removed.   

### Existing approaches

Preprocessing steps may depend on the technology used and the pathogen being studied and thus should be adjusted accordingly. Some common approaches in genomics studies include:

- Raw sequences quality check: {% tool "fastqc" %}
- Trimming out adapters and low-quality sequences: {% "trimmomatic" %}
- Quality checks: further information can be found on the [Quality control - Pathogen characterisation](/quality-control/pathogen-characterisation) page.

## Analysis

The analysis of data to characterise a pathogen of interest can involve methodologies from different fields. While genomics approaches are of common interest, analysis of other data types, such as proteomics and metabolomics, and their combination can be of special importance.

### Considerations

- **The computational resources**: Verify that the appropriate computational resources are available. Depending on the volume and complexity of the data, you might need to make use of large computing clusters or cloud computing resources.  
- **The location of your data**: Ensure that the chosen computing infrastructure and platforms have access to the data. It is important to consider the distance between the data storage and computing, as it can significantly impact transfer times and costs.
- **Document the steps**: Report every step of the data analysis process. Including software versions employed, parameters utilised, the computing environment employed, reference genome used, as well as any “manual” data curation steps. More information on recording provenance can be found on the [Provenance pages](/provenance/) 
- **Collaborative analysis**: it is important that partners have access to the data, tools, and workflows. It is crucial that systems are in place to track changes to the tools and workflows used, and that the history of modifications is accessible to all collaborators. 

### Existing approaches

There are several types of analysis that can be performed on pathogen-related data, depending on the specific research question and type of data being analysed. Here are some solutions:
- Consider using the available computational infrastructure to scale up your analysis capabilities. This may include applying for access to large computing cluster resources with e.g. {% tool ëurohpc"%} or making use of public Galaxy servers such as {% tool "galaxy-europe" %}.
- **Genomic analysis**: Including whole genome sequencing (WGS), this analysis allows the interpretation of genetic information encoded along the genome (DNA or RNA). Genomic analysis can be used for a wide range of applications to characterise many aspects of pathogen variability, such as Variants of Concern (VOC) and antimicrobial resistance profiles in bacteria (AMR). Examples of tools that allow us to take into account the genomic characteristics of pathogens (e.g. genomic structure and size, gene annotations, mobile genetic elements) are:
  - Sequence Alignment
    - {% tool "bowtie2" %}
    - {% tool "bwa" %}
    - {% tool "samtools" %}
  - Genome Assembly
    - {% tool "canu"%}
    - {% tool "velvet" %}
    - {% tool "spades" %}
  - Phylogenetic Analysis
    - {% tool "clustalw" %}
    - {% tool "muscle" %}
    - {% tool "mafft" %}
    - {% tool "raxml" %}
    - {% tool "iqtree" %}
  - Molecular Clock
    - {% tool "mrbayes" %}
    - {% tool "beast" %}
    - {% tool "beauti" %}
  - Variant calling
    - {% tool "dragen-gatk" %}
    - {% tool "freebayes" %}
    - {% tool "varscan" %}
  - Annotation
    - {% tool "annovar" %}
    - {% tool "snpeff" %}
    - {% tool "vep" %}
    - {% tool "dbnsfp" %}
  - All-in-one Bioinformatic Tools
    - {% tool "snippy" %}
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

