---
title: General Guidelines - Provenance
description: General considerations and approaches related to provenance
contributors: [Rudolf Wittner, Stian Soiland-Reyes, Simone Leo, Mari Kleemola, Simone Sacchi, Diana Pilvar, Irena Vipavc Brvar, Robin Navest]
page_id: <!---TODO--->
redirect_from: <!---TODO--->
rdmkit:
  - name: Data provenance
    url: https://rdmkit.elixir-europe.org/data_provenance
training:
  - name: FAIR data and provenance with RO-Crate and Galaxy
    registry:
    url: https://gallantries.github.io/video-library/modules/ro-crate
  - name: BBMRI.QM TRAINING ISO/TS 23494-1:2023 “BIOTECHNOLOGY – PROVENANCE INFORMATION MODEL FOR BIOLOGICAL MATERIAL AND DATA”
    url: https://www.bbmri-eric.eu/services/bbmri-qm-iso-23494-1-2023/ 
  - name: Provenance training
    registry: TeSS
    url: https://tess.elixir-europe.org/search?q=provenance
faircookbook:
  - name: Provenance information
  - url: https://w3id.org/faircookbook/FCB036
fairsharing:
  - name: Relationship graphs
    url: https://fairsharing.gitbook.io/fairsharing/about-our-records/relation-graphs
  - name: ISO 23494
    url: https://fairsharing.org/FAIRsharing.ce6e9d 
  - name: W3C Provenance Data Model
    url: https://fairsharing.org/FAIRsharing.36c7ea 
  - name: Research Object Crate (RO-Crate)
    url: https://fairsharing.org/FAIRsharing.wUoZKE 
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction
*“Provenance is a record that describes the people, institutions, entities, and activities involved in producing, influencing, or delivering a piece of data or a thing"*. Depending on the actual content of provenance, it can be used for various purposes, such as to reproduce documented processes, or to assess the quality or fitness-for-purpose of documented objects, which may include, for example, biological samples or data. Examples of provenance may include information about how the data was produced, where, when, and by whom the data was collected, and how the data has been processed. Provenance information can be modelled and encoded according to different schemas [see existing approaches].

Provenance is typically realised as metadata of a documented object, such as a dataset. When discussing provenance, it is important to clarify what exactly is meant by the term “provenance” in a particular scenario or a use case. For instance, whether provenance is part of metadata, whether descriptive metadata (such as sample storage temperature) is included in provenance, what actual information is stored in provenance, etc. This is especially difficult when discussing provenance across different domains, where the  understanding and the usage of the term “provenance” may differ. This page uses the term to refer to the general concept without any presumption about what specific information is recorded in provenance. This may be specified in the domain-specific provenance pages. 

## Good practices for provenance information
### Considerations
1. **Purpose**. Provenance collection should serve a pre-defined purpose. Without a defined purpose for provenance collection, it is not possible to determine what provenance information must be collected to serve a specific use case. 
* a. **Backward traceability** of documented objects is **the most crucial purpose** of provenance collection, as it is a prerequisite for any other purposes. For instance, we can not assess the quality of a dataset without being able to trace back from what other objects and how the dataset was generated.
2. **Interoperability**. Generated provenance information should be interoperable with provenance coming from other sources, to enable its **automated** processing. This is particularly important in settings where objects described by provenance can be combined or shared (between organisations). The interoperability should be achieved on both semantic and syntactic levels. The Common Provenance Model (see Existing approaches) serves as a glue to integrate domain specific provenance standards.
3. **Trustworthiness**. The generated provenance information must be trustworthy so others can make decisions using the information stored in provenance. The level of required trustworthiness is dependent on the purpose, for which provenance is used. 
4. **Confidentiality & privacy**. Provenance may contain any non-public or sensitive information. It would be possible for the provenance to contain e.g. location and time of data acquisition and (contact) information about the principal investigator of a study. For that purpose, confidentiality of provenance must be addressed and the privacy of the subjects must be protected.

Common purposes for provenance collection include:
1. **Traceability**. The ability to trace back the history of the documented object.
2. **Reproducibility**. The ability to reproduce the same or similar results using the same or similar setup of the process. See [the PRIMAD model](https://doi.org/10.4230/DagRep.6.1.108) for a more detailed description of reproducibility.
3. **Quality and fitness-for-purpose assessment**. The ability to assess quality and fitness-for-purpose of a documented object. This is especially important for objects used as an input for studies, as these inputs affect the quality of the study results.
4. **Copyright and licensing**. For data reuse, the copyright and/or licensing agreements affecting the dataset can be recorded in provenance. This allows researchers to determine whether this dataset can be used regardless of the purpose. Consider whether data sources are subject to any copyright and/or licensing agreement affecting their reuse in an original dataset. Information about licences and terms of use can be added to the provenance information.
5. **Terms & conditions** under which the dataset can be used can be mentioned under provenance.
## Existing approaches
### W3C PROV
[W3C PROV](https://www.w3.org/TR/prov-overview/) is a general purpose standard for provenance information. The standard suggests expression of provenance in terms of entities, activities, agents, and their mutual relations. The standard’s data model is realised in different serialisations, including the [PROV-O ontology](https://www.w3.org/TR/prov-o/), which have been extended for various domains.
In addition to the [PROV primer](https://www.w3.org/TR/prov-primer/) and the [PROV Book](https://www.provbook.org/) gives a detailed introduction to using PROV.
There are currently two major implementations for handling the data model: Java implementation ({% tool "provtoolbox" %}) and Python implementation ({% tool "provpython %}).

### The Common Provenance Model
The [Common Provenance Model](https://doi.org/10.1038/s41597-022-01537-6) (CPM) is an extension of W3C PROV that aims to provide advanced support for the integration of provenance information from heterogeneous multi-organizational environments,, where documented objects pass through several organisations. This may include, for instance, a scenario where a sample is acquired and processed in a clinical environment, passed to a biobank for storage, used as an input to generate data (eg, omics or image data) in a laboratory, and these data is later processed in computational infrastructures (e.g. to train AI models). In particular, it provides guidelines for the representation of domain-independent provenance information, to which domain-specific provenance information can be attached in a prescribed way.
The latest publicly available version of the CPM is available in the BY-COVID project’s [provenance deliverable](https://zenodo.org/records/10927253). The idea behind the common provenance model is described in [a publication](https://doi.org/10.1038/s41597-022-01537-6).
The CPM forms a conceptual foundation for the ISO 23494 provenance standard series. 

### ISO 23494 provenance standard series
The ISO 23494 Provenance information model for biological material and data is a provenance standard series defines: 1) general requirements on provenance information management; 2) the usage of the CPM to achieve interoperability of provenance; 3) provenance model for biological material and data.; 
The first part of the standard series, *ISO 23494-1 Biotechnology — [Provenance information model for biological material and data – Part 1: Design concepts and general requirements](https://www.iso.org/standard/80715.html)*, has been already published as a technical specification, and it is currently being revised and promoted to an international standard (publication anticipated in 2026). The ISO international standards enable organisations to be accredited that they follow the requirements specified in the standard. 
The other parts of the standard series have not been published yet. Anticipated release of the second part of the standard series, [*ISO 23494-2 Biotechnology — Provenance information model for biological material and data – Part 2: Common Provenance Model*](https://www.iso.org/standard/87714.html), is anticipated to be published as an international standard in 2026. The standard will enable accreditation of devices and SW to be accredited for providing provenance information in an interoperable manner.
[*ISO 23494-3 Biotechnology — Provenance information model for biological material and data Part 3: Provenance of Biological Material*](https://www.iso.org/standard/89236.html) is the third part of the series, currently under development. It aims to provide standardised terminology for provenance information documenting biological material handling. 
Further information about the standard series and about other parts of the standard series are described in a publication called [Toward a common standard for data and specimen provenance in life sciences](https://doi.org/10.1002/lrh2.10365).

### RO-Crate
{% tool "research-object-crate" %} is a lightweight implementation of a *FAIR Digital Object*, which is able to pack data together with its metadata into a Research Object. It is based on Linked Data standards including {% tool "schema-org" %} and [JSON-LD](https://json-ld.org/), but can be written and consumed as regular JSON.
The [RO-Crate specifications](https://www.researchobject.org/ro-crate/specification.html) can be used to form different [RO-Crate profiles](https://www.researchobject.org/ro-crate/profiles.html), which are suitable for various domains and use cases. While the base specifications already contain [some guidelines on representing the provenance of data entities](https://www.researchobject.org/ro-crate/1.1/provenance.html#software-used-to-create-files) included in the crate, some contexts require a more detailed description to enhance traceability and reproducibility. To meet this demand, several provenance-oriented RO-Crate profiles are being developed:
The [Workflow Run RO-Crate working group](https://www.researchobject.org/workflow-run-crate/) is developing a collection of [profiles to describe the execution of computational workflows](https://www.researchobject.org/workflow-run-crate/profiles/). The profiles define provenance descriptions at different granularity levels, from “black box” (only workflow-level inputs, outputs and parameters are considered) to step-by-step rundown.


The CPM team, with the help of the RO-Crate community, is developing an RO-Crate profile for representing CPM-compliant provenance and meta-provenance in an RO-Crate. This work is anticipated to serve as a groundwork for part 5 of the ISO 23494 provenance standard series,  *ISO 23494-5 Biotechnology — Provenance information model for biological material and data – Part 5:Provenance of Data Processing.*
Support for RO-Crate provenance reporting is being added or is planned to be added to several workflow engines, including {% tool "galaxy" %}, {% tool "common-workflow-language" %}, {% tool "snakemake" %}, {% tool "streamflow" %}, {% tool "sapporo-wes" %}, {% tool "compss" %}, {% tool "wfexs" %}.

### Dataverse provenance
*“The Dataverse Project is an open source web application to share, preserve, cite, explore, and analyze research data”*. Inclusion of provenance information in Dataverse is described on [this webpage](https://guides.dataverse.org/en/5.6/user/dataset-management.html). Dataverse requires JSON format with W3C standards. Provenance capture tools like provR, RDataTracker, NoWorkFlow, recordr, or CamFlow could be used to create this provenance information.

## More relevant tools
* {% tool "openprovenance" %}: Set of user-friendly web applications for storing, validating, and translating W3C PROV-based provenance representations.
* {% tool "provenance-storage" %}: A prototype of a provenance management service implementing the CPM (ISO 23494-2).
* {% tool "provr" %}: Collect meta-data from scripts written in the R programming language.
* {% tool "rdatatracker" %}: An R library to collect provenance from R scripts.
* {% tool "noworkflow" %}: The noWorkflow project aims at allowing scientists to benefit from provenance data analysis even when they don't use a workflow system.
* {% tool "recordr" %}: Provenance tracking for R.
* {% tool "camflow" %}: CamFlow is a Linux Security Module (LSM) designed to capture data provenance for the purpose of system audit.
