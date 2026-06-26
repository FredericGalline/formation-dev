# 08.7 — L'API REST WordPress & le pont React

- **Thème :** 08 — WordPress
- **Prérequis :** 07 (APIs/REST), 05.6 (consommer une API en React), 08.3
- **Idée centrale :** WordPress expose **nativement** une API REST. C'est le **pont**
  entre le back WordPress et un front React — y compris en **headless**.

## 🎯 Objectifs

L'apprenant sait consommer l'API REST de WordPress depuis React et exposer ses propres
endpoints.

## 📚 Notions à connaître

- 🎯 **L'API REST native.** WordPress expose le contenu sous `/wp-json/wp/v2/…`
  (`/posts`, `/pages`, CPT exposés via `show_in_rest`, lien 08.3). Tout ce qu'on a vu en
  T07 s'applique.
- 🎯 **Consommer depuis React.** Récupérer des contenus WP avec `fetch` dans un
  `useEffect` (réutilise **exactement** 05.6 : chargement / succès / erreur).
- 🎯 **Exposer ses endpoints.** `register_rest_route` pour créer ses propres routes
  (lien conception d'API 07.4), avec un **`permission_callback`** pour la sécurité.
- 🎯 **L'authentification.** *Application Passwords* pour un accès externe ; **nonces**
  pour les requêtes d'un utilisateur **connecté** côté site (lien 08.8, 06.4).
- 🎯 **Le headless.** WordPress comme **back-office de contenu** (le CMS), un front
  **découplé** en React/Next consomme l'API. Avantages et limites.
- 📌 **Pagination & filtres.** L'API REST WP est paginée et filtrable (réflexes 07.3).
- 📖 *(culture)* **WPGraphQL**, l'écosystème headless (Faust, etc.) et ses compromis.

## ✅ Critères de maîtrise

1. **Consommer l'API REST WP** depuis un composant React (liste de contenus, 3 états).
2. **Déclarer un endpoint personnalisé** avec `register_rest_route` + `permission_callback`.
3. Expliquer ce qu'est un **WordPress headless** et quand c'est pertinent.

## ⚠️ Pièges courants

- CPT/méta **non exposés** (`show_in_rest` oublié) → invisibles dans l'API.
- Endpoint custom **sans `permission_callback`** → faille de sécurité.
- Ignorer la **pagination** de l'API → données tronquées (lien 07.3).
- Choisir le **headless par mode**, sans en peser les coûts (SEO, aperçu, complexité).

## 🔗 Ressources

- WordPress — *REST API Handbook* :
  <https://developer.wordpress.org/rest-api/>
- WordPress — *Adding Custom Endpoints* :
  <https://developer.wordpress.org/rest-api/extending-the-rest-api/adding-custom-endpoints/>
