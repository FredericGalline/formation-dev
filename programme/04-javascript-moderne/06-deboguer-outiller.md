# 04.6 — Déboguer & outiller son JS

- **Thème :** 04 — JavaScript moderne
- **Prérequis :** 04.1–04.5
- **Idée centrale :** savoir **trouver ses bugs** méthodiquement (devtools, points
  d'arrêt) et **écrire du code propre** (linter, formateur) vaut plus que connaître
  cent astuces. C'est ici qu'on approfondit les **devtools** entrevus en 01.3.

## 🎯 Objectifs

L'apprenant sait déboguer du JavaScript avec les outils du navigateur et comprend le
rôle des outils de qualité de code.

## 📚 Notions à connaître

- 🎯 **La console.** `console.log`, mais aussi `console.warn`, `console.error`,
  `console.table` (pratique pour les tableaux d'objets).
- 🎯 **Les devtools — onglet Sources.** Poser un **point d'arrêt** (breakpoint),
  exécuter **pas à pas**, **inspecter les variables** à un instant T. Bien plus puissant
  que semer des `console.log`.
- 🎯 **Lire une erreur.** Comprendre un message et sa **pile d'appels** (*stack trace*) :
  *quoi*, *où* (fichier:ligne), *dans quel enchaînement*.
- 🎯 **Une méthode de débogage.** Reproduire → isoler → formuler une hypothèse →
  vérifier. Pas de tâtonnement au hasard.
- 📌 **ESLint & Prettier.** **ESLint** repère erreurs et mauvaises pratiques ;
  **Prettier** formate automatiquement. *Pourquoi* : du code homogène, des bugs attrapés
  tôt, moins de débats de style.
- 📖 *(culture)* **TypeScript** : ajouter des **types** au JavaScript (autocomplétion,
  erreurs détectées avant l'exécution). À connaître : on en croise partout, y compris
  dans l'écosystème React. *(approfondi plus tard si besoin)*
- 📖 *(culture)* l'instruction `debugger`, les *source maps*.

## ✅ Critères de maîtrise

1. **Poser un breakpoint** et **inspecter une variable** dans les devtools.
2. **Lire une stack trace** pour localiser l'origine d'un bug.
3. Expliquer **le rôle d'ESLint et de Prettier** et la valeur de TypeScript.

## ⚠️ Pièges courants

- Déboguer **uniquement** au `console.log`, à l'aveugle, sans breakpoints.
- **Ignorer les warnings** du linter (souvent de vrais futurs bugs).
- Lire l'erreur en diagonale au lieu de **suivre la stack trace**.
- Confondre une erreur **côté navigateur** (console) et **côté réseau** (onglet Network).

## 🔗 Ressources

- MDN — *Gérer les erreurs JavaScript* (et devtools) :
  <https://developer.mozilla.org/fr/docs/Learn/JavaScript/First_steps/What_went_wrong>
- Chrome DevTools — *Déboguer le JavaScript* :
  <https://developer.chrome.com/docs/devtools/javascript>
