---
title: Fonctions et opérations
linktitle: Fonctions et opérations
toc: true
type: book
date: "2019-11-03T00:00:00+01:00"
draft: false

weight: 2

gallery_item:
- album: gallery
  image: /mathdisc/fonctions/diag1.svg
  caption: chemin correspondant à la bijection $f(x,y)$
- album: gallery
  image: /mathdisc/fonctions/diag2.svg
- album: gallery
  image: /mathdisc/fonctions/diag3.svg
- album: gallery
  image: /mathdisc/fonctions/diag4.svg
---

## Exercice 3

  Si $n<m$, il n'existe pas d'injection d'un ensemble à $m$ éléments dans un ensemble à $n$ éléments. Une formulation plus imagée de ce résultat est le _principe des tiroirs_ (ou encore __pigeon-hole principle_), à savoir: si ${n<m}$ et que l'on veut placer $m$ chemises dans $n$ tiroirs alors un tiroir au moins
  contiendra plusieurs chemises. Plus précisément, montrer qu'un tiroir contiendra au moins un nom\-bre entier $p\ge \frac{m}{n}$ chemises.

**Indication :** Soit $A=\\{1,2,\ldots,m\\}$ l'ensemble des chemises à répartir et soit $A\_i$ l'ensemble des chemises contenues dans le tiroir $i$. Notez que $$|A|= \sum\_{i=1}^n|A\_i|$$ et raisonez par contradiction en prennant $|A_i|< \frac{m}{n}$.

## Exercice 4

On dit qu'un ensemble $E$ est _dénombrable_ s'il existe une bijection entre cet ensemble et $\mathbb{N}$. Montrer que $\mathbb{N}^2 = \mathbb{N} \times \mathbb{N}$ est dénombrable. On pourra montrer que les fonctions $f$ et $g$ suivantes sont des bijections de $\mathbb{N}^2$ dans $\mathbb{N}$ : $f(x,y) = y+(0+1+ 2+\cdots+(x+y))$ et $g(x,y)=2^y(2x+1)-1$.

**Solution :** Le premier dessin représente le chemin correspondant à la bijection $f(x,y) = y + (0 + 1 + 2 + \cdots + (x + y))$, les trois autres représentent des autres chemins possibles.

{{< gallery >}}

Une autre façon de montrer cette bijection consiste à utiliser la _« moitié »_ de N pour numéroter $\mathbb{N} \times \\{0\\}$, puis la _« moitié »_ de ce qui reste pour numéroter $\mathbb{N} \times \\{1\\}$, puis la _« moitié »_ de ce qui reste pour numéroter $\mathbb{N} \times \\{2\\}$, etc (bijection $g$).

$\mathbb{N} = \\{0, 1, 2, 3, \ldots\\}$, on compte de 2 en 2 pour numéroter $\mathbb{N} \times \\{0\\}$. 

Il reste :

$\mathbb{N}_1 = \\{1,3,5,7,\ldots\\}$, on compte de 2 en 2 pour numéroter $\mathbb{N}\times\\{1\\}$. 

Il reste :

$\mathbb{N}_2 =\\{3,7,11,15,\ldots\\}$, on compte de 2 en 2 pour numéroter $\mathbb{N}\times\\{2\\}$. 

Il reste :

$\mathbb{N}_3 = \\{7,15,23,31,\ldots\\}$, etc.

{{< figure library="true" src="/mathdisc/fonctions/diag5.svg" lightbox="true" >}}

Pour prouver plus formellement que $f$ est une bijection, considérons la suite définie par $u_p = 1 + \cdots + p$ pour $p \le 1$, et $u_0 = 0$. Par définition cette suite est strictement croissante. Ainsi, pour tout entier $n$, il existe un unique entier $p$ tel que $u_p \le n < u_p+1$. Le couple $(x, y)$ antécédent de $n$ par $f$ est alors défini par : $y = n − u_p$ et $x = p − y$.
