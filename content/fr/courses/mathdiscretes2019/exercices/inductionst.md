---
title: Induction structurelle
linktitle: Induction structurelle
toc: true
type: book
date: "2019-11-04T00:00:00+01:00"
draft: false

weight: 5
---

## Exercice 6

Soit $F\_0 = \\{a\\}$ et $F\_1 = \\{s\\}$ . On considère l'ensemble $\mathcal{T}$ des termes construits sur $F\_0 \cup F\_1$.

1.  Démontrer que $\mathcal{T} =\\{s^n(a) \mid n \in \mathbb{N}\\}$, où $s^n(a)$ est défini inductivement par : $s^0(a)=a$ et pour tout $n \in \mathbb{N}$, $s^{n+1}(a) = s(s^n(a))$.

    **Indication :** L'ensemble $\mathcal{T}$ est défini inductivement par :

    _(B)_ $a$ appartient à  $\mathcal{T}$.

    _(I)_ Pour tout $t \in \mathcal{T}$, $s(t)$ appartient à $\mathcal{T}$

    Montrez d'abord que $\\{s^n(a) \mid n \in \mathbb{N}\\}$ est inclus dans $\mathcal{T}$, par récurrence sur $n$. Pour l'inclusion réciproque, on montre par induction sur la structure de $\mathcal{T}$ que pour tout terme $t \in \mathcal{T}$, il existe $k$ tel que $t = s^k(t)$.

Sur le domaine $D = \mathbb{N}$, on associe à la constante $a$ la valeur $a\_D \in \mathbb{N}$ et au symbole de fonction $s$ la fonction $s_D : D \longrightarrow D$ ; On rappelle que l'interprétation $h^\*$ des termes $T$ (à valeur dans $D$) est telle que :

_(B')_ Si $t = a \in F\_0$, $h^\*(t) = a\_D$,

_(I')_ Si $t = s(t\_1)$, $h^\*(t) = s_D(h^\*(t\_1))$.

Calculer $h^\*$ dans les cas suivants :

2.  $a\_D = 0$, $s\_D(n) = n + 1$.

    **Indication :** Dans ces trois questions, il faut deviner la forme générale de la valeur d'un terme, en calculant $h^\*(s(a))$, $h^\*(s^2(a))$, etc. Le cas de base (à vérifier) est toujours obtenu par $h^\*(a)=a_D$. Vérifiez par induction que $h^\*(s^{n}(a))=n$ pour tout $n$.

3.  $a\_D = 1$, $s\_D(n) = 2n$.

    **Indication :** Vérifiez par induction que $h^*(s^{n}(a))=2^n$ pour tout $n$.

4.  $a\_D = 1$, $s\_D(n) = n + 2$.

    **Indication :** Vérifiez par induction que $h^\*(s^{n}(a))=2n+1$ pour tout $n$.
