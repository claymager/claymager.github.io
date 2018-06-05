---
layout: post
title: Abstract Clustering
---

## Introduction

This project is the first in a series with the modest goal of using NLP
techniques to detect scientific papers that would be/should be/were retracted.

A necessary prerequisite is to cluster papers into topics similar enough that
their domain-specific language is irrelevant. Published keywords, while potentially helpful, were not prevalent enough in the corpus to validate their use. 

Abstracts, as opposed to the full-text of articles, are widely available and easy to scrape or process in large quantities. [Here](https://github.com/claymager/abstract_clustering), we compare clusters of
abstracts and of full-text documents to show that by performing NPL clustering on abstracts, we can get equivalent clusters of the full documents. This will then allow targetted processing to find retracted papers within similar documents, and potentially generalizable patterns.
