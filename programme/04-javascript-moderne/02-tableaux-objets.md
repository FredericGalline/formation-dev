# 04.2 — Tableaux & objets

- **Thème :** 04 — JavaScript moderne
- **Prérequis :** 04.1
- **Idée centrale :** la vraie vie, c'est manipuler des **données** : des listes
  (tableaux) et des fiches (objets). Savoir les transformer proprement est le cœur du
  métier — et exactement ce qu'on fera en boucle dans React.

## 🎯 Objectifs

L'apprenant sait manipuler des tableaux et des objets, et transformer un tableau de
données avec les méthodes modernes.

## 📚 Notions à connaître

- 🎯 **Les tableaux.** Création (`[]`), accès par **index** (à partir de 0), `.length`,
  ajout/retrait (`push`/`pop`).
- 🎯 **Parcourir.** `for...of` et `.forEach()` (pour un effet de bord).
- 🎯 **Les méthodes essentielles.**
  - **`.map()`** : transformer chaque élément → **nouveau** tableau.
  - **`.filter()`** : garder ceux qui passent un test.
  - **`.find()`** : trouver le premier qui correspond.
  - **`.reduce()`** : agréger en une valeur (somme, regroupement).
- 🎯 **Les objets.** Paires **clé/valeur**, accès `obj.cle` ou `obj["cle"]`, ajout/modif,
  méthodes.
- 🎯 **Le tableau d'objets.** Le format de données le plus courant (une liste de fiches).
  Le combiner avec `map`/`filter` est le geste de base.
- 📌 **JSON.** Le format texte d'échange (cf. 01.2) : `JSON.parse` (texte → objet),
  `JSON.stringify` (objet → texte).
- 📌 **Immutabilité.** Préférer **créer** un nouveau tableau/objet plutôt que **muter**
  l'existant (`map`/`filter`/spread) — réflexe essentiel pour React.
- 📖 *(culture)* `Map`/`Set`, `sort`, `some`/`every`, chaînage de méthodes.

## ✅ Critères de maîtrise

1. **Manipuler un tableau d'objets** : filtrer puis transformer avec `filter` + `map`.
2. **Accéder et modifier** les propriétés d'un objet.
3. Expliquer la différence **`map` (retourne un tableau) vs `forEach` (effet de bord)**.

## ⚠️ Pièges courants

- Confondre **`map`** (produit un nouveau tableau) et **`forEach`** (ne retourne rien).
- **Muter** un tableau pendant qu'on le parcourt.
- Oublier que les **index commencent à 0** (et `length - 1` pour le dernier).
- Modifier un objet/tableau « partagé » sans le vouloir (effets de bord).

## 🔗 Ressources

- MDN — *Les tableaux* :
  <https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Indexed_collections>
- MDN — `Array.prototype.map` :
  <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array/map>
