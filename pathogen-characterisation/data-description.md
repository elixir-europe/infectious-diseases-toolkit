---
title: Data description
description: Finding (meta)data standards and documentation
contributors:
  [Wolmar Nyberg Åkerström, Zahra Waheed, Liane Hughes, Flora D'Anna, Patricia Palagi, Wolfgang Maier, Diana Pilvar, Rafael Andrade Buono]
page_id: pc_data_description
rdmkit:
  - name: "Your tasks: Documentation and metadata"
    url: https://rdmkit.elixir-europe.org/metadata_management
  - name: "Human Pathogen Genomics"
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

## Introduction 
Ensuring that data is adequately described is crucial to enable others to be able to reuse it or reproduce work. For general information on the importance of data description, please see [the documentation and metadata section of RDMkit](https://rdmkit.elixir-europe.org/metadata_management).

There are many different types of data that relate to pathogen characterisation. You may need to describe, for example, biological specimens, the protocols used in data collection, and/or genomic data. This page will inform you of what you need to consider when describing data related to pathogen characterisation. By following the guidance on this page, you should be able to share your data with all the description necessary to enable others to reuse it.

## Good practices for describing data in general
You should always plan your study with [data sharing](https://rdmkit.elixir-europe.org/data_publication) in mind. Identifying the information necessary for sharing your data effectively will allow you to generate documentation that is both well structured and complete. Describing the data entails extracting the information, recording it according to existing best practice guidelines and standards, and extending descriptions where needed.

### Considerations
When defining a general data description strategy, it is important to consult relevant guidelines and adopt accepted standards.
* **Include enough detail to inform assessment by your peers and the wider research community.**
The way that you describe and document your data will vary depending on the type of study. The descriptions should include all of the information necessary for others to be able to understand and process the data that you share. It should also include sufficient information to enable an informed assessment of the reliability of the data and the comptence with which they were generated. The descriptions are usually organised following research community guidelines and then structured as metadata to make the data FAIR.
* **Review the submission guidelines of the repositories that you intend to submit data into.** Different repositories often require different levels/types of metadata, and restrict access to the data to different extents. This is largely linked to the fact that different repositories have different aims/audiences, and will therefore enable users to search different parts of the metadata. It is important to check the requested data formats and the checklists specified by the repositories. We encourage you to go beyond just the minimum data required by the repository, as this will likely increase the reusability of your data in different contexts. Contact the repositories via their helpdesks if you have any questions about whether you are able to include different types of metadata.
* **Adopt shared practices for annotating experiments.** Some research communities (e.g. ECDC) have developed guidelines detailing shared/common practices for describing experiments and how to embed descriptions in the data. By adopting a shared standard, your data are likely to be more accessible and understandable to potential users. At a minimum, it is generally recommended that you describe the design of the study/program, collected specimens, sample preparation steps, experimental protocols, and workflow. 
* **Follow the recommendations from national and international authorities** including e.g. public health authorities, epidemic surveillance programs, and research data communities.
* **Share/reference information about cohorts, samples, instruments, protocols, materials and methods.** It is important to retain information about which protocols (including which version) were used at each step of your experiments, as well as which samples were prepared and processed together. This can include, for example, information about the model number of the instruments used, the biobanks samples used, and the suppliers of kits. This can allow users to identify potential issues and artefacts and even generate new data.
* **Share/reference data assets, software versions & computational workflows.** You should include links/references to source data used, and describe analytic workflows (with runtime quality metrics). Other information could include bioinformatics protocols used, and the versions of software and computational workflows used. This is crucial for understanding exactly what was done as well as identifying potential areas for improvement.
* **Protect the privacy of human research subjects and patients.** Whilst providing complete data descriptions is generally advisable, some data will need to be anonymised before it can be shared. You should describe how and why sensitive data were masked or removed.

### Existing approaches

* Refer to the {% tool "fairsharing" %} registry for standards related to repositories. For example, [the BY-COVID Data Resources FAIR Sharing collection](https://fairsharing.org/3773) includes references to implemented standards.
* Refer to [ECDC’s Infectious disease topics](https://www.ecdc.europa.eu/en/infectious-disease-topics) for active surveillance initiatives and shared reporting standards related to the disease associated with the pathogen under study. Examples of COVID-19 materials include:
  * [ECDC’s Methods for the detection and identification of SARS-CoV-2 variants](https://www.ecdc.europa.eu/en/publications-data/methods-detection-and-characterisation-sars-cov-2-variants-second-update)
  * [ECDC’s Surveillance and study protocols](https://www.ecdc.europa.eu/en/covid-19/surveillance/study-protocols)
  * [ECDC’s TESSy reporting protocol for COVID-19](https://www.ecdc.europa.eu/sites/default/files/documents/COVID-19-Reporting-Protocol-v5.1.pdf) 
* Refer to [WHO's publications](https://www.who.int/publications) to learn more about standards, tracking, and reporting for pathogens affecting global health. For example:
  * [WHO’s Genomic sequencing of SARS-CoV-2: a guide to implementation for   * maximum impact on public health, 8 January 2021](https://apps.who.int/iris/handle/10665/338480), notably chapter 3 on project planning/study design and chapter 4 on data sharing guidance.
  * [WHO’s Guidance for surveillance of SARS-CoV-2 variants: Interim guidance, 9 August 2021](https://www.who.int/publications/i/item/WHO_2019-nCoV_surveillance_variants)
* [The PHA4GE SARS-CoV-2 contextual data specification package](https://doi.org/10.1093%2Fgigascience%2Fgiac003) has examples of how to design data collection templates as well as practices for effective data sharing.
*  Refer to guidelines of international consortia and focus groups. For example, the RDA COVID-19 Working Group's [Recommendations and Guidelines on data sharing](https://doi.org/10.15497/rda00052). Released in 2020, it includes information on adopting shared practices.
* Outline the data sharing platforms, data description standards, and checklists, in your [data management plan](https://rdmkit.elixir-europe.org/data_management_plan#what-should-you-write-in-a-dmp).

## Biological samples
### Considerations
Many different types of material can be sampled to monitor and identify pathogens.
* **Describing environmental samples.** It is important to describe and provide metadata about your samples e.g. about geolocalisation, time-zone in which sample were taken, and the meteorological conditions at the time of collection.
* **Describing samples related to human hosts.**
For biological samples from human hosts, consider that national authorities adopt and customise international recommendations.
* **Describing samples that do not originate from natural environments or hosts**. This includes cultured/lab grown samples.
* **Describing pooled samples**
### Existing approaches
* Descriptions of biological samples (metadata) must be provided alongside the molecular data. Therefore, repositories such as {% tool "ena" %} and GISAID have specific requirements for the description of biological samples.
  * Which sample metadata should be submitted to repositories, regardless of pathogenic organism, is often debated. However, important metadata for a pathogen context is below:
    * Taxon id / scientific name of sample.
    * Geographic location.
    * Collection date.
    * Host scientific name.
    * Host health state.
    * Collector name.
    * Collecting institution.
    
<!-- MOVE THIS TO THE SEQUENCING BIT BELOW? E.g. key information to collect about sequencing for an ENA submission: platform/ instrument, instrument model, library source, library selection, library strategy --> 

* International and community efforts have been made to harmonise or provide unified checklists. For example, [there is a list of issues in mapping between ENA/GISAID.](https://docs.google.com/spreadsheets/d/1gNpdZKOUKPemMUHR107JRSeaWjPczlMIUp5fP5-kR9g/edit#gid=0)
<!-- ideally change doc link above to more formal link --> 
* Check WHO's guidance on metadata standards. See, for example, [their guidance for COVID-19](https://apps.who.int/iris/handle/10665/338480), notably chapter 6, table 2.

<!-- NEED INPUT FROM OTHERS TO EXPAND THIS## Protocols and procedures (/workflows) 
### Considerations
* Describe applications of existing protocols
* Describe study specific procedures
* Describe computational workflows and tools

### Existing approaches -->
 
## Genome data of viral pathogens
The screening and genome reconstruction of viruses is crucial in understanding the pathenogenesis of a pathogen, and in enabling the sources of outbreaks to be traced rapidly.

### Considerations
Whilst it is inherently important to follow general best practices for genome data management, there are also specific considerations for this type of data:

* **Aim for someone else to be able to replicate the experiments.**
You should adopt common practices to enable others to compile and use data generated across different research projects and public health initiatives. This includes being able to add more samples to extend the scope of a study.
* **Describe the design of the study/program and experimental variables.**
This includes, for example, the purpose of the study, the variables and observations required to reach its goals, and how the genome data fits into this context.
* **Describe how the samples were prepared for sequencing.**
This includes describing how and where specimens were collected and the process used to create the samples containing the genomic material of interest. You should also reference protocols, reagent kits, instruments, and note any key observations and choices made.
* **Describe how sequencing was performed and configured.**
This includes, for example, describing which sequencing technologoy was used and the corresponding platform, instrument models, and the library preparation protocols selected for the experiment. You should note any key observations and choices, such as the assessment of samples, multiplexing/demultiplexing approach, software settings, and other factors that strongly influence the results.
* **Describe how the data was exported and processed.** 
Describing which file formats were used, what each file contains, how the different files are related to each other, and if/how some information was masked or discarded.
* **The potential differences in policies between the data repositories to which you will submit**. For example, there are differences between GISAID and ENA, with GISAID having a more restrictive licence than ENA.

### Existing approaches
* State the objective of your study. Examples of study objectives include: 'To determine the genome of an emerging pathogen', and 'phylogenetic analysis for understanding of how pathogens evolve'.
* State the type(s) of data that you have. This could include: reads, sequences (assembly, variants, consensus), alignments, and annotations.
* There is guidance on which metadata should be included for submissions to repositories (for example, ENA provides both [general guidelines](https://ena-docs.readthedocs.io/en/latest/submit/general-guide.html) and [guidelines specific for pathogens](https://ena-docs.readthedocs.io/en/latest/faq/pathogen-subs-guide.html)). Refer to these guidelines to explore which metadata can be included with your submission.
* In the guidelines associated with submissions to repositories like ENA, some metadata fields will be listed as mandatory, meaning that they must be included with submissions. However, in order to ensure consistency and reproducibility, it is important to include other pieces of metadata that may not be considered mandatory. Below is a list of metadata that you should include with submissions (please refer to [guidance from ENA](https://ena-docs.readthedocs.io/en/latest/submit/reads/webin-cli.html) to clarify the terms used below):
    * Collection protocol used.
    * Information about genome preparation; RNA/DNA extraction protocol, amplification protocols, contaminant, and which samples were prepared together.
    * Information about library preparation.
    * Configuration of sequencing instrument.
    * Information about pooled/multiplexed runs, including the instruments used, configurations used, whether processing was automated/manual, and demultiplexing.
    * A description of how the instrument data was converted to standardised formats.
    * The algorithms used in normalisation/alignment protocols. You should refer to [general best practice for sequencing projects](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008260).

* Data files with reads produced by sequencing instruments often contain fragments of the host organism’s DNA. When the host is a human research subject or patient, these fragments must be masked or removed from the data files before they can be submitted.

<!--MOVE THIS TO DATA SOURCES * The most prominent platforms for viral genome data sharing in Europe are the European COVID-19 Data Portal (ENA) and GISAID’s databases. Data should be deposited to both of these platforms and measures should be taken to ensure that consensus sequences and corresponding instrument reads can be referenced across the two platforms and across surveillance systems, such as the NCOV* reporting subjects in ECDC’s TESSy / EpiPulse. Access to instrument reads is important for validation and analysis using alternative or improved workflows.
  * GISAID focuses on data sharing related to viruses and the EpiCoV™ database is specifically designed for sharing COVID-19 and SARS-CoV-2 genome data. EpiCoV™ is an important resource for many public health authorities and researchers but the database is currently limited to provide access to consensus sequences and enforces a license that places some restrictions on how and by whom the data can be accessed and reused in downstream analysis.
  * The European COVID-19 Data Portal is also specifically designed for sharing COVID-19 and SARS-CoV-2 data and provides access to a wide range of data including consensus sequences and reads submitted to ENA—or any member of INSDC. Data submitted to ENA is provided under a free and unrestricted access policy that enables further innovations such as public dashboards and analysis pipelines and targeted or local surveillance initiatives. 
  * Contributions and access to national and European surveillance systems is usually administered by national health authorities. Some of the data contained in these systems may not be suitable for widespread or public sharing and the main purpose of the systems is to support policy and public health actions.-->
