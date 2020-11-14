# NF_hackathon2020 

## COLLABORATIVE ONTOLOGY FOR NEUROFIBROMATOSIS

### https://nfhack-platform.bemyapp.com/#/projects/5f884652419639001b6d0174


This project created a R-package essential to start compiling & assembling the varied data published through ontologies.

Specifically, the functions retrieve ontology data, based on a term, from BioOntology Repository, and parse it to get a combined ontology of the term. The reason for using BioOntology is mentioned in the 'Presentation Script' (unfortunately, time to record a presentation was not found as there weren't additional members, likely due to the seemingly complicated methods for handling Ontologies and inexperienced former opinion of the trivialities of making an Ontology). 

However, this package is ready to be published as an ongoing project to connect to the base of a domain's knowledge base (Ontologies) via published data.

The R package can be found here: 

https://github.com/KrishnaTO/OntologyTermAggregator


The demo is available here: https://github.com/KrishnaTO/NF_hackathon2020/blob/main/Demo/SearchviaCombinedOntology.Rmd

The input used, Searchtoclasses_json.RData, is just a pre-downloaded convinience data object to be called for efficiency purposes from within the script. It will not be useful for any other term substitution other than the default within the demo.

The outputs are combined_output.csv, which hold the unique IDs, Descriptions, IRI links and other variables from the script, and the latter combined_output.complex.RData which holds the properties and metalinks for the term sources. At this time, the data can be followed by their variable names within the R global environment, and further development will follow due to time constraints.

To reproduce these results, please clone this repo, and run the Demo Rmd file. To fully use the functionality, you will have to obtain a BioOntology API Key (freely available [via signup/account settings](https://bioportal.bioontology.org/account)). If prefer not to, the input data will allow you to continue running the script from line 61. 

## Conclusion/Discussion: 

Future considerations and TODOs for this package were originally outlined in the [Presentation Script](https://github.com/KrishnaTO/NF_hackathon2020/blob/main/Presentation%20Script) and quoted here:

Some additional potentials include exporting in Protege readable RDF format, which will allow researchers to visualize and share the term graphs relatively more easily.

*Another is to rank terms by various factors to add some simplications before domain experts are required to curate.
R can also be used to directly output the associations directly, instead of relying on Protege.
These functions can also be extended to expand the trees with parents / children fitting of this combined term.
Lastly, the overwhelming opportunity of applying Natural Language Processing to simplify the aggregated axioms, just as much as you can use NLP to process written articles to build upon term usage.*

Future collaborators would ideally include the skills I'm sorely lacking, especially being able to run the OWL API, compiled from java. As well, collaborators who may have NLP knowledge to automate cleaning up the rampant minor modifications present throughout the results would be of great help. Lastly, anyone looking to decrypt RDF/XML syntax data for building knowledge graphs would be welcome!
