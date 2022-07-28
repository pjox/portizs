---
title: "BERTrade: Using Contextual Embeddings to Parse Old French"
authors:
- Loïc Grobol
- Mathilde Regnault
- admin
- Benoît Sagot
- Laurent Romary
- Benoît Crabbé
date: "2022-06-21T22:12:59Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In The 13th Language Resources and Evaluation Conference
publication_short: In LREC 2022

abstract: "The successes of contextual word embeddings learned by training large-scale language models, while remarkable, have mostly occurred for languages where significant amounts of raw texts are available and where annotated data in downstream tasks have a relatively regular spelling. Conversely, it is not yet completely clear if these models are also well suited for lesser-resourced and more irregular languages. We study the case of Old French, which is in the interesting position of having relatively limited amount of available raw text, but enough annotated resources to assess the relevance of contextual word embedding models for downstream NLP tasks. In particular, we use POS-tagging and dependency parsing to evaluate the quality of such models in a large array of configurations, including models trained from scratch from small amounts of raw text and models pre-trained on other languages but fine-tuned on Medieval French data."

# Summary. An optional shortened abstract.
summary: We consider several neural language models, some of which trained or fine-tuned on a new corpus of raw Old and Middle French texts, and use their internal representations of words as inputs to train taggers and parsers on the SRCMF treebank.

tags:
featured: true

links:
# - name: ACL Anthology
#   url: https://www.aclweb.org/anthology/2020.acl-main.156/
# - name: ACL 2020
#   url: https://acl2020.org/
- name: HAL
  url: https://hal.archives-ouvertes.fr/hal-03736840
# - name: arXiv
#   url: https://arxiv.org/abs/2202.09452
url_pdf: http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.119.pdf
url_code: 'https://zenodo.org/record/6461220'
#url_dataset: 'https://oscar-corpus.com'
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

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides:
---
