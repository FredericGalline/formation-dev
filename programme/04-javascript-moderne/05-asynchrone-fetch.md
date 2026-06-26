# 04.5 — L'asynchrone : promesses, `async/await` & `fetch`

- **Thème :** 04 — JavaScript moderne
- **Prérequis :** 01.2 (HTTP/JSON/API), 04.1–04.2
- **Idée centrale :** parler à un serveur prend du **temps**. L'asynchrone permet
  d'attendre une réponse **sans bloquer** la page. C'est le mécanisme exact qu'on
  utilisera pour connecter React à une API (et à WordPress).

## 🎯 Objectifs

L'apprenant sait faire un appel à une API REST, traiter la réponse JSON et gérer les
états de chargement et d'erreur.

## 📚 Notions à connaître

- 🎯 **C'est quoi l'asynchrone.** Certaines opérations (réseau, fichiers) prennent du
  temps ; on ne **bloque** pas le reste en les attendant.
- 🎯 **Les promesses.** Une valeur « à venir » : états *pending* → *resolved* / *rejected*,
  enchaînées par `.then()` / `.catch()`.
- 🎯 **`async` / `await`.** La syntaxe moderne et lisible : `await` met en pause jusqu'à
  la résolution, dans une fonction `async`.
- 🎯 **`fetch`.** Appeler une URL : `const res = await fetch(url); const data = await
  res.json();`. Lien direct avec HTTP (01.2).
- 🎯 **Gérer les états.** **chargement** (loading), **succès** (afficher les données),
  **erreur** (`try/catch` + vérifier **`res.ok`**). Ces trois états reviendront en React.
- 📌 **Vérifier la réponse.** `fetch` **ne rejette pas** sur un 404/500 : il faut tester
  `res.ok` / `res.status` soi-même.
- 📖 *(culture)* `Promise.all` (paralléliser), `AbortController` (annuler), CORS
  (pourquoi un appel est parfois bloqué), bibliothèques comme `axios`.

## ✅ Critères de maîtrise

1. **Appeler une API** avec `fetch` + `async/await` et **récupérer le JSON**.
2. **Gérer l'erreur** avec `try/catch` et vérifier **`res.ok`**.
3. Décrire et gérer les **trois états** : chargement, succès, erreur.

## ⚠️ Pièges courants

- **Oublier `await`** → on manipule une promesse au lieu de la donnée.
- Croire que **`fetch` lève une erreur sur un 404** (non : vérifier `res.ok`).
- Ne **pas gérer l'erreur** (réseau coupé, API en panne) → page cassée.
- Bloquer l'UI ou ignorer l'état de **chargement**.

## 🔗 Ressources

- MDN — *Utiliser fetch* :
  <https://developer.mozilla.org/fr/docs/Web/API/Fetch_API/Using_Fetch>
- MDN — *Les promesses* :
  <https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Using_promises>
