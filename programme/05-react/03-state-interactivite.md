# 05.3 — Le state & l'interactivité (`useState`)

- **Thème :** 05 — React
- **Prérequis :** 05.2, 04.2 (immutabilité)
- **Idée centrale :** le **state**, ce sont les données d'un composant qui **changent**
  dans le temps. Quand le state change, React **redessine** automatiquement l'UI.

## 🎯 Objectifs

L'apprenant sait gérer un état local avec `useState` et réagir aux événements
utilisateur.

## 📚 Notions à connaître

- 🎯 **C'est quoi le state.** Une donnée **interne** qui évolue (un compteur, un champ,
  une liste). À distinguer des props (qui viennent du parent).
- 🎯 **`useState`.** `const [valeur, setValeur] = useState(initiale);`. On **lit**
  `valeur`, on **met à jour** avec `setValeur(...)`.
- 🎯 **Le re-render.** Appeler `setValeur` déclenche un **nouveau rendu** du composant
  avec la nouvelle valeur. (On ne modifie jamais la variable directement.)
- 🎯 **Les événements en React.** `onClick`, `onChange`… en **camelCase**, recevant une
  **fonction** : `<button onClick={handleClick}>`.
- 🎯 **Ne jamais muter le state.** On crée une **nouvelle** valeur (spread, `map`,
  `filter`) au lieu de modifier l'existante (lien direct 04.2).
- 📌 **Mise à jour basée sur l'ancienne.** `setCount(prev => prev + 1)` quand la nouvelle
  valeur dépend de l'ancienne.
- 📌 **Lifting state up.** Remonter un state au **parent commun** quand plusieurs
  composants doivent le partager.
- 📖 *(culture)* les **règles des hooks** (appelés au top niveau, jamais dans une
  condition/boucle) et pourquoi.

## ✅ Critères de maîtrise

1. **Créer un compteur / un toggle** avec `useState` et un gestionnaire d'événement.
2. **Mettre à jour le state sans le muter** (ex. ajouter un élément à une liste).
3. Expliquer **state vs props** et ce qui déclenche un re-render.

## ⚠️ Pièges courants

- **Muter** le state (`state.push(...)`) au lieu de créer une nouvelle valeur → l'UI ne
  se met pas à jour.
- **Appeler** la fonction au lieu de la passer : `onClick={handleClick()}` (mauvais) vs
  `onClick={handleClick}` (bon).
- Lire une valeur **juste après** `setState` et la croire à jour (la mise à jour est
  asynchrone, visible au prochain rendu).
- Mettre un hook **dans une condition** (viole les règles des hooks).

## 🔗 Ressources

- React — *L'état : la mémoire d'un composant* :
  <https://fr.react.dev/learn/state-a-components-memory>
- React — *Réagir à des événements* :
  <https://fr.react.dev/learn/responding-to-events>
