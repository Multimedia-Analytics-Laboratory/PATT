<div align="center">

# Learning to Track from Privileged Target Appearances

**Xin Chen, Jiao Xu, Dong Wang, Huchuan Lu, and Kede Ma**

[[Paper](https://arxiv.org/abs/2609.02471)]

</div>

## Overview

Target templates define what a visual tracker searches for, yet the templates available at inference trade off *localization certainty* with *appearance freshness*: the initial ground-truth template is exact but becomes stale, whereas recent templates better reflect the current appearance but are cropped from uncertain predictions. We quantify this bottleneck with a non-deployable oracle that supplies an exact current-frame target crop, improving AUC on LaSOT by 15.2 percentage points. This gap reveals a training-only opportunity: frame-level ground truths provide exact current- and future-frame target crops, although such crops are unavailable at deployment. We introduce Privileged Appearance Transfer for Tracking (**PATT**), a teacher-student training framework that transfers these privileged appearances to a deployable tracker through multi-level representation prediction. The privileged teacher observes exact target crops from past, current, and future frames, whereas the student receives only past-frame templates and learns to predict the teacher's search representations. To avoid transferring unreliable teacher signals, PATT weights this transfer by the teacher's relative localization advantage over the student and its absolute localization accuracy. After training, the teacher, latent predictor, reliability weights, and privileged crops are removed, leaving standard student-only inference. Across seven benchmarks at two model scales, PATT achieves consistent gains under both long- and short-term tracking protocols.

## Motivation

![Motivation for learning from privileged target appearances](figures/motivation.png)

## Framework

![Overview of the PATT framework](figures/framework.png)

## Code and Models

Code and models will be released soon.
