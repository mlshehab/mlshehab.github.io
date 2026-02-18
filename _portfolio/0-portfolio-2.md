---
title: "Traffic Rule Compliant AVs using end-to-end RL"
excerpt: "Ongoing project on using end-to-end RL with Reward Machines to encode traffic rule compliance into the RL learned policy."
collection: portfolio
---

TL;DR: Traffic-rule compliance is a non-markovian specification. For example, in a stop-and-go scenario, the AV can only pass the stop line after it has already stopped. This means that specifying the correct behavior requires storing the AV's history (hence the non-markovianity). This yields RL algorithms that rely on markovian rewards obselete. In this work, we show that traffic rule compliance can be encoded into an end-to-end RL controller for self driving cars. By carefully designing reward machines that encode these rules, we obtain controllers that obey the traffic laws in 100% of the tested scenarios, and achieve a 0% collision rate. 

A sample reward machine for the stop-and-go task is presented here. 

<img src="/images/stop_and_go.png" alt="Sample Reward Machine for Stop-and-Go Task" style="max-width:50%; height:auto;">

> 
> If you are eager to know what the labels of the above figure stand for, please wait until our manuscript is out!
>

Here's a sample of the resulting behaviors in a [highway-env](https://github.com/Farama-Foundation/HighwayEnv) simulator. The training curves are shown next, comparing our method to some baselines. 

<video width="70%" height="auto" controls>
  <source src="/images/stop_n_go_vid.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<img src="/images/stop_and_go_training_curves.png" alt="Training Curves for Stop-and-Go Task" style="max-width:70%; height:auto; display:block; margin:auto;">

<p style="text-align:center; font-size:0.95em;">Figure: Training curves showing the performance of our method compared to baselines.</p>


We are also working on an unsignalized intersection scenario generated using [Scenic](http://scenic-lang.org/). By encoding a first-come-first-serve logic using scenic, we can generate training scenario where background vehicles also comply with the priorty rules at intersection. 
