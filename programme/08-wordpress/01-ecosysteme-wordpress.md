# 08.1 — L'écosystème WordPress

- **Thème :** 08 — WordPress
- **Prérequis :** 06 (PHP, BDD), 01.4 (côté serveur)
- **Idée centrale :** WordPress = un **noyau** (core) que l'on **étend** avec des **thèmes**
  (l'apparence) et des **plugins** (les fonctionnalités). On ne touche **jamais** au core.

## 🎯 Objectifs

L'apprenant comprend l'architecture de WordPress et sait où chaque chose se trouve.

## 📚 Notions à connaître

- 🎯 **Les trois couches.** **Core** (le moteur, à ne pas modifier) ; **thèmes**
  (l'apparence et les gabarits) ; **plugins** (les fonctionnalités ajoutées).
- 🎯 **Thème vs plugin.** Règle d'or : ce qui touche à l'**apparence** → thème ; ce qui
  est une **fonctionnalité** (qui devrait survivre à un changement de thème) → plugin.
- 🎯 **Front-office vs back-office.** Le site public vs l'administration (`/wp-admin`).
- 🎯 **Où vivent les choses.** `wp-content/themes/`, `wp-content/plugins/`,
  `wp-content/uploads/` ; le fichier de config `wp-config.php`.
- 🎯 **Le rôle de la base de données.** WordPress stocke **tout** le contenu et la config
  en base (rappel T06.5) ; les fichiers, eux, portent le code.
- 📌 **Un environnement local.** Installer WP en local (Docker, *Local*, etc.) pour
  développer sans risque.
- 📖 *(culture)* WordPress.org (auto-hébergé) vs WordPress.com (hébergé), la licence
  **GPL**, la part de marché du CMS.

## ✅ Critères de maîtrise

1. Expliquer la **séparation core / thème / plugin** et ce qui va où.
2. **Localiser** thèmes, plugins, uploads et `wp-config.php` dans l'arborescence.
3. Décider, pour une fonctionnalité donnée, si elle relève d'un **thème** ou d'un **plugin**.

## ⚠️ Pièges courants

- **Modifier le core** (mises à jour qui écrasent tout, faille de sécurité). Jamais.
- Mettre une **fonctionnalité** dans le thème → elle disparaît si on change de thème.
- Éditer directement en **production** via l'éditeur de l'admin (pas de versioning).
- Croire que le contenu est « dans les fichiers » (il est en **base de données**).

## 🔗 Ressources

- WordPress — *Developer Resources* : <https://developer.wordpress.org/>
- *WordPress Theme vs Plugin* (doc officielle développeur).
