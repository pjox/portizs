---
title: Induction sur $\mathbb{N}$
linktitle: Induction sur $\mathbb{N}$
toc: true
type: docs
date: "2019-11-03T00:00:00+01:00"
draft: false
menu:
  mathdiscretes2019:
    parent: exercices
    weight: 4

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4

#markup: mmark
---

## Exercice 7

1.  Montrer que pour tout $n\in \mathbb{N}$, $(n+1)^2-(n+2)^2-(n+3)^2+(n+4)^2=4$.

    **Indication :** Developpez l'expresion :-)

2.  En déduire que tout entier $m$ peut s'écrire comme somme et différence des carrés $1^2, 2^2,\ldots , n^2$ pour un certain $n$, c'est-à-dire que pour tout $m$ :

    $P(m)$ : il existe $n\in \mathbb{N}$, et $\varepsilon _1,\ldots, \varepsilon _n\in \{-1,1\}$, tels que $m=\varepsilon\_{1}1^2+\varepsilon\_{2}2^2+\cdots +\varepsilon\_{n}n^2$.

    **Indication :** Écrivez $0,1,2,3$ comme somme et différence des carrés, puis montrez que $P(m)$ implique $P(m+4)$ en utilisant 1.

## Exercice 8

1.  On suppose qu'une propriété $P$ définie sur $\mathbb{N}$ vérifie :

    (i) $P(1)$ est vraie.

    (ii) Si $P(n)$ est vraie alors $P(2n)$ est vraie (pour $n \geq 1$).

    (iii) Si $P(n)$ est vraie alors $P(n - 1)$ est vraie (pour $n \geq 2$).
    
    Montrer par récurrence sur $n$ que $P(n)$ est vraie pour tout $n \geq 1$.

    **Solution :** _Base :_ $P(1)$ vraie (par (i))

    _Induction :_ Supposons $P(n)$ vraie pour un entier $n \geq 1$, alors par (ii) $P(2n)$ vraie et par (iii) $P(2n - 1), \ldots, P (n + 1)$ vraies, car $2n, 2n-1, \ldots, n+1$ sont supérieurs ou égaux à $2$. Donc $P(n)$ implique $P(n + 1)$ pour $n \geq 1$ et on obtient le résultat.

2.  On veut montrer que la moyenne arithmétique est supérieure à la moyenne géométrique. 

    Soient $a\_1, \dots, a\_n$ $n$ nombres réels positifs, avec $n \geq 1$ ; on pose $A = (a\_1 + \ldots + a\_n)/n$ et $G = (a\_1 \cdots a\_n )^{1/n}$ , montrer que $A \geq G$.

    **Indication :** Par induction sur $n$ on montre $P(n)$ vraie pour tout $n$, où : $$P(n): \text{ pour tout } n \text{-uplet } a\_1,\dots,a\_n>0, \ A\geq G$$

    _Base :_ ($n = 1$, et $A = G$ inutile pour le raisonnement) $n = 2$ et $(a\_1 + a\_2)/2 \geq \sqrt{a_1 a_2}$ en effet $(\sqrt{a\_1}-\sqrt{a\_2})^2=a\_1+a\_2-2\sqrt{a\_1 a\_2}\geq 0$.

    _Induction :_ Montrer $P (n) \Longrightarrow P (n - 1)$ et $P (n) \Longrightarrow P (2n)$ pour tout $n \geq 2$, d'où le résultat.

    *   $P (n) \Longrightarrow P (2n)$ : Prenez $(a\_1+\ldots+a\_n+a\_{n+1}+\ldots+a\_{2n})/2n$, appliquez l'hypothèse de récurrence deux fois et utilisez $P(2)$.
  
    *   $P (n) \Longrightarrow P (n - 1)$ : Pour montrer $P(n-1)$ pour $a\_1,\ldots, a\_{n-1}$ donnés, on choisit d'ajouter $a\_n=(a\_1+\cdots+a\_{n-1})/(n-1)$ et on va utiliser $P(n)$ sur le $n$-uplet ainsi formé.
       
        On a $$A\_{n-1}=\frac{(a\_1+\dots+a\_{n-1})}{(n-1)}=a\_n$$

        et $$\begin{align}
        A\_n&=\frac{(a\_1+\dots+a\_{n-1})+\frac{(a\_1+\dots+a\_{n-1})}{(n-1)}}{n}\\\\\
        &=\frac{(n-1)(a\_1+\dots+a\_{n-1})+(a\_1+\dots+a\_{n-1})}{n(n-1)}\\\\\
        &=\frac{(a\_1+\dots+a\_{n-1})}{(n-1)}=a\_n
        \end{align}$$

        d'où $A=(a\_1+\dots+a\_n)/n=(a\_1+\dots+a\_{n-1})/(n-1)=a\_n$. Montrez que $P (n) \Longrightarrow P (n - 1)$.