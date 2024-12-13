---
title: FAIR data
description: Apply the FAIR principles to infectious disease research data, emphasizing documentation, accessibility, metadata standards, and interoperability to promote transparency, collaboration, and reuse.
contributors: ["Marcos Casado Barbero", "Romain David", "Iris Van Dam", "Rudolf Wittner"]
page_id: fd_data_description
redirect_from: /fair-data/data-description
rdmkit:
  - name: Why are the FAIR principles needed?
    url: https://rdmkit.elixir-europe.org/about#why-are-the-fair-principles-needed
  - name: Identifiers
    url: https://rdmkit.elixir-europe.org/identifiers
  - name: Sensitive data
    url: https://rdmkit.elixir-europe.org/sensitive_data
  - name: What is data reuse
    url: https://rdmkit.elixir-europe.org/reusing#what-is-data-reuse
fairsharing:
  - name: European Genome-phenome Archive (EGA)
    url: https://fairsharing.org/FAIRsharing.mya1ff
  - name: European Nucleotide Archive (ENA)
    url: https://fairsharing.org/FAIRsharing.dj8nt8
  - name: Database of Genotypes and Phenotypes (dbGaP)
    url: https://fairsharing.org/FAIRsharing.88v2k0
  - name: Ontology Lookup Service (OLS)
    url: https://fairsharing.org/FAIRsharing.Mkl9RR
related_pages:
    data_sources: [hchd_data_sources]

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction

The [FAIR principles](https://www.go-fair.org/fair-principles/) provide guidelines for making research data (i.e. digital assets) **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable ([Wilkinson et al., 2016](https://doi.org/10.1038/sdata.2016.18 )). In infectious diseases research, adhering to these principles is crucial for facilitating data sharing, collaboration, and accelerating progress towards:
* Meta-analyses
* Reliable transmission maps
* Understanding of the spread and evolution of pathogens
* Improved diagnostics, treatments, and vaccines

By ensuring maximal data usability, FAIRness increases the efficiency and impact of your infectious disease research. 


## Findability

Findability is a crucial aspect of infectious diseases research, as it ensures that relevant data and resources can be easily discovered and located by researchers and other stakeholders. 

This is particularly important in the context of infectious diseases, where **rapid access to accurate, comprehensive and purpose-specific data is essential** for effective outbreak response and disease management. 

Moreover, by making infectious disease data more findable, researchers promote transparency, accountability and reproducibility of infectious diseases research, as well as avoid duplicating the effort of their discoveries. Ultimately, all of these factors help to build trust among stakeholders and enable better and faster collaborations and knowledge sharing.


### Considerations

* Use (globally) unique and persistent [identifiers](https://rdmkit.elixir-europe.org/identifiers) (e.g. [biosample:SAMEA6864906](https://www.ebi.ac.uk/biosamples/samples/SAMEA6864906)) for each of your records, asserting they are unambiguously resolvable from anywhere in the world.
* Use standard naming conventions for human and disease data (e.g. [Brill-Zinsser](https://www.ebi.ac.uk/ols/ontologies/efo/terms?short_form=EFO_0007182) disease), as well as for taxonomic classifications (e.g. [taxonomy:9606](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?mode=Info&id=9606) for humans or [taxonomy:2697049](https://identifiers.org/taxonomy:2697049) for COVID-19). 
* Describe your data with clear variable names with possible searchable keywords and comprehensive descriptions: choose field standards if possible. Prioritise primary and usual users' standards, but do not forget that metadata may be used by novel users to the field, to which you can cater with generic and understandable. Metadata must be sufficient and appropriate.
* Register your data as open and accessible as possible through repositories and data portals (e.g. {% tool "ega" %}, {% tool "dbgap" %}, {% tool "health-portal" %}…). 
* Make your webpage machine accessible and readable, especially for search engines. You can always check the findability of the data you submitted (e.g. using a new session on a web browser), adjust and correct it if needed.

### Existing approaches

* It is vital that the data you produce gets archived in a permanent archive that allows for controlled distribution, not just for the set of years your project is active. Some examples of human archives are the {% tool "ega" %} and {% tool "dbgap" %}, also encompassed by other major frameworks like {% tool "biostudies" %} or the {% tool "covid-19-data-portal" %}.
* Take a look at other approaches at the [Finding metadata](/data-sources/human-clinical-and-health-data) section.


## Accessibility

Accessibility in infectious diseases research is crucial to ensure quick, secure and equitable access to clinical and biomolecular data for all, regardless of the reputational or economical power of researchers and institutions, thus promoting the infectious disease research to be community driven.

### Considerations

* Albeit the emergency of an infectious disease outbreak may pose a tempting chance to obtain human (meta)data through a back-door, when dealing with personal data, and specially [sensitive information](https://rdmkit.elixir-europe.org/sensitive_data), privacy and security measures must remain in place:
    * Sensitive (meta)data must be accessible through the authorised (and community approved) procedures of the archives to which they are submitted. 
    * You should avoid distributing (meta)data through unsecured channels (e.g. sending metadata of patients in an email to another researcher elsewhere), and instead make use of the procedures already in place by archives. 
* In a rapid environment like an infectious disease outbreak, (meta)data may also change rapidly: human errors may occur and making changes to (meta)data records may be a necessity. Nevertheless, for the sake of traceability, it is crucial that the (meta)data you submit to an archive is not removed, even when the information it contains is technically wrong: there are other alternatives (e.g. record deprecation) that allow for traceability. Additionally, it is also important to state when a record has been withdrawn, updated or replaced.
* For all of these aspects, your institution will often do the work for you, you just need to follow their guidance. If not existing, report your action to national repositories or international disciplinary repositories: they provide efficient support for data deposit.
* Check the accessibility of your data. Your dataset, when submitted to an archive, is likely to have a landing page with several data access services (e.g., download, transcription, contact person, visualisation…). From the perspective of someone foreign to the system to access the data, try to find out how easy it is and then adjust and retest. To increase the quality of accessibility, you can also apply the stable [W3C WCAG](https://www.w3.org/WAI/standards-guidelines/wcag/) and use their tools and methods to assess it.

### Existing approaches 

* There are multiple archives with secure procedures already in place for the distribution of sensitive human information through authentication and granted access. For example, the {% tool "ega" %} has a request and grant method to provide secure ad-hoc access to human datasets.
* Check other use-cases and examples at the [Data access]((/human-clinical-and-health-data/data-sources)) section.


## Interoperability

Interoperability is essential for infectious diseases research because it enables the **integration and analysis of data from different sources** (e.g. different hospitals, countries, biological sources, etc.), leading to a more comprehensive understanding of disease transmission, prevention, and treatment. 

Without interoperability, data silos may emerge, restricting researchers' ability to link different datasets and slowing progress in the fight against infectious diseases. Specifically, issues such as synonymy and polysemy can lead to misinterpretation of scientific results and hinder the clear communication of recommendations, which can be crucial, especially during a pandemic.

### Considerations

* Provide detailed metadata for infectious disease datasets, including the source, collection date, location, and any performed protocols (e.g. nasal swab being the method of isolation: [EFO:0010741](http://www.ebi.ac.uk/efo/EFO_0010741)). Even when the granularity of the (meta)data varies, you should always use descriptive fields with broadly understandable values. 
* Use controlled vocabularies and ontologies to describe human data and infectious diseases (e.g. [EFO:0007182](http://www.ebi.ac.uk/efo/EFO_0007182) for Brill-Zinsser disease). Furthermore, do not forget contextual data that must meet intercommunity standards, for example: time, temperature, pressure, chemical components… 
* Controlled vocabulary refers to a set of terms, standardised by the field community,  used to describe and categorise concepts, ensuring consistency and accuracy in data organisation and retrieval. For example, when an infectious disease (e.g., malaria) has multiple names (e.g., Plasmodium infection, jungle fever), it is recommended to use the designated one in the ontologies to minimise redundancy and improve data integration.
* Make use of existing metadata standards, such as Data Catalog Vocabularies (DCATs) or the Minimum information about a single amplified genome (MISAG) and a metagenome-assembled genome (MIMAG) of bacteria and archaea ([Bowers et al., 2017](https://www.nature.com/articles/nbt.3893)).
* Structure your data so that it is [machine-actionable](https://rdmkit.elixir-europe.org/machine_actionability#what-does-machine-readable-machine-actionable-or-machine-interpretable-mean-for-data-and-metadata-in-rdm).
* Your data should include qualified references to other data sources and metadata, which would increase the traceability and context of your dataset. This may ultimately be needed for necessary meta analyses in pandemic situations. References in fields like the source of patient data (e.g. [UBERON:0001707](http://purl.obolibrary.org/obo/UBERON_0001707)), the laboratory that performed the analysis (e.g. including the name of the laboratory, the name of the institution, and its location), or the specific protocol (e.g. [sample collection](https://journals.asm.org/doi/full/10.1128/JCM.40.11.3956-3963.2002)) used, greatly enhance the quality and transparency of the data. 
* Verify interoperability by reviewing the definitions of variables and linking them to relevant ontology concepts, ensuring that potential users can assess the compatibility of their data. To achieve this, import corresponding definitions and consult with your data producers to confirm that field definitions do not have significant discrepancies with the data you generate. That has to be done each time you integrate new variables and variable names/definitions.

### Existing approaches

* For controlled vocabularies and ontologies you can use the {% tool "ols" %}. This handy service compiles multiple ontologies through which you can search at once. 
Examples of ontologies related to infectious diseases and human data and diseases are EFO (Experimental Factor Ontology), MONDO (Mondo Disease Ontology), HP (Human Phenotype Ontology), CIDO (Ontology of Coronavirus Infectious Disease), IDO (Infectious Disease Ontology), IDO-COVID-19 (The COVID-19 Infectious Disease Ontology), VIDO (The Virus Infectious Disease Ontology), DOID (Human Disease Ontology), the OBI (Ontology for Biomedical Investigations), and VO (Vaccine Ontology).
* It is possible to disseminate any recommendation on how to choose “good” ontologies, participating in the better understanding of well used and better recognized terminologies in related fields. To do it, some ideas can be found in: [Identifying, naming and interoperating data in a Phenotyping platform network : the good, the bad and the ugly.](https://doi.org/10.5281/zenodo.3539259) 
* To aid with the taxonomy classification of your samples (human source, xenografts, tissue cultures, viral agents, etc.) you can make use of the [NCBI's taxonomybrowser](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi).
* Please refer to RDA COVID-19 recommendation (and others) to help you to use most recognized terminologies adapted to your case: RDA COVID-19 Working Group. (2020). [RDA COVID-19 Recommendations and Guidelines on Data Sharing (1.0)](https://doi.org/10.15497/rda00052)


## Reusability

Infectious disease research heavily relies on the reusability of human clinical and health data, well-defined usage policies, and metadata with community approved quality check processes and sufficient, appropriate and trustworthy provenance information. Without these elements, conducting effective research in this field can be challenging or even impossible.

### Considerations

* Metadata quality is needed to truly see the data quality and data reusability. Without the metadata, the data, regardless of its quality, is unusable.
* The provenance of your data must be transparent for effective tracking of infectious diseases. Key provenance fields include, for example: the geographic location of the study or data source, the date and time of data collection, sources of patient demographic information (e.g., age, gender, ethnicity), sample collection and processing methods (e.g., blood draw, tissue biopsy, RNA extraction), and ethical or legal considerations (e.g., informed consent, data ownership, privacy regulations). The content of provenance information is always context-dependent, tailored to the purpose of provenance collection and the nature of the data produced. Efficient and accurate metadata for provenance should also capture all sensor parameters, ensuring replicability even if the original sensor is no longer available.
* Make sure that the clinical data you intend to share complies with the applicable laws regarding privacy (e.g. [GDPR Art. 9](https://gdpr-info.eu/art-9-gdpr/)), and rely on the existing data archives for its distribution. When possible, make sure that your data is not completely blocked from being reused, which would render it unusable when shared. Remember: as safe as it needs, but as open for research as the regulations allow.
* Infectious diseases may require an even quicker approach to data discoverability (multi-indexation), distribution and reuse. Within this timeframe, developing a plan from scratch for the data collection, storage, sharing, access, dissemination and reuse seems unfeasible. This timeframe advocates for a thorough preparation: you should create protocols for each of these steps, so that when the time comes, you and your team are prepared.
* Check your reusability (your dataset should have a landing page with several data and other digital object access services e.g. download, transcription, contact person, visualisation…) -> adjust and retest with different kinds of users to better understand their needs. If potential users are not sure of your data content : data quality, they never reuse them for their own study. (several checklists exist, see for instance: [PARSEC DDOMP](https://doi.org/10.5281/zenodo.3891427))

### Existing approaches 

* Redacting and interpreting data reuse policies is a complex and tedious task, especially when time is the main bottleneck of the research. For this reason, Data Use Conditions ({% tool "the-data-use-ontology" %}) were created (search for yours at {% tool "ols" %}). These allow to annotate datasets with usage restrictions, enabling: 
    * Automatic discovery of the data based on user authorization level or intended use.
    * A quick and easy interpretation, from the perspective of the users, of the conditions to be met for data usage.  (e.g. use very well known and open licences like [Creative Commons](https://creativecommons.org/) and repositories that permit public licences and embargos like {% tool "zenodo" %})
* Make these controls in an iterative way and publish your metadata!
* Keep track of data reuses, and if publicly available, give a perspective of what was done with your dataset
* Make your dataset citable by uploading it to a well-established data repository that provides DOI or another stable identifier! 
