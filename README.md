# Kaggle-Multi-modal-CITE-seq-Prediction-ML-project using Gaussian solver and NMF coded from scratch.

In this project CITE-seq is a single-cell sequencing assay in which both gene and cell-surface protein expression is measured in single-cells. This "multi-modal" analysis allows for biological knowledge discovery about the relationships between protein markers of cell type and the underlying transcriptional (gene expression) state.

There is no biology that is needed to understand, other than that there are strong relationships between expression of particular proteins and corresponding gene expression.

Protein expression is measured using Antibody-Derived Tags (ADT), while single-cell RNA-sequencing is used to quantify the abundance of RNA transcripts in each cell.

The goal of this competition is to predict the protein expression profile of 25 proteins in 1000 test cells given the gene expression of 639 genes in those cells. In order to predict this information, you are given 4000 cells from the same experiment with information on all 25 proteins and 639 genes. Use the training data (possibly including the test RNA data) to most accurately predict the protein expression.

I use multivariate regression that involves learning a model on the training set that predicts each ADT feature in terms of all RNA features, then plugging in for the ADT features given the learned coefficients on the test set.

For the second method i use NMF by Learning a model on the entire training + test dataset, masking missing values in the ADT/test sample/feature block. Then multiply out the model.
