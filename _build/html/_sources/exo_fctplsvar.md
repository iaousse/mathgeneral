# Exercices 

## Exercice 1

Montrer que si $x_n \to x$ dans $(X, d)$ alors $d(x_n,y) \to d(x,y)$ pour tout $y\in X$. Généralement, si $x_n \to x$ et $y_n \to y$, montrer que $d(x_n,y_n) \to d(x,y)$.


## Exercice 2
Soit l'espace métrique $(X, d)$ avec $X =]0, 1[$ et $d$ la distance usuelle (associée à la valeur absolue).

On considère la suite $(a_n)$ définie par $a_n=\dfrac{1}{n}$ pour tout $n\geq 1$. La suite est-elle bornée ? Est-elle de Cauchy ? Est-elle convergente dans $X$?

## Exercice 3
Soit l'espace métrique $(\mathbb R^2, d)$ avec $d$ est définie pour tout $ X = (x_1, x_2), Y= (y_1, y_2) \in \mathbb R^2$ par $d(X, Y) = |x_1 - y_1| + |x_2 - y_2|$.

Vérifier que $d$ est bel est bien une distance sur $\mathbb R^2$.

Considérons la suite $(u_n)_n$ d'éléments de $\mathbb R^2$ telle que pour tout $n \geq 1, u_n = (\dfrac{1}{n}, \dfrac{2n+1}{n+1})$.

Montrer que $u_n \to (0, 2)$

## Exercice 4
Soient $\mathcal C [0, 1]$ l'ensemble de fonctions continues sur $[0, 1]$, ainsi que $d_1$ et $d_\infty$ deux application définies par:

$$
\begin{aligned}
d_1 \colon \mathcal C [0, 1]\times \mathcal C [0, 1] &\to \mathbb R^+ \\
(f, g) &\mapsto d_1(f, g) = \int_0^1 |f(t)-g(t)| dt
\end{aligned}
$$

et

$$
\begin{aligned}
d_\infty \colon \mathcal C [0, 1]\times \mathcal C [0, 1] &\to \mathbb R^+ \\
(f, g) &\mapsto d_\infty(f, g) = \max\{|f(t)-g(t)|: t \in [0, 1]\}
\end{aligned}
$$

Vérifier que $d_1$ et $d_\infty$ sont des distances sur $\mathcal C [0, 1]$.

Soient $(f_n)_n$ une suite de fonctions continues sur $[0, 1]$ tel que pour tout $n\geq 0$ la fonction $f_n$ est définie par $f_n(t) = t^n$ pour $t\in [0, 1]$ et $f$ la fonction nulle ($f(t) = 0 $ pour tout $t\in [0,1]$). 

Montrer que $(f_n)_n$ converge vers $f$ avec la distance $d_1$  et ne converge pas vers $f$ avec la distance $d_\infty$.


## Exercice 5

Soit l'espace métrique $(\mathbb R^2, d)$ avec $d$ définie dans l'exercice 3. Soit $x_n = (a_n , b_n)$ une suite d'éléments de3 $\mathbb R^2$. Montrer que $x_n \to l=(l_1, l_2)$ si, et seulement si, les suites réelles $a_n \to l_1$ et $b_n \to l_2$.


## Exercice 6
Une fonction $f: X \to Y$ entre deux espace métriques est dite **isométrie** si $f$ préserve les distance: $\rho(f(x),f(y)) = d(x, y)$ pour tout $x, y \in X$. Montrer qu'une isométrie est continue.

Montrer que l'inclusion de $\mathbb R$ dans $\mathbb R^2$ definie par $ x \mapsto (x,0)$ est une isométrie. 

## Exercice 7

Montrer que toute application $f: \mathbb N \to \mathbb R$ est continue. Les deux espaces métriques sont munis de la distance associée a la valeur absolue.

## Exercice 8

Soit $f: \mathbb R \to \mathbb R$ une application continue. Montrer que $\{x\in \mathbb R: f(x)>0\}$ est un ouvert de $\mathbb R$ et que $\{x\in \mathbb R: f(x)=0\}$ est un fermé de $\mathbb R$.
