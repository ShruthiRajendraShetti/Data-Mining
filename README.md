# Advanced Dimensionality Reduction

# Assignment 1.1
## Colab Link - https://colab.research.google.com/drive/1LgRzPAplVq09NJC3YYvZmI0aUX-nsogY?usp=sharing

## Overview
This project demonstrates various dimensionality reduction techniques on both synthetic and real datasets (image and tabular). The objective is to explore the strengths and weaknesses of different methods and provide meaningful insights through visualizations.

## Datasets
1. **Image Data**: 
   - Generated synthetic breast histopathology-like images (Benign vs Malignant).
2. **Tabular Data**:
   - Generated synthetic Heart Disease dataset with 10 features and binary labels.

## Techniques Implemented
1. **Principal Component Analysis (PCA)**
2. **t-SNE (t-Distributed Stochastic Neighbor Embedding)**
3. **UMAP (Uniform Manifold Approximation and Projection)**
4. **ISOMAP**
5. **Other Techniques** (if implemented, e.g., MDS, Autoencoders)

## Results and Observations
| **Technique** | **Dataset**       | **Strengths**                     | **Weaknesses**                     |
|---------------|-------------------|-----------------------------------|-------------------------------------|
| PCA           | Image, Tabular    | Fast, interpretable               | Limited to linear relationships     |
| t-SNE         | Image, Tabular    | Excellent clustering              | Computationally expensive           |
| UMAP          | Image, Tabular    | Fast, preserves global structure  | Sensitive to hyperparameters        |
| ISOMAP        | Image, Tabular    | Captures non-linear relationships | Sensitive to neighborhood size      |

- **PCA**: Works best for capturing global variance in linear data.
- **t-SNE**: Superior for small datasets with clear cluster formations.
- **UMAP**: Balances computational efficiency and clustering quality.
- **ISOMAP**: Useful for capturing complex non-linear structures.


# Assignment 1.2 Dimensionality Reduction using Data Bricks

## Colab Link - https://colab.research.google.com/drive/1rAGe1aMJjIPVRysTQJDPC02q7Pl9Y5a2?usp=sharing

## Overview
This project explores popular dimensionality reduction techniques, including PCA, t-SNE, UMAP, and ISOMAP, applied to synthetic and real-world datasets (e.g., image and tabular data). The goal is to analyze their performance and suitability for various data types.

## Datasets
1. **Image Data**:
   - Synthetic histopathology-like images (Benign vs Malignant).
2. **Tabular Data**:
   - Synthetic Heart Disease dataset with 10 features.

## Techniques and Observations
1. **PCA**:
   - Captures maximum variance in fewer components.
   - Suitable for linear data structures.
2. **t-SNE**:
   - Excellent for visualizing clusters in non-linear datasets.
   - Computationally expensive.
3. **UMAP**:
   - Balances speed and accuracy.
   - Preserves local and global structures effectively.
4. **ISOMAP**:
   - Captures non-linear structures through geodesic distance preservation.

## Key Results
- PCA provided an overview of global variance but struggled with non-linear clusters.
- t-SNE and UMAP excelled in forming distinct clusters for image datasets.
- ISOMAP was effective in revealing underlying geometry but required careful tuning.

