# Project 2 - Ames Housing Data and Kaggle Challenge

General Assembly DSI 19 Project 2 Adrian Teng 

## Project Introduction

In this project, I am tasked to create a regression model based on the Ames Housing Dataset to predict the price of a house at sale.

## Problem Statement

A real estate company is trying to re-evaluate on the pricing of their housings at sale. Through this action, the company hope that it will increase the profit from the popular housing by not selling undervalue  and at the same time bringing more sales with a reasonable pricing for the less popular housing. It will improve the service of the company that they could provide to their clients, for example, in getting a house within the market value depending on their demand. 

Hence, a Linear regression, Ridge and Lasso regression models will be created based on Ames Housing Data to show which model is more accurate in predicting the price of a house. 



## Executive Summary

In this project, it is splitted into three parts respectively:
- Data Cleaning (01_data_cleaning)
- Exploratory Data Analysis (02_eda)
- Conclusion (03_conclusion)

In the first notebook, 01_data_cleaning, data was reviewed. Missing and 'nan' values was replaced and outliners 

In the second notebook, 02_eda, numberical and categorical lists were created. Visualizing on features and correlation was done. New interaction features was created for better understanding.

In the third notebook, 03_conclusion, base line model was created with the top two features using linear regression to do comparison. Subsequently, dummies was added and tested with linear regression again. Next, standard scalar was used to test for Ridge and Lasso.

## Data Dictionary

[Link to data description] (http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

## Conclusion 

For the base line model, I have used linear regression for comparsion. Starting without getting dummies with only top two features, the score was relatively decent ~0.75. However, after getting dummies into the data and by adding more features into linear regression again, the score improved significantly ~0.91. 

Next, before trying Lasso and Ridge I have decided to use standard scalar. The Ridge score and Lasso score increased slightly and is comparable ~0.93/0.94. They result between Lasso and Ridge is similar and very close to perfect score 1.

Thus, I have decided to let Kaggle do the job and see which model will get a better score. In the end Lasso had a better score at 32595.7 and it will be recommended to predict the price of a house at sale.

Looking into the top 3 features against sale price:
- overall quality
- total area
- garage area

Overall quality
- Most of the house sold is at 5-7(average to good), at the price range between 50k-400k
- 8-9(above good), have the highest spread of price and the lowest minimum

Total Area
- Very high correlation, close to higher area almost equal to higher price
- High concentration 1800 to 3600 sq feet, around 100k to 360k

Garage Size
- High concentration 200-600 sq feet (good fit for 1-2 cars), around 80k-260k

## Recommendation

- Model to use Lasso
- Keeping the quality average to good conditions, at least clean and nothing is spoil
- 200-600 sq feet for garage size, good fit 1-2 cars (excess space can make for other purpose)
- Separate big area to 2 units or adding essential facilities ( within 1800 to 3600 sq feet)

