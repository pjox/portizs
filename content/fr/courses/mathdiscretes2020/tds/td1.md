---
title: "TD1 : Ensembles, Relations, Fonctions"
linktitle: Exercices TD1
toc: true
type: book
date: "2020-10-14T00:00:00+01:00"
lastmod: "2020-10-14T00:00:00+01:00"
draft: false

---

## Lois de Morgan

Soient $A, B$ des ensembles, alors

$$\overline{A \cap B} = \overline{A} \cup \overline{B}$$
$$\overline{A \cup B} = \overline{A} \cap \overline{B}$$

**Preuve :**

1.  On commence par montrer $\overline{A \cap B} \subseteq \overline{A} \cup \overline{B}$, donc supposons $x \in \overline{A \cap B}$, i.e., $x \notin A \cap B$. Comme $A \cap B = \\{y \mid y \in A \text{ et } y \in B \\}$, alors $x \notin A$ ou $x \notin B$. Si $x \notin A$ donc $x \in \overline{A} \subseteq \overline{A} \cup \overline{B}$. Si $x \notin B$, donc $x \in \overline{B} \subseteq \overline{A} \cup \overline{B}$. Dans les deux cas $x \in \overline{A} \cup \overline{B}$ et en conséquence $\overline{A \cap B} \subseteq \overline{A} \cup \overline{B}$. 

    Pour montrer l'autre inclusion, supposons en raisonnant par l'absurde que $x \in \overline{A} \cup \overline{B}$ mais que $x \notin \overline{A \cap B}$. Donc $x \in A \cap B$, c'est-à-dire, $x \in A$ et $x \in B$; mais cela implique que $x \notin \overline{A}$ et $x \notin \overline{B}$, i.e., $x \notin \overline{A} \cup \overline{B}$, une contradiction. En conséquence $x \in \overline{A \cap B}$ et alors $\overline{A \cap B} = \overline{A} \cup \overline{B}$

2.  Supposons $x \in \overline{A \cup B}$, i.e., $x \notin A \cup B$. Comme $A \cup B = \\{y \mid y \in A \text{ ou } y \in B \\}$, alors $x \notin A$ et $x \notin B$. On peut en déduire immédiatement $x \notin \overline{A} \cap \overline{B}$.

    Pour l'autre inclusion, supposons $x \in \overline{A} \cap \overline{B}$ mais $x \notin \overline{A \cup B}$. Donc $x \in A \cup B$, c'est-à-dire, $x \in A$ ou $x \in B$, mais de $x \in \overline{A} \cap \overline{B}$ on sait que $x \notin A$ et $x \notin B$. On obtient une contradiction et en consequence $x \in  \overline{A \cup B}$, i.e., $\overline{A \cup B} = \overline{A} \cap \overline{B}$.

## Exercice 2.4

Soient $A, B, C$ trois parties de $E$. Montrer que si $\bigl(A \cup B\subseteq A \cup C$ et $A\cap B\subseteq A\cap C \bigr)$ alors $B\subseteq C$. Dans quel cas a-t-on l'égalité $B=C$?

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Supposons $A \cup B \subseteq A \cup C$ et $A \cap B \subseteq A \cap C$.
Puisque $A \cup B \subseteq A \cup C$ et $B \subseteq A \cup B$, on a $B \subseteq A \cup C$ et par conséquent $B \subseteq B \cap (A \cup
C)$. Appliquons la distributivité de $\cap$ sur $\cup$ : $B \subseteq B \cap (A \cup C) = (B \cap A)\cup (B \cap C)$ puis la deuxième inclusion de l'énoncé $(B \cap A) \subseteq (A \cap C)$, on obtient $B \subseteq (A \cap C)\cup (B \cap C)$ et on utilise la distributivité de $\cup$ sur $\cap$ pour regrouper les termes $(A \cap C)\cup (B \cap C)=(A \cup B)\cap C$ donc finalement $B = (A \cup B)\cap C \subseteq C$.

Montrons que $B=C \Leftrightarrow \bigl(A \cup B = A \cup C$ et $A \cap B = A \cap C \bigr)$. L'implication $\Rightarrow$ est immédiate. Réciproquement, en appliquant deux fois le résultat de la question précédente (l'un avec $A$, $B$ et $C$ dans l'ordre de l'énoncé, l'autre en échangeant les rôles de $B$ et $C$) on obtient $B \subseteq C$ et $C\subseteq B$, donc $B=C$.
{{< /spoiler >}}

## Exercice 2.7

Soit $E$ un sous-ensemble d'un ensemble $F$ et $x$ un élément de $F$ qui n'est pas dans $E$. Montrer que : $$\mathcal{P}(E \cup \{x\}) = \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$$

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
*   $\mathcal{P}(E\cup\\{x\\})\subseteq \mathcal{P}(E)\cup\\{\\{x\\}\cup A \mid A \in \mathcal{P}(E)\\}$
  
    Soit $B$ une partie de $E \cup \\{x\\}$, on distingue deux cas. Si $x \in B$, alors $B - \\{x\\}$ est une partie de $E$, et on a donc $B \in \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$ ce qui permet d'obtenir $B \in \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$. Sinon, si $x \notin B$, alors $B$ est une partie de $E$ et on obtient directement $B \in \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$.

*   $\mathcal{P}(E)\cup\\{\\{x\\}\cup A \mid A \in \mathcal{P}(E)\\} \subseteq \mathcal{P}(E \cup \\{x\\})$

    Soit $B \in \mathcal{P}(E) \cup \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$, on a $B \in \mathcal{P}(E)$ ou $B \in \\{\\{x\\} \cup A \mid A \in \mathcal{P}(E)\\}$ et donc il vient $B \subseteq E$ ou $B = \\{x\\} \cup A$ pour une certaine partie $A$ de $E$, c’est à dire pour un ensemble $A \subseteq E$. Dans les deux cas on a bien $B \subseteq E \cup \\{x\\}$ ce qui permet finalement d’obtenir $B \in \mathcal{P}(E \cup \\{x\\})$.

**Remarque :** Cette démonstration est l'étape de récurrence qui permet de montrer que pour tout ensemble fini $E$ à $n$ éléments, l'ensemble $\mathcal{P}(E)$ des parties de $E$ a pour cardinal $2n$. En effet, pour $n = 0$, l’ensemble $E$ est vide, donc $\mathcal{P}(E) = \\{\emptyset\\}$ a un seul élément. Considérons un ensemble ayant $n + 1$ éléments, il est de la forme $E \cup \\{x\\}$ pour un élément $x$ n'appartenant pas à $E$. L’hypothèse de récurrence donne $\text{card}(\mathcal{P}(E)) = 2^n$ et on déduit de la démonstration ci-dessus que le cardinal de $\mathcal{P}(E \cup \\{x\\})$ est égal à $2 \times \text{card}(\mathcal{P}(E))$, ce qui permet de conclure.
{{< /spoiler >}}

## Exercice 7

On considère l'ensemble ${\mathbb{N}}\times ( \mathbb{N} \setminus \{0\})$, c'est-à-dire l'ensemble des couples d'entiers naturels dont le deuxième élément est non nul. Soit $R$ définie sur cet ensemble par :

$$(a,b) R (c,d) \text{ ssi } ad=bc$$

Démontrer que $R$ est une relation d'équivalence.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Noter que $(a,b) R (a,b)$ pour tout $(a,b)\in {\mathbb{N}}\times ( \mathbb{N} \setminus \{0\})$, puisque $ab=ba$; donc la relation $R$ est reflexive.

Supposons que $(a,b) R (c,d)$. Alors $ad=bc$ et en particulier, $cb=da$. Donc, par définition, $(c,d)R(a,b)$ et la relation $R$ est symétrique.

Supposons que $(a,b) R (c,d)$ et que $(c,d) R (e,f)$. Alors $ad=bc$ et $cf=de$. En particulier $(ad)(cf)=(bc)(de)$, et en simplifiant par $cd$ on obtient $af=be$. Il faut aussi vérifier le cas particulier où $c=0$, puisque $d \neq 0$. On obtient alors $(a,b)R(e,f)$ d'où $R$ est transitive.

Comme $R$ est réflexive, transitive et symétrique, c'est une relation d'équivalence.

Notons que si la paire ordonnée $(a,b)$ est écrite sous forme de fraction $\frac{a}{b}$, alors la relation $R$ est la définition d'égalité de deux fractions, c'est-à-dire $\frac{a}{b}=\frac{c}{d}$ si et seulement si $ad=bc$.
{{< /spoiler >}}

## Exercice 11.2

Soit $E$ un ensemble et $\equiv$ une relation d'\'equivalence sur $E$.

1.   On considère l'application $f : E \to E\_{/\equiv}$ qui à tout $x \in E$ associe $f(x)=\[x\]\_{\equiv}$. $f$ est-elle injective ? surjective ? bijective ?
2.   Soient $F$ un ensemble et $g : E_{/\equiv} \to F$ et $h : E \to F$ deux applications telles que pour tout $x \in E$, $h(x)=g(\[x\]_{\equiv})$. Montrer que $g$ est injective si et seulement si pour tous $x,x' \in E$, $h(x)=h(x')$ implique $x \equiv x'$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}

1.   $f$ n’est pas nécessairement injective : si $x,x' \in E$ et $x \equiv x'$, alors $f(x) = f(x')$ même si $x \neq x'$. $f$ est surjective : soit $y \in E_{/\equiv}$, alors il existe $x$ tel que $y = \[x\]\_{\equiv}$ et $y = f(x)$. $f$ n’est donc pas nécessairement bijective.

2.   Supposons $g$ injective. Soient $x,x' \in  E$ tels que $h(x) = h(x')$. Alors par définition, $g\(\[x\]\_{\equiv}\) = g\(\[x'\]\_{\equiv}\)$. Or, $g$ est injective, donc $\[x\]\_{\equiv} = \[x'\]\_{\equiv}$ et $x \equiv x'$. Réciproquement,  soient $y, y' \in E\_{/\equiv}$ tels que $g(y) = g(y')$. Pour tout $x \in y$, $h(x) = g(y)$ et pour tout $x' \in  y'$, $h(x') = g(y')$. Donc, $h(x) = h(x')$ pour tous $x \in y, x' \in y'$. Par hypothèse, cela signifie que $x \equiv x'$, pour tous $x \in y, x'  \in y'$. Donc $\[x\]\_{\equiv} = y = \[x'\]\_{\equiv} =y'$ et $g$ est injective.

{{< /spoiler >}}

## Exercice 12

Si $n<m$, il n'existe pas d'injection d'un ensemble à $m$ éléments dans un ensemble à $n$ éléments. Une formulation plus imagée de ce résultat est le _principe des tiroirs_ (ou encore _pigeon-hole principle_), à savoir: si ${n<m}$ et que l'on veut placer $m$ chemises dans $n$ tiroirs alors un tiroir au moins contiendra plusieurs chemises. Plus précisément, montrer qu'un tiroir contiendra au moins un nombre entier $p\ge \frac{m}{n}$ chemises.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Soit $A=\\{1,2,\ldots,m\\}$ l'ensemble des chemises à répartir et soit $A\_i$ l'ensemble des chemises contenues dans le tiroir $i$, pour $i\in \[n\]$. $A\_1, \ldots, A\_n$ forment une partition de $A$, donc

$$|A|= \sum_{i=1}^n|A_i|\,.$$

Si l'on avait: $\forall i\in \[n\]$, $|A_i| < \frac{m}{n}$, on pourrait en déduire

$$|A| = \sum_{i=1}^n |A_i| < n\times \frac{m}{n}=m,$$

une contradiction; donc on a $|A\_i| \geq \frac{m}{n}$ pour un $i$ au moins.
{{< /spoiler >}}

## Exercice 14

On dit qu'une application $f:E \to E$ est une involution si et seulement si pour tout $x \in E$, $f(f(x)) = x$. Montrer que si $f$ est une involution alors $f$ est bijective.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Soit $f:E \to E$ une involution. Montrons que $f$ est bijective. Si $x_1,x_2 \in E$ sont tels que $f(x\_1)=f(x\_2)$, alors
$f(f(x_1))=f(f(x_2))$, et puisque $f$ est involutive, on a alors $x\_1=x\_2$, et donc $f$ est injective. Soit $x \in E$, puisque $f$ est involutive, on a $x = f(f(x))$, et donc $x$ admet bien un antécédent $f(x) \in E$ par $f$ qui est donc une application surjective.
{{< /spoiler >}}

## Exercice 18

On dit qu'un ensemble $E$ est _dénombrable_ s'il existe une bijection entre cet ensemble et $\mathbb{N}$. Montrer que $\mathbb{N}^2 = \mathbb{N} \times \mathbb{N}$ est dénombrable. On pourra montrer que les fonctions $f$ et $g$ suivantes sont des bijections de $\mathbb{N}^2$ dans $\mathbb{N}$ : $f(x,y) = y+(0+1+ 2+\cdots+(x+y))$ et $g(x,y)=2^y(2x+1)-1$.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Le premier dessin représente le chemin correspondant à la bijection $f(x,y) = y + (0 + 1 + 2 + \cdots + (x + y))$, les trois autres représentent des autres chemins possibles.

{{< figure library="true" src="/media/mathdisc/fonctions/diag1.svg" caption="chemin correspondant à la bijection $f(x,y)$" >}}
{{< figure library="true" src="/media/mathdisc/fonctions/diag2.svg" >}}
{{< figure library="true" src="/media/mathdisc/fonctions/diag3.svg" >}}
{{< figure library="true" src="/media/mathdisc/fonctions/diag4.svg" >}}

Une autre façon de montrer cette bijection consiste à utiliser la _« moitié »_ de N pour numéroter $\mathbb{N} \times \\{0\\}$, puis la _« moitié »_ de ce qui reste pour numéroter $\mathbb{N} \times \\{1\\}$, puis la _« moitié »_ de ce qui reste pour numéroter $\mathbb{N} \times \\{2\\}$, etc (bijection $g$).

$\mathbb{N} = \\{0, 1, 2, 3, \ldots\\}$, on compte de 2 en 2 pour numéroter $\mathbb{N} \times \\{0\\}$. 

Il reste :

$\mathbb{N}_1 = \\{1,3,5,7,\ldots\\}$, on compte de 2 en 2 pour numéroter $\mathbb{N}\times\\{1\\}$. 

Il reste :

$\mathbb{N}_2 =\\{3,7,11,15,\ldots\\}$, on compte de 2 en 2 pour numéroter $\mathbb{N}\times\\{2\\}$. 

Il reste :

$\mathbb{N}_3 = \\{7,15,23,31,\ldots\\}$, etc.

{{< figure library="true" src="/media/mathdisc/fonctions/diag5.svg" >}}

Pour prouver plus formellement que $f$ est une bijection, considérons la suite définie par $u_p = 1 + \cdots + p$ pour $p \le 1$, et $u_0 = 0$. Par définition cette suite est strictement croissante. Ainsi, pour tout entier $n$, il existe un unique entier $p$ tel que $u_p \le n < u_p+1$. Le couple $(x, y)$ antécédent de $n$ par $f$ est alors défini par : $y = n − u_p$ et $x = p − y$.
{{< /spoiler >}}

## Exercice 20

Montrer qu'il n'existe pas de bijection entre un ensemble et l'ensemble de ses parties.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
On montre simplement qu'il n'existe pas de surjection $f$ entre un ensemble $E$ et l'ensemble de ses parties. En effet, supposons qu'une telle application existe. Pour toute partie $X$ de $E$, il existe un élément $x \in E$ tel que $X=f(x)$. Considérons à présent la partie de $E$  définie par $A = \\{ x \in E \mid x \notin f(x) \\}$. Par hypothèse, $A$ est l'image d'un élément $a \in E$, et on a donc $A = f(a)$. Deux cas sont possibles. Si $a \in A$, alors, par définition de $A$, $a \notin f(a)$. Or $f(a) = A$ ce qui est contradictoire. Sinon $a \notin A$, et alors, par définition de $A$, $a \in f(a)$. Or $f(a) = A$ ce qui est contradictoire.
{{< /spoiler >}}

## Exercice 21.1

Montrer que $(\mathbb{N}, + ,0)$ et $(\wp(E), \cup ,\emptyset)$ sont des monoïdes commutatifs.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
cf. définition.
{{< /spoiler >}}

## Exercice 21.2

Soit $A$ un alphabet. L'ensemble des mots de $A^\*$ de longueur paire est-il un monoïde pour la concaténation ? Même question pour l'ensemble des mots de $A^\*$ de longueur impaire.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Longueur paire: stable pour la concaténation puisque la somme de deux nombres pairs est paire et $\varepsilon$ l'élément neutre de la concaténation en fait partie, donc sous-monoïde de $A^\*$.

Longueur impaire: instable la concaténation puisque la somme de deux nombres impairs est paire et $\varepsilon$ l'élément neutre de la concaténation n'en fait pas partie, donc pas un sous-monoïde de $A^\*$.
{{< /spoiler >}}
