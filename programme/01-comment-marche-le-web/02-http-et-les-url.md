# 01.2 — HTTP & les URL

- **Thème :** 01 — Comment marche le web
- **Prérequis :** 01.1 (client/serveur, requête/réponse)
- **Idée centrale :** HTTP est la **langue** du dialogue web ; l'URL en est l'**adresse**.

## 🎯 Objectifs

L'apprenant sait décomposer une URL, reconnaître les méthodes de base et lire un
code de statut pour comprendre ce que dit le serveur.

## 📚 Notions à connaître

- 🎯 **HTTP, c'est quoi.** Le protocole (l'ensemble de règles) qui structure la requête
  et la réponse entre client et serveur. « HyperText Transfer Protocol ».
- 🎯 **Anatomie d'une URL.** Savoir nommer les morceaux de
  `https://exemple.fr/blog/article?id=12#commentaires` :
  - **schéma** (`https`), **domaine** (`exemple.fr`), **chemin** (`/blog/article`),
  - **paramètres / query** (`?id=12`), **fragment / ancre** (`#commentaires`).
- 🎯 **GET vs POST.** GET = *je demande / je lis* (l'info passe dans l'URL) ;
  POST = *j'envoie / je modifie* (l'info passe dans le corps de la requête).
- 🎯 **Lire un code de statut.** Au moins : **200** (OK), **301/302** (redirection),
  **404** (page introuvable), **500** (erreur côté serveur). Savoir ce que chacun
  *signifie* et de quel côté est le problème.
- 📌 **Les en-têtes (headers).** Des métadonnées de la requête/réponse (type de
  contenu, langue, cache…). Savoir que ça existe et à quoi ça sert globalement.
- 📌 **HTTP vs HTTPS.** Le « S » = sécurisé (chiffré). Le détail vient en 01.5.
- 📖 *(culture)* **API & JSON.** Beaucoup d'échanges renvoient non pas une page mais des
  **données** au format **JSON** — la base des API (et du pont React ↔ WordPress).

## ✅ Critères de maîtrise

1. Donné une URL, **nommer chaque partie** (schéma, domaine, chemin, query, fragment).
2. Choisir **GET ou POST** sur un cas simple et **justifier** (lire une page vs envoyer
   un formulaire).
3. Donné un code (404, 500, 200, 301), **dire ce qu'il signifie** et **de quel côté**
   (client/serveur) regarder.

## ⚠️ Pièges courants

- Croire qu'un **404** est forcément « un bug du code » (souvent juste une mauvaise URL).
- Confondre **404** (introuvable, côté requête) et **500** (le serveur a planté).
- Mettre des données sensibles (mot de passe) dans l'URL d'un **GET** (visible, loggé).
- Oublier le `?` / `&` dans la query, ou confondre `?` (query) et `#` (fragment).

## 🔗 Ressources

- MDN — *Présentation de HTTP* : <https://developer.mozilla.org/fr/docs/Web/HTTP/Overview>
- MDN — *Codes de statut HTTP* : <https://developer.mozilla.org/fr/docs/Web/HTTP/Status>
- MDN — *Qu'est-ce qu'une URL ?* :
  <https://developer.mozilla.org/fr/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL>
