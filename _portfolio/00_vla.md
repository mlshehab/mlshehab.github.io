---
title: "Tactile-Annotated Vision Language Action Models"
excerpt: ".<br/><img src='/images/tavla_intro_figure.png'>"
collection: portfolio
---

In this ongoing work, we propose Tactile-Annotated Vision-Language-Action models (TaVLA), a
framework for integrating tactile feedback into VLA models through visual augmentation.
Current VLA models often struggle with contact-rich manipulation because tactile and force-
related information is not directly observable from RGB images. TaVLA extracts shear vectors
from visuo-tactile sensors and overlays them onto multi-view RGB images as spatially-grounded
annotations, allowing the policy to use tactile information without modifying the VLA
architecture or inducing major domain shift from pre-training. We validate TaVLA on a Franka
Emika Panda robot equipped with GelSight tactile sensors and multi-view RGB cameras. On
contact-rich tasks requiring physical reasoning, such as differentiating object mass and aligning
gears, TaVLA outperforms vision-only and alternative multimodal baselines, achieving an 80%
success rate.  

Below are videos of the tactile-augmented VLA policy, with the command: 
```place bottle in blue bin if empty, otherwise place in orange bin.```


Full Medicine Bottle:

<video width="90%" height="auto" controls>
  <source src="/images/full_tavla.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

Empty Medicine Bottle:
<video width="90%" height="auto" controls>
  <source src="/images/empty_tavla.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>