# Triplify ASVe

This repository contains materials related to the semantic representation of the archival contents of the Venice State Archive (ASVe). These materials were produced by Michele Jacopo Alessandro Stefani, during his internship at EPFL's DHLAB, carried out between November 2016 and August 2017, under the supervision of Matteo Romanello (DHLAB), Maud Ehrmann (DHLAB), Dorit Raines (Ca' Foscari) and Manuela Simeoni (Ca' Foscari University Library).

The goal of this project was to produce a semantic description of ASVe's archival funds and series, which could be used in Linked Book's citation graph to express citations between secondary literature and archival primary sources.

## Survey of ontologies for archival sources

The first step in the project was to carry out a survey of existing ontologies to model and represent archival contents. All survey materials can be found in the folder [`./survey-ontologies/`](survey-ontologies/). As a result of this survey, Records in Context (RiC) emerged as the go-to ontology for semantic description of archival contents. At the time of the internship, RiC was still under development, and no RDF/OWL implementations of the ontology existed. Thus, Michele Stefani created an OWL version of the RiC ontology draft, which can be found at [`openrefine-conversion/RiC-CM_DraftOntology20170510.owl`](openrefine-conversion/RiC-CM_DraftOntology20170510.owl). This is now superseeded by the official ontology implementation, published at <https://www.ica.org/standards/RiC/ontology.html>.

## Data

The Venice State Archive publishes detailed metadata about its contents via its online information system [SiASVe](http://www.archiviodistatovenezia.it/siasve/cgi-bin/pagina.pl). Since these metadata are offered only as HTML pages, we scraped SiASVe's web pages in order to extract the underling data in a machine-readable format. In particular, we made use of the tree view offered by SiASVe to derive information about the hierarchical structure of the archive contents. The scraped data is at [`openrefine-conversion/input/ASVe_content_from_API.csv`](openrefine-conversion/input/ASVe_content_from_API.csv), while a list of SiASVE inconsistencies that were dected in this process is at [`openrefine-conversion/input/asve_hierarchy_inconsistencies.csv`](openrefine-conversion/input/asve_hierarchy_inconsistencies.csv) 


## Data conversion with OpenRefine
