# Pump-it-Up-Data-Mining-the-Water-Table
Github Link : https://github.com/KrishPraba/Pump-it-Up-Data-Mining-the-Water-Table

This repository contains code generated for submissions made for the competition **Pump it Up: Data Mining the Water Table**, hosted by **DrivenData.**

The files in this repository are :
  1. **Pump it up - EDA** - Exploratory data analysis on the features of the dataset.
  2. **Pump it Up - Preprocessing & Feature Engineering** - Pre processing the data and employing feature engineering techniques to the features of the dataset to create a clean     dataset that was used for modelling
  3. **Pump it Up - Modelling & Post processing** - Using various modelling techniques on the cleaned dataset generated from the notebook above and comparing result, Post processing was also conducted


## Exploratory Data Analysis

First the missing values and unique column values were analysed to get an overview of the outliers and the null values in the dataset

Next Numeric columns were analysed. Here the statistics of the numeric data was observed (mean, median, number of datapoints etc) , next coorelation between the numeric variables was visualised following this histograms and violin plots were used to visualise the variability of the numeric columns. The longitude and latitude was also plotted using a map to 
visualise the regions they were spread on and identify the outliers.

Following this Object columns were analysed. Sets of object columns with certain degree of similarities were analysed together using groupby() functionalities to detect hierarchies and using bar plots to visulaise the spread of datapoints over the three label classes using these results inferences were made. Other unique columns were also analysed. Duplicate columns were identified and columns with only one unique column value was also discovered.

Finally an analysis on the spread of datapoints over the three target classes was visualised using barplot and it was discovered that there was a major class imbalance between the three target classes


## Pre-processing and Feature Engineering

Mutual information scores were calculated and visualised. Following this outliers and missing values were handled using a combination of multiple approaches depending on the column
  1. The null values in the columns were filled with a seperate unique category which was "Unknown" for object columns. No null values were observed from numeric columns
  2. The outliers of the installer columns ( columns with value "0" ) were converted to a unique category "Unknown"
  3. The outliers of the longitude and population columns ( columns with value "0" ) were converted to the mean value of the datapoints
  4. The outliers of the construction year field ( columns with value "0" ) were converted to the median value of the datapoints
 
Feature encoding was done on the categorical features. Two approaches were tried out onehot encoding and label encoding, Label encoding proved to be effective and efficient considering the large number of features present. Normalisation was also done on the numerical features using minimax normalisation.

Finally based on the exploratory data analysis conducted on the features multiple features were dropped.


## Modelling and Postprocessing

### Models used
  1. CATBoost Classifer
  2. RandomForestClassifier
  3. ExtraTreesClassifier
  4. XGBClassifier
  5. GradientBoostingClassifier
  6. SVM
  7. AdaBoost Classifier
 
### Post processing
Feature importance plots were plotted to identify the most important features, using RandomForest Classifier. SHAP dependence contribution plots were also plotted as part of post processing.


## Results Obtained

DrivenData Username - **moracse_170454J**


      
