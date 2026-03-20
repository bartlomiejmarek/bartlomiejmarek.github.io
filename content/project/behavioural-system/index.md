---
title: Behavioural Biometric System Based on Typing Errors
summary: People make characteristic mistakes when they type. Can those mistakes serve as a biometric signature for authentication? This project built — and rigorously evaluated — a system that answers yes.
tags:
  - ML
  - NLP
  - Biometrics
date: "2023-02-01"
---

## The Idea

Typing-error biometrics is a relatively unexplored niche within behavioural biometrics. The intuition is straightforward: the kinds of mistakes a person makes while typing — which keys they swap, which sequences trip them up — are influenced by motor memory, habits, and native language. These patterns are consistent across sessions and differ between individuals.

This project — my Bachelor's thesis — set out to build a complete **user verification and identification system** that captures those patterns, extracts them as features, and uses them to authenticate users.

## System Design

The system combines a **keylogger** with a lightweight **text editor** to collect raw keystroke and typing-error data during controlled sessions. From the collected text we extract features using:

- **Natural language processing techniques** — edit distance, n-gram error profiles, phonetic similarity measures.
- **Statistical metrics** — error frequency, error type distribution, correction latency.

User profiles are built from these features and authentication decisions are made using several ML classifiers compared head-to-head.

## Results

The system achieved competitive verification and identification performance on our collected dataset, demonstrating that typing errors carry a genuine biometric signal. The project also surfaced interesting failure modes: users who type very carefully (few errors) are harder to profile, and session length significantly affects stability.

## Related Publication

The theoretical basis and a subset of results were published in [*User Authentication and Identification System Based on Behavioural Biometrics of Typing Errors*](/publications/behavioursep/) (SEP 2023).

Follow-up work on the effect of spellcheckers on this signal is described in the [Spellchecker Analysis](/project/spellcheckers-analysis/) project.
