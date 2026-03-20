---
title: "Benchmarking Empirical Privacy Protection for Adaptations of Large Language Models"
authors:
- Bartłomiej Marek
- Lorenzo Rossi
- Vincent Hanke
- Xun Wang
- Michael Backes
- Franziska Boenisch
- Adam Dziedzic

date: "2025-04-23"
doi: ""

publishDate: "2025-04-23"

publication_types: ["paper-conference"]

publication: "The Fourteenth International Conference on Learning Representations (ICLR 2026)"
publication_short: "ICLR 2026"

abstract: "Recent work has applied differential privacy (DP) to adapt large language models (LLMs) for sensitive applications, offering theoretical guarantees. However, its practical effectiveness remains unclear, partly due to LLM pretraining, where overlaps and interdependencies with adaptation data can undermine privacy despite DP efforts. To analyze this issue in practice, we investigate privacy risks under DP adaptations in LLMs using state-of-the-art attacks such as robust membership inference and canary data extraction. We benchmark these risks by systematically varying the adaptation data distribution, from exact overlaps with pretraining data, through in-distribution (IID) cases, to entirely out-of-distribution (OOD) examples. Additionally, we evaluate how different adaptation methods and different privacy regimes impact the vulnerability. Our results show that distribution shifts strongly influence privacy vulnerability: the closer the adaptation data is to the pretraining distribution, the higher the practical privacy risk, even without direct data overlap. We find that parameter-efficient fine-tuning methods, such as LoRA, achieve the highest empirical privacy protection for OOD data."

tags:
- Privacy
- LLM
- Differential Privacy

featured: true

links:
  - name: OpenReview
    url: 'https://openreview.net/forum?id=IoT0PpDILA'
    icon_pack: ai
    icon: open-access

url_pdf: 'https://openreview.net/pdf?id=IoT0PpDILA'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

projects: []
slides: ""
---

{{< callout note >}}
**ICLR 2026 — Oral Presentation** (top ~1.8% of submissions)
{{< /callout >}}
