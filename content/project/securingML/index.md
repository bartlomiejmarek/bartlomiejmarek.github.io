---
title: Defending ML-based Android Malware Detectors Against Backdoor Attacks
summary: Machine learning powers modern Android malware detection — but it is vulnerable to backdoor attacks. We propose a feature-selection defence that reduces this risk without sacrificing accuracy.
tags:
  - ML
  - AI
date: "2024-07-01"
---

## Background

Machine learning has become the engine of modern Android malware detection. Classifiers trained on app features — API calls, permissions, network behaviour — can identify malicious apps with high accuracy. But ML models are not immune to adversarial manipulation.

A **backdoor attack** embeds a hidden trigger in the training data. At inference time, apps that carry this trigger are silently misclassified as benign. In a real deployment this could allow an entire malware family to slip past the detector as long as the adversary controls a few poisoned samples in the training pipeline.

## Our Approach

Working in collaboration with **NASK (National Research Institute)**, we studied backdoor attacks against Android malware detectors in both **classic** (centralised) and **federated learning** scenarios. We then proposed a defensive feature selection method that:

1. Identifies and removes features that are statistically associated with the trigger signal.
2. Reduces the attack surface the adversary can exploit, without requiring knowledge of which specific attack strategy was used.
3. Maintains detection accuracy on clean samples.

We evaluated the defence against multiple attack variants — including stronger, more realistic federated-learning attacks — and found that it consistently reduces backdoor success rates with minimal impact on clean accuracy.

## Why It Matters

As federated learning is increasingly adopted to train models collaboratively across device fleets, the risk of poisoning attacks grows. A practical, data-agnostic defence is therefore an important building block for trustworthy ML security systems.

## Related Publication

Full details are available in [*Securing ML-based Android Malware Detectors: A Defensive Feature Selection Approach against Backdoor Attacks*](/publications/securingml/) (CCGridW 2024, IEEE/ACM).
