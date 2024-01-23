---
title: Pathogen characterisation
description: General considerations for pathogen characterization quality control.
contributors: [Clementina Elvezia Cocuzza, Fotis Psomopoulos, Eva Garcia Alvarez, Rudolf Wittner, Stian Soiland-Reyes, Hedi Peterson, Paul De Geest]
page_id: pc_quality_control
redirect_from: /pathogen-characterisation/quality-control
rdmkit:
  - name:
    url:
training:
  - name:
    registry:
    url:

---

## Introduction

Pathogen characterization encompasses many different features of the organism. In addition, comparison of the same pathogen from different sources is also needed in order to properly describe it. However, results from datasets generated from different sources cannot be pooled and/or compared if sample provenance data, standardised methods and quality control procedures are not followed. These procedures concern all steps of the dataset creation, starting from the collection of the samples, to the analysis of the data, which should be further documented by provenance.

Viral analysis in a pandemic scenario, concerning different geographic areas and/or communities is dependent on the possibility of analysing standardised data and metadata. Thus, the standardisation of sample collection, transport, preanalytical and analytical processing of samples used for viral detection and characterization is essential.

## Sample handling: key for data quality 
### Considerations
Data quality must be considered and quality measures should be taken from  the very beginning of the process which lead to pathogen detection and characterization, including all preanalytical and analytical procedures applied. These procedures include sample collection and transport, if needed, to the facilities where the analyses are performed. In addition to the procedures, it is key to pay attention to the existing conditions during the different steps of sample collection and processing. Hence, it is important not only to collect relevant information, but also to store it as standardised as possible, to improve interoperability and reusability of the resulting data.

### Existing approaches
The information collected regarding these steps really depends on the process and on what metadata is needed for a given project. However, the metadata about sample acquisition, processing and handling should be as rich as possible to enhance reusability of the data. The two lists below contain some general variables that may be relevant when collecting, transporting and storing samples, depending on the type of sample:

* For collection step, the following information should be controlled and documented:
    * Geographical area / site of collection.
    * Date and time of sample collection.
    * Environmental parameters.
    * Sample volume and other sample characteristics.

* Regarding Samples Transport and Storage:
    * Conditions of data transport (refrigerated, room temperature, etc).
    * Time from collection to analysis. 

The information needed heavily depends on the research/the investigations to be carried out. For the specific case of wastewater, using samples for pathogen surveillance might need specific information about sample handling for further data analysis, such as:

* Geographical area / site of collection and population size served by the wastewater plant from which the sample is being collected.
* Environmental parameters such as rainfall or other environmental aspects or variables that may affect viral target detection and quantification.
* Wastewater sample characteristics: sample volume, 24 hrs composite sample characteristics (m3/24 hrs), grab sample collection or other parameters, such as resuspended solids characteristics (mg/L).

## Preanalytical and analytical methods
### Considerations
During the preanalytical and analytical processing of the samples, there are several variables that can potentially affect the data resulting from them (some of them listed below). Thus, following guidelines on the standardisation of methods  and keeping track of the chosen procedures are key to get meaningful data from the samples.

* For both, the pre-analytical and analytical methods, it depends on the type of samples and on the pathogen to be investigated but some of the most relevant variables to consider and keep track are:
    * sample starting volume; 
    * pathogen concentration methods / protocols if any;
    * extraction methods (protein, DNA, RNA, etc), if any. Keep the information about the devices/technology/kits used, starting volume of sample concentrate, elution volume following extraction, etc;
    * hardware/instruments used.

* From the analytical methods:
    * target sequence, if any;
    * analytical methods (ie PCR, qPCR, etc);
    * information about the enzymes/reagents/kits used (ie. concentrations, volumes, etc.);
    * analytical steps and/or conditions (ie. temperatures, time, number of PCR cycles, etc);
    * hardware/instruments used;

### Existing approaches

For the analysis part, especially if it is done in different facilities or even countries, reference standards should be used when available, choosing the ones specific for the domain of study when possible.

Quality assurance / quality control (QA/QC) measures should be always in place when performing the analyses, and they are especially relevant when no standard operating procedures are available or followed.

* Some quality measures that may be:
    * Consider the use of any reference material, for instance, samples having quantified pathogen/viral material to compare with the samples that are being analysed and/or procedures that are  used.
    * Always include a negative and a positive control sample and document the ones that are being used.
    * Consider to follow standardised protocols when possible and also reference it in the metadata.

Using wastewater samples for pathogen surveillance might benefit from the following quality control steps:
* Quality control of the preanalytical process
    * Spiking wastewater samples with exogenous calibrated virus reference material, such as mengovirus or murine norovirus, before preanalytical processing in order to evaluate the efficiency of viral concentration and extraction procedures (by evaluating the recovery of the exogenous reference material introduced into the sample prior to preanalytical processing). 
    * Including a negative control sample during the nucleic acid extraction procedure to evaluate for potential cross contamination.
* Quality control of the quantitative analytical detection
    * Standard calibrated reference material (such as EURM-019 / EURM-014 single stranded RNA provided by the Joint Research Center)

In particular the European Commission Recommendation (EU) 2021/472 of 17 March 2021 has advocated the use of a common approach to establish a systematic surveillance of SARS-CoV-2 and its variants in wastewaters in the EU (OJ L 98 19.03.2021, p. 3). Standards for PCR/Digital-PCR (polymerase chain reaction) are indicated in this Recommendation document and shortly described below:

* (a) Threshold cycle value of real-time polymerase chain reaction (RT-qPCR) should be below 40 to report a sample as positive either for qPCR (quantitative polymerase chain reaction) analysis or to use for sequencing.
* (b) Alternative quantification approaches to RT-qPCR (as digital polymerase chain reaction - dPCR) could be used provided that they achieve results equivalent to RT-qPCR and apply quality requirements equivalent to RT-qPCR.
* (c) All samples should be run at least in duplicates to avoid false positive or false negative results.
* (d) The analytical procedure of real-time polymerase chain reaction used should include adequate controls to assess at least the efficiency of the concentration/extraction steps and the absence of significant reaction inhibition.
* (e) Each run should include appropriate standards (at least 3 point serial dilutions in triplicate employing synthetic SARS-CoV-2 RNA) and positive and negative controls to determine if the PCR/qPCR run produced reliable results.
* (f) A quantification cycle (Cq) cut-off value for positive samples should be set [at] 5 cycles before the termination of the amplification protocol to avoid misattribution of late fluorescence signals.
* (g) A negative extraction control should be used to account for any contamination during the RNA extraction.

## NGS pathogens data
### Considerations

A systematic approach to metadata standardisation and data harmonisation makes it possible to combine and compare datasets, consequently promoting a more universal use and reuse of the data. The European Nucleotide Archive (ENA) has set up some standards for SARS-CoV-2, listed in the next section. When possible, it is recommended to use topic-specific standards and, for facilitating this good practice, ENA has also standardised checklists for particular use cases, such as water surveillance.

There are no established best practices (at the data analysis level) to effectively assess variants from the incomplete sequencing data. This is mostly due to the fact that the definitions of different variants often share a significant percentage of mutations, with the number of unique mutations per definition radically decreasing with the number of variants considered in the study. 

Metadata standards are lacking; the systematic approach to metadata standardisation and data harmonisation will make it possible to combine and compare datasets, consequently promoting a more universal use and reuse of the data. 

### Existing approaches

When it comes to the metadata about the sequenced sample, ENA has put in place some checklists to fill in at data submission for several organism types, an example for pathogen samples can be found [here](https://www.ebi.ac.uk/ena/browser/view/ERC000033). These checklists include some mandatory fields, which are checked upon submission to make sure that they are filled in and contain acceptable values.

The metadata describing the sequencing experiment have to be submitted to ENA in an [standardised format](https://ena-docs.readthedocs.io/en/latest/submit/reads/webin-cli.html#metadata-validation). Several file types are accepted by the ENA when it comes to raw sequencing reads. There are different tools available to check their quality during the steps of the sequencing process from raw data to processed data. Examples of those tools widely used in the genomics community are:

* {% tool "fastqc" %}: Gives a report of the quality of the sequencing data using FASTQ files as input.
* {% tool "samtools" %}: Not specific for quality purposes, it has some functionality that can support quality assessment of SAM, BAM and CRAM files.
* {% tool "vcftools" %}: Similarly not limited to quality purposes, but it allows to assess the structural integrity of a VCF file.
* ISO/IEC 23092-4:2020(en), Information technology — Genomic information representation — Part 4: Reference software elaborates on reference software for genomic information representation

Finally, ENA performs some quality control on some of these files, [mainly on CRAM files](https://ena-docs.readthedocs.io/en/latest/submit/reads/webin-cli.html#cram-file-validation) and [assembled sequences](https://ena-docs.readthedocs.io/en/latest/submit/assembly/genome.html#validation-rules). Even though these are not specific for SARS-CoV-2 submissions, they do have an additional check for sequence length (max 31kbp) for submissions in the latter format.

Standards from  European Commission Recommendation (EU) 2021/472 of 17 March 2021 has advocated the use of a common approach to establish a systematic surveillance of SARS-CoV-2 and its variants in wastewaters in the EU ([OJ L 98 19.03.2021, p. 3, CELEX](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32021H0472)) document regarding Next Generation Sequencing of wastewater surveillance

* (a) At least 1 million reads-per-sample should be generated and read length should be above 100 base pair, according to ECDC technical recommendations ([Sequencing of SARS-CoV-2](https://www.ecdc.europa.eu/sites/default/files/documents/Sequencing-of-SARS-CoV-2-first-update.pdf); [Guidance for representative and targeted
genomic SARS-CoV-2 monitoring](https://www.ecdc.europa.eu/sites/default/files/documents/Guidance-for-representative-and-targeted-genomic-SARS-CoV-2-monitoring-updated-with%20erratum-20-May-2021.pdf)).
* (b) At least 3 genetic markers per variant should be reported for better characterization of mutations for High Throughput Sequencing analysis of wastewater.

## NGS data analysis
### Considerations

After the sequence generation stage, the actual analysis of the data takes place (see [Pathogen characterisation - Data analysis](/pathogen-characterisation/data-analysis)). Depending on the type of approach (targeted vs untargeted) there are slight differences to the main steps. However, regardless of the approach, the first step is always quality assessment of the data, for which there are commonly used tools, as the ones indicated in the following section.

### Existing approaches
For the overall quality (first step of the data analysis), there are some standardised tools (such as {% tool "fastqc" %}, {% tool "multiqc" %}) that can offer such an assessment that is domain agnostic. Key considerations are sufficient quality per nucleotide / read and overall mapping across the target pathogens (in case of targeted approaches).


Standards from  European Commission Recommendation (EU) 2021/472 of 17 March 2021 has advocated the use of a common approach to establish a systematic surveillance of SARS-CoV-2 and its variants in wastewaters in the EU ([OJ L 98 19.03.2021, p. 3, CELEX](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32021H0472)) document regarding normalisation of wastewater surveillance samples

* (a) Viral number of gene copies should be normalised by the population number served by the sewer system and using the wastewater flow for better comparability of measurements between different locations.
* (b) Additional normalisation controls using cross-assembly phage (c) or pepper mild mottle virus are recommended for this purpose.
* (c) If data for none of viruses referred to in point (b) can be obtained, alternative parameters could be used provided they deliver equivalent corrections for meteorological or other influences causing fluctuations of the viral load, which are not related to the pandemic such as precipitation or other meteorological effects. 


Further information on wastewater quality control can be found in Wastewater QC workflow in GalaxyTrakr (SSQuAWK3) ([protocols.io](https://www.protocols.io/)) protocol that has a nice listing of quality indicators that were defined in the context of SARS-CoV-2, but are easily generalizable.
