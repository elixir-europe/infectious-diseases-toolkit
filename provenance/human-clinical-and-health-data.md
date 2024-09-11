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

## HL7 FHIR Provenance

[HL7 FHIR](http://hl7.org/fhir/) is an interoperability standard for healthcare information exchange between systems. FHIR aims to define the key entities involved in healthcare information exchange as resources.

FHIR provides support for [expression of provenance](https://www.hl7.org/fhir/provenance.html) information of resources. Provenance of a resource is "a record that describes entities and processes involved in producing and delivering or otherwise influencing that resource", and "tracks information about the activity that created, revised, deleted, or signed a version of a resource, describing the entities and agents involved".

The provenance part of HL7 FHIR extends W3C PROV.
