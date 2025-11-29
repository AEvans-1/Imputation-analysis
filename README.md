Abstract Text
Background: Missing data is a pervasive issue in clinical pathology datasets, introducing bias if not handled
correctly. This problem is exacerbated in rare cancers with low data availability. Imputation refers to filling in
missing values, and its use is common, yet there is no consensus on the best method in small datasets. As
healthcare becomes increasingly data-driven, rare cancers risk being left behind.
Methods: Imputation methods were evaluated in a dataset of patients treated with cisplatin for trophoblastic
tumours (n=30). Missing data was removed creating clean data (n=22), and logistic regression models
generated. Larger simulated datasets (n=50, n=100, n=200) were created by adding Gaussian noise. Missing
values were added at random, imputed, and then compared to true values over 1000 iterations, with root
mean squared error (RMSE), mean absolute error (MAE), and raw bias (RB) calculated in standard deviation
units (SDs). Regression models were rebuilt after imputing the original dataset and compared to complete-
case models.
Results: Random forest single imputation (RF-SI) was most accurate in the original dataset (RMSE 0.77 SDs,
MAE 0.62 SDs, RB -0.044 SDs). K-nearest neighbour (KNN) gave similar results in the original dataset, but
outperformed RF-SI in larger datasets (RMSE 0.49 SDs vs 0.56 SDs at n=200). Multiple imputation (MI)
methods were least accurate in very small datasets but improved as datasets trended larger. RB was
consistently low across all methods and datasets(<|0.1|SDs). KNN and RF-SI did not skew regression when
used to impute the original dataset.
Conclusions: RF-SI is the most accurate method of imputation for very small clinical datasets, with KNN more
effective as size increases. MI performed poorly with low patient numbers but improved as datasets trended
larger. Both KNN and RF-SI can support regression modelling in rare disease research.
