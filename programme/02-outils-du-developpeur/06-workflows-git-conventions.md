# 02.6 — Workflows Git & conventions

- **Thème :** 02 — Outils du développeur
- **Prérequis :** 02.3 (Git local), 02.4 (branches, PR/MR, conflits)
- **Idée centrale :** au-delà des commandes, une équipe a besoin d'un **workflow** partagé
  et de **conventions** : comment on branche, comment on nomme, comment on fusionne. C'est
  ce qui rend la collaboration fluide et l'historique lisible.

## 🎯 Objectifs

L'apprenant comprend les stratégies de branches courantes, les conventions de commits et
de nommage, et le cycle complet d'une contribution.

## 📚 Notions à connaître

- 🎯 **PR = MR.** C'est le **même concept** : une demande de fusion d'une branche après
  relecture. **GitHub** l'appelle *Pull Request* (PR), **GitLab** *Merge Request* (MR).
  Aucune différence de fond.
- 🎯 **Les stratégies de branches (les « workflows »).**
  - **GitHub Flow** : simple — `main` toujours déployable + branches de **fonctionnalité
    courtes** → PR/MR → merge. Le plus répandu aujourd'hui.
  - **Git Flow** : plus structuré (`main`, `develop`, `feature/`, `release/`, `hotfix/`),
    adapté aux **releases versionnées**.
  - **Trunk-based** : branches **très courtes**, intégration fréquente sur le tronc.
- 🎯 **Nommer ses branches.** Une convention claire : `type/description-courte`
  (ex. `feat/formulaire-contact`, `fix/bug-login`).
- 🎯 **Les Conventional Commits.** Un format standard de message :
  `type(portée): description` (`feat`, `fix`, `docs`, `refactor`…). *Pourquoi* :
  historique lisible, génération automatique de changelogs.
- 🎯 **Tags & releases.** **Marquer** une version dans l'historique (un *tag*, ex.
  `v1.2.0`) selon le **versionnage sémantique** (semver, lien 02.5).
- 📌 **`merge` vs `rebase`.** `merge` conserve l'historique tel quel ; `rebase` le
  **réécrit** pour le rendre linéaire. **Ne jamais rebaser une branche partagée**.
- 📌 **Le cycle complet d'une contribution.** Issue → branche → commits → push → **PR/MR**
  → revue (Thème 09) → merge → tag/release → suppression de la branche.
- 📖 *(culture)* protection de branche, `CODEOWNERS`, *squash merge*, intégration
  continue (CI, lien T10).

## ✅ Critères de maîtrise

1. Expliquer que **PR et MR** désignent la même chose (GitHub vs GitLab).
2. **Décrire une stratégie de branches** (au moins GitHub Flow) et dire quand elle convient.
3. **Nommer une branche** et **écrire un commit** au format Conventional Commits ; dire à
   quoi servent les **tags**.

## ⚠️ Pièges courants

- Croire que **PR et MR** sont deux choses différentes.
- Travailler directement sur **`main`** au lieu d'une branche dédiée.
- Des branches **trop longues** qui divergent → fusions douloureuses (*merge hell*).
- Messages de commit **non conventionnels** (« maj », « wip ») → historique illisible.
- **Rebaser une branche partagée** et casser l'historique des autres.

## 🔗 Ressources

- *GitHub Flow* : <https://docs.github.com/fr/get-started/using-github/github-flow>
- *Conventional Commits* : <https://www.conventionalcommits.org/fr/>
- Atlassian — *Comparaison des workflows Git* :
  <https://www.atlassian.com/fr/git/tutorials/comparing-workflows>
