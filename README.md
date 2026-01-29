# Embedding-Driven Multimodal Siamese Framework for Robust False Alarm Detection in Critical Care Monitoring

## Abstract

False arrhythmia alarms in Intensive Care Units (ICUs) can reach false alarm rates as high as 88.8%, contributing to alarm fatigue and delayed clinical responses. Despite recent progress with deep learning, robust false-alarm suppression remains challenging in noisy, heterogeneous multimodal recordings and under strong class imbalance.

This work proposes a **lightweight embedding-driven multimodal Siamese framework** that validates arrhythmia alarms by jointly modeling:

1. Raw multichannel physiological waveforms,
2. Arrhythmia-type metadata, and
3. A rule-based model output as structured prior knowledge.

The architecture employs **multi-scale convolutional encoders** in a Siamese configuration to learn discriminative representations from paired alarm and reference segments, together with a **task-specific distance-based constraint** designed to improve class separability under severe imbalance. To further enhance robustness, the pipeline incorporates extensive signal preprocessing and a **temporal window-shifting data augmentation strategy**.

Experiments were conducted on the **PhysioNet / Computing in Cardiology Challenge 2015** dataset using **stratified five-fold cross-validation** and evaluated with both the official Challenge metric and standard classification measures. The proposed method achieves a **Challenge score of 0.8498 ± 0.0686** and an **F1-score of 0.9101 ± 0.0406**, outperforming replicated state-of-the-art baselines while using substantially fewer trainable parameters (**878,925 vs. 3.28M**).

Ablation studies demonstrate that the combination of **data augmentation**, **arrhythmia embeddings**, and **rule-based priors** yields complementary performance gains, highlighting the benefit of integrating multimodal representation learning with explicit domain knowledge. These results indicate that the proposed framework is a **computationally efficient and practically deployable solution** for real-time false alarm reduction in ICU monitoring, and a promising direction for clinically informed multimodal AI at the bedside.

---

## Supplementary Materials

The supplementary materials associated with this work are provided as a PDF file available **within this repository**.

📄 **Supplementary Materials (PDF):**

* [Supplementary Material PDF](https://github.com/rodriguezhh/icu-false-alarm-reduction/blob/main/Supplementary_Material/supplementary_material.pdf)

> The supplementary document contains additional architectural details, experimental configurations, and extended results that complement the main manuscript.
