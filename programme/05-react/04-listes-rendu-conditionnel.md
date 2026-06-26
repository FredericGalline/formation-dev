# 05.4 — Listes & rendu conditionnel

- **Thème :** 05 — React
- **Prérequis :** 05.3, 04.2 (`map`/`filter`)
- **Idée centrale :** afficher des **données dynamiques** : transformer un tableau en UI
  avec `map`, et n'afficher certaines parties que **sous condition**.

## 🎯 Objectifs

L'apprenant sait afficher une liste à partir d'un tableau et conditionner l'affichage.

## 📚 Notions à connaître

- 🎯 **Afficher une liste.** `tableau.map(item => <Carte ... />)` directement dans le JSX
  (réutilise tout ce qui a été vu en 04.2).
- 🎯 **La prop `key`.** Chaque élément d'une liste a besoin d'une **`key` unique et
  stable** (un identifiant métier de préférence). React s'en sert pour suivre les
  éléments efficacement.
- 🎯 **Le rendu conditionnel.** `{condition && <X />}` (afficher si vrai), ternaire
  `{cond ? <A/> : <B/>}`, ou *early return*.
- 🎯 **Les états d'affichage.** Gérer le cas **liste vide**, et plus tard les états
  *chargement* / *erreur* (05.6).
- 📌 **Combiner.** `filter` puis `map` pour afficher une sous-liste.
- 📖 *(culture)* coût des grandes listes, **virtualisation** (n'afficher que le visible).

## ✅ Critères de maîtrise

1. **Afficher une liste** d'éléments à partir d'un tableau d'objets avec `map` et une
   **`key`** correcte.
2. **Conditionner** l'affichage d'un élément (`&&` ou ternaire).
3. Gérer proprement le cas **liste vide**.

## ⚠️ Pièges courants

- **Oublier la `key`** (warning React, bugs d'affichage subtils).
- Utiliser l'**index du tableau comme `key`** quand la liste peut changer d'ordre
  (préférer un identifiant stable).
- Mettre une **logique complexe** directement dans le JSX (extraire dans une variable
  ou une fonction).
- Rendre `{0 && <X/>}` et voir un `0` s'afficher (piège des valeurs *falsy*).

## 🔗 Ressources

- React — *Afficher des listes* : <https://fr.react.dev/learn/rendering-lists>
- React — *Affichage conditionnel* :
  <https://fr.react.dev/learn/conditional-rendering>
