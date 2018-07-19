---
layout: post
title: Ski World Cup dnf rates
---

## Introduction

The intention for this project was to use linear regression to predict rates
of did-not-finish (DNF) in world cup alpine ski racing events.

## Data

Data was scraped from published FIS records, from 2010 to 2018.

 - event type (slalom, GS, etc)
 - date
 - entrants
 - location

I set 150 events aside for validation, and used the remaining 600 for
modelling.

## Model design

### Loss function: Mean Absolute Error
Certain observational features that were not available in the data, such as
poor visibility or snow conditions, could have significant effects on DNF rate
and would be obvious to people on the ground. MAE avoids
penalizing such outliers as strongly as MSE or adjusted R^2^.

### Regularization: L1
I tend to prefer L1 in theory. Might be the biologist in me, but I prefer
to zero irrelevant signals. At the time I also thought I had a lot of features
to control.

## Results

![coefficients](https://raw.githubusercontent.com/claymager/claymager.github.io/master/images/fis_coefs.png)
By far the strongest predictor was event type, with DNFs in Slalom being the most common and Downhill being the least. The position in the ski season, the gender of the athletes, and the 
geographic region also played significant roles.

[residuals](https://raw.githubusercontent.com/claymager/claymager.github.io/master/images/fis_resid.png)
Apparent heteroschedasticity of the residuals is largely because of the lower-bound rate of 0 .

