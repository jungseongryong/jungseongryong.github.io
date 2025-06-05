---
title: "ToDi: Token-wise Distillation via Fine-Grained Divergence Control"
authors:
- admin
- "Suwan Yoon"
- "DongGeon Kim"
- "Hwanhee Lee"
date: "2025-05-22T06:51:16Z"    # arXiv 첫 제출(v1) 날짜 (UTC)
doi: "10.48550/arXiv.2505.16297" # arXiv DOI

# Schedule page publish date (NOT publication's date).
publishDate: "2025-05-22T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""


  Large language models (LLMs) offer impressive performance but are impractical for resource-constrained deployment due to high latency and energy consumption. Knowledge distillation (KD) addresses this by transferring knowledge from a large teacher to a smaller student model. However, conventional KD, notably approaches like Forward KL (FKL) and Reverse KL (RKL), apply uniform divergence loss across the entire vocabulary, neglecting token-level prediction discrepancies.
  
  By investigating these representative divergences via gradient analysis, we reveal that FKL boosts underestimated tokens, while RKL suppresses overestimated ones, showing their complementary roles. Based on this observation, we propose Token-wise Distillation (ToDi), a novel method that adaptively combines FKL and RKL per token using a sigmoid-based weighting function derived from the teacher-student probability log-ratio.
  
  ToDi dynamically emphasizes the appropriate divergence for each token, enabling precise distribution alignment. We demonstrate that ToDi consistently outperforms recent distillation baselines using uniform or less granular strategies across instruction-following benchmarks. Extensive ablation studies and efficiency analysis further validate ToDi’s effectiveness and practicality.

# Summary: 풀 abstract 대신, 짧게 요약된 버전을 적습니다. (원문 초록의 첫 두 문장 정도를 발췌해도 무방합니다.)
summary: "Large language models (LLMs) offer impressive performance but are impractical for resource-constrained deployment. 우리는 토큰 단위로 KL 발산을 제어하는 새로운 지식 증류 방법 ToDi를 제안하여, 기존 방법보다 정교한 분포 정렬을 가능케 한다."


tags:
- "Large Language Models"
- "Knowledge Distillation"
- "Compression"

featured: true

links:
- name: Custom Link
  url: http://example.org
url_pdf: http://arxiv.org/pdf/1512.04133v1
url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
url_dataset: '#'
url_poster: '#'
url_project: ''
url_slides: ''
url_source: '#'
url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

This work is driven by the results in my [previous paper](/publication/conference-paper/) on LLMs.

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
