---
layout: post
title:  "More data ≠ better results?"
categories: [featured, exclude]
image: assets/images/comingsoon.png
tags: [project, eda]
keywords: [arterial corridor, camera, SPaT, simulation, calibration, edge computing]
---
Recently my PhD student and I have been exploring a seemingly simple problem. The result: sometimes having more data may cause more harm than good.

### The Problem
This problem originated from a recent collaboration with Argonne National Lab. The team wants a realistic traffic simulator. This has been a long studied problem in the transportation research community for decades, because 

1. traffic simulators are notoriously unrealistic; 
2. calibrating such as simulator has been a less well-defined, or well-benchmarked, and tedious task. 

It is also a problem I've been working on for a while. So being presented with this challenge I thought it wouldn't be a new challenge, but I was wrong.

The specific corridor that we're interested in modeling is the Roosevelt Rd EW, 7 intersections leading up to the Michigan Ave. in downtown Chicago. The goal is to replicate a normal day traffic scenario on the Roosevelt corridor in the simulation, which requires setting up the correct variations of origin-destination (OD) flows on all routes. This is a typical OD flow calibration problem and is often *underdetermined*, as there are infinitely many solutions to this problem. 

<!-- $$min \left|\right|$$ -->

Since we have multiple data sources (see below), hopefully this problem can be regularized.

[insert a picture]

### The Data
There are three possible data sources:

#### 1. Vehicle counts at intersections
Thanks to the MCS team at Argonne, which has been leading the Edge Computing project Sage Node [link], we are able to measure the number of cars waiting at each lane at each intersection. This gives us the intended movement of each vehicle. 

However, due to the edge computing constraint, the current configuration only allows to process 1min of video data every 7-11 minutes. That is, every 7-11 min window, the system will output the traffic count for the video recording collected during the first 1 min.

This essentially gives a sparse observation. If unfortunate, we may miss an interesting event happening outside of the recording time, but such a configuration would still give us important trend, such as morning and evening rush hour.

[insert a sage node picture with traffic count]

#### 2. Link-based average travel time
Another data source is from a commercial platform RITIS, that collects link-level average speed and travel time from floating vehicles. Essentially, they have access to about 4% penetration of drivers who have their smart phone locations turned on and constantly logging their GPS information. This data is then aggregated to [TMC links][tmc_links].

However, we discovered that the TMC links from the dataset and the links on the map do not match exactly, which makes the expected travel time inconsistent with that from the RITIS data. Eventually we used some manual mapping to have multple TMC links matached with muliple links on the map. To some extent, this aggregation step introduces some errors. For example, if link 1 and link 2 are connected by an intersection, the average travel time to traverse both links may not be the sum of two, because cars leave or enter at that intersection.

[insert plot tmc links]

#### 3. Signal phase and timing (SPaT)
SPaT

### The Results

[TMC Links][tmc_links]:https://wiki.openstreetmap.org/wiki/Proposal:Relation:tmc/TMC_Links


