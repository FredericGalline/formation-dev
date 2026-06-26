# 09.4 — Écrire ses premiers tests

- **Thème :** 09 — Qualité & méthode
- **Prérequis :** 09.3, 04 (JS), 06 (PHP)
- **Idée centrale :** passer de la théorie à la pratique : écrire de vrais tests
  unitaires, les lancer, et savoir lire un échec — en JavaScript comme en PHP.

## 🎯 Objectifs

L'apprenant sait écrire et exécuter un test unitaire simple dans les deux langages du
parcours.

## 📚 Notions à connaître

- 🎯 **L'anatomie d'un test : Arrange / Act / Assert.** Préparer le contexte, exécuter
  l'action, **vérifier** le résultat (l'assertion).
- 🎯 **Un test unitaire JS.** Avec **Vitest** ou **Jest** : `describe()` (regrouper),
  `it()`/`test()` (un cas), `expect(...).toBe(...)` (l'assertion).
- 🎯 **Un test unitaire PHP.** Avec **PHPUnit** : une classe de test, des méthodes
  `test...`, des assertions (`assertSame`, `assertTrue`…).
- 🎯 **Lancer & lire.** Exécuter la suite, **lire un échec** : ce qui était attendu vs
  obtenu, et où.
- 📌 **Mocks / stubs (notion).** Simuler une dépendance (réseau, base) pour **isoler**
  l'unité testée.
- 📌 **Tester un composant React.** Avec **Testing Library** : tester le **comportement**
  vu par l'utilisateur, pas l'implémentation (lien T05).
- 📖 *(culture)* *snapshot testing*, *fixtures*, organisation des fichiers de test.

## ✅ Critères de maîtrise

1. **Écrire un test unitaire** simple (JS **ou** PHP) avec une assertion pertinente.
2. **Lancer la suite** de tests et interpréter le résultat.
3. **Lire un test en échec** et corriger le code (ou le test) en conséquence.

## ⚠️ Pièges courants

- Des tests **dépendants** les uns des autres (l'ordre d'exécution change le résultat).
- Des **assertions floues** ou trop larges qui ne vérifient rien d'utile.
- Tester l'**implémentation** (détails internes) au lieu du **comportement** → tests
  fragiles.
- Oublier les **cas limites** et les erreurs (lien 09.3).

## 🔗 Ressources

- Vitest — *Getting Started* : <https://vitest.dev/guide/>
- PHPUnit — *Writing Tests* :
  <https://docs.phpunit.de/en/current/writing-tests-for-phpunit.html>
- Testing Library : <https://testing-library.com/docs/>
