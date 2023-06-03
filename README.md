# GRCh38-Protein-Clustering
A basic k-means model classifying proteins translated from the GRCh38 human genome.

The program reads in the first chromosome's sequence from the GRCh38, and translates functional proteins from it.
It then vectorizes these using two different approaches, of which Word2Vec was found to be exponentially better.
Running k-means clustering algorithm on this gives 100 clusters, with a range of distribution between (100,160).

It then tests out the model on some of the remaining functional proteins, for which distribution was found to be within the same range.

What is next is to compare these results with an actual database/model, and to improve it.
