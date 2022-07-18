# GBA-KG 

![Release](https://img.shields.io/badge/Release-Ver1.0.0-blue.svg)

Gut-brain axis knowledge graph(GBA-KG) is a knowledge graph that integrates existingknowledge graphs in the biomedical field and information on microbiology and psychiatry in the literature. GBA-KG integrates a large number of biomedical resources, describing the relationship between microorganisms, genes, diseases, anatomy, compounds, molecular functions, biological processes, cellular components and pathways, expanding the knowledge map in microbial psychiatric diseases. We describe the process from prototyping GBA-KG to information extraction and information updating. It is convenient for researchers to learn, and multi-modal analysis can be combined with machine learning algorithms in the future.  

## Cloning and installing 

The setting up of the GBA is easy and might just take a few mintues.To get a copy of the GitHub repository on your local machine, please open a terminal windown and run:  
```
git clone https://github.com/liwenqingi/GBA-KG.git
```  
This will create a new folder named "GBA-KG" on your current location. After this, follow the instructions in "Building GBA-KG".  
## Building GBA-KG  
The construction of KG consists of two main steps, the first is to integrate multiple resources, the second is to acquire knowledge from literature and update it.  
### Integrate multiple resources  
Ontology resources can be load into neo4j by `run_kg_creation.py`.The ontology databases and hetionet knowledge graph provided within the GBA-KG have their own licenses and the use of GBA-KG still requires compliance with these data use restrictions. Please, visit the data sources directly for more information:  

| Source type | Source | URL |
| --- | --- | --- |
| Ontology | Human Disease Ontology | https://www.ebi.ac.uk/ols/ontologies/doid | 
| Ontology | OGG: Ontology of Genes and Genomes | https://www.ebi.ac.uk/ols/ontologies/ogg |
| Ontology | NCBI organismal classification | https://obofoundry.org/ontology/ncbitaxon.html |
| Ontology | Chemical Entities of Biological Interest | https://www.ebi.ac.uk/ols/ontologies/chebi |
| Ontology | Uber-anatomy ontology | https://www.ebi.ac.uk/ols/ontologies/uberon |
| Ontology | Gene Ontology | https://www.ebi.ac.uk/ols/ontologies/go |
| Knowledge Graph | Hetionet | https://github.com/hetio/hetionet | 
### Literature knowledge acquisition
Document information can be manually organized into triples and imported. For the currently supported relationships, please refer to the a file. At the same time, we use NLP methods to accelerate this process.  
![Process](https://github.com/liwenqingi/GBA-KG/blob/main/NLP_process.png)
