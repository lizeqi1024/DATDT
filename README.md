# DATDT: Decoupled Appearance-Trajectory Deep Tracking

> **Note**: This paper is currently under review at IEEE TCSVT. Code and models will be released upon acceptance.

## Overview

DATDT is a visual object tracking method that decouples appearance and trajectory processing to address the trajectory guidance dilution issue. 

## Key Ideas

- **Decoupled Design**: Process appearance and trajectory in separate pathways instead of early feature fusion
- **Trajectory Prediction**: Lightweight MLP-based motion forecasting (13K parameters)  
- **Adaptive Template Update**: Quality assessment before template updates
- **Target-aware Cropping**: Dynamic scale adjustment for fast motion scenarios


### Main Results
We achieve  79.9% AO on GOT-10k and 71.0% AUC on NFS30, and maintain real-time performance at 55.5 FPS on a single RTX 4070Ti SUPER GPU. 

![sota_comparison1](assets/sota_comparison1.png)

![sota_comparison2](assets/sota_comparison2.png)


### Raw Results

📁 Download Links:

Baidu Netdisk: https://pan.baidu.com/s/1T_NzprtueI0GsJx0DRB5QQ Code: i4nu

Got-10k visualizations are available in the result folders (e.g., `got10k_submit.zip`, `visualization.zip`).

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

