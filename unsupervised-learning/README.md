# Unsupervised Learning: Clustering & PCA

Part of my [ML-learning-journey](../README.md). This notebook explores unsupervised learning on the Seeds dataset, using K-Means clustering to group data without labels and PCA to reduce dimensions and visualise the result.

## Dataset
[Seeds Dataset](https://archive.ics.uci.edu/dataset/236/seeds) (UCI Machine Learning Repository). It has 210 wheat kernels from three varieties, each described by 7 geometric measurements:

area, perimeter, compactness, length, width, asymmetry, groove

The true variety (class) is used only to check how well the clusters match, not to train the model.

## What's covered
1. Exploration: scatter plots of every feature pair, coloured by true class
2. K-Means in 2D: clustering on compactness vs. asymmetry with k=3, compared against the original classes
3. K-Means in higher dimensions: clustering on all 7 features, then plotting the same two axes to compare with the true classes
4. PCA: reducing the 7 features (210 × 7) down to 2 principal components
5. Clusters vs. truth in PCA space: K-Means labels and true classes plotted side by side on the 2 components

## Key takeaways
- K-Means on two hand-picked features gives clusters that don't match the real classes well.
- Using all 7 features gives much better clusters.
- PCA squeezes the 7 features into 2 axes so the clusters can be seen in a single plot, and the K-Means groups line up closely with the true varieties.

## Files
- unsup-learning.ipynb: notebook with code and plots
- seeds_dataset.txt: the dataset

## Tech stack
Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn

## Run it yourself
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook
```