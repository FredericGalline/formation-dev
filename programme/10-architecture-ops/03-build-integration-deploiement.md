# 10.3 — Build, intégration & déploiement (CI/CD)

- **Thème :** 10 — Architecture & Ops *(sensibilisation)*
- **Prérequis :** 02.6 (Git, PR), 09 (tests), 02.5 (build/npm)
- **Idée centrale :** automatiser le chemin du code, de la PR à la mise en ligne :
  **construire**, **tester** automatiquement à chaque changement (CI), puis **déployer**
  (CD). Moins d'erreurs humaines, plus de confiance.

## 🎯 Objectifs

L'apprenant comprend ce qu'est un pipeline CI/CD et le rôle de chaque étape.

## 📚 Notions à connaître

- 🎯 **Le build.** Transformer le code source en **artefact déployable** (compiler/bundler
  le front, ex. Vite ou `@wordpress/scripts`, lien 02.5).
- 🎯 **L'intégration continue (CI).** À chaque **push / PR**, lancer **automatiquement**
  les tests et les linters (lien Thème 09). On détecte les régressions tout de suite.
- 🎯 **Le déploiement continu (CD).** **Automatiser** la mise en ligne une fois la CI
  verte, vers staging puis production.
- 🎯 **Le pipeline.** Une suite d'étapes : **installer → build → tester → déployer**.
  Si une étape échoue, on s'arrête.
- 📌 **Les outils.** **GitHub Actions** / **GitLab CI** : des fichiers de workflow
  décrivent le pipeline.
- 📌 **Le rollback.** Pouvoir **revenir** à une version précédente en cas de problème
  (lien tags/releases, 02.6).
- 📖 *(culture)* déploiement **bleu-vert**, **canary**, artefacts et registres.

## ✅ Critères de maîtrise

1. Expliquer la différence **CI vs CD**.
2. **Décrire les étapes** d'un pipeline (install → build → test → deploy).
3. Dire **pourquoi** lancer les tests automatiquement à chaque push.

## ⚠️ Pièges courants

- **Déployer à la main** sans tests ni traçabilité.
- Un pipeline qui **ne lance pas les tests** (CI décorative).
- **Aucune stratégie de rollback** quand un déploiement casse la prod.
- Mettre des **secrets** en clair dans les fichiers de pipeline (lien 10.2).

## 🔗 Ressources

- GitHub Actions — *Découvrir* : <https://docs.github.com/fr/actions>
- Atlassian — *CI/CD expliqué* :
  <https://www.atlassian.com/fr/devops/continuous-delivery-tutorials/principles-of-continuous-delivery>
