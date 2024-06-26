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

2.**NER Comparison:** We compare the behaviour of two linguistic processing libraries (Stanza and Spacy) on NER on the same set of texts and develop methods to compare the Named Entities found in the texts with RDF entities present in the corresponding graphs.

## Instructions

Requires python release > 3.10.

```shell
 pip install -r requirements.txt
```

## Organization

The folders are organized as per the project description and the notebooks related to each section are found within each folder.
The corpus collected can be found in the Data Directory folder.

**Part 1 - Comparing and Clustering Texts**

1.1 **Data Collection**

* Retrieve the first 100 biographies and corresponding knowledge graph for Nobel laureates from Wikipedia.
* Store biographies in individual text files and knowledge graph in JSON files.
* Use the `fetch_biography` function to automate biography retrieval and fallback to page_id lookup if necessary.
* Lemmatize texts, remove stopwords and non-alphabetic characters with `clean_text_spacy`, preparing data for analysis.
  
1.2 **Data Analysis**

Text:

* Process text from each biography to remove stopwords and punctuation, then concatenate into a single string per category.
* Analyze and visualize the 50 most frequent words with word clouds.
* Calculate and plot the minimum, maximum, and average number of sentences and bigrams per sentence for each category.


Graphs:

* Aggregate all knowledge graph data into a DataFrame, setting values to represent RDF triples.
* Conduct SPARQL queries to isolate RDF subjects and objects, excluding laureate names to prevent data bias.
* Identify the top 50 RDF properties and display them in property clouds for each category.

1.3 **Clustering**

Text:

* Clustering is performed on the textual data of each laureate’s biography.
* Apply KMeans clustering to form two clusters based on the analysis of the biographical text.
* Evaluate the clusters by comparing them against ground truth and calculating supervised metrics.

Graphs:

* Fetch and retrieve the knowledge graph for each laureate from JSON files using the laureate's name.
* Extract the literal values from the URLs in the knowledge graph, focusing on the last part of each URL which corresponds to the literal value of the object.
* Compaire the resulting clusters to the ground truth.
  
**Part 2 - SpaCy and Stanza performance for NER**

2.1 **Named Entity Recognition**

* Use both SpaCy and Stanza to detect and extract named entities from each biography.
* For each entity, save the text, number of words, and start and end positions in a DataFrame. 
* Extract entity data into DataFrames.
* Compute average, minimum, and maximum numbers of named entities and words per entity.
* Create visualizations that highlight differences and similarities in entity recognition performance.
  
2.2 **NER - analysis by entity type**

Check biographies for the following:

* Count spans with full overlap where both packages predict the same named entity.
* Count spans with partial overlap in predictions.
* Identify spans predicted as an entity by one tool but not by the other.
* Check agreement on the entity type (e.g., Person, Location, Organization) for spans with any level of overlap.
* Use visualization to compare the frequency and agreement of NER between Stanza and Spacy, segmented by entity type and document category.

2.3 **NER - verification against knowledge graph**

* Determine how many predicted NEs can be found in the KG for each person, using regular expressions to account for potential mismatches between the NE spans in text and KG entity labels.
* Calculate the ratio of accurately matched NEs to total NEs predicted by each package for each person, providing a measure of verification confidence.

## Result

These results and comprehensive analyses will be presented during our presentation, scheduled for June 21st, 2024.
