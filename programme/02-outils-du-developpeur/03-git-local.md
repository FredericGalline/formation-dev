# 02.3 — Git : versionner son travail (en local)

- **Thème :** 02 — Outils du développeur
- **Prérequis :** 02.2 (terminal, fichiers)
- **Idée centrale :** Git, c'est la **machine à remonter le temps** du code. On ne perd
  plus jamais son travail, et on peut toujours revenir en arrière.

## 🎯 Objectifs

L'apprenant sait versionner un projet en local : enregistrer des étapes (commits)
propres et lire l'historique.

## 📚 Notions à connaître

- 🎯 **Pourquoi versionner.** Garder un **historique** des changements, revenir à un
  état antérieur, comprendre *qui a changé quoi et quand*. C'est le vrai « Enregistrer »
  du développeur.
- 🎯 **Le dépôt (repo).** Un dossier suivi par Git (`git init`). Git y enregistre des
  **instantanés** successifs du projet.
- 🎯 **Le cycle de base.** Modifier des fichiers → `git add` (préparer ce qu'on veut
  enregistrer, la *zone de staging*) → `git commit` (enregistrer l'instantané avec un
  message).
- 🎯 **Voir où on en est.** `git status` (quoi de modifié / préparé), `git log`
  (l'historique), `git diff` (ce qui a changé exactement).
- 🎯 **Le `.gitignore`.** Lister les fichiers à **ne pas** versionner : `node_modules/`,
  `vendor/`, fichiers de secrets, fichiers générés.
- 📌 **Un bon message de commit.** Court, clair, à l'impératif (« Ajoute le formulaire
  de contact »), une intention par commit.
- 📌 **Revenir en arrière.** Notions de `git restore <fichier>` (annuler des modifs non
  commitées) et consulter un ancien commit.
- 📖 *(culture)* à quoi sert vraiment la zone de staging, comment Git stocke les choses
  (objets, hash).

## ✅ Critères de maîtrise

1. **Initialiser** un dépôt et faire **2-3 commits** propres avec des messages clairs.
2. Lire l'état et l'historique : `git status`, `git log`, `git diff`.
3. **Créer un `.gitignore`** pertinent et expliquer pourquoi on ignore `node_modules`.

## ⚠️ Pièges courants

- Tout committer en bloc avec un message inutile (« maj », « fix »).
- **Committer des secrets** (mots de passe, clés) ou `node_modules/` → d'où le
  `.gitignore`.
- Confondre `add` (préparer) et `commit` (enregistrer).
- Croire qu'un commit envoie le code « en ligne » (non : c'est **local**, voir 02.4).

## 🔗 Ressources

- *Pro Git* (livre officiel, gratuit, en français) :
  <https://git-scm.com/book/fr/v2>
- MDN — *Git et GitHub* :
  <https://developer.mozilla.org/fr/docs/Learn/Tools_and_testing/GitHub>
