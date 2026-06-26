# 07.1 — Qu'est-ce qu'une API & REST

- **Thème :** 07 — APIs & intégrations
- **Prérequis :** 01.2 (HTTP, URL, méthodes, statuts), 04.2 (JSON)
- **Idée centrale :** une API est un **contrat** qui permet à deux programmes d'échanger.
  Sur le web, le style dominant est **REST** : des **ressources** manipulées via les
  méthodes HTTP.

## 🎯 Objectifs

L'apprenant sait expliquer ce qu'est une API REST et faire correspondre une action à une
méthode HTTP et une URL.

## 📚 Notions à connaître

- 🎯 **C'est quoi une API.** *Application Programming Interface* : un point d'entrée
  défini par lequel un programme expose des fonctions/données à d'autres programmes.
- 🎯 **API web / REST.** Des **ressources** (ex. `articles`) identifiées par des **URL**,
  manipulées avec les méthodes HTTP : **GET** (lire), **POST** (créer), **PUT/PATCH**
  (modifier), **DELETE** (supprimer).
- 🎯 **Les conventions REST.** Ressources au pluriel (`/articles`), élément précis
  (`/articles/12`), pas de **verbe** dans l'URL (pas `/getArticles`). Les **codes de
  statut** (01.2) disent le résultat.
- 🎯 **Le format.** **JSON** la plupart du temps (échanger des données structurées,
  rappel 04.2).
- 🎯 **Sans état (*stateless*).** Chaque requête est autonome : le serveur ne « se
  souvient » pas de la précédente (l'identité passe par l'auth, 07.2).
- 📌 **Collections vs élément**, et **paramètres de requête** pour filtrer/trier/paginer
  (`/articles?categorie=news&tri=date`).
- 📌 **Idempotence.** `GET`, `PUT`, `DELETE` répétés donnent le même résultat ; `POST`
  non (crée à chaque fois). Notion utile pour les *retries* (07.3).
- 📖 *(culture)* SOAP (legacy), gRPC, panorama d'APIs publiques connues.

## ✅ Critères de maîtrise

1. Expliquer **avec ses mots** ce qu'est une API REST.
2. **Faire correspondre** une action CRUD à la bonne **méthode HTTP + URL**.
3. **Lire une réponse JSON** d'API et en extraire une information.

## ⚠️ Pièges courants

- Confondre **API** (interface pour programmes) et **site web** (pages pour humains).
- Mettre des **verbes dans les URLs** (`/createArticle`) au lieu d'utiliser les méthodes.
- Utiliser **`GET` pour modifier** des données (à réserver à la lecture).
- Croire qu'une API « garde » l'état entre deux appels (elle est *stateless*).

## 🔗 Ressources

- MDN — *Introduction aux API web côté client* :
  <https://developer.mozilla.org/fr/docs/Learn/JavaScript/Client-side_web_APIs/Introduction>
- *REST API Tutorial* (en) : <https://restfulapi.net/>
