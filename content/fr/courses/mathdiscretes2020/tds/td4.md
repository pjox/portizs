---
title: "TD4 : Induction structurelle"
linktitle: Exercices TD4
toc: true
type: book
date: "2020-10-14T00:00:00+01:00"
lastmod: "2020-11-18T00:00:00+01:00"
draft: false
---

## Exercice 5

L'ordre préfixe sur $A^*$ peut être défini de deux manières différentes :

1. Pour tous mots $u, v \in A^*$, $u \preceq^1_{pref} v$ s'il existe $w \in A^*$ tel que $v=uw$.
2. Définition inductive :

    **(B)** pour tout mot $v \in A^*$,  $\varepsilon \preceq^2_{pref} v$.

    **(I)** Si $u,v \in A^*$ sont tels que $u \preceq^2_{pref} v$, alors pour toute lettre $a \in A$, $au \preceq^2_{pref} av$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
On considère les deux relations comme des sous-ensembles $R_1$ et $R_2$ de $A^\* \times A^\*$ et on montre les inclusions réciproques.

($R_1 \subseteq R_2$). On considère la propriété $P(u)$ : pour tout $v \in A^\*$, si $(u,v) \in R_1$ alors $(u,v) \in R_2$ et on montre cette propriété par récurrence sur la longueur de $u$. Pour $|u|=0$, c'est-à-dire $u = \varepsilon$, soit $v \in A^*$ alors $(u,v) \in R_1$ et aussi $(u,v) \in R_2$ d'après (B) donc $P(\varepsilon)$ est vraie. On suppose la propriété vraie pour tout mot de longueur $n$ et on considère $u$ de longueur $n+1>0$, donc $u = a u'$ pour $a \in A$ avec $u'$ de longueur $n$. Soit $v$ tel que $(u,v) \in R_1$.  Alors il existe $w$ tel que $v =uw=au'w$. Donc $v$ commence par $a$ et peut s'écrire $v=av'$. On en déduit que $v'=u'w$ donc $(u',v') \in R_1$.  En appliquant l'hypothèse de récurrence pour $u'$ de longueur $n$, on obtient $(u',v') \in R_2$. D'après (I) dans la définition de $R_2$, on en déduit $(au',av') \in R_2$, donc $(u,v) \in R_2$, et $P(u)$ est vraie.\\ Ainsi $P(u)$ est vraie pour tout mot $u$ et $R_1 \subseteq R_2$.

($R_2 \subseteq R_1$). Par définition, $R_2$ est le plus petit ensemble satisfaisant (B) et (I). Ainsi, montrer que $R_1$ satisfait aussi ces deux propriétés nous donnera l'inclusion cherchée. Comme $(\varepsilon, v) \in R_1$ pour tout $v \in A^*$, (B) est satisfaite par $R_1$. Soit maintenant $(u,v) \in R_1$ et $a \in A$. Alors il existe $w$ tel que $v = uw$ donc $av=auw$, ce qui donne $(au,av) \in R_1$ et $R_1$ satisfait aussi (I), ce qui donne le résultat.
{{< /spoiler >}}

## Exercice 6

On définit l'ensemble $\mathcal{L}$ inductif suivant :

  **(B)** $\texttt{nil} \in\mathcal{L}$

  **(I)** pour tout $n\in \mathbb{N}$, pour tout $x\in \mathcal{L}$, $n | x \in \mathcal{L}$.

## Exercice 6.1

Montrer par induction structurelle que si $x\in\mathcal{L}$, alors soit $x=\verb+nil+$, soit il existe $a_1, \cdots, a_k\in \mathbb{N}$ tels que  $x=a_k|\cdots|a_1 | \verb+nil+$. On appelle $a_1, \dots, a_k$ les _élements_ de $x$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Si $x=\texttt{nil}$, alors la propriété est trivialement vérifiée. Soit $n\in\mathbb{N}$ et $y\in \mathcal{L}$ tels que $x=n\mid y$. Alors, par hypothèse d'induction, soit $y= \texttt{nil}$, soit il existe $a_1,\cdots, a_k\in \mathbb{N}$ tels que $y=a_k\mid\cdots\mid a_1 \mid \texttt{nil}$. Dans le premier cas, $x=n|\texttt{nil}$, et en posant $a_1=n$, on a bien $x=a_1\mid \texttt{nil}$. Dans le second cas, par construction, $x = n \mid a_k\mid\cdots\mid a_1 \mid \texttt{nil}$, donc en posant $a_{k+1}=n$, il existe bien $a_1,a_2,\cdots, a_k,a_{k+1}\in\mathbb{N}$ tels que $x=a_{k+1}\mid a_k\mid\cdots\mid a_1 \mid \texttt{nil}$
{{< /spoiler >}}

## Exercice 6.2

Soit la fonction $s:\mathcal{L}\rightarrow \mathbb{N}$ définie par $s(\verb+nil+)=0$ et, pour tout $n\in\mathbb{N}$, pour tout $x\in\mathcal{L}$, $s(n|x)=n+s(x)$. Calculer $s( 1| 2 |  3 | \texttt{nil})$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
$$\begin{align}
s( 1| 2 |  3 | \texttt{nil})&=1+s( 2 |  3 | \texttt{nil})\\\\
&=1+2+s( 3 | \texttt{nil})\\\\
&=1+2+3+s(\texttt{nil})\\\\
&=1+2+3+0\\\\
&=6.
\end{align}$$
{{< /spoiler >}}

## Exercice 6.3

Montrer que, pour tout $x\in\mathcal{L}$, si $x=\texttt{nil}$ $s(x)=0$, sinon $s(x)=\sum_{i=1}^k a_i$ où les $a_i$ sont les éléments de $x$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Pour le cas de base $x=\texttt{nil}$, par définition $s(x)=0$. Soit maintenant $x=n\mid y$ pour $n\in \mathbb{N}$ et $y\in \mathcal{L}$. Par hypothèse d'induction, si $y=\texttt{nil}$, $s(y)=0$, sinon, $s(y)=\sum_i^k a_i$ où $a_1, \cdots, a_k$ sont les éléments de $y$. Si $y=\texttt{nil}$, alors $x=n\mid \texttt{nil}$, et le seul élément de $x$ est $n$. Alors par définition, $s(x)=n+s(y)=n+0=n$. Si $y=a_k\mid \cdots \mid a_1$, alors les éléments de $x$ sont $n, a_1, \cdots, a_k$, et, par définition de $s$, $s(x)=n+s(y)=n+\sum_i^k a_i$. La propriété est donc bien vérifiée pour tout $x\in\mathcal{L}$.
{{< /spoiler >}}
