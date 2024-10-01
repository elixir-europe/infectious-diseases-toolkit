---
title: Human biomolecular data
description: Analysing Human biomolecular related data.
contributors: [Aina Jené Cortada, Arnau Soler Costa]
page_id: hbd_data_analysis
redirect_from: /human-biomolecular-data/data-analysis
rdmkit:
  - name: Human Data
    url: https://rdmkit.elixir-europe.org/human_data
  - name: Sensitive Data
    url: https://rdmkit.elixir-europe.org/sensitive_data
  - name: Biomolecular simulation data  
    url: https://rdmkit.elixir-europe.org/biomolecular_simulation_data
  - name: Data analysis
    url: https://rdmkit.elixir-europe.org/data_analysis
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction

Data analysis, as in Human biomolecular data of infectious diseases, involves exploring the data collected to gain an understanding of the messages within a dataset and identifying relationships between variables using mathematical formulas or models. Moreover, it is always crucial to follow the best practices and especially the FAIR principles (Findability, Accessibility, Interoperability, and Reusability) to  enable the collection and flow of information in the best way possible.

### General considerations

Some considerations for analysing human biomolecular data of infectious diseases are:

- Select the tools best suited for the analysis of your data.
- Document the exact steps used for data analysis.
- Choose between several computing infrastructure types, e.g. cluster, cloud.
- Take into account the computing resources needed.
- Which type of data are you using, e.g. DNAseq, ATACseq, CNV.
- Integration of different types of data (e.g. RNAseq and DNAseq).
- Ensure following the FAIR principles.
- Guarantee access to the data and tools for all collaborators, for reproducibility.
    - Providing your code 
    - Providing your execution environment
    - Providing your workflows
    - Providing your data analysis execution

When looking for solutions to some of the considerations above, you may have a look at the information available on the [RDMkit website](https://rdmkit.elixir-europe.org/data_analysis#what-are-the-best-practices-for-data-analysis).

### Existing approaches

Below you can find some general existing approaches in order to help with and improve your data analysis pipeline/protocol:

- **Container environments**: As an alternative to package management systems you can consider container environments like {% tool "docker" %} or {% tool "singularity" %}.
- **Web-based platform**: Provides a centralised location for software developers to store, manage, collaborate, and share their code. You can use {% tool "github" %} (widely used), {% tool "gitlab" %} or {% tool "bitbucket" %}.
- **Workflow platforms**: Allows the user to manage your data and provide an interface (web, GUI, APIs) to run complex pipelines and review their results. For instance: {% tool "galaxy" %} and {% tool "arvados" %} (CWL-based, open source).
- **Workflow runners**: Allows you to take a workflow written in a proprietary or standardised format (such as the CWL standard) and execute it locally or on a remote computer infrastructure. For instance, {% tool "toil-cwl-runner" %}, the reference CWL runner ({% tool "cwltool" %}), {% tool "nextflow" %}, {% tool "snakemake" %}, {% tool "cromwell" %}.
- **Integration Pipelines**: These pipelines are used to integrate different types of data, such as genomic, proteomic, and metabolomic data. It involves steps such as data preprocessing, data integration, and functional analysis. Tools like {% tool "omicsgenerator" %} can be used for data integration.

## Preprocessing

Data preprocessing is the phase in the project where data is converted into a desired format and prepared for analysis. Is a crucial step in data analysis that involves cleaning, transforming, and preparing data for analysis. The goal of preprocessing is to ensure that the data is of high quality and is suitable for the intended analysis. Preprocessing can involve a range of steps, depending on the type of data and the analysis being performed. 

Preprocessing is a critical step in data analysis of Human biomolecular data of infectious diseases because it can greatly impact the accuracy and reliability of the analysis results. By ensuring that the data is of high quality and suitable for analysis, preprocessing can help researchers obtain more accurate and meaningful insights from this data.

### Considerations

Here are some common considerations involved in data preprocessing:

- **Data cleaning**: This step involves identifying and correcting errors or inconsistencies in the data. Examples of data cleaning include removing duplicates, correcting typos or misspellings, and identifying and handling missing data.
- **Data transformation**: This step involves transforming the data to make it suitable for analysis. Examples of data transformation include converting data types (e.g., from categorical to numerical), scaling data, and normalising data.
- **Remove low-quality samples**: Samples that have low sequencing depth, high number of missing values, or poor alignment quality can be removed from the dataset to ensure that the remaining samples are of high quality.
- **Identify and remove outliers**: Outliers are data points that fall outside the expected range of values and can skew the analysis results. Outliers can be identified using statistical methods and removed from the dataset.
- **Check for batch effects**: Batch effects are systematic differences in the data that arise from technical or experimental factors. Batch effects can be identified using statistical methods and removed from the dataset.
- **Data normalisation**: Normalisation is a common preprocessing step that aims to remove systematic biases in the data. Normalisation methods should be evaluated to ensure that they are effective and do not introduce additional biases.
- **Perform quality control checks at each preprocessing step**: Quality control checks should be performed at each preprocessing step to ensure that the data is of high quality and suitable for the intended analysis. 

### Existing approaches

Preprocessing could be done using the state of art bioinformatics tools and/or programming languages that have different functions and packages to work and process this kind of data. For example, Python, RStudio or using Command-Line, are different approaches to enable the user performing all the necessary and wanted steps to do the desired preprocessing pipeline/protocol. 

When looking for quality control protocols, see [Quality control - Human biomolecular data ](/quality-control/human-biomolecular-data) page.

## Analysis

The analysis of human biomolecular data involves the use of various techniques and approaches to extract meaningful information from biological samples such as DNA, RNA, proteins, and metabolites. 

This stage relies on the previous stages (collection, processing) that will lay the foundations for the generation of new knowledge by providing accurate and trustworthy data.

### Considerations

- **The location of your data**: Proximity to computing resources is crucial due to its impact on data transfer across infrastructures. It is worthwhile to compare the cost of transferring large data volumes versus the transfer of virtual machine images for analysis purposes.
- **Analysis of the data**: Prior to analyzing the data, it is necessary to evaluate the computing environment and make a decision among various types of computing infrastructures, such as clusters or clouds. Additionally, selecting the suitable work environment, such as command line or web portal, based on individual requirements and expertise, is crucial.
- **Best tools**: You need to select the tools best suited for the analysis of your data.
- **Document the steps**: Accurate documentation of the data analysis process is essential, encompassing the precise steps taken, software versions employed, parameters utilized, and the computing environment employed. However, it is important to mention that the "manual" manipulation of the data can potentially complicate this documentation procedure.
- **Collaborative analysis**: When engaging in collaborative data analysis, it is crucial to ensure that all collaborators have access to the data and tools required. This can be facilitated by establishing virtual research environments that provide a shared platform for seamless collaboration.
  
### Existing approaches

There are several types of analysis that can be performed on human biomolecular data, depending on the specific research question and type of data being analysed. Here are some common types of analysis:

- **Gene expression analysis**: This involves measuring the expression levels of genes in a biological sample and comparing them across different conditions or groups of samples. This can be done using techniques such as microarray analysis or RNA sequencing. 
    - *Sequence alignment*: {% tool "star" %} and {% tool "hisat2" %}
    - *Gene expression analysis*: {% tool "deseq2" %} and {% tool "edger" %}
- **Genomic analysis**: This involves the interpretation of genetic information encoded in DNA sequences. DNA data analysis can be used for a wide range of applications, such as identifying genetic variants associated with disease, studying the evolution of species, and understanding the molecular mechanisms underlying biological processes.
    - *Sequence alignment*: {% tool "bowtie2" %} and {% tool "bwa" %}
    - *Structural variant detection*: {% tool "delly" %}, {% tool "lumpy" %}, {% tool "manta" %} and {% tool "gridss" %}
    - *Genome assembly*: {% tool "canu" %}, {% tool "flye" %}, {% tool "wtdbg2" %} and {% tool "spades" %}
    - *Phylogenetic analysis*: {% tool "clustalw" %}, {% tool "muscle" %}, {% tool "mafft" %} and {% tool "phyml" %}
    - *Variant calling*: {% tool "dragen-gatk" %}, {% tool "deepvariant" %}, {% tool "freebayes" %} and {% tool "varscan" %}
    - *Annotation*: {% tool "annovar" %}, {% tool "snpeff" %}, {% tool "vep" %} and {% tool "dbnsfp" %}
- **Epigenetic analysis**: This involves measuring changes in DNA methylation, histone modifications, or other epigenetic marks in different samples or conditions. This can help to understand how gene expression is regulated and identify potential biomarkers or therapeutic targets.
    - *DNA methylation analysis*: {% tool "bismark" %}, {% tool "methylkit" %} and {% tool "methylpipe" %}
    - *Histone modification analysis*: {% tool "macs" %} and {% tool "sicer2" %}
- **Protein-protein interaction analysis**: This involves identifying proteins that interact with each other and exploring the functional consequences of these interactions. This can help to identify new targets for drug development and understand disease mechanisms.
    - *Interaction databases*: {% tool "biogrid" %} and {% tool "intact" %}
    - *Network analysis*: {% tool "cytoscape" %} and {% tool "genemania" %}
- **Metabolomics analysis**: This involves measuring the levels of small molecules (metabolites) in biological samples and comparing them across different conditions or groups of samples. This can help to identify biomarkers of disease or drug response.
    - *Data processing*: {% tool "xcms-online" %}, {% tool "mzmine" %} and {% tool "openms" %}
    - *Statistical analysis*: {% tool "metaboanalyst" %} and {% tool "metsign" %}

## Postprocessing

The postprocessing part refers to the steps taken after the initial analysis to refine and interpret the results. Postprocessing steps are important because they can help to identify biological patterns and relationships that were not apparent in the initial analysis, and to ensure that the results are biologically meaningful and reproducible.

### Considerations

Some considerations to take into account when performing postprocessing on human biomolecular data include:

- **Interpretation**: Once the results have been generated, it is important to interpret them in a biologically meaningful context. This can include identifying enriched pathways or gene sets, performing network analysis, or annotating the results.
- **Visualisation**: It is important to visualise the results in a clear and informative way. This can help to identify patterns and relationships in the data, and to communicate the results to others in a clear and accessible way.

### Existing approaches

- **Functional Enrichment Analysis**: These analyses are used to identify enriched pathways and biological functions associated with differentially expressed biomolecules. It involves steps such as gene ontology analysis, pathway analysis, and network analysis. Tools like {% tool "gsea" %}, {% tool "go" %}, {% tool "kegg" %}, {% tool "david" %} and {% tool "cytoscape" %} can be used for functional enrichment analysis and/or also annotate the results.

- **Visualisation**:
    - Generate plots and heatmaps using tools such as {% tool "ggplot2" %} or {% tool "matplotlib" %}
    - Visualise data in a genomic context using tools such as {% tool "igv" %} or {% tool "ucsc-genome-browser" %}

All these workflows and tools can be adapted and customised based on the specific type of data being analysed and the research question being addressed.
