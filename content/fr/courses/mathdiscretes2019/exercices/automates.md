---
title: Langages et automates
linktitle: Langages et automates
toc: true
type: book
date: "2019-11-04T00:00:00+01:00"
draft: false

weight: 6
---

## Exercice 2

Soit $A$ un alphabet contenant la lettre $b$. Soit $X=\\{b\\}$ et $Y=(A\setminus \{b\})\cdot \\{b\\}^\*$.

1.  Décrire informellement les éléments de $X^\*$, $Y$ et $Y^\*$.

    **Solution :** $X^\*$ est l'ensemble des mots (y compris le mot vide) formés uniquement de $b$.

    $Y$ est l'ensemble des mots non vides dont la première lettre n'est pas un $b$ et dont toutes les autres sont des $b$. En effet $u \in Y$ si et seulement si $u=vw$ avec $u \in A\setminus \\{b\\}$ et $ v\in \\{b\\}^\*$.

    $Y^\*$ est l'ensemble formé du mot vide et de tous les mots non vides ne commençant pas par $b$.

2.  Montrer que tout mot de $A^\*$ commençant par une lettre distincte de $b$ appartient à $Y^\*$.

    **Indication :** Soit un mot $u$ de $A^\*$ dont la première lettre n'est pas un $b$. Notez qu'il s'écrit donc $$x\_1b^{p\_1}x\_2b^{p\_2}\cdots b^{p\_{n-1}}x\_nb^{p\_n},$$ avec $x\_i\in A\setminus \\{b\\}$.

3.  Montrer que tout mot $u$ de $A^*$ s'écrit de façon unique sous la forme $u=vw$, où $v\in X^\*$ et $w\in Y^\*$.

    **Indication :** Soit $u$ un mot de $A^\*$. S'il contient au moins une lettre différente de $b$, notez qu'il s'écrit $b^pxu'$ avec $x \neq b$. D'après 1), $b^p \in X^\*$, et d'après 2), $xu' \in Y^\*$. Montrez que la décomposition est unique.

    Si $u$ ne contient que des $b$, alors il appartient à $X^\*$, et comme $\varepsilon \in Y^\*$, $u \in X^\*\cdot Y^\*$. Montrez que la décomposition est unique.
