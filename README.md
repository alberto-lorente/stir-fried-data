# Data Science Project 2024 - Stir-fried data

Authors:
Alberto Lorente Galé,
Oyetunji Daniel Abioye,
Ziyan Xu and
Pin-Xun Huang

Supervisor:
Prof. Claire Gardent

MSc Natural Language Processing,
Université de Lorraine

## Project Overview

This project focused on analyzing Nobel laureates in Physics and Chemistry through clustering of biographical texts and knowledge graph data, including a comparison of linguistic processing libraries for named entity recognition (NER).

## Two Main Parts

1.**Text and Knowledge Graph Analysis:** We collect and cluster Wikipedia biographies and corresponding knowledge graph data of Nobel laureates in Physics and Chemistry. This involves data collection, statistics, visualization, linguistic processing, and clustering to segment and analyze the collected data.

2.**NER Comparison:** We compare the behaviour of two linguistic processing libraries (e.g., Stanza and Spacy) on NER on the same set of texts and develop methods to compare the Named Entities found in the texts with RDF entities  present in the corresponding graphs.

## Instructions

```shell
 pip install -r requirements.txt
```

## Usage

After installing dependency packages. Run all cells in `Notebook.ipynb`

**Part 1 - Comparing and Clustering Texts**

1.1 **Data Collection**
```shell
 Data_Collection.ipynb
```

1.2 **Data Analysis**
```shell
 Graph_Data_Analysis.ipynb
```
```shell
 Textual_Data_Analysis.ipynb
```

1.3 **Clustering**
```shell
 Clustering_1. Biography-based_Clusters.ipynb
```
```shell
 Clustering_Knowlwdge_Graph.ipynb
```

**Part 2 - SpaCy and Stanza performance for NER**

2.1 **Named Entity Recognition**
```shell
 NER_Spacy.ipynb
```
```shell
 NER_Stanza.ipynb
```

2.2 **NER - analysis by entity type**
```shell
 NER_Comparison.ipynb
```
```shell
 NER_Process_DFs.ipynb
```

## Results

Detailed results and comprehensive analyses will be presented during our project presentation, scheduled for June 21st, 2024.
