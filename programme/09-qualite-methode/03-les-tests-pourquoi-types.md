# 09.3 — Les tests : pourquoi & les types

- **Thème :** 09 — Qualité & méthode
- **Prérequis :** Thèmes 04–08 (du code à tester)
- **Idée centrale :** tester, c'est **vérifier automatiquement** que le code fait ce qu'on
  attend — et qu'il continue de le faire après chaque modification. C'est ce qui permet
  d'avancer **sans peur de casser**.

## 🎯 Objectifs

L'apprenant comprend l'intérêt des tests et sait distinguer les grands types de tests.

## 📚 Notions à connaître

- 🎯 **Pourquoi tester.** **Confiance** (le code marche), **non-régression** (il marche
  encore après un changement), **documentation vivante** (les tests montrent l'usage attendu).
- 🎯 **Test unitaire.** Vérifie **une unité** isolée (une fonction, un composant). Rapide,
  nombreux.
- 🎯 **Test d'intégration.** Vérifie que **plusieurs pièces** fonctionnent **ensemble**
  (ex. une fonction + la base de données).
- 🎯 **Test E2E (end-to-end).** Simule le **parcours utilisateur complet** dans un vrai
  navigateur (ex. Playwright/Cypress). Lent mais réaliste.
- 🎯 **La pyramide des tests.** Beaucoup d'**unitaires** (base), moins d'**intégration**,
  peu d'**E2E** (sommet). Question de coût et de rapidité.
- 🎯 **Un bon test.** Rapide, **isolé** (indépendant des autres), **déterministe** (même
  résultat à chaque fois), **lisible**.
- 📌 **TDD (notion).** Écrire le test **avant** le code. Couverture de tests : utile mais
  **pas un but en soi** (100 % ne garantit pas l'absence de bug).
- 📖 *(culture)* *mocks*/*stubs* (simuler une dépendance), tests lancés en **CI** (lien T10).

## ✅ Critères de maîtrise

1. **Distinguer** unitaire / intégration / E2E sur des exemples concrets.
2. Expliquer la **pyramide des tests** et pourquoi cette répartition.
3. Citer ce qui fait un **bon test** (isolé, déterministe, rapide, lisible).

## ⚠️ Pièges courants

- Ne tester que le **cas idéal** (« happy path ») et oublier les **cas limites**.
- Des tests **lents** ou **fragiles** (qui cassent au moindre détail) → on finit par les ignorer.
- Viser **100 % de couverture** comme objectif plutôt que des tests **utiles**.
- Tout tester en **E2E** (lent, coûteux) au lieu de privilégier l'unitaire.

## 🔗 Ressources

- MDN — *Introduction au test automatisé* :
  <https://developer.mozilla.org/fr/docs/Learn/Tools_and_testing/Cross_browser_testing/Automated_testing>
- *Testing Pyramid* (Martin Fowler, en) :
  <https://martinfowler.com/articles/practical-test-pyramid.html>
