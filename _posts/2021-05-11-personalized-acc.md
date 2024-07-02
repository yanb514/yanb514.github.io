---
layout: post
title:  "Personalized ACC in a digital twin framework"
categories: [featured]
tags: [project]
image: assets/images/Unity2.png
---
Advanced driver-assistance systems (ADAS) have matured over the past few decades with the dedication to enhance user experience and gain a wider market penetration. However, personalization components, as a mean to make the current technologies more acceptable and trustworthy for users, have been gaining momentum only very recently. In my recent work with Toyota InfoTech Labs, we aim to learn personalized longitudinal driving behaviors via a Gaussian Process (GP) model. The proposed method learns from individual driver’s naturalistic car-following behavior, and outputs a desired acceleration profile that suits the user’s preference. The learned model, together with a predictive safety filter that prevents rear-end collision, is used as a personalized adaptive cruise control (PACC) system.

Numerical experiments show that GP-based PACC (GP-PACC) can reproduce the driving styles of human drivers up to 80% more accurately than baseline models (i.e., optimal velocity model and intelligent driver model). Additionally, GP-PACC is further validated by human-in-the-loop experiments on the Unity game engine-based driving simulator. Trips driven by GP-PACC and two other baseline ACC algorithms with driver override rates are recorded and compared. Results show that all drivers override the GP-PACC less frequently, indicating drivers trust GP-PACC more than other ACC algorithms.