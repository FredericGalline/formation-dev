# 11.2 — Qu'est-ce que le MCP (Model Context Protocol)

- **Thème :** 11 — Développer à l'ère de l'IA *(capstone)*
- **Prérequis :** 07 (APIs), 11.1
- **Idée centrale :** le **MCP** est un **standard ouvert** qui connecte les assistants
  IA aux outils et aux données — un connecteur **universel**, là où chaque intégration
  était auparavant du sur-mesure.

## 🎯 Objectifs

L'apprenant sait expliquer ce qu'est le MCP, le problème qu'il résout, et ce qu'un
serveur MCP expose.

## 📚 Notions à connaître

- 🎯 **Le problème.** Une IA est puissante mais « enfermée » : sans accès à *tes* outils,
  *tes* données, *ton* contexte. Connecter chaque IA à chaque outil à la main, c'est un
  problème combinatoire (N × M intégrations).
- 🎯 **MCP = Model Context Protocol.** Un **standard ouvert** (créé par Anthropic,
  open-source) qui définit **une seule façon** de brancher un assistant IA sur des outils
  et des sources de données.
- 🎯 **L'analogie : le « port USB-C de l'IA ».** Un connecteur universel — au lieu d'un
  câble propriétaire par appareil, une prise unique pour tout brancher.
- 🎯 **Ce que ça change.** Un serveur MCP écrit **une fois** est utilisable par **toute**
  application IA compatible (Claude Code, Cursor, et d'autres). On ne réécrit plus
  l'intégration pour chaque assistant.
- 📌 **Ce que MCP expose (3 primitives).** Des **outils** (des actions que l'IA peut
  déclencher), des **ressources** (des données/du contexte à lire), des **prompts** (des
  modèles d'instructions réutilisables).
- 📖 *(culture)* l'écosystème : des serveurs MCP existent déjà pour GitHub, des bases de
  données, des outils de gestion… et pourquoi le MCP est devenu un standard de fait.

## ✅ Critères de maîtrise

1. Expliquer **avec ses mots** ce qu'est le MCP et le problème qu'il résout.
2. Citer l'**analogie USB-C** et ce qu'apporte un **standard** (écrire une fois, réutiliser partout).
3. Nommer les **trois primitives** exposées par un serveur MCP (outils, ressources, prompts).

## ⚠️ Pièges courants

- Confondre **MCP** (le protocole de connexion IA ↔ outils) et une **API REST** classique
  (même esprit d'intégration, mais MCP est spécialisé pour les assistants IA).
- Croire que MCP « est » l'IA : c'est la **plomberie** qui relie l'IA à tes outils, pas le
  modèle lui-même.
- Penser qu'il faut tout coder soi-même : beaucoup de serveurs MCP **existent déjà**.

## 🔗 Ressources

- *Model Context Protocol* — site officiel : <https://modelcontextprotocol.io/>
- *Introduction au MCP* (documentation Anthropic).
