# Convergence

## Suites bornées, suites convergentes et suites de Cauchy 

Dans tout ce qui suit, toutes propriété valide pour un espace métrique $(X, d)$ est en particulier valide pour un espace vectoriel normé $(E,\mathcal N)$ considéré comme un espace métrique $(E,d)$ avec $\forall x,y \in E, d(x,y)=\mathcal N(x-y)$. Sauf pour une propriété relative à un espace vectoriel normé ou dans des exemples, nous allons considérer que les espaces métriques.

```{admonition} Définition (suite bornée)

Soient $(X, d)$ un espace métrique, et $(a_n)=(a_n)_{n \in \mathbb N}$ une suite d'éléments de $X$.
La suite $(a_n)$ est dite bornée si l'ensemble $\{a_0, \ldots\}$ est borné.
```


```{admonition} Définition (suite convergente)

Soient $(X, d)$ un espace métrique, et $(a_n)=(a_n)_{n \in \mathbb N}$ une suite d'éléments de $X$.
On dit que la suite $(a_n)$ converge (ou encore tend ) vers $l \in X$ lorsque $n$ tend vers $\infty$ si la suite $(d(a_n, l))$ est une suite réelle qui converge vers 0. 

```

Lorsque la suite $(a_n)$ converge vers $l $, on note $a_n \underset{n \to +\infty}{\overset{d}{\longrightarrow}}l$ ou $a_n \underset{n \to +\infty}{{\longrightarrow}}l$ si on ne doit pas spécifier la distance $d$ ou encore $a_n \longrightarrow l$.

```{admonition} Proposition

Les expressions suivantes sont équivalentes :

- la suite $(a_n)$ converge vers $l \in X$,
- $\forall \epsilon > 0, \exists N \geq 0, \forall n \geq N, d(a_n, l) <\epsilon$,
- $\forall \epsilon > 0, \exists N \geq 0$ l'ensemble $\{a_n, n \geq N\} \subset B(l, \epsilon)$,
- Pour toute boule ouverte de centre $l$, la suite est incluse dans cette boule à partir d'un certain rang.
- Pour tout ouvert contenant $l$, la suite est incluse dans cet ouvert à partir d'un certain rang.
- Pour tout voisinage de $l$, la suite est incluse dans ce voisinage à partir d'un certain rang.
```

```{admonition} Proposition

Si $a_n \longrightarrow l$ et $b_n \longrightarrow l'$ alors la suite réelle $(d(a_n, b_n))$ tend vers $d(l, l')$
```

```{admonition} Démonstration
:class: dropdown
Nous avons 

$$
\left | d(a_n, b_n) -  d(l, l') \right | \leq d(a_n, l) + d(b_n, l')
$$

Or, $a_n \longrightarrow l$ et $b_n \longrightarrow l'$ donc  $(d(a_n, l)) \longrightarrow 0$ et $(d(b_n, l')) \longrightarrow 0$. Donc $d(a_n, b_n) \longrightarrow  d(l, l')$
```

Dans un espace métrique les limites quand elles existent sont unique.

```{admonition} Proposition

Si $a_n \longrightarrow l$ et $a_n \longrightarrow l'$ alors  $l=l'$
```

```{admonition} Démonstration
:class: dropdown
Nous avons 
On utilise la proposition précédente (on pose $b_n=a_n$) 

la suite $(d(a_n, b_n))=(d(a_n, a_n))$ qui vaut 0 pour toute $n \in \mathbb N$ tend vers $d(l, l')$ donc $d(l, l')=0$.

```


```{admonition} Proposition

Si $a_n \longrightarrow l$ alors la suite $(a_n)$ est bornée.
```

```{admonition} Démonstration
:class: dropdown
Soit $\epsilon>0)$, alors il existe $N \geq 0$ tel que $\{a_n, n \geq N+1\} \subset \{a_n, n \geq N\} \subset B(l, \epsilon)$

D'autre part, soient $M_0 = d(a_0, l), M_1 = d(a_1, l), \ldots, M_{N} = d(a_N, l)$.

Posons $M= max\{M_0, M_1, \ldots, M_N, \epsilon \}$. Alors $\forall n \in \mathbb N, d(a_n,l)<M$. Donc $\{a_n, n \in \mathbb N\} \subset B(l, M)$.

La suite $(a_n)$ est bornée.

```



```{admonition} Définition
Soit $(a_n)_{n\geq 0}$ une suite d'un espace métrique $(X, d)$. La suite $(a_n)$ est dite une **suite de Cauchy** si:


$$
\forall \epsilon > 0 ~~ \exists N \in \mathbb N, ~~ \forall n, m \geq N, ~~ d(a_n, a_m) < \epsilon
$$


```

```{admonition} Proposition
Soient $E$ un espace vectoriel, $l\in E$, $\mathcal N_1, \mathcal N_2$ deux norme sur $X$, et $(a_n)$ une suite d'éléments de $E$. Si $\mathcal N_1$ et $\mathcal N_2$ sont équivalentes alors : $a_n \underset{n \to +\infty}{\overset{\mathcal N_1}{\longrightarrow}}l$ si, et seulement si, $a_n \underset{n \to +\infty}{\overset{\mathcal N_2}{\longrightarrow}}l$

```


```{admonition} Proposition
- Une suite qui converge est une suite de Cauchy.

- Une suite de Cauchy est bornée

```

```{admonition} Démonstration
:class: dropdown
- Soit $(a_n)$ une suite d'élément d'un espace métrique $(X,d)$ qui converge vers $l \in X$. 

Soit $\epsilon>0$.

Pour $\dfrac{\epsilon}{2}$, il existe $N\geq 0 $ , $\forall n \geq N$, $d(a_n, l)<\dfrac{\epsilon}{2}$


Soit $n, m \geq N$, donc nous avons $d(a_n, l)<\dfrac{\epsilon}{2}$ et $d(a_m, l)<\dfrac{\epsilon}{2}$

D'après l'inégalité triangulaire :  $d(a_n, a_m) \leq  d(a_n, l) +  d(a_m, l) < \epsilon$.

et ça pour tout $n, m \geq N$.
Par suite, pour tout $\epsilon > 0$, il existe $N \geq 0$, $\forall n, m \geq N, d(a_n, a_m) < \epsilon$.

Donc la suite $(a_n)$ est une suite de Cauchy.


- Soit $(a_n)$ une suite d'éléments d'un espace métrique $(X,d)$ qui est de Cauchy.

Donc 

$$
\forall \epsilon > 0 ~~ \exists N \in \mathbb N, ~~ \forall n, m \geq N, ~~ d(a_n, a_m) < \epsilon
$$

Soit $\epsilon>0$
Nous avons,

$$
\exists N \in \mathbb N^{*}, ~~ \forall n, m \geq N, ~~ d(a_n, a_m) < \epsilon
$$

 
Pour $m=N$ nous avons $\forall n\geq N, ~~ d(a_n, a_{N}) < \epsilon$

On pose $M = max(\epsilon, d(a_0, a_{N}), d(a_1, a_{N}), \dots, d(a_{N-1}, a_{N}))$

Donc $\forall n \in \mathbb N, d(a_n, a_N)<M$.

Les éléments de la suite appartiennent à la boule ouverte de centre $a_N$ et de rayon $M$.

Donc la suite est bornée.


```


## Suite extraite, valeur d'adhérence


```{admonition} Définition
Soit $(a_n)_{n\geq 0}$ une suite d'un espace métrique $(X, d)$. Une suite $(v_n)_{n\in \mathbb N}$ est appelée suite extraite, ou sous-suite, de  $(a_n)$ s'il existe une application $\varphi$ strictement croissante de $\mathbb N$ dans $\mathbb N$, vérifiant:

$$
\forall n \in \mathbb N, v_n = a_{\varphi(n)}
$$

```


```{admonition} Exemples

- La suite $(a_{n+1})_{n\in \mathbb N}$ est une suite extraite de la suite $(a_{n})_{n\in \mathbb N}$.

- Les suites $(a_{2n})_{n\in \mathbb N}$ et $(a_{2n+1})_{n\in \mathbb N}$ sont deux suites extraites de $(a_{n})_{n\in \mathbb N}$.

```

**Remarque**: si $\varphi$ est une application strictement croissante de $\mathbb N$ dans $\mathbb N$, on a $\forall n \in \mathbb N, \varphi(n)\geq n$ (récurrence).


```{admonition} Proposition
Soit $(a_n)_{n\geq 0}$ une suite d'un espace métrique $(X, d)$ qui converge vers $l \in X$. Si $(v_n)_{n\in \mathbb N}$ est une suite extraite de  $(a_n)$ alors $(v_n)$ converge vers $l\in X$.
```

```{admonition} Démonstration
:class:dropdown

Soit Soit $(a_n)_{n\geq 0}$ une suite d'un espace metrique $(X, d)$ converge vers $l \in X$. Soit $(v_n)_{n\in \mathbb N}$ est une suite extraite de  $(a_n)$.

Donc il existe $\varphi $ une application $\mathbb N $ dans $\mathbb N$ strictement croissante telle que : $v_n = a_{\varphi(n)}$ pour tout $n$ de $\mathbb N$.

Soit $\epsilon >0$

Donc il existe $N \in \mathbb N$ tel que pour tout $n \geq N, d(a_n, l)<\epsilon$

Puisque pour tout $n \in \mathbb N, \varphi(n)\geq n$ donc $d(a_{\varphi(n)}, l)>\epsilon$ pour tout $n \in mathbb N$.

Donc la suite $(v_n)=((a_{\varphi(n)})$ converge vers $l$.
```

```{admonition} Définition
Soit $(a_n)_{n\geq 0}$ une suite d'un espace métrique $(X, d)$. On dit que $l\in X$ est une valeur d'adhérence de la suite s'il existe une suite extraite de $(a_n)_{n\geq 0}$ qui converge vers $l$
```


```{admonition} Exemples

- la limite d'une suite convergente est une valeur d'adhérence de cette suite, en particulier, **c'est la seule valeur d'adhérence**. (Pourquoi ?)

- En considère $\mathbb R$ menu de la distance usuelle. Alors la suite $u_n = (-1)^n$ a deux valeurs d'adhérence : $-1$ et $1$.
```

```{admonition} Proposition
Soit $(a_n)_{n\geq 0}$ une suite  de Cauchy d'un espace métrique $(X, d)$. Si $(v_n)_{n\in \mathbb N}$ est une suite extraite de  $(a_n)$ qui converge vers $l\in X$, alors $(a_n)$  converge vers $l\in X$.

Autrementdit, une suite de Cauchy qui possède une valeur d'adherence est convergente.

```

```{admonition} Démonstration
:class: dropdown

Soit Soit $(a_n)_{n\geq 0}$ une suite  de Cauchy d'un espace metrique $(X, d)$ 


Pour tout $\epsilon >0$ il existe $N \in \mathbb N$ tel que pour tout $n, m \geq N, d(a_n, a_m)<\dfrac{\epsilon}{2}$

Soit $(v_n)$ une sous suite qui converge vers $l\in X$.

Donc il existe une application $\varphi $ de $\mathbb N$ dans $\mathbb N$ strictement croissante telle que: $v_n= a_{\varphi(n)}$ pour tout $n \in \mathbb N$.

D'autre part, puisque la sous suite est convergente vers $l$,  il existe $N_1 \in \mathbb N$ tel que pour tout $n \geq N_1, d(v_n,l)=d(a_{\varphi(n)},l) <\dfrac{\epsilon}{2}$

On pose, $N_2 = max(N, N_1)$.

Alors, 

$$
\forall n \geq N_2, d(a_n, l)\geq d(a_n, a_{\varphi(n)}) + d(a_{\varphi(n)},l )< \dfrac{\epsilon}{2} + \dfrac{\epsilon}{2} = \epsilon
$$


Puisque pour tout $n \in \mathbb N, \varphi(n)\geq n$ donc $d(a_{\varphi(n)}, l)>\epsilon$ pour tout $n \in \mathbb N$.

Donc la suite $(a_n)$ converge vers $l$.
```




