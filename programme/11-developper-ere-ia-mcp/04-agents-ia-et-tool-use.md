# 11.4 — Agents IA & *tool use*

- **Thème :** 11 — Développer à l'ère de l'IA *(capstone)*
- **Prérequis :** 11.2, 11.3
- **Idée centrale :** un **agent IA** ne se contente pas de répondre — il **agit** : il
  utilise des outils, en boucle, pour atteindre un but. Le mécanisme de base s'appelle le
  ***tool use*** (l'appel d'outils).

## 🎯 Objectifs

L'apprenant comprend ce qu'est un agent IA, le principe du *tool use*, et quand un agent
est pertinent.

## 📚 Notions à connaître

- 🎯 **Le *tool use* (appel d'outils).** On décrit à l'IA des **outils** (des fonctions
  avec un nom, une description, des paramètres) ; l'IA **décide** d'en appeler un, reçoit
  le **résultat**, et continue. C'est ce qui relie l'IA au monde (et ce que le MCP
  standardise, 11.2).
- 🎯 **Qu'est-ce qu'un agent.** Une IA placée dans une **boucle** : elle perçoit, décide,
  **agit** (via des outils), observe le résultat, et recommence jusqu'à atteindre le but.
- 🎯 **Workflow vs agent.** Un **workflow** est piloté par **ton code** (étapes
  déterministes, tu gardes la main) ; un **agent** décide **lui-même** sa trajectoire
  (plus flexible, moins prévisible).
- 📌 **Quand utiliser un agent.** Pour une tâche **complexe et multi-étapes** difficile à
  scripter d'avance. Pour une tâche simple et bien définie, un **simple appel** ou un
  workflow suffit (et coûte moins, cf. 11.5).
- 📌 **Garder le contrôle.** Validation des actions sensibles, limites (nombre d'étapes),
  journalisation — un agent autonome doit rester **encadré**.
- 📖 *(culture)* systèmes **multi-agents**, **RAG** (donner à l'IA des documents à
  consulter), les frameworks d'agents.

## ✅ Critères de maîtrise

1. Expliquer le principe du ***tool use*** (l'IA appelle un outil, reçoit le résultat,
   continue).
2. Définir ce qu'est un **agent** (l'IA dans une boucle perception → décision → action).
3. Distinguer **workflow** (piloté par le code) et **agent** (piloté par le modèle), et
   dire quand chacun convient.

## ⚠️ Pièges courants

- Dégainer un **agent** là où un simple appel suffit (plus lent, plus cher, moins prévisible).
- Laisser un agent agir **sans garde-fou** sur des actions sensibles (suppression, envoi…).
- Croire que l'agent « comprend » son but : il **optimise** vers ce qu'on lui a décrit —
  d'où l'importance d'un objectif clair.

## 🔗 Ressources

- *Tool use / function calling* — documentation des fournisseurs d'IA.
- *Building effective agents* (article de référence sur workflows vs agents).
