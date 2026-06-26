# 05.6 — Les effets & consommer une API (`useEffect`)

- **Thème :** 05 — React
- **Prérequis :** 05.3, 04.5 (`fetch`, async/await, 3 états)
- **Idée centrale :** brancher React sur le **monde extérieur** (une API). `useEffect`
  sert à exécuter du code **après** le rendu — typiquement, aller chercher des données.

## 🎯 Objectifs

L'apprenant sait charger des données depuis une API REST dans un composant et gérer les
états chargement / succès / erreur.

## 📚 Notions à connaître

- 🎯 **`useEffect`.** Exécuter un **effet de bord** (appel réseau, abonnement) après le
  rendu : `useEffect(() => { … }, [deps])`.
- 🎯 **Le tableau de dépendances.** `[]` = au **montage** seulement ; `[x]` = à chaque
  changement de `x`. Comprendre quand l'effet se relance.
- 🎯 **Charger des données.** Appeler `fetch` (04.5) dans l'effet, stocker le résultat
  dans un state, déclencher le rendu.
- 🎯 **Les trois états en React.** `loading`, `data`, `error` — exactement les trois
  états du 04.5, mais gérés en state et reflétés dans le JSX (05.4).
- 📌 **Le nettoyage (cleanup).** Retourner une fonction depuis l'effet pour annuler /
  se désabonner (éviter les fuites et les mises à jour après démontage).
- 📌 **Le pont WordPress.** Consommer l'**API REST de WordPress** depuis React est un cas
  concret central de la spécialité *(teaser du Thème 07)*.
- 📖 *(culture)* **React Query / SWR** : pourquoi on délègue souvent le *data fetching*
  (cache, revalidation) ; le double-appel d'effet en **Strict Mode** en dev.

## ✅ Critères de maîtrise

1. **Charger des données** d'une API dans un `useEffect` au montage et les afficher.
2. **Gérer les trois états** (chargement / succès / erreur) dans l'UI.
3. Expliquer le rôle du **tableau de dépendances**.

## ⚠️ Pièges courants

- **Oublier le tableau de dépendances** → effet à chaque rendu → boucle d'appels.
- Mettre des **dépendances incohérentes** (effet qui ne se relance pas / trop souvent).
- Ne pas gérer **l'erreur** ni le **chargement** (lien 04.5).
- `fetch` qui aboutit après le **démontage** du composant (d'où le cleanup).

## 🔗 Ressources

- React — *Synchroniser avec des effets* :
  <https://fr.react.dev/learn/synchronizing-with-effects>
- React — *Tu n'as peut-être pas besoin d'un effet* :
  <https://fr.react.dev/learn/you-might-not-need-an-effect>
