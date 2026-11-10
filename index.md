---
layout: default
title: DSC 180A Methodology Assignment 4
---

# DSC 180A Methodology Assignment 4

**Name:** Daniel Huang

**Email:** [dah028@ucsd.edu](mailto:dah028@ucsd.edu)

**Section:** D05 Deep learning techniques for understanding and mitigating electric energy costs at home

**Mentor:** Haojian Jin, Michael Deisher (Azimuth AI), Sylvia Downing (Azimuth AI)

---

**What is the most interesting topic covered in your domain this quarter?**

Zero-shot forecasting from simulation alone was the most interesting topic. The SarSim0 paper shows that models trained only on simulated SARIMA data can forecast unseen real datasets, which suggests synthetic data could stand in for the grid measurements that utilities restrict.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to evaluate our detector on real grid data once we have DERConnect access. I would train one model on default SarSim0 data and one on our grid-specific version, then compare precision, recall, AUROC, and false positive rate on labeled electrical anomalies.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would not treat Chronos-2 as the main target, since from-scratch training was compute-limited and did not beat the pretrained model. Instead, I would test smaller architectures such as PatchTST earlier and run a systematic sweep of SarSim0 configurations. I would also fix a concrete definition of “anomaly” at the start.

**What other techniques would you be interested in using in your project?**

I would like to inject synthetic anomalies (for example, voltage sags and PMU dropouts) into evaluation data, using the point-wise versus pattern-wise taxonomy from Lai et al. I would also add simple classical baselines such as autoregression, which did well in the anomaly detection benchmarks we read, and event-based metrics that avoid the inflated scores of point-adjusted F1.
