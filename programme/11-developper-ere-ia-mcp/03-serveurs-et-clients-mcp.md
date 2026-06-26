# 11.3 — Serveurs & clients MCP

- **Thème :** 11 — Développer à l'ère de l'IA *(capstone)*
- **Prérequis :** 11.2, 07.2 (authentification)
- **Idée centrale :** le MCP fonctionne en **client / serveur** : l'assistant IA (le
  client) se connecte à un ou plusieurs **serveurs MCP** qui exposent des capacités. C'est
  ainsi que l'IA accède concrètement au monde extérieur.

## 🎯 Objectifs

L'apprenant comprend l'architecture client/serveur du MCP et sait utiliser un serveur
MCP existant.

## 📚 Notions à connaître

- 🎯 **Client vs serveur.** Le **client MCP** = ton assistant (Claude Code, Cursor…). Le
  **serveur MCP** = un programme qui expose une capacité (accès à GitHub, à une base de
  données, à des fichiers…). Un client peut se brancher sur **plusieurs** serveurs.
- 🎯 **Le transport.** En **local** (le serveur tourne sur ta machine, communication via
  l'entrée/sortie standard) ou **à distance** (via HTTP). Les messages sont structurés
  (format **JSON-RPC**).
- 🎯 **Utiliser un serveur existant.** Le **déclarer** dans la configuration de son client,
  l'**authentifier** si besoin (token / OAuth — rappel 07.2), puis l'IA peut s'en servir.
- 📌 **Créer son propre serveur MCP.** *(awareness)* Exposer **ses** outils/données à
  l'IA — des SDK existent pour le faire. À savoir que c'est possible et accessible.
- 📌 **La sécurité.** Un serveur MCP peut toucher à des choses **sensibles** (dépôts,
  bases, fichiers) : n'utiliser que des serveurs **de confiance**, gérer les **permissions**
  et garder les **secrets** hors du code (lien 06.4, 10.2).
- 📖 *(culture)* les SDK MCP, les registres de serveurs, l'évolution du protocole.

## ✅ Critères de maîtrise

1. Expliquer le rôle d'un **client** et d'un **serveur** MCP, et donner un exemple de
   chaque.
2. Décrire comment on **utilise un serveur MCP existant** (déclarer + authentifier).
3. Citer **un risque de sécurité** lié à un serveur MCP et une parade.

## ⚠️ Pièges courants

- Confondre le **client** (l'assistant) et le **serveur** (la capacité exposée).
- Brancher un serveur MCP **non vérifié** qui accède à des données sensibles.
- Mettre des **secrets** dans la configuration du serveur en clair / dans le dépôt.
- Croire qu'il faut tout développer : commencer par les **serveurs existants**.

## 🔗 Ressources

- *MCP — Concepts (clients, serveurs, transports)* : <https://modelcontextprotocol.io/docs>
- *SDK MCP* (pour créer un serveur) — voir la documentation officielle.
