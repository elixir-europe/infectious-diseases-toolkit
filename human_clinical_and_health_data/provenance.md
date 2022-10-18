---
title: Provenance
description: Tracking data and analysis steps
contributors: [Rudolf Wittner, Stian Soiland-Reyes]
page_id: <!---REPLACE THIS with a shortened page name, with lower case letters and spaces, or an acronym in upper and lower case letters--->
rdmkit: <!---put the name and URL of the relevant link or links to RDMkit for generic guidelines not specific to infectious diseases--->
  - name: <!---the name of the RDMkit page--->
    url: <!---the URL of the RDMkit page--->
related_pages: 
  showcase: [<!---REPLACE THIS with the page IDs of the showcase pages that you want to list here as related pages--->]
  human_biomolecular_data: [<!---REPLACE THIS with the page IDs of the human_biomolecular_data pages that you want to list here as related pages--->]
  human_clinical_and_health_data: [<!---REPLACE THIS with the page IDs of the human_clinical_and_health_data pages that you want to list here as related pages--->]
  social_and_economic_impact: [<!---REPLACE THIS with the page IDs of the social_and_economic_impact pages that you want to list here as related pages--->]
  pathogen_characterisation: [<!---REPLACE THIS with the page IDs of the pathogen_characterisation pages that you want to list here as related pages--->]
training:
  - name:
    registry:
    url:
---

---

## W3C PROV

[W3C PROV](https://www.w3.org/TR/prov-overview/) is a general purpose standard for provenance information. The standard suggest expression of provenance in terms of entities, activities, agents, and their mutual relations. The standard's data model is realized in different serialization, including the [PROV-O ontology](https://www.w3.org/TR/prov-o/), which have been extended for various domains. 

In addition to the [PROV primer](https://www.w3.org/TR/prov-primer/), the [PROV Book](https://www.provbook.org/) gives a detailed introduction to using PROV. 

## HL7 FHIR Provenance

[HL7 FHIR](http://hl7.org/fhir/) is an interoperability standard for healthcare information exchange between systems. FHIR aims to define the key entities involved in healthcare information exchange as resources.

FHIR provides support for [expression of provenance](https://www.hl7.org/fhir/provenance.html) information of resources. Provenance of a resource is "a record that describes entities and processes involved in producing and delivering or otherwise influencing that resource", and "tracks information about the activity that created, revised, deleted, or signed a version of a resource, describing the entities and agents involved".

The provenance part of HL7 FHIR extends W3C PROV. 

## The Common Provenance Model

The aim of the [Common Provenance Model](https://doi.org/10.1038/s41597-022-01537-6) (CPM) is to provide support for integration of provenance information from heterogeneous environments. In particular, it provides guidelines for domain-independent provenance information representation (so called provenance backbone), to which domain specific provenance information can be attach in a prescribed way.

The CPM is an extension of W3C PROV.

The CPM forms a conceptual foundation for an ISO standard series _ISO 23494 Provenance information model for biological specimen and data_. The ISO standard is still in early phases of its development. 

## RO-Crate

[RO-Crate](https://www.researchobject.org/ro-crate) is a lightweight implementation of a _FAIR Digital Object_, which is able to pack data together with its metadata into a _Research Object_. [RO-Crate specifications](https://www.researchobject.org/ro-crate/specification.html) can be used to form different [RO-Crate profiles](https://www.researchobject.org/ro-crate/profiles.html), which are suitable for various domains and use cases. 

RO-Crate is based on Linked Data standards including [schema.org](https://schema.org/) and [JSON-LD](https://json-ld.org/) but can be written and consumed as regular JSON. 


