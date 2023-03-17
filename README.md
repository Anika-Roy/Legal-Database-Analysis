# Legal Database Analysis
## Anika Roy- UG2 CND -2021113008

This repository is an exploration of a legal database from [Development Data Lab](https://www.devdatalab.org/) whose csvs can be downloaded [here](https://www.dropbox.com/sh/hkcde3z2l1h9mq1/AAB2U1dYf6pR7qij1tQ5y11Fa/csv?dl=0&subfolder_nav_tracking=1). This is a database of ~80 million Indian district court data across states and my objective was to extract meaningful data and insights from it and to train models that could be used to predict something useful.

## Directory Structure
 The task had 2 broad subproblems- Analysis and Classification. 3 insights required for analysis are in the analysis folder named insight_x.ipynb. Classification using ML models has been split into 2 notebooks-- traditional ML models and Neural Networks. Insights for classification problems are in the jupyter notebooks themselves. Every subfolder in plots contains images of all the plots in the notebook. The directory structure is:
```
.
+-- README.md
+-- analysis
|   +-- insight_1.ipynb
|   +-- insight_2.ipynb
|   +-- insight_3.ipynb
+-- classification
|   +-- neural-network.ipynb
|   +-- trad-ml-models.ipynb
+-- plots
|	+-- insight_1
|	+-- insight_2
|	+-- insight_3

```

## Commands to run

All code was written on kaggle, so running files is just running a jupyter notebook. All modules that are needed have been imported in the notebook intself (like plotly express, pandas, numpy sklearn classifiers etc). 

## The approach I followed

1. The first step was to understand all the data we had been provided. I did this by creating an [excel sheet](https://docs.google.com/spreadsheets/d/1pPcdgJegBD0y-4DMisjrn77bCCmAhoh4xHnkMjYPdjk/edit?usp=sharing) with all meta data that we had been provided so that I could clearly see what all data I can extract.
2. Through analysing the meta data provided, I found biases that that could be studied like how tenure of judges changes with gender and judge position or the performance of various states in resolving cases of Domestic violence and how that performance has changed over the years.
3. For classification, I chose to predict case verdicts using ML models so that people filing the case under certain judges with specific case types in a particular region can weigh their odds of winning and optimise on that
4. The frequency of many verdicts is very low, making the data skewed and thus tougher to train a model on. Thus I chose 3 broad labels-- convicted, acquitted and others. In spite of this, the 'disp_var_missing' label still made the data a little skewed.
5. I divided the whole project into multiple notebooks so that they could be run parallely and a single error somewhere in the beginning wouldn't cascade downwards.
6.  I divided my ML training notebooks into - traditional models( Catagorical Naive Bayes, K- nearest neighbours, Decision trees and Random Forest) and training a artificial neural network. The highest accuracy here was 0.85 with Random Forest.
7. Then I trained a sequential neural net using the same parameters as traditional ML models except for judge id. The first run of the neural network gave a 0.96 accuracy which I have submitted. However, I didn't achieve this in any subsequent runs. 
8. After a lot of debugging and proof-reading, the project was complete!

## Link to the repository

The respository link is [here](https://github.com/Anika-Roy/Legal-Database-Analysis). Hope you like it!

## Bibliography
1. https://medium.com/analytics-vidhya/machine-learning-classification-algorithms-with-codes-5a8af4491fcb
2. https://www.analyticsvidhya.com/blog/2021/10/implementing-artificial-neural-networkclassification-in-python-from-scratch/
3. https://www.kaggle.com/code/durgancegaur/a-guide-to-any-classification-problem
4. https://towardsdatascience.com/my-ml-model-fails-why-is-it-the-data-d8fbfc50c254
5. https://www.analyticsvidhya.com/blog/2021/10/implementing-artificial-neural-networkclassification-in-python-from-scratch/
6. https://www.mltut.com/implementation-of-artificial-neural-network-in-python/
7. https://towardsdatascience.com/using-the-right-dimensions-for-your-neural-network-2d864824d0df
8. https://machinelearningmastery.com/how-to-choose-loss-functions-when-training-deep-learning-neural-networks/
















