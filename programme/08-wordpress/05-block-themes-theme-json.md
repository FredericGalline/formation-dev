# 08.5 — Block themes & `theme.json`

- **Thème :** 08 — WordPress
- **Prérequis :** 08.4, 03.6 (variables/design tokens)
- **Idée centrale :** le WordPress **moderne** : on compose **tout le site** avec des
  blocs (Full Site Editing), et on centralise le design dans **`theme.json`**.

## 🎯 Objectifs

L'apprenant comprend le fonctionnement d'un block theme et le rôle central de
`theme.json`.

## 📚 Notions à connaître

- 🎯 **Le Full Site Editing (FSE).** Éditer en-têtes, pieds de page, gabarits — **tout** —
  directement avec des blocs, depuis l'**éditeur de site**.
- 🎯 **`theme.json`.** Le fichier de **configuration centralisée** du thème : palette de
  couleurs, typographies, espacements, réglages des blocs. C'est l'équivalent WordPress
  des **design tokens** (lien direct 03.6).
- 🎯 **Templates & template parts.** Désormais en **HTML de blocs** (`templates/`,
  `parts/`) plutôt qu'en PHP.
- 🎯 **Les patterns.** Des **motifs** de blocs réutilisables (une section « héros », une
  grille de cartes) qu'on insère et adapte.
- 📌 **Variations de style.** Proposer plusieurs « thèmes » visuels via des variantes de
  `theme.json`.
- 📖 *(culture)* la cohabitation **thèmes classiques / block themes**, l'état de
  l'écosystème et la trajectoire de WordPress.

## ✅ Critères de maîtrise

1. Expliquer ce qu'est un **block theme** et le **FSE**.
2. **Lire un `theme.json`** : y repérer couleurs, typographies, espacements.
3. Faire le lien entre **`theme.json`** et la notion de **design tokens** (03.6).

## ⚠️ Pièges courants

- Chercher à tout faire en **PHP** comme en thème classique (le block theme raisonne en
  blocs et `theme.json`).
- Mettre des valeurs **en dur** dans le CSS au lieu de passer par `theme.json`.
- Confondre l'**éditeur de site** (block theme) et le **Customizer** (thème classique).
- Ignorer les **patterns**, et tout recomposer à la main à chaque fois.

## 🔗 Ressources

- WordPress — *Block Theme Handbook* :
  <https://developer.wordpress.org/themes/block-themes/>
- WordPress — *Global Settings & Styles (`theme.json`)* :
  <https://developer.wordpress.org/themes/global-settings-and-styles/>
