# Reading Experience Ontology (REO)
"READ-IT (Reading Europe Advanced Data Investigation Tool) is a 3-years (2018-2020) transnational, interdisciplinary R&D project funded by the Joint Programming Initiative for Cultural Heritage that will build a unique large-scale, user-friendly, open access, semantically-enriched investigation tool to identify and share groundbreaking evidence about 18th-21st century Cultural Heritage of reading in Europe", source [READ-IT Project Website](https://readit-project.eu/). 

The Reading Experience Ontology is one of the outcome of READ-IT project. More about the methodology and requirements of REO can be found in this [paper](http://www.semantic-web-journal.net/content/understanding-phenomenology-reading-through-modelling-0) (under review).

This repository includes two versions of REO:

- V1.x, this version is a minimal, stand-alone ontology representing the consensus reached by the project on a set of key concepts and relations necessary for the study of reading experiences.
- V2.x, this version extends V1.x including concepts not currently used and/or under evaluation. 

The latest version of REO is the V1.8. With this version we rolled back from the initial hypothesis of alignments with CIDOC-CRM to a stand-alone version.

## READ-IT
The JPI READ-IT (Reading Europe Advanced Data Investigation Tools) is an interdisciplinary project aiming to advance the study of reading in both understanding of the phenomenon and methods. READ-IT brings together researchers from different disciplines and case studies on different countries, languages, periods and social groups with the goals of:  

- Designing, developing and validating a common digital toolbox, able to support the interoperability of research data 

- Addressing broad research questions requiring both a large-scale data collection and a broad view on the European continent geographical and temporal landscape.

Behind these goals, there are two major hidden methodological assumptions: 

1. a large-scale data collection cannot be done within a consistent research framework, in terms of either a large-scale use case and disciplinary methodologies and theories 

2. reading is a multi-facets phenomenon and therefore its understanding requires a bridging the different components and perspectives, object and focus of the different disciplines involved.  

In this view, REO provides the common conceptual infrastructure beyind the READ-IT toolbox. 

## Approach to modelling
REO value is firstly related to providing a common view of what is the reading phenomenon. 

In this regard, REO had been developed combing the study of sources of reading experiences, such as transcriptions of interviews and diaries, with the engagement of READ-IT researchers. 

The development followed an Agil-like approach in multiple phases and interations, from September 2018 to January 2020. More about it can be found it this [paper](http://www.semantic-web-journal.net/content/understanding-phenomenology-reading-through-modelling-0) (under review).

## Outline of REO
REO covers three macro conceptual area:

1. The reader agent
2. The reading resource
3. The reading process

These broad area includes a range of concepts and relations with some varietions between the different versions. We describe here the main concepts of REO.

### The reader agent
A key feature of REO is the distinction between PERSON and READER. In REO, the PERSON is the agent (reading) while with READER is the state of the PERSON at the time of reading. 

In this view, PERSON is the partition of all permanent features of a reading agent, such as date of birth, while READER is the partition of the dynamic features, e.g. known languages. Thus, for each PERSON is possible to have multiple states of READER.

A key concept and pilar of REO is STATE_OF_MIND, part of the READER. STATE_OF_MIND represents a partial mind state of the reading agent, such as emotions, memories, aims. STATE_OF_MIND are of three main types:

1. BELIEF, what the reader knows or thinks
2. MEMORY, what the reader remembers
3. FEELING, what the reader feels 

Furthermore, STATE_OF_MIND can have four main roles (in relation to the reading process):

1. DISPOSITION toward reading in general (e.g. of a genre, author, etc)
2. PREMISE of a specific reading process (preceeding the reading or causing the reading)
3. EFFECT of a specific reading process (co-occurring during the reading)
4. OUTCOME of a specific reading process (following and effect of a reading)

### The reading resource
In the description of reading resources, REO provides an upper-structure based on the FRBR conceptualisation of Work, Expression, Manifestation and Item [IFLA FRBR](https://www.ifla.org/publications/functional-requirements-for-bibliographic-records). 

REO is meant to address the vagueness of testimonies of reading experience. Indeed, some testimonies provides detailled description of what the reported experience is about, e.g. a specific expression, concept, character, plot twist, while other testimonies do not provide any specific detail. 

In this view, REO provide the following hierarchy:

- READING_RESOURCE
  - CONTENT (upperclass of FRBR's Work and Expression)
  - MEDIUM (upperclass of FRBR's Manifestation and Item)

Similarly with the reading agent, REO introduce the concept of STATE_OF_MEDIUM (the partition of the dynamic features of a medium). ALTERATION is a specialisation of the STATE_OF_MEDIUM used to represent the modifications of the medium, such as notes, marginalia or damage. 

### The reading process

