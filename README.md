# GRCh38-Protein-Clustering
A basic k-means model classifying proteins translated from the GRCh38 human genome.

The program reads in the first chromosome's sequence from the GRCh38, and translates functional proteins from it.
It then vectorizes these using two different approaches, of which Word2Vec was found to be exponentially better.
Running k-means clustering algorithm on this gives 100 clusters, with a range of distribution between (1000,1600)(Version 2).

It then tests out the model on some of the remaining functional proteins, for which distribution was found to be within the same range.

What is next is to compare these results with an actual database/model, and to improve it.

The trained model has been uploaded to the main branch itself.

Versions:
  1. Finding a suitable model. First attempt is using tfidfvectorizer which yieled a model with no usage (12000 proteins in a single cluster, from 12500 approx). Second model using Word2Vec yielded much more favourable results.
  2. Training the k-means model using Word2Vec on 10% of chromosome 1, and predicting clusters for another 10%. The proteins in each cluster were in the range (1000,1600).
 
 You can find the previous versions in the folder 'versions.'

Find the dataset here: [GRCh38 Human Genome (DNA)](https://www.kaggle.com/datasets/aliabedimadiseh/grch38-human-genome-dna)

Find my notebook on [Kaggle](https://www.kaggle.com/) which you can copy and edit directly here: [My Notebook](https://www.kaggle.com/code/shashwatsaini04/grch38-protein-clustering)

Note: Github does not seem to support Plotly graph previews, hence some graphs are not being displayed.
