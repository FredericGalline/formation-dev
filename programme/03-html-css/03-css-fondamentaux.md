# 03.3 — CSS : les fondamentaux

- **Thème :** 03 — HTML & CSS
- **Prérequis :** 03.1 (HTML, `id`/`class`)
- **Idée centrale :** le CSS applique du style au HTML via des **sélecteurs**. Comprendre
  *qui gagne* quand plusieurs règles s'appliquent (cascade & spécificité) évite 90 % des
  galères de débutant.

## 🎯 Objectifs

L'apprenant sait écrire des règles CSS, cibler les bons éléments, et comprendre
pourquoi une règle l'emporte sur une autre.

## 📚 Notions à connaître

- 🎯 **Attacher le CSS.** Feuille externe (`<link rel="stylesheet">`, **à privilégier**),
  `<style>` dans le head, ou `style="..."` inline (à éviter). Pourquoi externe : on
  sépare structure et présentation.
- 🎯 **Anatomie d'une règle.** `sélecteur { propriété: valeur; }`. Lire et écrire une
  déclaration.
- 🎯 **Les sélecteurs de base.** Par élément (`p`), par **classe** (`.carte`), par `id`
  (`#header`), descendant (`.carte p`), groupé (`h1, h2`).
- 🎯 **La cascade & l'héritage.** D'où vient le mot *Cascading* : plusieurs sources de
  styles se superposent ; certaines propriétés (couleur, police) **s'héritent** des
  parents.
- 🎯 **La spécificité.** Qui gagne en cas de conflit : `id` > `classe` > élément. Plus un
  sélecteur est « précis », plus il pèse lourd.
- 🎯 **`!important` est un piège.** Il force une règle et casse la cascade : à éviter,
  c'est presque toujours le signe d'un problème de spécificité mal géré.
- 🎯 **Nommer une classe.** Des noms **lisibles et orientés sens** (`.bouton-primaire`,
  pas `.rouge`). Introduction à **BEM** (`bloc__element--modificateur`). On **style par
  classe**, pas par `id` (réutilisable, spécificité maîtrisée).
- 📌 **Organisation.** Commentaires, regroupement logique, ordre de lecture d'une feuille.
- 📖 *(culture)* reset/normalize CSS, méthodologies (BEM, utility-first), couches `@layer`.

## ✅ Critères de maîtrise

1. **Cibler les bons éléments** avec des sélecteurs adaptés (classe, descendant, groupé).
2. **Expliquer quelle règle gagne** sur un conflit donné (cascade + spécificité).
3. **Nommer ses classes** de façon lisible et justifier *pourquoi styler par classe*
   plutôt que par `id`.

## ⚠️ Pièges courants

- Dégainer **`!important`** pour « forcer » au lieu de comprendre la spécificité.
- **Styler par `id`** → spécificité trop forte, non réutilisable.
- Des noms de classes liés à l'**apparence** (`.bleu`, `.gros`) au lieu du **sens**.
- Tout mettre en **inline** → impossible à maintenir.

## 🔗 Ressources

- MDN — *Les bases de CSS* :
  <https://developer.mozilla.org/fr/docs/Learn/CSS/First_steps>
- MDN — *La cascade et l'héritage* :
  <https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance>
