# Continuité

Dans la présente section, sauf indication contraire, $(X, d)$ et $(Y, \rho)$ sont deux espace métriques arbitraires et $f$ une application de $X$ dans $Y$.

## Applications continues

```{admonition} Définition

On dit que $f$ est continue en un point $x\in X$ si:

$\forall \epsilon>0, \exists \delta>0, \forall y \in X: d(x, y)<\delta \Rightarrow \rho(f(x), f(y))<\epsilon$

Le réel $\delta$ dépend de $f, x$  et $\epsilon$

```


Cette définition peut être reformulée de la façon suivante: $f$ est continue en $x$ si pour tout $\epsilon>0$, il existe un réel $\delta>0$ tel que $f(B^d(x, \delta)) \subset B^\rho(f(x), \epsilon)$ ou encore $B^d(x, \delta) \subset f^{-1}(B^\rho(f(x))$.

Si $f$ est continue en tous points de $X$, on dit que $f$ est continue sur $X$. Ou tout simplement $f$ est continue.

```{admonition} Théorème

Etant donnée une application $f : (X, d) \to (Y, \rho)$, les assertions suivantes sont équivalentes:

- $f$ est continue sur $X$
- Pour tout $x \in X$, si $(x_n)$ est une suite d'éléments de $X$ qui converge vers $x$. Alors la suite $f(x_n)$ (qui d'éléments de $Y$) converge vers $f(x)$ dans $Y$.
- Si $F$ est un fermé de $Y$, alors $f^{-1}(F)$ est fermé de $X$.
- Si $U$ est un ouvert de $Y$, alors $f^{-1}(U)$ est un ouvert de $X$.
```

```{admonition} Proposition

Soient $f : X \to Y$ et $g : Y \to M$ avec $X, Y, M$ sont des espaces métriques. Si $f$ est continue en $x\in X$ et $g$ est continue en $f(x)\in Y$, alors $g\circ f: X \to M$ est continue en $x\in X$.

```

```{admonition} Théorème

Soit $f : (X, d) \to (Y, \rho)$, une application continue. Si $K$ est un sous-ensemble compact de $X$, alors $f(K)$ est un compact de $Y$.
```
```{admonition} Corollaire
Soit $(X, d)$ compact. Si $f : (X, d) \to \mathbb R$ est continue, alors $f$ est bornée et atteint ses bornes.
```

```{admonition} Corollaire

Soient $a, b \in \mathbb R$. Si $f : [a, b] \to \mathbb R$ est continue, alors l'image de $f$ est un segment de la forme $[c, d]$ pour certain $c, d \in \mathbb R$.
```

```{admonition} Corollaire
Soit $(X, d)$ compact. Alors $\|f\|_\infty = \max_{t\in X} |f(t)|$ est norme sur $\mathcal C(X)$, l'espace vectoriel de fonctions a valeurs réelles continue sur $X$.
```
