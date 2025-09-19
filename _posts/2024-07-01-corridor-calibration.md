---
layout: post
title: "A digital twin infrastructure calibrated on real-world corridor data"
categories: [featured]
tags: [project]
image: assets/images/digital_testbed.png
image_link: https://drive.google.com/file/d/1xjl9UkrndOd8Njgg4wSKrhVSPub3z5uS/view?usp=drive_link
paper_link: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5065262
github_link: https://github.com/yanb514/CorridorCalibration
slides_link: https://drive.google.com/file/d/1xjl9UkrndOd8Njgg4wSKrhVSPub3z5uS/view?usp=drive_link
---

Imagine you’re driving on a congested freeway and find yourself caught in stop-and-go waves. These seemingly spontaneous traffic patterns—where vehicles repeatedly speed up and slow down—are surprisingly hard to replicate in microsimulation models. Even with perfectly calibrated inputs based on individual vehicle trajectories, many models struggle to capture the collective dynamics that emerge at the system level.

### The problem 

For decades, we’ve been working toward building digital twins of our roadways—but a persistent gap remains between the microscopic and macroscopic. On one hand, we can model how individual drivers behave in close detail: how one car follows another, how drivers react to speed changes, and so on. But when we zoom out, those same models often fail to reproduce the larger traffic phenomena we actually observe—like stop-and-go waves or systemic congestion.

So here’s the question: instead of fixating on modeling every vehicle’s trajectory (which is difficult to observe and even harder to scale), what if we focused on the emergent patterns we *can* see and measure?

### The approach: calibration based on the patterns

Rather than attempting to replicate every vehicle trajectory (an area extensively studied through driver behavior identification and car-following model calibration), we shift focus to what transportation agencies have long measured and monitored: flow, speed, and occupancy, as captured by loop detectors embedded in most highways. These aggregate traffic metrics offer a practical and scalable foundation for building behaviorally realistic digital twins of freeway systems.

Our approach implements a simulation-in-the-Loop optimization framework, where the traffic simulation environment (SUMO) is iteratively tuned to align with real-world sensor data. This creates a feedback loop: observed traffic patterns guide the simulation, and the simulation continuously adjusts its internal parameters to better reflect reality.


The workflow is:
1. **Data-driven initialization**: Real-time or historical measurements from loop detectors feed into the model, including flow, speed, and occupancy at measured locations.
2. **Behavioral tuning**: We adjust microscopic simulation parameters governing car-following, lane-changing, and speed choice behavior to improve fidelity.
3. **Pattern-level validation**: Custom metrics assess how well the simulated traffic reproduces observed system-level patterns (e.g., shockwave propagation, congestion dynamics).


### Some findings

In the process of calibration, we found that although there are a wide range of parameters to tune (e.g., following distance preferences, lane-changing aggresiveness, speed heterogeneity), only a few things actually impact the overall traffic patterns:
- IDM parameters such as free-flow speed and desired time-headway, predominately influences the patterns
- Speed measurements alone are usually sufficient to calibrate all parameters


### Scaling up: Interstate 24 as a testbed
The true test of our framework came when we applied it to a real-world freeway segment: Interstate 24. This corridor experiences the full spectrum of traffic behavior—from free-flow conditions to heavy congestion—and offered a challenging, high-variability environment for model validation.

The results were promising:
Our calibrated simulation reproduced key macroscopic features such as recurring bottlenecks, stop-and-go waves, and flow breakdowns. The model generalized well to different traffic conditions. All of these are achieved using DOT type of traffic measurement data only.


### Why this matters

With a validated digital twin that mirrors real-world traffic behavior, agencies and researchers can explore scenarios that are otherwise risky, costly, or impossible to test in the field:

- **Evaluating emerging technologies**: Assess how connected or autonomous vehicles influence traffic stability and throughput.
- **Traffic operations optimization**: Simulate new signal timing plans or ramp metering strategies before live deployment.
- **Infrastructure planning**: Compare the cost-effectiveness of adding lanes versus smarter traffic management.
- **Policy testing**: Model the impact of regulatory changes like variable speed limits, HOV lane enforcement, or tolling strategies.

You can find the complete implementation at [github.com/yanb514/CorridorCalibration](https://github.com/yanb514/CorridorCalibration).

---
**Repository**: [github.com/yanb514/CorridorCalibration](https://github.com/yanb514/CorridorCalibration)<br>
**Slides**: [Presentation](https://drive.google.com/file/d/1xjl9UkrndOd8Njgg4wSKrhVSPub3z5uS/view?usp=drive_link)<br>
**Manuscript**: [Calibrating microscopic traffic models with macroscopic data](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5065262)<br>
**Authors**: Yanbing Wang (ASU), Felipe de Souza (ANL), Yaozhong Zhang (ANL), Dominik Karbowski (ANL)
