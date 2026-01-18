**ABSTRACT:**

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



**SUPPLEMENTARY METHODS:** 

When dealing with model generation and dataset analysis it is importnat to consider the relationship between variables prior to analysis. Therefore the following plot was created to visualise correlations between variables in the entire dataset.
<img width="3000" height="3000" alt="dataset_wide_correlation_plot" src="https://github.com/user-attachments/assets/d83fed9c-10ec-47d7-aba6-102847401927" />


The structure of missing data can have a large impact on imputation quality and reliability, especailly when dealing with such small sample sizes. Therefore the structure of missing data across all permuatations of dataset used in the present study are included bellow as well as a correlation matrix to exmain variable co-linearity. 
**Original dataset missing structure:**
<img width="1800" height="1200" alt="original_data_missing_distribution" src="https://github.com/user-attachments/assets/73ee2a3c-50e7-485a-bbb6-47560e373202" />
This graph shows the structure of missingess in the original dataset prior to cleaning 

**Cleaned/augmented dataset missingness structures**
a)
<img width="1800" height="1200" alt="original_data_missing_distribution" src="https://github.com/user-attachments/assets/b1bdf7ec-1bb3-490c-a6bf-b019adc06661" />
b)
<img width="1800" height="1200" alt="augmented_50_to_impute_data_missing_distribution" src="https://github.com/user-attachments/assets/19afa2d5-afe6-4e38-8f52-c4cc83f8ac79" />
c)
<img width="1800" height="1200" alt="augmented_100_to_impute_data_missing_distribution" src="https://github.com/user-attachments/assets/216292fb-a493-4c12-bfb5-17ace54e3a93" />
d)
<img width="1800" height="1200" alt="augmented_200_to_impute_data_missing_distribution" src="https://github.com/user-attachments/assets/8e309a98-6ea1-471c-b277-a6d664a4e9fb" />



These graphs show the structure of missingness in the cleaned original dataset (a) as well as the agumented datasets with 50 (b), 100 (c), and 200 (d) "patients" respectively. These are a representation of what the simulated missingness added to datasets for imputation evaluation in the evaluation loop looks like. As the missingess in the evalueation loop is random every time these simply serve to illustrate the difference between synthetic missingness that imputaiton was evaluated on compared to the naturally occureing missingess of the original dataset 
