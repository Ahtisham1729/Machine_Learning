# K-Means Clustering on NEU Steel Surface Defect Dataset

This project applies unsupervised machine learning techniques—specifically **K-Means clustering**—to classify images of steel surface defects from the NEU dataset. It explores the effect of **dimensionality reduction using PCA** on clustering performance and visualizes clustering results in both 2D and 3D spaces.

## Table of Contents
- [Dataset](#dataset)
- [Project Overview](#project-overview)
- [How to Run](#how-to-run)
- [Results](#results)
- [Dependencies](#dependencies)

## Dataset
The [NEU Surface Defect Database](https://github.com/shreyaspadhye/NEU-Defect-Detection) consists of grayscale steel surface images classified into six defect categories:
- Crazing
- Inclusion
- Patches
- Pitted Surface
- Rolled-in Scale
- Scratches

For this project:
- 50 training images per class
- 20 testing images per class
were randomly sampled to form a balanced dataset.

## Project Overview

The following tasks were performed:
1. **Image Preprocessing**  
   Images were:
   - Converted to grayscale
   - Resized to 64×64 pixels
   - Normalized to [0, 1]
   - Flattened into 4096-dimensional vectors

2. **K-Means Clustering (Raw Data)**  
   KMeans was applied directly to the 4096-dimensional vectors. Accuracy was evaluated by mapping each cluster to a class label using majority voting.

3. **PCA + KMeans**  
   PCA was used to reduce dimensionality. KMeans was applied on projections with varying component counts (5–64), and classification accuracy was tracked.

4. **Visualization**  
   - Confusion matrices were generated
   - PCA error-vs-dimension plot was created
   - 3D scatter plot using first three principal components

## How to Run
Prepare Dataset
Download the NEU-DET dataset and modify train_src and val_src paths in the notebook.

Run the Notebook
Open NEU_KMeans_PCA_Notebook.ipynb in Jupyter or VSCode and execute cells sequentially.

Interpret Results
Confusion matrices and accuracy scores are printed. PCA plots and 3D visualizations are generated.

## Results

Task	               Accuracy (Train)	 Accuracy (Test)
Raw Data + KMeans	   38.3%	         25.8%
PCA (l=40) + KMeans	   41.7%	         36.7%

The best trade-off between dimensionality and generalization was achieved at 40 principal components.

## Dependencies

Python 3.8+
numpy
opencv-python
pandas
matplotlib
scikit-learn

You can install them with:

pip install numpy opencv-python pandas matplotlib scikit-learn



