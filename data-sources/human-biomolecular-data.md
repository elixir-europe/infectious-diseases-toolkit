---
title: Human biomolecular data
description: Finding and sharing data for human biomolecular related data sources.
contributors: [Aina Jené Cortada, Arnau Soler Costa]
page_id: hbd_data_sources
redirect_from: /human-biomolecular-data/data-sources
rdmkit:
  - name: Human Data
    url: https://rdmkit.elixir-europe.org/human_data
  - name: Sensitive Data
    url: https://rdmkit.elixir-europe.org/sensitive_data
  - name: Biomolecular simulation data  
    url: https://rdmkit.elixir-europe.org/biomolecular_simulation_data
  - name: Data transfer
    url: https://rdmkit.elixir-europe.org/data_transfer
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

## Introduction

This document aims to serve as a comprehensive resource for anyone interested in the data sources platforms of infectious diseases using human biomolecular data, which have become increasingly important in recent years as a result of advancements in technology and the ever-growing threat of global pandemics. 

By providing this overview of the data sources platforms of infectious diseases using human biomolecular data, this document aims give the user information on where to find these types of data and how to access them (secondary use of the data) and to facilitate the development of new research initiatives and collaborations in the field.


### What is human biomolecular data, and why is it important for infectious diseases research?

Human biomolecular data refers to information obtained from the analysis of biological molecules, such as DNA, RNA, proteins, and metabolites. This type of data is used to study the molecular mechanisms underlying disease and to identify potential drug targets.

Human clinical data, on the other hand, refers to information obtained from the study of patients, including their medical histories, physical exams, and laboratory tests. This type of data is used to diagnose and treat disease, as well as to evaluate the safety and efficacy of new therapies.

While both types of data are important for understanding human health and disease, they are collected and analysed in different ways and for different purposes. 

Human biomolecular data is of great importance in infectious disease research because it plays a critical role in understanding the molecular basis of the disease. By analyzing the biomolecular data, researchers can gain a deeper understanding of the disease's pathogenesis, evolution, and transmission. Personalised medicine is another area where biomolecular data can be applied. By analyzing an individual's biomolecular data, researchers can develop personalised treatment plans that are tailored to the specific needs of the patient. For example, if a patient has a genetic mutation that predisposes them to a particular disease, this information can be used to develop a personalised treatment plan that takes into account the patient's genetic profile.

Furthermore, its significance extends far beyond disease diagnosis and treatment, encompassing a broader scope of applications. For instance, a secondary use of human biomolecular data becomes vital at the population level, facilitating important policy responses during future infectious disease outbreaks. Additionally, investigating the cost-effectiveness of interventions based on these datasets enables optimal resource allocation for the most impactful healthcare strategies. By analyzing this data, we can make well-informed decisions to protect public health in a long term. 

It is important to mention that most analyses of human biomolecular data are complemented by using the clinical data related to them.

<!-- ## Data deposition and FAIRness -->

<!--- Currently in standby waiting to check the clinical data sources FAIRness.--->

<!-- ### Considerations -->

## Data deposition

For advancing in the understanding of human biomolecular data, data deposition plays a pivotal role. The deposition of this data in publicly accessible databases serves as a valuable resource for scientists and researchers worldwide. It enables the integration and analysis of diverse datasets as well as by sharing and archiving data, researchers can ensure the reproducibility and transparency of their findings, allowing others to validate and build upon their work, encouraging collaboration. 
In summary, data deposition not only fuels scientific progress but also empowers the global scientific community to unlock the complexities of human biology, ultimately leading to improved health outcomes and advancements in medical research.

### Considerations

- Choose a reliable and established public database or repository for data deposition.
- Ensure that the data is properly organized, documented, and annotated for easy understanding and interpretation.
- Adhere to data sharing and privacy regulations to protect sensitive information and maintain data confidentiality.
- Include metadata, such as experimental protocols, sample characteristics, and data processing methods, to provide context and facilitate reproducibility.
- Use standardized data formats and ontologies to enhance interoperability and enable integration with other datasets.
- Use metadata standards (such as {% tool "dcat" %}) to describe datasets in data catalogs, publishers increase discoverability and enable applications easily to consume metadata from multiple catalogs. It further enables decentralized publishing of catalogs and facilitates federated dataset search across sites. 
- Include appropriate quality control measures to ensure data accuracy and reliability.
- Consider data anonymization or de-identification techniques to protect the privacy of individuals involved in the study.
- Provide sufficient data access and sharing permissions, specifying any restrictions or limitations, while ensuring compliance with legal and ethical requirements.
- Consider long-term data preservation strategies to ensure the accessibility and availability of the deposited data for future researchers.
- Promote open and collaborative practices by encouraging data citation and acknowledgement to recognize the contributions of the original data creators.

Please note that these considerations are general in nature and may vary depending on the specific requirements and guidelines of the chosen data repository or database.

### Existing approaches

- **Public databases:** Various publicly accessible databases serve as repositories for human biomolecular data, such as the {% tool "ncbi" %} databases (e.g., {% tool "genbank" %}, {% tool "geo" %}, {% tool "sra" %}) and European Bioinformatics Institute ({% tool "ebi" %}) databases (e.g., {% tool "european-nucleotide-archive" %}, {% tool "arrayexpress" %}).
- **Controlled access repositories:** Some data deposition platforms, like dbGaP ({% tool "dbgap" %}) and EGA ({% tool "ega" %}), adopt a controlled access model to protect sensitive human biomolecular data. Researchers interested in accessing the data need to request permission and comply with specific data usage policies.
- **Data integration platforms:** Platforms like the {% tool "ga4gh" %} provide frameworks and standards for federated data access and integration across multiple repositories. These initiatives aim to facilitate the aggregation and analysis of human biomolecular data from diverse sources while maintaining data privacy and security.
- **Data citation and DOI assignment:** To acknowledge and promote the contributions of researchers who deposit human biomolecular data, many repositories assign unique digital object identifiers (DOIs) to datasets. This enables proper citation and recognition of the deposited data, enhancing its visibility and impact.
- **Data submission portals:** Some repositories offer user-friendly web portals or submission systems that guide researchers through the process of depositing human biomolecular data. These portals often provide templates, validation checks, and step-by-step instructions to ensure the completeness and quality of the deposited data.
- **Consortium-specific databases:** Collaborative research initiatives often establish dedicated databases for sharing and depositing human biomolecular data, such as The Cancer Genome Atlas ({% tool "tcga" %}) for cancer genomics data or the Genotype-Tissue Expression ({% tool "gtex" %}) project for gene expression data across different tissues.
- **Standardized data formats:** Commonly used data formats like FASTQ, BAM, and VCF facilitate data deposition and sharing by ensuring compatibility and interoperability between different analysis tools and databases.
- **Data publication:** Journals and publishers increasingly require researchers to deposit their human biomolecular data in public repositories as a prerequisite for publication. This promotes data sharing, reproducibility, and transparency in scientific research.
- **Data sharing platforms:** Online platforms like {% tool "figshare" %}, {% tool "zenodo" %}, and {% tool "dryad" %} provide researchers with the means to deposit and share their human biomolecular data, ensuring its long-term accessibility and enabling collaboration.

## Search and discoverability

**Search and discoverability** are crucial for finding and accessing relevant information, resources, and data related to a specific topic or area of interest. Infectious diseases can evolve rapidly and have significant impacts on public health, making it necessary to monitor and respond to outbreaks effectively. This requires access to up-to-date information on disease prevalence, transmission patterns, and clinical outcomes, which can come from various sources, such as clinical data, biomolecular data, public health reports, and social media.

**Standardised terminology and data formats** are also essential for effective search and discoverability in infectious disease surveillance. The use of common disease codes and data structures can facilitate the integration and analysis of data from multiple sources, making it easier to identify trends and patterns. This can improve the ability to identify emerging disease threats and develop effective disease control measures. See [Data harmonisation](#data-harmonisation) section.

**Biomolecular data sources** can be facilitated through the use of standardised data formats and data sharing platforms, allowing the  development of effective diagnostic and treatment strategies of infectious diseases data. 

Overall, search and discoverability are essential for effective infectious disease surveillance and response. By ensuring that relevant data sources are easily accessible and usable, public health professionals can more effectively monitor and control the spread of infectious diseases, ultimately protecting public health.

### Considerations

Despite the growing amount of infectious disease data stored in various sources, finding and analyzing this data can be challenging for the scientific community. There is a clear need for a user-friendly and efficient way to discover and analyse this data.

- **Data sharing platforms**: Access to data sharing platforms can facilitate the discovery and sharing of biomolecular data related to infectious diseases. Such as the {% tool "covid-19-data-portal" %}.
- **Data privacy and security**: Privacy and security protocols must be in place to protect sensitive biomolecular data from unauthorised access.
- **National regulations**: Taking into account the National regulations and the General Data Protection Regulation ([GDPR](https://gdpr-info.eu/)) rules.
- **Data quality**: High-quality biomolecular data is critical for accurate disease surveillance, diagnosis, and analysis. Efforts should be made to ensure that data quality is maintained throughout the data lifecycle. See [Quality control - Human biomolecular data](/quality-control/human-biomolecular-data) page.
- **Data storage and management**: Proper data storage and management practices must be followed to ensure that biomolecular data is organised and easily accessible to relevant parties.
- **Metadata**: Metadata should be included with biomolecular data to provide context and facilitate search and discoverability.
- **Collaboration**: Collaboration between data producers, curators, and users can promote effective search and discoverability of biomolecular data related to infectious diseases.
- **Data standardization**: Standardised data formats and common disease codes are essential for integrating and analyzing biomolecular data from different sources.

### Existing approaches

Consequently, we have compiled some of the main tools, portals, and data sharing platforms that allow for searching and discovering biomolecular data related to infectious diseases from various sources with the next considerations.

- Beacon: {% tool "beacon" %} is an API (usually extended with a user interface) that allows for data discovery of phenoclinic and biomolecular data. The version 2 (v2) of the Beacon protocol has been accepted as GA4GH standard in Spring 2022. It includes, among other changes:
  - Query options for biological or technical metadata using filters defined through CURIEs (e.g. phenotypes, disease codes, sex or age).
  - An option to trigger the next step in the data access process (e.g. who to contact or which are the data use conditions).
  - An option to jump to another system where the data could be accessed (e.g. if the Beacon is for internal use of the hospital, to provide the Id of the EHR of the patients having the mutation of interest).
  - Annotations about the variants found, among which the expert/clinician conclusion about the pathogenicity of a given mutation in a given individual or its role in producing a given phenotype.
  - Information about cohorts.

  Useful links related to Beacon v2:
  - [Beacon v2 Website](https://beacon-project.io)
  - [Beacon v2 Models](https://docs.genomebeacons.org/models/)
  - [Beacon v2 GitHub](https://github.com/ga4gh-beacon/beacon-v2/)
  - [Beacon v2 GitHub API](https://github.com/EGA-archive/beacon2-ri-api)
  - [Beacon v2 Reference Implementation paper](https://academic.oup.com/bioinformatics/article/38/19/4656/6671215)

  Example of Beacon v2 with synthetic data:
  - [Synthetic data (CINECA)](https://ega-archive.org/studies/EGAS00001002472)
  - [CINECA Beacon v2 API](https://ega-archive.org/beacon-apis/cineca/)
 
 Beacon v2 implementations with COVID-19 data:
<table><thead>
  <tr>
    <th>Beacons</th>
    <th>Viral genomes</th>
    <th>Patient basic data</th>
    <th>Patient rich data</th>
    <th>Patient genomics</th>
    <th>Epidemiological data</th>
  </tr></thead>
<tbody>
  <tr>
    <td>{% tool "crg-covid-19-viral-beacon" %}</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
    <td>–</td>
    <td>–</td>
  </tr>
  <tr>
    <td>{% tool "ega-beacon" %}</td>
    <td>–</td>
    <td>X</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
  </tr>
  <tr>
    <td>COVID-19 NL</td>
    <td>–</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
    <td>–</td>
  </tr>
  <tr>
    <td>{% tool "unott-beacon" %}</td>
    <td>–</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
    <td>–</td>
  </tr>
  <tr>
    <td>{% tool "bento-platform" %}</td>
    <td>X</td>
    <td>X</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
  </tr>
  <tr>
    <td>{% tool "andalusia-beacon" %}</td>
    <td>X</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
    <td>–</td>
  </tr>
  <tr>
    <td>{% tool "covid19-beacon" %}</td>
    <td>X</td>
    <td>X</td>
    <td>–</td>
    <td>–</td>
    <td>X</td>
  </tr>
  <tr>
    <td>{% tool "viral-ai" %}</td>
    <td>X</td>
    <td>–</td>
    <td>–</td>
    <td>–</td>
    <td>–</td>
  </tr>
</tbody></table>

- Biosamples: {% tool "biosamples" %} stores and supplies descriptions and metadata about biological samples used in research and development by academia and industry. For example it stores data from infectious diseases such as COVID-19.
- COVID-19 DataPortal: The {% tool "covid-19-data-portal" %} facilitates data sharing and analysis in order to accelerate coronavirus research and acts as a Data sharing platform. The European COVID-19 Data Platform consists of three connected components:
  - {% tool "sars-cov2-data-hubs" %}, which organise the flow of SARS-CoV-2 outbreak sequence data and provide comprehensive open data sharing for the European and global research communities.
  - {% tool "fega" %}, which provides secure controlled access sharing of sensitive patient and research subject data sets relating to COVID-19 while complying with stringent privacy national laws.
  - {% tool "covid-19-data-portal" %}, which brings together and continuously updates relevant COVID-19 datasets and tools, will host sequence data sharing and will facilitate access to other SARS-CoV-2 resources.

  You can find further information about the Covid-19 Data Portal on [RDMkit](https://rdmkit.elixir-europe.org/covid19_data_portal).

## Data access and transfer

Sharing genetic and molecular information between researchers and institutions is essential for gaining a better understanding of human biology and disease. This is especially important when it comes to infectious diseases. By studying the genetic makeup of pathogens and how they interact with human cells, researchers can identify new targets for treatments and vaccines. They can also develop strategies to prevent or contain potential outbreaks before they occur.

Of course, sharing this kind of sensitive information comes with challenges. Privacy, security, and ethical considerations must be taken into account. Researchers need to handle this information responsibly and with respect for individuals' rights. Legal and regulatory barriers can also impede data sharing and collaboration.

However, the benefits of sharing human biomolecular data outweigh the risks. Access to this data is crucial for scientific progress and medical advancements. It's important for us to continue finding ways to responsibly and securely share this valuable resource. 

### Considerations

When looking for solutions to human biomolecular data access, you should consider the following aspects:

- **Data Security and Privacy:** Prioritize solutions that ensure strict data security and compliance with ethical guidelines, protecting sensitive biomolecular information and adhering to regulatory requirements.
- **Interoperability and Data Sharing:** Choose solutions that seamlessly integrate with existing biomolecular research platforms and data repositories, facilitating secure data sharing and collaboration among researchers.
- **Data Reproducibility and Transparency:** Choose solutions that promote data reproducibility by providing transparent methodologies, making it easier for researchers to validate and build upon previous findings.
- **Data Quality and Standardization:** Verify that the solution provides reliable and accurate data, while supporting data standardization and metadata organization for consistent data exchange and improved research outcomes.
- **Data Integration Capabilities:** Depending on you study, prioritize solutions that can seamlessly integrate diverse biomolecular data types, such as genomics, proteomics, and metabolomics, for comprehensive analysis and insights.
- **Data structure:** Choose a database with a defined data structure, enabling homogeneity of the data and facilitating standardized and consistent data storage, retrieval and usability.
- **Scalability and Performance:** Look for solutions capable of efficiently handling large-scale biomolecular data sets while maintaining optimal performance, supporting advanced analysis tools for meaningful insights.
- **User-Friendly Interface:** Opt for solutions with intuitive interfaces and flexible access controls, enabling researchers of varying technical backgrounds to access, analyze, and interpret data effectively.

When looking for solutions to data transfer, you can check [RDMkit](https://rdmkit.elixir-europe.org/data_transfer).

### Existing approaches

- You can check a list of existing controlled access repositories:
  - {% tool "ega" %}
  - {% tool "estonian-biobank" %}
  - {% tool "dutch-covid19-data-portal" %}
  - {% tool "panther" %} 
  - {% tool "ace-cohort" %}
- You can use one of these standards to make your data use conditions publicly available to possible data requesters.
  - The {% tool "the-data-use-ontology" %} is an international standard, which provides codes to represent data use restrictions for controlled access datasets.
  - The {% tool "ada-m" %} provides a standardised way to unambiguously represent the conditions related to data discovery and access. 
  - By depositing your data to one of the existing controlled access repositories, they will already show the data use conditions (e.g. [EGAD00001007777](https://ega-archive.org/datasets/EGAD00001007777))
- A data access committee (DAC) is a group responsible for reviewing and approving requests for access to sensitive data, such as human biomolecular data. Its role is to ensure that requests are in compliance with relevant laws and regulations, that data is being used for legitimate scientific purposes, and that privacy and security are being maintained. To know more about what is a DAC and how to become one, you can check the [European Genome-phenome Archive - Data Access Committee](https://ega-archive.org/submission/data_access_committee) website.

You can find further information about sharing human data on [RDMkit](https://rdmkit.elixir-europe.org/human_data#sharing-and-reusing-of-human-data).

## Data harmonisation

To ensure that researchers can effectively utilise data, it is essential that it be collected and stored in a standardised manner. Using standardised formats and databases facilitates data sharing across research groups, enabling more efficient and effective analysis. This approach not only saves time, but also yields more accurate results.

Thanks to the Sars-CoV-2 outbreak, the scientific community has established standards, schemes, and data models with controlled vocabularies and ontologies explained in detail in the Human Clinical and Health Data section. One example could be the [Developing a standardized but extendable framework to increase the findability of infectious disease datasets](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9950378/) paper from February of 2023.

### Considerations

- Looking for an existing standardised metadata schema for human biomolecular data, like {% tool "miabis" %} or [EGA](https://ega-archive.org/submission/sequence/programmatic_submissions) schemas. 
- Incorporating key data elements such as patient demographics, clinical features, and laboratory test results in the metadata schema
- Ensuring interoperability with other existing metadata schemas to facilitate data sharing and integration
- Including metadata fields for sample collection, processing, and storage information to ensure data quality and reproducibility
- Implementing controlled vocabularies and ontologies for standardised annotation and data integration
- Enabling data harmonisation across different studies to facilitate meta-analyses and systematic reviews
- Seek input and feedback from stakeholders across the research and public health communities to ensure that the schema meets the needs of diverse users and supports a range of research questions and applications.
- Regularly updating and refining the metadata schema to accommodate new data types and emerging research needs.

### Existing approaches

* When looking for solutions to standards, schemas, ontologies and vocabularies, you can check [the RDMkit](https://rdmkit.elixir-europe.org/metadata_management#how-do-you-find-appropriate-standard-metadata-for-datasets-or-samples) for documentation.
* {% tool "fairsharing" %} is also a good resource to find metadata standards that can be useful for your research.

