# dikusa-core-ontology

Core ontology for integrating data of the partner institutions within the Dikusa-project

## Description

### The Ontology
* is used as a common core ontology to harmonize the data of the partners which internally use their own specialized ontology 
* will consist of the central entities described in the projects of Dikusa such as person, place, group, object, bibliographic item and event
* technnoloy used: RDFS, RDF-star, OWL, SHACL
* RDF-star is mainly used to include information on provenance of facts, which can be annotated to any triple in the knowöedge base
* OWL is used for labeling inverse relations
* SHACL is used to allow for validating instance data against the schema

## Validation

Using standard tools - such as those provided with Apache Jena - instance data as found in folder example_data can be validated against the schema as described by shacl constraints (under open world assumption).  
For Apache Jena: shacl v -s schema_file -d instance_data_file 

## Author

kompetenzwerkd@saw-leipzig.de

## Copyright

2022, Sächsische Akademie der Wissenschaften zu Leipzig

## License

AGPLv3
