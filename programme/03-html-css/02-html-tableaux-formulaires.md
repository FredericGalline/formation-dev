# 03.2 — HTML : tableaux & formulaires

- **Thème :** 03 — HTML & CSS
- **Prérequis :** 03.1
- **Idée centrale :** deux briques HTML très concrètes et très utilisées : présenter des
  **données** (tableaux) et **collecter** des informations (formulaires) — proprement
  et de façon accessible.

## 🎯 Objectifs

L'apprenant sait construire un tableau de données correct et un formulaire accessible
avec des champs bien associés à leurs libellés.

## 📚 Notions à connaître

### Tableaux
- 🎯 **Quand utiliser un tableau.** Pour des **données tabulaires** (un planning, des
  prix), **jamais** pour faire de la mise en page (c'est le rôle du CSS).
- 🎯 **Structure d'un tableau.** `<table>`, `<thead>`/`<tbody>`, `<tr>` (ligne), `<th>`
  (cellule d'en-tête) vs `<td>` (cellule de données), `<caption>` (titre du tableau).
- 📌 **Accessibilité.** `scope="col"`/`scope="row"` sur les `<th>` pour lier en-têtes et
  cellules.

### Formulaires
- 🎯 **Le conteneur `<form>`.** Avec `action` (où envoyer) et `method` (`GET`/`POST`,
  cf. 01.2).
- 🎯 **`<label>` + `for`.** Chaque champ a un **label associé** (`<label for="email">`
  ↔ `<input id="email">`). Essentiel pour l'accessibilité et le confort (cliquer le
  label active le champ).
- 🎯 **Les types d'`<input>`.** `text`, `email`, `password`, `number`, `date`,
  `checkbox`, `radio`… Le bon type améliore la saisie (clavier mobile) et la validation.
- 🎯 **Les autres champs.** `<textarea>` (texte long), `<select>`/`<option>` (liste),
  `<button>` (`type="submit"` vs `type="button"`).
- 📌 **Validation native.** `required`, `min`/`max`, `pattern`, `type="email"` — le
  navigateur vérifie *avant* l'envoi, sans JavaScript.
- 📌 **Regrouper.** `<fieldset>` + `<legend>` pour regrouper des champs liés (ex. une
  adresse, un groupe de radios).
- 📖 *(culture)* ce que deviennent les données envoyées (traitement serveur, teaser du
  Thème 06).

## ✅ Critères de maîtrise

1. **Construire un tableau** de données correct (`thead`/`tbody`, `th` avec `scope`).
2. **Construire un formulaire** simple où **chaque champ a un `label` associé** et le
   **bon type** d'`input`.
3. Ajouter une **validation native** (`required`, `type="email"`) et l'expliquer.

## ⚠️ Pièges courants

- Utiliser un **tableau pour la mise en page** (vieille pratique, à bannir).
- Des **labels non associés** (ou pas de label du tout) → inaccessible.
- Mettre `id` en double entre champs → l'association `label/for` casse.
- Oublier `type="submit"` ou en mettre plusieurs sans le vouloir.

## 🔗 Ressources

- MDN — *Les tableaux HTML* :
  <https://developer.mozilla.org/fr/docs/Learn/HTML/Tables>
- MDN — *Les formulaires web* :
  <https://developer.mozilla.org/fr/docs/Learn/Forms>
