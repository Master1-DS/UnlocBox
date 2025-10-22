# Rôle : Documentation, Relecture et Assurance Qualité

**Membre :**  KENFACK LEKANE FRANK 22T2847


Ma mission était de m'assurer de la qualité, de la clarté et de la reproductibilité du projet.

---

## 1. Recherche et Documentation

* **Facteur de Régularisation ($\lambda$) :** J'ai effectué des recherches complémentaires pour clarifier le rôle exact du facteur de régularisation $\lambda$. J'ai fourni une explication claire (utilisée dans les tutoriels) sur son rôle d'équilibre entre la fidélité aux données ($||Ax-y||$) et l'a priori sur la solution ($||x||_1$ ou $||x||_{TV}$).
* **Documentation des Formats :** J'ai rédigé les `README.md` pour chaque dossier de tutoriel, en expliquant le choix du format `.mlx` (Live Script) et les alternatives comme `.ipynb` (Jupyter) ou l'export PDF.

---

## 2. Relecture et Assurance Qualité (QA)

J'ai servi de "client test" pour l'ensemble du projet.

* **Relecture de la Présentation :** J'ai vérifié la cohérence de la présentation LaTeX, corrigé les fautes de frappe et vérifié que les équations mathématiques s'affichaient correctement.
* **Test des Tutoriels :**
    * J'ai exécuté les deux scripts `.mlx` dans un environnement MATLAB "propre" (sans chemin pré-configuré).
    * J'ai identifié le bug initial `Unrecognized function 'init_unlocbox'`, permettant au groupe d'ajouter la procédure `addpath`.
    * J'ai vérifié que le code était commenté et que les graphiques de résultats étaient lisibles et corrects.
