---
title: Data description
description: Finding (meta)data standards and documentation
contributors:
  - Wolmar Nyberg Åkerström
  - Zahra Waheed
  - Liane Hughes
  - Flora D'Anna
  - Patricia Palagi
  - Wolfgang Maier
  - Diana Pilvar
  - Rafael Andrade Buono
page_id: pc_data_description
rdmkit:
  - name: "Your tasks: Documentation and metadata"
    url: https://rdmkit.elixir-europe.org/metadata_management
  - name: Human Pathogen Genomics
    url: https://rdmkit.elixir-europe.org/human_pathogen_genomics
related_pages: 
  showcase: []
  human_biomolecular_data: []
  human_clinical_and_health_data: []
  socioeconomic_data: []
  pathogen_characterisation: []
training:
  - name:
    registry: 
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---
<!-- Content has been transferred an revised from the IDTk Contentathon Google Document:  https://docs.google.com/document/d/1fWpj-ti13wYsm1yCzn3Fsj1AbC-k4ePCO0Sk7K-HjuQ/edit -->
<!-- See also the associated pull request for IDTk:   https://github.com/elixir-europe/infectious-diseases-toolkit/issues/151 -->
<!-- See also the associated GitHub pages:   https://pari-neic.github.io/infectious-diseases-toolkit/pathogen-characterisation/data-description -->

## Introduction 
Ensuring that data is adequately described is crucial to enable others to be able to reuse it or reproduce work.. For general information on the importance of data description, please see [the documentation and metadata section of RDMkit](https://rdmkit.elixir-europe.org/metadata_management).

There are many different types of data that relate to pathogen characterisation. You may need to describe, for example, biological specimens, the protocols used in data collection, and/or genomic data. This page will inform you of what you need to consider when describing data related to pathogen characterisation. It should enable you to share your data with sufficient description to enable reuse.

## Good practices for describing data in general
You should always plan your study with [data sharing](https://rdmkit.elixir-europe.org/data_publication) in mind. Identifying the information necessary for sharing your data effectively will allow you to generate documentation that is both well structured and complete. Describing the data entails extracting the information, recording it according to existing best practice guidelines and standards, and extending descriptions where needed.

### Considerations
When defining a general data description strategy, it is important to consult relevant guidelines and adopt accepted standards.
* **Review the submission guidelines of the repositories you intend to submit data into.** Different repositories will often require different levels/types of metadata, or enable you to restrict access to different extents. This is because different repositories will enable users to search for different aspects of metadata, for example. It is important to check their requested data formats and checklists. We encourage you to go beyond just the minimum data required by the repository, as this will likely increase the reusability of your data in different contexts. Do contact them via helpdesk if you have any questions here.
* **Adopt shared practices for annotating experiments.** Some research communities (e.g. ECDC) have developed guidelines detailing shared/common practices for describing experiments and how to embed descriptions in the data. By adopting a shared standard, your data are likely to be more accessible and understandable to potential users. At a minimum, it is generally recommended that you describe the design of the study/program, collected specimens, sample preparation steps, experimental protocols and workflow. 
* **Follow the recommendations from national and international authorities** including e.g. public health authorities, epidemic surveillance programs, and research data communities.
* **Share/reference information about cohorts, samples, instruments, protocols, materials & methods.** It is important to retain information about which protocols (including which version) were used at each step of your experiments, as well as which samples were prepared and processed together. This can include, for example, information about the model number of the instruments used, the biobanks samples used, and the suppliers of kits. This can allow users to identify potential issues and artefacts and even generate new data.
* **Share/reference data assets, software versions & computational workflows.** You should include links/references to source data used, and describe analytic workflows (with runtime quality metrics). Other information could include bioinformatics protocols used, and the versions of software and computational workflows used. This is crucial for understanding exactly what was done as well as identifying potential areas for improvement.
* **Protect the privacy of human research subjects and patients.** Whilst providing complete data descriptions is generally advisable, some data will need to be anonymised before it can be shared. You should describe how and why sensitive data were masked or removed.

### Existing approaches

* Refer to the [FAIR Sharing registry](https://fairsharing.org) for standards related to repositories. For example, [the BY-COVID related FAIR Sharing collection](https://fairsharing.org/3773).
* RDA COVID-19 Working Group. Recommendations and Guidelines on data sharing. Research Data Alliance, 2020. DOI: https://doi.org/10.15497/rda00052. Includes information about adopting shared practices.
* Refer to [ECDC’s Infectious disease topics](https://www.ecdc.europa.eu/en/infectious-disease-topics) for active surveillance initiatives and shared reporting standards related to the disease associated with the pathogen under study. Examples of COVID-19 materials include:
  * [ECDC’s Methods for the detection and identification of SARS-CoV-2 variants](https://www.ecdc.europa.eu/en/publications-data/methods-detection-and-characterisation-sars-cov-2-variants-second-update)
  * [ECDC’s Surveillance and study protocols](https://www.ecdc.europa.eu/en/covid-19/surveillance/study-protocols)
  * [ECDC’s TESSy reporting protocol for COVID-19](https://www.ecdc.europa.eu/sites/default/files/documents/COVID-19-Reporting-Protocol-v5.1.pdf) 
* Refer to [WHO's publications](https://www.who.int/publications) to learn more about standards, tracking and reporting for pathogens affecting global health. For example:
  * [WHO’s Genomic sequencing of SARS-CoV-2: a guide to implementation for   * maximum impact on public health, 8 January 2021](https://apps.who.int/iris/handle/10665/338480), notably chapter 3 on project planning/study design and chapter 4 on data sharing guidance.
  * [WHO’s Guidance for surveillance of SARS-CoV-2 variants: Interim guidance, 9 August 2021](https://www.who.int/publications/i/item/WHO_2019-nCoV_surveillance_variants)
* [The PHA4GE SARS-CoV-2 Contextual Data Specification for Open Genomic Epidemiology](https://www.preprints.org/manuscript/202008.0220/v1), examples of how to design data collection templates and practices for effective data sharing
* Outline the data sharing platforms, data description standards, and checklists, including the desired   [data management plan](https://rdmkit.elixir-europe.org/data_management_plan#what-should-you-write-in-a-dmp).

## Biological samples
### Considerations
Many different types of material can be sampled to monitor and identify pathogens.
* **Describing environmental samples.** It is important to describe and provide metadata about your samples e.g. about geolocalisation, time-zone in which sample were taken, the meteorological conditions.
* **Describing human host related samples.**
For biological samples from human hosts, consider that national authorities adopt and customise international recommendations.
* **Describing samples that do not originate from natural environments or hosts** this includes cultured/lab grown samples.
* **Describing pooled samples**
### Existing approaches
* Description of biological samples must be provided together with molecular data and metadata. Therefore, repositories such as ENA and GISAID might have specific requirements for description of biological samples.
  * For ENA
Which sample metadata must be submitted to ENA, regardless of pathogenic organism, is often debated. However, important metadata for a pathogen context is below:
    * Tax id / scientific name of sample
    * Geographic location
    * Collection date
    * Host scientific name
    * Host health state
    * Collector name
    * Collecting institution
    
<!-- MOVE THIS TO THE SEQUENCING BIT BELOW? E.g. key information to collect about sequencing for an ENA submission: platform/ instrument, instrument model, library source, library selection, library strategy --> 

* International and community efforts have been made to harmonise or provide unified checklists. For example, [there is a list of issues in mapping between ENA/GISAID.](https://docs.google.com/spreadsheets/d/1gNpdZKOUKPemMUHR107JRSeaWjPczlMIUp5fP5-kR9g/edit#gid=0)
<!-- ideally change doc link above to more formal link -WOLMAR, IS THERE A MORE FORMAL LINK? --> 
* Check WHO's guidance on metadata standards. See, for example, [their guidance for COVID-19](https://apps.who.int/iris/handle/10665/338480), notably chapter 6, table 2.

<!-- NEED INPUT FROM OTHERS TO EXPAND THIS## Protocols and procedures (/workflows) 
### Considerations
* Describe applications of existing protocols
* Describe study specific procedures
* Describe computational workflows and tools

### Existing approaches -->

  * https://pha4ge.org/wp-content/uploads/2022/02/giac003.pdf (work this in) 
## Genome data of viral pathogens
The screening and genome reconstruction of viruses is crucial in rapidly tracing the source of an outbreak and understanding the pathenogensis of a pathogen.

### Considerations
Descriptions for genome data should follow good practices for describing data in general (see paragraph above). When looking for existing approaches to describe your viral genomic data, you should first consider the following aspects:
* **Provide information about the design of the study/program and experimental variables.**
This includes, for example, the purpose of the study, the variables and observations required to reach its goals, and how the genome data fits into this context.
* **Describe how the genomes were prepared for sequencing.**
Make sure to describe every step of your genome preparation process in
detail, so that others can reproduce it.
* **Describe how sequencing was performed and configured.**
Describing the sequencing protocol is essential when determining whether results are comparable.
<!--WOLMAR - CAN YOU PROVIDE ANY LINKS HERE AND CLARIFY THE POINTS?* **Describe the genomic data files and descriptions embedded in genomic data files**
Refer to the manufacturer’s/tool’s description of how the data were encoded in the
files—different ways to encode information in free text fields or different scales for
numerical values, also custom fields and extensions. Reference/describe conventions
used for annotations/recording field values provided by the specific study/programme
Data sharing:
* Raw Reads and sequences:
  * If you aim to share data in open repositories (e.g. ENA…), be sure to remove human related reads → In “existing approach” points to existing workflows for that (or data analysis page?). Apply anonymisation technicques (other pages talking about this?)
  * Both ENA and EpiCoV™ impose restrictions on what file formats they can accept and how the data must be prepared before uploading them to the platforms. In order to complete a submission to both platforms the consensus sequence must be saved in a FASTA format file, while the corresponding reads must be saved as BAM, CRAM or FASTQ format files. The files must also be anonymized by removing human related reads and identifiers followed by compressing (GZIP) and recording checksums (MD5) (for the compressed files).
-->
* **The potential differences in policies between the data repositories to which you will submit**. For example, there are differences between GISAID and ENA, with GISAID having a more restrictive licence than ENA.


### Existing approaches
* State the objective of your study. Examples of study objectives include: 'To determine the genome of an emerging pathogen', and 'phylogenetic analysis for understanding of how pathogens evolve'.
* State the type(s) of data that you have. This could include: reads, sequences (assembly, variants, consensus), alignments, and annotations.
<!-- WOLMAR - CAN YOU PROVIDE ANY LINKS HERE AND CLARIFY THE POINTS? * Essential protocols to be described in detail are:
 * Collection protocol (see biological sample paragraph above)
  * Genome preparation: RNA/DNA Extraction protocol, Amplification protocols, Contaminations, samples that were prepared together, … 
* Critical information to be provided about the sequencing set-up is:
Something about be important to mention for a protocol (e.g., index for multiplex illumina VS something specific for Nanopore?)
    * Library preparation
    * Sequencing instrument configuration
    * Pooled / multiplexed runs, instruments, configuration, automated / manual processing, demultiplexing
    * How was the instrument data converted to standardised formats WANT LINKS-->
* Include information about how the data was processed, such as the algorithm(s) used and the normalisation/alignment protocols. You should refer to [general best practice for sequencing projects](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008260)

<!-- WOLMAR - CAN YOU PROVIDE ANY LINKS HERE AND CLARIFY THE POINTS?* Description of data files:
    * Examples of conventions used for annotations/recording field values provided by the specific study/programme: xxx
    * Examples of file formats with variations across instruments/tools: FASTA/FASTQ, BAM/SAM/CRAM, VCF, GFF3/GTF ASK FOR LINKS- if none, remove -->

* Data files with reads produced by sequencing instruments often contain fragments of the host organism’s DNA. When the host is a human research subject or patient, these fragments must be masked or removed from the data files before they can be submitted.

<!--MOVE THIS TO DATA SOURCES * The most prominent platforms for viral genome data sharing in Europe are the European COVID-19 Data Portal (ENA) and GISAID’s databases. Data should be deposited to both of these platforms and measures should be taken to ensure that consensus sequences and corresponding instrument reads can be referenced across the two platforms and across surveillance systems, such as the NCOV* reporting subjects in ECDC’s TESSy / EpiPulse. Access to instrument reads is important for validation and analysis using alternative or improved workflows.
  * GISAID focuses on data sharing related to viruses and the EpiCoV™ database is specifically designed for sharing COVID-19 and SARS-CoV-2 genome data. EpiCoV™ is an important resource for many public health authorities and researchers but the database is currently limited to provide access to consensus sequences and enforces a license that places some restrictions on how and by whom the data can be accessed and reused in downstream analysis.
  * The European COVID-19 Data Portal is also specifically designed for sharing COVID-19 and SARS-CoV-2 data and provides access to a wide range of data including consensus sequences and reads submitted to ENA—or any member of INSDC. Data submitted to ENA is provided under a free and unrestricted access policy that enables further innovations such as public dashboards and analysis pipelines and targeted or local surveillance initiatives. 
  * Contributions and access to national and European surveillance systems is usually administered by national health authorities. Some of the data contained in these systems may not be suitable for widespread or public sharing and the main purpose of the systems is to support policy and public health actions.-->
