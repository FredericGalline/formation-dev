# 05.7 — Aller plus loin (hooks avancés, routing, écosystème)

- **Thème :** 05 — React
- **Prérequis :** 05.1 → 05.6
- **Idée centrale :** une fois les bases solides, connaître les **briques suivantes** et
  surtout **savoir qu'elles existent** et quand les sortir. Ce chapitre est surtout de la
  sensibilisation : on n'attend pas la maîtrise de tout.

## 🎯 Objectifs

L'apprenant connaît les hooks et outils courants au-delà des bases, et sait où aller
pour approfondir.

## 📚 Notions à connaître

- 📌 **`useContext`.** Partager une donnée (thème, utilisateur connecté) sans la faire
  descendre en props à travers tous les niveaux (résout le *prop drilling* de 05.2).
- 📌 **`useRef`.** Référencer un élément du DOM ou conserver une valeur **sans**
  déclencher de re-render.
- 📌 **`useMemo` / `useCallback`.** Mémoriser un calcul / une fonction pour **optimiser**
  — **seulement quand c'est mesuré et nécessaire** (ne pas sur-optimiser par défaut).
- 📌 **Le routing.** Avec **React Router** : naviguer entre « pages » dans une
  application monopage (SPA), liens et URL.
- 📌 **Custom hooks.** Extraire une logique réutilisable dans son propre hook
  (`useFetch`, `useToggle`).
- 📖 *(culture)* **Next.js** : framework React full-stack (rendu serveur, routing,
  API) — très répandu.
- 📖 *(culture)* **état global** (Redux, Zustand) pour les grosses apps ;
  **React Query / SWR** pour le *data fetching*.
- 📖 *(culture)* **tester** un composant (Testing Library) — relié au Thème 08.

## ✅ Critères de maîtrise

> Ce chapitre est volontairement en sensibilisation : on ne « bloque » pas dessus.

1. Expliquer **à quoi sert `useContext`** et le problème qu'il résout.
2. Décrire le rôle d'un **routeur** dans une SPA.
3. Savoir **citer** Next.js, un gestionnaire d'état global et un outil de data fetching,
   et dire *quand* on s'y intéresserait.

## ⚠️ Pièges courants

- **Sur-optimiser** avec `useMemo`/`useCallback` partout, sans mesure → complexité inutile.
- Dégainer un **état global** (Redux) pour un besoin que `useState`/`useContext` couvrent.
- Multiplier les **dépendances** (bibliothèques) avant d'en avoir vraiment besoin.

## 🔗 Ressources

- React — *Référence des hooks* : <https://fr.react.dev/reference/react>
- React Router : <https://reactrouter.com/>
- Next.js : <https://nextjs.org/docs>
