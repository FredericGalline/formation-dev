# 04.3 — JavaScript moderne (ES6+) & modules

- **Thème :** 04 — JavaScript moderne
- **Prérequis :** 04.1, 04.2
- **Idée centrale :** la syntaxe moderne (depuis ES6/2015) rend le code plus **court** et
  plus **clair**. C'est *exactement* le style qu'on lit et écrit en React.

## 🎯 Objectifs

L'apprenant sait lire et écrire du JavaScript moderne, et organiser son code en modules.

## 📚 Notions à connaître

- 🎯 **Les fonctions fléchées (arrow).** `const add = (a, b) => a + b;`. Syntaxe concise,
  omniprésente dans les callbacks (`map`, `filter`).
- 🎯 **Les *template literals*.** Chaînes en `` `backticks` `` avec interpolation
  `` `Bonjour ${nom}` `` et multi-lignes.
- 🎯 **La déstructuration.** Extraire des valeurs : `const { nom, age } = personne;`,
  `const [a, b] = tableau;`. Très utilisé pour les props en React.
- 🎯 **Spread / rest (`...`).** Copier/fusionner (`{ ...obj, x: 1 }`,
  `[...t1, ...t2]`), ou regrouper des arguments.
- 🎯 **Les modules.** `export` ce qu'un fichier expose, `import` ce dont on a besoin.
  C'est ainsi qu'on **découpe son code** en fichiers réutilisables.
- 📌 **Confort.** Paramètres par défaut, raccourci d'objet (`{ nom }`), **optional
  chaining** `obj?.prop`, **nullish** `valeur ?? defaut`.
- 📖 *(culture)* l'historique ES5 → ES6+, la **transpilation** (Babel), pourquoi les
  navigateurs ont rattrapé le retard.

## ✅ Critères de maîtrise

1. **Réécrire** un bout de code « ancien » en moderne (arrow, template literal,
   déstructuration).
2. **Découper** un programme en plusieurs fichiers avec `export` / `import`.
3. Utiliser **spread** pour copier/fusionner un objet ou un tableau sans le muter.

## ⚠️ Pièges courants

- Le **`this`** : différent entre fonction classique et arrow (à connaître tôt).
- **Chemins d'import** erronés (`./` vs nom de paquet) → module introuvable.
- Croire que **spread copie en profondeur** : c'est une copie **superficielle**
  (*shallow*).
- Surcharger le code de syntaxe « maligne » au détriment de la lisibilité.

## 🔗 Ressources

- MDN — *Les modules JavaScript* :
  <https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Modules>
- MDN — *Affectation par décomposition (destructuring)* :
  <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment>
