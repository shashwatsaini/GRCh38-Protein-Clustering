# GRCh38-Protein-Clustering
A basic k-means model classifying proteins translated from the GRCh38 human genome.

The program reads in the first chromosome's sequence from the GRCh38, and translates functional proteins from it. Refer to 'Versions' below to look into the working.

It then tests out the model on some of the remaining functional proteins.

What is next is to compare these results with an actual database/model, and to improve it.

The trained model has been uploaded to the main branch itself.

Versions:
  1. Finding a suitable model. First attempt is using tfidfvectorizer which yieled a model with no usage (12000 proteins in a single cluster, from 12500 approx). Second model using Word2Vec yielded much more favourable results.
  2. Training the k-means model using Word2Vec on 10% of chromosome 1, and predicting clusters for another 10%. The proteins in each cluster were in the range (1000,1600).
  3. The best approach so far, finding the amino acid composition for each percentage of the protein sequence (25%, 50%, etc.) which provided a very rudimentary inclusion of the structure of amino acids. The stark advantage of using this approach is visible in the graphs, where clusters have clearly been seperated, especially in the 3-dimensional PCA graph, thus rendering all previous versions futile.
 
 You can find the previous versions in the folder 'versions.'

Find the dataset here: [GRCh38 Human Genome (DNA)](https://www.kaggle.com/datasets/aliabedimadiseh/grch38-human-genome-dna)

Find my notebook on [Kaggle](https://www.kaggle.com/) which you can copy and edit directly here: [My Notebook](https://www.kaggle.com/code/shashwatsaini04/grch38-protein-clustering)

Note: Github does not seem to support Plotly graph previews, hence some graphs are not being displayed.
