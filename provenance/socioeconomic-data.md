---
title: Socioeconomic data
description: Tracking socioeconomic data and documenting the analysis steps applied to it.
contributors: [Rudolf Wittner, Mari Kleemola, Simone Sacchi, Diana Pilvar, Irena Vipavc Brvar, Eva Garcia Alvarez, Robin Navest]
page_id: sed_provenance
redirect_from: /socioeconomic-data/provenance

---

## Introduction
Provenance of socioeconomics data refers to the history of the data, starting from their origin and gathering all the processes applied to them. Socioeconomics data provenance is directly related to their utility, trustworthiness and to some quality dimensions such as reliability. It provides data users the information they need to analyse the data in a meaningful manner, enabling reproducibility.

## Considerations
When generating the provenance of socioeconomics data, there are some factors that must be taken into account:
*	Identify and document all actors that took part in the processing of the data from their collection. 
*	Identify and document the collection methods and the data sources.
*	Include information about the socio-economic situation that was in place when the data were generated. 
*	Document he processes the data went through including the quality measures applied.
*	Document different version of the data.
In addition, the provenance data should follow standards, enhancing interoperability.

## Existing approaches
### Data Documentation Initiative metadata standards
Scenarios and use cases, as well as encoding provenance metadata within the widely used Data Documentation Initiative (DDI) metadata standard, are discussed by [Lagoze et al. (2013)](https://doi.org/10.1007/978-3-319-03437-9_13). In this publication they propose an encoding of the provenance metadata using the Data Documentation Initiative (DDI) metadata standard.

[Data Documentation Initiative (DDI)](https://ddialliance.org/products/overview-of-current-products) is a suite of products to describe quantitative and qualitative research data in the social, behavioural, economic, and health sciences. Using DDI one can document and manage different stages of the research data lifecycle, such as conceptualization, collection, processing, distribution, discovery, and archiving. Documenting data with DDI facilitates understanding, interpretation, and use of data by people, software systems, and computer networks. [Controlled vocabularies](https://ddialliance.org/controlled-vocabularies) in several languages are in place, which makes the presentation of metadata in different languages easier.

DDI standards cover the following areas:
* Conceptual objects: concept, unit, unit type, universe, population, geographic structures, and representation.
* Methodological objects: approaches to sample selection, data capture, weighting, quality control, and process management.
* Processing: data capture, data processing, analysis, and data management.
* Quantitative and qualitative data objects: concept, universe, representation, usage, data type, record, record relationships, storage, access, and descriptive statistics
* Data management: ownership, access, rights management, restrictions, quality standards, organization, agent management, relationship between products, versioning, and provenance.

As a practical example, the [CESSDA Metadata Model](https://zenodo.org/doi/10.5281/zenodo.4672413) is based on the DDI Lifecycle standard.

### Structured Data Transformation Language
[Structured Data Transformation Language (SDTL)](https://ddialliance.org/products/sdtl/1.0) is an independent intermediate language for representing data transformation commands. Statistical analysis packages (e.g., SPSS, Stata, SAS, and R) provide similar functionality, but each one has its own proprietary language. SDTL consists of JSON schemas for common operations, such as RECODE, MERGE FILES, and VARIABLE LABELS. SDTL provides machine-actionable descriptions of variable-level data transformation histories derived from any data transformation language. Provenance metadata represented in SDTL can be added to documentation in [DDI](https://ddialliance.org/products/overview-of-current-products) and other metadata standards.

### Social Sciences and Humanities Open Cloud Reference Ontology
The [Social Sciences and Humanities Open Cloud Reference Ontology (SSHOCro)](https://www.sshopencloud.eu/sshocro) proposes an ontological model and RDF (Resource Description Framework) schema to be used as a top-level ontology for organizing knowledge and information found distributed across various primary sources of information in the Social Sciences and Humanities Open Cloud (SSHOC). It provides a semantic interoperability framework for the description of the data life cycle used by Social Science and Humanities researchers. SSHOCro is modeled as an extension of [CIDOC CRM](https://www.cidoc-crm.org/).

### Statistical Data and Metadata eXchange
As described in the [official site for the Statistical Data and Metadata eXchange (SDMX) community](https://sdmx.org/?page_id=2555/), SDMX is designed to describe statistical data and metadata, normalise their exchange, and improve their efficient sharing across statistical and similar organisations. It provides an integrated approach to facilitating statistical data and metadata exchange, enabling interoperable implementations within and between systems concerned with the exchange, reporting and dissemination of statistical data and their related meta-information.
It consists of technical standards (including the Information Model), statistical guidelines and an IT architecture and tools and is an [ISO standard](http://www.iso.org/iso/catalogue_detail.htm?csnumber=52500).

Many IT tools have been developed to support the use and implementation of SDMX, examples of such tools are the {% tool "sdmx-registry" %}, the {% tool "dsw" %} and the {% tool "sdmx-ri" %}.

