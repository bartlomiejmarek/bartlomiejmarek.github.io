---
title: Spellchecker Impact on Typing-Error Biometrics
summary: Automatic spellcheckers silently erase the very signal that typing-error biometric systems rely on. We benchmarked how bad the damage is — and what it means for system design.
tags:
  - Biometrics
date: "2024-07-08"
---

## The Problem

Typing-error biometric systems (see the [Behavioural Biometric System](/project/behavioural-system/) project) rely on recording the characteristic mistakes a user makes while typing. But modern operating systems and applications apply **automatic spellcorrection** before the keystrokes ever reach the application layer. This silently erases part — or all — of the biometric signal before it can be captured.

How much damage do spellcheckers actually do? And which checkers are most harmful? This project answers both questions.

## Methodology

We built a controlled benchmark using **context-free grammar sentences** that allow programmatic manipulation of the text. We generated two classes of typos:

- **QWERTY-proximity typos** — swaps between physically adjacent keys, reflecting genuine motor-error patterns.
- **Random typos** — uniformly sampled substitutions, serving as a noise baseline.

We then ran each sentence through a suite of popular Python spellcheckers — including `pyspellchecker`, `autocorrect`, `textblob`, `jamspell`, and others — and measured how many biometrically informative errors each checker removed versus preserved.

## Key Findings

- Aggressive context-aware checkers removed the vast majority of QWERTY-proximity errors, the most biometrically valuable class.
- Simple dictionary-based checkers were far less destructive and preserved more of the signal.
- Random typos were more resistant to correction, but they carry less individual-specific information.

## Implications for System Design

Any real-world deployment of typing-error biometrics must either (a) operate at the raw keylogger level, below the spellchecker, or (b) account for spellchecker interference in feature extraction. Ignoring this can lead to false confidence in laboratory results that do not transfer to production.

## Related Publication

The full benchmark is described in [*Spellchecker Analysis for Behavioural Biometric of Typing Errors Scenario*](/publications/spellcheckers/) (SECRYPT 2024).
