# Principal-Component-Analysis-PCA-on-the-Wine-Dataset
This project is part of the University of Colorado Boulder Master of Science (MSc) in Artificial Intelligence program and demonstrates dimensionality reduction techniques using Principal Component Analysis (PCA) on the Wine dataset.

Overview:
The project follows a structured unsupervised learning workflow, including data exploration, preprocessing, dimensionality reduction, and evaluation. The Wine dataset, containing 178 samples with 13 chemical features, is first analyzed to highlight differences in feature scales. Summary statistics show that certain features (e.g., proline) have significantly larger ranges than others, which would dominate variance-based methods like PCA if left unscaled. To address this, z-score standardization is applied, ensuring all features contribute equally.

A PCA model is then fitted to the standardized data to extract principal components and analyze the proportion of variance explained. The first principal component (PC1) explains approximately 36% of the total variance, while the second (PC2) explains about 19%, meaning the first two components together capture roughly 55% of the dataset’s structure. This indicates that a substantial portion of the high-dimensional information can be represented in just two dimensions.

Using cumulative variance analysis, the minimum number of components required to retain at least 80% of the total variance is 5, demonstrating effective dimensionality reduction from 13 → 5 features with limited information loss.

Loadings are examined to interpret the principal components. Results show that PC1 is primarily driven by phenolic compounds (e.g., flavanoids and total phenols), indicating that these chemical properties are the most influential sources of variation across wine samples. This provides meaningful domain insight into which features differentiate the data most strongly.

The dataset is transformed into principal component space for visualization. A scatter plot of PC1 vs PC2 reveals clear structure in the data, with samples spreading along dominant variance directions and certain observations appearing far from the origin, indicating potential outliers. As expected, the correlation between PC1 and PC2 is approximately zero, confirming that the components are orthogonal.

Finally, PCA is used for data reconstruction to evaluate information loss. Using all components results in near-zero reconstruction error (perfect recovery), while reducing to 5 components (80% variance) introduces moderate error, and reducing further to 2 components significantly increases error (~0.45 MSE). This demonstrates the trade-off between dimensionality reduction and information preservation.

Technologies Used:
Python, Pandas, NumPy, Scikit-learn, Matplotlib (for data processing, dimensionality reduction, and visualization)

Dataset:
The dataset used is the Wine dataset, which contains chemical analysis results of wines derived from three different Italian cultivars. Each sample includes measurements such as alcohol content, flavanoids, and color intensity, making it well-suited for exploring feature scaling and dimensionality reduction techniques like PCA.
