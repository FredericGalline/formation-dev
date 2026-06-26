# 07.3 — Consommer une API tierce robustement

- **Thème :** 07 — APIs & intégrations
- **Prérequis :** 07.1, 07.2, 04.5 (`fetch`/async)
- **Idée centrale :** appeler une API « quand tout va bien » est facile ; la
  **robustesse**, c'est gérer le réel : erreurs, grandes listes, limites de débit, et
  appeler **au bon endroit** (front ou serveur).

## 🎯 Objectifs

L'apprenant sait consommer une API tierce de façon fiable, en gérant erreurs,
pagination et limites.

## 📚 Notions à connaître

- 🎯 **Lire la doc et appeler.** Identifier l'URL, la méthode, les en-têtes (auth),
  les paramètres ; faire l'appel (rappel `fetch` 04.5, ou côté serveur en PHP).
- 🎯 **Gérer les erreurs.** Vérifier le **statut** (`res.ok`, 4xx/5xx), gérer les pannes
  réseau et les **timeouts**. Ne jamais supposer que ça marche.
- 🎯 **La pagination.** Les grandes listes arrivent **par pages** (`?page=2` ou curseur).
  Il faut **boucler** pour tout récupérer — sinon données tronquées.
- 🎯 **Les limites de débit (*rate limiting*).** Trop d'appels → **429 Too Many
  Requests**. Respecter les quotas, espacer (*backoff*), lire les en-têtes de quota.
- 🎯 **Où appeler.** Un appel nécessitant un **secret** se fait **côté serveur** (jamais
  exposer la clé au navigateur, lien 07.2). Le front appelle alors *ton* serveur.
- 📌 **Retries & idempotence.** Réessayer prudemment (uniquement les opérations
  idempotentes, 07.1) ; mettre en cache ce qui peut l'être.
- 📖 *(culture)* SDK/clients officiels, outils pour tester (**Postman**, **Insomnia**).

## ✅ Critères de maîtrise

1. **Consommer une API paginée** en récupérant l'ensemble des résultats.
2. **Gérer les erreurs** (statut, réseau) et réagir à un **429**.
3. Décider **où placer l'appel** (front vs serveur) selon la présence d'un secret.

## ⚠️ Pièges courants

- **Ignorer la pagination** → on ne traite que la première page sans s'en rendre compte.
- **Aucune gestion d'erreur** → l'app casse à la première panne d'API.
- **Exposer un secret** en appelant une API authentifiée depuis le front.
- **Marteler** l'API (boucle sans limite) → blocage pour dépassement de quota.

## 🔗 Ressources

- MDN — *Récupérer des données du serveur (fetch)* :
  <https://developer.mozilla.org/fr/docs/Learn/JavaScript/Client-side_web_APIs/Fetching_data>
- MDN — *429 Too Many Requests* :
  <https://developer.mozilla.org/fr/docs/Web/HTTP/Status/429>
