---
title: SARS-CoV-2 sequencing in Estonia 2021-2022
contributors: [Diana Pilvar, Hedi Peterson]
description: Full-genomic sequencing and analysis of SARS-CoV-2 strains in Estonia during 2021-2022.
affiliations: [University of Tartu, Republic of Estonia Health Board]
page_id: korogenoest 
---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style_guide when writing the content of this page. -->

<!--- Showcase pages should detail a particular combination of standards and tools from an infrastructural or domain perspective to tackle infectious diseases related data challenges. --->

## Introduction 

<!--- In this section you should provide a brief overview of the context that makes Showcase necessary. It is useful to mention the projects under which the showcase was created, the involved research infrastructures, and the disease it is meant to tackle --->
Sequencing initiatives in Estonia began in September 2020. The KoroGeno-EST-3 and KoroGeno-EST-2022 projects took over the sequencing activities in May 2021, and their work concluded at the end of 2022. Here, we describe the workflow of samples and data employed by the [KoroGeno-EST-3 and KoroGeno-EST-2022 projects](https://kliinilinemeditsiin.ut.ee/et/sisu/eesti-sars-cov-2-taisgenoomide-jarjestamine-ja-analuus-korogeno-est-1est-2est-3) .



## Who is the KoroGeno-Est showcase intended for?

<!--- In this section you should provide a brief account of the target audience or intended users for the showcase --->
This showcase provides a high-level overview of the full workflow that was used to monitor the SARS-CoV-2 situation in Estonia by sequencing a proportion of positive PCR samples in the country. The showcase could be beneficial for a general overview but also trigger potential contact with research groups or health boards that need to set up their automatic data handling and sequencing pipelines.

## SARS-CoV-2 sequencing in Estonia (KoroGeno-Est)

**(Illustration goes here)**

**Figure caption:** The figure illustrates major analysis steps carried out in Estonia to sequence and analyse SARS-CoV-2 PCR positive samples.

In Estonia the SARS-CoV-2 sequencing was carried out in collaboration with the SYNLAB Eesti, Health Board Estonia and University of Tartu. The Synlab provided information on the basic sample metadata and PCR outcome, Health Board provided sample metadata on e.g. age, gender, county, vaccination information. 

The central data storage was at GitLab instance at the University of Tartu. The University of Tartu research groups merged the data, created plate information files for sequencing, collecting the sequencing results, generated custom reports, interactive dashboards and brokered data to ENA. In addition to data sequenced in Estonia, also data from ECDC was analysed in similar manner to provide accurate overview of the situation.

#### The aim of KoroGeno-EST
The aim of KoroGeno-EST-3 and KoroGeno-EST-2022 (hereafter, Study) studies was to sequence and conduct molecular-epidemiology analysis for more than 15 000 SARS-CoV-2 full genomes from 1 May to 31 December 2022 in Estonia. The number of weekly sequenced strains depended directly on the epidemiological situation, including the number of newly diagnosed SARS-CoV-2 cases, as well as the need to monitor clinically, demographically, or mutationally significant strains. 

Based on the sequenced samples, weekly reports were prepared for the Republic of Estonia Health Board (hereafter, Health Board (HB)) and "[European Centre for Disease Prevention and Control (ECDC)](https://www.ecdc.europa.eu/en)". In collaboration with the HB, SARS-CoV-2 genomic data was used to analyze infection clusters to trace newly infected subjects. 

In addition, the study identified the prevalence of variants associated with higher pathogenicity or infectiousness or corresponding mutations. Based on these data, authorities got a better overview of circulating SARS-CoV-2 strains as well as imported cases. In general, the current study made a significant contribution to the governmental decision-making process and helped more efficiently suppress the spread of the COVID-19 epidemic.

### Metadata and sample acquisition

Throughout most of the pandemic, SYNLAB Eesti testing sites in Estonia provided free SARS-CoV-2 PCR testing for all individuals living in the country. The free testing stopped for general population in May 2022 and for risk groups in November 2022. Self-paid testing has been available since 2020.

#### Sample metadata
Initially, at the beginning of the pandemic, all persons testing positive were contacted by the Health Board authorities and asked to provide details of their recent travels, family and work situation, in addition to more standard metadata of age, gender and place of living. This type of data collection was ongoing till spring 2022, after which only more general metadata was collected (gender, age, county). Once vaccination was made available to the public in spring 2021, also vaccination information was obtained first from the people themselves, and later data was systematically obtained from the [Health and Welfare Information Systems Centre](https://www.tehik.ee). In addition hospitalisation information was provided by the Health Board.

#### PCR testing
The laboratory of  SYNLAB Eesti carried out PCR testing. They captured Ct values and  particular mutation sites such as (Y453F) for all positively tested samples. The social security codes that uniquely identify a person in Estonia were shared with the Health Board, who together with the virology experts from the University of Tartu chose samples for sequencing. In general, the samples were carefully selected to ensure representation of the Estonian demographic and geographic subgroups, with additional samples taken from outbreaks that occurred at hospitals, elderly homes or work places. The data at individual level was linked at the Health Board and sample IDs from SySYNLAB Eesti lab and the matching metadata IDs were created. Both the Health Board and SYNLAB Eesti uploaded the data about the samples to an access restricted Gitlab repository.  

In addition to sequencing carried out in Estonia, samples were also sent to ECDC. The metadata for these samples followed the same pipeline as above. But the sequences were downloaded from dedicated ECDC websites and bioinformatically processed the same manner as the samples sequenced in Estonia.

#### Metadata cleaning and standardised
The metadata was semi-automatically cleaned and automatically standardised by custom-developed Python scripts. The following metadata types were cleaned and standardised -  age, age group, county, region of country, symptom onset date, place of infection,  vaccine producer and dose  (all applies to data being available).


### Sequencing and sequence analysis

The samples moved from SYNLAB Eesti and hospitals laboratories directly to the University of Tartu Genome Centre Core lab who carried out the sequencing using Illumina X10 sequencer. Based on the sample information and original location on the laboratory plates the automatic pipeline generated the 96-well plate layouts needed to carry out the sequencing.

The sequencing was carried out using [Arctic3](https://www.protocols.io/view/covid-19-artic-v3-illumina-library-construction-an-j8nlke665l5r/v5) and later [Arctic4](https://www.protocols.io/view/covid-19-artic-v4-1-illumina-library-construction-j8nlk4b36g5r/v2)  libraries.  At times also [NebNext Arctic](https://www.protocols.io/view/nebnext-artic-protocols-collection-rm7vz3rxrgx1/v1T) protocols were tested out. 

The raw sequences were initially analysed by the Illumina Dragen pipeline but was moved soon to the Galaxy workflow developed by the Galaxy community led by Wolfgang Maier. The pipeline includes removing the human reads from the raw sequences, mapping the reads to the consensus sequence of SARS-CoV-2, identifying mutations, creating multiple alignments, calling the Pangolin lineages and NextClade clades.  The work was carried out at the [Galaxy instance](https://galaxy.hpc.ut.ee/) hosted by the [ETAIS](https://etais.ee/) at the [University of Tartu HPC](https://hpc.ut.ee/). All the identified information on the samples was automatically fetched from the dedicated Galaxy address to the Gitlab repository and merged with the rest of the metadata about the samples.

### Generating custom reports

Based on the report templates provided by the ECDC, reports were filled in automatically  based on the sequencing results. These reports included variants of concern (VoCs), specific set of mutations or deletions defined by the ECDC such as S-gene deletion, 501_V2 variants etc. Similar reports were also generated for the Health Board to consult the Government.

### Dashboards

#### Description of the closed dashboard
The data table of all the samples was made available at the access restricted website for the Health Board employees and project participants to provide epidemiological and virological consultations. The database included all metadata provided for the samples, sequencing outcomes and was interactive providing filtering and sorting among other customisation options. In addition data could be downloaded for further custom analysis. The closed website of the project dashboard included also different interactive plots that allowed the users to pick the variables to be plotted (e.g. Ct values against vaccination status, county against lineages), but also lineage overview where individual lineages could be included or dismissed, time frame to be selected. In addition,  for each sequenced plate mutation plots and Ct value plots were implemented to carry out visual inspection as part of the quality control of the sequencing outcomes. In all the dashboards, users could select if they wanted to include data only sequenced in Estonia, by ECDC or both. 

#### Public dashboards
In addition to the access restricted dashboards, public data on the clades, percentage of all positive samples in Estonia been sequenced and clade distribution across counties, regions and age groups were made available and regularly updated at the [Estonian COVID19Dataportal](https://covid19dataportal.ee/genomics_transcriptomics/).  In order to illustrate the virus evolution a public [Nextstrain Auspiece](https://auspice.biit.cs.ut.ee/ncov/est) instance was set up. In regular time intervals, all samples were rerun to obtain the latest lineage annotations.

### Data brokering to ENA 

To upload data to [European Nucleotide Archive (ENA)](https://www.ebi.ac.uk/ena/browser/) we registered our research [projects at the ENA](https://www.ebi.ac.uk/ena/browser/text-search?query=korogeno-est) following the [guideline](https://ena-docs.readthedocs.io/en/latest/submit/study.html). At the beginning we created individual projects for a data batch but later joined many under one. The Data broker generated ENA metadata files using ENA virus pathogen reporting standard checklist ERC000033 filling out mandatory and recommended fields ([checklist](https://www.ebi.ac.uk/ena/browser/view/ERC000033), [metadata template](https://github.com/ELIXIR-Belgium/ENA-metadata-templates)).  The preparatory work for data brokering to ENA was done by a dedicated Galaxy workflow. A typical workflow of extraction of Galaxy results to the metadata file and metadata ERC000033 file generation took about 1h. 

Out of the three different raw sequencing data uploading ways, Estonia used the Galaxy-CLI instance which is a wrapper for the ENA upload tool. The wrapper is [available](https://github.com/usegalaxy-eu/ena-upload-cli) along with the [dedicated guide](https://rdm.elixir-belgium.org/covid-19/sarscov2_submission.html) that was [published](https://doi.org/10.1093/bioinformatics/btab421) in 2021.


### Alternative text for Galaxy ENA uploader. 
Galaxy ENA uploader takes raw reads as fastq files and metadata spreadsheet as an input. Then human reads are removed from the sequence data and the raw sequences gets uploaded to ENA along with the accompanying metadata. After variation analysis and consensus sequence workflow execution also consensus sequences get uploaded to ENA.

### Figure caption for Galaxy ENA uploader. 
An overview of SARS-CoV-2 raw reads and metadata upload steps to ENA enabled by Galaxy.

All the sequenced raw reads results were uploaded to the University of Tartu Galaxy instance. From there the data manager selects a batch and successfully sequenced samples into a working collection. Forward and reverse sequences are paired up and run through the workflow of dehumanisation of raw sequence reads (uses Metagen-FastQC). 

In Galaxy ENA uploader we marked the metadata checklist (ERC000033) and uploaded the filled-out template. From there we selected the runs input format from a paired collection (that is human sequence free) and added an affiliation center and run the ENA upload tool.

As of March 2023, over 23 000 Estonian SARS-CoV-2 sequences have been uploaded to ENA. The majority were sequenced during the KoroGeno-EST studies (14 251), complemented by 9978 successfully sequenced samples from ECDC. 

The KoroGeno-EST studies were conducted in cooperation with the University of Tartu, the Estonian Health Board and SYNLAB Eesti OÜ during 2021-2022. The study was approved by Research Ethics Committee of the University of Tartu. The [KoroGeno-EST-3 and KoroGeno-EST-2022 projects](https://kliinilinemeditsiin.ut.ee/et/sisu/eesti-sars-cov-2-taisgenoomide-jarjestamine-ja-analuus-korogeno-est-1est-2est-3) were financed by the Republic of Estonia's Ministry of Education and Research.

### Considerations in Estonia

- Estonia has a single national Health Board
- e-Estonia and the X-road (e-Identity, e-Health Records, e-Governance) infrastructure allows easy data linking across data sources using the personal identification number.
- There has been previous studies and cooperation between the Health Board and the University of Tartu in virus monitoring (HIV, Flu)
- There were no additional local laws restraining the study
- While the code of the dashboards, data handling is not publicly available the team is happy to consult researchers facing similar situation in the future. The best way is to send an email to [ELIXIR-Estonia](elixir@ut.ee).  The original [Galaxy workflows](https://workflowhub.eu/workflows?filter%5Bproject%5D=33&filter%5Bquery%5D=covid) adapted and used are publicly available. 

### External links to resources relevant to the KoroGeno-Est showcase

[Estonian Covid19Dataportal](https://covid19dataportal.ee/en/) 
[Overview of the SARS-CoV-2 projects (in Estonian)](https://kliinilinemeditsiin.ut.ee/et/sisu/eesti-sars-cov-2-taisgenoomide-jarjestamine-ja-analuus-korogeno-est-1est-2est-3) 
[Information on how to register a study to ENA](https://ena-docs.readthedocs.io/en/latest/submit/study.html)
 [ENA virus pathogen reporting standard checklist](https://www.ebi.ac.uk/ena/browser/view/ERC000033) 
[ENA metadata templates](https://github.com/ELIXIR-Belgium/ENA-metadata-templates) 
[Galaxy wrapper for the ENA upload tool](https://github.com/usegalaxy-eu/ena-upload-cli) 
[Submission of SARS-Cov-2 raw reads to ENA in Galaxy](https://rdm.elixir-belgium.org/covid-19/sarscov2_submission.html)
[General Guide On ENA Data Submission by ENA](https://ena-docs.readthedocs.io/en/latest/submit/general-guide.html)
[European Nucleotide Archive Quick tour by EMBL-EBI](https://www.ebi.ac.uk/training/online/courses/ena-quick-tour/)
[Example metadata template ERC000033](https://github.com/ELIXIR-Belgium/ENA-metadata-templates/blob/main/templates/ERC000033/example_metadata_template_ERC000033.xlsx )


<!--- In this section you should provide a brief summary of the uses of the showcase, i.e. when you would use this showcase resource ---> 

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->


<!---Information about affiliations below will be added to the affiliations.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-an-institution-infrastructure-project-or-funder  --->
