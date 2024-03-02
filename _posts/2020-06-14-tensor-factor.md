---
layout: post
title:  "Large spatial-temporal data processing via tensor factorization"
categories: [  ]
image: assets/images/aotheatmap.png
tags: [project]
---

The US Environmental Protection Agency identifies that urban heat islands can negatively impact a community’s environment and quality of life. Using low cost urban sensing networks, it is possible to measure the impacts of mitigation strategies in communities at a fine-grained scale, informing context-aware policies and infrastructure design. However, fine-grained city-scale data analysis is complicated by common, tedious data cleaning tasks such as removing outliers and imputing missing data. To address the challenge of data cleaning, this article introduces a robust low-rank tensor factorization method to automatically correct anomalies and impute missing entries for high-dimensional urban environmental datasets. We validate the method on a synthetically degraded National Oceanic and Atmospheric Administration temperature dataset, with a recovery error of 4%, and apply it to the Array of Things city-scale sensor network in Chicago, IL.