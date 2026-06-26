# 05.5 — Les formulaires contrôlés

- **Thème :** 05 — React
- **Prérequis :** 05.3 (state), 03.2 (formulaires HTML)
- **Idée centrale :** en React, la **source de vérité** d'un champ, c'est le **state**.
  Le champ affiche le state, et chaque frappe met le state à jour : c'est un composant
  **contrôlé**.

## 🎯 Objectifs

L'apprenant sait construire un formulaire contrôlé, gérer plusieurs champs et traiter la
soumission.

## 📚 Notions à connaître

- 🎯 **Le champ contrôlé.** `value={valeur}` + `onChange={e => setValeur(e.target.value)}`
  : le state pilote l'affichage du champ, et inversement.
- 🎯 **Plusieurs champs.** Soit un `useState` par champ, soit un **objet de state** mis à
  jour par spread (`setForm({ ...form, email: e.target.value })`).
- 🎯 **La soumission.** `onSubmit` sur le `<form>` + **`e.preventDefault()`** (rappel
  04.4) pour ne pas recharger la page, puis traiter les données.
- 📌 **Validation simple.** Vérifier les valeurs avant l'envoi, afficher un message.
- 📌 **Accessibilité.** Conserver les bonnes pratiques HTML (label/for, types) vues en
  03.2.
- 📖 *(culture)* composants **non contrôlés** (`useRef`), bibliothèques de formulaires
  (**React Hook Form**) pour les cas complexes.

## ✅ Critères de maîtrise

1. **Construire un champ contrôlé** (state ↔ input) et afficher sa valeur en direct.
2. **Gérer un formulaire à plusieurs champs** et le **soumettre** (`preventDefault` +
   traitement).
3. Expliquer ce qu'est un **composant contrôlé** et pourquoi le state est la source de
   vérité.

## ⚠️ Pièges courants

- Mettre `value` **sans `onChange`** → champ « bloqué » (React le rend en lecture seule).
- **Muter** l'objet de state au lieu d'utiliser le spread.
- Oublier **`preventDefault`** sur le `submit` → la page se recharge.
- Mélanger contrôlé et non contrôlé (warning React « controlled/uncontrolled »).

## 🔗 Ressources

- React — *Réagir à la saisie avec un état* :
  <https://fr.react.dev/learn/reacting-to-input-with-state>
- React — `<input>` (composants contrôlés) :
  <https://fr.react.dev/reference/react-dom/components/input>
