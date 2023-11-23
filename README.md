# House-Prices
This repository was made to explain the project of **[Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview/tutorials)**:

**The comments in the codes are in PT-BR**
## Objectives:
- Complete project using the Kaggle database to predict house prices in the USA.
## Main libraries used:
- Pandas, Numpy, Sklearn (metrics, linear model, model selection), XGBoost and Seaborn.
## You can find me at:
&nbsp;<a href="https://www.linkedin.com/in/brunofcb/">
  <img src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white">
</a>&nbsp;
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
## [Step 3.1: Data Processing](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Terceira%20parte.ipynb)
- Utilizing the dataset generated in [step 2](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Segunda%20Parte.ipynb), with the data already processed, we began by analyzing the **correlation between numerical variables and the most frequent values of text variables**.
- For text processing, I chose to **eliminate very similar values** and then used functions to assist in the processing. 
- I also used the **OneHotEncoder and OrdinalEncoder** to process the remaining text columns.
- After performing these treatments, I submitted it once again on Kaggle to assess the results after this initial part and determine how to proceed with the rest of the dataset.
- The public score returned by Kaggle was: 0,19178. I worsened my project a bit, so I need to continue treating the remaining data
## [Step 3.2: Data Processing_2](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Terceira%20Parte_2.ipynb)
- After the Kaggle result, I started processing the rest of the database, treating the text columns.
- I separated the columns into indices, checking whether or not there is a classification in order, following the data given in the document
- After separating the data, we obtained 169 columns, (initially we had 80, disregarding the SalePrice column)
- Submitting the base to Kaggle, we obtained a result of 0.59356. The worsening of the result is due to the exaggerated number of columns with few lines, which I will deal with in the next step.
## [Step 4: Checking other models.](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Quarta%20Parte_1.ipynb)
- At this stage I chose to do 2 simulations with 2 other models. A first simulation using base 3.1 and another using base 3.2.
- In addition to linear regression (which was the model that initially had the best performance), I used XGBoost (suggested by the database itself) and Random Forest.
- Performing the same treatments on both bases. Random Forest had better performance and we used it in the test base.
- Submitting the database to Kaggle, we obtained a result of 0.15459 in [step 4.1](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Quarta%20Parte_1.ipynb) and a Score of 0.15301 using [step 4.2](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Quarta%20Parte_2.ipynb), that is, just by changing the model used we achieved a substantial improvement in the data.
- 
## [Step 5: Considerations and results.](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Kaggle.png)
- When analyzing this model I tried to be as careful as possible to avoid overfitting, at no point did I go after the 0.0 score, I just wanted to create a general model so that it can be used on any other occasion.
- All Kaggle results are available in the Kaggle.
   ![Kaggle](https://github.com/BrunoFelipeCB/House-Prices/blob/main/Kaggle.png)
