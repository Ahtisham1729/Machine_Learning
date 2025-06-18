# K-Means Clustering on NEU Steel Surface Defect Dataset

This project applies unsupervised machine learning techniques—specifically **K-Means clustering**—to classify images of steel surface defects from the NEU dataset. It explores the effect of **dimensionality reduction using PCA** on clustering performance and visualizes clustering results in both 2D and 3D spaces.

## Table of Contents
- [Dataset](#dataset)
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Directory Structure](#directory-structure)
- [How to Run](#how-to-run)
- [Results](#results)
- [Dependencies](#dependencies)
- [Acknowledgments](#acknowledgments)

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

