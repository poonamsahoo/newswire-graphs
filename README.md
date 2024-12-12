# newswire-graphs
A graph analysis of the Dell Research Newswire Dataset, specifically focused on characterizing newspaper similarities and behaviors. 

Our code is split up into four folders:
- **DATA** contains notebooks for aggregating data from the original newswire dataset, webscraping ground truths from Dave Leip's Atlas of US Presidential Elections, and pushing our resulting datasets to huggingface.
- **HOMOGNN** contains the code for creating our homogeneous newswire graph and our code for training GNNs on said graph
- **HETEROGNN** contains the code for creating our heterogeneous newswire graph and our code for training heterogeneous GNNs on said graph
- **EVAL** contains notebooks for evaluating model performance such as our Political Ideology detection experiment, our evaluation plots, and TSNE visualization and HDBSCAN clustering of the resulting node embeddings
