---
layout: post
title:  "Identifiability of car-following dynamics"
categories: []
image: assets/images/contour_CTHRV_1.webp
tags: [project]
---

The advancement of in-vehicle sensors provides abundant datasets to estimate parameters of car-following models that describe driver behaviors. The question of parameter identifiability of such models (i.e., whether it is possible to infer its unknown parameters from the experimental data) is a central system analysis question, and yet still remains open. We present both structural and practical parameter identifiability analysis on four common car-following models: (i) the constant-time headway relative-velocity (CTH-RV) model, (ii) the optimal velocity model (OV), (iii) the follow-the-leader model (FTL) and (iv) the intelligent driver model (IDM). The structural identifiability analysis is carried out using a differential geometry approach, which confirms that, in theory, all of the tested car-following systems are structurally locally identifiable, i.e., the parameters can be uniquely inferred under almost all initial condition and admissible inputs by observing the space gap alone. In a practical setting, we propose an optimization-based numerical direct test to determine parameter identifiability given a specific experimental setup (the specific initial conditions and input are known). The direct test conclusively finds distinct parameters under which the CTH-RV and FTL are not identifiable under the given initial condition and input trajectory.
