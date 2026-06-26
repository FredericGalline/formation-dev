# 08.6 — Développer un bloc Gutenberg

- **Thème :** 08 — WordPress
- **Prérequis :** 05 (React, JSX), 02.5 (npm), 08.5
- **Idée centrale :** créer ses **propres blocs** pour l'éditeur. Point clé : l'éditeur
  Gutenberg **est écrit en React** — tout ce qui a été appris au Thème 05 sert ici.

## 🎯 Objectifs

L'apprenant sait développer un bloc Gutenberg simple, statique et dynamique.

## 📚 Notions à connaître

- 🎯 **C'est quoi un bloc.** L'unité de contenu de l'éditeur (un paragraphe, une image,
  un bloc sur mesure). Un bloc a une **interface d'édition** et un **rendu**.
- 🎯 **`block.json`.** Le fichier de **métadonnées** du bloc (nom, attributs, supports,
  scripts) — la source de vérité, déclarée à WP via `register_block_type`.
- 🎯 **`edit` vs `save`.** `edit` = l'aperçu **dans l'éditeur** (en **React/JSX**, lien
  T05) ; `save` = le HTML **enregistré**. Pour un contenu calculé au chargement, on fait
  un **bloc dynamique** (rendu côté serveur via `render.php` / `render_callback`).
- 🎯 **Les attributs.** Les **données** du bloc (texte, choix, couleur), stockées et
  éditées via le state de l'éditeur (mêmes réflexes que `useState`, T05.3).
- 🎯 **Les *supports*.** Activer des fonctionnalités natives (couleurs, espacements,
  aligns) sans les recoder.
- 🎯 **L'outillage.** `@wordpress/scripts` et **`create-block`** pour démarrer et
  **compiler** le bloc (lien npm, T02.5).
- 📌 **Statique vs dynamique.** Statique = HTML figé dans `save` ; dynamique = HTML
  recalculé à l'affichage (contenu qui évolue).
- 📖 *(culture)* l'**Interactivity API** pour des blocs interactifs côté front, `viewScript`.

## ✅ Critères de maîtrise

1. **Créer un bloc simple** avec `create-block` et le déclarer (`block.json`).
2. Expliquer la différence **`edit` / `save`** et **statique / dynamique**.
3. Ajouter un **attribut** éditable au bloc et l'afficher.

## ⚠️ Pièges courants

- Modifier le `save` d'un bloc déjà utilisé sans gérer la **dépréciation** → « bloc
  invalide » dans l'éditeur.
- Vouloir du contenu **dynamique** dans un bloc **statique** (utiliser un rendu serveur).
- Oublier de **compiler** (`build`) après modification (lien T02.5).
- Coder l'éditeur sans réaliser que c'est du **React** (réutiliser T05).

## 🔗 Ressources

- WordPress — *Block Editor Handbook (créer un bloc)* :
  <https://developer.wordpress.org/block-editor/getting-started/>
- WordPress — *`block.json` Metadata* :
  <https://developer.wordpress.org/block-editor/reference-guides/block-api/block-metadata/>
