# Advanced Dimensionality Reduction

# Assignment 1.1
## Colab Link - ### https://colab.research.google.com/drive/1LgRzPAplVq09NJC3YYvZmI0aUX-nsogY?usp=sharing

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


Assignment 1.2 
Colab Link - https://colab.research.google.com/drive/1rAGe1aMJjIPVRysTQJDPC02q7Pl9Y5a2?usp=sharing

