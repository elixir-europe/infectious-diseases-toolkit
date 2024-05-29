---
title: Using the ENA data submission toolbox for SARS-CoV-2 data
contributors: [Bert Droesbeke] 
description: High scale publishing of infectious diseases data to ENA using easy to use metadata templates. 
affiliations: [VIB,BE]
page_id: ena_upload
related_pages:
  showcase: [covid19_galaxy_project, korogenoest]
training:
  - name: Screencast of the Galaxy ENA upload tool
    registry: YouTube
    url: https://www.youtube.com/watch?v=POiQG-7O7rw

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style_guide when writing the content of this page. -->

<!--- Showcase pages should detail a particular combination of standards and tools from an infrastructural or domain perspective to tackle infectious diseases related data challenges. --->

## Introduction 

The COVID-19 pandemic has highlighted the importance of open and FAIR (Findable, Accessible, Interoperable, Reusable) data. Rapid access to diverse genome sequences of SARS-CoV-2 is identified as crucial for developing tests, vaccines, treatments, policies as well as detecting and monitoring new variants. The {% tool "european-nucleotide-archive" %} and the Global Initiative on Sharing All Influenza Data (GISAID) are primary repositories for SARS-CoV-2 data, with GISAID having stricter limitations on data reuse.

Despite an increase in number of submissions to both repositories, the ENA requirement of command line knowledge for bulk submissions was found to be a significant hinderance. To address this, a new set of tools was developed to simplify the submission of SARS-CoV-2 sequences to ENA. This included streamlining the process and integrating with platforms like Galaxy, to provide a user-friendly interface and additional tools for preprocessing and analysis.

To read more in detail how ELIXIR Belgium provided tooling for SARS-CoV-2 sequence submissions to ENA, please visit the [Covid-19 section on the RDM Guide](https://rdm.elixir-belgium.org/covid-19/).  


## Who is the showcase intended for?

The main targets of the ENA data submission toolbox are researchers, institutions, and support facilities that need to make data submissions to the {% tool "european-nucleotide-archive" %}.
Because the tools can be used to submit any sample type to the ENA, the potential user community is large and relates to the user community of ENA itself. Both the command line and Galaxy submission tools are appealing for labs/researchers sequencing medium to large numbers of samples.

The Galaxy submission tools have the biggest potential for adoption by many users, since they allow bulk sequence submissions for researchers with no command line or programming skills. Additionally, these can be integrated in existing Galaxy sequence analysis workflows. These characteristics make them convenient for both frequent and sporadic use

## What is the showcase?

The components described below allow for a single-step submission process, a graphical user interface, secure credential handling, tabular-formatted metadata and the possibility to remove human reads prior to submission.

{% include image.html file="ena-submission-toolbox.svg" caption="<b>Figure 1.</b> Overview of the ENA data submission toolbox components." alt="Overview of ENA upload toolbox" %}

To improve the submission of SARS-CoV-2 nucleotide sequences to {% tool "european-nucleotide-archive" %}, we have collaboratively developed and compiled a command line tool, a set of Galaxy tools and Galaxy workflows essential for cleaning, assembling, and submitting SARS-CoV-2 sequences to the European Nucleotide Archive (ENA). Using Galaxy offers numerous advantages, such as a user-friendly graphical interface, access to a wide range of tools and workflows for preprocessing, downstream analysis, and visualization of sequences, including those specific to SARS-CoV-2 (Maier et al., 2021). Additionally, Galaxy provides a platform for sharing data and metadata, facilitating international collaboration, integrating with other public resources, and enabling the publication of FAIR data and analysis workflows.


### Human Reads Cleaning Tool
To comply with Europe’s General Data Protection Regulation (GDPR), human genetic information must be removed from raw data before submission to ENA. We have integrated {% tool "metagen-fastqc" %} into Galaxy for this purpose. A series of steps were wrapped into a single Galaxy tool, allowing users to filter human data from the data.

### ENA upload cli 
Submitting raw reads to ENA can be done via the website, Webin-CLI, or programmatically using curl commands. Programmatic submissions are preferable for bulk uploads but require bioinformatics expertise to generate XML metadata files and upload data via FTP. To simplify this, a Python command line interface (CLI), {% tool "ena-upload-cli" %}, was created. This CLI eases submission for bioinformaticians by converting user-friendly TSV files or Excel templates (see previously) into the required XML files. It manages FTPS uploads, validates metadata before submission, and allows for adding, modifying, canceling, and releasing study, sample, experiment, and run ENA objects without the need to login into Webin portal.

The Python package {% tool "ena-upload-cli" %} is available on pipy and bioconda.

### The Galaxy ENA upload tool
To make the process accessible to researchers with limited bioinformatics expertise, we wrapped the ENA upload tool as a {% tool "ena-upload-tool" %}. It is part of the Intergalactic Utilities Commission (IUC), a curated collection of Galaxy tools. Galaxy instance administrators can find installation details, and users can find usage instructions on our Submission of SARS-CoV-2 raw reads page.

### The Galaxy ENA consensus submission tool
To facilitate the submission of genome assemblies, a Galaxy wrapper {% tool "ena-webin-cli" %} of the ENA {% tool "webin-cli" %} was created. The tool wrapper simplified the creation of the mandatory manifest file by allowing users to interactively fill in the assembly metadata and submit SARS-CoV-2 consensus data to ENA.

### Galaxy Docker container

If you cannot use the Galaxy instances at useGalaxy.eu, .be, or .au, possibly due to GDPR reasons, a ready-to-use Docker container is made available. This container includes additional tools, made available in the [SARS-CoV-2](https://github.com/galaxyproject/SARS-CoV-2/) GitHub repository since February 2020, in an effort published by Maier et al. (2021) to provide publicly accessible infrastructure and workflows for SARS-CoV-2 data analyses. The repository featured workflows for Genomics, Cheminformatics, and Proteomics analyses. This centralization of workflows made it easy for Galaxy administrators to deploy and install the tools and workflows together with the other submission tools and create a one stop shop for processing and submitting SARS-CoV-2 sequencing data. The Docker container allows for the local deployment of a fully functional Galaxy instance. It will ensure that data remains on-premise until submission. More information on how to obtain and deploy the container can be found on the [GitHub repository](https://github.com/ELIXIR-Belgium/Galaxy-SARS-CoV-2-sequence-upload).

## What can you use the ENA data submission toolbox for?
 
The work described in the showcase can be readily used in different ways.

### Direct use for SARS-CoV-2 sequence submission

The tools and workflows mentioned here are available at the [useGalaxy.be](https://usegalaxy.be/) instance. The submission of raw reads can also be readily performed through [useGalaxy.eu](https://usegalaxy.eu) and [useGalaxy.org.au](https://usegalaxy.org.au/).

The Galaxy Docker container can be used to deploy a functioning instance containing all the tools described.
Instructions on using the components are described in the [ELIXIR-Belgium RDM Guide](https://rdm.elixir-belgium.org/covid-19/).

### Repurposing o the showcase for other organisms


A [general purpose container](https://github.com/ELIXIR-Belgium/ena-upload-container) for deploying a Galaxy instance capable of submitting both raw sequences and genome assemblies of all [ENA Sample checklists](https://www.ebi.ac.uk/ena/browser/checklists) is available.




## Publications

- Roncoroni, M., Droesbeke, B., Eguinoa, I., De Ruyck, K., D’Anna, F., Yusuf, D., Grüning, B., Backofen, R., & Coppens, F. (2021). A SARS-CoV-2 sequence submission tool for the European Nucleotide Archive. Bioinformatics, 37(21), 3983–3985. [https://doi.org/10.1093/bioinformatics/btab421](https://doi.org/10.1093/bioinformatics/btab421)

- Baker D, van den Beek M, Blankenberg D, Bouvier D, Chilton J, et al. (2020) No more business as usual: Agile and effective responses to emerging pathogen threats require open data and open analytics. PLOS Pathogens 16(8): e1008643. [https://doi.org/10.1371/journal.ppat.1008643](https://doi.org/10.1371/journal.ppat.1008643)


## Support

<!-- Describe how the showcase is funded or supported. -->
This work was supported by Fonds Wetenschappelijk Onderzoek [I002819N] and Sonderforschungsbereich/TRR [167/2 Z01].
