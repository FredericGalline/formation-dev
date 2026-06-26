# 08.10 — `theme.json` & variations de style (approfondi)

- **Thème :** 08 — WordPress *(approfondissement)*
- **Prérequis :** 08.5 (block themes, intro `theme.json`), 03.6 (design tokens)
- **Idée centrale :** `theme.json` pilote tout le design d'un block theme, et les
  **variations de style** (`/styles/*.json`) permettent d'en proposer des déclinaisons —
  **partielles** : elles ne reprennent **pas** tout `theme.json`, elles n'**overrident**
  que ce qu'elles déclarent.

## 🎯 Objectifs

L'apprenant maîtrise la structure de `theme.json`, la distinction *settings/styles*, et
sait créer une variation de style partielle.

## 📚 Notions à connaître

- 🎯 **La structure de `theme.json`.** Les sections clés : `version`, **`settings`**,
  **`styles`**, `customTemplates`, `templateParts`, `patterns`.
- 🎯 **`settings` vs `styles`.** `settings` = ce qui est **activé / proposé** (palette,
  échelles d'espacement, typographies, unités) ; `styles` = ce qui est **appliqué par
  défaut** (les valeurs réellement rendues). Distinction fondamentale.
- 🎯 **Styles par élément et par bloc.** `styles.elements` (lien, titre, bouton…) et
  `styles.blocks` (réglages spécifiques à un type de bloc).
- 🎯 **Les variations de style (`/styles/*.json`).** Des fichiers **partiels** : on n'y
  met **que** ce qu'on change (ex. une palette « sombre »), le reste est **hérité** de
  `theme.json`. Inutile (et déconseillé) de tout recopier.
- 🎯 **La cascade.** `theme.json` du core → `theme.json` du thème → **variation** choisie
  → styles **utilisateur** (réglages faits dans l'éditeur de site). Le plus spécifique
  l'emporte.
- 🎯 **Tokens & propriétés CSS.** `settings.custom` et la palette génèrent des **custom
  properties** CSS — le lien direct avec les design tokens (03.6).
- 📌 **CSS sur mesure.** `styles.css` (et par bloc) pour du CSS additionnel ;
  `appearanceTools` pour activer d'un coup un lot de réglages.
- 📌 **Variations au niveau d'un bloc.** Proposer des styles alternatifs pour un bloc donné.
- 📖 *(culture)* l'évolution du **schéma** `theme.json` (versions), l'outil *Create Block Theme*.

## ✅ Critères de maîtrise

1. **Lire un `theme.json`** et distinguer ce qui relève de `settings` (proposé) et de
   `styles` (appliqué).
2. **Créer une variation de style partielle** dans `/styles/` qui n'override que le nécessaire.
3. Expliquer la **cascade** et l'**héritage** entre `theme.json`, variations et styles utilisateur.

## ⚠️ Pièges courants

- **Recopier tout `theme.json`** dans une variation : c'est **partiel**, on ne met que les overrides.
- Confondre **`settings`** (ce qui est proposé/activé) et **`styles`** (ce qui est appliqué).
- Mettre du **CSS en dur** dans une feuille séparée alors que `theme.json` le gère (perte de cohérence).
- Oublier que les **styles utilisateur** (éditeur de site) priment sur le thème.

## 🔗 Ressources

- WordPress — *Global Settings & Styles (`theme.json`)* :
  <https://developer.wordpress.org/themes/global-settings-and-styles/>
- WordPress — *Style Variations* :
  <https://developer.wordpress.org/themes/global-settings-and-styles/style-variations/>
