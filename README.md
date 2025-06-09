# PDB-structures-selection
## Computational Methods for PDB Structure Selection

The structural clustering and selection of protein models were performed using a custom Python pipeline. Atomic coordinates (x, y, z) were extracted from PDB files using Biopython, excluding heteroatoms, and standardized to a fixed maximum length (9,000 atoms) to ensure uniform feature vectors (27,000 dimensions). Feature normalization was applied via scikit-learn’s StandardScaler, followed by dimensionality reduction using UMAP (n_neighbors=15, min_dist=0.1, Euclidean metric) to generate 2D embeddings. Cluster analysis combined:

K-means clustering (optimal *k*=4 determined by silhouette scores) and Hierarchical clustering (Ward linkage, distance threshold=8) to group structurally similar conformations.

This approach enabled the identification of representative DHODH-inhibitor complexes for further validation, aligning with the study’s focus on host-directed therapy against SARS-CoV-2
