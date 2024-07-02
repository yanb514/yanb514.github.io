---
layout: post
title:  "Estimation for heterogeneous traffic states"
categories: []
image: assets/images/comingsoon.jpg
tags: [project]
---

This work explores the state estimation problem for heterogeneous traffic (a multiclass flow composed of vehicles with distinct sizes and driving behaviours) using
particle filtering (PF) approaches. We consider three enhanced variations of the
bootstrap PF to improve estimation. The benchmark PF utilises a deterministic
partial differential equation and an additive process noise that is state-independent.
For the enhanced variations we first consider a parameter-adaptive PF that also
allows model parameters to be adjusted. The second variation is a standard PF
with spatially-correlated noise. The last variation combines parameter-adaptive and
the spatially-correlated-noise approaches. We compare the four filters in numerical
experiments that represent complex heterogeneous traffic scenarios, as well as on
real-world heterogeneous traffic data. The results show that the enhanced filters can
achieve up to an 80% and 46% of accuracy improvement as compared to an open
loop simulation without measurement correction, with the synthetic settings and
with real traffic data, respectively. Moreover, the enhanced filters outperform the
standard PF in all the traffic scenarios based on accuracy.


#### Resources
- [Estimation for heterogeneous traffic using enhanced particle filters][article]

[article]: https://lab-work.github.io/download/wang2021estimation.pdf