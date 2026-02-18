---
title: "Traffic Rule Compliant AV using end-to-end RL"
excerpt: "Ongoing project on using end-to-end RL with Reward Machines to encode traffic rule compliance into the learned policy."
collection: portfolio
---

TL;DR: Traffic-rule compliance is a non-markovian specification. For example, in a stop-and-go scenario, the AV can only pass the stop line after it has already stopped. This means that specifying the correct behavior requires storing the AV's history (hence the non-markovianity). This yields RL algorithms that rely on markovian rewards obselete. In this work, we show that traffic rule compliance can be encoded into an end-to-end RL controller for self driving cars. By carefully designing reward machines that encode these rules, we obtain controllers that obey the traffic laws in 100% of the tested scenarios, and achieve a 0% collision rate. 

A sample reward machine for the stop-and-go task is presented here. 

<img src="/images/stop_and_go.png" alt="Sample Reward Machine for Stop-and-Go Task" style="max-width:70%; height:auto;">

> [!WARNING]
> If you are eager to know what the labels stand for, please wait until our manuscript is out!

Here's a video demonstrating the resulting behaviors in a [highway-env](https://github.com/Farama-Foundation/HighwayEnv) simulator. 

<img src="/images/intersection_sg_rm.gif" alt="Stop-and-Go Demo" style="max-width:70%; height:auto;">
