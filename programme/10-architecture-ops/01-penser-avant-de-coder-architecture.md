# 10.1 — Penser avant de coder : architecture

- **Thème :** 10 — Architecture & Ops *(sensibilisation)*
- **Prérequis :** avoir mené quelques petits projets (Thèmes 04–08)
- **Idée centrale :** avant d'écrire du code, **réfléchir** : qu'est-ce qu'on construit,
  comment le découper, où mettre quoi. Une bonne architecture rend un projet
  **compréhensible et évolutif**.

## 🎯 Objectifs

L'apprenant sait découper un projet en responsabilités claires et reconnaître la dette
technique.

## 📚 Notions à connaître

- 🎯 **Penser avant de coder.** Comprendre le **besoin**, esquisser une solution, la
  **découper** en morceaux avant de se lancer. Coder n'est pas la première étape.
- 🎯 **La séparation des responsabilités.** Chaque partie a **un rôle clair** (affichage,
  logique métier, accès aux données). On ne mélange pas tout.
- 🎯 **Organiser un projet.** Une **arborescence cohérente** : on sait où trouver et où
  ajouter les choses, sans deviner.
- 📌 **Les patterns courants.** Savoir que des modèles éprouvés existent (MVC,
  composants, services) — sans les plaquer partout.
- 📌 **La dette technique.** Les raccourcis d'aujourd'hui qui coûteront demain. Elle est
  parfois **assumée** (livrer vite), mais doit être **consciente** et remboursée.
- 📌 **Documenter les décisions.** Un `README` utile, et la notion d'**ADR** (consigner
  *pourquoi* une décision a été prise).
- 📖 *(culture)* couplage faible / cohésion forte, principes **SOLID**, schémas
  d'architecture.

## ✅ Critères de maîtrise

1. **Découper** un petit projet en responsabilités distinctes.
2. **Organiser** une arborescence de projet cohérente et la justifier.
3. Expliquer ce qu'est la **dette technique** et comment la gérer consciemment.

## ⚠️ Pièges courants

- **Coder avant** d'avoir compris le besoin.
- **Tout mélanger** (affichage + logique + données dans le même fichier).
- **Sur-architecturer** un petit projet (abstractions inutiles, lien 09.1).
- **Ignorer la dette** jusqu'à ce qu'elle bloque tout.

## 🔗 Ressources

- *Refactoring Guru* — *Design Patterns* (en, culture) :
  <https://refactoring.guru/design-patterns>
- Martin Fowler — *Technical Debt* (en) :
  <https://martinfowler.com/bliki/TechnicalDebt.html>
