---
title: Quiz 1
linktitle: Quiz 1
toc: true
type: docs
date: "2019-10-20T00:00:00+01:00"
draft: false
menu:
  mathdiscretes:
    parent: control
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3

---

## Exercice 1

Soit $E$ un sous-ensemble d'un ensemble $F$ et $x$ un élément de $F$ qui n'est pas dans $E$. Montrer que : $$\mathcal{P}(E \cup \{x\}) = \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$$

### Solution

*   $\mathcal{P}(E\cup\\{x\\})\subseteq \mathcal{P}(E)\cup\\{\\{x\\}\cup A \mid A \in \mathcal{P}(E)\\}$
  
    Soit $B$ une partie de $E \cup \\{x\\}$, on distingue deux cas. Si $x \in B$, alors $B - \\{x\\}$ est une partie de $E$, et on a donc $B \in \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$ ce qui permet d'obtenir $B \in \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$. Sinon, si $x \notin B$, alors $B$ est une partie de $E$ et on obtient directement $B \in \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$.

*   $\mathcal{P}(E)\cup\\{\\{x\\}\cup A \mid A \in \mathcal{P}(E)\\} \subseteq \mathcal{P}(E \cup \\{x\\})$

    Soit $B \in \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$, on a $B \in \mathcal{P}(E)$ ou $B \in \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$ et donc il vient $B \subseteq E$ ou $B = \\{x\\} \cup A$ pour une certaine partie $A$ de $E$, c’est à dire pour un ensemble $A \subseteq E$. Dans les deux cas on a bien $B \subseteq E \cup \\{x\\}$ ce qui permet finalement d’obtenir $B \in \mathcal{P}(E \cup \\{x\\})$.

**Remarque :** Cette démonstration est l'étape de récurrence qui permet de montrer que pour tout ensemble fini $E$ à $n$ éléments, l'ensemble $\mathcal{P}(E)$ des parties de $E$ a pour cardinal $2n$. En effet, pour $n = 0$, l’ensemble $E$ est vide, donc $\mathcal{P}(E) = \\{\emptyset\\}$ a un seul élément. Considérons un ensemble ayant $n + 1$ éléments, il est de la forme $E \cup \\{x\\}$ pour un élément $x$ n'appartenant pas à $E$. L’hypothèse de récurrence donne $\text{card}(\mathcal{P}(E)) = 2^n$ et on déduit de la démonstration ci-dessus que le cardinal de $\mathcal{P}(E \cup \\{x\\})$ est égal à $2 \times \text{card}(\mathcal{P}(E))$, ce qui permet de conclure.

## Exercice 2

Montrer que si $A$ admet un plus grand élément alors cet élément est l'unique  élément maximal.

### Solution

Supposons que $A$ admet un plus grand  élément $M \in A$. Alors, pour tout $a \in A$, $a \preceq M$ .Donc, pour tout $a\in A$, si $M \preceq a$, alors $M = a$ (par antisymétrie de la relation d'ordre), et $M$ est un  élément maximal. De plus cet élément maximal est unique : supposons qu'il existe $M'$ un autre élément maximal. Alors, comme $M' \preceq M$, mais comme $M'$ est un élément maximal, alors $M' = M$.

## Exercice 3

Soit $\*$ une opération binaire sur un ensemble $E$. Démontrer que si $\*$ admet un élément neutre, cet élément neutre est unique.

### Solution

Soient $\epsilon$ et $\epsilon'$ deux éléments neutres, on a $\epsilon'=\epsilon'\*\epsilon=\epsilon$.

## Exercice 4

Soit $a$ un entier. Soit $P_a(n)$ la propriété « $9 \mid (10^n +a)$ ». Montrer que, pour tout entier $a$ et tout $n \in \mathbb{N}$, $P_a(n)$ implique $P_a(n+1)$ . A-t-on $P_a(n)$ pour tout $n \in \mathbb{N}$ ?

### Solution

$(10^{n+1} + a) − (10^n + a) = 10\times 10^n − 10^n = 9 \times 10^n$ donc $P_a(n)$ implique $P_a(n + 1)$. 

Pour que la propriété soit vraie pour tout $n$,il faut qu'elle soit vraie en $0$, soit $9\mid a+1$ et $a=−1 \mod 9$. C'est le cas pour $a = −1$ par exemple mais pas pour $a = +1$. On voit ici combien le cas de base est important.

## Exercice 5

On considère un ensemble $E$ muni d'une opération binaire notée $\sqcup$ telle que $\sqcup$ est commutative, associative et idempotente (c'est-à-dire pour tout $x \in E$, $x \sqcup x = x$). On définit la relation $\preceq$ sur $E$ par : $x \preceq y$ si $x \sqcup  y = y$.

1. Montrer que $\preceq$ est une relation d’ordre.
2. Montrer que toute paire d’éléments admet une borne supérieure.

### Solution

1.  On va montrer que $\preceq$ est réflexive, antisymétrique et transitive.
    * **Réflexive :** Soit $x \in E$ comme $\sqcup$ est idempotente alors $x \sqcup x = x$ donc $x \preceq x$, et $\preceq$ est réflexive.
    * **Antisymétrique :** Soient $x,y \in E$, et supposons que $x \preceq y$ et $y \preceq x$. Donc par définition on a $x \sqcup  y = y$ et $y \sqcup  x = x$. Alors en utilisant la commutativité de $\sqcup$ on obtient $$x = y \sqcup  x = x \sqcup y = y$$ donc $\preceq$ est antisymétrique.
    * **Transitive :** Soient $x,y,z \in E$, et supposons que $x \preceq y$ et $y \preceq z$. Donc par définition on a $x \sqcup  y = y$ et $y \sqcup  z = z$. Alors en utilisant la associativité de $\sqcup$ on obtient $$x \sqcup z = x\sqcup (y \sqcup z) = (x \sqcup y) \sqcup z = y \sqcup z = z$$. Donc $x \preceq z$ et $\preceq$ est transitive.

2.  Soit $D = \\{x, y\\}$ un ensemble à deux éléments. Alors $z = x \sqcup y$ est bien un majorant de $D$ car $x \sqcup z = z$ et $y \sqcup z = z$, par commutativité et associativité. De plus, tout majorant $z'$ de $D$ (qui satisfait donc $x \sqcup z' = z'$ et $y \sqcup z' = z'$) vérifie : $$z\sqcup z' =(x\sqcup y) \sqcup z' = x \sqcup (y\sqcup z') = x \sqcup z' = z'$$ donc $z \preceq z'$ et $z$ est le plus petit majorant.