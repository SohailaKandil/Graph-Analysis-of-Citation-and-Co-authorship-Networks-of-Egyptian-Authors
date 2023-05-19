# Graph_Analysis_of_Citation_Network [![DOI](https://zenodo.org/badge/114928249.svg)](https://zenodo.org/badge/latestdoi/114928249)  
Code for reproducing the experiments, figures, and tables presented in the paper 
**Mishra, S., Fegley, B. D., Diesner, J., & Torvik, V. I. (2018). Self-Citation is the Hallmark of Productive Authors, of Any Gender. PLoS One.**  Replication steps provided in [REPLICATION.md](REPLICATION.md)  

## Data  
In this project we collect data of egyptian papers by sending API requests to semantic scholar website using the API key for a higher requests rate. Then we do analysis on them. Data collection is performed in the following Two stages:

#### 1. webscrabing google scholar (the professors profiles page) to collect a data set of the professors names and their affiliations.
+ The dataset comprises information on 13,027 researchers, including both Egyptians and individuals affiliated with Egyptian universities.
+ The data provides details about the researchers' names and affiliations.
+ This dataset is collected by scraping the Google Scholar website using Python library Selenium.
+ The data specifically focuses on researchers affiliated with the following universities: Ain Shams University, Cairo University, EJUST University, Alexandria University, Banha University, Assiut University, and Zewail University.   

#### 2. Getting the data of the papers written by these authors using semantic scholar API.
+ Final dataset: 31,508 research papers.
+ Each paper includes at least one researcher from Egypt or affiliated with an Egyptian university.
+ Paper details: title, unique paper ID, publication year, and a list of authors with their names, IDs in semantic scholar, Number of references cited and a list of all reference titles and corresponding IDs for each paper.
+ Final dataset collection methodology: Utilized Semantic Scholar API to request data for each author identified initially in the dataset collected earlier.
+ API requests limitations:
 + The Semantic Scholar API key allows a request rate of 100 requests per second.
 + The API returns a maximum of 500 authors' data for each paper.
 + The API returns a maximum of 1000 references for each paper.
[For more information on semantic scholar API requests visit: ]([URL](https://api.semanticscholar.org/api-docs?utm_medium=email&_hsmi=230452164&_hsenc=p2ANqtz-_qqTwwj9_nmTTO1Rgps8SST_95rgUi3jjt4VxwQ6BOaFkEntuUMB8csVGToUyoMQSRQzZT6HYiybCLxIdnx3v4VVoIhA&utm_content=230452164&utm_source=hs_automation))

 

## Acknowledgments
This work was made possible in part with funding to VIT from [NIH grant P01AG039347](https://projectreporter.nih.gov/project_info_description.cfm?aid=8475017&icde=18058490) and [NSF grant 1348742](http://www.nsf.gov/awardsearch/showAward?
AWD_ID=1348742). The funders had no role in study design, data collection and analysis, decision to publish, or preparation of the manuscript.

## License  
Self-citation analysis data based on PubMed Central subset (2002-2005) by Shubhanshu Mishra, Brent D. Fegley, Jana Diesner, and Vetle Torvik is licensed under a Creative Commons Attribution 4.0 International License. Permissions beyond the scope of this license may be available at https://github.com/napsternxg/PubMed_SelfCitationAnalysis.
