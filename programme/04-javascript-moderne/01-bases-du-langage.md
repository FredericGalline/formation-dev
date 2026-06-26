# 04.1 — Les bases du langage

- **Thème :** 04 — JavaScript moderne
- **Prérequis :** 01.3 (rôle de JS), 02 (éditeur, console)
- **Idée centrale :** avant tout le reste, les briques universelles de la
  programmation, version JavaScript : stocker des valeurs, décider, répéter, factoriser.

## 🎯 Objectifs

L'apprenant sait écrire des fonctions qui utilisent variables, conditions et boucles,
et exécuter du JavaScript dans le navigateur.

## 📚 Notions à connaître

- 🎯 **Où s'exécute JS et comment l'inclure.** Dans le navigateur (rappel 01.4), via
  `<script src="..." defer>`. La **console** (devtools) pour tester et afficher
  (`console.log`).
- 🎯 **Variables : `let` et `const`.** `const` par défaut (valeur qui ne sera pas
  réaffectée), `let` si elle change. **On n'utilise plus `var`.**
- 🎯 **Les types primitifs.** `string`, `number`, `boolean`, `null`, `undefined`. JS est
  à **typage dynamique** (le type suit la valeur).
- 🎯 **Les opérateurs.** Arithmétiques (`+ - * / %`), comparaison **`===` (strict) vs
  `==` (à éviter)**, logiques (`&& || !`).
- 🎯 **Les conditions.** `if/else`, l'opérateur ternaire `cond ? a : b`, `switch`.
- 🎯 **Les boucles.** `for`, `while`, et surtout **`for...of`** pour parcourir.
- 🎯 **Les fonctions.** Déclaration, **paramètres**, **`return`**. Une fonction = une
  responsabilité, un nom clair.
- 📌 **La portée (scope).** Variables visibles dans leur bloc `{ }`. `const` empêche la
  réaffectation, mais **un objet `const` reste modifiable**.
- 📖 *(culture)* coercition de types, valeurs « *falsy* » (`0`, `""`, `null`…).

## ✅ Critères de maîtrise

1. **Écrire une fonction** qui prend des paramètres, utilise une condition et/ou une
   boucle, et **retourne** un résultat.
2. Choisir **`const` ou `let`** à bon escient et l'expliquer.
3. Expliquer la différence **`===` vs `==`** et pourquoi on préfère le strict.

## ⚠️ Pièges courants

- Utiliser **`==`** (comparaison laxiste, coercition surprenante) au lieu de `===`.
- Croire que **`const` rend immuable** : non, il interdit juste la **réaffectation**.
- Utiliser **`var`** (legacy, portée piégeuse).
- Oublier le **`return`** et s'étonner que la fonction « ne renvoie rien ».

## 🔗 Ressources

- MDN — *Premiers pas en JavaScript* :
  <https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps>
- *JavaScript.info* (en, très pédagogique) : <https://javascript.info/>
