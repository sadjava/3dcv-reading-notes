# Title: Towards Robust Monocular Depth Estimation: Mixing Datasets for Zero-shot Cross-dataset Transfer
## Author: Ren´e Ranftl (2020)
## Article: [arxiv](https://arxiv.org/pdf/1907.01341.pdf)
## Task: Depth Estimation 
___

### General Content
Mixing data from various datasets greately impoves monocular depth estimation. To demonstrate generalization power authors use zero-shot cross-dataset transfer, i.e. evaluation on datasets that were not seen during training.

### Keypoints
* Shift and scale invariant losses
* Comparison between combinations of losses
* Comparison between encoders

### Notes 
* Shift and scale invariant (ssi) losses: ssimse; ssimae; ssitrim, which trims 20% of largest residuals.Reasoning for trimming is that outliers in the ground truth should never influence training. Shift estimation is median depth. Scale estimation is mean shifted back depth. Aligned depths were used for loss i.e. depth without shift over scale.
* Scale invariant loss (si): silog, which uses inverse depths.

### Results
* SOTA results at the time.
* Tools that enable mixing multiple datasets during training, even if their annotations are incompatible.
* Freely available models at [github](https://github.com/intel-isl/MiDaS).