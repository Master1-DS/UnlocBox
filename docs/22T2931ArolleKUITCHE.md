# Rôle : Création du Tutoriel 2 (Inpainting TV)

**Membre :**  KUITCHE AROLLE NACHARD 22T2931


J'ai développé le second tutoriel sur l'analyse convexe, portant sur la restauration d'image (Inpainting) par Variation Totale (TV), au format MATLAB Live Script (`.mlx`).

---

## 1. Analyse du Problème (Inpainting TV)

Le but est de reconstruire une image dont des pixels sont manquants, en utilisant un a priori de lissage par morceaux (contours préservés) :
$$x^* = \arg \min_x \frac{1}{2} ||A(x)-y||_2^2 + \lambda ||x||_{TV}$$

* **Fonction Lisse ($f_1$) :** Le terme de fidélité $f_1(x) = \frac{1}{2} ||A(x)-y||_2^2$, où $A$ est un opérateur de masquage.
* **Fonction Non-Lisse ($f_2$) :** Le terme de régularisation $f_2(x) = \lambda ||x||_{TV}$.

---

## 2. Implémentation du deuxième tutoriel en Live Script (`.mlx`)



* **Préparation des données :**
    * Chargement de l'image de test `cameraman.tif`.
    * Création d'un masque `mask` aléatoire pour simuler 50% de perte de pixels.
    * Création de l'image observée `y_observe`.
* **Implémentation de $f_1$ :** Définition de la structure `f1` avec son gradient $\nabla f_1(x) = A^T (A(x) - y)$.
* **Implémentation de $f_2$ :** Définition de la structure `f2` en utilisant le proximal `prox_tv` fourni par la toolbox.
* **Débogage Technique :**
    * Assistance au chef de projet pour résoudre les problèmes d'initialisation (`addpath(genpath(...))` pour Linux).
    * Résolution des erreurs de chemin pour le chargement de l'image `cameraman.tif`.
* **Visualisation :** Création d'une figure comparant l'image originale, l'image masquée et l'image restaurée par TV.
