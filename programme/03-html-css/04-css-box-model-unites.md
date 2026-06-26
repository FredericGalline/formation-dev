# 03.4 — CSS : le box model & les unités

- **Thème :** 03 — HTML & CSS
- **Prérequis :** 03.3
- **Idée centrale :** en CSS, **chaque élément est une boîte**. Comprendre comment cette
  boîte occupe l'espace (et avec quelles unités) est la clé de toute mise en page.

## 🎯 Objectifs

L'apprenant comprend le modèle de boîte, sait maîtriser les espacements et choisir la
bonne unité selon le besoin.

## 📚 Notions à connaître

- 🎯 **Le box model.** Quatre couches autour du contenu : **content** → **padding**
  (intérieur) → **border** → **margin** (extérieur). Savoir les distinguer (le padding
  est *dedans*, la margin *dehors*).
- 🎯 **`box-sizing: border-box`.** Par défaut, `width` ne compte que le contenu →
  surprises quand on ajoute padding/border. Avec `border-box`, la largeur inclut padding
  et border : on le met quasi systématiquement (`*{ box-sizing: border-box }`).
- 🎯 **`display`.** Notions de **block** (prend toute la largeur, s'empile), **inline**
  (au fil du texte), **inline-block**. (Flex/grid au chapitre suivant.)
- 🎯 **Les unités.** **`px`** (absolu), **`%`** (relatif au parent), **`em`** (relatif à
  la police de l'élément), **`rem`** (relatif à la racine — idéal pour des tailles
  cohérentes et accessibles). Savoir *quand* choisir laquelle.
- 📌 **Couleurs & typographie.** `hex` / `rgb` / `hsl` ; `font-family`, `font-size`,
  `line-height`, `font-weight`.
- 📌 **Margin collapsing.** Deux marges verticales adjacentes fusionnent (piège
  classique qui surprend les débutants).
- 📖 *(culture)* unités relatives au viewport (`vw`/`vh`), `ch`, `min()`/`max()`/`clamp()`.

## ✅ Critères de maîtrise

1. **Identifier et régler** content/padding/border/margin sur un élément, et expliquer
   l'effet de `box-sizing: border-box`.
2. **Choisir la bonne unité** (`rem` vs `px` vs `%`) selon le cas et le justifier.
3. Repérer et corriger un problème d'espacement courant (ex. *margin collapsing*).

## ⚠️ Pièges courants

- Confondre **padding** (intérieur) et **margin** (extérieur).
- Oublier **`border-box`** → largeurs qui « débordent » dès qu'on ajoute du padding.
- Tout en **`px`** → typographie peu accessible (préférer `rem` pour le texte).
- Être surpris par le **margin collapsing** sans le connaître.

## 🔗 Ressources

- MDN — *Le modèle de boîte* :
  <https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/The_box_model>
- MDN — *Valeurs et unités CSS* :
  <https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Values_and_units>
