---
title: Pathogen characterisation
description: Analysing Pathogen related data.
contributors: [Eva Garcia Alvarez, Francesco Messina, Fotis Psomopoulos, Rafael Andrade Buono, Romain David, Andreas Scherer, Isabel Cuesta, Sarai Varona, Emilia Arjona, Juan Ledesma, Pablo Mata, Daniel Valle, Jaime Ozáez]
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

### General Considerations

Some typical considerations involved in this step:

- **Data cleaning**: Finds and corrects errors in the data. For example,  eliminating duplicates, removing too short genomic reads, and trimming not useful information such as contaminating host data.
- **Quality control checks**: Should be conducted at each step to ensure that the data is suitable for the intended analysis.     	
- **Exclusion of low-quality samples**: Samples with low-quality scores should be marked and removed. In genomics studies, samples with missing values, low sequencing depth, and contaminations might be removed.   
- **Host read removal**: Depending of the sample type, the host and the analysis to be performed, it is strongly recommended removing reads from the host that can affect the analysis  
- **Origin of the reads**:
  - _Short reads or long reads_:  Short reads, generated by platforms like Illumina, offer high accuracy with low error rates but can be challenging for assembling repetitive regions. Long reads, produced by technologies such as Oxford Nanopore or PacBio, enable more comprehensive genome assemblies and structural variant detection, though they may have higher error rates.
  - _Sequencing platform_: Different platforms vary in read quality, length, and throughput. For example, Illumina MiSeq may experience a significant decrease in R2 read quality when performing 300-cycle paired-end sequencing.
  - _Enrichment of the library_: Depending on the study’s objective, different enrichment methods can be used, such as PCR amplification with specific primers (amplicon sequencing), probe-based hybridization capture (target enrichment), or amplification-free sequencing. Some enrichment methods may present specific quality issues that need to be addressed.
  - _fast5 or fastq files_: ONT sequencing data can be stored in different formats, each requiring specific software for analysis

### Existing approaches

Preprocessing steps may depend on the technology used and the pathogen being studied and thus should be adjusted accordingly. Some common approaches in genomics studies include:

- Short reads:
  - Raw sequences quality check: {% tool "fastqc" %}
  - Trimming out adapters and low-quality sequences: {% tool "trimmomatic" %}, {% tool "fastp" %}, {% tool "cutadapt" %}, {% tool "SOAPnuke" %}
- Long reads:
  - basecalling softwares: {% tool "guppy" %}, {% tool "dorado" %}
  - Raw sequences quality check: {% tool "nanoplot" %}, {% tool "nanoq" %}, {% tool "pycoqc" %}, {% tool "longqc" %}, {% tool "minionqc" %}
  - Trimming out adapters and low-quality sequences: {% tool "porechop" %}, {% tool "nanofilt" %}
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
  - Short reads:
    - All-in-one Bioinformatic Tools: {% tool "snippy" %}, {% tool "dragen-gatk" %}
    - Sequence Alignment: {% tool "bowtie2" %}, {% tool "bwa" %} and {% tool "samtools" %}
    - Genome Assembly: {% tool "canu"%}, {% tool "velvet" %} and {% tool "spades" %}
    - Phylogenetic Analysis: {% tool "clustalw" %}, {% tool "muscle" %}, {% tool "mafft" %}, {% tool "raxml" %}, {% tool "fasttree" %} and {% tool "iqtree" %}
    - Molecular Clock: {% tool "mrbayes" %}, {% tool "beast" %} and {% tool "beauti" %}
    - Variant calling: {% tool "dragen-gatk" %}, {% tool "freebayes" %}, {% tool "bcftools" %} and {% tool "ivar" %}
    - Varoant annotation: {% tool "annovar" %}, {% tool "snpeff" %}, {% tool "vep" %} and {% tool "dbnsfp" %}
    - Genome annotation: {% tool "prokka" %}, {% tool "bakta" %} or {% tool "dfast" %}
    - Consensus genome generation: {% tool "bcftools" %}, {% tool "samtools" %}
  - Long reads:
    - All-in-one Bioinformatic Tools: {% tool "artic" %}
    - Sequence Alignment: {% tool "minimap2" %}  
    - Genome Assembly: {% tool "canu" %}, {% tool "flye" %}, {% tool "raven" %}, {% tool "miniasm" %}, {% tool "dragonflye" %}  
    - Assembly Polishing: {% tool "racon" %}  
    - Phylogenetic Analysis: {% tool "clustalw" %}, {% tool "muscle" %}, {% tool "mafft" %}, {% tool "raxml" %}, {% tool "fasttree" %}, {% tool "iqtree" %}  
    - Molecular Clock: {% tool "mrbayes" %}, {% tool "beast" %} and {% tool "beauti" %}
    - Variant Calling: {% tool "medaka" %}, {% tool "nanopolish" %}, {% tool "nanocaller" %}  
    - Variant Annotation: {% tool "snpeff" %}  
    - Genome annotation: {% tool "prokka" %}, {% tool "bakta" %} or {% tool "dfast" %}
  - Hybrid:  
    - Genome Assembly: {% tool "dragonFlye" %}, {% tool "unicycler" %}  
    - Polishing: {% tool "pilon" %}, {% tool "polypolish" %}

- **Expression analysis** (fungal genomes):
  - Sequence Alignment: {% tool "star" %}, {% tool "hisat2" %}, {% tool "kallisto" %}  
  - Quantification: {% tool "salmon" %}, {% tool "rsem" %}  
  - Removal of ribosomal RNA: {% tool "sortmerna" %}  
  - Differential expression analysis: {% tool "deseq2" %}

- **Metagenomics analysis**: Sequencing all genetic material in a sample can provide comprehensive data about the composition of the microbial community. In the context of infectious diseases, it can aid in identifying multiple pathogens simultaneously in clinical, as well as environmental samples. Examples of tools in this type of analysis are:
  - 16S rRNA sequencing: {% tool "qiime2" %}
  - Shotgun sequencing: {% tool "spades" %}, and {% tool "megahit" %}
- Assigning taxonomic labels: {% tool "kraken2" %}, {% tool "kaiju" %}, {% tool "diamond" %}, {% tool "megan" %}, {% tool "metaphlan" %}, {% tool "centrifuge" %}, {% tool "motus" %}, {% tool "krakenuniq" %}, {% tool "kmcp" %}, {% tool "ganon" %}, {% tool "clark" %}

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
- **Quality metrics**: It is important to obtain different quality metrics to evaluate the accuracy or quality of the data generated during the analysis. Depending on the analysis performed, the metrics and tools may vary significantly.

### Existing approaches

- **Spatial-temporal analysis and visualisation**: using a combined approach of phylogenetic, spatial distribution, and molecular clock, this approach aids in designing strategies to control and prevent the spread of infectious diseases, as well as in the development of effective treatments, and vaccines.
  - Spatial distribution of strain: {% tool "nextstrain" %}
- **Lineage, subtyping or clade assignment**: {% tool "pangolin" %}, {% tool "nextclade" %}, {% tool "irma" %}, {% tool "fluserver" %}, {% tool "genome-detective" %}, {% tool "hcv-glue" %}
- **Drug resistance and virulence factor characterisation**: genomic analysis can be used to characterise pathogens for specific resistance against drugs and help develop strategies to fight the spread of drug-resistant strains.
  - Antimicrobial resistance (AMR) and virulence factors: {% tool "resfinder" %}, {% tool "amrfinderplus" %}, {% tool "ariba" %}, {% tool "abricate" %} and {% tool "pathogenwatch" %}
  - Viral drug resistance: {% tool "hivdb-stanford" %} and {% tool "fluserver" %}
  - Hepatitis C and B resistance profilers: Geno2pheno, {% tool "hcv-glue" %}
- **Interaction analysis and functional enrichment analysis**: placing the identified protein interactions and regulatory networks in the context of the affected biological pathways allows for a better understanding of disease mechanisms and potential drug targets.
  - Network analysis: {% tool "cytoscape" %} and {% tool "celldesigner" %}
  - Gene enrichment analysis: {% tool "enrichr" %}, {% tool "go" %} and {% tool "g-profiler" %}
  - Interaction Databases: {% tool "biogrid" %} and {% tool "intact" %}
  - Integrative diagrams:
    - A [disease map](https://disease-maps.org/) can be used to represent a conceptual model of the molecular mechanisms of a disease. An example is the {% tool "covid19map" %}.
- **Analysis metrics**:
  - Genome alignment metrics: {% tool "samtools" %}, {% tool "picard" %}
  - _de novo_  assembly metrics: {% tool "quast" %}
  - Expression analysis quality metrics: {% tool "rseqc" %}, {% tool "qualimap" %}, {% tool "dupradar" %}, {% tool "preseq" %}
- **General results aggregation**:
  - General metrics: {% tool "multiqc" %}
  - Antibiotic Resistance Genes: {% tool "hamronization" %}

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

## Data analysis of bacterial outbreaks

### General considerations

An outbreak in infectious diseases is defined as the increase in the number of cases of a disease above what is typically expected in a specific area or among a particular population over a certain period of time. Outbreak can occur in localized regions, such as a community, or they can spread across wider areas. They can involve new infectious or re-emergence of previously controlled diseases. Common examples include outbreaks of Influenza, SARS-CoV2, or Foodborne illnesses like caused by Listeria monocytogenes among others.

In order to know if an outbreak is caused by the same pathogen, it is necessary to isolate and characterize the pathogen using  phenotypic or genotypic techniques, which is known as a typification process or Microbial typing. It is used to differentiate between strains or species of microorganisms for various purposes, such as epidemiological studies, infection tracking, and outbreak investigations to pinpoint the source of foodborne outbreaks. It can also be used to identify which microorganisms are most virulent and cause serious diseases, resistant to antimicrobial drugs, or able to survive and multiply.

Techniques for microbial typing include traditional methods, like serotyping, fragment based methods and sequence based methods.

The gold standard for bacterial typing is pulsed-field gel electrophoresis (PFGE) and has been widely used for tacking outbreaks of foodborne pathogens, such as E.coli and Salmonella. However, technologies like Whole Genome Sequencing (WGS) have replaced PFGE due to their higher precision and resolution.

Different levels of sequence information can be associated with different  taxonomic levels. A single locus (i.e. 16S rRNA) is enough to distinguish from phylum to genus and, in some cases, species, while subspeciation requires incorporating  more genes, such as the 7 from MLST or the 53 loci from ribosomal MLST. The highest resolution power comes from incorporating the whole genome sequencing (WGS).

One of the significant advantages of whole genome sequencing (WGS) is its application in comparative genomics, enabling the determination of the phylogenetic relationships among a group of bacterial strains. There are several methods to assess the similarity between different genomes (i.e. gen-by-gen approaches: Multi-Locus Sequence Typing -wgMLST, Core Genome Multi-Locus Sequence Typing -cgMLST, or Single Nucleotide Polymorphisms -SNPs approach).

wgMLST analyzes the entire genome, considering all the genes present in the genome. This method allows for a comprehensive understanding of the genetic variation within and between species.

cgMLST focuses specifically on the set of genes that are present in all strains of a species, the core genome. This excludes accessory genes, genes not necessary for organism survival or reproduction under standard conditions, (i.e. virulence genes) that may vary among strains.

### Existing approaches

There are different tools available for bacterial outbreak analysis. Here they are classified based on the stage of the analysis.

- Starting with sequencing reads .fastq files:
  - **Pre-processing**: During this step we aim to obtain a set of good quality reads that can be used for further analysis. We will inspect the quality of the raw reads, discard all the reads that don’t meet the quality standards and remove adapters, primers or unwanted sequences that may interfere with later steps of the analysis. Tools: {% tool "fastqc" %}, {% tool "fastp" %}
  - **Bacterial genome identification**: Identifying the organisms that are present in our samples is crucial. Even though the microbiology lab could’ve sent information about the organisms present in the samples, there could be contaminations that would lead to mapping, variant calling and annotation errors. Tools: {% tool "kmerfinder" %}
  - **De-novo assembly**: If we want to make an in-depth analysis of the samples, we cannot work with a mess of unordered pieces of DNA. The reads can be aligned and merged (assembled) into a single sequence which we will use as a representation of the original DNA from the organism in the sample. Tools:  {% tool "unicycler" %}
- Once we have the assembly or reconstructed DNA strand, we can proceed with further analysis:
  - **Genomic features annotation**: Using the assembled sequence, the aim of this step is to automatically detect genes or subproducts of genes that may have functional properties in a non-specific way. These features can be relevant to characterize the organism in our samples as they may include strain-specific genes. Tools: {% tool "prokka" %}, {% tool "bakta" %}, {% tool "dfast" %}
  - **AMR/virulence characterization**: Contrary to the previous step, here the aim to do a specific search for relevant genes, including virulence factors and antibiotic-resistance genes. The main difference is that the search is performed within domain-specific databases:
    - Tools: {% tool "ariba" %}, {% tool "amrfinderPlus" %}  
    - Databases: [VFDB for virulence factors](http://www.mgc.ac.cn/VFs/), [CARD for antibiotic resistance genes](https://card.mcmaster.ca/), [NCBI RefGene Pathogen Database: VF and AMR](https://www.ncbi.nlm.nih.gov/pathogens/refgene/)
  - **Plasmid identification**: Sometimes the previously mentioned genes are found inside plasmids, which might restrain the previous tools from finding them. Not only that, but plasmids are quite relevant as they can be the source of horizontal gene transfer. These tools are used to find and characterize these plasmids: {% tool "ariba" %}, {% tool "plasmidid" %}
  - **MLST characterization**: MLST (Multi-Locus Sequence Typing) is an unambiguous procedure for characterizing isolates of bacterial species using the sequences of internal fragments of (usually) seven housekeeping genes. The aim is to obtain a profile based on the alleles for each gene, which can be used to establish relationships between the samples and the possible source of the outbreak. Tools: {% tool "ariba" %} used along with the [PubMLST database](https://pubmlst.org/).
    - Note: Different species may have different MLST schemes, so it is crucial to use the appropriate schema for each one.
  - **SNP calling and Core-SNPs matrix**: To find relationships between the samples and a possible source, phylogenetic distance can be a good measure. This distance is calculated by counting all the different pairwise SNP positions among samples. However, since the number of SNPs increases exponentially with the number of samples, a good approach is to use only the SNPs that are common to all samples (Core SNPs). These values are represented in a distance matrix, which is then used to create a phylogenetic tree. Tools: {% tool "snippy" %}
  - **Phylogenetic tree**: Using the previously obtained distance matrix, it is possible to create a phylogenetic tree, which is a visual representation of the genetic relationships between the samples, based on clustering algorithms. This is useful to group similar samples together and infer potential outbreak sources.  
    Tools: {% tool "iqtree" %}
  - **wgMLST and cgMLST**: These are both gene-by-gene approaches. Genome assembly data is aligned to a scheme consisting of a set of loci and their corresponding allele sequences to perform allele calling. Each isolate is then characterized by its allele profile, and comparing multiple samples generates an allele distance matrix. Tools: {% tool "chewbbaca" %}
    - Schema resources:  
      - [Ridom schemas](https://www.cgmlst.org/ncs/)
      - [Chewbbaca's schemas](https://chewbbaca.online/stats)
      - [PubMLST](https://pubmlst.org/)
      - [Enterobase](https://enterobase.warwick.ac.uk/)
  - **Pathogen-specific typing tools**: MLST is not always enough to characterize a certain species. Some species have their unique typing methods. Here are species-specific tools:  
    - _Escherichia / Shigella_: {% tool "ectyper" %}, {% tool "shigatyper" %} or {% tool "shigeifinder" %}
    - _Haemophilus_: {% tool "hicap" %} or {% tool "ssuissero" %}
    - _Klebsiella_: {% tool "kleborate" %}
    - _Legionella_: {% tool "legsta" %}
    - _Listeria_: {% tool "lissero" %}
    - _Mycobacterium_: {% tool "tbprofiler" %} and {% tool "mtbseq" %}
    - _Neisseria_: {% tool "meningotype" %} or {% tool "ngmaster" %}
    - _Pseudomonas_: {% tool "pasty" %}
    - _Salmonella_: {% tool "seqsero" %} and {% tool "sistr" %}
    - _Staphylococcus_: {% tool "agrvate" %}, {% tool "spatyper" %} and {% tool "sccmec" %}
    - _Streptococcus_: {% tool "emmtyper" %}, {% tool "pbptyper" %} or {% tool "ssuissero" %}  
    - Source: [Bactopia Merlin](https://bactopia.github.io/v3.0.0/bactopia/merlin/)

- Available pipelines: These pipelines synthesize some of the previous steps into a single workflow, making bioinformatics analysis easier:
  - **Bacterial assembly and annotation (short reads, long reads, hybrid):**  
    - [nf-core/bacass](https://nf-co.re/bacass/)
  - **Screening of functional genes:**  
    - [nf-core/funcscan](https://nf-co.re/funcscan/)
  - **Taxonomy classification (short and long metagenomic reads):**  
    - [nf-core/taxprofiler](https://nf-co.re/taxprofiler/)
  - **Complete analysis of bacterial genomes:**  
    - [Bactopia](https://bactopia.github.io/latest/)

## Viral outbreak

### General considerations

Analysis of outbreaks when a virus is suspected to be the responsible for constitutes an important tool for disease control.

A proper identification of the virus is needed to find whether there are already measures described for its prevention and contention so that the spread of the infection can be managed in order to avoid new potential cases.  In certain scenarios, molecular diagnostic methods, such as PCR, do not achieve the viral identification and the application of other protocols, such as deep sequencing (i.e. metagenomics) is needed to correctly identify the pathogen.

Further analyses that can be performed are phylogenetic analysis and genome characterisation The former is useful to identify the links between different samples from the same outbreak and track the spread of the infection as well as locate its potential origin, in case additional control measures are needed. The latter is based on genome analysis in order to find specific biological characteristics of that virus that can help to identify potential effective treatments or the application of more extreme control measures (i.e. mutations related to antiviral resistance or high pathogenicity).

### Existing approaches

There are different tools available for bacterial outbreak analysis. Here they are classified based on the stage of the analysis.

- **Pre-processing**: Data preprocessing is a crucial initial step prior to data analysis that involves reads quality check, low-quality cleaning and trimming, removal of adapters, primers or unwanted sequences from raw sequencing reads. Some of the tools to perform this process are:  
  - Short-reads: {% tool "fastqc" %}, {% tool "fastp" %}, {% tool "cutadapt" %} or {% tool "ivar" %}
  - Long-reads: {% tool "nanoplot" %} and {% tool "nanofilt" %}  
- **Viral species identification**: Accurately identifying the viral species present in samples is essential for responding to viral outbreaks, especially when the causative agent is unknown. This step involves classifying the sample's reads into various viral taxonomic species, using tools such as: {% tool "kraken2" %} / {% tool "krona" %} or {% tool "diamond" %} / {% tool "megan" %}  
- **Reference-genome mapping**: This approach is particularly useful when the viral species causing the outbreak is known, a reference genome is available, and the viral genome does not exhibit significant variability. It involves aligning sequencing reads to the reference genome, which is a crucial step for accurate variant calling and in-depth genetic analysis. Widely used tools are:
  - Short-reads: {% tool "bowtie2" %} and {% tool "bwa" %}  
  - Long-reads: {% tool "minimap2" %}  
- **Variant calling**: This step involves identifying genetic variations, such as single nucleotide polymorphisms (SNPs), insertions, deletions, and structural variants within a sample by comparing its sequencing data to a reference genome. Some useful tools are: {% tool "ivar" %}, {% tool "bcftools" %} and {% tool "lofreq" %}
- **Variant annotation**: Variant annotation is a step following variant calling that involves assigning biological and clinical significance to identified genetic variants. This step typically involves mapping variants to genes, determining their potential impact on protein function, and assessing their association with known phenotypes, diseases, or traits. Available tools are: {% tool "snpeff" %} and {% tool "snpsift" %}  
- **Consensus genome reconstruction**: Once we know the differences (variants) between the sample and the reference genome, we can change the positions in the reference genome to obtain a consensus genome `.fasta` file that can serve as the sample's assembled genome. Tools: {% tool "bcftools" %}  
- **_de novo_ assembly**: When the viral reference genome is not known or is highly variable, _de novo_  assembly is a better approach than reference genome mapping. _de novo_ assembly reconstructs a viral genome’s reads without the need of a reference genome into longer contiguous sequences (contigs) and scaffolds. These can be compared to a database (using any of the tools for taxonomic classification mentioned above) to identify the pathogen. Some of the widely used tools are:  
  - Short-reads: {% tool "spades" %} and {% tool "unicycler" %}
  - Long-reads: {% tool "canu" %}, {% tool "flye" %}, {% tool "raven" %}, {% tool "miniasm" %} and {% tool "dragonflye" %}
  - Hybrid: {% tool "dragonflye" %} and {% tool "unicycler" %}
- **Phylogeny**: In the context of addressing a viral outbreak, phylogenetic studies can help in tracing the origins and transmission pathways of the infection. Generating phylogenetic trees visually represents the connections between organisms, illustrating how they have diverged over time. The process of performing phylogenetic analysis involves several steps:  
  - Sequence alignment of the generated genomes. Tools: {% tool "mafft" %}, {% tool "muscle" %} or {% tool "clustalw" %}
  - Core genome SNPs: The core genome consists of the genes that are shared among all the samples/strains in the analysis, providing a stable genetic framework for comparative analysis. Tools: {% tool "snippy" %}  
  - Phylogenetic trees: With the multiple sequence alignment or the core SNPs, researchers can perform phylogenetic analysis. The choice of algorithm and evolutionary model will influence the results, with commonly used tools including: {% tool "iqtree" %} and {% tool "nextstrain" %}  
- **Lineage/clade/type**: When the virus causing the outbreak has been typed with different lineages, clades, or types/subtypes, it is essential to characterize this aspect of the samples. The information generated from both the phylogenetic tree, combined with lineage data, can help determine the connections between samples involved in the outbreak. Tools: {% tool "pangolin" %} or {% tool "nextclade" %}.
- **Available pipelines**:  
  - [nf-core/viralrecon](https://wonder.cdc.gov/amd/flu/irma/irma.html): is a bioinformatics analysis pipeline used to perform assembly and intra-host/low-frequency variant calling for viral samples.  
  - {% tool "irma" %}: was designed for the robust assembly, variant calling, and phasing of highly variable RNA viruses. Currently, IRMA is deployed with modules for influenza, ebolavirus, and coronavirus.

