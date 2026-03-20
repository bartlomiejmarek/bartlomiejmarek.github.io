---
title: Multilingual Audio DeepFake Detection
summary: Can state-of-the-art audio deepfake detectors generalise beyond English? A benchmark across 8 languages reveals significant gaps — and a path forward.
tags:
  - DF
  - ML
date: "2024-12-23"
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/bartlomiejmarek/are_audio_df_polyglots
  - icon: file-pdf
    icon_pack: fas
    name: Paper
    url: https://arxiv.org/abs/2412.17924
---

## Motivation

The overwhelming majority of audio deepfake (DF) detection research is built on English-language datasets such as ASVspoof. Yet synthetic speech technology is language-agnostic — TTS and voice-conversion systems produce convincing fakes in any language. This raises an uncomfortable question: **are our best detectors actually polyglots, or are they just good at English?**

This project — which forms the core of my Master's thesis — set out to answer that question systematically.

## What We Did

We evaluated a range of state-of-the-art DF detection models on speech spanning **8 languages**: English, German, Polish, Ukrainian, Russian, Spanish, French, and Italian. For each language we studied three settings:

1. **Zero-shot** — model trained only on English, evaluated on a target language.
2. **Intra-linguistic adaptation** — model fine-tuned and evaluated within the same non-English language.
3. **Cross-linguistic adaptation** — model fine-tuned on one language and evaluated on another.

We also analysed which acoustic features survive the language shift and which become noise.

## Key Findings

- Zero-shot transfer degrades sharply for most languages, with equal-error rates sometimes tripling compared to English performance.
- Intra-linguistic fine-tuning recovers much of the performance, confirming that **target-language data is the most important factor**.
- Cross-linguistic transfer is inconsistent: languages with shared phonology can partially share knowledge, but there is no reliable free lunch.
- Models that encode language-agnostic artefacts of neural vocoders are more robust; models that latch onto language-specific prosody are brittle.

## Takeaways for Practitioners

If you are deploying audio deepfake detection in a non-English environment, you should not assume English-trained baselines will protect you. Collecting even a small amount of target-language data for adaptation can make a decisive difference.

## Related Publication

The research is described in detail in [*Are Audio DeepFake Detection Models Polyglots?*](/publications/audio-deepfakes-polyglots/) (arXiv 2024).
