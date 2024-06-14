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
* Total number of bi-gram occurrences per category. Min/max/avg number of bi-gram occurrences per sentence per category.

Graphs

* 50 most frequent properties and property cloud for each category.
* Min/max/avg number of facts per category together. Histograms and box plots for number of facts per graph for each category.

1.3 **Clustering**

Train clustering modelS with using KMeans to predict two distinct clusters, including:

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

Check biographies for the following:

* Count spans with full overlap where both packages predict the same named entity.
* Count spans with partial overlap in predictions.
* Identify spans predicted as an entity by one tool but not by the other.
* Check agreement on the entity type (e.g., Person, Location, Organization) for spans with any level of overlap.
* Use visualization to compare the frequency and agreement of NER between Stanza and Spacy, segmented by entity type and document category.

2.3 **NER - nverification against knowledge graph**

* Determine how many predicted NEs can be found in the KG for each person, using regular expressions to account for potential mismatches between the NE spans in text and KG entity labels.
* Calculate the ratio of accurately matched NEs to total NEs predicted by each package for each person, providing a measure of verification confidence.
 
## Results


