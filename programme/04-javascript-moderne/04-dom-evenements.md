# 04.4 — Le DOM & les événements

- **Thème :** 04 — JavaScript moderne
- **Prérequis :** 01.3 (le DOM), 03.1 (HTML), 04.1–04.3
- **Idée centrale :** rendre une page **vivante** : sélectionner des éléments, les
  modifier, et **réagir** aux actions de l'utilisateur. Comprendre ça « à la main »
  éclaire *pourquoi* React existe.

## 🎯 Objectifs

L'apprenant sait manipuler le DOM en JavaScript et réagir aux événements utilisateur.

## 📚 Notions à connaître

- 🎯 **Rappel : le DOM.** JS agit sur l'arbre de la page *après* son chargement
  (`defer` ou `DOMContentLoaded`).
- 🎯 **Sélectionner.** `document.querySelector('.carte')` (le premier),
  `querySelectorAll` (tous).
- 🎯 **Modifier.** `textContent` (texte sûr), `classList` (add/remove/toggle), attributs
  (`setAttribute`), `style`. **`innerHTML` avec prudence** (risque XSS avec des données
  non maîtrisées).
- 🎯 **Créer / insérer / supprimer.** `document.createElement`, `append`, `remove`.
- 🎯 **Les événements.** `element.addEventListener('click', handler)`. L'objet **`event`**,
  `event.target`, et **`event.preventDefault()`** (ex. empêcher l'envoi par défaut d'un
  formulaire).
- 📌 **Formulaires.** Récupérer les valeurs des champs, réagir au `submit`.
- 📌 **Propagation.** Le *bubbling* et la **délégation d'événements** (un seul écouteur
  sur un parent).
- 📖 *(culture)* coût des manipulations du DOM (reflow/repaint) → **pourquoi React gère
  le DOM à ta place** (pont vers le Thème 05).

## ✅ Critères de maîtrise

1. **Sélectionner et modifier** des éléments (texte, classes) en réponse à une action.
2. **Réagir à un clic et à un `submit`** avec `addEventListener` + `preventDefault`.
3. **Créer dynamiquement** des éléments (ex. afficher une liste à partir d'un tableau).

## ⚠️ Pièges courants

- **`innerHTML`** avec des données utilisateur → faille **XSS**.
- Oublier **`preventDefault`** sur un `submit` (la page se recharge).
- Manipuler le DOM **avant** qu'il soit prêt (script sans `defer`).
- Ajouter un écouteur **dans une boucle** sans réfléchir (préférer la délégation).

## 🔗 Ressources

- MDN — *Manipuler le DOM* :
  <https://developer.mozilla.org/fr/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents>
- MDN — *Les événements* :
  <https://developer.mozilla.org/fr/docs/Learn/JavaScript/Building_blocks/Events>
