---
title: "TD2 : Ensembles ordonnés, Relations d'ordre"
linktitle: Exercices TD2
toc: true
type: docs
date: "2020-10-14T00:00:00+01:00"
lastmod: "2020-11-18T00:00:00+01:00"
draft: false
menu:
  mathdiscretes:
    parent: exos
    weight: 20

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2000

---



## Exercice 12

Soit $E$ un ensemble muni d'une relation d'ordre $\leq$. Montrer que si cette relation est totale, alors pour tout $x,y \in E$ :
$$(x \leq y \text{ et } x \neq y) \text{ ssi } y \not \leq x$$

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
On montre deux implications.

($\Rightarrow$) On raisonne par l'absurde. Supposons que $y \leq x$. Par hypothèse, puisque $\leq$ est une relation antisymétrique et $x \leq y$, on obtient $x=y$ ce qui contredit l'hypothèse $x \neq y$.

($\Leftarrow$) On raisonne par l'absurde. Supposons que la proposition $(x \leq y \text{ et } x \neq y)$ soit fausse. Cela signifie que soit $x \not \leq y$, soit $x=y$. Dans le premier cas, on a $x \not \leq y$ et, par hypothèse, $y \not \leq x$, ce qui est contradictoire puisque $\leq$ est supposée totale.
Dans le deuxième cas, $x=y$ contredit l'hypothèse $y \not \leq x$.
{{< /spoiler >}}

## Exercice 13

On considère un ensemble $E$ muni d'une opération binaire notée $\sqcup$ telle que $\sqcup$ est commutative, associative et idempotente (c'est-à-dire pour tout $x \in E$, $x \sqcup x = x$). On définit la relation $\preceq$ sur $E$ par : $x \preceq y$ ssi $x \sqcup y = y$.

## Exercice 13.1

Montrer que $\preceq$ est une relation d'ordre.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
La réflexivité est due à l'idempotence, l'antisymétrie résulte de la commutativité et la transitivité est une conséquence de l'associativité.

Remarquer que si $A$ est un ensemble, l'ensemble $E$ des parties de $A$ muni de l'union satisfait ces hypothèses, la relation d'ordre étant l'inclusion. De même, l'ensemble $E= \\{0,1\\}$ muni de l'opération "ou" satisfait ces hypothèses, la relation d'ordre est la relation naturelle sur $\\{0,1\\}$ avec $0 \preceq 1$
{{< /spoiler >}}

## Exercice 13.2

Montrer que toute paire d'éléments admet une borne supérieure.

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
Soit $D=\\{x,y\\}$ un ensemble à deux éléments. Alors $z=x \sqcup y$ est bien un majorant de $D$ car $x \sqcup z = z$ et $y \sqcup z=z$, par commutativité et associativité. De plus, tout majorant $z'$ de $D$ (qui satisfait donc $x \sqcup z' = z'$ et $y \sqcup z'=z'$) vérifie : $z \sqcup z'=(x \sqcup y)\sqcup z'=x \sqcup (y\sqcup z')=x \sqcup z'=z'$ donc $z \preceq z'$ et $z$ est le plus petit majorant.
{{< /spoiler >}}

## Exercice 14

Soit $E$ un ensemble. On considère l'ensemble $\wp(E)$ des parties de $E$, muni de la relation d'ordre partiel $\subseteq$. Montrer que pour tout $n \geq 2$ :

$$\inf(\\{A_1,A_2,\cdots,A_n\\}) = \bigcap\limits_{i=1}^{n} A_{i} \text{ et } \sup(\\{ A_1, \cdots , A_{n} \\}) = \bigcup\limits_{i=1}^{n} A_{i}$$

### Solution

{{< spoiler text="Cliquer ici pour voir la solution" >}}
On procède par récurrence sur $n$. Pour $n=2$, on montre que :

($i$) $\inf(\\{A_1,A_2\\}) = A_1 \cap A_2$. Il suffit de remarquer que $A_1 \cap A_2$ est un minorant de $\\{A_1,A_2 \\}$ puisque $A_1 \cap A_2 \subseteq A_1$ et $A_1 \cap A_2 \subseteq A_2$, et c'est le plus grand minorant de $\\{A_1,A_2 \\}$ car si un ensemble $K$ est tel que $K \subseteq A_1$ et $K \subseteq A_2$, alors on a $K \subseteq A_1 \cap A_2$.

($ii$) $\sup(\\{A_1,A_2\\}) = A_1 \cup A_2$. Il suffit de remarquer que $A_1 \cup A_2$ est un majorant de $\\{A_1,A_2 \\}$ puisque $A_1 \subseteq A_1 \cup A_2$ et   $A_2 \subseteq A_1 \cup A_2$, et c'est le plus petit majorant de $\\{A_1,A_2 \\}$ car si un ensemble $K$ est tel que $A_1 \subseteq K$ et $A_2 \subseteq K$, alors on a $A_1 \cup A_2 \subseteq K$.

On suppose à présent (par hypothèse de récurrence) que :

$$\inf(\\{A_1,A_2,\cdots,A_n\\}) = \bigcap\limits_{i=1}^{n} A_{i} \text{ et } \sup(\\{ A_1, \cdots , A_{n} \\}) = \bigcup\limits_{i=1}^{n} A_{i}$$

et on montre que :

($i$) $\inf(\\{A_1,A_2,\cdots,A_n,A_{n+1}\\}) = \bigcap_{i=1}^{n+1} A_{i}$. On a $\inf(\{B_1,B_2\}) = B_1 \cap B_2$, et en posant $B_1 = \inf(\\{A_1,A_2,\cdots,A_n\\})$ et $B_2 = A_{n+1}$, il suffit de montrer que :

$$\inf(\\{A_1,A_2,\cdots,A_n,A_{n+1}\\}) = \inf(\inf(\\{A_1,A_2,\cdots,A_n\\}),A_{n+1})$$

Posons $C = \inf(\inf(\\{A_1,A_2,\cdots,A_n\\}),A_{n+1})$. Par définition, $B_1$ est un minorant de $\\{A_1,A_2,\cdots,A_n\\}$ et $C$ est un minorant de $\\{ B_1 , A_{n+1} \\}$. On a donc  $B_1 \subseteq A_i$ pour tout $i$ ($1 \le i \le n$), $C \subseteq B_1$, et $C \subseteq A_{n+1}$. Par transitivité, il vient $C \subseteq A_i$ pour tout $i$ ($1 \le i \le n+1$) et $C$ est donc bien un minorant de $\\{A_1,A_2,\cdots,A_n,A_{n+1}\\}$. Montrons que c'est le plus grand minorant. Si $K$ est un minorant de $\{A_1,A_2,\cdots,A_n,A_{n+1}\}$, c'est également un minorant de $\\{A_1,A_2,\cdots,A_n\\}$ dont le plus grand minorant est $B_1$. On a donc $K \subseteq B_1$. De plus, on a $K \subseteq A_{n+1}$ et donc $K$ est aussi un minorant de $\\{ B_1 , A_{n+1} \\}$ dont le plus grand minorant est $C$. On obtient donc finalement bien $K \subseteq C$.

($ii$) $\sup(\{A_1,A_2,\cdots,A_n,A_{n+1}\}) = \bigcup_{i=1}^{n+1} A_{i}$. Puisque $\sup(\\{B_1,B_2\\}) = B_1 \cup B_2$, il suffit de poser $B_1 = \sup(\\{A_1,A_2,\cdots,A_n\\})$ et $B_2 = A_{n+1}$, et de montrer que :

$$\sup(\\{A_1,A_2,\cdots,A_n,A_{n+1}\\}) = \sup(\sup(\\{A_1,A_2,\cdots,A_n\\}),A_{n+1})$$

Posons $C = \sup(\sup(\\{A_1,A_2,\cdots,A_n\\}), A_{n+1})$. Par définition, $B_1$ est un majorant de $\\{A_1,A_2,\cdots,A_n\\}$ et $C$ est un majorant de $\\{ B_1 , A_{n+1} \\}$. On a donc  $A_i \subseteq B_1$ pour tout $i$ ($1 \le i \le n$), $B_1 \subseteq C$, et $A_{n+1} \subseteq C$. Par transitivité, il vient $A_i \subseteq C$ pour tout $i$ ($1 \le i \le n+1$) et $C$ est donc bien un majorant de $\\{A_1,A_2,\cdots,A_n,A_{n+1}\\}$. Montrons que c'est le plus petit majorant. Si $K$ est un majorant de $\{A_1,A_2,\cdots,A_n,A_{n+1}\}$, c'est également un majorant de $\\{A_1,A_2,\cdots,A_n\\}$ dont le plus petit majorant est $B_1$. On a donc $B_1 \subseteq K$. De plus, on a $A_{n+1} \subseteq K$ et donc $K$ est aussi un majorant de $\\{ B_1 , A_{n+1} \\}$ dont le plus petit majorant est $C$. On obtient donc finalement bien $C \subseteq K$.
{{< /spoiler >}}
