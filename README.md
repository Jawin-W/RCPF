# Beyond Whole-Image Forensics

## Generalizable AI-Generated Image Detection via Sampled Patch Ranking and Fusion

This project presents **Reconstruction-Ranked Complementary Patch Fusion (RCPF)**, a local-input forensic framework for generalizable AI-generated image detection. Instead of extracting features from an entire image, RCPF makes image-level predictions from a small set of sampled local patches.

## Framework

The model framework figure is available as a PDF:

[Download the RCPF framework figure](figure2.pdf)

## Main Results

Mean performance on the OpenSDI and AIGIBench benchmarks is summarized below. Values are reported in percentage points.

| Method | OpenSDI Acc. | OpenSDI F1 | AIGIBench Acc. | AIGIBench A.P. |
|---|---:|---:|---:|---:|
| CNNDet | 70.87 | 61.57 | 56.8 | 65.4 |
| UnivFD | 75.72 | 72.20 | 57.6 | 60.3 |
| FreqNet | 66.31 | 56.39 | 55.7 | 60.2 |
| NPR | 76.45 | 74.85 | 57.2 | 65.3 |
| SPAI | 76.77 | 72.89 | 52.2 | 54.3 |
| FreqDINO | 90.40 | 89.13 | 59.1 | 66.6 |
| DFFreq | 84.93 | 83.99 | 77.9 | 82.0 |
| FALCON-Net | 79.88 | 77.43 | 64.3 | 65.0 |
| **RCPF (Ours)** | **92.87** | **92.65** | **79.7** | **83.7** |

RCPF achieves the best mean performance on both benchmarks, with particularly strong gains on OpenSDI and competitive generalization across the diverse AIGIBench sources.

## Random-Sampling Ablation

We evaluate 100 random seeds (10–1000, step 10) for patch sampling with default settings. As shown in [Figure 3](figure3.pdf), the spans of mean Acc. and mean A.P. are 0.23% and 0.28% on AIGIBench, while those of mean Acc. and mean F1 are 0.29% and 0.33% on OpenSDI, respectively, indicating negligible variation from random sampling.

[View Figure 3: Random-sampling ablation results (PDF)](figure3.pdf)
