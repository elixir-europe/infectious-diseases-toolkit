---
title: Switzerland
country_code: CH
contributors: [Aitana Neves, Patricia Palagi] 
coordinators: [Aitana Neves]

national_resources: 
  - name: Swiss Pathogen Surveillance Platform (SPSP)
    description: SPSP is a secure One-health online platform that enables near real-time sharing under controlled access of pathogen genomic data and their associated clinical/epidemiological metadata. During COVID-19, it served as the Swiss SARS-CoV-2 genomic data hub, collecting data, annotating it, communicating reports to the federal public health authorities and openly re-sharing anonymised data on the Covid-19 Data Platform.
    how_to_access: The resource contains sensitive data and is only accessible to registered users (IP white-listing and two factor authentication). Anonymised data are shared on the ENA.
    instance_of:
    related_pages:
      data_sources: [pc_data_sources]
      provenance: [pc_provenance]
      quality_control: [pc_quality_control]
    url: https://www.spsp.ch
    registry:
      biotools:
      fairsharing:
      tess:
  - name: Research Data Management (RDM) sources in Switzerland
    description: RDMkit page on Switzerland's RDM guidelines and resources.
    how_to_access: 
    instance_of:
    related_pages:
      pathogen_characterisation:  
    url: https://rdmkit.elixir-europe.org/ch_resources
  - name: COVID-19 Data Portal aggregation of Swiss COVID-19 data
    description: COVID-19 Data Portal aggregation of Swiss COVID-19 data
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: 
    url: https://www.covid19dataportal.org/search?query=switzerland&requestFrom=searchBox
  - name: V-pipe
    description: V-pipe is the bioinformatics pipeline that integrates various open-source software packages for assessing viral genetic diversity from next-generation sequencing (NGS) data derived from intra-host virus populations
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_analysis] 
    url: https://cbg-ethz.github.io/V-pipe/
  - name: ViralZone
    description: ViralZone is a SIB Swiss Institute of Bioinformatics web-resource for all viral genus and families, providing general molecular and epidemiological information, along with virion and genome figures. Each virus or family page gives an easy access to UniProtKB/Swiss-Prot viral protein entries
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_sources] 
    url: https://viralzone.expasy.org
  - name: Nextstrain
    description: Nextstrain is an open-source project to harness the scientific and public health potential of pathogen genome data. It provides a continually-updated view of publicly available data alongside powerful analytic and visualization tools for use by the community. The goal is to aid epidemiological understanding and improve outbreak response 
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_analysis] 
    url: https://nextstrain.org
  - name: CoV Spectrum
    description: CoV-Spectrum is an interactive tool to analyze and discover variants of SARS-CoV-2. Main features include a powerful search engine that supports amino acid and nucleotide mutation filtering, the comparison of multiple variants, and a built-in fitness advantage estimation model. 
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_sources] 
    url: https://cov-spectrum.org/explore/Europe/AllSamples/Past6M
  - name: Covariants
    description: CoVariants provides an overview of SARS-CoV-2 variants and mutations that are of interest. It displays what mutations define a variant, what impact they might have (with links to papers and resources), where variants are found, and link the variants in Nextstrain.  
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_sources] 
    url: https://covariants.org/
  - name: COVTriage
    description: COVTriage is a search engine developed as part of SIBiLS (Swiss Institute of Bioinformatics Literature Services), which purpose is to rank the COVID-19 literature (Medline, PMC, Cord-19) according to the 9 axes of the COVoc ontology (controlled vocabulary to support literature triage for COVID-19). This resource supports COVID-19 / SARS-CoV-2 research.
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_sources] 
    url: https://candy.hesge.ch/COVTriage/
  - name: Computational Linguistics for COVID-19
    description: To process COVID-19-related scientific publications automatically to detect mentions of domain-specific entities of particular relevance (such as genes, symptoms, drugs, organs, etc.). To enhance accessibility to the literature, for example, simplifying the search of papers dealing with a particular gene or identifying unexpected connections between different entities.
    how_to_access: 
    instance_of: 
    related_pages:
      pathogen_characterisation: [pc_data_analysis] 
    url: https://covid19.nlp.idsia.ch/

---

## Introduction 
<!---General Infectious diseases data considerations for your country--->

Switzerland is a federal republic composed of 26 cantons. Switzerland's health system is highly decentralised, with significant responsibility for public health measures and policies resting with the country's cantons. The [Federal Office of Public Health](https://www.bag.admin.ch/bag/en/home.html) (FOPH) is responsible for coordinating national health policies, but the cantons have a high degree of autonomy in implementing these policies.


## Health authorities
<!--- A section to list and provide context to agencies/authorities/institutions which define public health measures and policies --->
The FOPH plays a critical role in setting national public health goals and guidelines, overseeing the country's health insurance system, and coordinating responses to public health emergencies. It has a Communicable Diseases Division in charge of monitoring, publishing regular reports on the epidemiological situation, and laying down and implementing prevention and control strategies. The FOPH also manages national health registries and monitors health indicators, such as disease incidence rates and vaccination coverage. FOPH may also require laboratories, healthcare institutions and other institutions of the cantons to communicate their stocks of therapeutic products, protective equipment and other medical goods essential for maintaining healthcare capacities. In 2023, the Swiss Government (FOPH, the [Federal Statistical Office](https://www.bfs.admin.ch/bfs/en/home.html), and the [Federal Department of Home Affairs](https://www.edi.admin.ch/edi/en/home.html)) launched [DigiSanté](https://www.bag.admin.ch/bag/fr/home/strategie-und-politik/nationale-gesundheitsstrategien/digisante.html), a national programme to foster the digital transformation of the Swiss healthcare systems. DigiSanté will create an ecosystem where different actors produce, use and process data within and for the benefit of healthcare.

In addition to the FOPH, there are several other agencies and institutions involved in shaping public health policy and research in Switzerland. These include a network of National Reference Centers, Swiss societies for microbiology and infectious diseases,  the [Swiss Academy of Medical Sciences](https://www.samw.ch/en.html), the [Swiss Tropical and Public Health Institute](https://www.swisstph.ch/en/about), lobbies and the [Swiss National Science Foundation](https://snf.ch/en), among others.

Switzerland also participates in international public health organisations, such as the World Health Organization (WHO) which provide guidance and support for public health measures at the national and international level.

In March 2020, the Swiss Federal Council declared a state of emergency and announced a series of measures to control the spread of SARS-CoV-2, restricting the cantons’ power of decision. Country's extensive network of laboratories, composed of 15 university hospital centres, private laboratories and high-throughput sequencing platforms,  ramped up testing capacity to identify new cases. A national genomic surveillance program was notably implemented by the Reference Laboratory for Emerging Viral Infections in collaboration with the FOPH. The genomic data were generated by the laboratories and fed into the [Swiss Pathogen Surveillance Platform](https://www.spsp.ch) (SPSP),  which sent automatic variants reports to FOPH, allowing it to have and provide regular updates on the variants of concern on the [national dashboard](https://www.covid19.admin.ch/en/overview).  Together with other contextual data, it supported FOPH in issuing guidance to the public on how to prevent the spread of the virus. The government also launched a contact tracing app to help identify potential COVID-19 cases and prevent further transmission. 

On 1 April 2022, Switzerland returned to a normal situation, and responsibility for measures to protect the population moved back to the cantons. The measures can therefore differ from one canton to another.

## Disease surveillance initiatives

Switzerland has a well-established disease surveillance system that plays a critical role in monitoring and responding to outbreaks of infectious diseases. Here are some of the key disease surveillance initiatives in Switzerland:

* FOPH coordinates a [sentinel surveillance system](https://www.bag.admin.ch/bag/en/home/krankheiten/infektionskrankheiten-bekaempfen/meldesysteme-infektionskrankheiten.html) for monitoring a range of infectious diseases including influenza-like illness or COVID-19 cases. It involves a network of healthcare providers who report data on disease incidence and trends. Samples may also be sent to national reference laboratories for further characterization e.g., by PCR or sequencing.
* Swiss Paediatric Surveillance Unit: The [Swiss Paediatric Surveillance Unit](https://www.spsu.ch/en/home) (SPSU) is a national survey system to document rare paediatric pathologies and rare complications of more common diseases by children treated in hospitals in Switzerland, including those caused by some infectious disease.
* National Notification System: The FOPH National Notification System requires healthcare providers to report cases of certain infectious diseases to the FOPH. This system enables the FOPH to track the spread of diseases, identify outbreaks, and initiate public health responses.
* Laboratory surveillance: Switzerland has an extensive network of National Reference Centers that are involved in disease surveillance, including the [CRIVE/NAVI](https://www.hug.ch/laboratoire-virologie/centre-national-reference-pour-infections-virales) - the National Reference Center for Influenza and Emerging Viruses, and [Anresis](https://www.anresis.ch/) - the Swiss Centre for Antibiotic Resistance surveillance. These laboratories conduct diagnostic tests and monitor trends in disease activity.
* Hospital-based surveillance of Influenza and COVID-19 ([CH-SUR](https://www.unige.ch/medecine/hospital-covid/)): the Geneva University Hospitals, the Institute of Global Health at the University of Geneva, and the FOPH maintain an Influenza and COVID-19 hospital-based sentinel surveillance system. This registry records clinical and epidemiological information on Influenza, COVID-19 and other respiratory virus infections, collecting data from 18 Swiss hospitals. 
* Travel health surveillance: Switzerland also has a system for monitoring the health of travellers, particularly those returning from high-risk areas. The system involves screening travellers for symptoms of infectious diseases and providing them with information and guidance on how to prevent the spread of disease.

All these surveillance initiatives are funded by the FOPH and coordinated by them or in collaboration with institutions and laboratories. In the specific case of COVID-19, all the national monitoring efforts are summarised [here](https://www.bag.admin.ch/bag/en/home/krankheiten/ausbrueche-epidemien-pandemien/aktuelle-ausbrueche-epidemien/novel-cov/situation-schweiz-und-international/monitoring.html).

## Dashboards and visualisation platforms

* [Dashboard COVID-19 Switzerland FOPH  overview](https://www.covid19.admin.ch/en/overview)
* [COVID-19 Data Portal direct access to Swiss COVID-19-related data](https://www.covid19dataportal.org/search?query=switzerland&requestFrom=searchBox )


## National data sources
<!--- A section to list and provide context to national data sources. In the context of BY-COVID, a data source can be a repository which should include at least the metadata and ideally the data, that might not be directly available when considering sensitive data. Also, repositories should have the capacity to share this data and therefore have a governance model in place on how to do it. It can also include registries of data sources important for the field, with a direct link to the original data sources to be able to request access to the data. --->


* [SPSP](https://www.spsp.ch/) - A secure One-health online platform that enables near real-time sharing under controlled access of pathogen whole genome sequences (WGS) and their associated clinical/epidemiological metadata. Since 2021 it has centralized and processed all SARS-CoV-2 sequencing data within the national genomic surveillance program. 
* [Swiss Biobanking Platform](https://swissbiobanking.ch/sbp-directory/) - a list of aggregated information on Swiss biobanks and infrastructures.
* [Swissmedic](https://www.swissmedic.ch/swissmedic/en/home/humanarzneimittel.htm) - The Swiss entity who authorises distribution in Switzerland of any medicinal products.
* [SPHN Consortium on Maelstrom](https://sphn.ch/network/data-coordination-center/maelstrom/) - Among them the Swiss HIV Cohort study http://www.shcs.ch/
* [Anresis](https://www.anresis.ch/) - The Swiss Centre for Antibiotic Resistance is a nationwide, representative surveillance system and research instrument for antibiotic resistance and consumption. It is led by the Institute for [Infectious Diseases](https://www.ifik.unibe.ch/index_eng.html) (IFIK) of the University of Bern and is financially supported by the FOPH and the IFIK.

## Regulations
<!--- Ethical and legal regulations in the country, committees etc --->

### Ethics

Appointed by the Federal Council, the supreme executive and directorial authority of the Swiss Confederation, the [Swiss National Advisory Commission on Biomedical Ethics](https://www.nek-cne.admin.ch/en/homepage-nek-cne/page) (NCE) advises the authorities from an ethical perspective in the field of human biomedicine. It also counts on the support from the [Swiss Academy of Medical Sciences](https://www.samw.ch/en.html),  an independent institution that provides general guidance on ethical issues in medicine and healthcare, e.g. for the triage of Covid-19 patients. It develops guidelines and recommendations for medical professionals, policymakers, and the public.

Regarding research, the [Swiss National Ethics Committee](https://swissethics.ch/en) is the umbrella organisation of the cantonal Ethics Committees in charge of reviewing and approving study protocols. 

### Laws and regulations  

The Communicable Diseases Legislation aims to enable a timely detection, monitoring, prevention and control of infectious diseases. It revolves around the Federal Act of 28 September 2012 on Controlling Communicable Human Diseases (Epidemics Act, EpidA) and ordinances. A revised version should be presented in June 2023.

The use of human data in research is regulated by Human Research Legislation, and in particular the Human Research Act and Ordinances. The legislation is designed to safeguard the dignity, privacy and health of people involved in research.

<!---## Domain-specific infrastructures or resources 
 e.g. human data, covid-19. Please, only add domain-specific resources that you think don't fit in the table at the bottom

SPHN?

S3C ? the Swiss SARS-CoV-2 Sequencing Consortium was until the end of 2022 the largest SARS-Cov-2 sequencing effort in Switzerland. Together with multiple diagnostic labs and sequencing centres, they have established a workflow for the surveillance of up to thousands of samples per week. Information on these samples is shared within a short turnaround time with the FOPH and also with GISAID and ENA with the help of SPSP. 

Wastewater initiatives?

--->
