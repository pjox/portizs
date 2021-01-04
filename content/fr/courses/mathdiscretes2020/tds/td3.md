---
title: "TD3 : Induction sur $\\mathbb{N}$"
linktitle: Exercices TD3
toc: true
type: book
date: "2020-10-14T00:00:00+01:00"
lastmod: "2020-11-18T00:00:00+01:00"
draft: false
---



## Exercice 3

La suite harmonique est définie par $H_n = 1+1/2+\cdots + 1/n$  pour $n\geq 1$.

## Exercice 3.1

Montrer que $H_{2^n}\geq 1+n/2$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
**Cas de base** : Pour $n=0$, $H_1=1=1+0/2$.

**Cas d'induction** : Montrons que $P(n)$ implique $P(n+1)$ pour tout $n\geq 0$, où $P(n) \ : H_{2^n}\geq 1+n/2$. On a

$$ \begin{align} 
H_{2^{n+1}} &= H_{2^n}+\underbrace{1/(2^n+1)+\cdots+1/2^{n+1}}_{2^n\text{ termes }\geq  1/2^{n+1}}\geq 1+ n/2+1/2\\\\
& =1+(n+1)/2
\end{align}$$
{{< /spoiler >}}

## Exercice 3.2

Montrer par induction que $H_n = p_n/q_n$ avec $p_n$ entier positif impair et $q_n$ entier positif pair pour $n \geq 2$. En déduire que $H_n$ n'est pas entier pour $n\geq 2$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Il faut ici une induction généralisée pour le cas (ii) de l'étape d'induction.
**Base** : $H_2=3/2$.

**Induction** :

$$H_{n+1} = \frac{p_n}{q_n}+\frac{1}{n + 1} = \frac{(n+1)p_n +q_n}{(n+1)q_n}.$$

1. si $n+1$ impair, $(n+1)p_n+q_n$ impair et $(n+1)q_n$ pair.
2. si $n+1$ pair, soit $n+1=2k$, alors :

$$\begin{align}
H_{n+1} &= 1+1/2+ \dots +1/(n+1) \\\\
&= 1+1/3+ \dots +1/(2k-1) + 1/2(1 + 1/2 + \dots + 1/k) \\\\
&= p_k/2q_k+a/b =\frac{bp_k+2aq_k}{2q_kb} \\\\
&\text{avec } b = 1 \times 3 \times \dots \times (2k - 1) \text{ impair}
\end{align}$$
et on obtient bien que $H_{n+1}$ est le quotient d'un terme impair par un terme pair dans les deux cas, ce qui achève notre raisonnement.
{{< /spoiler >}}

## Exercice 7.1

On suppose qu'une propriété $P$ définie sur $\mathbb{N}$ vérifie :

1. $P (1)$ est vraie
2. si $P (n)$ est vraie alors $P (2n)$ est vraie (pour $n \geq 1$)
3. si $P (n)$ est vraie alors $P (n - 1)$ est vraie (pour $n \geq 2$).

Montrer par récurrence sur $n$ que $P (n)$ est vraie pour tout $n \geq 1$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
**Base** : $P (1)$ vraie (par (1))

**Induction** : Supposons $P (n)$ vraie pour un entier $n \geq 1$, alors par (2) $P (2n)$ vraie et par (3) $P (2n - 1), \dots, P (n + 1)$ vraies, car $2n, 2n-1, \ldots,  n+1$ sont supérieurs ou égaux à $2$. Donc $P (n)$ implique $P (n + 1)$ pour  $n \geq 1$ et on obtient le résultat.
{{< /spoiler >}}

## Exercice 7.2

On veut montrer que la moyenne arithmétique est supérieure à la
moyenne géométrique.  Soient $a_1, \dots, a_n$ $n$ nombres réels positifs, avec $n \geq 1$ ; on pose $A = (a_1 + \dots + a_n)/n$ et $G = (a_1 \dots a_n )^{1/n}$ , montrer que $A \geq G$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Par induction sur $n$ on montre $P(n)$ vraie pour tout $n$, où :

$$ P(n): \text{ pour tout } n\text{-uplet } a_1,\dots,a_n>0, \ A\geq G$$

**Base** : ($n = 1$, et $A = G$ inutile pour le raisonnement) $n = 2$ et $(a_1 + a_2)/2 \geq \sqrt{a_1 a_2}$ en effet $(\sqrt{a_1}-\sqrt{a_2})^2=a_1+a_2-2\sqrt{a_1 a_2}\geq 0$.

**Induction** : $P (n) \Longrightarrow P (n - 1)$ et  $P (n) \Longrightarrow P (2n)$ pour tout $n \geq 2$, d'où le résultat.

* $P (n) \Longrightarrow P (2n)$ :

$$\begin{align}
&(a_1+\dots+a_n+a_{n+1}+\dots+a_{2n})/2n\\\\
&=1/2\left((a_1+\dots+a_n)/n+(a_{n+1}+\dots+a_{2n})/n\right)\\\\
&\geq1/2\left((a_1\dots a_n)^{1/n}+(a_{n+1}\dots a_{2n})^{1/n}\right)\\\\
&\text{(par hypothèse de récurrence appliquée deux fois)}\\\\
&\geq(a_1\dots a_n a_{n+1}\dots a_{2n})^{1/2n} \text{ par } P(2)
\end{align}$$

* $P (n) \Longrightarrow P (n - 1)$ :

pour montrer $P(n-1)$ pour $a_1,\dots a_{n-1}$ donnés, on choisit d'ajouter $a_n=(a_1+\dots+a_{n-1})/(n-1)$ et on va utiliser $P(n)$ sur le $n$-uplet ainsi formé.

On a

$$A_{n-1}=\frac{(a_1+\dots+a_{n-1})}{(n-1)}=a_n$$

et

$$\begin{align}
A_n&=\frac{(a_1+\dots+a_{n-1})+\frac{(a_1+\dots+a_{n-1})}{(n-1)}}{n}\\\\
&=\frac{(n-1)(a_1+\dots+a_{n-1})+(a_1+\dots+a_{n-1})}{n(n-1)}\\\\
&=\frac{(a_1+\dots+a_{n-1})}{(n-1)}=a_n
\end{align}$$

d'où $A=(a_1+\dots+a_n)/n=(a_1+\dots+a_{n-1})/(n-1)=a_n$. Par $P(n)$, $A\geq(a_1 \dots a_n )^{1/n}=(a_1 \dots a_{n-1})^{1/n}A^{1/n}$, d'où $A^{1-1/n}\geq(a_1 \dots a_{n-1})^{1/n}$ et en élevant à la puissance $n/(n-1)$, on obtient $A=(A^{1-1/n})^{n/(n-1)}\geq (a_1 \dots a_{n-1})^{(1/n)\times(n/(n-1)}=(a_1 \dots a_{n-1})^{1/(n-1)}$, ce qui correspond à $P(n-1)$.
{{< /spoiler >}}

## Exercice 8.1

Montrer que pour tout $n\in \mathbb{N}$, $(n+1)^2-(n+2)^2-(n+3)^2+(n+4)^2=4$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
On développe l'expression (astucieusement :smile:) et on obtient le résultat:
$$\begin{align}
&(n+1)^2-(n+2)^2-(n+3)^2+(n+4)^2\\\\
&=(n+1)^2-(n+1+1)^2-(n+3)^2+(n+3+1)^2\\\\
&=(n+1)^2-(n+1)^2-2(n+1)-1\\\\
&\phantom{=}-(n+3)^2+(n+3)^2+2(n+3)+1\\\\
&=2(n+3)-2(n+1)=2(3-1)=4.
\end{align}$$
{{< /spoiler >}}

## Exercice 8.2

En déduire que tout entier $m$ peut s'écrire comme somme et différence des carrés $1^2, 2^2,\ldots , n^2$ pour un certain $n$, c'est-à-dire que pour tout $m$ :

$P(m)$ : il existe $n\in \mathbb{N}$, et $\varepsilon\_1,\ldots, \varepsilon\_n\in \{-1,1\}$, tels que $m=\varepsilon\_{1}1^2+\varepsilon\_{2}2^2+\cdots +\varepsilon\_{n}n^2$.

_Indication_ : montrer d'abord le résultat pour $m\in\\{0,1,2,3\\}$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
On voit (tout de suite ... ) que $0 = 1^2+2^2-3^2+4^2-5^2-6^2+7^2,$ que $1=1^2,$ que $2=-1^2-2^2-3^2+4^2$ et que $3=-1^2+2^2$. Puis $P(m)$ implique $P(m+4)$ car $4=(n+1)^2-(n+2)^2-(n+3)^2+(n+4)^2$.
{{< /spoiler >}}
