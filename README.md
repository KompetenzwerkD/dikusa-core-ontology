# dikusa-core-ontology

This dataset contains a central data model / ontology used for the linking of digital cultural data of research projects in Saxony, Germany. It is applied by six Saxon non-university research institutions within the [DIKUSA-project](https://www.saw-leipzig.de/de/projekte/dikusa) (Vernetzung digitaler Kulturdaten in Sachsen). Future use as a means of data integration between these partners is intended.

## Description

### The Ontology
* is used as a common core ontology to harmonize the data of the partners which internally use their own (more) specialized ontology 
* consists of the central entity types described in the sub-projects of DIKUSA such as person, place, group, object, bibliographic item and event
* technnologies used: RDFS, RDF-star, OWL, SHACL
* RDF-star is mainly used to include information on provenance of facts, which can be annotated to any triple / statement in a knowledge base
* OWL is used for labeling inverse relations
* SHACL is used to allow for validating instance data against the schema
* the RDFS-schema including SHACL-constraints can be found in: core_ontology_schema.ttl
* the RDFS-schema without SHACL-constraints can be found in: core_ontology_schema_no_shacl.ttl
* additional controlled vocabularies can be found in the vocabs-folder in SKOS-format, more will follow as results of the modelling and data acquisition processes of the sub-projects

### Documentation
* as a starting point rdfs:comment is used as a short description of every class and property
* rdfs:label provides additional labels in English and German
* descriptive web pages for all classes and properties based on these information and the structural rdfs-information will be added to thje documentation-folder at a later point
* The file core_ontology_howto.ttl found in example_data contains typical examples of usage of the data model
* Links to additional visualisations are provided in the following

### Visualisation
Since the ontology is rather complex and the Turtle-file is difficult to comprehend, additional visualisations can be created based on some mockup ttl-files:
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
* [Complex file: Real world examples as used in core_ontology_howto.ttl](https://www.ldf.fi/service/rdf-grapher?rdf=https://raw.githubusercontent.com/KompetenzwerkD/dikusa-core-ontology/main/example_data/core_ontology_howto_no_rdfstar.ttl&from=ttl&to=png)

### Additional Information
* [Slides in German presented on 29.04.2022](https://github.com/KompetenzwerkD/dikusa-core-ontology/blob/main/documentation/Dikusa%20Datenmodell%20Folien%2029.04.2022.pdf)

### Progress
So far all main Categories: Persons, Places, Events, Objects, Groups and Works (bibliographic items) have been modelled. The current state forms the basis of further discussions with project partners.

## Validation

Using standard tools - such as those provided with Apache Jena - instance data as found in folder example_data can be validated against the schema as described by shacl constraints (under open world assumption). For validating your own instance data against the schema please be aware that all subclass relations need to be included in your data (see supplied file in example_data) and not (only) in the schema. This is expected by shacl-tools.
For Apache Jena use the following command: shacl v -s schema_file -d instance_data_file 

## Author

kompetenzwerkd@saw-leipzig.de

## Copyright

2022-2024, Sächsische Akademie der Wissenschaften zu Leipzig

## License

AGPLv3
