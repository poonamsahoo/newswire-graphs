# newswire-graphs
A graph analysis of the [Dell Research Newswire Dataset](https://huggingface.co/datasets/dell-research-harvard/newswire), specifically focused on characterizing newspaper similarities and behaviors. 

# INTRO
Our code is split up into four folders:
- **DATA** contains notebooks for aggregating data from the original newswire dataset, webscraping ground truths from Dave Leip's Atlas of US Presidential Elections, and pushing our resulting datasets to huggingface.
- **HOMOGNN** contains the code for creating our homogeneous newswire graph and our code for training GNNs on said graph
- **HETEROGNN** contains the code for creating our heterogeneous newswire graph and our code for training heterogeneous GNNs on said graph
- **EVAL** contains notebooks for evaluating model performance such as our Political Ideology detection experiment, our evaluation plots, and TSNE visualization and HDBSCAN clustering of the resulting node embeddings

## DATA
This folder consists of the following jupyter notebooks
1. [**`[FIN] outlet_metadata_construction.ipynb`**](DATA/%5BFIN%5D%20outlet_metadata_construction.ipynb)  
   Constructs and compiles metadata for newspaper outlets. This includes processing details like city, state, and location of newspaper outlets for further analysis.

2. **`[FIN] webscraping political ground truths.ipynb`**  
   Implements a web scraping pipeline to gather political ground truth data from Dave Leip's Atlas of US Presidential Elections. We specifically aggregate county-level US presidential election data.

3. **`[FIN]_to_hf.ipynb`**  
   Prepares datasets for integration with Hugging Face for easier access down the road.

## HOMOGNN
1. **`[FIN] create_homo_graph.ipynb`**  
   Constructs the homogeneous graph we use to train our GNNs. Nodes consist of newspapers and articles, with edges connecting when a newspaper runs a particular article. 

2. **`[FIN] train_homo_gnn.ipynb`**  
   Code for training our GNNs. Includes hyperparameter tuning and multiple architectures

## HETEROGNN
1. **`[FIN] create_heterograph.ipynb`**  
   Constructs the bipartite heterogeneous graph we use to train our heterogeneous GNNs. Nodes consist of newspapers and articles, with edges connecting when a newspaper runs a particular article. 

2. **`[FIN] hetero_train.ipynb`**  
   Code for training our heterogeneous GNNs. Includes hyperparameter tuning and multiple architectures

## EVAL

1. **`[FIN] eval_baseline.ipynb`**  
   Evaluates baseline models for Political Ideology Detection experiment. This notebook includes performance metrics such as accuracy, F1 score, AUC, etc. 
   
2. **`[FIN] eval_hetero.ipynb`**  
   Evaluates the performance of models trained on heterogeneous graphs for Political Ideology Detection experiment. This notebook includes performance metrics such as accuracy, F1 score, AUC, etc.

3. **`[FIN] eval_homo.ipynb`**  
   Evaluates the performance of models trained on homogeneous graphs for Political Ideology Detection experiment. This notebook includes performance metrics such as accuracy, F1 score, AUC, etc.

4. **`[FIN] Create ROC-AUC Graphs.ipynb`**  
   Generates ROC-AUC graphs to evaluate model performance. This notebook helps visualize and compare classifier effectiveness.

5. **`[FIN] TSNE and HDBSCAN Clustering.ipynb`**  
   Analysis and visualization of newspaper node embeddings. Performs dimensionality reduction using t-SNE and other dimensionality-reduction methods and clusters data using HDBSCAN.
