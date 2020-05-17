---
title: "CamemBERT: a Tasty French Language Model"
authors:
- Louis Martin
- Benjamin Muller
- admin
- Yoann Dupont
- Laurent Romary
- Éric de la Clergerie
- Djamé Seddah
- Benoît Sagot
date: "2020-07-06T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *The 58th Annual Meeting of the Association for Computational Linguistics*
publication_short: In *ACL 2020*

abstract: Pretrained language models are now ubiquitous in Natural Language Processing. Despite their success, most available models have either been trained on English data or on the concatenation of data in multiple languages. This makes practical use of such models---in all languages except English---very limited. In this paper, we investigate the feasibility of training monolingual Transformer-based language models for other languages, taking French as an example and evaluating our language models on part-of-speech tagging, dependency parsing, named entity recognition and natural language inference tasks. We show that the use of web crawled data is preferable to the use of Wikipedia data. More surprisingly, we show that a relatively small web crawled dataset (4GB) leads to results that are as good as those obtained using larger datasets (130+GB). Our best performing model CamemBERT reaches or improves the state of the art in all four downstream tasks.

# Summary. An optional shortened abstract.
summary: We explore the impact of the training data size on a French version of RoBERTa. (Equal contribution by the first three authors).

tags:
featured: true
links:
- name: arXiv
  url: https://arxiv.org/abs/1911.03894/
- name: Website
  url: https://camembert-model.fr/
- name: ACL 2020
  url: https://acl2020.org/
- name: HAL
  url: https://hal.inria.fr/hal-02445946
#url_pdf: https://ids-pub.bsz-bw.de/frontdoor/deliver/index/docId/9021/file/Suarez_Sagot_Romary_Asynchronous_Pipeline_for_Processing_Huge_Corpora_2019.pdf
#url_code: 'https://github.com/pjox/goclassy'
url_dataset: 'https://oscar-corpus.com'
#url_poster: '#'
#url_project: ''
#url_slides: '/files/CMLC_7_slides.pdf'
#url_source: '#'
#url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
 caption: 'Image credit: [**Alix Chagué**](https://alix-tz.github.io/en/index.html)'
 focal_point: ""
 preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- CamemBERT

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides:
---

Equal contribution by the first three authors, order of names assigned alphabetically.
