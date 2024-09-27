---
title: An automated pipeline for analysing brain autoradiography images
contributors: [Isabel Kemmer] 
description: Development of an open source, semi-automated processing pipeline for aligning autoradiography images from mouse brain tissue to study infection-induced neuroinflammation funded by the ISIDORe project. 
affiliations: [European Union, Euro-BioImaging, ISIDORe]
page_id: brain_autoradiography

---

## Introduction 

Coronavirus disease 2019 (Covid-19) has been linked to a range of neurological conditions, including neuroinflammation and impaired energy metabolism in the brain. In the field of neuroscience, a variety of tracers are frequently employed to investigate diverse aspects of brain health and dysfunction. Indeed, recent articles have demonstrated the presence of pronounced inflammatory processes in the brains of long COVID patients, by the use of inflammatory and metabolic tracers in positron emission tomography (PET) imaging ([Guedj, E et al.](https://doi.org/10.1007/s00259-021-05215-4), [Visser, D et al.](https://doi.org/10.1101/2022.06.02.22275916)) and Autoradiography (ARG).
This showcase details the development, of an open-source, user-friendly, automated analysis pipeline for aligning and processing autoradiography images from mouse brain. Funded by the [ISIDORe project](https://isidore-project.eu/), this so called {% tool "mbat" %} facilitates enhanced efficiency, accuracy, and reproducibility in the registration and analysis of images in studies aiming to elucidate the characteristics and underlying mechanisms of neuroinflammation due to infection or other causes.

## Who is the showcase intended for?

The MBAT tool is important for life science researchers working with autoradiographic data of the mouse brain. Thematically, this analysis has been specifically designed to study neuronal changes and neuroinflammation due to (viral) infection, but is also broadly applicable to all other neuroscience topics.
Since the tool is built to be user-friendly, researchers with minimal knowledge of scientific programming can use and greatly benefit from the tool. Being open source, the pipeline can be easily adapted to individual research projects by researchers with more in-depth, advanced bioinformatics skills. The analyzed brain regions from the pipeline can be also of interest to AI and computer scientists.

## What is the showcase?

{% include image.html file="/MBAT_scheme.png" caption="Figure 1. Development of an open source, semi-automated processing pipeline for aligning autoradiography images from mouse brain tissue to study infection-induced neuroinflammation. The python-based pipeline takes input from data generated through Euro-BioImaging and is itself developed by funding from the ISIDORe project and allows users to align the images in a [Napari](https://napari.org/stable/)-based user interface to the [Allen Brain Atlas](https://portal.brain-map.org/). The full code is open source available on GitHub." alt="Image with a central symbolic computer screen with the program MBAT. Arrows flowing in and out of the screen denoting inputs (data generated through Euro-Bioimaging, Funding from ISIDORe project, Tool development with Python and Napari) and outputs (Analyzed data and Code deposition on GitHub) of the software." %}

Neuroinflammation, such as that associated with SARS-CoV-2 or other infectious diseases, can be studied using autoradiography (ARG). With higher resolution than PET, this method visualizes the anatomical distribution of a protein of interest in (animal) tissue to quantify the photostimulated intensity per unit area in brain regions of interest. Depending on the specific marker used, one can study brain inflammation or measure synaptic degeneration. Since inflammation does not occur to the same extent in all areas, it is necessary to examine specific regions of interest. Traditionally, this image analysis is quite laborious, as individual brain regions of interest have to be drawn manually each time, which leads to high heterogeneity between researchers and is additionally very time consuming.

To solve this problem, researcher Zuzana Cockova (Charles University) and Junel Solis, an image analyst at Turku BioImaging, part of the Euro-BioImaging Finnish Advanced Microscopy Node, developed an automatic pipeline for brain autoradiography image analysis, the Mouse Brain Alignment Tool. This image analysis pipeline was initially designed and applied to mouse brain ARG images acquired at the Turku PET Center, part of the Euro-BioImaging Finnish Biomedical Imaging Node, to investigate brain damage caused by COVID-19.
MBAT is a Python-based software tool that automates the ARG image analysis process, enabling researchers to focus on specific sub-regions of the brain. It includes a  Napari-based user interface that allows ARG slides of mouse brain tissue to be preprocessed and registered to topographical data from Allen Brain Atlas regions. This allows researchers to preprocess their ARG sections using different layout schemes contained in whole-slide images and automatically convert these sections into single images. The included user interface allows the user to match brain sections with the atlas and calculate mean background intensity. MBAT converts data from the Allen Institute’s Mouse Brain Atlas and stores the topographical information of various brain regions in a local database as regions of interest (ROIs), which can then be overlaid onto the ARG image. The user can translate, rotate, scale, and even edit brain region ROIs. The ARG signal for each ROI can be quantified and stored in a data file, enabling the user to process sections in smaller batches and resume the workflow later, rendering the workflow particularly user-friendly. The pipeline is available for anyone to reuse on {% tool "github" %}.

## What can you use the tool for?
 
The Mouse Brain Alignment Tool provides an automated pipeline for analyzing brain autoradiography images. MBAT allows end-users to focus on image analysis without technical interruption, thereby increasing the reliability and reproducibility of results, thus expanding the possibilities of neurobiology research. The software is open source and packaged so that anyone, even without administrator access, can download and readily use the tool.
The current iteration of MBAT is only applicable to ARG images of mouse brain, as it relies on the Mouse Brain Atlas. However, by incorporating additional standardized brain atlases, such as those for the rat animal model, it could be made more widely applicable to other brain analyses. With a few minor modifications, the tool can also be applied to a range of different image file types. In essence, the tool is useful for any application that aims to measure signals in coronal slices of the brain, whether through autoradiography or alternative staining methods, including fluorescent staining. Thus, the tool can greatly facilitate neuroinflammation research, whether induced through infectious diseases or other causes.

## Acknowledgments

Data collection: Turku PET Centre

Tool Development: Zuzana Cockova (Charles University),  Junel Solis (image analyst at Turku BioImaging, part of Euro-BioImaging Finnish Advanced Microscopy Node)

Additional help: Arina Rybina (Scientific project manager, Euro-BioImaging), Isabel Kemmer (FAIR Image Data Steward, Euro-BioImaging)

### Support

This showcase was funded by the [ISIDORe project](https://isidore-project.eu/) funded by the European Commission (Grant number 101046133). 
