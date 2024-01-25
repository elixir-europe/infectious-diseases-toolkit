---
title: ENA data submission toolbox
contributors: [Bert Droesbeke] 
description: High scale publishing of infectious diseases data to ENA using easy to use metadata templates. 
affiliations: [VIB]
page_id: "ena-upload"
related_pages: 
  pathogen_characterisation: []
  socioeconomic_data: []
  human_biomolecular_data: []
  human_clinical_and_health_data: []
training:
  - name: Screencast of the Galaxy ENA upload tool
    registry: YouTube
    url:

# More information on how to fill in this metadata section can be found here https://www.infectious-diseases-toolkit.org/contribute/page-metadata
---

<!-- Please take in mind our style guide https://www.infectious-diseases-toolkit.org/contribute/style_guide when writing the content of this page. -->

<!--- Showcase pages should detail a particular combination of standards and tools from an infrastructural or domain perspective to tackle infectious diseases related data challenges. --->

## Introduction 

<!--- In this section you should provide a brief overview of the context that makes Showcase necessary. It is useful to mention the projects under which the showcase was created, the involved research infrastructures, and the disease it is meant to tackle --->

As a life-science data Research Infrastructure in Europe, ELIXIR contributes to increasing publicly available COVID-19-related data. This showcase highlights the commitment of ELIXIR Belgium in supporting the submission of SARS-CoV-2 nucleotide sequences to public repositories.
The (ENA) data submission toolbox simplifies the submission of sequence data, including raw reads and assembled sequences, for researchers. European Nucleotide Archive (ENA) is a fully open repository dedicated to storing raw sequencing data, assemblies, and annotation data.

## Who is the showcase intended for?

<!--- In this section you should provide a brief account of the target audience or intended users for the showcase --->
People who want to submit RAW The tools are designed to be compatible with all ENA sample checklists which cover a brought spectrum within the data life sciences. Find out which sample checklist would apply to your submission on the [ENA website](https://www.ebi.ac.uk/ena/browser/checklists)

The showcase is intended for researchers, bioinformaticians, and anyone involved in contributing to the global effort against the COVID-19 pandemic. Whether you're an experienced bioinformatician or a researcher with limited informatics background, our tools and workflows cater to your needs.

## What is the showcase?

<!--- In this section you should provide a brief description of what the showcase is i.e. what it comprises of and a general description for it.  --->
<!--- Start with a graphical representation of the showcase, with a caption and an alternative text (alt). The graphical representation should be a diagram showing the different standards, tools, data sources that are used to tackle the challenge. The diagram should show how these different modules connect with one another  --->
{% include image.html file="" caption="Figure 1. " alt="" %}


ENA submission toolbox is comprised of three tools:
The ‘ENA upload CLI’: a command line tool to register studies and samples and submit raw read data to the ENA.
The ‘Galaxy ENA upload tool’: a Galaxy wrapper of the above (1.) tool. 
A Galaxy consensus submission tool: a wrapper of ENA Webin-CLI (the only ENA tool that allows programmatic submission of consensus sequences for all sample types)
Together with other tools available in Galaxy, tools 2 and 3 make a one-stop solution for the submission of SARS-CoV-2 (and other species) data and metadata to the ENA using Galaxy. The Galaxy platform has a graphical user interface and includes our tools for raw read submission (based on the command line tool), cleaning of human reads, consensus sequence assembly and the submission of these consensus sequences to ENA.


ENA submission toolbox is comprised of three tools:

* The ‘[ENA upload CLI](https://github.com/usegalaxy-eu/ena-upload-cli)’: a command line tool to register studies and samples and submit raw read data to the ENA. Simplify bioinformaticians' submission process with a Python CLI that generates XML files and handles FTP uploading.
* The ‘[Galaxy ENA upload tool](https://github.com/galaxyproject/tools-iuc/tree/master/tools/ena_upload)’: a Galaxy wrapper of the above (1.) tool. 
* A Galaxy consensus submission tool: seamlessly submit SARS-CoV-2 consensus data to ENA using the [ENA Webin-CLI](https://github.com/enasequence/webin-cli) in the back. (the only ENA tool that allows programmatic submission of consensus sequences for all sample types)

The Galaxy tools are shipped in a [Docker container]() which deploys a Galaxy instance containing a tool to clean human reads from the raw reads. Comply with GDPR by removing human genetic information from raw data using the Metagen-FastQC Galaxy tool. All tools and workflows are included in a custom Galaxy Docker container for easy deployment.

Access COVID-19 variant discovery and consensus building workflows for Illumina WGS, amplicon, and ONT amplicon data.

The Tools
Human Reads Cleaning Tool

ENA Reads Submission Tool (Command Line)


Galaxy ENA Reads Submission Tool
A user-friendly Galaxy tool for researchers without informatics experience to submit sequences to ENA.

COVID-19 Genome Analysis Workflows
Includes variant discovery and consensus building workflows for diverse sequencing data types.

Galaxy Docker Container

## What can you use the SHOWCASE for?
 
<!--- In this section you should provide a brief summary of the uses of the showcase, i.e. when you would use this showcase resource ---> 

<!---Information about contributors will be added to the CONTRIBUTORS.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-extra-info-to-the-contributors --->


<!---Information about affiliations below will be added to the affiliations.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-an-institution-infrastructure-project-or-funder  --->
