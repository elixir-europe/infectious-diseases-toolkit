---
title: Provenance
description: Tracking data and analysis steps
---

W3C PROV

W3C PROV [1] is a general purpose standard for provenance information. The standard suggest expression of provenance in terms of entities, activities, agents, and their mutual relations. The standard's data model is built on the top of the PROV-O ontology, which can be extended for various domains. 

[1] https://www.w3.org/TR/prov-overview/

HL7 FHIR Provenance

HL7 FHIR is an interoperability standard for healthcare information exchange between systems. FHIR aims to define the key entities involved in healthcare information exchange as resources. [1]

FHIR provides support for expression of provenance information of resources. Provenance of a resource is "a record that describes entities and processes involved in producing and delivering or otherwise influencing that resource" [2], and "tracks information about the activity that created, revised, deleted, or signed a version of a resource, describing the entities and agents involved" [2].

HL7 FHIR is an extension of W3C PROV. 

[1] D. Bender and K. Sartipi, "HL7 FHIR: An Agile and RESTful approach to healthcare information exchange," Proceedings of the 26th IEEE International Symposium on Computer-Based Medical Systems, 2013, pp. 326-331, doi: 10.1109/CBMS.2013.6627810.

[2] https://www.hl7.org/fhir/provenance.html

The Common Provenance Model

The aim of the Common Provenance Model (CPM) [1] is to provide support for integration of provenance information from heterogeneous environments. In particular, it provides guidelines for domain-independent provenance information representation (so called provenance backbone), to which domain specific provenance information can be attach in a prescribed way.

The CPM is and extension of W3C PROV.

The CPM forms a conceptual foundation for an ISO standard series "ISO 23494 Provenance information model for biological specimen and data". The ISO standard is still in early phases of its development. 

[1] Wittner, R., Mascia, C., Gallo, M. et al. Lightweight Distributed Provenance Model for Complex Real–world Environments. Sci Data 9, 503 (2022). https://doi.org/10.1038/s41597-022-01537-6

RO Crate

RO Crate is an implementation of a FAIR digital object, which is able to pack data together with its metadata [1]. RO Crate specification can be used to define various RO Crate profiles, which are suitable for various domains and use cases. 

[TODO Link to applicable RO Crate profiles specifications. ]

[1] https://www.researchobject.org/ro-crate/![image](https://user-images.githubusercontent.com/45092709/196181800-4c05ff34-64a0-453b-ab01-9c7ee808f606.png)
