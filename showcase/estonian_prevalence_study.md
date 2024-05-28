---
title: Lessons learned from implementing the prevalence study of SARS-CoV-2 in Estonia during 2020-2023
contributors: [Uku Raudvere, Diana Pilvar]
description: Insights and practical guidelines from the SARS-CoV-2 prevalence study in Estonia, covering the project's execution, challenges, and key lessons
affiliations: [University of Tartu, EE]
related_pages:
  showcase: [korogenoest]
page_id: prevalence_est
---

## Introduction

The prevalence study on the SARS-CoV-2 epidemic in Estonia was conducted between 23 April 2020, and 30 January 2023. Individuals from across the country were randomly surveyed and tested to provide the government with essential data for making informed decisions to manage and curb the spread of the virus. 

The study received funding from the Estonian Ministry of Education and Research (grants SMVPT20243, SMVPT20599, 2014-2020.15.01.22-0162) from 23 April 23 2020, to 31 August 2023. Additionally, it was supported by the European Union and the European Commission from 1 May 2021, to 31 August 2023.

The project was a collaborative effort that brought together experts from various disciplines, including statisticians, clinicians, bioinformaticians, social scientists, and software developers, with the backing of the University of Tartu administration and private companies.

The study provided the government with valuable insights that informed policy decisions throughout the pandemic. It assessed COVID-19 prevalence, antibody presence in the population, vaccine effectiveness, public sentiment towards vaccination and restrictions, and changes in behaviors such as handwashing, avoiding contact, and reducing shopping trips.


## Who is the prevalence study showcase intended for?

This showcase is intended for researchers, data scientists, policymakers, and other stakeholders planning and designing large-scale epidemiological studies. It aims to provide insights and practical guidelines on managing the various technical, statistical, and logistical challenges encountered in such studies. It exposes lessons learned that can help the design of future actions.


## What is the showcase?

### The aim of the prevalence study

The prevalence study in Estonia aimed to identify and track SARS-CoV-2 infections within the population. This involved determining the actual prevalence rates across various demographic groups such as age, sex, county, and nationality, as well as among asymptomatic individuals.

The study also focused on the dynamics of the virus' spread over time. By monitoring how the number and proportion of infected individuals changed, researchers could identify associated factors and assess the effectiveness of public health measures. This dynamic tracking was useful for responding to the pandemic in real-time and evaluating the effect of interventions.

With the introduction of vaccines and antibody tests in 2021, the study's scope expanded to include blood sampling and antibody quantification. This allowed researchers to evaluate the effectiveness of different vaccines and understand the likelihood of repeated COVID-19 infections. By tracking antibody levels, the study provided insights into the immune response within the population, contributing to better-informed public health strategies.

Each survey wave (33 in total) included approximately 2500 respondents. After the wave ended, the research team presented interim summaries to the government, which served as the basis for assessing and modifying the effectiveness of measures to curb the virus' spread. Each survey wave lasted one week. 

The population prevalence of SARS-CoV-2 and changes in the prevalence in the adult general population in Estonia during the 1st year of COVID-19 epidemic have been published in an [article](https://doi.org/10.1016/j.puhe.2022.02.004).

A subset of the positive samples were sequenced as part of the [KoroGeno-Est project](https://www.infectious-diseases-toolkit.org/showcase/korogenoest.html).


### Dashboards

We developed a closed and secured dashboard for real-time tracking of the study progress. The visualisations from the dashboard were useful for generating biweekly updates for the government.
Final conclusions and selected visualisations were shared publicly in Estonian national news and the University of Tartu [website](https://ut.ee/en/content/study-prevalence-coronavirus-estonia).


### Lessons Learned


- **Address Diminishing Response Rates Early**: Anticipate and proactively address the decline in response rates over time. Implement strategies such as targeted follow-ups, reminders, and incentives to maintain engagement and participation. This helps ensure that your confidence intervals remain tight and your statistical analysis remains robust.
- **Implement Adaptive Weighting Strategies**: Be prepared to adjust your weighting methods as response rates may correlate with specific behaviors or attitudes, such as willingness to be vaccinated. Regularly review and recalibrate your weighting to accurately reflect the changing demographics of your study population, ensuring your findings remain valid and representative.
- **Plan for Evolving Study Designs**: Recognise that societal needs and public health conditions can change rapidly, affecting the scope and requirements of the study. Build flexibility into your study design from the outset, and regularly re-evaluate and adapt your technical and data strategies as the study progresses. This ensures that your study remains relevant and responsive to current conditions.
- **Standardise Technical Tools and Pipelines**: Establish and communicate clear technical standards and preferred tools for your interdisciplinary team early on. Create a unified workflow and data pipeline to ensure consistency and compatibility across different technologies and skill sets. This helps streamline collaboration, reduces errors, and maximises efficiency.
- **Restrict Freeform Responses to Protect Privacy**: Avoid using freeform response fields where respondents can inadvertently provide personally identifiable information. Instead, use structured response options to control the type of data collected. This approach simplifies data classification and analysis, reduces the risk of privacy breaches, and ensures compliance with data protection regulations.
- **Prioritise Privacy-Conscious Data Collection**: Design your data collection process to gather only the information that is essential for your analysis while avoiding combinations of demographic details that could lead to the identification of individuals. This helps to maintain participant confidentiality and trust, and ensures that your data practices comply with ethical standards and legal requirements.
- **Manage Knowledge Transfer Effectively**: Long-term studies often involve changes in personnel and collaborators. Develop robust processes for training new team members and transferring knowledge efficiently. Document roles, processes, and key insights comprehensively to ensure continuity and minimise disruptions due to staff turnover.
- **Emphasise Early Documentation**: Start your project with a strong focus on comprehensive documentation practices. Maintain detailed records of methodologies, decisions, and changes throughout the study. Good documentation facilitates onboarding, fosters transparency, and helps prevent misunderstandings and errors as the project evolves.
- **Maintain a Consistent Data Dictionary**: Keep an up-to-date and detailed data dictionary that documents the definitions, formats, and transformations of all data fields. Regularly update this resource to reflect any changes. A consistent data dictionary ensures clarity and consistency, aids in data interpretation, and enhances collaboration among team members.
- **Ensure Role Duplication and Cross-Training**: Implement role duplication from the beginning of the study to build redundancy into your team structure. Encourage cross-training to ensure that multiple team members are capable of performing key tasks. This approach mitigates the risk of knowledge gaps and operational disruptions during absences or transitions, promoting a more resilient project workflow.
- **Pay Immediate Attention to Data Issues**: Address data issues as soon as they are identified, ideally at the point of collection. Establish protocols for prompt troubleshooting and resolution to prevent problems from escalating. Timely intervention helps maintain data quality and integrity, reducing the complexity and cost of correcting issues later in the process.
- **Plan for Long-Term Commitment:** Recognise early on that long-term studies require sustained efforts and comprehensive planning.
- **Transition Quickly from Temporary to Standardised Processes**: Recognise that initial ad-hoc processes, often implemented under time constraints and high pressure, should be temporary. As soon as it becomes clear that the project will extend beyond initial expectations, shift to more robust and standardised procedures. This proactive transition helps enhance efficiency, data integrity, and overall project sustainability, moving from quick fixes to sustainable solutions.
- **Strict data quality standards:** Enforce rigorous data quality standards between partners and make data quality the provider's responsibility.
- **Comprehensive data exchange:** Avoid sending "chunked" data between partners. Always exchange the full dataset available at that point to prevent data loss and potential confusion.
- **Timely processing:** Implement a time limit for all stages of the process to ensure timely responses and reduce the complexity of late-stage data processing.


## What can you use the SHOWCASE for?

The showcase can be used as a resource for understanding the key lessons learned during the COVID-19 prevalence study in Estonia. It offers practical advice on preparing for long-duration studies, enforcing data quality standards, managing privacy issues, and maintaining effective communication among interdisciplinary teams. 

Whilst the code underlying the data handling and dashboards is not publicly available, the team is happy to discuss it with researchers developing similar solutions. The best way is to send an email to [ELIXIR-Estonia](elixir@ut.ee).

### External links to resources relevant to the prevalence showcase

- [The study website](https://ut.ee/en/content/study-prevalence-coronavirus-estonia)


## Acknowledgements

The study was approved by Research Ethics Committee of the University of Tartu.

Core team at University of Tartu: Data handling and analysis solutions: Uku Raudvere, Mihkel Solvak, Liis Kolberg, Jaak Vilo, Hedi Peterson; Statistical design and analysis: Meelis Käärik, Ene-Margit Tiit, Krista Fischer, Tuuli Jürgenson; Sequencing: Tuuli Reisberg, Lili Milani, Mait Metspalu; Epidemiological analysis: Anneli Uusküla; Ethical considerations: Aime Keis; Project oversight and public appearance: Ruth Kalda, Mikk Jürisson, Kristjan Vassil.

AS Kantar-Emor 
OÜ Medicum Eriarstiabi 
SYNLAB Eesti OÜ


### Support
