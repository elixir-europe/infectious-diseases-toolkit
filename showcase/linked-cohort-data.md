---
title: Linked pathogen and host data across archives - a multi-omics, SARS-CoV-2 cohort case study
contributors: [Gabriele Rinck, Zahra Waheed] 
description: Here we describe the first example of linking and sharing a COVID-19, multi-omics cohort data set via the EMBL-EBI infrastructure. 
affiliations: [EMBL-EBI]
page_id: LinkedCohortData

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style_guide when writing the content of this page. -->

<!--- Showcase pages should detail a particular combination of standards and tools from an infrastructural or domain perspective to tackle infectious diseases related data challenges. --->

## The importance of data integration 

Cohort studies produce invaluable data typically including a range of different data types, such as clinical (e.g. patient health records, blood markers, treatment details) as well as multi-omics data (such as genomic sequence, transcriptomic or proteomic data). However, often these data types are siloed in archives specific for each type. Data integration, i.e, linking these data types on a participant level across different repositories, adds more depth to the dataset by bringing the pathogen and host data into context, allowing a more comprehensive analysis of the entire collection of data.     

Here we describe the first example of linking and sharing a multi-omics SARS-CoV-2 cohort dataset with multiple time points, via the European Molecular Biology Laboratory-European Bioinformatics Institute’s (EMBL-EBI) infrastructure. 


## Who is the SHOWCASE intended for?

This showcase is intended for any groups who would like to FAIRly share cohort study data, and would like to better understand how this can be performed. More broadly, the linking mechanism described below is applicable to any group whose research involves different types of molecular data being obtained from the same biological sample. 
The showcase will also be useful for those wishing to access linked clinical and multi-omics data from cohort studies. 

## Sharing the linked EMC Pilot Cohort Dataset

{% include image.html file="/EMC_pilot_data_diagram.png" caption="Figure 1. An overview of the data integration process across EMBL-EBI archives. At the ENA, all SARS-CoV-2 sequence data undergo in-house systematic analysis, and these products feed into the European Variation Archive (EVA) and Ensembl. More details can be found from the pre-print [here](https://www.biorxiv.org/content/10.1101/2023.04.19.537514v2.full.pdf)." %}

The team at Erasmus Medical Centre (EMC Rotterdam, NL) collected data from a cohort of 151 Polymerase Chain Reaction (PCR)-confirmed COVID-19 individuals who had been admitted to the hospital with a respiratory infection or respiratory failure in 2020-2021. After harmonisation of the clinical-epidemiological data using the International Severe Acute Respiratory and emerging Infection Consortium’s (ISARIC) data dictionary for the {% tool "isaric-covid-19-crf" %} (carried out by ReCoDID partners at the university hospital in Heidelberg, Germany), the sensitive, pseudonymised clinical-epidemiological data were submitted to the {% tool "ega" %}, SARS-CoV-2 sequences were deposited in {% tool "european-nucleotide-archive" %} and {% tool "arrayexpress" %}/{% tool "biostudies" %} was used to archive antibody profiles as well as B-cell and T-cell data (see Figure 1). 

The various data types were linked on participant level by utilising the {% tool "biosamples" %} data archive which can capture relationships between samples. In a hierarchical structure a top-level sample ID was created which represents the patient (and the associated EGA record). Further BioSample IDs were created for each time point and/or data type and these were linked to the top-level sample ID of this patient, creating a link between data types on participant level (see Figure 2). 

{% include image.html file="/EMC_pilot_sample_diagram.png" caption="Figure 2. Schematic of participant level linking of Biosamples. ‘V’ refers to Viral, while ‘H’ refers to non-sensitive human samples (e.g. representing data types, or the top-level COVID-19 patient)." %}

### Composition of the EMC Pilot Cohort Dataset:

The composition of the EMC SARS-CoV-2 Dataset is summarised below and in Figure 3.    

- Clinical-epidemiological information is available for all 151 patients that tested PCR-positive for SARS-CoV-2. For 77 of those, additional data types are available and these have also been submitted and linked; for the remaining 74 patients only clinical-epidemiological data is available. (Archived in {% tool "ega" %}, controlled access managed through a [Data Access Committee (DAC)](https://ega-archive.org/dacs/EGAC00001002851));
- 80 SARS-CoV-2 sequences are available for 63 patients, with 1-4 sequences per patient. (Archived in {% tool "european-nucleotide-archive" %}, open access);
- Antibody profiles are available for 40 patients with 2-5 time points per patient, with a total of 147 data points. (Archived in {% tool "arrayexpress" %}/{% tool "biostudies" %}, open access);
- T-cell data are available for 28 patients with 1, 3 or 4 time points per patient and a total of 51 data points. (Archived in {% tool "arrayexpress" %}/{% tool "biostudies" %}, open access);
- B-cell data are available for 17 patients with either one or 3 time points and a total of 29 data points. (Archived in {% tool "arrayexpress" %}/{% tool "biostudies" %}, open access).

All sample records for this dataset, together with the appropriate links, can be viewed in the {% tool "biosamples" %} database [here](https://www.ebi.ac.uk/biosamples/samples?text=ReCoDID+COVID-19+pilot+study).

{% include image.html file="/EMC_pilot_dataset_composition_diagram.png" caption="Figure 3. A Venn diagram showing the different combinations of data types for all 151 patients in the EMC study." %}


## The Cohort Browser - improving the Findability of Cohort Datasets

While the BioSamples database is key to capturing the linking of data types on a participant level, the {% tool "pathogens-cohort-browser" %} presents a range of study-level information about each cohort. Similar to a shop window, it enhances the findability of the datasets and as an integral part of the {% tool "pathogens-portal" %}, serves as the primary entry point into accessing cohort data.

{% include image.html file="/cohort_browser_img.png" caption="Figure 4. The cohort browser brings together study-level information, links to the datasets and provides search and filtering functionality to improve data discoverability." %}

The Cohort Browser lists discovery metadata of cohort studies and provides links to the available data types. Where possible, basic aggregate data are also included and future search and filtering functionality will allow users to locate datasets of interest. 

## What can you use the SHOWCASE for?

- this showcase provides a proof of concept for linking and sharing of entire cohort datasets in line with FAIR principles, with data sharing being as open as possible and as closed as necessary. 
- this showcase provides the first public, cohort study example of linking different biological data types, at the sample-level, across dedicated archives.
- the applied linking process significantly increases the interoperability between the bespoke archives for the various data types, making it easier to access and analyse them.
- linking these data types on a participant level also adds more depth to the dataset by bringing the pathogen and host data into context, allowing a more comprehensive analysis.
This is particularly important in public health but will equally provide a better understanding of infectious diseases in the context of both pathogen & their host factors.

## Acknowledgements
### ReCoDID Project Team Members
The work presented here was a coordinated effort of multiple teams covering the different aspects of the process:    

**Data collection and submissions** were coordinated by the Viroscience department at Erasmus Medical Centre (EMC), Rotterdam, NL:    
Clara Amid, Janko van Beek, Gijs van Nierop, Rory de Vries, Marion Koopmans.    

**Harmonisation of clinical-epidemiological data** was performed at the University Hospital Heidelberg, Germany:    
Frank Tobian, Thomas Jänisch.    

The **infrastructure for data sharing and support for the data linking process** was provided by EMBL-EBI, Hinxton, UK:    
Gabriele Rinck, Zahra Waheed, Nadim Rahman, Marcos Casado Barbero, Mallory Freeberg, Dipayan Gupta, Anja Füllgrabe, Ugis Sarkans, Guy Cochrane.    

Additional people who have contributed:    
Coline Thomas, Marianna Ventouratou, Suran Jayathilaka and Vishnukumar Balavenkataraman Kadhirvelu.

### Support
ReCoDID project is funded by the European Union’s Horizon 2020 Research and Innovation Programme, grant agreement N° 825746, and the Canadian Institutes of Health Research, Institute of Genetics (CIHR-IG), grant agreement N° 01886-000.

