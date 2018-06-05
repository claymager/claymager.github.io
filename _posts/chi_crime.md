---
layout: post
title: Chicago crime
---

## Introduction
The City of Chicago has the CLEAR (Citizen and Law Enforcement Analysis and Reporting) system
for making a vast amount of crime data public. I decided to look at this for my Week 3 project at Metis, hoping to get some power for predicting the type of crime to occur.

I looked at only the the absolute basics, as far as features went. Latitude and longitude, time of day, time of year, and a brief location description. The goal was to make a useable model that could be accessed through a phone in seconds, with little to no human input.

Ultimately I found very little predictive power in the provided data, but I'd like to revisit this project in the future.
I still feel there's a lot of potential, and that I just haven't found the important features yet.
Latitude and longitude were predictive with a Random Forest built around a bagging classifer (and numerous other models).
There may be a way to encode location in a way that improves predictive power over this naïve
implementation, but I haven't found it yet. Many, bizarrely, do worse, even when latitude and longitude are included.

## Data
