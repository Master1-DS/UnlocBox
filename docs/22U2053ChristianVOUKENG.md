# Rôle : Leader Présentation - Structure et Synthèse Technique

**Membre :** VOUKENG DJIOKENG CHRISTIAN ROUSSEL 22U2053

Ma responsabilité principale a été de diriger la création de la présentation, depuis l'analyse des documents sources jusqu'au développement technique de la structure LaTeX Beamer.

---

## 1. Analyse et Synthèse des Supports

J'ai analysé en profondeur les deux PDF (Guide Utilisateur et Papier arXiv) pour en extraire la structure logique de la présentation.

* **Extraction des Concepts :** Identification des concepts fondamentaux (Problème $min \sum f_n(x)$, Opérateur Proximal, *Proximal Splitting*) qui devaient former la colonne vertébrale de la présentation.
* **Définition de la Structure (Storyboarding) :** Conception du plan en 20 slides, en équilibrant la théorie (analyse convexe) et la pratique (syntaxe UNLocBoX).

## 2. Développement Technique (LaTeX Beamer)

J'ai mis en place l'environnement LaTeX Beamer et géré tous les aspects techniques et le débogage.

* **Configuration Initiale :** Choix et configuration du thème Beamer (`Madrid`), incluant la page de titre personnalisée (logo, faculté, département).
* **Débogage du Sommaire :** Résolution du problème du "sommaire vide" en ajoutant les commandes `\section{}` et en gérant le cycle de double compilation de LaTeX.
* **Correction de la Mise en Page :**
    * Résolution des avertissements `Overfull \vbox` (dépassement vertical) sur la page de titre en utilisant l'option `[shrink]`.
    * Nettoyage du pied de page pour supprimer les noms des auteurs sur chaque slide (via `\author[]{...}`).
* **Formatage du Code :** Intégration des exemples de code MATLAB (syntaxe `f1.grad = ...`) dans des environnements `verbatim` clairs.

## 3. Supervision et Coordination

* J'ai assuré la cohérence entre le contenu de la présentation et les tutoriels développés par les autres membres.
* J'ai rédigé le contenu des sections techniques fondamentales (Cas 1: Lisse, Cas 2: Non-Lisse, Cas 3: Contraintes).
