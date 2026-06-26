# 02.4 — Git & GitHub : travailler à plusieurs

- **Thème :** 02 — Outils du développeur
- **Prérequis :** 02.3 (Git en local)
- **Idée centrale :** GitHub, c'est Git **partagé**. Plusieurs personnes travaillent sur
  le même projet sans se marcher dessus, grâce aux **branches** et aux **Pull Requests**.

## 🎯 Objectifs

L'apprenant sait synchroniser son travail avec un dépôt distant, travailler sur une
branche, proposer ses changements via une Pull Request et résoudre un conflit simple.

## 📚 Notions à connaître

- 🎯 **Local vs distant (remote).** Ton dépôt sur ta machine ↔ une copie partagée sur
  **GitHub** (ou GitLab). Le distant est le point de rendez-vous de l'équipe.
- 🎯 **Synchroniser.** `git clone` (récupérer un projet), `git push` (envoyer ses
  commits), `git pull` (récupérer ceux des autres).
- 🎯 **Les branches.** Une ligne de travail isolée. On crée une branche **par
  fonctionnalité** (`git switch -c ma-feature`) pour ne pas toucher la branche
  principale tant que ce n'est pas prêt.
- 🎯 **Fusionner.** Ramener une branche dans une autre (`git merge`) une fois le travail
  validé.
- 🎯 **La Pull Request (PR) / Merge Request.** Proposer ses changements, les faire
  **relire** par l'équipe, discuter, puis fusionner. C'est le cœur du travail en équipe.
- 🎯 **Les conflits.** Quand deux personnes modifient la même zone : Git ne sait pas
  choisir et demande à un humain. Savoir **lire les marqueurs** (`<<<<`, `====`,
  `>>>>`) et garder la bonne version.
- 📌 **Le workflow d'équipe.** Brancher → coder → push → PR → revue → merge → supprimer
  la branche. Garder sa branche à jour (pull régulier).
- 📖 *(culture)* forks, conventions de commits, protection de branche, intégration
  continue (CI).

## ✅ Critères de maîtrise

1. **Cloner** un dépôt, créer une **branche**, committer, **pousser** et ouvrir une
   **Pull Request**.
2. **Mettre à jour** sa copie locale avec `git pull` sans tout casser.
3. **Résoudre un conflit simple** (lire les marqueurs, choisir, committer la résolution).

## ⚠️ Pièges courants

- Travailler **directement sur `main`** au lieu d'une branche dédiée.
- `push` rejeté parce qu'on n'a pas `pull` d'abord (le distant a avancé).
- **Paniquer** devant un conflit : c'est normal et ça se lit calmement.
- Le **`git push --force`** qui écrase le travail des autres → à éviter (surtout sur
  une branche partagée).

## 🔗 Ressources

- GitHub — *Hello World* (premier dépôt, première PR) :
  <https://docs.github.com/fr/get-started/start-your-journey/hello-world>
- *Pro Git* — branches et travail distribué : <https://git-scm.com/book/fr/v2>
