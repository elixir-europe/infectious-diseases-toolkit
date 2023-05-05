---
title: Data analysis
description: Analising Human biomolecular related data
contributors: [Aina Jené Cortada, Arnau Soler Costa]
page_id: hbd_data_analysis
rdmkit:
  - name: Human Data
    url: https://rdmkit.elixir-europe.org/human_data
  - name: Sensitive Data
    url: https://rdmkit.elixir-europe.org/sensitive_data
  - name: Biomolecular simulation data  
    url: https://rdmkit.elixir-europe.org/biomolecular_simulation_data
  - name: Data analysis
    url: https://rdmkit.elixir-europe.org/data_analysis
related_pages: 
  showcase: []
  human_biomolecular_data: [hbd_data_sources]
  human_clinical_and_health_data: [hchd_data_sources, hchd_data_analysis]
  socioeconomic_data: []
  pathogen_characterisation: []
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction

Data analysis, as in Human biomolecular data of infectious diseases, involves exploring collected data to gain an understanding of the messages within a dataset and identifying relationships between variables using mathematical formulas or models. The analysis phase workflow is iterative, with steps repeated several times to explore data and optimise the workflow. Depending on whether the data is quantitative or qualitative, different methods are used for data analysis. The data analysis phase follows the often-automated and batched data processing stage.

As data analysis generates new knowledge and information, it is a critical stage in the research process. To follow best practices for analysing human biomolecular data of infectious diseases, it is important to document all steps taken in the analysis workflow, including data preprocessing, statistical analysis, and the use of tools and algorithms. This documentation should be detailed enough to enable others to reproduce the analysis and results. Additionally, it is crucial to follow the FAIR principles (Findability, Accessibility, Interoperability, and Reusability) to ensure that the data, code, and results are easily discoverable, accessible, and reusable by other researchers.

When looking for more information [here](https://rdmkit.elixir-europe.org/analysing#what-should-be-considered-for-data-analysis).

### General considerations

Some considerations for analysing human biomolecular data of infectious diseases are:

- Select the tools best suited for the analysis of your data.
- Document the exact steps used for data analysis.
- Choose between several computing infrastructure types, e.g. cluster, cloud.
- Take into account the computing resources needed.
- Which type of data are you using, e.g. DNAseq, ATACseq, CNV.
- Integration of different types of data (e.g. RNAseq and DNAseq).
- Ensure access to the data and tools for all collaborators, for reproducibility.
    - Providing your code 
    - Providing your execution environment
    - Providing your workflows
    - Providing your data analysis execution

When looking for solutions to some of the considerations above, you can check [this](https://rdmkit.elixir-europe.org/data_analysis#what-are-the-best-practices-for-data-analysis) documentation.

### Existing approaches

Here you can find some more general existing approaches in order to help and improve the data analysis pipeline/protocol:

- **Container environments**: As an alternative to package management systems you can consider container environments like [Docker](https://www.docker.com/) or [Singularity](https://sylabs.io/).
- **Web-based platform**: Provides a centralised location for software developers to store, manage, collaborate, and share their code.- You can use [GitHub](https://github.com/) (widely used), [GitLab](https://about.gitlab.com/) or [Bitbucker](https://bitbucket.org/).
- **Workflow platforms**: Allows the user to manage your data and provide an interface (web, GUI, APIs) to run complex pipelines and review their results. For instance: [Galaxy](https://rdmkit.elixir-europe.org/galaxy_assembly) and [Arvados](https://arvados.org/) (CWL-based, open source).
- **Workflow runners**: Allows the user to take a workflow written in a proprietary or standardiSed format (such as the CWL standard) and execute it locally or on a remote computer infrastructure. For instance, [toil-cwl-runner](https://toil.readthedocs.io/en/latest/running/cwl.html), the reference CWL runner ([cwltool](https://pypi.org/project/cwltool/)), [Nextflow](https://www.nextflow.io/), [Snakemake](https://snakemake.readthedocs.io/en/stable/), [Cromwell](https://cromwell.readthedocs.io/en/stable/tutorials/FiveMinuteIntro/).
- **Integration Pipelines**: These pipelines are used to integrate different types of data, such as genomic, proteomic, and metabolomic data. It involves steps such as data preprocessing, data integration, and functional analysis. Tools like [OmicsIntegrator](https://github.com/fraenkel-lab/OmicsIntegrator) can be used for data integration.

## Preprocessing

Data preprocessing is the phase in the project where data is converted into a desired format and prepared for analysis. Is a crucial step in data analysis that involves cleaning, transforming, and preparing data for analysis. The goal of preprocessing is to ensure that the data is of high quality and is suitable for the intended analysis. Preprocessing can involve a range of steps, depending on the type of data and the analysis being performed. 

Preprocessing is a critical step in data analysis of HUman biomolecular data of infectious diseases because it can greatly impact the accuracy and reliability of the analysis results. By ensuring that the data is of high quality and suitable for analysis, preprocessing can help researchers obtain more accurate and meaningful insights from this data.

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

Preprocessing could be made using the state of art bioinformatics tools and/or programming languages that have different functions and packages to work and process this kind of data. For example, Python, RStudio or using Command-Line, are different approaches to enable the user performing all the necessary and wanted steps to do the desired preprocessing pipeline/protocol. 

When looking for quality control protocols, see [Human biomolecular data - Quality control](https://www.infectious-diseases-toolkit.org/human-biomolecular-data/quality-control) page.

## Analysis

The analysis of human biomolecular data involves the use of various techniques and approaches to extract meaningful information from biological samples such as DNA, RNA, proteins, and metabolites. 

### Existing approaches

There are several types of analysis that can be performed on human biomolecular data, depending on the specific research question and type of data being analysed. Here are some common types of analysis:

- **Gene expression analysis**: This involves measuring the expression levels of genes in a biological sample and comparing them across different conditions or groups of samples. This can be done using techniques such as microarray analysis or RNA sequencing. 
    - *Sequence alignment*: [STAR](https://github.com/alexdobin/STAR) and [HISAT2](https://github.com/DaehwanKimLab/hisat2)
    - *Gene expression analysis*: [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html) and [EdgeR](https://bioconductor.org/packages/release/bioc/html/edgeR.html)
- **Genomic analysis**: This involves the interpretation of genetic information encoded in DNA sequences. DNA data analysis can be used for a wide range of applications, such as identifying genetic variants associated with disease, studying the evolution of species, and understanding the molecular mechanisms underlying biological processes.
    - *Sequence alignment*: [Bowtie2](https://github.com/BenLangmead/bowtie2) and [BWA](https://github.com/lh3/bwa)
    - *Structural variant detection*: [Delly](https://github.com/dellytools/delly), [Lumpy](https://github.com/arq5x/lumpy-sv), [Manta](https://github.com/Illumina/manta) and [GRIDSS](https://github.com/PapenfussLab/gridss)
    - *Genome assembly*: [Canu](https://github.com/marbl/canu), [Flye](https://github.com/fenderglass/Flye), [wtdbg2](https://github.com/ruanjue/wtdbg2) and [SPAdes](https://github.com/ablab/spades)
    - *Phylogenetic analysis*: [ClustalW](https://github.com/coldfunction/CUDA-clustalW), [MUSCLE](https://github.com/rcedgar/muscle), [MAFFT](https://github.com/GSLBiotech/mafft) and [PhyML](https://github.com/stephaneguindon/phyml)
    - *Variant calling*: [Dragen-GATK](https://gatk.broadinstitute.org/hc/en-us/articles/360045944831), [DeepVariant](https://github.com/google/deepvariant), [FreeBayes](https://github.com/freebayes/freebayes) and [VarScan](https://github.com/dkoboldt/varscan)
    - *Annotation*: [ANNOVAR](https://github.com/WGLab/doc-ANNOVAR), [SnpEff](https://github.com/pcingola/SnpEff), [VEP](https://github.com/Ensembl/ensembl-vep) and [dbNSFP](https://github.com/shiquan/bcfanno/blob/master/Documentation/database/dbNSFP.md)
- **Epigenetic analysis**: This involves measuring changes in DNA methylation, histone modifications, or other epigenetic marks in different samples or conditions. This can help to understand how gene expression is regulated and identify potential biomarkers or therapeutic targets.
    - *DNA methylation analysis*: [Bismark](https://github.com/FelixKrueger/Bismark), [MethylKit](https://github.com/al2na/methylKit) and [methylPipe](https://bioconductor.riken.jp/packages/3.1/bioc/html/methylPipe.html)
    - *Histone modification analysis*: [MACS](https://github.com/macs3-project/MACS) and [SICER2](https://github.com/zanglab/SICER2)
- **Protein-protein interaction analysis**: This involves identifying proteins that interact with each other and exploring the functional consequences of these interactions. This can help to identify new targets for drug development and understand disease mechanisms.
    - *Interaction databases*: [BioGRID](https://github.com/BioGRID) and [IntAct](https://github.com/intact-portal)
    - *Network analysis*: [Cytoscape](https://apps.cytoscape.org/) and [GeneMANIA](https://github.com/GeneMANIA/genemania)
- **Metabolomics analysis**: This involves measuring the levels of small molecules (metabolites) in biological samples and comparing them across different conditions or groups of samples. This can help to identify biomarkers of disease or drug response.
    - *Data processing*: [XCMS](https://xcmsonline.scripps.edu/landing_page.php?pgcontent=mainPage), [MZmine](http://mzmine.github.io/) and [OpenMS](https://github.com/OpenMS/OpenMS)
    - *Statistical analysis*: [MetaboAnalyst](https://www.metaboanalyst.ca/) and [MetSign](https://pubmed.ncbi.nlm.nih.gov/21932828/)

## Postprocessing

The postprocessing part refers to the steps taken after the initial analysis to refine and interpret the results. Post-processing steps are important because they can help to identify biological patterns and relationships that were not apparent in the initial analysis, and to ensure that the results are biologically meaningful and reproducible.

### Considerations

Some considerations to take into account when performing postprocessing on human biomolecular data include:

- **Interpretation**: Once the results have been generated, it is important to interpret them in a biologically meaningful context. This can include identifying enriched pathways or gene sets, performing network analysis, or annotating the results.
- **Visualisation**: It is important to visualise the results in a clear and informative way. This can help to identify patterns and relationships in the data, and to communicate the results to others in a clear and accessible way.

### Existing approaches

- **Functional Enrichment Analysis**: These analyses are used to identify enriched pathways and biological functions associated with differentially expressed biomolecules. It involves steps such as gene ontology analysis, pathway analysis, and network analysis. Tools like [GSEA](https://www.gsea-msigdb.org/gsea/index.jsp), [GO](http://geneontology.org/docs/go-enrichment-analysis/), [KEGG](https://www.bioconductor.org/packages//2.11/data/annotation/html/KEGG.db.html), [DAVID](https://david.ncifcrf.gov/) and [Enrichr](https://github.com/guokai8/EnrichR) can be used for functional enrichment analysis and/or also annotate the results.

- **Visualisation**:
    - Generate plots and heatmaps using tools such as [ggplot2](https://github.com/tidyverse/ggplot2) or [matplotlib](https://github.com/matplotlib/matplotlib)
    - Visualise data in a genomic context using tools such as [IGV](https://software.broadinstitute.org/software/igv/) or [UCSC Genome Browser](https://genome.ucsc.edu/)

All these workflows and tools can be adapted and customised based on the specific type of data being analysed and the research question being addressed.
