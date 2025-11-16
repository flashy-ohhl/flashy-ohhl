# Semantic-AD
This is the official implementation of Interpretable and Generalizable Diffusion Planning via Vision-Language Guidance and Agent-Aware Trajectory Initialization.The code will be released upon acceptance.

## 📣 Overview

We propose a vision-language guided diffusion planning framework for autonomous driving, integrating:

- **High-level semantic driving instructions** extracted using a Vision-Language Model (Qwen2.5-VL)
- **Agent-aware spatial distribution cues** projected onto a BEV map
- **Dynamic trajectory initialization** for more structured, adaptive diffusion sampling
- **Conditional diffusion decoding** that improves interpretability, rationality, and intent alignment

Our framework significantly enhances **generalizability**, **safety**, **interpretability**, and **trajectory consistency** across complex driving scenarios.


## 🏛️ Framework Overview

<p align="center">
  <img src="assets/main.png" width="900">
</p>

**Figure:** Overview of our language-guided diffusion planner.  
The architecture fuses multi-modal perception (RGB, LiDAR), vehicle state, learned semantic cues, and agent-aware priors to guide diffusion-based trajectory generation.

## 🚗 Qualitative Results

### 1. Comparison with Baselines

<p align="center">
  <img src="assets/compare.png" width="900">
</p>
**Figure:** Comparison with representative baseline planners.  
Our method produces more consistent, scene-aware, and drivable trajectories (red = prediction, green = ground truth).

### 2. Vision-Language Guidance (Ablation Example)

<p align="center">
  <img src="assets/vlm.png" width="700">
</p>

**Figure:** Examples illustrating the effect of VLM semantic priors (e.g., “turn left”, “follow the lane”, “slow down”).  
Semantic cues enforce stronger intent consistency and reduce ambiguous planning behaviors.

### 3. Interaction-Aware Conflict Handling (DIFM)

<p align="center">
  <img src="assets/ablation.png" width="700">
</p>

**Figure:** Our DIFM module resolves conflicts between semantic direction (`f_dir`) and interaction fields (`f_interact`), improving safety around dynamic agents.

## 📊 Quantitative Summary

<p align="center">
  <img src="assets/table.png" width="700">
</p>
Quantitative comparison of our method against representative baselines on the Nav-test benchmark. Our method achieves state-of-the-art performance across key metrics, demonstrating superior planning quality, safety, and task completion efficiency.




# 🔒 Code Availability

The implementation is not yet publicly available as it is still in the submission process. 
The code will be released once the paper is accepted.
