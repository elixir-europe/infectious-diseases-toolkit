---
title: Human clinical and health data
description: Tracking data and analysis steps.
contributors: [Rudolf Wittner, Stian Soiland-Reyes, Simone Leo]
page_id: hchd_provenance
redirect_from: /human-clinical-and-health-data/provenance
rdmkit:
  - name: Data provenance
    url: https://rdmkit.elixir-europe.org/data_provenance
training:
 - name: FAIR data and provenance with RO-Crate and Galaxy
    registry:
    url: https://gallantries.github.io/video-library/modules/ro-crate
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## W3C PROV

[W3C PROV](https://www.w3.org/TR/prov-overview/) is a general purpose standard for provenance information. The standard suggests expression of provenance in terms of entities, activities, agents, and their mutual relations. The standard's data model is realized in different serializations, including the [PROV-O ontology](https://www.w3.org/TR/prov-o/), which have been extended for various domains.

In addition to the [PROV primer](https://www.w3.org/TR/prov-primer/), the [PROV Book](https://www.provbook.org/) gives a detailed introduction to using PROV.

## HL7 FHIR Provenance

[HL7 FHIR](http://hl7.org/fhir/) is an interoperability standard for healthcare information exchange between systems. FHIR aims to define the key entities involved in healthcare information exchange as resources.

FHIR provides support for [expression of provenance](https://www.hl7.org/fhir/provenance.html) information of resources. Provenance of a resource is "a record that describes entities and processes involved in producing and delivering or otherwise influencing that resource", and "tracks information about the activity that created, revised, deleted, or signed a version of a resource, describing the entities and agents involved".

The provenance part of HL7 FHIR extends W3C PROV.

## The Common Provenance Model

The [Common Provenance Model](https://doi.org/10.1038/s41597-022-01537-6) (CPM) is an extension of W3C PROV that aims to provide support for the integration of provenance information from heterogeneous environments. In particular, it provides guidelines for the representation of domain-independent provenance information (provenance _backbone_), to which domain-specific provenance information can be attached in a prescribed way.

The CPM forms a conceptual foundation for the ISO standard series _ISO 23494 Provenance information model for biological specimen and data_. The ISO standard is still in an early phase of its development.

## RO-Crate

{% tool "research-object-crate" %} is a lightweight implementation of a _FAIR Digital Object_, which is able to pack data together with its metadata into a _Research Object_. It is based on Linked Data standards including {% tool "schema-org" %} and [JSON-LD](https://json-ld.org/), but can be written and consumed as regular JSON.

The [RO-Crate specifications](https://www.researchobject.org/ro-crate/specification.html) can be used to form different [RO-Crate profiles](https://www.researchobject.org/ro-crate/profiles.html), which are suitable for various domains and use cases. While the base specifications already contain some [guidelines on representing the provenance of data entities](https://www.researchobject.org/ro-crate/1.1/provenance.html#software-used-to-create-files) included in the crate, some contexts require a more detailed description to enhance traceability and reproducibility. To meet this demand, several provenance-oriented RO-Crate profiles are being developed:

* The [Workflow Run RO-Crate working group](https://www.researchobject.org/workflow-run-crate/) is developing a collection of [profiles to describe the execution of computational workflows](https://www.researchobject.org/workflow-run-crate/profiles/). The profiles define provenance descriptions at different granularity levels, from "black box" (only workflow-level inputs, outputs and parameters are considered) to step-by-step rundown.

* The CPM team, with the help of the RO-Crate community, is developing an RO-Crate profile for representing CPM-compliant provenance and meta-provenance in an RO-Crate.

Support for RO-Crate provenance reporting is being added or is planned to be added to several workflow engines, including {% tool "galaxy" %}, {% tool "common-workflow-language" %}, {% tool "snakemake" %}, {% tool "streamflow" %}, {% tool "sapporo-wes" %}, {% tool "compss" %}, {% tool "wfexs" %}.
