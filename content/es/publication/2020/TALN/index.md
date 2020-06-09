---
title: "Les modèles de langue contextuels Camembert pour le Français : impact de la taille et de l'hétérogénéité des données d'entrainement"
authors:
- Louis Martin 
- Benjamin Muller
- admin
- Yoann Dupont
- Laurent Romary
- Éric de la Clergerie
- Benoît Sagot
- Djamé Seddah
author_notes:
- "Contribución a partes iguales"
- "Contribución a partes iguales"
- "Contribución a partes iguales"
date: "2020-06-08T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *La 27e conférence sur le Traitement Automatique des Langues Naturelles*
publication_short: In *TALN 2020*

abstract: Contextual word embeddings have become ubiquitous in Natural Language Processing. Until recently, most available models were trained on English data or on the concatanation of corpora in multiple languages. This made the practical use of models in all languages except English very limited. The recent release of monolingual versions of BERT (Devlin et al., 2019) for French established a new state-of-the-art for all evaluated tasks. In this paper, based on experiments on CamemBERT (Martin et al., 2019), we show that pretraining such models on highly variable datasets leads to better downstream performance compared to models trained on more uniform data. Moreover, we show that a relatively small amount of web crawled data (4GB) leads to downstream performances as good as a model pretrained on a corpus two orders of magnitude larger (138GB).

# Summary. An optional shortened abstract.
summary: We explore the impact of the training data size and heterogeneity on French language modeling.

tags:
featured: false
links:
- name: TALN 2020
  url: https://jep-taln2020.loria.fr/
- name: HAL
  url: https://hal.archives-ouvertes.fr/hal-02784755
- name: Website
  url: https://camembert-model.fr/
url_pdf: https://jep-taln2020.loria.fr/wp-content/uploads/JEP-TALN-RECITAL-2020_paper_151.pdf
#url_code: 'https://github.com/pjox/goclassy'
url_dataset: 'https://oscar-corpus.com'
#url_poster: '#'
#url_project: ''
#url_slides: '/files/CMLC_7_slides.pdf'
#url_source: '#'
#url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
#image:
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#  focal_point: ""
#  preview_only: false

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
