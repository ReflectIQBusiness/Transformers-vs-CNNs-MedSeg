# 🧠 3D Medical Image Segmentation Benchmark: Transformers vs. CNNs

**A benchmark study evaluating 8 modern 3D medical image segmentation architectures across 4 public datasets using a unified MONAI pipeline.**

> _“Evaluating Attention Mechanisms in Transformers and CNNs: A Hybrid Model Benchmark in Medical Segmentation”_  
> Hasnae Briouya, Asmae Briouya, Ali Choukri, Mohamed Amnai

---

## 📌 Overview

This repository provides reproducible Kaggle notebooks and resources to benchmark and analyze the performance of state-of-the-art CNN and Transformer-based models for medical image segmentation. It evaluates models across **4 datasets** for segmenting **brain tumors, strokes, liver tumors, and hippocampal structures**.

---

## 🧪 Models Benchmarked

- **UNet** – Lightweight CNN with skip connections
- **VNet** – 3D residual CNN
- **AttentionUNet** – UNet with attention gates
- **DynUNet** – Dynamic receptive field CNN
- **SegResNet** – Residual encoder-decoder CNN
- **HighResNet** – High-resolution residual 3D CNN
- **UNETR** – Transformer-based encoder-decoder
- **Swin-UNETR** – Hierarchical Swin Transformer with local-global attention

All models are implemented with [MONAI](https://monai.io/), using the same data pipeline and evaluation metrics.

---

## 🗂 Datasets

| Dataset                 | Anatomy          | Imaging Modality | Task                                |
|-------------------------|------------------|------------------|-------------------------------------|
| **BraTS 2021**          | Brain            | MRI (T1, T2, FLAIR, T1ce) | Glioma segmentation (ET, TC, ED) |
| **ISLES 2022**          | Brain            | MRI (DWI, ADC, FLAIR)     | Stroke lesion segmentation        |
| **LiTS 2017**           | Liver            | CT                     | Liver and tumor segmentation       |
| **Decathlon Task04**    | Hippocampus      | MRI (T1)                | Hippocampal structure segmentation |

> Please download datasets from their official sources. Due to license restrictions, we do not redistribute medical datasets here.

---

## 📈 Evaluation Metrics

The models are evaluated with the following:

- **Dice Score**
- **Hausdorff Distance (95th percentile)**
- **Precision**
- **Recall**
- **F1 Score**
- **Computational Metrics**: GFLOPs, Model Parameters (MB), Training Time (s)


Make sure MONAI and PyTorch are available:
  pip install monai torch torchvision nibabel


