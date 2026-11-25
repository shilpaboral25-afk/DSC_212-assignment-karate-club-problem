# Modularity on the Karate Club Graph (DSC212)

This repository has my DSC 212 assignment for the Graph Theory module that I did using spectral modularity to find communities in Zachary's Karate Club network.

## What the notebook does
1. Loads the Karate Club graph with NetworkX and builds the modularity matrix `B = A - k k^T / 2m`.
2. Splits the graph in two using the leading eigenvector of `B` and compares it with the real split of the club.
3. Keeps splitting each group (recursive bisection) until the largest eigenvalue is not positive.
4. Draws the graph after every split with a fixed layout, one color per community, nodes labeled by ID.
5. After every split, computes degree, betweenness, closeness and clustering for every node.
6. Plots how these metrics change over the iterations.
7. Ends with a short discussion

## Results
- First split: 2 groups, Q = 0.3715, only node 8 differs from the real split.
- Final: 5 communities, Q = about 0.41.

## Reference
Newman, M. E. J. (2006). Modularity and community structure in networks. *PNAS*, 103(23), 8577-8582.
