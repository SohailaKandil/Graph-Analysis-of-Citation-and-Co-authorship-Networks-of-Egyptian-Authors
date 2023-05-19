# Graph_Analysis_of_Citation_Network [![DOI](https://zenodo.org/badge/114928249.svg)](https://zenodo.org/badge/latestdoi/114928249)  
Code for reproducing the experiments, figures, and tables presented in the paper 
**Mishra, S., Fegley, B. D., Diesner, J., & Torvik, V. I. (2018). Self-Citation is the Hallmark of Productive Authors, of Any Gender. PLoS One.**  Replication steps provided in [REPLICATION.md](REPLICATION.md)  

## Data  
In this project we collect data of egyptian papers by sending API requests to semantic scholar website using the API key for a higher requests rate. Then we do analysis on them. Data collection is performed in the following Two stages:

#### 1.1. webscrabing google scholar (the professors profiles page) to collect a data set of the professors names and their affiliations.
+ The data set size is 13,027 of Egyptian researchers names and affiliations.
In the initial stage, we performed web scraping on the Google Scholar website to obtain a dataset of size 13,027. This dataset included author names and affiliations. To accomplish this, we utilized the Selenium library in Python. To prevent exceeding the data scraping rate imposed by Google Scholar, we implemented a structured approach. Specifically, we collected data for each university in a single session, ensuring sufficient time intervals between each scraping instance. The data collection process focused on researchers from prominent Egyptian universities such as Ain Shams University, Cairo University, EJUST university, Alexandria University, Banha University, Assiut University, and Zewail University.    

#### 1.2. Getting the data of the papers written by these authors using semantic scholar API.
After this step, we obtained our final dataset consisting of 31,508 research papers.This is the data set that we analyze in the project. Each paper in the dataset includes at least one researcher who is either from Egypt or affiliated with an Egyptian university. In our dataset, each paper includes important information such as its title, unique paper ID in semantic scholar, publication year, and a list of authors with their respective names and IDs in semantic scholar. Furthermore, we collected the number of references cited in each paper and added a list of all the references, including their titles and corresponding IDs for each paper in the dataset.

To collect the dataset, we utilized the Semantic Scholar API to request the data of each author identified in the initial stage. These requests enabled us to collect a dataset containing the titles, publication IDs, and publication times of their respective papers. Additionally, we used further API requests with each paper's ID to retrieve information regarding its references, number of citations, and the names of all authors associated with the publication.

## Acknowledgments
This work was made possible in part with funding to VIT from [NIH grant P01AG039347](https://projectreporter.nih.gov/project_info_description.cfm?aid=8475017&icde=18058490) and [NSF grant 1348742](http://www.nsf.gov/awardsearch/showAward?
AWD_ID=1348742). The funders had no role in study design, data collection and analysis, decision to publish, or preparation of the manuscript.

## License  
Self-citation analysis data based on PubMed Central subset (2002-2005) by Shubhanshu Mishra, Brent D. Fegley, Jana Diesner, and Vetle Torvik is licensed under a Creative Commons Attribution 4.0 International License. Permissions beyond the scope of this license may be available at https://github.com/napsternxg/PubMed_SelfCitationAnalysis.
