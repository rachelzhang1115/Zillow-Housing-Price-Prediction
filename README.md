# Housing Price Prediction with Scrapped Zillow Data
For this project, I predicted housing prices with housing features data scrapped from Zillow.com. I collected a total of 1,487 observations, while each observation includes features such as house address, bed, bath, sqft, lot size, house type, year built, and school ratings, and the target value sold price.

**Data Correlation Visualization**
* For initial analysis, I visualized the correlation between the target variable and each of the feature variables using `sns.pairplot()`

**Train-Test Split**
* Used the last digit of street number as a metric for train-test split. 
* Doing so avoids the data leakage problem since this split method will group similar-featured apartments from the same address into the same dataset.

**Feature Engineering**
* Sorted `feature_importances` for all the features. 
* For the least important features, I generated a random permutation of those features and ran the same model with the randomly permuted features. A feature has to perform better than its randomly permuted pair to be included in the future models.

**Model Selection**
* Trained Linear Regression, Lasso CV, Random Forest, and Gradient Boosting Regressions with a grid search for best parameters. 
* Random Forest Regression has the best R-square (0.77).
* Visualized model's fitness and residuals using `matplotlib`

**Conclusion**
* Square footage, lot size, and house type matters the most for housing prices


