# 07.5 — Documentation, webhooks & GraphQL

- **Thème :** 07 — APIs & intégrations
- **Prérequis :** 07.1 → 07.4
- **Idée centrale :** trois ouvertures qui complètent la maîtrise des APIs : **documenter**
  (le contrat lisible), **être notifié** (webhooks), et **élargir l'horizon** (GraphQL).

## 🎯 Objectifs

L'apprenant sait lire une documentation d'API, comprend le principe des webhooks et
situe GraphQL par rapport à REST.

## 📚 Notions à connaître

- 🎯 **Documenter une API.** Une API sans doc est inutilisable. **OpenAPI** (anciennement
  Swagger) décrit endpoints, paramètres et réponses de façon standardisée ; **Swagger
  UI** permet de l'explorer et de la tester.
- 🎯 **Les webhooks.** L'inverse de l'appel classique : au lieu d'**interroger** sans
  cesse (*polling*), c'est l'API qui **t'appelle** (envoie une requête à *ton* URL) quand
  un événement survient (paiement reçu, commit poussé…).
- 📌 **Tester/explorer.** Postman, Insomnia, ou Swagger UI pour essayer une API sans
  écrire de code.
- 📌 **Polling vs webhook.** Quand l'un, quand l'autre (fréquence, fraîcheur, charge).
- 📖 *(culture)* **GraphQL** : un seul endpoint où **le client choisit les champs** qu'il
  veut, évitant le sur/sous-chargement de REST. Utile pour des besoins de données
  complexes ; ne **remplace pas** REST partout.
- 📖 *(culture)* API gateways, quotas et observabilité côté fournisseur.

## ✅ Critères de maîtrise

1. **Lire une spécification OpenAPI/Swagger** et y repérer un endpoint et sa réponse.
2. Expliquer ce qu'est un **webhook** et quand le préférer au *polling*.
3. Dire en une phrase ce que **GraphQL** change par rapport à REST.

## ⚠️ Pièges courants

- Livrer une API **sans documentation** (inexploitable par les autres).
- Confondre **webhook** (l'API te notifie) et **polling** (tu interroges en boucle).
- Croire que **GraphQL remplace toujours REST** (chacun a ses cas).
- Exposer une URL de webhook **sans la sécuriser** (vérifier la signature de l'émetteur).

## 🔗 Ressources

- *OpenAPI / Swagger* : <https://swagger.io/docs/specification/about/>
- *GraphQL — Introduction* (en) : <https://graphql.org/learn/>
