# Rôle : Création du Tutoriel 1 (LASSO)

**Membre :** KONZOU SODEA ALAN PEREC 22T2957

Ma contribution a été de développer le premier tutoriel sur l'analyse convexe, en se concentrant sur le problème LASSO, au format MATLAB Live Script (`.mlx`).

---

## 1. Analyse du Problème (LASSO)

J'ai modélisé le problème LASSO, qui vise à trouver une solution éparse :
$$x^* = \arg \min_x \frac{1}{2} ||Ax-y||_2^2 + \lambda ||x||_1$$

J'ai décomposé ce problème en deux fonctions convexes, comme requis par UNLocBoX :

1.  **Fonction Lisse ($f_1$) :** Le terme de fidélité aux données $f_1(x) = \frac{1}{2} ||Ax-y||_2^2$.
2.  **Fonction Non-Lisse ($f_2$) :** Le terme de régularisation (parcimonie) $f_2(x) = \lambda ||x||_1$.

---

## 2. Implémentation du Live Script (`.mlx`)

J'ai créé le fichier `Tutoriel_1_LASSO.mlx` en alternant texte explicatif et code exécutable.

* **Génération des données :** Création d'un signal `x_vrai` épars, d'une matrice de mesure `A` et d'un vecteur de mesures bruitées `y`.
* **Implémentation de $f_1$ :** Définition de la structure `f1` en fournissant :
    * `f1.grad` : Le gradient $\nabla f_1(x) = A^T (Ax - y)$.
    * `f1.beta` : La constante de Lipschitz du gradient.
* **Implémentation de $f_2$ :** Définition de la structure `f2` en fournissant :
    * `f2.prox` : L'opérateur proximal, en utilisant le `prox_l1` fourni par la toolbox.
* **Résolution :** Appel au solveur principal `solvep(x0, {f1, f2}, param)` pour trouver la solution.
* **Visualisation :** Création d'un graphique (`stem`) comparant le signal original `x_vrai` et la solution `x_solution` retrouvée.
