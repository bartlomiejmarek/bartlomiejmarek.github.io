---
title: "Natural Identifiers for Privacy and Data Audits in Large Language Models"
authors:
- Lorenzo Rossi
- Bartłomiej Marek
- Franziska Boenisch
- Adam Dziedzic

date: "2026-04-01"
doi: ""

publishDate: "2026-04-01"

publication_types: ["paper-conference"]

publication: "The Fourteenth International Conference on Learning Representations (ICLR 2026)"
publication_short: "ICLR 2026"

abstract: "Assessing the privacy of large language models (LLMs) presents significant challenges. In particular, most existing methods for auditing differential privacy require the insertion of specially crafted canary data during training, making them impractical for auditing already-trained models without costly retraining. Additionally, dataset inference, which audits whether a suspect dataset was used to train a model, is infeasible without access to a private non-member held-out dataset. Yet, such held-out datasets are often unavailable or difficult to construct for real-world cases since they have to be from the same distribution (IID) as the suspect data. These limitations severely hinder the ability to conduct scalable, post-hoc audits. To enable such audits, this work introduces natural identifiers (NIDs) as a novel solution to the above-mentioned challenges. NIDs are structured random strings, such as cryptographic hashes and shortened URLs, naturally occurring in common LLM training datasets. Their format enables the generation of unlimited additional random strings from the same distribution, which can act as alternative canaries for audits and as same-distribution held-out data for dataset inference."

tags:
- Privacy
- LLM
- Differential Privacy

featured: false

links:
  - name: OpenReview
    url: 'https://openreview.net/forum?id=doaAUf9Pi7'
    icon_pack: ai
    icon: open-access

url_pdf: 'https://openreview.net/pdf?id=doaAUf9Pi7'
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
