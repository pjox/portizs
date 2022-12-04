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
- "Contribué à parts égales"
- "Contribué à parts égales"
- "Contribué à parts égales"
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

abstract: Les modèles de langue neuronaux contextuels sont désormais omniprésents en traitement automatique des langues. Jusqu’à récemment, la plupart des modèles disponibles ont été entraînés soit sur des données en anglais, soit sur la concaténation de données dans plusieurs langues. L’utilisation pratique de ces modèles — dans toutes les langues sauf l’anglais — était donc limitée. La sortie récente de plusieurs modèles monolingues fondés sur BERT (Devlin et al., 2019), notamment pour le français, a démontré l’intérêt de ces modèles en améliorant l’état de l’art pour toutes les tâches évaluées. Dans cet article, à partir d’expériences menées sur CamemBERT (Martin et al., 2019), nous montrons que l’utilisation de données à haute variabilité est préférable à des données plus uniformes. De façon plus surprenante, nous montrons que l’utilisation d’un ensemble relativement petit de données issues du web (4Go) donne des résultats aussi bons que ceux obtenus à partir d’ensembles de données plus grands de deux ordres de grandeurs (138Go).

# Summary. An optional shortened abstract.
summary: Nous explorons l'impact de la taille et de l'hétérogénéité des données d'entraînement sur la modélisation de la langue française.

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
