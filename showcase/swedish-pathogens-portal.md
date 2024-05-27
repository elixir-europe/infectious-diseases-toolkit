---
title: The Swedish Pathogens Portal
contributors:
  [Liane Hughes, Katarina Öjefors Stark, Anna Asklöf, Elisabeth Sundström]
description: A web portal that provides information about available datasets, resources, tools, and services related to pandemic preparedness in Sweden. We offer support to all those involved in pandemic preparedness research that are affiliated with a Swedish research institution or university.
affiliations: [SE, SciLifeLab]
page_id: swedish_pathogens_portal
related_pages:
  showcase: [korogenoest, covid19_galaxy_project]
training:
---

## Introduction

Sharing data as openly and FAIRly as possible is key in accelerating research progress. The importance of this was perhaps never more widely acknowledged than during the COVID-19 pandemic, when it was done at unprecedented levels in order to mitigate the impacts of the pandemic on society. In early 2020, multiple partners worked together to launch [the European COVID-19 Data Platform](https://www.embl.org/news/science/embl-ebi-launches-covid-19-data-portal/) to facilitate FAIR and open sharing. Part of this Platform was the {% tool "covid-19-data-portal" %}, which was the primary web interface to the Platform.

A network of national portals, similar to the {% tool "covid-19-data-portal" %}, was established to facilitate data sharing by individual countries. Sweden was the first country to launch their national portal; the Swedish COVID-19 Data Portal was launched in June 2020. The scope of the national portal has since expanded and shifted in accordance with the needs and interests of the research community. This showcase describes the Portal, now known as the {% tool "swedish-pathogens-portal" %}, and how the content and scope has changed over time. The showcase could enable others to establish national/local portals in a health emergency, like a pandemic, and provides insight as to how the scope of such portals can be changed to ensure preparedness for future emergencies.

## Who is the showcase intended for?

The primary target audience for the {% tool "swedish-pathogens-portal" %} is the Swedish research community. The Portal also has multiple secondary audiences, including individuals involved in industry, healthcare, policy making, as well as the general public (primarily in Sweden). The content of the Portal is also often viewed internationally, and can be made use of by those based in other countries.

## What is this showcase intended for?

The {% tool "swedish-pathogens-portal" %} provides information about available datasets, tools, and services related to pandemic preparedness in Sweden. In addition, the {% tool "swedish-pathogens-portal" %} works to accelerate research by providing support for managing data related to pathogens and/or pandemic preparedness. Direct research data management support is also available from the team behind the Portal for anyone affiliated with a Swedish research institution or university.

{% include image.html file="/Swedish_pathogens_portal.png" caption="Figure 1. Information about the groups associated with the Swedish Pathogens Portal and how data flows. We receive/retrieve data and information from multiple sources ('data and information providers'), the team works to turn this into particular types of content (e.g. data dashboards and data highlights). Our target audience ('data and information consumers') then makes use of that information. We are guided by multiple stakeholders.
" %}

### Portal history and scope

In early 2020, The [European Commission funded and initiated the European COVID-19 Data Platform](https://www.embl.org/news/science/embl-ebi-launches-covid-19-data-portal/) to facilitate data FAIR and open data sharing. Multiple partners contributed to the Platform, including European Molecular Biology Laboratory (EMBL) and European Open Science Cloud-Life (EOSC-Life). In April 2020, EMBL’s European Bioinformatics Institute (EMBL-EBI) and partners launched the {% tool "covid-19-data-portal" %} as the primary web interface of the Platform. A network of national portals was then quickly established to facilitate data sharing by individual countries. The focus of these portals was primarily on making data and information that was more specific to a given country (e.g. country-specific resources and funding opportunities) available.

Sweden was the first country to launch their national portal. This national portal was originally launched as The Swedish COVID-19 Data Portal in June 2020. The Portal was developed on [assignment from the Swedish Research Council (Vetenskapsrådet)](https://www.vr.se/english/just-now/news/news-archive/2020-06-03-new-national-portal-makes-research-data-on-covid-19-accessible.html). The [initial scope of the Portal was to facilitate and promote FAIR and open sharing of COVID-19 data](https://pathogens.se/updates/first_year/) originating from Swedish research institutions, universities, and other organisations. All of the code for the Portal, including the [code needed to generate the website](https://github.com/ScilifelabDataCentre/covid-portal), the [visualisations shown on the Portal](https://github.com/ScilifelabDataCentre/covid-portal-visualisations), and [other scripts used to collect data](https://github.com/ScilifelabDataCentre/covid-portal-scripts), were shared openly from the outset. This enabled others to make use of the code, and it was quickly reused by other countried to make their own national portals e.g. {% tool "estonian-covid-19-data-portal" %}.

In 2022, the Portal became part of the [SciLifeLab Pandemic Laboratory Preparedness programme](https://www.scilifelab.se/pandemic-response/pandemic-laboratory-preparedness/), which is based on government funding awarded to SciLifeLab ([Research proposition Prop. 202/21:60](https://www.regeringen.se/rattsliga-dokument/proposition/2020/12/forskning-frihet-framtid--kunskap-och-innovation-for-sverige/)). At this point, the scope of the Portal was expanded to include data and information about not only COVID-19, but also other pathogens and pandemic preparedness in general. This reflected a shift in the needs and focus of the research community towards pandemic preparedness and away from COVID-19 specifically. The Portal was thus renamed ‘The Swedish COVID-19 and Pandemic Preparedness Portal’. At this time, the Portal continued working with multiple national and international organisations in order to determine how the research community should transition resources established for COVID-19 to ensure future pandemic preparedness.

In 2023, the Portal was rebranded as ‘{% tool "swedish-pathogens-portal" %}’, and it became the first national node of the {% tool "pathogens-portal" %}. This was in line with ongoing efforts across the global research community to ensure that resources developed for COVID-19 could be maintained for future pandemics. These efforts are key in ensuring a faster and more efficient response in the event of future outbreaks or pandemics. The scope of the Portal now extends to all topics related to pandemic preparedness, including general infectious disease biology.

### Portal aims

- To provide research data management support in order to make research data related to pandemic preparedness and pathogens as open and FAIR as possible.
- To collate data, tools, and services focused on pandemic preparedness and pathogen data.
- To promote data from the Swedish research community related to pathogens, their effects on the host, and the methods to treat and prevent infectious disease.
- To collaborate with communities at both the national and international levels.
- To act as a use case for how research communities can be built around common themes.

## What can you use the showcase for?

- To find information about available datasets related to pandemic preparedness in Sweden (e.g. [studies of the effectiveness of vaccines](https://pathogens.se/dashboards/recovac/), or [wastewater data collected to monitor for outbreaks of multiple pathogens](https://pathogens.se/dashboards/wastewater/)).
- To find information about tools related to pandemic preparedness in Sweden (e.g. the [Register Utilizer Tool (RUT)](https://pathogens.se/register-based-research/), and [pandemic preparedness capabilities](https://pathogens.se/resources/).
- To find information about services related to pandemic preparedness in Sweden (e.g. [the Swedish COVID-19 Sample Collection Database](https://pathogens.se/biobanks/), which details biobanks samples related to COVID-19).
- To promote data and/or code shared as openly and FAIRly as possible (e.g. creating dynamic, interactive [data dashboards](https://pathogens.se/dashboards/), and publishing data-centric news articles about the work, known as [data highlights](https://pathogens.se/highlights/).
- To find information about [upcoming events related to pandemic preparedness](https://pathogens.se/events/) (including events on pathogen biology, and topics such as antibiotic resistance).
- To enable the identification of potential collaborators for research projects (e.g. by checking lists of [ongoing research projects](https://pathogens.se/research_projects/)).
- To find [funding opportunities relevant for researchers in Sweden](https://pathogens.se/funding/) that work in areas related to pandemic preparedness (including infection biology and antibiotic resistance).

## How to reuse this resource

All of the code related to this resource has been made openly available. The [code needed to generate the Portal](https://github.com/ScilifelabDataCentre/covid-portal) has been reused multiple times as the basis for other national COVID-19 Data Portals. It could, in principle, be reused to generate other types of portals, including national nodes of the {% tool "pathogens-portal" %}.

Code has also been made available for features that have been integrated into this resource. This includes, for example, the [visualisations presented in our data dashboards](https://github.com/ScilifelabDataCentre/covid-portal-visualisations), for which all code is available in a separate GitHub repository. Not only could this code be used to create similar features for use on the web, the code could also be used to generate visualisations for research publications and other promotional materials. Another example would be the [code underlying the biobanks sample collection database](https://github.com/ScilifelabDataCentre/covid-sample-collection-database), which could be used as a basis for other databases.

A large amount of data has been collated on the web portal itself e.g. [data related to Swedish publications on COVID-19](https://pathogens.se/publications/). This can be downloaded and reused for other purposes, such as for machine learning.
