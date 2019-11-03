---
title: Relations d'ordre
linktitle: Relations d'ordre
toc: true
type: docs
date: "2019-11-03T00:00:00+01:00"
draft: false
menu:
  mathdiscretes:
    parent: exercices
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3

#markup: mmark
---

## Exercice 10

Soient $(A, \leq_1)$ et $(B, \leq_2)$ deux ordres bien fondés. Les
ordres suivants sont-ils bien fondés ?

1.  Sur $A \times B$, l'ordre produit $(a, b) \leq (a', b')$ si et
seulement si  $a \leq\_1 a'$ et $b \leq\_2 b'$.

    **Indication :** Prenez $(a\_n, b\_n)$ une suite décroissante de $A \times B$. Notez que si $(a\_n,b\_n)$ est une suite décroissante stricte, $a\_n$ et $b\_n$ sont toutes deux décroissantes mais pourraient être décroissantes au sens large. Montrez qu'on peut extraire de $a\_n$ et $b\_n$ des sous-suites infinies $a\_i$ et $b\_j$ décroissantes strictement. Remarquez que « on ne peut pas extraire de $a\_n$ une sous-suite décroissante stricte » équivaut « $a\_n$ est ultimement stationnaire » et faites un raisonnement par cas.
    
    Pour l'autre direction, prenez $a\_i$ et $b\_j$ décroissantes strictes dans des ordres bien fondés, et montrez que $(a\_n,b\_n)$ est décroissante stricte.

2.  Sur $A \times B$, l'ordre lexicographique.

     **Indication :** Soit $X$ une partie non vide de $A \times B$, montrez qu'elle a un élément minimal. Prenez $X_A = \\{a \mid \exists b (a, b) \in  X\\}$ : comme $A$ est bien fondé, $X\_A$ a un élément minimal $m\_A$. Soit $X\_{m\_A} = \\{b \mid (m\_A, b) \in X\\}$ : comme $B$ est bien fondé $X\_{m\_A}$ a un élément minimal $m\_B$. Vérifiez que $(m\_A, m\_B)$ est minimal dans $X$.

## Exercice 12

Soit $f: \mathbb{N}\times \mathbb{N}\to \mathbb{N}$ définie par :
$$\begin{cases}
f(0,n) = n+1,\\\\\
f(m,0) = f(m-1,1), & \text{ si } m\geq 1\\\\\
f(m,n) = f(m-1, f(m,n-1)), & \text{ si } m, n \geq 1\\\\\
\end{cases}$$

1.  Calculer $f(1,n)$ et $f(2,n)$.

    **Solution :**

    $f(1,n) = f(0,f(1,n-1))=1+f(1,n-1),$ donc (par rec.) $f(1,n) = n+2$ car on s'arrête à $f(1,0)=f(0,1)=2.$

    $f(2,n) = f(1,f(2,n-1))=2+f(2,n-1),$ donc $f(2,n)=2n+3$ car $f(2,0)=f(1,1)=3.$

2.  Montrer que $f(m,n)$ est définie pour tout couple $(m,n)$ $\in \mathbb{N}\times \mathbb{N}.$

    **Indication :** Par induction généralisée sur $\mathbb{N}\times \mathbb{N}$ muni de son ordre lexicographique.

3.  Soit $g: \mathbb{N} \times \mathbb{N} \longrightarrow \mathbb{N}$ définie par : $$\begin{cases}
g(0,n) = n+1,\\\\\
g(m,0) = g(m-1,1), & \text{si } m\geq 1\\\\\
g(m,n) = g(m-1, g(m,n+1)), & \text{si } m, n \geq 1\\\\\
\end{cases}$$
    Pour quels couples $(m, n) \in \mathbb{N} \times \mathbb{N}$ la fonction $g(m, n)$ est-elle définie ?

    **Solution :** Pour tous les couples $(0,n)$, $n \in \mathbb{N}$ et pour $(1,0)$.
