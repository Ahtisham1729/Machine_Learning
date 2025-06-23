# MLP Regression on Cantilever Beam Data

This project applies a Multi-Layer Perceptron (MLP) to predict displacements $(u_x, u_y)$ from spatial coordinates $(x, y)$ on a 2D cantilever beam using FEM data.

## Contents

- `data/` — Contains the input file `collocation_linear.csv` with sampled FEM displacements data.
- `results/` — Stores output plots, MSE tables, and the break-even analysis figure.
- `MLP_regression.ipynb` — Jupyter notebook containing data preprocessing, model training, hyperparameter tuning, interpolation comparisons, and result generation.

## Dependencies

This project requires the following Python libraries:

- numpy
- pandas
- scikit-learn
- scipy
- matplotlib