# 01.4 — Statique vs dynamique, front vs back

- **Thème :** 01 — Comment marche le web
- **Prérequis :** 01.1, 01.3
- **Idée centrale :** comprendre **qui fait quoi** et **où le code s'exécute** —
  la distinction qui structurera toute la suite (React = front, WordPress = back).

## 🎯 Objectifs

L'apprenant sait situer où s'exécute un morceau de code (navigateur ou serveur) et
classer un site/une fonctionnalité en statique/dynamique, front/back.

## 📚 Notions à connaître

- 🎯 **Site statique vs dynamique.**
  - **Statique** : le serveur renvoie des fichiers tout prêts, identiques pour tous
    (une page « vitrine » figée).
  - **Dynamique** : le contenu est **généré à la demande** (selon l'utilisateur, la
    base de données, l'heure…). Un blog, une boutique, un espace connecté.
- 🎯 **Front-end vs back-end.**
  - **Front-end** = ce qui tourne **dans le navigateur** (HTML/CSS/JS), ce que voit
    l'utilisateur.
  - **Back-end** = ce qui tourne **sur le serveur** (logique, base de données,
    génération des pages).
- 🎯 **Où s'exécute le code.** Savoir dire, pour un bout de logique donné, s'il tourne
  **côté client** (navigateur) ou **côté serveur** — et pourquoi ça change tout
  (sécurité, données, performance).
- 📌 **Où se situe WordPress.** Un back-end (PHP) qui **génère du HTML** côté serveur à
  partir d'une base de données. *(Teaser de la spécialité, Thème 07.)*
- 📌 **Où se situe React.** Du front-end (JS) qui **s'exécute dans le navigateur** pour
  rendre l'interface interactive. *(Teaser, Thème 05.)*
- 📖 *(culture)* **SSR vs CSR, SPA.** Rendu côté serveur vs côté client, application
  monopage. Juste savoir que ces approches existent.

## ✅ Critères de maîtrise

1. Donné des exemples (page « mentions légales », blog WordPress, calculatrice en JS),
   les **classer** statique/dynamique **et** front/back, avec justification.
2. Pour une fonctionnalité simple, dire **où elle s'exécute** (client ou serveur) et
   **pourquoi**.
3. Expliquer en une phrase la différence **front-end / back-end**.

## ⚠️ Pièges courants

- Croire que « dynamique » = « avec des animations » (le dynamisme est sur le
  **contenu**, pas l'esthétique).
- Penser que tout le JavaScript tourne côté serveur (par défaut, le JS du web tourne
  dans le **navigateur**).
- Mélanger « front-end » (où ça s'affiche) et « statique » (comment c'est généré) :
  ce sont deux axes différents.

## 🔗 Ressources

- MDN — *Front-end et back-end* (pages d'introduction au développement web).
- MDN — *Côté client vs côté serveur* :
  <https://developer.mozilla.org/fr/docs/Learn/Server-side/First_steps/Client-Server_overview>
