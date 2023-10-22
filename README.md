# House-Prices
This repository was made to explain the project of **[Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview/tutorials)**:
## [Step 1: First model](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Primeira%20parte.ipynb)
- At the beginning, I chose to do only basic treatments, removing empty values ​​without any type of data engineering.
- For simplicity, I treated empty values ​​as '-1', to make it clear that the data transition process was correct, but the data was non-existent. As there are no negative values ​​native to the base, this transformation will not be a problem.
- To use the machine learning models, we removed all text columns, and after separating the kaggle training database into training and testing, we used 3 methods that I thought were simplest to carry out the analyses.
- To evaluate the model, I will use the [mean absolute error](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html) and the [mean squared error](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html), as these are the criteria used in the competition.
- The public score **returned by Kaggle was: 0.25476**. It's important to note that we won't aim for a 0.0 error to avoid overfitting."
## [Step 2: Data Cleaning](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Segunda%20Parte.ipynb)
- In this stage, I began **data preprocessing and cleaning**, analyzing **various values and missing information** to determine the best strategy.
- In some columns, **empty values did not indicate a lack of information**, but rather the absence of a specific attribute, for example, the fireplace.
- In other cases, the missing information truly represented a lack. Therefore, I chose to replace these values with some meaningful attribute.
- The same model from [stage 1](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Primeira%20parte.ipynb) was used."
- The public score returned by Kaggle was: 0,1812.
## [Step 3: Data Processing](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Terceira%20parte.ipynb)
-Utilizing the dataset generated in [step 2](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Segunda%20Parte.ipynb), with the data already processed, we began by analyzing the **correlation between numerical variables and the most frequent values of text variables**.
- For text processing, I chose to **eliminate very similar values** and then used functions to assist in the processing. 
- I also used the **OneHotEncoder and OrdinalEncoder** to process the remaining text columns.
- After performing these treatments, I submitted it once again on Kaggle to assess the results after this initial part and determine how to proceed with the rest of the dataset.
- The public score returned by Kaggle was: 0,19178. I worsened my project a bit, so I need to continue treating the remaining data
