---
layout: page
title: Datasets
---
<strong>Two-vehicle ACC driving, Tennessee 2019</strong>
The data is collected from a 2019 model year ACC vehicle driven on a stretch of Interstate-65 for 15 min. The data is collected directly from the factory-installed radar unit via the follower vehicle's CAN bus, and contains velocity, space gap to the lead vehicle, relative velocities and accelerations. The data is preprocessed with an even sampling rate of 10Hz.

The detailed descriptions of data files are as follows:
1. Processed_CAN_Data_CMDa.csv
  * This csv file contains evenly sampled data in 5 columns: timestamps (s), follower vehicle velocity (m/s), lead vehicle velocity (m/s), space gap (m), ACC command acceleration (m/s^2)

2. Processed_CAN_Data_a.csv
  * This csv file contains evenly sampled data in 5 columns: timestamps (s), follower vehicle velocity (m/s), lead vehicle velocity (m/s), space gap (m), ACC vehicle actual acceleration (m/s^2)

The key reference paper for the dataset is:
- Y. Wang, G. Gunter, M. Nice and D. Work. Estimating adaptive cruise control model parameters from on-board radar units, 2019. <a href="https://arxiv.org/abs/1911.06454">Preprint</a>
<a href="https://vanderbilt.box.com/s/76m0vmlpzoj2059p047yt0jkx3mtyxdp">Download data</a>

<strong>Two-vehicle ACC driving, Tennessee 2018</strong>
- Description: A set of car following experiments are conducted to collect data from a 2015 luxury electric vehicle equipped with a commercial adaptive cruise control (ACC) system. Velocity, relative velocity, and spacing data collected during the experiments are used to calibrate an optimal velocity relative velocity car following model for both the minimum and maximum following settings.
- Publication: G. Gunter, C. Janssen, W. Barbour, R. Stern and D. Work, "Model based string stability of adaptive cruise control systems using field data," in IEEE Transactions on Intelligent Vehicles. doi: 10.1109/TIV.2019.2955368. <a href="http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8910461&isnumber=7448921">URL</a>
- <a href="#">Download</a>


<strong>Two-vehicle and platoon ACC driving, Arizona 2018</strong>
- Description: The driving data of each of the seven distinct vehicle models from two different vehicle makes in 2018 is collected with ACC engaged by the follower vehicle. In addition, the data of a multi-vehicle platoon experiment in which all vehicles are the same year, make and model is also collected.
- Publication: G. Gunter, D. Gloudemans, R. E. Stern, S. McQuade, R. Bhadani, M. Bunting, M. L. Delle Monache, B. Seibold, J. Sprinkle, B. Piccoli, and D. B. Work. Are commercially implemented adaptive cruise control systems string stable? 2019. <a href="https://arxiv.org/abs/1905.02108">Preprint</a>
- <a href="https://vanderbilt.app.box.com/v/accData">Download two-vehicle test data</a>
- <a href="https://vanderbilt.app.box.com/v/accData">Download platoon test data</a>

<strong>Urbana 10 car ring road test, 2016</strong>
This dataset contains trajectory and fuel consumption data from a series of 10 vehicle ring road tests as an extension to the Sugiyama et al. (2008) experiments. The dataset contains video data, the extracted trajectories from the camera, the smoothed trajectories, and the OBD-II logs from each equipped vehicle containing fuel consumption information.

<a href="https://uofi.box.com/v/RingRoadTRB">Download</a>

<strong>Ring-road experiment with one autnomous vehicle, Arizona 2016</strong>
- Description: The data is collected through the experiments on a circular track with a fleet of 22 vehicles, one of which is a self-driving capable Cognitive and Autonomous Test (CAT) Vehicle.
- Publication: R.E. Stern, S. Cui, M.L. Monache, R. Bhadani, M. Bunting, M. Churchill, N. Hamilton, R, Haulcy, H. Pohlmann, F. Wu, B. Piccoli, B. Seibold, J. Sprinkle, & D.B. Work (2018). Dissipation of stop-and-go waves via control of autonomous vehicles: Field experiments. ArXiv, abs/1705.01693. <a href="https://arxiv.org/abs/1705.01693">Preprint</a>
- <a href="https://doi.org/10.15695/vudata.cee.1">Download</a>


<strong>The Arizona Ring Experiments Dataset (ARED), Arizona 2018</strong>
- Description: Naturalistic driving data from a series of experiments to understand the development of phantom traffic jams.
- Publication: F. Wu, Stern, R. E., Cui, S., Monache, M. Laura Dell, Bhadani, R., Bunting, M., Churchill, M., Hamilton, N., Wu, F., Piccoli, B., Seibold, B., Sprinkle, J., and Work, D. B., The Arizona Ring Experiments Dataset (ARED). 2018.
- <a href="https://doi.org/10.15695/vudata.cee.2">Download</a>
