# 08.9 — Optimiser le chargement des assets (*enqueue* avancé)

- **Thème :** 08 — WordPress *(approfondissement)*
- **Prérequis :** 08.8 (`wp_enqueue_*`), 08.2 (hooks)
- **Idée centrale :** charger un script/style, ce n'est pas qu'« enqueue » : c'est le faire
  **au bon endroit, dans le bon ordre, sans bloquer le rendu, et seulement quand c'est
  utile**. C'est l'un des principaux leviers de performance d'un site WordPress.

## 🎯 Objectifs

L'apprenant sait charger les assets de façon optimisée et contextuelle, et retirer ceux
qui sont inutiles.

## 📚 Notions à connaître

- 🎯 **Les dépendances (`$deps`).** Déclarer ce dont un script a besoin pour garantir
  **l'ordre** de chargement (ex. un script qui dépend d'un autre).
- 🎯 **Le versioning (`$ver`).** Le numéro de version sert de **cache-busting** : sans
  lui (ou s'il ne change pas), le navigateur peut servir une **ancienne** version en
  cache après une modif.
- 🎯 **Ne pas bloquer le rendu.** Charger **en pied de page** (`in_footer`) et utiliser la
  **stratégie `defer`/`async`** (paramètre `strategy`, WP 6.3+) pour ne pas retarder
  l'affichage.
- 🎯 **Le chargement conditionnel.** **LE** point clé : ne charger un asset **que là où il
  sert** (`is_singular()`, `is_page()`, `has_block()`…). Charger tout partout est la
  cause n°1 de lenteur.
- 🎯 **Retirer l'inutile.** `wp_dequeue_script` / `wp_deregister_style` pour enlever des
  assets superflus injectés par WordPress ou un plugin.
- 📌 **Passer des données au JS.** `wp_localize_script` / `wp_add_inline_script` (ex.
  URL d'API, nonce — lien 08.7/08.12) plutôt que des données en dur.
- 📌 **Styles par bloc.** `wp_enqueue_block_style` : un style chargé **seulement si le
  bloc est présent** sur la page.
- 📌 **Modules de script.** `wp_enqueue_script_module` (WP 6.5+) pour de vrais **modules
  ES** (lien 04.3).
- 📖 *(culture)* bundling, *code splitting*, HTTP/2, l'impact sur les Core Web Vitals (08.11).

## ✅ Critères de maîtrise

1. **Enqueuer** un script avec **dépendances**, **version** et **`defer`**.
2. **Charger un asset conditionnellement** (seulement sur la bonne page / si le bloc est présent).
3. **Dequeuer** un asset inutile injecté par WP ou un plugin.

## ⚠️ Pièges courants

- **Tout charger partout** → poids et requêtes inutiles sur chaque page.
- Oublier le **versioning** → les utilisateurs gardent l'ancien fichier en cache.
- `defer` sur un script dont **dépend** un autre non encore chargé → erreur JS.
- Enqueuer sur le **mauvais hook** (trop tôt/tard) ou en dur dans le template.

## 🔗 Ressources

- WordPress — *Including CSS & JavaScript* :
  <https://developer.wordpress.org/themes/basics/including-css-javascript/>
- WordPress — `wp_enqueue_script` (paramètre `strategy`) :
  <https://developer.wordpress.org/reference/functions/wp_enqueue_script/>
