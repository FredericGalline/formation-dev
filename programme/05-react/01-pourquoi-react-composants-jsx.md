# 05.1 — Pourquoi React, composants & JSX

- **Thème :** 05 — React
- **Prérequis :** 04.3 (ES6+, modules), 04.4 (DOM)
- **Idée centrale :** au lieu de **manipuler** le DOM étape par étape (impératif), on
  **décrit** l'UI voulue (déclaratif) et React se charge de la refléter à l'écran.

## 🎯 Objectifs

L'apprenant comprend le problème que résout React, sait écrire un composant simple en
JSX et démarrer un projet.

## 📚 Notions à connaître

- 🎯 **Le problème.** Manipuler le DOM à la main (04.4) ne passe pas à l'échelle dès que
  l'UI se complexifie (états multiples, listes, synchronisation).
- 🎯 **L'idée de React : déclaratif.** On décrit *à quoi ressemble l'UI pour un état
  donné* ; React calcule et applique les changements du DOM à notre place.
- 🎯 **Le composant.** Une **fonction** qui retourne de l'UI. Réutilisable, nommée en
  **PascalCase** (`Carte`, `BoutonPrimaire`).
- 🎯 **JSX.** Écrire du « HTML dans le JavaScript ». Différences clés : `className` (pas
  `class`), expressions JS entre accolades `{ }`, attributs en camelCase.
- 🎯 **Un seul élément racine.** Un composant retourne un seul nœud → on enveloppe dans
  un **Fragment** `<> … </>` si besoin.
- 🎯 **Démarrer un projet.** Avec **Vite** (`npm create vite`), comprendre la structure
  (`main.jsx`, `App.jsx`) et lancer le serveur de dev.
- 📌 **Composer dès le départ.** Une UI = un **arbre de composants**.
- 📖 *(culture)* le **Virtual DOM**, la compilation du JSX, les alternatives (Vue,
  Svelte) — même idée déclarative.

## ✅ Critères de maîtrise

1. Expliquer **pourquoi React** (déclaratif vs manipulation manuelle du DOM).
2. **Écrire un composant** qui retourne du JSX avec une expression `{ }`.
3. **Démarrer un projet** Vite et afficher son propre composant.

## ⚠️ Pièges courants

- Écrire **`class`** au lieu de **`className`** en JSX.
- Oublier l'**élément racine unique** (utiliser un Fragment).
- Nommer un composant en **minuscule** (React le prendrait pour une balise HTML).
- Vouloir **manipuler le DOM** à la main dans React (on décrit, on ne touche pas).

## 🔗 Ressources

- React — *Documentation officielle (apprendre)* : <https://fr.react.dev/learn>
- Vite — *Démarrage* : <https://vite.dev/guide/>
