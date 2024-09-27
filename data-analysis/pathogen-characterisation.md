---
title: Pathogen characterisation
description: Analysing Pathogen related data.
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
---
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
- Collect the suitable reference data about the pathogen of interest, preferentially from community-accepted repositories, e.g. {% tool "european-nucleotide-archive" %} and {% tool "gisaid" %}. It is worth noting that the right reference should be chosen taking into account mutation features, time of isolation, classification, phenotype, and genomic structure.
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
- Trimming out adapters and low-quality sequences: {% tool "trimmomatic" %}
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
- Consider using the available computational infrastructure to scale up your analysis capabilities. This may include applying for access to large computing cluster resources with e.g. {% tool "eurohpc"%} or making use of public Galaxy servers such as {% tool "galaxy-europe" %}.
- **Genomic analysis**: Including whole genome sequencing (WGS), this analysis allows the interpretation of genetic information encoded along the genome (DNA or RNA). Genomic analysis can be used for a wide range of applications to characterise many aspects of pathogen variability, such as Variants of Concern (VOC) and antimicrobial resistance profiles in bacteria (AMR). Examples of tools that allow us to take into account the genomic characteristics of pathogens (e.g. genomic structure and size, gene annotations, mobile genetic elements) are:
  - Sequence Alignment: {% tool "bowtie2" %}, {% tool "bwa" %} and {% tool "samtools" %}
  - Genome Assembly: {% tool "canu"%}, {% tool "velvet" %} and {% tool "spades" %}
  - Phylogenetic Analysis: {% tool "clustalw" %}, {% tool "muscle" %}, {% tool "mafft" %}, {% tool "raxml" %} and {% tool "iqtree" %}
  - Molecular Clock: {% tool "mrbayes" %}, {% tool "beast" %} and {% tool "beauti" %}
  - Variant calling: {% tool "dragen-gatk" %}, {% tool "freebayes" %} and {% tool "varscan" %}
  - Annotation: {% tool "annovar" %}, {% tool "snpeff" %}, {% tool "vep" %} and {% tool "dbnsfp" %}
  - All-in-one Bioinformatic Tools: {% tool "snippy" %}

- **Metagenomics analysis**: Sequencing all genetic material in a sample can provide comprehensive data about the composition of the microbial community. In the context of infectious diseases, it can aid in identifying multiple pathogens simultaneously in clinical, as well as environmental samples. Examples of tools in this type of analysis are:
  - 16S rRNA sequencing: {% tool "qiime2" %}
  - Shotgun sequencing: {% tool "spades" %}, and {% tool "megahit" %}
  - Assigning taxonomic labels: {% tool "kraken2" %}

- **Proteomics analysis**: Proteomics, primarily utilising mass spectrometry techniques, offers a powerful tools for examining proteins and their interplay. This can provide valuable insights into irregularities associated with infectious diseases and potentially uncover mechanisms of drug resistance. Examples of tools in this type of analysis are:
  - Mass Spectrometry Data Extraction Software: {% tool "readw" %}
  - Search Algorithms: {% tool "x-tandem" %}, {% tool "omssa" %} and {% tool "maxquant" %}
  - Statistical Validation: {% tool "peparml" %}
  - Quantitative Tools: {% tool "apex" %} and {% tool "maxquant" %}

- **Metabolomics analysis**: This involves measuring the levels of small molecules (metabolites) produced by specific pathogens in biological samples, comparing them across different conditions or groups of samples. Examples of tools in this type of analysis are:
  - Mass Spectrometry Software: {% tool "xcms" %} and {% tool "metaboanalyst" %}
  - NMR Spectroscopy Software: {% tool "chenomx" %}
  - Data Processing: {% tool "xcms" %}, {% tool "mzmine" %} and {% tool "openms" %}

## Postprocessing
In pathogen characterisation, the postprocessing steps are crucial to evaluate and interpret the results. These steps are important to identify strain relationships and specific molecular variation patterns linked to peculiar phenotypes of pathogens (e.g. drug resistance, virulence, and transmission rate). Such results must be biologically meaningful and reproducible, considering also the clinical aspects and treatment implications.

### Considerations

Some considerations about postprocessing steps in pathogen characterization include:
- **Interpretation**: it is important to interpret them in a biologically meaningful context. This should consider the following aspects: report the variability of specific pathogens; find out new strains that could become concerning; identify specific genes or mutations associated with pathogenic variation.
- **Transformation**: Consider having postprocessing steps to ensure that outputs are transformed or converted into interoperable and open formats. This ensures that subsequent pipelines and collaborators can readily make use of the results. 
- **Visualisation**: To allow a clear interpretation of the clinical practice, it is important to visualise the results clearly, to make the results clear also to all professionals involved.

### Existing approaches

- **Spatial-temporal analysis and visualisation**: using a combined approach of phylogenetic, spatial distribution, and molecular clock, this approach aids in designing strategies to control and prevent the spread of infectious diseases, as well as in the development of effective treatments, and vaccines.
  - Spatial distribution of strain: {% tool "nextstrain" %}
- **Drug resistance characterisation**: genomic analysis can be used to characterise pathogens for specific resistance against drugs and help develop strategies to fight the spread of drug-resistant strains.
  - Antimicrobial resistance (AMR): {% tool "resfinder" %} and {% tool "pathogenwatch" %}
  - Viral drug resistance: {% tool "hivdb-stanford" %} 
- **Interaction analysis and functional enrichment analysis**: placing the identified protein interactions and regulatory networks in the context of the affected biological pathways allows for a better understanding of disease mechanisms and potential drug targets.
  - Network analysis: {% tool "cytoscape" %} and {% tool "celldesigner" %}
  - Gene enrichment analysis: {% tool "enrichr" %}, {% tool "go" %} and {% tool "g-profiler" %}
  - Interaction Databases: {% tool "biogrid" %} and {% tool "intact" %}
  - Integrative diagrams:
    -  A [disease map](https://disease-maps.org/) can be used to represent a conceptual model of the molecular mechanisms of a disease. An example is the {% tool "covid19map" %}.

## Data analysis of wastewater surveillance for infectious diseases

Wastewater surveillance has emerged as a valuable tool for monitoring infectious diseases, providing a non-invasive method to track the spread of pathogens within communities. This approach has gained significant attention during the COVID-19 pandemic, particularly for detecting and analysing SARS-CoV-2 variants. By analysing wastewater samples, researchers can identify the presence and prevalence of infectious agents, offering insights into public health trends. Here we focus on the analysis of wastewater with an emphasis on SARS-CoV-2. 

### Considerations

Even though the considerations for this specific field are very similar to the ones described in the previous paragraphs, there are some approaches that are used in the context of wastewater surveillance.

### Existing approaches

Several tools and workflows have been developed or adapted for the analysis of wastewater data, especially in the context of SARS-CoV-2 surveillance:
 - **Specific Tools for SARS-CoV-2**: Certain tools (such as {% tool "freyja"%}, {% tool "cojac"%}, and {% tool "lineagespot" %}) are specifically designed for analysing SARS-CoV-2 data, providing capabilities such as variant detection and lineage tracking.
 - **Repurposed Tools**: Originally developed for other types of genomic data, tools like {% tool "kallisto" %} or {% tool "kraken2" %}, have been successfully applied to wastewater data analysis, offering high performance in read alignment and taxonomic classification.
- In addition, here are **several bioinformatics protocols and solutions** that could be used in the context of wastewater next-generation sequencing (NGS) data analysis.
  - {% tool "pigxs" %}: provides a comprehensive solution for sequencing and analysing SARS-CoV-2 in wastewater.
  - Detection of SARS-CoV-2 variants in Switzerland by genomic analysis of wastewater samples [medRxiv](https://www.medrxiv.org/content/10.1101/2021.01.08.21249379v2): COWWID: A GitHub repository from the CBG-ETHZ group offering tools for detecting SARS-CoV-2 variants in Switzerland
  - [CDC Module 2.7](https://www.cdc.gov/amd/training/covid-toolkit/module2-7.html): Wastewater based variant tracking for SARS-CoV-2
  - The Public Health Alliance for Genomic Epidemiology GitHub organization makes available a mapping to the {% tool "european-nucleotide-archive" %}: {% tool "sars-pha4ge" %}
  - {% tool "phes-odm" %} as an open data model for wastewater surveillance
  - Viral Lineage Quantification (VLQ), Kallisto-Approach: [Lineage abundance estimation for SARS-CoV-2 in wastewater using transcriptome quantification techniques](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-022-02805-9) and corresponding repository at {% tool "vlq" %}
  - [Performance benchmark of tools](https://peerj.com/articles/14596/), evaluating tools like Kraken2, Kallisto, Freyja, implemented in {% tool "c-wap" %} 
  - Wastewater quality control workflow in GalaxyTrakr [(SSquAWK4)](dx.doi.org/10.17504/protocols.io.kxygxzk5dv8j/v9). Further quality control aspects are discussed in the [Quality Control - Pathogen Characterisation page](/quality-control/pathogen-characterisation)
  - ECDC [Guidance document](https://www.ecdc.europa.eu/sites/default/files/documents/Guidance-for-representative-and-targeted-genomic-SARS-CoV-2-monitoring-updated-with%20erratum-20-May-2021.pdf) for representative and targeted genomic SARS-CoV-2 monitoring








