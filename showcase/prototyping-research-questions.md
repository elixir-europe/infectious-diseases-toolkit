---
title: "Prototyping federated causal research questions reusing sensitive health data"
search_exclude: true #leave as “true” until the page is complete and ready to be made public
contributors: [<!---REPLACE THIS with comma separated list of contributors--->] 
description: "Methodological framework for causal federated research based on real-world observational data sources across national borders"
affiliations: [BE, ES, FI, AT, Sciensano, IACS, THL, GÖG]
page_id: "prototyping_research_questions"
related_pages: 
  pathogen_characterisation: [<!---REPLACE THIS with the page IDs of the pathogen_characterisation pages that you want to list here as related pages--->]
  socioeconomic_data: [<!---REPLACE THIS with the page IDs of the socioeconomic_data pages that you want to list here as related pages--->]
  human_biomolecular_data: [<!---REPLACE THIS with the page IDs of the human_biomolecular_data pages that you want to list here as related pages--->]
  human_clinical_and_health_data: [<!---REPLACE THIS with the page IDs of the human_clinical_and_health_data pages that you want to list here as related pages--->]
training:
  - name: Learn about DAGs and DAGitty
    registry: Other
    url: https://dagitty.net/learn/
  - name:  BY-COVID Spring 23 Use Cases Workshop: Integration of socioeconomic data in observational studies on vaccine effectiveness
    registry: Zenodo
    url: https://zenodo.org/doi/10.5281/zenodo.7985916 


## Introduction 

Leveraging “real-world” observational data sources, often sourced by reusing routinely collected data (i.e., secondary use), to infer causality offers great opportunities for informing health policy while raising some challenges for its implementation. Applying such  a causal framework often implies the need for detailed sensitive individual-level data in order to mitigate confounding. Conducting causal research across national borders consequently brings challenges in terms of sensitive data access and interoperability.
The use case defined within the BY-COVID project aimed to ensure interoperability across national borders by enabling a federated approach complying with privacy and data protection regulations. This showcase presents the proposed methodology, and subsequently applies it to a policy-relevant research question (i.e., [investigating the real-world effectiveness of the SARS-CoV-2 primary vaccination program in populations spanning different countries](https://zenodo.org/doi/10.5281/zenodo.7551181)), aiming to facilitate a rapid response in the case of a next pandemic.

## Who is the showcase intended for?

The proposed methodology provides step-by-step guidance for researchers assessing causal public health research questions directed towards populations crossing (national) borders. Researchers from scientific institutions, providing evidence feeding into public health policy, can benefit from the proposed methodology. 


## What is the showcase?

The methodological framework for [federated causal inference based on real-world observational data sources](https://doi.org/10.1186/s12874-023-02068-3) includes a step-by-step guidance (see Figure 1), from defining a research question, to establishing a causal model, identifying and specifying data requirements in a common data model, generating synthetic data, and developing an interoperable and reproducible analytical pipeline for distributed deployment. It requires close collaboration between a coordinating research team (also referred to as the ‘Coordination Node’) and institutions hosting or being able to acquire access to the required sensitive individual-level data (also referred to as ‘Participant Nodes’).

{% include image.html file="/prototyping_use_cases_to_tackle_future_pandemic_Figure-1.png" caption="Figure 1. The methodological framework consists of several consecutive steps. Step 1 to 5 are part of a ‘conceptual and instrumental phase’ within the framework and are conducted by the Coordination Node without access to real-world data. Steps 6 and 7 involve the extraction, transformation and analysis of real-world data within the jurisdiction of each of the Participant Nodes. Step 8 is the final step conducted by the Coordination Node which produces comparable results to inform policy. " alt="Visual representation of the proposed methodological framework." %}

### Building blocks

#### Defining the research question
The research question needs to be precisely defined following the [PICO(T) scheme](https://en.wikipedia.org/wiki/PICO_process). 

#### Establishing a causal model
Graphical causal models, such as [Directed Acyclic Graphs (DAGs)](https://doi.org/10.1016/j.jclinepi.2021.08.001), enables researchers to explicitly state the underlying assumptions that are made to estimate the causal effect of interest. Thereby, it provides a clear and transparent graphical way to identify confounding bias and other potential sources of bias under the described assumptions and subsequently informs the study design and statistical analysis. The [DAGitty](https://www.dagitty.net/) web application provides an environment for creating, editing, and analysing causal diagrams.

#### Specifying data requirements
The data requirements (i.e., the variables as identified in the causal model) are captured in a Common Data Model (CDM), detailing syntactic and semantic considerations to achieve interoperability between Participant Nodes. Each of the variables is characterised  within the model description of the CDM, including (1) the model entity, (2) the variable label, (2) a description of the variable, (3) the encoding system, (4) the variable format and type, (5) the units of measurement, (6) the requirement level, (7) the variable-level validation rules, (8) the variable properties (observed/calculated), and (9) the possible data sources. 

#### Generating synthetic data
Synthetic data can be simulated by capturing the technical and syntactic requirements as specified in the Common Data Model (CDM) and using either non-informative mathematical distributions or expected distributions based on prior knowledge, thereby avoiding exposure of the real sensitive data.

#### Developing an interoperable analytical pipeline
The interoperable analytical scripts can be developed using the synthetic data. The analysis should include a comprehensive Data Quality Assessment (DQA), a validation check of compliance with the Common Data Model (CDM) specification, and a descriptive analysis providing characteristics of the study population. The analytics are dependent on the specified research question and can apply different methods to address biases and handle missing data. The analytical pipeline should only produce aggregated results that have lost all sensitive properties, i.e., compliant with disclosure policies.

#### Extracting, linking and transforming the real-world observational data
Each Participant Node (i.e., institutions hosting or being able to require access to individual-level real-world population, health and care data) is responsible for the data access application process, and the subsequent processing of the data following the guidelines provided by the Common Data Model (CDM) specification. The development and publishing of a Data Management Plan (DMP), for example using [Argos](https://argos.openaire.eu/splash/index.html)’ services, facilitates a rapid data access application process.

#### Deploying the analytical pipeline
The interoperable analytical pipeline should be distributed and deployed within a secured processing environment (SPE) of each Participant Node. It requires as input the transformed data complying with the Common Data Model (CDM) specification. The pipeline can be provided as single or multiple scripts implementing the statistical analysis using auditable open-source software or can be containerised (e.g., using a [Docker container](https://polaris.imag.fr/arnaud.legrand/research/readings/acm_sigops_si_rsea/p71-boettiger.pdf)), providing a fixed environment dealing with system and software dependencies.

#### Comparing and/or pooling the local results
To integrate results across different populations, the aggregated non-sensitive statistics produced as local outputs of the analytical pipeline are shared and can be compared and/or pooled by the Coordination Node in the form of a meta-analysis. 


## What can you use the SHOWCASE for?
 
The proposed methodology can be applied to any well-defined population health research question and is generalisable to many situations, increasing preparedness for infectious diseases. It was demonstrated within the BY-COVID project by prototyping a workflow to assess the real-world effectiveness of SARS-CoV-2 primary vaccination compared to partial or no vaccination in preventing SARS-CoV-2 infection in populations spanning different countries.
The research question was defined (step 1) following the PICOT strategy, and a [study protocol](https://zenodo.org/doi/10.5281/zenodo.7551181) was developed to provide a plan of action containing the study objectives and planned methodology. Subsequently, the [Directed Acyclic Graph (DAG), Common Data Model (CDM) and synthetic dataset](https://doi.org/10.5281/zenodo.7572373) (steps 2, 3 and 4), together with all supporting research objects (see Figure 2), were developed and published on Zenodo. 

{% include image.html file="/prototyping_use_cases_to_tackle_future_pandemic_Figure-2.png" caption="Figure 2. Overview of the executed steps and produced research objects during the implementation of the proposed methodological approach steps 1 to 4." alt="Visual representation of the executed steps." %}

An analytical pipeline was developed and tested with the support of the synthetic data (step 5) using the R statistical programming language as sequential Quarto documents (.qmd files) reflecting and reporting the outputs of different modules (see Figure 3): thus, (1) Data Quality Assessment (DQA) of the original input data, (2) validation of the original input data to check compliance with the Common Data Model (CDM), (3) imputation of missing data where required, (4) iterative matching of the exposed to unexposed individuals and a balance assessment of the matched population, (5) a descriptive analysis of the matched and unmatched study population, and (6) a survival analysis in the matched study population. A detailed documentation of the statistical methods, as well as a README file guiding users on the script deployment, accompanies the statistical scripts in a [dedicated GitHub repository](https://github.com/by-covid/BY-COVID_WP5_T5.2_baseline-use-case).  

{% include image.html file="/prototyping_use_cases_to_tackle_future_pandemic_Figure-3.png" caption="Figure 3. Graphical overview of the developed analytical pipeline, consisting of different subsequent modules, each producing an interactive report." alt="Graphical overview of the analytical pipeline." %}

A detailed description of the security measures that will be implemented to prevent unauthorised access to personal data within the secured processing environments (SPEs) of each of the Participating Nodes, as well as a description of the anonymisation/pseudonymisation techniques that will be implemented, is provided in the published [Data Management Plan (DMP)](https://zenodo.org/doi/10.5281/zenodo.7625783).

The [preliminary outputs](https://zenodo.org/doi/10.5281/zenodo.7871533), i.e., interactive reports of each main step of the analytical pipeline, have been published for Aragon, Spain. 

<!---Information about affiliations below will be added to the affiliations.yaml . Further instructions can be found at https://www.infectious-diseases-toolkit.org/contribute/editorial-board-guide#adding-an-institution-infrastructure-project-or-funder  --->


## Acknowledgments

The work was executed as part of the BeYond-COVID project, more specifically within the context of one of the project's use cases.

Contributors: Nina Van Goethem, Enrique Bernal-Delgado, Francisco Estupiñán-Romero, Marjan Meurisse, Javier González-Galindo, Natalia Martínez-Lizaga, Santiago Royo-Sierra, Simon Saldner, Lorenz Dolanski-Aghamanoukjan, Alexander Degelsegger-Marquez, Stian Soiland-Reyes, Markus Perola, and Teemu Paajanen.

Participant nodes: Sciensano (Belgium), IACS (Spain), THL (Finland), and GÖG (Austria).


We also want to acknowledge the participation and feedback from Vasso Kalaitzi (KNAW/DANS), Claudia Habl (GÖG), Gunter Maier (GÖG), Mirjam Knol (RIVM), Chantal Reusken (RIVM), Mariken Tijhuis (RIVM), Leon Schutte (RIVM), Kati Kristiansson (THL), Pekka Jousilahti (THL), Jostein Starrfelt (NIPH), Hinta Meijerink (NIPH).


### Support

<!-- Describe how the showcase is funded or supported. -->
