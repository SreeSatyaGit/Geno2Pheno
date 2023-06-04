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


# Model Architecture

The model architecture used in this project follows a sequential structure, where each layer is connected in a linear manner. Here is a high-level explanation of the model's architecture:

## Convolutional Layers:
The model starts with three Convolutional (Conv1D) layers. These layers learn and extract important patterns from the input gene expression data. Each Conv1D layer applies a set of filters to capture different features and activations within the data. <br>

## MaxPooling Layers: 
After each Conv1D layer, a MaxPooling1D layer is added. Max pooling reduces the spatial dimensions of the data, helping to extract the most relevant information while reducing computational complexity.<br>
## Flatten Layer: 
The output from the last MaxPooling1D layer is then flattened into a one-dimensional vector. This step converts the multidimensional data into a format suitable for feeding into the subsequent fully connected layers.<br>
## Dense Layers: 
The flattened vector is passed through two fully connected Dense layers. These layers contain multiple neurons that learn complex relationships between the extracted features from the earlier layers. The activation function used in these layers is Rectified Linear Unit (ReLU), which introduces non-linearity and allows the model to learn more complex representations.<br>
## Output Layer: 
The final Dense layer has a softmax activation function, which converts the model's output into a probability distribution over the different phenotype classes. In this case, the model aims to classify the input gene expression data into one of the 8 possible phenotype classes.<br>
## Model Compilation: 
The model is compiled with the Adam optimizer, which is an efficient optimization algorithm for training deep learning models. The categorical cross-entropy loss function is used to measure the difference between predicted and actual phenotypes. Additionally, the model's performance is evaluated based on the accuracy metric, which measures the percentage of correctly classified samples.

# Confusion Matrix and Accuracy

By utilizing UMAP labels, we trained a supervised CNN model and achieved an impressive accuracy of 87%. The confusion matrix below provides a detailed breakdown of the model's performance in classifying different phenotypic outcomes.

## Confusion Matrix

The confusion matrix showcases our supervised CNN model's performance in accurately classifying phenotypes with minimal misclassifications. The high accuracy and balanced performance across classes clearly demonstrate the effectiveness of our model in mapping genotypes to phenotypes based on gene expression values.

<img width="496" alt="Screenshot 2023-05-31 at 11 19 46 AM" src="https://github.com/SreeSatyaGit/Geno2Pheno/assets/122564841/15b27c3f-dd86-4e15-a93e-84d183ad5bfa">

## Accuracy
<img width="563" alt="Screenshot 2023-05-31 at 10 54 03 AM" src="https://github.com/SreeSatyaGit/Geno2Pheno/assets/122564841/5d6c66ac-d5bd-4f98-8f43-f32a2479db3d">
