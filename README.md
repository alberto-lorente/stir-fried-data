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

2.**NER Comparison:** We compare the behaviour of two linguistic processing libraries (e.g., Stanza and Spacy) on NER on the same set of texts and develop methods to compare the Named Entities found in the texts with RDF entities present in the corresponding graphs.

## Instructions

```shell
 pip install -r requirements.txt
```

## Usage

After installing dependency packages. Run all cells in `Notebook.ipynb`

**Part 1 - Comparing and Clustering Texts**

1.1 **Data Collection**

Extract the Wikipedia biographies and associate knowledge graph for two distinct categories:Nobel laureates in Physics & Nobel laureates in Chemistry.

Organize data outputs into a pandas DataFrame to link texts with their respective categories and store each biography in individual text files. Furthermore, keep detailed knowledge graph in JSON files which can map back to each person easily.

1.2 **Data Analysis**

Analysis the differences between the two catagoreis, including:

Text

* 50 most frequent words and word cloud for each category (Text).
* Min/max/avg number of sentences per category together with the corresponding histograms and box plots.
* Total number of bi-gram occurrences per category. Min/max/avg
number of bi-gram occurrences per sentence per category.

Graphs

* 50 most frequent properties and property cloud for each category.
* Min/max/avg number of facts per category together. Histograms and box plots for number of facts per graph for each category.

1.3 **Clustering**

Train a clustering model with using KMeans to predict two distinct clusters, including:

* Text: Each person's collected biography text.
* Knowledge Graph: Each person's collected facts, linearise as a single string for processing.

For both data inputs, conduct a comparative analysis by calculating various supervised and unsupervised metrics, along with visualisations to illustrate the differences between the clusters formed from textual and knowledge graph. 

**Part 2 - SpaCy and Stanza performance for NER**

2.1 **Named Entity Recognition**

* Extract Named Entities: Use Stanza and Spacy to process each biography and retrieve named entities.
* Store Results: Organize the extracted data into Pandas dataframes or JSON files for easy access and comparison.
* Statistics: Calculate avg, min, and max numbers of named entities and words per entity for each category and library.
* Visual Comparisons: Create visualizations to compare these statistics across categories and libraries, highlighting performance differences.

2.2 **NER - analysis by entity type**


2.3 **NER - Nverification against knowledge graph**


## Results

Detailed results and comprehensive analyses will be presented during our project presentation, scheduled for June 21st, 2024.
