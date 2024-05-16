---
title: Human biomolecular data
description: This page explains in detail the importance of quality control for human biomolecular data in the context of infectious diseases, as well as explains the steps to follow.
contributors: [Aina Jené Cortada, Mireia Marin Ginestar, Clementina Elvezia Cocuzza, Arnau Soler Costa]
page_id: hbd_quality_control
redirect_from: /human-biomolecular-data/quality-control
related_pages:
  pathogen_characterisation: [pc_attributing_credit]
rdmkit:
  - name: Data quality
    url: https://rdmkit.elixir-europe.org/data_quality
fairsharing:
  name: BY-COVID Data Resources
  url: https://fairsharing.org/3773
---

## Introduction

The study of human biomolecular data, including genomics, transcriptomics, proteomics, and metabolomics, has significantly advanced our understanding of the pathogenesis, treatment and prevention of infectious diseases. However, the quality of human biomolecular data can significantly impact the accuracy and reliability of the results obtained from analyses.

Quality control (QC) is an essential step in the analysis of human biomolecular data, particularly in infectious diseases. QC involves assessing the quality of the data generated during sample collection, processing, and analysis to identify and remove errors, biases, and artefacts that may affect the accuracy and interpretation of the results. In this page, we will discuss the essential QC steps for human biomolecular data specific to infectious diseases.

## Sample collection and processing

The first step in QC for human biomolecular data is ensuring the proper collection and processing of samples. This includes collecting all clinical information that will be relevant for the analysis.
To have some guidance and considerations related to the sample collection and processing you can visit [this](https://www.cdc.gov/coronavirus/2019-ncov/lab/guidelines-clinical-specimens.html) documentation.

### Considerations

- **Rapid and Efficient Sample Collection**: During an infectious disease outbreak, it is crucial to collect samples as quickly and efficiently as possible to identify and contain the spread of the disease. A well-organised sampling plan should be implemented, including guidelines for sample collection, transport, and storage, and appropriate training should be provided to personnel.
- **Safety Precautions**: Safety precautions are crucial during an infectious disease outbreak to prevent the spread of the disease among the sample collection team and laboratory personnel. Appropriate protective equipment, such as gloves, masks, and gowns, should be provided to personnel, and guidelines for handling infectious samples should be strictly followed.
- **Scalability**: During an outbreak, the number of samples to be collected and processed may be significantly higher than normal. Therefore, the biomolecular analysis pipeline should be scalable and able to process a large number of samples quickly and accurately.
- **High-Throughput Sample Processing**: High-throughput sample processing methods, such as automated nucleic acid extraction and purification systems, can significantly increase the speed and efficiency of sample processing during an outbreak. These methods can help reduce the risk of contamination and human error and increase the accuracy and reliability of the results.
- **Collaboration and Data Sharing**: During an outbreak, collaboration and data sharing between different laboratories and research institutions can significantly accelerate the pace of research and help identify effective treatments and interventions quickly. Therefore, it is crucial to establish effective communication channels and data-sharing platforms to facilitate collaboration between different stakeholders.

### Existing approaches

When looking for solutions to sample collection and processing, you can check [this](https://rdmkit.elixir-europe.org/collecting) documentation.

## Assessment of data quality and data preprocessing

Pre-analytical errors, such as wrong labelling of the specimen, the incorrect specimen collection device, incorrect specimen type are the most frequently reported sources of error (between 48% and 62%) within the clinical laboratory, as stated in this 2021 [publication](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7917444/#s0120), Quality Assurance in the Clinical Virology Laboratory.

Conducting quality control is an essential step to avoid these kinds of errors. Quality metrics such as read depth, coverage, and base quality scores can help identify errors, artifacts, and biases in the data. Tools such as FastQC, Qualimap, and Picard can be used to assess data quality and generate summary reports. On the other hand, tools such as the FastQScreen and GRAF-pop and GRAF-sex, can be used to ensure the correct labelling of the samples. Further details on these tools are outlined below.

It’s also important to notice the need for international standards, reference materials, and external quality assessment to support quality assurance. Although it can be a challenging and a complex process, verifying and validating assay methods, monitoring assay performance over time, and ensuring traceability to international standards for calibration are key points for high quality results. 

After assessing data quality, the next step is data preprocessing. Data preprocessing involves cleaning and filtering the data to remove errors, artifacts, and biases that may affect downstream analysis. Common preprocessing steps include read trimming, adapter removal, quality filtering, and read alignment. Tools such as Trimmomatic, Cutadapt, and BWA can be used for data preprocessing.

### Considerations

- **Sample Quality Control**: The quality of the biological sample used for biomolecular analysis is critical for the reliability and accuracy of the resulting data. Therefore, it is essential to implement quality control measures to assess the quality of the sample, including its purity, integrity, and suitability for downstream analysis.
- **Standardization and Calibration**: Standardisation and calibration of the biomolecular analysis methods used are essential for ensuring the accuracy and reliability of the results. This includes the use of validated assays, appropriate positive and negative controls, and quality assessment metrics to monitor the performance of the assays.
- **Reproducibility and Robustness**: Reproducibility and robustness of the biomolecular analysis methods used are crucial for ensuring the consistency and reliability of the results across different laboratories and researchers. Therefore, it is essential to evaluate the reproducibility and robustness of the methods used, including the variability of results obtained by different operators, equipment, and reagents.
- **Data Quality Assessment and Reporting**: Data quality assessment and reporting are critical for ensuring the accuracy and reliability of the results and communicating the findings to stakeholders effectively. This includes implementing appropriate data quality control measures, such as quality assessment metrics and statistical analysis, to identify and correct potential sources of error and ensure the accuracy and reliability of the data. Additionally, clear and concise reporting of the results, including appropriate data visualisation and interpretation, can help communicate the findings effectively to stakeholders.

### Existing approaches

#### Bioinformatics tools for quality control

The following bioinformatics tools are usually part of a bioinformatics pipeline that is used for the identification of a specific variant of a known pathogen. Therefore, they can be used for infectious diseases but also in other scientific domains.

- {% tool "fastqc" %}: FastQC is a widely used quality control tool for next-generation sequencing (NGS) data. It provides a comprehensive analysis of the sequence quality, including per base sequence quality, sequence length distribution, adapter content, and GC content. FastQC generates graphical reports that allow users to identify potential issues and assess the overall quality of the sequencing data.
- {% tool "samtools" %}: Samtools is a widely used suite of tools for working with sequencing data in the SAM/BAM format. It can be used for a variety of tasks, including sorting, merging, indexing, and filtering SAM/BAM files. Samtools also includes a quality control tool called "samtools flagstat," which generates statistics on the number and proportion of reads that pass various quality filters, such as mapping quality, read length, and base quality.
- {% tool "bcftools" %}: Bcftools is a set of tools for working with variant calls in the VCF format. It can be used for tasks such as filtering, merging, and comparing VCF files. Bcftools includes several quality control tools, such as "bcftools stats," which generates summary statistics on the quality of variant calls, such as the number of variants called, the proportion of variants passing quality filters, and the distribution of variant quality scores.
- {% tool "qualimap" %}: Qualimap is a quality control tool that assesses the quality of the sequencing data at different stages of the analysis pipeline, including read mapping, coverage, and expression analysis. It generates various graphical outputs that allow users to assess the quality and reliability of the data at each step of the analysis.
- {% tool "gatk" %}: GATK is a widely used tool for variant calling and genotyping from NGS data. It uses various filtering and quality control options to identify high-quality variants and reduce false positives in the analysis.
- {% tool "picard" %}: Picard is a suite of tools that provides quality control and processing of NGS data, including duplicate read removal, format conversion, and alignment. It is widely used in sequencing data analysis pipelines to improve the quality and reliability of the data.
- {% tool "trimmomatic" %}: Trimmomatic is a tool used for the removal of adapter sequences, low-quality reads, and sequences with ambiguous bases from NGS data. It uses various filtering and trimming options to improve the quality of the sequencing data and prepare it for downstream analysis.
- {% tool "fastqc-screen" %}:  FastQScreen is a quality control tool used to detect contamination in sequencing data (FASTQ files). It screens the input data against a database, formed by the genomes of all of the organisms that could have contaminated the sample, along with PhiX, Vectors or other contaminants commonly seen in sequencing experiments.
- {% tool "graf-pop" %}: GRAF-pop is a software tool that infers the subject ancestry. For the estimation it uses about 100,000 SNPs from genotype datasets, which can be in PLINK and VCF format. 
- {% tool "graf-sex" %}: GRAF-sex determines subject sexes using the genotypes. It’s used to validate the self-reported sexes in phenotype datasets.

#### Diagnostic assays quality control

- **Sample type, collection methods and transport to the laboratory**: considering the test that is going to be performed while choosing the sample type and collection methods is a crucial step to ensure the validity and quality of the results. To get detailed guidelines for Collecting and Handling of Clinical Specimens for COVID-19 Testing, you can visit this Centers for Disease Control and Prevention [documentation](https://www.cdc.gov/coronavirus/2019-ncov/lab/guidelines-clinical-specimens.html).
- **Internal human control**: an important aspect is human resource management, for instance, ensuring personnel training, competency, and continuous professional development is necessary.
- **External quality assessment**: external audits are an essential part for ensuring the quality of the procedures. They provide an objective overview that will state any discrepancies between the results and reveal  points of improvement.
- **Procedural documents**:  How an speciﬁc laboratory activity is conducted or how a piece of equipment is has been used must be recorded in standard operating procedures (SOPs) and equipment operating procedures (EOPs). These records will ensure results reproducibility. It’s also important to notice that these records must undergo regular reviews, ensuring that they remain compliant.
- **Negative and positive controls**: including negative controls it’s important to detect contamination in the reagents, consumables, and general laboratory environment. Including negative controls in each run of diagnostic molecular testing based on RT-PCR, for example, will avoid false positive results resulting from cross-contamination. As well as positive controls for the target sequence/s used in the individual assays, to ensure no false negative results due to reagents failure. For example, the study of a housekeeping human gene would ensure quality of the sample collection procedure, as it controls that the sample has human material and the quality of the analytical procedure, making it possible to check that there is no PCR inhibition and the reagents are working properly.

## Collection of metadata

Proper metadata, adhering to the FAIR principles, significantly enhances the overall quality of biomedical studies. It enables researchers to find, access, and understand data, promotes interoperability for collaboration, and ensures that data is reusable for future research endeavours. 

To ensure the correct  and standard collection of metadata the definition of a metadata schema, beforehand, in an excel or spreadsheet, is a core decision. An interoperable, but yet, customizable metadata scheme can be found in this [publication](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9950378/). 

The mandatory and optional variables must be selected depending on the aim of the study and should include any relevant clinical data such as vaccination state, age, gender, or hospitalisation. More considerations about metadata can be found in the [Data resources page](https://www.infectious-diseases-toolkit.org/data-sources/human-biomolecular-data). 

While completing the forms, the use of ontologies is highly recommended: 
- Infectious Disease Ontology (IDO), a suite of interoperable ontology modules aiming to provide coverage of all aspects of the infectious disease domain. Further details about IDO can be found in this [paper](https://pubmed.ncbi.nlm.nih.gov/34275487/).
- CovidO, an ontology for covid-19 metadata, is described in this [paper](https://link.springer.com/article/10.1007/s11227-023-05509-4).

Besides sample metadata, assay metadata describing how the results were generated is also necessary. This metadata will depend on the type of assay (antigenic, molecular, target genes of the assay, serological, etc) and it should include all the used variables on which the results depend on.

In conclusion, the meticulous collection of metadata stands as a cornerstone in the pursuit of conducting high-quality biomedical studies. Embracing and implementing robust metadata practices not only enhances the transparency, reproducibility, and reliability of research findings but also aligns seamlessly with the FAIR principles. By systematically documenting and organising essential contextual information, researchers contribute not only to the integrity of their own studies but also to the broader scientific community's ability to harness and build upon valuable knowledge. Therefore, investing in comprehensive metadata collection is not just a procedural necessity; it is a commitment to elevating the overall quality and impact of biomolecular research.
  

