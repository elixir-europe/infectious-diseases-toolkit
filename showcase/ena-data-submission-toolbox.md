---
title: ENA data submission toolbox
contributors: [Bert Droesbeke] 
description: High scale publishing of infectious diseases data to ENA using easy to use metadata templates. 
affiliations: [VIB,BE]
page_id: "ena-upload"
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

<!--- In this section you should provide a brief overview of the context that makes Showcase necessary. It is useful to mention the projects under which the showcase was created, the involved research infrastructures, and the disease it is meant to tackle --->


The COVID-19 pandemic has highlighted the importance of open and FAIR (Findable, Accessible, Interoperable, Reusable) data. Rapid access to diverse genome sequences of SARS-CoV-2 is identified as crucial for developing tests, vaccines, treatments, policies as well as detecting and monitoring new variants. The European Nucleotide Archive (ENA) and the Global Initiative on Sharing All Influenza Data (GISAID) are primary repositories for SARS-CoV-2 data, with GISAID focusing on consensus sequences and ENA storing raw reads.

Despite an increase in submissions to both repositories, a significant imbalance between the two repositories was identified, with GISAID having more submissions due to easier submission processes compared to the more complex ENA, which requires command line knowledge. To address this, a new set of tools was developed to simplify the submission of SARS-CoV-2 sequences to ENA by streamlining the process and integrating with platforms like Galaxy, which provides a user-friendly interface and additional tools for preprocessing and analysis.

To read more in detail how ELIXIR Belgium provided tooling for SARS-CoV-2 sequence submissions to ENA, please visit the [Covid-19 section on the RDM Guide](https://rdm.elixir-belgium.org/covid-19/).  


## Who is the showcase intended for?

<!--- In this section you should provide a brief account of the target audience or intended users for the showcase --->
Because the tools can be used to submit any sample type to the ENA, the potential user community is large and relates to the user community of ENA itself. Both the command line and Galaxy submission tools are appealing for labs/researchers sequencing medium to large numbers of samples.

The Galaxy submission tools have the biggest potential for adoption by many users, since they allow bulk sequence submissions for researchers with no command line or programming skills. Additionally, these can be integrated in existing Galaxy sequence analysis workflows. These characteristics make them convenient for both frequent and sporadic us

<!--- In this section you should provide a brief description of what the showcase is i.e. what it comprises of and a general description for it.  --->
<!--- Start with a graphical representation of the showcase, with a caption and an alternative text (alt). The graphical representation should be a diagram showing the different standards, tools, data sources that are used to tackle the challenge. The diagram should show how these different modules connect with one another  --->

## What can you use the ENA data submission toolbox for?
 
<!--- In this section you should provide a brief summary of the uses of the showcase, i.e. when you would use this showcase resource ---> 

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->


<!---Information about affiliations below will be added to the affiliations.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-an-institution-infrastructure-project-or-funder  --->

{% include image.html file="ena-submission-toolbox.svg" caption="<b>Figure 1.</b> Overview of the ENA Data Submission Toolbox components." alt="Overview of ENA upload toolbox" %}

To improve the submission of SARS-CoV-2 nucleotide sequences to {% tool "european-nucleotide-archive" %}, we have collaboratively developed and compiled a command line tool, a set of Galaxy tools and Galaxy workflows essential for cleaning, assembling, and submitting SARS-CoV-2 sequences to the European Nucleotide Archive (ENA). Using Galaxy offers numerous advantages, such as a user-friendly graphical interface, access to a wide range of tools and workflows for preprocessing, downstream analysis, and visualization of sequences, including those specific to SARS-CoV-2 (Maier et al., 2021). Additionally, Galaxy provides a platform for sharing data and metadata, facilitating international collaboration, integrating with other public resources, and enabling the publication of FAIR data and analysis workflows.


The ENA data submission toolbox is comprised of multiple tools including:

* The ‘[ENA upload CLI](https://github.com/usegalaxy-eu/ena-upload-cli)’: a command line tool to register studies and samples and submit raw read data to the ENA. Simplify bioinformaticians' submission process with a Python CLI that generates XML files and handles FTP uploading.
* The ‘[Galaxy ENA upload tool](https://github.com/galaxyproject/tools-iuc/tree/master/tools/ena_upload)’: a Galaxy wrapper of the above (1.) tool. 
* A Galaxy consensus submission tool: seamlessly submit SARS-CoV-2 consensus data to ENA using the [ENA Webin-CLI](https://github.com/enasequence/webin-cli) in the back. (the only ENA tool that allows programmatic submission of consensus sequences for all sample types)

* Human read cleaning tool: Galaxy tool to remove human reads from raw reads to comply with Europe’s General Data Protection Regulation (GDPR) 


### 

Access COVID-19 variant discovery and consensus building workflows for Illumina WGS, amplicon, and ONT amplicon data.
Human Reads Cleaning Tool


### Galaxy Docker Container

In February 2020 the [SARS-CoV-2](https://github.com/galaxyproject/SARS-CoV-2/) repo was created by the Galaxy Project to provide publicly accessible infrastructure and workflows for SARS-CoV-2 data analyses. It featured three different types of analyses: Genomics, Cheminformatics, and Proteomics. This centralization of Galaxy workflows made it easy for Galaxy administrators to download and install the workflows and tools. 

Includes variant discovery and consensus building workflows for diverse sequencing data types.

The Galaxy tools are shipped in a [Docker container]() which deploys a Galaxy instance containing a tool to clean human reads from the raw reads. Comply with GDPR by removing human genetic information from raw data using the Metagen-FastQC Galaxy tool. All tools and workflows are included in a custom Galaxy Docker container for easy deployment.

## Publication

Roncoroni, M., Droesbeke, B., Eguinoa, I., De Ruyck, K., D’Anna, F., Yusuf, D., Grüning, B., Backofen, R., & Coppens, F. (2021). A SARS-CoV-2 sequence submission tool for the European Nucleotide Archive. Bioinformatics, 37(21), 3983–3985. [https://doi.org/10.1093/bioinformatics/btab421](https://doi.org/10.1093/bioinformatics/btab421)


## Support

<!-- Describe how the showcase is funded or supported. -->
This work was supported by Fonds Wetenschappelijk Onderzoek [I002819N] and Sonderforschungsbereich/TRR [167/2 Z01].
