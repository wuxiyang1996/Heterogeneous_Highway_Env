# Heterogeneous Highway-env for iPLAN
Our forked version of [**highway-env**](https://github.com/Farama-Foundation/HighwayEnv) used in our paper:

[**iPLAN: Intent-Aware Planning in Heterogeneous Traffic via Distributed Multi-Agent Reinforcement Learning**](https://arxiv.org/abs/2306.06236)

More details could be found in the main page of [**highway-env**](https://github.com/Farama-Foundation/HighwayEnv)
and [**iPLAN**](https://github.com/wuxiyang1996/iPLAN).

# Installation
```angular2html
pip install Heterogeneous_Highway_Env
```

# Major Changes
* Add two behavior-driven vehicle models, `DefensiveVehicle` and `AggressiveVehicle` in `vehicle/behavior.py`.
* Add multi-agent support for `Highway` scenario given in `envs/highway_env.py`, modify the `MultiAgentWrapper`
in `vehicle/common/abstract.py`.
* Add three heterogeneous traffic scenarios, `HighwayEnvHetero`, `HighwayEnvHetero_H` and `HighwayEnvHetero_VH`
in `envs/highway_env.py`, with vehicle ID broadcasting and different behavior-driven vehicles.
* Add multi-agent support for visualization in `Highway` scenario that allows a camera following each agent
and visualize their surroundings from their respective viewpoints.

# Animation
The animation shows 5 such learning agents (Green) with their surroundings from their respective viewpoints. 
Behavior-driven vehicles in the environment include: Normal (Blue), Aggressive (Purple) and Defensive (Yellow).
Vehicles terminate (Red) when colliding with other vehicles.

<p align="center">
    <img src="animation/iPLAN_Hetero_H_5_90.0_21.81.gif"><br/>
    <em> iPLAN in chaotic (hard) scenario of Heterogeneous Highway 
    (Num of agents succeed: 5, Avg. survival time: 90, Avg. speed: 21.81).</em>
</p>