---
title: Pathogen characterisation
description: Finding and sharing data for pathogen characterisation related data sources.
contributors: [Cillian De Gascun, Isabel Cuesta, Sarai Varona, Paula Mölling, Abeer Fadda, Dilza Campos, Aída Moure Fernández, Andreas Scherer]
no_robots: true
search_exclude: true
sitemap: false
page_id: pc_data_sources
rdmkit:
  - name:
    url:
training:
  - name:
    registry:
    url:
# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

**We are still working on the content for this page.** If you are interested in adding to the page, then:

[Feel free to contribute](/contribute/){: class="btn btn-primary btn-lg rounded-pill"}

This is a community-driven website, so contributions are welcome! You will, of course, be listed as a contributor on the page.

New content is announced on the [home page](/) and [news page](/about/news), so please check for updates there. You can also watch for changes on this page by using a free service like [Visual Ping](https://visualping.io/) or [Distill Web Monitor](https://distill.io/), or by using a [browser add-on](https://chrome.google.com/webstore/detail/distill-web-monitor/inlikjemeeknofckkjolnjbpehgadgge?hl=en).

<!--- In the context of BY-COVID, a data source can a repository which should include at least the metadata and ideally the data, that might not be directly available when considering sensitive data. Also, repositories should have the capacity to share this data and therefore have a governance model in place on how to do it. It can also include registries of data sources important for the field, with a direct link to the original data sources to be able to request access to the data. --->

## Introduction

Pathogen data is central to understanding, monitoring, and combating infectious diseases. It encompasses a wide range of information, including the identity, genomic features, antimicrobial resistance profiles, and epidemiological patterns of pathogens. The availability and appropriate use of pathogen data can enhance outbreak response, guide public health interventions, and support the development of diagnostics, treatments, and vaccines.

This section of the toolkit brings together key resources that support the sharing, access, and interpretation of pathogen-related data, especially in the context of public health and infectious diseases research.

## What is pathogen characterisation data, and why is it important for infectious diseases research?

Pathogen data refers to any type of data that describes microorganisms (bacteria, viruses, fungi, and parasites) that cause disease. This can include genomic sequences, phenotypic traits, resistance profiles, geographic spread, host interactions, and much more.

For infectious diseases research, pathogen data is essential to:

-	Detect and characterize emerging or re-emerging pathogens.
-	Monitor transmission dynamics and outbreak evolution.
-	Track antimicrobial resistance (AMR) patterns.
-	Develop targeted therapeutics and vaccines.
-	Inform public health responses at local, national, and global scales.

The quality, interoperability, and timely availability of pathogen data directly impact our ability to respond effectively to infectious disease threats.

## Pathogen data sources

Pathogen data sources include platforms, initiatives and projects that collect, standardize, and disseminate information on pathogens, often in the context of surveillance, outbreak response, and research. These resources vary in scope—some are global in nature while others focus on specific regions, pathogens, or types of data (e.g., genomic or phenotypic).

Below is a selection of key initiatives and platforms.

### Considerations

-	**Nature of the resources**: Pathogen data sources are typically community-driven initiatives, infrastructures, or consortia designed to collect, standardise, and share data across regions, institutions, and disciplines. Their scope may be global or regional, pathogen-specific or cross-cutting, and they often focus on genomic, phenotypic, or surveillance data.
-	**Sustainability and continuity**: Many of these platforms are project-based and depend on time-limited funding, which affects long-term data availability, maintenance, and user support. Sustainability planning is critical to preserve tools, datasets, and standards beyond the project's lifetime.
-	**Role in standardisation and integration**: These initiatives often lead the development of guidelines, metadata standards, and ontologies, ensuring that pathogen data is interoperable across systems. They are key to aligning practices across sectors (e.g. human, animal, and environmental health) and enabling cross-border data exchange.
-	**Enabling interoperability and reuse**: By providing shared infrastructure and community-agreed protocols, pathogen data sources allow for integration of diverse datasets—genomic, clinical, epidemiological—supporting complex analyses such as outbreak tracking or resistance monitoring.
-	**Community building and responsiveness**: These efforts foster collaboration, training, and equitable participation across countries and settings. During health emergencies, they often scale up or adapt to new challenges, playing a critical role in rapid data mobilisation.

### Existing approaches

{% tool "ispn" %}: Brings together experts in pathogen genomics to support global coordination, best practices, and innovation in sequencing-based surveillance.

{% tool "ecdc" %}: Provides data and technical support for pathogen surveillance and genomic epidemiology in Europe, including platforms like EpiPulse and TESSy.

{% tool "gmi" %}: Promotes global collaboration for sharing genomic and metadata from pathogens to improve outbreak detection and response.

{% tool "pdn" %}: A European collaboration to enhance interoperability and integration of pathogen data across sectors, with a focus on One Health.

{% tool "eu-wish" %}: Supports surveillance of pathogens through wastewater, providing early-warning indicators for public health threats.

{% tool "elixir-pathogen-fg" %}: Coordinates efforts across ELIXIR nodes to enhance bioinformatics services and standards for pathogen data in Europe.

{% tool "by-covid" %} (not active): Developed tools for accessing and integrating COVID-19-related data across domains during the pandemic.

{% tool "elixir-converge" %} (not active): Contributed to building FAIR data infrastructure, including components for infectious disease research.

{% tool "veo-aurora" %}: Focused on developing data integration and analytical pipelines for emerging viral threats.

{% tool "cog-uk" %} (not active): Delivered large-scale sequencing and analysis of SARS-CoV-2 in the UK, and informed real-time public health actions.

## Genomic data sources for research and public health

Genomic data sources are repositories or platforms that store and provide access to pathogens’ genomic sequences and associated metadata. Accessible genomic data underpins outbreak investigations, surveillance of antimicrobial resistance, and the development of diagnostics, treatments, and vaccines. For researchers, access to curated and high-quality pathogen data enables comparative genomics, phylogenetic studies, and the identification of genetic markers relevant to virulence or host adaptation. For public health, real-time genomic surveillance allows for early detection of emerging threats, tracking of variants of concern (e.g., SARS-CoV-2, influenza), and informed decision-making during epidemics and pandemics.

Ensuring that genomic data is openly available and shared following the FAIR principles (Findable, Accessible, Interoperable, and Reusable) is critical to maximize its impact. When data is FAIR, it can be easily discovered, accessed, and used by researchers and public health authorities around the world, fostering collaboration, transparency, and rapid responses to infectious disease threats.

### Considerations

When working with genomic data sources in the context of infectious diseases and pathogen data, the following specific considerations should be taken into account:

- Timeliness and rapid data sharing
  - Infectious disease outbreaks demand near real-time access to genomic data to enable early detection and rapid response.
- Data standardisation and harmonisation
  - Metadata (e.g. sample collection date, location, host, sequencing method) must follow consistent standards to allow meaningful comparison across studies and regions.
  - Use of standard ontologies to make metadata interoperable.
- Contextual metadata integration
  - Epidemiological, clinical, and environmental metadata should be integrated with genomic data to support robust pathogen characterisation and transmission analysis.
  - Incomplete or missing metadata significantly limits the utility of the sequence data.
- Ethical and legal considerations
  - Human-associated pathogen data may include sensitive information (e.g. host origin or location) potentially requiring host genome removal pre-processing.
  - Equity in data sharing should be promoted to avoid exploitation of low-resource settings.
- Access to raw data
  - The diversity of analysis tools and quality thresholds can lead to inconsistent processing and interpretation of genomic data.
  - Consensus genome sequences may not capture minority variants relevant for resistance or virulence.
  - Providing access to raw sequencing data (with host reads removed when appropriate) is crucial to ensure transparency, reproducibility, and reanalysis with updated methods or in new outbreak contexts.

### Existing approaches

- **General nucleotide sequence repositories**
  - {% tool "european-nucleotide-archive" %}, provides access to raw and assembled nucleotide sequence data across all domains of life.
  - {% tool "ncbi" %}, a comprehensive platform for sequence data and biological information.
  - {% tool "genbank" %} – A core component of NCBI for annotated nucleotide sequences.
- **Repositories focused on pathogen genomics and public health surveillance**
  - {% tool "gisaid" %} – A global initiative for sharing influenza and SARS-CoV-2 genomic data with rich metadata and contributor agreements.
  - {% tool "pathogen-data-portal" %} – Access point for pathogen data from the European COVID-19 Data Platform.
  - {% tool "bv-brc" %}, integrating tools and curated pathogen genomic datasets.
- **Typing and population genomics platforms**
  - {% tool "pubmlst" %} – Curated multilocus sequence typing databases for multiple pathogens.
  - {% tool "bigsdb" %} – Bacterial Isolate Genome Sequence Database for microbial population structure and typing
  - {% tool "enterobase" %} – Platform for genome-based analyses of enteric bacteria like Salmonella, Escherichia, and Clostridioides.
- **Genomic epidemiology and outbreak tracking platforms**
  - {% tool "pathogenwatch" %} – Tool for real-time genomic surveillance and antimicrobial resistance prediction.
  - {% tool "nextstrain" %} – Real-time tracking of pathogen evolution with visualisations and phylogenetic trees.
  - {% tool "outbreak-info" %} – COVID-19-focused dashboard combining genomic, epidemiological, and variant data.
- **Antimicrobial resistance repositories**
  - {% tool "card" %} – Curated resource of resistance genes, their molecular mechanisms, and associated antibiotics. Widely used for annotation and predictive bioinformatics.
  - {% tool "resfinder" %} – Web-based tool and database to identify acquired AMR genes in bacterial genomes from NGS data.
  - {% tool "abricate" %} - Mass screening of contigs for antimicrobial resistance or virulence genes. It comes bundled with multiple databases: NCBI, CARD, ARG-ANNOT, Resfinder, MEGARES, EcOH, PlasmidFinder, Ecoli_VF and VFDB. https://bio.tools/ABRicate
  - {% tool "deeparg" %} - A deep learning based approach to predict Antibiotic Resistance Genes (ARGs) from metagenomes.

## Public Health data sources

Public health data are typically collated, analysed, and published by national and international organisations to inform national and regional health policies, such as targeted surveillance or immunisation campaigns.  In the context of infectious diseases, data are typically collated for an established list of notifiable or priority pathogens.

Infections may be notified to public health bodies by treating clinicians or diagnostic laboratories: in addition, some pathogens, such as influenza, may be the subject of targeted or sentinel surveillance programmes to monitor vaccine effectiveness at the regional and global level.

In order to effectively inform policy, public health data ideally should be available in as near to real time as possible: however, this can be challenging with large data sets or infections that are very common.  In such situations, rather than attempt to capture all cases of a particular infection, the focus instead is on the burden of disease, typically including hospitalisation attendance rates, hospital and intensive care admission rates, and mortality rates.

The publication and sharing of these data is essential to allow for comparison of disease severity across jurisdictions, potentially providing an early warning-type system to international neighbours, as was seen with novel SARS-CoV-2 variants (of concern) during the recent pandemic.

### Considerations

- Pathogens to be notified
- Pathogen associated data to be gathered
- Case definition
- Diagnostic technique (screening/confirmatory)
- Requirement for sequencing
- Patient demographic data required
- Clinical data required
- Outcome of infection
- Data sharing/publication
- Data storage

### Existing approaches

Public health data are typically collated by local or national public health organisations in the first instance, and subsequently shared with regional/international bodies for wider dissemination.  Some of the most well established and recognisable international bodies are listed below.

- {% tool "epipulse" %}: EpiPulse is an online portal for European public health authorities and partner organisations to collect, analyse, share, and discuss infectious disease data for threat detection, monitoring, risk assessment and outbreak response.
- The European Surveillance System (TESSy)
- Early Warning and Response System of the EU (EWRS)
- WHO
- Global Influenza Surveillance and Response System (GISRS)
- Global Health Observatory
- Centers for Disease Control and Prevention (CDC)
- African CDC
- UK Health and Security Agency (UKHSA)

## Public Health data: priority pathogens lists

In addition to the notifiable infections mentioned above, some pathogens may also be designated as priority pathogens on account of their risk to public health at a regional or global level. Typically these pathogens cause a significant risk to public health due to the lack of effective vaccines or therapeutic agents. The designation as a priority pathogen is intended to guide research, development, and prevention strategies that might not otherwise be supported. An example of such a programme is the World Health Organisation’s Bacterial Pathogens Priority List, which aims to tackle the problem of antimicrobial resistance (AMR).

### Considerations

- Who prioritizes
- Prioritization criteria
- Benefits of prioritisation
- What changes with prioritisation
- What do countries have to do
- Who funds additional investment/workload 

### Existing approaches

- WHO Bacterial Pathogens Priority List
- WHO List of Pathogens with Epidemic and PHEIC Potential
- UKHSA Priority Pathogen Families Reference Tool
- CEPI (Coalition for Epidemic Preparedness Innovations) Priority Pathogens List

| Organization                                             | Acronym   | Institutional Link                                                    |
|----------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| World Organization for Animal Health                     | WOAH      | https://www.woah.org/en/home/                                         |
| National Institute of Allergy and Infectious Diseases    | NIAID     | https://www.niaid.nih.gov/                                            |
| European Center for Disease Prevention and Control       | ECDC      | https://www.ecdc.europa.eu/en                                         |
| World Health Organization                                | WHO       | https://www.who.int/                                                  |
| Africa Centers for Disease Control and Prevention        | AFRICACDC | https://africacdc.org/                                                |
| Centers for Disease Control and Prevention               | CDC       | https://www.cdc.gov/                                                  |
| Food and Agriculture Organization for the United Nations | FAO       | https://www.fao.org/home/en/                                          |
| European Food Safety Authority                           | EFSA      | https://www.efsa.europa.eu/en                                         |
| EU Wastewater Observatory for Public Health              | EU4S-DEEP | https://wastewater-observatory.jrc.ec.europa.eu/#/                    |
| UK Health Security Agency                                | UKHSA     | https://www.gov.uk/government/organisations/uk-health-security-agency |
