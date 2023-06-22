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
It is very important that data is adequately described in order for others to be able to make use of it and to promote reproducibility. For general information on the importance of data description, please see [the documentation and metadata section of RDMkit](https://rdmkit.elixir-europe.org/metadata_management).

There are many different types of data that relate to pathogen characterisation. This may include, for example, descriptions of biological specimens, of the protocols used in data collection, and/or genomic data. The information on this page is intended to show you what you should consider when describing different types of data related to pathogen characterisation. It should enable you to understand how to share your data with sufficient description to enable reuse.
## Good practices for describing data in general
You should always plan your study with data sharing in mind. Identifying the information necessary for effective data sharing will allow you to generate documentation that is both well structured and complete. Describing the data entails extracting the information, recording it according to existing best practice guidelines and standards, and extending descriptions where needed. 

### Considerations
When defining a general data description strategy, it is important to consult relevant guidelines and adopt accepted standards.
* **Review the submission guidelines of the repository/repositories you intend to submit data into.** Different repositories will often require different levels/types of metadata, or enable you to restrict access to different extents. This is because different repositories will enable users to search for different aspects of metadata, for example. It is important to check their requested data formats and checklists. We encourage you to go beyond just the minimum data required by the repository, as this will likely increase the reusability of your data in different contexts. Do contact them via helpdesk if you have any questions here.
* **Adopt shared practices for annotating experiments.** Some research communities have developed guidelines detailing shared/common practices for describing experiments and how to embed descriptions in the data. By adopting a shared standard, your data are likely to be more accessible and understandable to potential users. At a minimum, it is generally recommended that you describe the design of the study/program, collected specimens, sample preparation steps, experimental protocols and workflow. 
* **Follow the recommendations from national and international** authorities including e.g. public health authorities, epidemic surveillance programs, and research data communities.
* **Share/reference information about cohorts, samples, instruments, protocols, materials & methods.** It is important to retain information about which protocols (including which version) were used at each step of your experiments, as well as which samples were prepared and processed together. This can include, for example, information about the model number of the instruments used, the biobanks samples used, and the suppliers of kits. This can allow users to identify potential issues and artefacts and even generate new data.. 
* **Share/reference data assets, software versions & computational workflows.** You should include links/references to source data used, and describe analytic workflows (with runtime quality metrics). Other information could include bioinformatics protocols used, and the versions of software and computational workflows used. This is crucial for understanding exactly what was done as well as identifying potential areas for improvement.
* **Protect the privacy of human research subjects and patients.** Whilst providing complete data descriptions is generally advisable, some data will need to be anonymised before it can be shared. You should describe how and why sensitive data were masked or removed.
### Existing approaches
* Outline the data sharing platforms, data description standards, and checklists, including the desired   [data management plan](https://rdmkit.elixir-europe.org/data_management_plan#what-should-you-write-in-a-dmp).
* Refer to the [data sources page] to identify relevant data sharing platforms and related reporting schemas
* Refer to ECDC’s Infectious disease topics for active surveillance initiatives and reporting standards related to the disease associated with the pathogen under study.
  * ECDC’s Methods for the detection and identification of SARS-CoV-2 variants
  * ECDC’s Surveillance and study protocols
  * ECDC’s TESSy reporting protocol for COVID-19
  * WHO’s Genomic sequencing of SARS-CoV-2: a guide to implementation for   * maximum impact on public health, 8 January 2021, notably chapter 3 on project planning/study design and chapter 4 on data sharing guidance.
  * WHO’s Guidance for surveillance of SARS-CoV-2 variants: Interim guidance, 9 August 2021
* Refer to the FAIR Sharing registry to identify and share relevant reporting standards. 
  * https://pha4ge.org/wp-content/uploads/2022/02/giac003.pdf
  * The PHA4GE SARS-CoV-2 Contextual Data Specification for Open Genomic Epidemiology, examples of how to design data collection templates and practices for effective data sharing
  * RDA COVID-19 Working Group. Recommendations and Guidelines on data sharing. Research Data Alliance, 2020. DOI: https://doi.org/10.15497/rda00052 
  * Is the BY-COVID related FAIR Sharing collection relevant here? https://fairsharing.org/3656 
## Biological samples
### Considerations
Many different sources can be sampled to monitor and identify different pathogens.
* Describing environmental samples
It is important to describe and provide metadata especially about geolocalisation, time-zone when samples were taken, the meteorological conditions and other   (link to specific checklists and standards to described this should be provided in existing approaches)
* Describing human host related samples
For biological samples from human host, health authorities and communities? Provide both generic and specific guidelines. Usually, national authorities adopt and customise international recommendations. Check the national pages.
* Describing samples that do not originate from natural environments or hosts, e.g. cultured / lab grown etc.
* Describing pooled samples
### Existing approaches
* Description of biological samples must be provided together with molecular data and metadata. Therefore, repositories such as ENA and GISAID might have specific requirements for description of biological samples.
  * For ENA
Key sample metadata that must always be submitted to ENA, regardless of pathogenic organism is difficult to agree on, but important metadata for a pathogen context is below:
Tax id / scientific name of sample
Geographic location, collection date
host scientific name, host health state
collector name, collecting institution
E.g. key information to collect about sequencing for an ENA submission: platform/ instrument, instrument model, library source, library selection, library strategy  
  *  GISAID ?
* International and community efforts have been made to harmonise or provide unified checklists: 
Examples of issues in mapping between ENA/GISAID: https://docs.google.com/spreadsheets/d/1gNpdZKOUKPemMUHR107JRSeaWjPczlMIUp5fP5-kR9g/edit#gid=0
* WHO
## Protocols and procedures (/workflows) 
### Considerations
* Describe applications of existing protocols
* Describe study specific procedures
* Describe computational workflows and tools
### Existing approaches
## Genome data of viral pathogens
Virus screening and viral genome reconstruction are urgent and crucial for the rapid identification of viral pathogens, i.e., tracing the source and understanding the pathogenesis when a viral outbreak occurs. Analysis of this data is also important to identify mutations and track variation for effective genomic surveillance. 
### Considerations
Descriptions for genome data should follow good practices for describing data in general (see paragraph above). When looking for existing approaches to describe your viral genomic data, you should first consider the following aspects.
* *Provide information aboutthe design of the study/program and experimental variables.* 
The purpose of the study and what variables and observations are required to reach its goals and how the genome data fits into this context.
* *Describe how the genomes were prepared for sequencing*
Typically how the genomes were prepared to a state where RNA/DNA has been
extracted and amplified are ready to be prepared as libraries for the sequencing
Instrument. Make sure to describe every step of your genome preparation process in
detail, so that others can reproduce it. Include links to high quality repository submission files
* *Describe how sequencing was performed and configured*
The sequencing protocol applied might significantly affect your result. Describing
sequencing protocol is the only way to know if multiple data sources can be combined
or compared. 
* *Describe how the data was processed/analysed*
Alignment protocol needs to be described for publishing in repositories such as ENA or
XX. These repositories accept description as FREE TEXT? So, make sure to check
the info and the formats required from each repositories when you start your study. 
* *Describe the genomic data files and descriptions embedded in genomic data files*
Refer to the manufacturer’s/tool’s description of how the data were encoded in the
files—different ways to encode information in free text fields or different scales for
numerical values, also custom fields and extensions. Reference/describe conventions
used for annotations/recording field values provided by the specific study/programme
Data sharing:
* Raw Reads and sequences:
  * If you aim to share data in open repositories (e.g. ENA…), be sure to remove human related reads → In “existing approach” points to existing workflows for that (or data analysis page?). Apply anonymisation technicques (other pages talking about this?)
  * Both ENA and EpiCoV™ impose restrictions on what file formats they can accept and how the data must be prepared before uploading them to the platforms. In order to complete a submission to both platforms the consensus sequence must be saved in a FASTA format file, while the corresponding reads must be saved as BAM, CRAM or FASTQ format files. The files must also be anonymized by removing human related reads and identifiers followed by compressing (GZIP) and recording checksums (MD5) (for the compressed files).
* Which repositories to submit this data? 
  * Be aware there are differences between data repository requirements
* Variants
* Transition from data description to data sources page?
  * The data collected and described above should be shared in an open access repository for the global scientific community, which repository you should pick and any formatting to these repositories, can be found in the [Data Sources] page
### Existing approaches
* Describe your study and experimental variable as in this examples:
  * Examples of studies objectives: Determine the genome of an emerging pathogen, identify emerging variants in a population, phylogenetic analysis for understanding of how pathogens evolve, Genomics and epidemiological surveillance for tracking pathogen transmission and evolution
  * Examples of variables/data: reads, sequences (assembly, variants, consensus), alignments, annotations
* Essential protocols to be described in details are:
  * Collection protocol (see biological sample paragraph above)
  * Genome preparation: RNA/DNA Extraction protocol, Amplification protocols, Contaminations, samples that were prepared together, …
* Critical information to be provided about the sequencing set-up is:
Something about be important to mention for a protocol (e.g., index for multiplex illumina VS something specific for Nanopore?)
    * Library preparation
    * Sequencing instrument configuration
    * Pooled / multiplexed runs, instruments, configuration, automated / manual processing, demultiplexing
    * How was the instrument data converted to standardised formats
* Information about data processing to be described:
Algorithm used → in existing approaches, you could indicate where to publish the algorithm and how to link it 
Data normalisation protocol / alignment
Variant analysis → any parameter repository really want to know when publishing a variant?
* Description of data files:
Examples of conventions used for annotations/recording field values provided by the specific study/programme: xxx
Examples of file formats with variations across instruments/tools: FASTA/FASTQ, BAM/SAM/CRAM, VCF, GFF3/GTF
* Ten simple rules for annotating sequencing experiments, general guidance on how to prepare documentation for sequencing projects
* Data files with reads produced by sequencing instruments often contain fragments of the host organism’s DNA. When the host is a human research subject or patient, these fragments must be masked or removed from the data files before they can be submitted to ENA.
* The most prominent platforms for viral genome data sharing in Europe are the European COVID-19 Data Portal (ENA) and GISAID’s databases. Data should be deposited to both of these platforms and measures should be taken to ensure that consensus sequences and corresponding instrument reads can be referenced across the two platforms and across surveillance systems, such as the NCOV* reporting subjects in ECDC’s TESSy / EpiPulse. Access to instrument reads is important for validation and analysis using alternative or improved workflows.
  * GISAID focuses on data sharing related to viruses and the EpiCoV™ database is specifically designed for sharing COVID-19 and SARS-CoV-2 genome data. EpiCoV™ is an important resource for many public health authorities and researchers but the database is currently limited to provide access to consensus sequences and enforces a license that places some restrictions on how and by whom the data can be accessed and reused in downstream analysis.
  * The European COVID-19 Data Portal is also specifically designed for sharing COVID-19 and SARS-CoV-2 data and provides access to a wide range of data including consensus sequences and reads submitted to ENA—or any member of INSDC. Data submitted to ENA is provided under a free and unrestricted access policy that enables further innovations such as public dashboards and analysis pipelines and targeted or local surveillance initiatives. 
  * Contributions and access to national and European surveillance systems is usually administered by national health authorities. Some of the data contained in these systems may not be suitable for widespread or public sharing and the main purpose of the systems is to support policy and public health actions.
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

Make sure to add to the Tools and resources list table all of the tools and resources mentioned in the text.


## Concrete topic 2 <!---REPLACE THIS with the name of the topic. Example: Metadata harmonisation--->

Follow the same guidelines as in Concrete topic 1

### Considerations <!---This should not be replaced as these are considerations about concrete topic 1--->

Follow the same guidelines as in Concrete topic 1

### Existing approaches <!---This should not be replaced as these are existing approaches for concrete topic 1--->

Follow the same guidelines as in Concrete topic 1

Make sure to add to the Tools and resources list table all of the tools and resources mentioned in the text.


<!---add as many topics as need, following the same structure of topic title, Considerations, Existing approaches--->

<!---Information below will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->
name: 
orcid: 
git: 
affiliation: 
