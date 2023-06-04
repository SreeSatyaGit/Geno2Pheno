# Geno2Pheno - Introduction

This project aims to develop a Convolutional Neural Network (CNN) model that maps genotype to phenotype using gene expression values. By leveraging the power of deep learning and gene expression data, we seek to uncover the underlying relationship between genetic variations and observed phenotypic outcomes.

# Dataset
The Dataset used to train this model is from 10xGenomics which consists of Peripheral blood mononuclear cells (PBMCs) from a healthy donor. <br>https://support.10xgenomics.com/single-cell-gene-expression/datasets/1.1.0/pbmc3k?<br>

Estimated Number of Cells -> **2,700** <br>
Mean Reads per Cell -> **68,881** <br>
Median Genes per Cell -> **817** <br>

# Umap Visualization

UMAP (Uniform Manifold Approximation and Projection) is a powerful dimensionality reduction technique used for visualizing and exploring high-dimensional data. It preserves data structure, handles large datasets, and offers improved performance. UMAP finds applications in data visualization, exploratory data analysis, machine learning, clustering, and anomaly detection. It helps analyze complex datasets, identify patterns, improve machine learning efficiency, and detect outliers. Overall, UMAP is a versatile tool for understanding and extracting insights from high-dimensional data.

## Umap Visualization of the dataset

![2700_cells_umap](https://github.com/SreeSatyaGit/Geno2Pheno/assets/122564841/8b649df1-36e4-43e2-adfc-8c74d86d4554)

# Confusion Matrix and Accuracy

By utilizing UMAP labels, we trained a supervised CNN model and achieved an impressive accuracy of 87%. The confusion matrix below provides a detailed breakdown of the model's performance in classifying different phenotypic outcomes.

## Confusion Matrix
<img width="496" alt="Screenshot 2023-05-31 at 11 19 46 AM" src="https://github.com/SreeSatyaGit/Geno2Pheno/assets/122564841/15b27c3f-dd86-4e15-a93e-84d183ad5bfa">

## Accuracy
<img width="563" alt="Screenshot 2023-05-31 at 10 54 03 AM" src="https://github.com/SreeSatyaGit/Geno2Pheno/assets/122564841/5d6c66ac-d5bd-4f98-8f43-f32a2479db3d">
