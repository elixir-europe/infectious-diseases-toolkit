---
title: Human clinical and health data
description: Tracking data and analysis steps.
contributors: [Rudolf Wittner]
page_id: hchd_provenance
redirect_from: /human-clinical-and-health-data/provenance
rdmkit:
  - name: Data provenance
    url: https://rdmkit.elixir-europe.org/data_provenance
training:
  - name: FAIR data and provenance with RO-Crate and Galaxy
    registry:
    url: https://gallantries.github.io/video-library/modules/ro-crate
  - name: Galaxy trainig
    registry:
    url: https://bio.tools/galaxy
  - name: Common Workflow Language (CWL) trainig
    registry:
    url: https://fairsharing.org/FAIRsharing.8y5ayx
  - name: Snakemake trainig
    registry:
    url: https://tess.elixir-europe.org/search?q=Snakemake
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## HL7 FHIR Provenance

[HL7 FHIR](http://hl7.org/fhir/) is an interoperability standard for healthcare information exchange between systems. FHIR aims to define the key entities involved in healthcare information exchange as resources.

FHIR provides support for [expression of provenance](https://www.hl7.org/fhir/provenance.html) information of resources. Provenance of a resource is "a record that describes entities and processes involved in producing and delivering or otherwise influencing that resource", and "tracks information about the activity that created, revised, deleted, or signed a version of a resource, describing the entities and agents involved".

The provenance part of HL7 FHIR extends W3C PROV.

## Relevant tools
* {% tool "galaxy" %}: Open, web-based platform for data intensive biomedical research. Whether on the free public server or your own instance, you can perform, reproduce, and share complete analyses.
* {% tool "common-workflow-language" %}: An open standard for describing workflows that are build from command line tools
* {% tool "snakemake" %}: Snakemake is a framework for data analysis workflow execution
* {% tool "streamflow" %}: Container-native workflow manager for hybrid infrastructures
* {% tool "sapporo-wes" %}: Implementation of Workflow Execution Service (WES) or so-called Workflow-as-a-Service.
* {% tool "compss" %}: COMP Superscalar (COMPSs) is a task-based programming model which aims to ease the development of applications for distributed infrastructures, such as large High-Performance clusters (HPC), clouds and container managed clusters.
