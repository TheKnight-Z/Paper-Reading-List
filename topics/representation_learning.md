- [Perception](#Perception)
- [Control](#Control)
- [General Agents](#General)

## Perception
This part mainly focuses on vision-related tasks.
- Gaussian Splatting
  - ECCV 2024, A Compact Dynamic 3D Gaussian Representation for Real-Time Dynamic View Synthesis, [arXiv](https://arxiv.org/abs/2311.12897), [Code](https://github.com/raven38/EfficientDynamic3DGaussian).
    - To Summarize.


## Control

## General
Including perception, decision, dynamics and control etc., everything that an agent needs.
- ICML 2022, Denoised MDPs: Learning World Models Better Than The World Itself, [arXiv](https://arxiv.org/abs/2206.15477),[website page](https://www.tongzhouwang.info/denoised_mdp/)
  - Main: Manually disentangle controllable/uncontrollable and reward-re/irrelevant component in envs; the criterion is to **minimize the MI between $x$ and $s$** in a self-supervised way.
  - Limitation: Data-driven; what about taking prior from FM to help compress.
- RePo: Resilient Model-Based Reinforcement Learning by Regularizing Posterior Predictability, [arXiv](https://arxiv.org/abs/2309.00082), [website page](https://zchuning.github.io/repo-website/)
  - Main: learn the dynamics and reward based on $z_t$ which is compressed from $x_t = h(o_t)$ by using posterior $p(z_{t+1}|z_t,a_t,x_{t+1})$; test-time adaptation needs further investigation
  - Lessons: Lower bound for reward prediction and upper bound for dynamics compression; How can we solve the task-relevant stochasticity?

**To Read**: 

1. [CoRL 2023 LEAP workshop](https://openreview.net/group?id=robot-learning.org/CoRL/2023/Workshop/LEAP#tab-accept-oral)