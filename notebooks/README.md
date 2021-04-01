## Data Description
---

The study was carried out using Python 3.7 and Jupyter Notebooks. The input and output data files are `csv` and `xls` formats.

### Requirenmetns
`python -m spacy download en_core_web_sm`

### CORDIS data

The original files can be found in the original EU Open Data Portal landing page. This data will always contain the last updated version: [H2020 programmes](https://data.europa.eu/euodp/en/data/dataset/cordisref-data/resource/9840dedb-5abb-4724-a72c-6be08d3413f8)

The version of the data that is used for this study is the following  
`data/cordis-h2020projects.xlsx`

---

## Notebooks and files details

- `tech_example.xls`: A shot version of results csv (tech.csv)
- `sample_to_tag.csv`: Selection of projects to be manually tagged by an expert
- `sampleTagged.xls`: Selection of projects tagged
- `mitigation-technology-catalogue.xls`: Annotated catalogue of climate change mitigation technologies manually gathered from policy documents by an expert

- Notebook: `CleanTechTag-DeterministicModel.ipynb`  
    - Input `../data/mitigation-technology-catalogue.xls`
    - Input `../data/cordis-h2020projects.xlsx`
    - Output `../data/cleantechtag_deterministic_results.csv`

- Notebook: 
    `CleanTechTag-ProbabilisticModel.ipynb`
    - Input `../data/mitigation-technology-catalogue.xls`
    - Input `../data/cordis-h2020projects.xlsx`
    - Output `../data/cleantechtag_probabilistic_results.csv`

- Notebook: 
`CleanTechTag-DataAnalysis.ipynb`
    - Input `../data/cleantechtag_deterministic_results.csv` 
    - Input `../data/cleantechtag_probabilistic_results.csv`
    - Input `../data/mitigation-technology-catalogue.xls`
    - Output `../data/sample_to_tag.csv` 

- Notebook: 
`Final-Results.ipynb`
    - Input `extensive_catalogue.csv`
    - Input `cleantechtag_joint_results.csv`
    - Output `cordis-h2020projects-filtered-by-CleanTechTag-Final.xls`

- Selected sample for manual assesment
    - Output `../data/joint_results_cleantechtag.csv` Intersection between prob and det results
    - Output `../data/extensive_catalogue.csv` 
    - Output `../data/not_invested_technologies.csv` categories not invested
    - Output `../data/not_invested.xlsx` corresponds to the one above, this one is used in the article

--- 

## Annotation guidelines `cordis-h2020projects.xlsx`

The overall goal is to identify how much funding goes to technologies of climate change mitigation.  

Mitigation of climate change means here a human intervention to reduce the sources or enhance the sinks (= storage places) of greenhouse gases, such as carbon dioxide (CO2) or methane (CH4). Examples: increase of energy efficiency, solar power, afforestation; and NOT preparing shorelines for flood or nature conservation (because this is adaptation to climate change).  

Technology means here a configuration of processes, knowledge and material that together fulfil a function. Examples: car, chair, wood carving, showering, planting crops; and NOT corn or public meeting.  

Examples of climate change mitigation technology: wind turbine blade, heat pump, food packaging, power plant, algae for energy generation; and NOT awareness campaign, general research network that is not tied to a specific technology, educational tool.  

1)	Read project objective (column L).
2)	Does the objective mention that the project’s outcomes would lead to mitigation of climate change (perhaps among other goals)? If yes, then go to step 3; if no, discard project.
3)	Reading the objective, is the project about (or is promised to lead to) a new or adjusted technology? If yes, then go to step 4; if no, discard project.
4)	Add project.
When in doubt, you can ask: can this project lead to developing or improving a technology that would help reduce greenhouse gas emissions? If yes, then add.
