# DATDT: Decoupled Appearance-Trajectory Deep Tracking

> **Note**: This paper is currently under review at IEEE TCSVT. Code and models will be released upon acceptance.

## Overview

DATDT is a visual object tracking method that decouples appearance and trajectory processing to avoid trajectory guidance dilution in existing fusion-based approaches. Built upon HIPTrack, we introduce several improvements including explicit trajectory prediction, adaptive template updates, and target-aware cropping strategies.

## Key Ideas

- **Decoupled Design**: Process appearance and trajectory in separate pathways instead of early feature fusion
- **Trajectory Prediction**: Lightweight MLP-based motion forecasting (13K parameters)  
- **Adaptive Template Update**: Quality assessment before template updates
- **Target-aware Cropping**: Dynamic scale adjustment for fast motion scenarios


### Main Results
![sota_comparison1](assets/sota_comparison1.png)
![sota_comparison2](assets/sota_comparison2.png)

### Raw Results

```
raw_result/
├── ablation_study_1/          # Component ablation (baseline→full model)
├── ablation_study_2/          # Template update parameters
├── ablation_study_3/          # Trajectory window size analysis  
├── lasot/                     # LaSOT results
├── nfs/                       # NFS30 results
├── otb/                       # OTB2015 results
├── trackingnet/               # TrackingNet results
└── uav/                       # UAV123 results
```

**Verification**: All results can be directly evaluated using official toolkits. Each folder contains both raw tracking files and evaluation scripts.

### Visualization Results

We also provide visualization files showing tracking performance across different scenarios. Sample visualizations are available in the result folders (e.g., `got10k_submit.zip`, `visualization.zip`).

## Architecture

![Framework](assets/framework.png)

The key difference from existing methods is separating trajectory and appearance processing until the final scoring stage, which preserves trajectory guidance effectiveness.

## Current Status

- [x] Paper submitted to IEEE TCSVT
- [x] Raw evaluation results available
- [ ] Code organization in progress
- [ ] Models will be released upon acceptance


## Contact
- Zeqi Li: [GitHub](https://github.com/lizeqi1024)


## Citation
We hope the decoupled design perspective and thorough experimental analysis provide useful insights for the tracking community. If you find our work helpful for your research, please consider citing when the paper is accepted.

