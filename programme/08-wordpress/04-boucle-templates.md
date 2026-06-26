# 08.4 — La Boucle & la hiérarchie de templates

- **Thème :** 08 — WordPress
- **Prérequis :** 08.1, 08.3, 06.1 (PHP)
- **Idée centrale :** comprendre comment un thème **classique** affiche le contenu : WP
  choisit un **template** selon la page demandée, et **la Boucle** y parcourt les contenus
  à afficher.

## 🎯 Objectifs

L'apprenant sait lire un thème classique : repérer le bon template et comprendre la
Boucle.

## 📚 Notions à connaître

- 🎯 **La Boucle (*the Loop*).** Le motif qui parcourt les contenus :
  `if (have_posts()) { while (have_posts()) { the_post(); … } }`. C'est là qu'on affiche
  titre, contenu, etc.
- 🎯 **La hiérarchie de templates.** WordPress choisit **automatiquement** le fichier à
  utiliser selon la page : `front-page.php`, `single.php` (un article), `page.php`,
  `archive.php`, `404.php`… avec `index.php` en dernier recours.
- 🎯 **Les *template tags*.** Fonctions qui affichent le contenu courant : `the_title()`,
  `the_content()`, `the_permalink()`…
- 🎯 **Les parties communes.** `get_header()`, `get_footer()`, `get_sidebar()`,
  `get_template_part()` pour réutiliser des morceaux.
- 📌 **`WP_Query`.** Faire des **requêtes personnalisées** (afficher une liste filtrée de
  contenus) — et bien `wp_reset_postdata()` après.
- 📖 *(culture)* la **transition** vers les *block themes* (08.5) : la Boucle existe
  toujours, mais l'assemblage des pages se fait de plus en plus avec des **blocs**.

## ✅ Critères de maîtrise

1. **Lire et expliquer la Boucle** d'un thème classique.
2. Donné une page (un article, une archive), **dire quel template** WordPress utilisera.
3. Utiliser les **template tags** de base pour afficher un contenu.

## ⚠️ Pièges courants

- Oublier `the_post()` dans la Boucle (le contenu courant n'avance pas).
- Mal nommer un template → WP retombe sur `index.php` sans qu'on comprenne pourquoi.
- Modifier la requête principale au lieu d'utiliser une **`WP_Query`** dédiée.
- Oublier `wp_reset_postdata()` après une boucle secondaire.

## 🔗 Ressources

- WordPress — *The Loop* :
  <https://developer.wordpress.org/themes/basics/the-loop/>
- WordPress — *Template Hierarchy* :
  <https://developer.wordpress.org/themes/basics/template-hierarchy/>
