# Complétude

## Espace totalement bornés


```{admonition} Définition
Soient $(X, d)$ un espace métrique, et $A$ un sous-ensemble de $X$ ($A\subset X$).

On appelle **diamètre** de $A$ :

$$
diam(A)= sup\{d(a,b), a, b \in A\}
$$
 qui peut être reel ou $+\infty$.
```
```{admonition} Exemple
- Si $A$ est un singleton ($A= \{x\}$ avec $x\in X$) alors le diamètre de $A$ est : $diam(A)=0$
- Le diamètre d'une boule ouverte ($B(x,r)$) de centre $x$ est de rayon $r>0$  est: $diam(B(x,r))\leq 2r$
- Le diamètre d'une boule fermée ($B_f(x,r)$) de centre $x$ est de rayon $r>0$  est: $diam(B_f(x,r))\leq 2r$

```
```{admonition} Proposition
Si $A\subset B$ alors $diam(A)\leq diam(B)$.
```
```{admonition} Définition

Soient $(X, d)$ un espace métrique, et $A$ un sous-ensemble de $X$ ($A\subset X$).

L'ensemble $A$ est **totalement borné** si pour tout $\epsilon>0$, il existe un nombre fini de points $x_1, \ldots, x_n \in X$ tels que $A\subset \cup_{i=1}^nB(x_i, \epsilon)$.

On dit que l'ensemble $A$ est **couvert** par un nombre fini de $\epsilon$-boules (boules ouvertes de rayon $\epsilon$).
```


```{admonition} Exemples

- Un ensemble totalement borné est borné.

- Si $A\subset X$ est totalement borné et $B\subset A$ alors $B$ est aussi totalement borné.

- Un ensemble fini est totalement borné.

- Dans $\mathbb R$ muni de la distance usuelle, un ensemble est totalement borné si, et seulement si, il est borné (voir plus loins dans cette section).
```

```{admonition} Proposition

Soient $(X, d)$ un espace métrique, et $A$ un sous-ensemble de $X$ ($A\subset X$).

L'ensemble $A$ est **totalement borné** si pour tout $\epsilon>0$, il existe un nombre fini de points $x_1, \ldots, x_n \in A$ tels que $A\subset \cup_{i=1}^nB(x_i, \epsilon)$.
```

```{admonition} Démonstration

Soient $(X, d)$ un espace métrique, et $A$ un sous-ensemble de $X$ ($A\subset X$).

L'ensemble $A$ est totalement borné, donc

Pour tout $\epsilon>0$, il existe un nombre fini de points $x_1, \ldots, x_n \in X$ tels que $A\subset \cup_{i=1}^nB(x_i, \epsilon)$.


Soit $\epsilon>0$

Premièrement, il existe un nombre fini de points $x_1, \ldots, x_n \in X$ tels que $A\subset \cup_{i=1}^nB(x_i, \dfrac{\epsilon}{2})$.

Deuxièmement, on peut supposer que $A\cap B(x_i, \dfrac{\epsilon}{2}) \neq \emptyset$ (sinon on prend juste les points pour lesquels l'intersection des boules avec $A$ est non vide).

Soient $y_1, \ldots, y_n$ tels que pour tout $i$ :$y_i \in A\cap B(x_i, \dfrac{\epsilon}{2})$

Pour tout $i$ nous avons $B(x_i, \dfrac{\epsilon}{2})\subset B(y_i, \epsilon)$ (inégalité triangulaire).

En fin $A\subset \cup_{i=1}^nB(x_i, \dfrac{\epsilon}{2})\subset  \cup_{i=1}^nB(y_i, \epsilon)$.

```



```{admonition} Proposition

Soient $(X, d)$ un espace métrique, et $A$ un sous-ensemble de $X$ ($A\subset X$).

L'ensemble $A$ est totalement borné si, et seulement si, pour tout $\epsilon>0$ il existe un nombre fini d'ensembles $A_1, \ldots, A_n \subset A$ avec pour tout $i$ de $\{1, \ldots, n\}: diam(A_i)<\epsilon$ tels que:

$$
A\subset \cup_{i=1}^n A_i
$$

```


```{admonition} Proposition

Soient $(X, d)$ un espace métrique, et $(a_n)$ une suite d'éléments de $X$. Soit $A= \{a_n, n\geq 0\}$. Alors :

- Si $(a_n)$ est de Cauchy alors $A$ est totalement borné.

- Si $A$ est totalement borné, alors la suite $(a_n)$ admet une suite extraite qui est de Cauchy (admis)

```

```{admonition} Démonstration

Soit $\epsilon>0$, puisque la suite $(a_n)$ est de Cauchy, donc il existe $N\in \mathbb N$ tel que pour tout $n, m \geq N+1, d(a_n, a_m)<\dfrac{\epsilon}{2}$

Donc $ diam(\{a_n, n\geq N+1\}) \leq \dfrac{\epsilon}{2} < \epsilon$

On pose $A_1=\{a_0\}, A_2=\{a_1\}, \ldots, A_{N+1}=\{a_{N}\}, A_{N+1}=\{a_n, n\geq N+1\}$

Alors $A = \cup_{i=1}^{N+1}A_i$ et chaque $A_i$ a un diamètre inferieur a $\epsilon$ (pourquoi?)

Donc $A$ est totalement borné.
```


```{admonition} Théorème

Un ensemble $A$ est totalement borné si, et seulement si, tout suite d'éléments de $A$ admet une sous-suite qui est de Cauchy.
```

```{admonition} Démonstration

-  Si $A$ est totalement borné :

Soit $(a_n)$ une suite d'éléments de $A$. Alors l'ensemble $\{a_n, n\geq 0\}$ qui est une partie de $A$ est totalement borné.

Donc la suite admet une sous-suite qui est de Cauchy.

- Soit $A$ une sous ensemble avec la propriété "toute suite d'éléments de $A$ admet une sous-suite qui est de Cauchy"

Si $A$ est fini alors $A$ est totalement borné.


Sinon :

Supposons (par absurde) que $A$ n'est pas totalement borné. Donc il existe un $\epsilon>0$ tel que ne peut pas être couvert par un nombre fini de sous-ensemble de diamètre inferieur a $\epsilon$.

Nous allons construire une suite qui n'admet pas une sous-suite qui est de Cauchy. Si cette suite est construite, nous avons donc une contradiction et $A$ est totalement borné.

Soit $a_0$ un élément de $A$ ($A$ est infini donc cet élément existe).

Il existe au moins un élément $a_1$ tel que $d(a_0, a_1)\geq\epsilon$ car sinon alors tous les éléments de $A$ seront dans la boule $B(a_0, \epsilon)$ donc $A$ est totalement borné.

Supposons que nous avons construit $a_0, a_1, \ldots, a_n$ tel que la distance entre chaque deux éléments est supérieure ou égale a $\epsilon$.

Nous avons $A\setminus \{a_0, a_1, \ldots, a_n\}$ est différent de l'ensemble vide (car sinon $A$ serait fini)
alors il existe au moins un élément $a_{n+1}$ tel que $d(a_{n+1}, a_i)\geq \epsilon$ pour tout $i \in \{1, \ldots, n\}$ car sinon alors il existe $i_0 \in \{1, \ldots, n\}$ tel que pour tout élément $x$ de $A\setminus \{a_0, a_1, \ldots, a_n\}$, $d(a_{i_0}, x)<\epsilon$. Donc $A\setminus \{a_0, a_1, \ldots, a_n\}$ est totalement borné et puisque $\{a_0, a_1, \ldots, a_n\}$ est fini donc il est totalement borné. La réunion de deux ensembles totalement borné et totalement borné (pourquoi ?) donc $A$ est totalement borné. D'où l'existence de $a_{n+1}$. Enfin, par récurrence, nous avons construit une suite $(a_n)_{n\geq 0}$ dont chaque deux éléments différents ont une distance supérieure à $\epsilon$. Donc elle n'admet aucune sous-suite de Cauchy.
```
```{admonition} Proposition
Toute partie de $\mathbb R$ bornée est totalement bornée.
```

```{admonition} Démonstration

Une partie de $\mathbb R$ est bornée si elle est incluse dans une intervalle de la forme $[-R, R]$ (pour quoi?)

Donc si nous montrons que les intervalles de la forme $[-R, R]$ sont totalement bornés alors toute partie incluse dans cet intervalle est aussi totalement bornée (pourquoi?), en particulier, toute partie bornée est bornée.


Soit $R>0$. Montrons que l'intervalle $[-R, R]$ est totalement borné.

Soit $\epsilon>0$:

Soit $k\in \mathbb N$ tel que $k\geq \dfrac{4R}{\epsilon}$.

On pose $A_1 = ]-R-\dfrac{\epsilon}{2}, - R[, A_2 = ]-R, - R+\dfrac{\epsilon}{2}[, A_3 = ]-R+\dfrac{\epsilon}{2}, - R+2\dfrac{\epsilon}{2}[,\ldots, ]-R+(k-1)\dfrac{\epsilon}{2}, - R+k\dfrac{\epsilon}{2}[$

Alors il est claire que  $ [-R, R] \subset \cup_{i=1}^{k+1}A_i$ et que $A_i = B(-2R+(2k-1)\dfrac{\epsilon}{2}$).
Par suite $[-R, R]$ est totalement borné
En fin, Toute partie de $\mathbb R$ bornée est totalement bornée.
```



Dans $\mathbb R$, l'axiome de la borne supérieure est équivalent au fait que toute suite réelle de Cauchy est convergente. L'axiome de la borne supérieure stipule que : Toute partie de $\mathbb R$ non vide majorée admet une borne supérieure. Pour bien définir cette borne nous allons définir la notion du majorant. 
Soit $A$ une partie de $\mathbb R$ et $m$ un élément de $\mathbb R$:

- On dit que $m$ est un majorant de $A$ dans $\mathbb R$ si: $\forall x \in A , x \leq m$.
- On dit que $A$ est majorée dans $\mathbb R$ si $A$ admet au moins un majorant dans $\mathbb R$, c'est à dire si: $\exists m \in \mathbb R, \forall x \in A , x \leq m$.

L’axiome de la borne supérieure affirme qu’une telle partie admet un majorant qui est le plus petit des majorant. Cet élément est unique et est note $sup(A)$. La borne supérieure est caractérisée par :

**Caractérisation 1**: C'est le plus petit des majorants : Soit $A$ une partie de $\mathbb R$ et $M$ un élément de $\mathbb R$, alors $M$ est la borne supérieure si :

- $\forall x \in A, x\leq M$;
- $\forall \epsilon>0, \exists x \in A, M-\epsilon < x$.

**Caractérisation 2 (Caractérisation séquentielle)**: 

- Soit $A$ une partie de $\mathbb R$ majoree. Alors il existe une suite $(a_n)_{n\in \mathbb N}$ d'éléments de $A$ telle que : $\lim_{n \to \infty}a_n = sup(A)$;

- Soit $A$ une partie de $\mathbb R$ et $M$ un élément de $\mathbb R$. Si : 
* $M$ est un majorant de $A$
*  il existe une suite $(a_n)_{n\in \mathbb N}$ d'elements de $A$ telle que : $\lim_{n \to \infty}a_n = M$

Alors $M=sup(A)$



## Espace complet


```{admonition} Définition
Un espace métrique $(X,d)$ est **complet** si tout suite d'éléments de $X$ qui est de Cauchy est convergente.
```

```{admonition} Exemple
- $\mathbb R$ muni de la distance associe a la valeur absolu est un espace métrique complet (pourquoi ?)

- $\mathbb R^n$ est complet (parce que $\mathbb R$ l'est).

- Soit $X$ un ensemble muni de la distance $d$ définie par $d(x,y)= 1$ si $x\neq y$ et $d(x,y)= 0$ si $x= y$. Alors $(X,d)$ est complet (pourquoi?).
- l'ensemble $]0, 1[$ muni de la distance associée a la valeur absolue n'est pas complet (pourquoi?).

```
```{admonition} proposition (Caractérisation séquentielle des fermés)

Soient $(X,d)$ un espace métrique et $F$ un sous-ensemble de $X$ ($F\subset X$). Alors $F$ est fermé si, et seulement si, toute suite convergente d'éléments de $F$ converge dans $F$.
```

```{admonition} Démonstration

- Supposons que $F$ est fermé :

Soit $(a_n)$ une suite d'éléments de $F$ et $l\in X$ tel que $a_n \longrightarrow l$. Montrons que $l\in F$.

Par absurde, si $l \in X\setminus F$. Puisque $X\setminus F$ est ouvert et contient $l$ donc la suite est incluse dans cet ouvert à partir d’un certain rang. Ce qui est absurde car tous les éléments de la suite sont dans $F$.

Alors $l\in F$.


- Supposons que toute suite convergente d'éléments de $F$ converge dans $F$:

Montrons que $F$ est fermé, ceci dit, montrons que $X\setminus F$ est ouvert.

Par absurde supposons que  $X\setminus F$ n'est pas ouvert. Donc $\exists x \in X\setminus F, \forall \epsilon>0 B(x, \epsilon)\cap F \neq \emptyset$. 

Cela veut dire que $\forall n>0 B(x, \dfrac{1}{n})\cap F \neq \emptyset$.

Nous allons construire une suite d'éléments de $F$ qui converge vers $x$.

Soit $x_0 \in F$ quelconque. 

Pour $n\geq 1$ $B(x, \dfrac{1}{n})\cap F \neq \emptyset$. Donc soit $x_n$ un élément de $B(x, \dfrac{1}{n})\cap F$ pour tout $n$ de $\mathbb N^{*}$.

$(x_n)_{n\in \mathbb N}$ est donc une suite d'éléments de $F$ qui verifie $d(x_n, x)\leq n$ pour tout $n$ de $\mathbb N^{*}$.

Donc la suite $d(x_n, x)$ tend vers 0. Par suite $(x_n)_{n\in \mathbb N}$ tend vers $x$. Mais, toute suite convergente d'éléments de $F$ converge dans $F$. Ceci dit $x\in F$ ce qui est absurde. 

Donc $X\setminus F$ est ouvert ou encore $F$ est fermé.


```

```{admonition} Théorème

Soient $(X,d)$ un espace métrique complet et $A$ un sous-ensemble de $X$ ($F\subset X$). Alors $(A,d)$ est complet si, et seulement si, $F$ est fermé.
```


```{admonition} Démonstration

- Supposons que $(A,d)$ est complet (donc toute suite de Cauchy d'éléments de $A$ est convergente dans $A$)

Montrons que $A$ est fermé. Nous allons utiliser la caractérisation séquentielle des fermés.

Soit $(a_n)$ une suite d'éléments de $A$ qui converge dans $X$. Donc $(a_n)$ est une suite de Cauchy dans $X$. Donc elle est aussi de Cauchy dans $A$, puisque $(A,d)$ est complet donc $(a_n)$ converge dans $A$. Et ça pour toute suite d'éléments de $A$, donc A est fermé.


- Supposons que $A$  est fermé ( toute suite d'éléments de $A$ convergente dans $X$ converge dans $A$).

Montrons que $(A,d)$ est complet. C’est-à-dire que toute suite de Cauchy de $A$ est convergente.


Soit $(a_n)$ une suite d'éléments de $A$  qui est de Cauchy. Donc $(a_n)$ est aussi une suite d'éléments de $X$. Puisque $(X,d)$ est complet donc $(a_n)$ est convergente. Puisque $A$ est fermé, donc $(a_n)$ converge dans $A$. Et ça pour toute suite de Cauchy d'éléments de $A$.

Donc $(A, d)$ est complet.

```

On peut maintenant dire que : **si un espace métrique $(X,d)$ est totalement borné et complet alors toute suite d'éléments de $(X, d)$ possède une valeur d'adhérence (ou encore de toute suite d'éléments de $X$ on peut extraire une sous-suite convergente)**.

```{admonition} Définition
Un espace métrique est dit compact s'il est totalement borné et complet.
```

```{admonition} Exemple

Les sous-ensembles compacts de $\mathbb R$ sont les fermés bornés.
```

```{admonition} Théorème
Un espace métrique $(X, d)$ est compact si, et seulement si, toute suite d'éléments de $(X, d)$ possède une valeur d'adhérence (ou encore de toute suite d'éléments de $X$ on peut extraire une sous-suite convergente)

```

```{admonition} Démonstration

$$
\left\{
\begin{aligned}
&\mbox{totalement borné}&\\ \\
&+& \\ \\
&\mbox{complet}&
\end{aligned}
\right\} \Leftrightarrow \left\{
\begin{aligned}
&\mbox{toute suite d'éléments de $X$ admet une sous-suite de Cauchy}&\\ \\
&+& \\ \\
&\mbox{toute suite de Cauchy est convergente}&
\end{aligned}
\right\}
$$

```

```{admonition} Corollaire
Soit $A$ un sous-ensemble d'un espace métrique $X$. Si $A$ est compact, alors $A$ est fermé. Si $X$ est compact et $A$ est fermé, alors $A$ est compact.
```



