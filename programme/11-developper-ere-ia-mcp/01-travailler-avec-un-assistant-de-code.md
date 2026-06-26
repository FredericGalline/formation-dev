# 11.1 — Travailler avec un assistant de code

- **Thème :** 11 — Développer à l'ère de l'IA *(capstone)*
- **Prérequis :** 09.1 (code lisible), 09.5 (se débrouiller, demander de l'aide)
- **Idée centrale :** un assistant IA est un **copilote**, pas un pilote automatique. Il
  accélère énormément, mais **tu restes responsable** de tout le code qui part en production.

## 🎯 Objectifs

L'apprenant sait utiliser un assistant de code efficacement, avec les garde-fous qui
évitent d'accumuler de la dette invisible.

## 📚 Notions à connaître

- 🎯 **Copilote, pas pilote automatique.** L'IA propose ; toi tu décides, tu relis, tu
  assumes. Ton nom est sur le commit, pas le sien.
- 🎯 **Bien formuler sa demande.** Donner le **contexte**, l'**objectif** et les
  **contraintes** (mêmes réflexes qu'une bonne demande d'aide, 09.5). Une demande vague
  produit un code vague.
- 🎯 **Toujours relire et comprendre.** **Ne jamais intégrer du code qu'on ne comprend
  pas.** Si tu ne peux pas l'expliquer, tu ne peux pas le maintenir ni le déboguer.
- 🎯 **Vérifier ce que l'IA produit.** Lire, exécuter, **tester** (Thème 09). L'IA se
  trompe avec aplomb (cf. 11.5).
- 📌 **Itérer.** Découper la tâche, donner du feedback, corriger le tir — plutôt qu'un
  énorme prompt « fais tout ».
- 📌 **Garde-fous.** Ne pas exposer de **secrets** ni de données sensibles à l'IA (lien
  06.4, 10.2) ; se méfier des dépendances/API « inventées ».
- 📖 *(culture)* l'IA dans le workflow d'équipe (aide à la revue, aux tests, à la doc) ;
  cette formation, pilotée par IA, comme cas concret.

## ✅ Critères de maîtrise

1. **Formuler une demande claire** (contexte + objectif + contraintes) à un assistant.
2. **Relire, comprendre et vérifier** une proposition de l'IA avant de l'intégrer.
3. Citer **deux garde-fous** (secrets, vérification) et expliquer pourquoi on reste
   responsable du code.

## ⚠️ Pièges courants

- **Copier-coller sans comprendre** → dette invisible, bugs qu'on ne sait pas corriger.
- Prompt **vague** ou monolithique → résultat à côté de la plaque.
- **Faire confiance aveuglément** (l'IA hallucine — 11.5).
- **Exposer des secrets** ou du code confidentiel à un service externe.

## 🔗 Ressources

- *Bonnes pratiques d'usage des assistants de code* (docs des outils : Claude Code,
  Copilot, Cursor…).
- Renvoi interne : [09.5 — Déboguer & se débrouiller](../09-qualite-methode/05-deboguer-se-debrouiller.md).
