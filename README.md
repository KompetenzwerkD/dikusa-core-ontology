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

### Visualisation
Since the ontology is rather complex and the Turtle-file which also includes the shacl-constraints is difficult to comprehend, additional visualisations have been created:
* [Person part 1](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/person_test_1.ttl&from=ttl&to=png)
* [Person part 2](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/person_test_2.ttl&from=ttl&to=png)
* [Person part 3](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/person_test_3.ttl&from=ttl&to=png)
* [Person part 4](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/person_test_4.ttl&from=ttl&to=png)
* [Place part 1](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/place_test_1.ttl&from=ttl&to=png)
* [Place part 2](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/place_test_2.ttl&from=ttl&to=png)
* [Event part 1](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/event_test_1.ttl&from=ttl&to=png)
* [Event part 2](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/event_test_2.ttl&from=ttl&to=png)
* [Object part 1](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/object_test_1.ttl&from=ttl&to=png)
* [Object part 2](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/documentation/visualisation/object_test_2.ttl&from=ttl&to=png)

### Additional Information
* [Slides in German presented on 29.04.2022](https://github.com/KompetenzwerkD/dikusa-core-ontology/blob/main/documentation/Dikusa%20Datenmodell%20Folien%2029.04.2022.pdf)

### Progress
So far Persons, Places, Events and Objects have been modeled. The classes Work and Group are currently being developed.

## Validation

Using standard tools - such as those provided with Apache Jena - instance data as found in folder example_data can be validated against the schema as described by shacl constraints (under open world assumption). For validating your own instance data against the schema please be aware that all subclass relations need to be included in your data (see supplied file in example_data) and not (only) in the schema. This is expected by shacl-tools.
For Apache Jena use the following command: shacl v -s schema_file -d instance_data_file 

## Author

kompetenzwerkd@saw-leipzig.de

## Copyright

2022, Sächsische Akademie der Wissenschaften zu Leipzig

## License

AGPLv3
