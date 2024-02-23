[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3570769.svg)](https://doi.org/10.5281/zenodo.3570769)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Green](https://img.shields.io/badge/green-project-green)

---

## A qualitative-computational cataloguing of the EU-level public research and innovation portfolio of clean energy technologies (2014–2020)

**Dataset available in DataverseNL at: [dataverse.nl/doi:10.34894/Q80QUE](https://dataverse.nl/dataset.xhtml?persistentId=doi:10.34894/Q80QUE)**

To better allocate funds in the new EU research framework programme Horizon Europe, an assessment of current and past efforts is crucial. In this paper **we develop and apply a multi-method qualitative and computational approach to provide a catalogue of climate crisis mitigation technologies on the EU level between 2014 and 2020**. Using the approach, we observed no public EU-level funding for multiple technologies prioritised by the EU, such as low-carbon production and use of cement and chemicals, electric battery, and a number of industrial decarbonisation processes. We observed a rising trend in the funding of solar power and onshore wind, the adjacent to them power-to-X technology, as well as recycling. At the same time, the shares of funding into fuel cell, biofuel, demand-side energy management, microgrids, and waste management show a decline trend. With note of the exploratory character of the present paper, we propose that the EU Horizon 2020 funding of clean technologies only partially reflected the expectations of key institutionalised EU actors due to the existence of many non-funded prioritised technologies.

> The description and details of the computational framework and data analysis together with the data and file usage is described here: **[Data Analysis Description](https://github.com/MaastrichtU-IDS/clean-technologies-nlp/tree/master/notebooks/README.md)**

---

### Projects detected by CleanTechTag framework 
![](images/figure1.png)  

---

### Total cumulative number of projects and total contribution in million euro made by the EU per sector and technology group during the H2020 framework programme. 
![](images/figure3.png)  

---

### Prioritised (below) and non-prioritised (above) technologies costing 50 mln and less, per sector
![](images/figure4b.png)  

---

### Funding dynamics of the most important clean technologies over time.
![](images/figure4.png)  

---
## Citation

```latex
@article{KORETSKY2021100084,
title = {A qualitative-computational cataloguing of the EU-level public research and innovation portfolio of clean energy technologies (2014–2020)},
journal = {Current Research in Environmental Sustainability},
volume = {3},
pages = {100084},
year = {2021},
issn = {2666-0490},
doi = {https://doi.org/10.1016/j.crsust.2021.100084},
url = {https://www.sciencedirect.com/science/article/pii/S2666049021000608},
author = {Zahar Koretsky and Pedro V. {Hernández Serrano} and Seun Adekunle and Michel Dumontier},
keywords = {Innovation policy, Mitigation, Horizon 2020, Clean technology, Sustainability, Text mining}
}
```
---
## Access Protocols 🔐 

All Digital Objects (DOs) contained in this repository (i.e. Software, Datasets) are **[Open Access](https://en.wikipedia.org/wiki/Open_access)**, meaning that they are retrievable with a standard HTTP request from any browser such as cloning the repository, curl the resource or sumply pressing the download bottom. 👆🏼  

<img src="https://s3.amazonaws.com/libapps/accounts/33900/images/OAlogo.jpg" width="230" height="80">

- The repository can also be downloaded in  Zenodo at [zenodo.org/record/4657236](https://zenodo.org/record/4657236/files/MaastrichtU-IDS/clean-technologies-nlp-1.0.zip?download=1) and at Dataverse at [dataverse.nl/doi:10.34894/Q80QUE](https://dataverse.nl/dataset.xhtml?persistentId=doi:10.34894/Q80QUE)

- **SPARQL Endpoint**  
Unfortunately, this data does not have a data service available due to a lack of resources; however, the dataset `../data/joint_results_cleantechtag.csv` is semantically annotated following the standard vocabularies following the FAIR principles; therefore, you could easily set up a local SPARQL endpoint.
1. Open your terminal (you need Python installed)
2. Install the following 

`pip install rdflib-endpoint@git+https://github.com/vemonet/rdflib-endpoint@main`

3. Expose the RDF file to the local service 

`rdflib-endpoint serve ../data/cordis-cleantechtag.nt`

4. Go to your localhost at [http://0.0.0.0:8000](http://0.0.0.0:8000)

---
## Terms of Use 📃

*Copyright (C) 2021, Zahar Koretsky, Pedro V. Hernández Serrano, Seun Adekunle.*  

**Research Software LICENSE**  
[The code contained in this Github repository](https://nbviewer.org/github/MaastrichtU-IDS/clean-technologies-nlp/tree/master/notebooks/) is free software: you can redistribute it and/or modify it under the terms of the [GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.html) as published by the Free Software Foundation, either version 3 of the License, or any later version.

**Data LICENSE**  
The data terms of use are specific for this research project. There can be found in **[/clean-technologies-nlp/data/LICENSE](https://github.com/MaastrichtU-IDS/clean-technologies-nlp/tree/master/data/README.md)** document.

