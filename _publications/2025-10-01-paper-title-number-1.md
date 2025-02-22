---
title: "Learning Reward Machines from Partially Observed Optimal Policies"
collection: publications
category: manuscripts
permalink: /publication/2025-10-01-paper-title-number-1
excerpt: 'This paper deals with learning reward machines (FSM) from partial expert policies.'
date: 2025-02-06
venue: 'arXiv'
paperurl: 'https://www.arxiv.org/abs/2502.03762'
---

Inverse reinforcement learning is the problem of inferring a reward function from an optimal policy. In this work, it is assumed that the reward is expressed as a reward machine whose transitions depend on atomic propositions associated with the state of a Markov Decision Process (MDP). Our goal is to identify the true reward machine using finite information. To this end, we first introduce the notion of a prefix tree policy which associates a distribution of actions to each state of the MDP and each attainable finite sequence of atomic propositions. Then, we characterize an equivalence class of reward machines that can be identified given the prefix tree policy. Finally, we propose a SAT-based algorithm that uses information extracted from the prefix tree policy to solve for a reward machine. It is proved that if the prefix tree policy is known up to a sufficient (but finite) depth, our algorithm recovers the exact reward machine up to the equivalence class. This sufficient depth is derived as a function of the number of MDP states and (an upper bound on) the number of states of the reward machine. Several examples are used to demonstrate the effectiveness of the approach.

Here's a video of a [Franka Emika Panda robot](https://frankaemika.github.io/docs/index.html) stacking blocks using the reward machine learned. The simulation is done using the [CoppeliaSim](https://www.coppeliarobotics.com/) Simulator. The control is done using [PyRep](https://github.com/stepjam/PyRep).

<video width="640" height="360" controls>
  <source src="../images/lrm_panda_arm_stacking.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>