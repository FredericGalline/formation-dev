# 09.1 — Écrire du code lisible

- **Thème :** 09 — Qualité & méthode
- **Prérequis :** avoir écrit un peu de code (Thèmes 04–08)
- **Idée centrale :** on **lit** le code bien plus souvent qu'on ne l'**écrit**. Un code
  lisible se maintient, se relit et se débogue ; un code « malin » mais obscur coûte cher.

## 🎯 Objectifs

L'apprenant sait écrire et améliorer du code pour qu'un autre humain le comprenne sans effort.

## 📚 Notions à connaître

- 🎯 **Le nommage.** Des noms qui **disent l'intention** (`prixTotalTTC`, pas `x`/`tmp`/
  `data`). Le meilleur commentaire est souvent un bon nom.
- 🎯 **Fonctions courtes, une responsabilité.** Une fonction fait **une** chose et la fait
  bien. Si on doit écrire « et » pour la décrire, elle en fait trop.
- 🎯 **Commentaires utiles.** Expliquer le **pourquoi** (une décision, un cas tordu), pas
  le **quoi** (que le code dit déjà). Éviter le **sur-commentaire**.
- 🎯 **Conventions & cohérence.** Suivre le **style du projet** (indentation, nommage,
  organisation). La cohérence prime sur les préférences personnelles.
- 📌 **DRY & KISS.** Ne pas se répéter (factoriser la duplication), rester **simple** ;
  éviter la **sur-ingénierie** (abstraction prématurée « au cas où »).
- 📌 **Formatage automatique.** Linters/formatters (Prettier, ESLint — lien 04.6) pour ne
  pas perdre de temps sur le style.
- 📖 *(culture)* *clean code*, *code smells*, le **refactoring** (améliorer sans changer
  le comportement).

## ✅ Critères de maîtrise

1. **Renommer / refactorer** un bout de code obscur pour le rendre lisible.
2. **Juger** si un commentaire est utile ou superflu, et le corriger.
3. Repérer une fonction qui **fait trop** et la découper.

## ⚠️ Pièges courants

- Noms **cryptiques** (`x`, `tmp`, `data`, `truc`).
- **Sur-commenter** l'évident (`// incrémente i`) au lieu d'expliquer le pourquoi.
- **Duplication** (copier-coller) au lieu de factoriser.
- **Sur-ingénierie** : abstractions et options inutiles ajoutées « au cas où ».

## 🔗 Ressources

- *Refactoring Guru* — *Code Smells* (en) : <https://refactoring.guru/refactoring/smells>
- MDN — *Conventions de codage / bonnes pratiques* (guides généraux).
