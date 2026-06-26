# 07.2 — L'authentification des APIs

- **Thème :** 07 — APIs & intégrations
- **Prérequis :** 07.1, 01.5 (HTTPS), 06.4 (sécurité)
- **Idée centrale :** la plupart des APIs ne sont pas ouvertes à tous. **S'authentifier**,
  c'est prouver *qui appelle* pour obtenir l'accès — et le faire **sans exposer ses
  secrets**.

## 🎯 Objectifs

L'apprenant connaît les principaux modes d'authentification d'API et sait où placer un
secret en sécurité.

## 📚 Notions à connaître

- 🎯 **Pourquoi authentifier.** Identifier l'appelant, restreindre l'accès, mesurer
  l'usage, protéger les données.
- 🎯 **Les clés d'API.** Une chaîne secrète envoyée à chaque appel (souvent dans un
  **en-tête**). Simple, identifie une application.
- 🎯 **Tokens & JWT.** Un **jeton** obtenu après connexion, envoyé via l'en-tête
  `Authorization: Bearer <token>`. Le **JWT** encode des infos signées (qui, quoi,
  jusqu'à quand).
- 🎯 **OAuth 2.0 (notion).** **Déléguer** l'accès sans donner son mot de passe — le
  principe du « Se connecter avec Google ». À connaître dans les grandes lignes.
- 🎯 **Où mettre le secret.** Dans l'en-tête **`Authorization`**, **jamais** dans l'URL
  (loggée) ni dans du code **front public** (un secret vit **côté serveur**, lien 07.3).
- 🎯 **HTTPS obligatoire.** Sans chiffrement, un secret transite en clair (rappel 01.5).
- 📌 **Sessions vs tokens.** Cookie de session (état serveur) vs token autoportant.
- 📖 *(culture)* *refresh tokens*, *scopes* (permissions fines), expiration et rotation.

## ✅ Critères de maîtrise

1. **Ajouter une authentification** à un appel (clé d'API ou `Bearer` token dans
   l'en-tête).
2. Expliquer la différence entre **clé d'API** et **OAuth**.
3. Dire **où stocker un secret** et pourquoi jamais côté front public ni dans l'URL.

## ⚠️ Pièges courants

- Mettre une **clé/token en clair** dans le code front ou commité dans le dépôt.
- Passer le secret **dans l'URL** (`?api_key=…`) → visible et journalisé.
- Oublier **HTTPS** → secret interceptable.
- Confondre **authentification** (qui es-tu ?) et **autorisation** (as-tu le droit ?).

## 🔗 Ressources

- MDN — *Authentification HTTP* :
  <https://developer.mozilla.org/fr/docs/Web/HTTP/Authentication>
- *OAuth 2.0 — Introduction* (en) : <https://oauth.net/2/>
