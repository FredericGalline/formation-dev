# 03.5 — CSS : la mise en page (Flexbox & Grid)

- **Thème :** 03 — HTML & CSS
- **Prérequis :** 03.4 (box model, display)
- **Idée centrale :** disposer les éléments dans la page. Deux outils modernes et
  complémentaires : **Flexbox** (une dimension) et **Grid** (deux dimensions), le tout
  en **responsive**.

## 🎯 Objectifs

L'apprenant sait construire des mises en page courantes avec Flexbox et Grid, et les
adapter aux différentes tailles d'écran.

## 📚 Notions à connaître

- 🎯 **Le problème de la mise en page.** Avant Flexbox/Grid, centrer ou aligner était
  pénible (floats, hacks). Aujourd'hui c'est natif et propre.
- 🎯 **Flexbox (une dimension).** Sur le conteneur : `display: flex`, `flex-direction`
  (row/column), `justify-content` (axe principal), `align-items` (axe secondaire),
  `gap`. Idéal pour une barre de nav, une rangée de cartes, centrer un élément.
- 🎯 **Grid (deux dimensions).** Sur le conteneur : `display: grid`,
  `grid-template-columns` (ex. `repeat(3, 1fr)`), `grid-template-rows`, `gap`. Idéal pour
  une grille de contenus, une mise en page de page entière.
- 🎯 **Flexbox ou Grid ?** Flexbox pour aligner *sur une ligne/colonne* ; Grid pour un
  *vrai quadrillage* lignes × colonnes. On les **combine** souvent.
- 🎯 **Le responsive.** **Media queries** (`@media (min-width: 48rem) { … }`) pour
  adapter le style selon la largeur. Approche **mobile-first** (on conçoit petit écran
  d'abord, puis on enrichit).
- 📌 **Médias responsives.** `img { max-width: 100%; }` pour que les images ne débordent
  pas.
- 📖 *(culture)* container queries (s'adapter au conteneur, pas à l'écran), anciennes
  techniques (float) pour comprendre le legacy.

## ✅ Critères de maîtrise

1. **Réaliser une mise en page avec Flexbox** (ex. une barre de navigation alignée,
   centrer un élément).
2. **Réaliser une grille avec Grid** (ex. 3 colonnes qui passent à 1 sur mobile).
3. **Rendre une page responsive** avec au moins une media query, en mobile-first.

## ⚠️ Pièges courants

- Confondre les **axes** en Flexbox (`justify-content` vs `align-items`).
- Utiliser des **marges** partout pour espacer alors que **`gap`** est fait pour ça.
- Penser « desktop d'abord » et galérer à réduire (préférer **mobile-first**).
- Choisir Grid là où Flexbox suffit (ou l'inverse) — connaître la bonne dimension.

## 🔗 Ressources

- MDN — *Flexbox* :
  <https://developer.mozilla.org/fr/docs/Learn/CSS/CSS_layout/Flexbox>
- MDN — *Grid* :
  <https://developer.mozilla.org/fr/docs/Learn/CSS/CSS_layout/Grids>
- Jeux pour pratiquer : *Flexbox Froggy* et *Grid Garden*.
