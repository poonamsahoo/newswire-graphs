# newswire-graphs
A graph analysis of the Dell Research Newswire Dataset, specifically focused on characterizing newspaper similarities and behaviors. 

# Intro
Our code is split up into four folders:
- **DATA** contains notebooks for aggregating data from the original newswire dataset, webscraping ground truths from Dave Leip's Atlas of US Presidential Elections, and pushing our resulting datasets to huggingface.
- **HOMOGNN** contains the code for creating our homogeneous newswire graph and our code for training GNNs on said graph
- **HETEROGNN** contains the code for creating our heterogeneous newswire graph and our code for training heterogeneous GNNs on said graph
- **EVAL** contains notebooks for evaluating model performance such as our Political Ideology detection experiment, our evaluation plots, and TSNE visualization and HDBSCAN clustering of the resulting node embeddings

## Data
This folder consists of the following jupyter notebooks
1. **`[FIN] outlet_metadata_construction.ipynb`**  
   Constructs and compiles metadata for newspaper outlets. This includes processing details like city, state, and location of newspaper outlets for further analysis.

2. **`[FIN] webscraping political ground truths.ipynb`**  
   Implements a web scraping pipeline to gather political ground truth data from Dave Leip's Atlas of US Presidential Elections. We specifically aggregate county-level US presidential election data.

3. **`[FIN]_to_hf.ipynb`**  
   Prepares datasets for integration with Hugging Face for easier access down the road.
