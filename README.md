# Unstructured learning for cycling Grand Tours

Using dimensionality reduction and clustering techniques on data from cycling grand tours to group similar riders. Each tour consists of 21 individual stage races over varying terrain. There are incentives for riders to finish with the lowest overall time, to win individual stages, and to consistently finish near the front for mountain stages / sprint stages.

For each tour the riders that completed all of the stages are represented by their time gaps to the winner in each stage. This 21-dimensional data is then embedded into 2 dimensions using t-distributed stochastic neighbour embedding. The perplexity parameter is shown to greatly influence the embedding that is produced. A low level of perplexity was chosen as higher levels tended to embed data into a tight ball.

sklearn.mixture.BayesianGaussianMixture model is used to cluster the riders within the embedding. Rider groups across multiple tours are analysed to identify riders that appear in the same group more than once

