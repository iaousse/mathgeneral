# Solutions des Exercices F

## Solution de l'exercice 1

- L'ensemble des ouverts contenus dans $A$ est non vide puisqu'il contient l'ensemble vide. Soit $\mathcal{O}$ l'ensemble des ouverts contenus dans $A$. On définit $\mathring{A} = \bigcup_{U \in \mathcal{O}} U$. Montrons que $\mathring{A}$ est un ouvert contenu dans $A$ et que c'est le plus grand ouvert contenu dans $A$.

    - $\mathring{A} \subseteq A$ car tout ouvert $U \in \mathcal{O}$ est contenu dans $A$.
    - $\mathring{A}$ est un ouvert car c'est une union d'ouverts.
    - Si $V$ est un ouvert contenu dans $A$, alors $V \in \mathcal{O}$ et donc $V \subseteq \mathring{A}$.
    - L'unicité découle du fait que tout autre ouvert contenu dans $A$ doit être inclus dans $\mathring{A}$.
    
- L'ensemble des fermés contenant $A$ est non vide puisqu'il contient $X$. Soit $\mathcal{F}$ l'ensemble des fermés contenant $A$. On définit $\bar{A} = \bigcap_{F \in \mathcal{F}} F$. Montrons que $\bar{A}$ est un fermé contenant $A$ et que c'est le plus petit fermé contenant $A$.

    - $A \subseteq \bar{A}$ car tout fermé $F \in \mathcal{F}$ contient $A$.
    - $\bar{A}$ est un fermé car c'est une intersection de fermés.
    - Si $V$ est un fermé contenant $A$, alors $V \in \mathcal{F}$ et donc $\bar{A} \subseteq V$.
    - L'unicité découle du fait que tout autre fermé contenant $A$ doit contenir $\bar{A}$.

## Solution de l'exercice 2

1- Si $A$ est un ouvert, alors $\mathring{A} \subseteq A$. Par définition de l'intérieur, $A$ est inclus dans tout ouvert contenant $A$. Donc $A \subseteq \mathring{A}$ et donc $\mathring{A} = A$.

Réciproquement, si $\mathring{A} = A$, alors $A$ est un ouvert.

2- Si $A$ est un fermé, alors $\bar{A} \supseteq A$. Par définition de l'adhérence, $A$ est contenu dans tout fermé contenant $A$. Donc $\bar{A} \subseteq A$ et donc $\bar{A} = A$.

Réciproquement, si $\bar{A} = A$, alors $A$ est un fermé.


## Solution de l'exercice 3
deja fait durant la seance de td. Pour ceux qui n'ont pas assiste, consulter cette [video](https://www.google.com/search?q=montrer+que+les+norme+1%2C+2%2C+infini+sont+equivalentes&oq=montrer+que+les+norme+1%2C+2%2C+infini+sont+equivalentes&aqs=chrome..69i57.14881j0j7&sourceid=chrome&ie=UTF-8#fpstate=ive&vld=cid:3cc13405,vid:RwijQhUx7zc)


## Solution de l'exercice 4

Dans un espace vectoriel normé $(E, \mathcal N)$, on veut montrer que $B(x, r) = x + B(0, r) = x + rB(0, 1)$.
Dans l'exercice 4, les ensembles $B(x, r)$, $x + B(0, r)$ et $x + rB(0, 1)$ sont définis comme suit :

1. $B(x, r)$ est la boule ouverte centrée en $x$ et de rayon $r$. C'est l'ensemble des points $y$ de l'espace vectoriel normé $(E, \mathcal N)$ tels que la distance entre $x$ et $y$ (selon la norme $\mathcal N$) est strictement inférieure à $r$ :
   
	$$B(x, r) = \{y \in E \mid \|y - x\| < r\}$$

2. $x + B(0, r)$ est l'ensemble obtenu en ajoutant le vecteur $x$ à chaque élément de la boule ouverte centrée en $0$ et de rayon $r$. Cela revient à translater la boule ouverte $B(0, r)$ de sorte que son centre devienne $x$ :
   
	$$x + B(0, r) = \{x + y \mid y \in B(0, r)\}$$

3. $x + rB(0, 1)$ est l'ensemble obtenu en multipliant chaque élément de la boule ouverte centrée en $0$ et de rayon $1$ par le facteur $r$, puis en ajoutant le vecteur $x$. Cela revient à dilater la boule ouverte $B(0, 1)$ par un facteur $r$ et la translater de sorte que son centre devienne $x$ :

   $$x + rB(0, 1) = \{x + ry \mid y \in B(0, 1)\}$$

L'exercice demande de montrer que ces trois ensembles sont en réalité les mêmes, 
c'est-à-dire que $B(x, r) = x + B(0, r) = x + rB(0, 1)$.



Soit $y \in B(x, r)$. Alors, on a $\mathcal N(y - x) < r$. Posons $z = y - x$, on a donc $\mathcal N(z) < r$. Ceci signifie que $z \in B(0, r)$. Ainsi, $y = x + z \in x + B(0, r)$, et donc $B(x, r) \subseteq x + B(0, r)$.

Réciproquement, soit $y \in x + B(0, r)$. Alors, il existe $z \in B(0, r)$ tel que $y = x + z$. On a $\mathcal N(z) < r$, donc $\mathcal N(y - x) < r$, ce qui signifie que $y \in B(x, r)$. Ainsi, $x + B(0, r) \subseteq B(x, r)$.

Par conséquent, $B(x, r) = x + B(0, r)$.

De plus, soit $y \in B(0, r)$. Alors, $\mathcal N(y) < r$. Posons $z = \frac{1}{r} y$, on a donc $\mathcal N(z) < 1$. Ceci signifie que $z \in B(0, 1)$. Ainsi, $y = r z \in rB(0, 1)$, et donc $B(0, r) \subseteq rB(0, 1)$.

Réciproquement, soit $y \in rB(0, 1)$. Alors, il existe $z \in B(0, 1)$ tel que $y = r z$. On a $\mathcal N(z) < 1$, donc $\mathcal N(y) = \mathcal N(rz) = r \mathcal N(z) < r$, ce qui signifie que $y \in B(0, r)$. Ainsi, $rB(0, 1) \subseteq B(0, r)$.

Par conséquent, $B(0, r) = rB(0, 1)$.

En combinant les deux résultats, on obtient :

$$B(x, r) = x + B(0, r) = x + rB(0, 1)$$


## Solution de l'exercice 5

On doit montrer deux choses dans cet exercice :

1. Si $x_n \to x$ dans $(X, d)$, alors $d(x_n, y) \to d(x, y)$ pour tout $y \in X$.
2. Si $x_n \to x$ et $y_n \to y$, alors $d(x_n, y_n) \to d(x, y)$.

### Partie 1

On sait que $x_n \to x$ dans $(X, d)$. Donc, pour tout $\epsilon > 0$, il existe un entier $N$ tel que pour tout $n \geq N$, $d(x_n, x) < \epsilon$.

On veut montrer que $d(x_n, y) \to d(x, y)$ pour tout $y \in X$. Soit $y \in X$.

On utilise l'inégalité triangulaire : $|d(x_n, y) - d(x, y)| \leq d(x_n, x)$. Alors, pour tout $n \geq N$, on a :

$$|d(x_n, y) - d(x, y)| \leq d(x_n, x) < \epsilon$$

Donc, $d(x_n, y) \to d(x, y)$ pour tout $y \in X$.

### Partie 2

On sait que $x_n \to x$ et $y_n \to y$ dans $(X, d)$. Donc, pour tout $\epsilon > 0$, il existe des entiers $N_1$ et $N_2$ tels que pour tout $n \geq N_1$, $d(x_n, x) < \frac{\epsilon}{2}$ et pour tout $n \geq N_2$, $d(y_n, y) < \frac{\epsilon}{2}$.

On veut montrer que $d(x_n, y_n) \to d(x, y)$. On utilise à nouveau l'inégalité triangulaire :

$$|d(x_n, y_n) - d(x, y)| \leq |d(x_n, y_n) - d(x_n, y)| + |d(x_n, y) - d(x, y)|$$

On utilise encore l'inégalité triangulaire pour la première partie de la somme :

$$|d(x_n, y_n) - d(x_n, y)| \leq d(y_n, y)$$

Alors, pour tout $n \geq \max(N_1, N_2)$, on a :

$$|d(x_n, y_n) - d(x, y)| \leq d(x_n, x) + d(y_n, y) < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$

Donc, $d(x_n, y_n) \to d(x, y)$.


## Solution de l'exercice 6

On considère l'espace métrique $(X, d)$ avec $X = ]0, 1[$ et $d$ la distance usuelle (associée à la valeur absolue). On étudie la suite $(a_n)$ définie par $a_n = \dfrac{1}{n}$ pour tout $n \geq 1$.

### La suite est-elle bornée ?

Une suite est bornée si et seulement si elle admet une borne supérieure et une borne inférieure. Dans notre cas, pour tout $n \geq 1$, on a $0 < a_n = \dfrac{1}{n} < 1$. Donc, la suite $(a_n)$ est bornée.

### La suite est-elle de Cauchy ?

Une suite est de Cauchy si et seulement si, pour tout $\epsilon > 0$, il existe un entier $N$ tel que pour tous les entiers $p, q \geq N$, on a $d(a_p, a_q) < \epsilon$. Dans notre cas, la distance est la distance usuelle, donc $d(a_p, a_q) = |a_p - a_q| = \left|\dfrac{1}{p} - \dfrac{1}{q}\right|$.

Soit $\epsilon > 0$. On cherche un entier $N$ tel que pour tous les entiers $p, q \geq N$, on a $\left|\dfrac{1}{p} - \dfrac{1}{q}\right| < \epsilon$. Prenons $N = \left\lceil\dfrac{2}{\epsilon}\right\rceil$. Alors, pour tous les entiers $p, q \geq N$, on a :

$$\left|\dfrac{1}{p} - \dfrac{1}{q}\right| \leq \dfrac{1}{p} + \dfrac{1}{q} \leq \dfrac{1}{N} + \dfrac{1}{N} = \dfrac{2}{N} < \epsilon$$

Donc, la suite $(a_n)$ est de Cauchy.

### La suite est-elle convergente dans $X$ ?

On sait que la suite $(a_n)$ est de Cauchy et bornée. Comme la distance est la distance usuelle, on peut conclure que la suite $(a_n)$ est convergente dans $\mathbb{R}$.

Cependant, la limite de la suite $(a_n)$ dans $\mathbb{R}$ est 0, et $0 \notin X$. Donc, la suite $(a_n)$ n'est pas convergente dans $X$.


## Solution de l'exercice 7

Soit l'espace métrique $(\mathbb R^2, d)$ avec $d$ définie pour tout $X = (x_1, x_2), Y= (y_1, y_2) \in \mathbb R^2$ par $d(X, Y) = |x_1 - y_1| + |x_2 - y_2|$. 

### Vérifier que $d$ est bel est bien une distance sur $\mathbb R^2$

Pour montrer que $d$ est une distance sur $\mathbb{R}^2$, on doit vérifier les trois propriétés suivantes pour tous les points $X, Y, Z \in \mathbb{R}^2$ :

1. $d(X, Y) \geq 0$ et $d(X, Y) = 0 \Leftrightarrow X = Y$
2. $d(X, Y) = d(Y, X)$
3. $d(X, Z) \leq d(X, Y) + d(Y, Z)$ (inégalité triangulaire)

Alors

1. La somme des valeurs absolues est toujours non négative, donc $d(X, Y) \geq 0$. Si $d(X, Y) = 0$, alors $|x_1 - y_1| + |x_2 - y_2| = 0$, ce qui implique que $x_1 = y_1$ et $x_2 = y_2$, donc $X = Y$. Réciproquement, si $X = Y$, alors $d(X, Y) = |x_1 - x_1| + |x_2 - x_2| = 0$.

2. $d(X, Y) = |x_1 - y_1| + |x_2 - y_2| = |y_1 - x_1| + |y_2 - x_2| = d(Y, X)$.

3. $d(X, Z) = |x_1 - z_1| + |x_2 - z_2| \leq |x_1 - y_1| + |y_1 - z_1| + |x_2 - y_2| + |y_2 - z_2| = d(X, Y) + d(Y, Z)$.

Donc, $d$ est bien une distance sur $\mathbb R^2$.

### Considérons la suite $(u_n)_n$ d'éléments de $\mathbb R^2$ telle que pour tout $n \geq 1, u_n = (\dfrac{1}{n}, \dfrac{2n+1}{n+1})$

On veut montrer que $u_n \to (0, 2)$.

Pour montrer que la suite $(u_n)_n$ converge vers $(0, 2)$, on doit montrer que pour tout $\epsilon > 0$, il existe un entier $N$ tel que pour tout $n \geq N$, on ait $d(u_n, (0, 2)) < \epsilon$.

Soit $\epsilon > 0$. On a :

$$
d(u_n, (0, 2)) = | \frac{1}{n} - 0| + | \frac{2n+1}{n+1} - 2 | = | \frac{1}{n} | + | \frac{-1}{n+1} | = \frac{1}{n} + \frac{1}{n+1}
$$

On veut montrer que pour un $n$ suffisamment grand, cette expression est inférieure à $\epsilon$. Pour cela, on cherche $N$ tel que pour $n \geq N$ :

$$
\frac{1}{n} + \frac{1}{n+1} < \epsilon
$$

Comme $\frac{1}{n} \geq \frac{1}{n+1}$ pour tout $n \geq 1$, on a :

$$
\frac{1}{n} + \frac{1}{n+1} < 2 \cdot \frac{1}{n}
$$

Alors, on peut choisir $N$ tel que $2 \cdot \frac{1}{N} \leq \epsilon$. 
Par exemple, on peut prendre 
$N = \left\lceil \frac{2}{\epsilon} \right\rceil+1$, où $\lceil \cdot \rceil$ désigne la partie entiere.

Donc, pour tout $n \geq N$, on a :

$$
d(u_n, (0, 2)) = \frac{1}{n} + \frac{1}{n+1} < 2 \cdot \frac{1}{n} \leq 2 \cdot \frac{1}{N} \leq \epsilon
$$

Cela montre que la suite $(u_n)_n$ converge bien vers $(0, 2)$.


## Solution de l'exercice 8

Pour montrer que la suite $x_n \to l = (l_1, l_2)$ si, et seulement si, les suites réelles $a_n \to l_1$ et $b_n \to l_2$, on doit montrer que la convergence de la suite $x_n$ vers $l$ implique la convergence des suites $a_n$ vers $l_1$ et $b_n$ vers $l_2$, et vice versa.

(i) Supposons que $x_n \to l = (l_1, l_2)$. Alors, pour tout $\epsilon > 0$, il existe un entier $N$ tel que pour tout $n \geq N$,

$$
d(x_n, l) = |a_n - l_1| + |b_n - l_2| < \epsilon
$$

Si on prend $0 < \epsilon' = \frac{\epsilon}{2}$, on voit que pour $n \geq N$,

$$
|a_n - l_1| < \epsilon'
$$

Ceci montre que la suite $a_n$ converge vers $l_1$.

De manière similaire, en prenant également $0 < \epsilon'' = \frac{\epsilon}{2}$, on obtient que pour $n \geq N$,

$$
|b_n - l_2| < \epsilon''
$$

Ceci montre que la suite $b_n$ converge vers $l_2$.

(ii) Supposons maintenant que les suites $a_n \to l_1$ et $b_n \to l_2$. Pour tout $\epsilon > 0$, il existe un entier $N_1$ tel que pour tout $n \geq N_1$, 

$$
|a_n - l_1| < \frac{\epsilon}{2}
$$

De même, il existe un entier $N_2$ tel que pour tout $n \geq N_2$,

$$
|b_n - l_2| < \frac{\epsilon}{2}
$$

En prenant $N = \max(N_1, N_2)$, on a pour tout $n \geq N$,

$$
d(x_n, l) = |a_n - l_1| + |b_n - l_2| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon
$$

Ceci montre que la suite $x_n$ converge vers $l = (l_1, l_2)$.

Donc, on a montré que $x_n \to l = (l_1, l_2)$ si, et seulement si, les suites réelles $a_n \to l_1$ et $b_n \to l_2$.






