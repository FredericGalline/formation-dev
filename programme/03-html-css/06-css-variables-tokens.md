# 03.6 — CSS : variables & design tokens

- **Thème :** 03 — HTML & CSS
- **Prérequis :** 03.3, 03.4
- **Idée centrale :** centraliser ses valeurs (couleurs, espacements, polices) au lieu de
  les répéter partout. C'est la porte d'entrée vers la **cohérence** et les **design
  systems** — et un pont direct vers le travail en thème (WordPress, React).

## 🎯 Objectifs

L'apprenant sait utiliser les variables CSS pour centraliser ses styles et comprend le
concept de design tokens.

## 📚 Notions à connaître

- 🎯 **Les variables CSS (custom properties).** Déclarer `--couleur-primaire: #0b5;`
  (souvent sur `:root`), réutiliser avec `var(--couleur-primaire)`. Modifier une seule
  fois se répercute partout.
- 🎯 **La portée.** Une variable est héritée par les descendants ; on peut la
  **redéfinir** localement (utile pour des composants ou des thèmes).
- 🎯 **Pourquoi.** Éviter la répétition, garantir la **cohérence** (mêmes couleurs et
  espacements partout), faciliter les changements globaux.
- 🎯 **Le concept de design tokens.** Donner des **noms de sens** aux valeurs de design
  (`--espace-m`, `--rayon-bordure`, `--couleur-texte`) plutôt que des valeurs brutes
  éparpillées. C'est le vocabulaire partagé entre design et dev.
- 📌 **Thématisation.** Changer un thème (clair/sombre) en redéfinissant des variables
  (ex. via `prefers-color-scheme` ou une classe sur `<body>`).
- 📖 *(culture)* **SCSS / Sass** : ce que ça ajoute au CSS (variables de compilation,
  *nesting*, *mixins*, fonctions) et *pourquoi* — utile pour comprendre les projets
  existants. À mettre en regard des variables CSS natives, qui couvrent déjà beaucoup.
- 📖 *(culture)* **Tailwind / utility-first** et les **design systems** : autres façons
  d'industrialiser le style.

## ✅ Critères de maîtrise

1. **Définir et réutiliser des variables CSS** pour centraliser couleurs et espacements.
2. Expliquer **ce qu'est un design token** et l'intérêt de nommer par le sens.
3. Décrire en une phrase **ce que SCSS apporte** par rapport au CSS natif.

## ⚠️ Pièges courants

- Nommer une variable par sa **valeur** (`--bleu`) au lieu de son **rôle**
  (`--couleur-primaire`) → ingérable le jour où la couleur change.
- Confondre variables **CSS natives** (lues par le navigateur, dynamiques) et variables
  **SCSS** (résolues à la compilation, statiques).
- Croire qu'il *faut* SCSS : les variables CSS suffisent à beaucoup de projets.

## 🔗 Ressources

- MDN — *Les propriétés personnalisées (variables CSS)* :
  <https://developer.mozilla.org/fr/docs/Web/CSS/Using_CSS_custom_properties>
- Sass — *Documentation* (culture) : <https://sass-lang.com/documentation/>
