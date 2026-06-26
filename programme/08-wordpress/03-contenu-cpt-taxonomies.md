# 08.3 — Le contenu : posts, CPT & taxonomies

- **Thème :** 08 — WordPress
- **Prérequis :** 08.1, 08.2
- **Idée centrale :** WordPress structure le contenu en **types** (articles, pages, et
  des types **sur mesure**) et le **classe** avec des taxonomies. Bien modéliser son
  contenu, c'est la base d'un site maintenable.

## 🎯 Objectifs

L'apprenant sait modéliser du contenu avec des types personnalisés et des taxonomies.

## 📚 Notions à connaître

- 🎯 **Posts vs pages.** **Article** (post) : daté, classé, fait pour le flux
  (actualités) ; **page** : contenu statique hiérarchique (à propos, contact).
- 🎯 **Custom Post Types (CPT).** Créer ses propres types de contenu (`evenement`,
  `produit`, `bien_immobilier`) avec `register_post_type` (branché sur `init`, lien 08.2).
- 🎯 **Les taxonomies.** Classer le contenu : **catégories** et **étiquettes** natives,
  ou taxonomies **sur mesure** (`register_taxonomy`) — ex. « secteur », « ville ».
- 🎯 **Les champs personnalisés (méta).** Stocker des données supplémentaires sur un
  contenu (prix, date d'événement) via les **post meta**.
- 🎯 **`show_in_rest`.** Exposer un CPT/une méta à l'**API REST** et à l'**éditeur de
  blocs** — indispensable pour Gutenberg et le headless (lien 08.6, 08.7).
- 📌 **ACF (Advanced Custom Fields).** Outil très répandu pour gérer les champs
  personnalisés sans tout coder.
- 📖 *(culture)* métaboxes classiques, relations entre contenus.

## ✅ Critères de maîtrise

1. **Déclarer un CPT** et une **taxonomie** adaptés à un besoin donné.
2. Expliquer la différence **post / page / CPT** et **catégorie / étiquette / taxonomie
   custom**.
3. Dire pourquoi **`show_in_rest`** est important (éditeur de blocs, API, headless).

## ⚠️ Pièges courants

- Tout mettre dans des **pages** ou des **articles** au lieu de modéliser un **CPT**.
- Oublier `show_in_rest` → contenu invisible côté éditeur de blocs / API.
- Confondre **taxonomie** (classification) et **champ méta** (donnée d'un contenu).
- Déclarer un CPT **hors du hook `init`**.

## 🔗 Ressources

- WordPress — *Custom Post Types* :
  <https://developer.wordpress.org/plugins/post-types/>
- WordPress — *Taxonomies* :
  <https://developer.wordpress.org/plugins/taxonomies/>
