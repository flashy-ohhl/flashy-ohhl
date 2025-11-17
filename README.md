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

<!-- <p align="center">
  <img src="assets/table.png" width="700">
</p> -->
| Method | Input | Img. Backbone | NC ↑ | DAC ↑ | TTC ↑ | Comf. ↑ | EP ↑ | PDMS ↑ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| UniAD | Camera | ResNet-34 | 97.8 | 91.9 | 92.9 | 100 | 78.8 | 83.4 |
| LTF | Camera | ResNet-34 | 97.4 | 92.8 | 92.4 | 100 | 79.0 | 83.8 |
| PARA-Drive | Camera | ResNet-34 | 97.9 | 92.4 | 93.0 | 99.8 | 79.3 | 84.0 |
| VADv2 | Camera & Lidar | ResNet-34 | 97.2 | 89.1 | 91.6 | 100 | 76.0 | 80.9 |
| Transfuser | Camera & Lidar | ResNet-34 | 97.7 | 92.8 | 92.8 | 100 | 79.2 | 84.0 |
| DRAMA | Camera & Lidar | ResNet-34 | 98.0 | 93.1 | 94.8 | 100 | 80.1 | 85.5 |
| Hydra-NeXt | Camera & Lidar | ResNet-34 | 98.1 | 97.7 | 94.6 | 100 | 81.8 | 88.6 |
| Hydra-MDP | Camera & Lidar | ResNet-34 | 98.3 | 96.0 | 94.6 | 100 | 78.7 | 86.5 |
| DiffusionDrive | Camera & Lidar | ResNet-34 | 98.2 | 96.2 | 94.7 | 100 | 82.2 | 88.1 |
| GoalFlow | Camera & Lidar | ResNet-34 | 98.4 | 98.3 | 94.6 | 100 | 85.0 | 90.3 |
| Ours | Camera & Lidar | ResNet-34 | 99.3 | 96.4 | 96.5 | 100 | 84.5 | 90.4 |

Quantitative comparison of our method against representative baselines on the Nav-test benchmark. Our method achieves state-of-the-art performance across key metrics, demonstrating superior planning quality, safety, and task completion efficiency.

## 📬 Contact

If you have any questions or need additional materials:

**Email:** zjj@cumt.edu.cn


# 🔒 Code Availability

The implementation is not yet publicly available as it is still in the submission process. 
The code will be released once the paper is accepted.
