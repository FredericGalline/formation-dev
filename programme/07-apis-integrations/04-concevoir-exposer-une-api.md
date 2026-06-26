# 07.4 — Concevoir & exposer sa propre API

- **Thème :** 07 — APIs & intégrations
- **Prérequis :** 07.1, 06.2 (serveur), 06.4 (sécurité)
- **Idée centrale :** passer de l'autre côté : **fournir** une API que d'autres
  consommeront. Une bonne API est **prévisible** — endpoints clairs, bons statuts,
  erreurs explicites, sécurisée.

## 🎯 Objectifs

L'apprenant sait concevoir un jeu d'endpoints REST cohérent pour une ressource et
répondre proprement.

## 📚 Notions à connaître

- 🎯 **Penser en ressources.** Modéliser le domaine (`articles`, `utilisateurs`) et
  définir les endpoints REST associés (collection + élément, 07.1).
- 🎯 **Méthodes & statuts justes.** `GET 200`, `POST 201` (créé), `400` (requête
  invalide), `401`/`403` (auth/droits), `404` (introuvable), `500` (erreur serveur). Ne
  pas tout renvoyer en `200`.
- 🎯 **Valider les entrées.** Vérifier et assainir **toute** donnée reçue (lien 06.4)
  avant de l'utiliser.
- 🎯 **Structurer les réponses.** Format cohérent pour les données **et** pour les
  **erreurs** (message clair, code), pour que le consommateur s'y retrouve.
- 🎯 **Le versioning.** Préfixer (`/v1/…`) pour faire évoluer l'API sans casser les
  clients existants.
- 🎯 **La sécurité.** Authentifier/autoriser (07.2), valider/échapper (06.4), limiter le
  débit.
- 📌 **CORS.** Pourquoi un front d'un **autre domaine** est bloqué par défaut, et comment
  l'API l'autorise explicitement.
- 📌 **Le pont WordPress.** WordPress permet d'**exposer ses propres endpoints** via son
  API REST *(approfondi au Thème 08)*.
- 📖 *(culture)* design-first, contrats, HATEOAS.

## ✅ Critères de maîtrise

1. **Concevoir les endpoints REST** (CRUD) d'une ressource avec les bonnes méthodes.
2. **Choisir les codes de statut** adaptés, y compris pour les erreurs.
3. Expliquer le **versioning** et le rôle de **CORS**.

## ⚠️ Pièges courants

- Des **verbes dans les URLs** au lieu d'endpoints orientés ressources.
- Tout renvoyer en **`200`**, même les erreurs → le client ne peut pas réagir.
- **Ne pas valider** les entrées (faille de sécurité, lien 06.4).
- Oublier **CORS** et bloquer son propre front sans comprendre pourquoi.

## 🔗 Ressources

- MDN — *CORS* :
  <https://developer.mozilla.org/fr/docs/Web/HTTP/CORS>
- *REST API Design Best Practices* (en) : <https://restfulapi.net/rest-api-design-tutorial-with-example/>
