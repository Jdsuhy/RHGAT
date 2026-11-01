# RHGAT

RHGAT is a hybrid dual-graph Transformer framework with hypergraph
contrastive learning for circRNA--miRNA interaction (CMI) prediction. The
model combines RNA foundation model representations with adaptive
bipartite-graph and hypergraph structure learning to identify potential
circRNA--miRNA associations.


# Requirements

-   Python 3.7 or higher
-   PyTorch (tested with 2.2.2 + CUDA 11.8)
-   multimolecule (for the RNA-FM model)
-   safetensors
-   scikit-learn
-   numpy
-   scipy
-   matplotlib
-   pandas

# Data

Put all required data files in the `./Data/` directory.

The input data preparation pipeline requires:

-   circRNA and miRNA sequence files:
    -   `circRNA.csv` (column 0: circRNA id, column 1: sequence)
    -   `miRNA.csv` (column 0: miRNA id, column 1: sequence)
-   Known circRNA--miRNA interaction file:
    -   `circRNA_miRNA_matrix.csv`
-   circRNA similarity matrices:
    -   `circ_seq_similarity.csv`
    -   `circ_str_similarity.csv`
    -   `circ_exp_similarity.csv`
-   miRNA similarity matrices:
    -   `mi_seq_similarity.csv`
    -   `mi_str_similarity.csv`
    -   `mi_exp_similarity.csv`


# Output

During training, the program prints:

-   Cross-validation fold index
-   AUC
-   AUPR
-   F1-score
-   ACC
-   Precision
-   Recall
-   Specificity
-   MCC
