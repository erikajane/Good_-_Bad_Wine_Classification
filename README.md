# Good or Bad Wine Classification

## Introduction

When looking for a new wine to try, the hope is that you pick a good one. Unfortuantely, you won't know that wine is good or not until you taste it. Luckily if you are able to obtain the physiochemical properties of the wine you intend on buying, you can figure out if the wine is good or not.

What makes a 'high quality' wine, 'high quality'? (What features does a high quality wine include?

Can we predict whether a wine is 'high quality' or not by looking at it's features?

## The Data

From University of California, Irvine’s Machine Learning Repository, two datasets were utilized, __winequality-red__ and __winequality-white__ (https://archive.ics.uci.edu/ml/datasets/wine+quality). The two datasets include physicochemical information  on either red or white wine samples from Northern Portugal. The following twelve physicochemical features for each observed wine sample are as follows:

 - fixed acidity
 - volatile acidity
 - citric acid
 - residual sugar
 - chlorides
 - free sulfur dioxide
 - total sulfur dioxide
 - density
 - pH
 - sulphates
 - alcohol
 - quality

Since the goal of this project is to determine whether a wine is good or bad, we will be trying to predict quality (scored between 1 and 10), using the other physiochemical features.

## Data Preprocessing and Exploratory Data Analysis

### Red Wine

The red wine dataset included 1599 observations, but after dropping 240 duplicates, 1359 observations remain.

Although, quality is scored on a scale of 1 through 10, we see that the red wine samples only scored quality scores between 3 and 8. The majority of wine had been given scores of 5 and 6.

##### Insert Picture Here (Red_Wine_Quality_Distribution.png)

Since the goal is to classify whether a wine is good or bad, the quality scores are reassigned. Wines  with a quality of 6 and below are assigned a numberic value of __0__ and will be considered _'bad wines'_ and wines with a quality score of 7 and above are reassigned a value of __1__ and will be considered _'good wines'_.

##### Insert Picture Here (Red_Wine_Good_Bad_Distribution.png)

After binning our target variable, quality, into binary variables for good and bad wine, the dataset now has __1,175 Bad Wines__ and __184 Good Wines__.

##### Insert Picture Here (Red_Wine_Good_Bad_Wine_Distribution_Stats.png)

