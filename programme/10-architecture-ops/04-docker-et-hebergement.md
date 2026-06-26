# 10.4 — Docker & l'hébergement

- **Thème :** 10 — Architecture & Ops *(sensibilisation)*
- **Prérequis :** 01.1 (client/serveur), 10.2 (environnements)
- **Idée centrale :** comprendre **où** tourne le code une fois livré, et comment
  **Docker** aide à le faire tourner **partout de la même façon**.

## 🎯 Objectifs

L'apprenant comprend ce que résout Docker et où le code est hébergé (serveur, DNS).

## 📚 Notions à connaître

- 🎯 **Le problème que résout Docker.** « Ça marche sur ma machine » : un **conteneur**
  embarque l'application **et son environnement** (versions, dépendances) pour tourner à
  l'identique partout (lien parité, 10.2).
- 🎯 **Conteneur vs machine virtuelle.** Le conteneur est **léger** (partage le noyau de
  l'hôte) ; la VM embarque tout un système. Notion.
- 🎯 **Image / conteneur / Dockerfile.** Une **image** est un modèle figé ; un
  **conteneur** est une image qui tourne ; le **Dockerfile** décrit comment construire
  l'image. **docker-compose** orchestre plusieurs conteneurs (ex. PHP + base de données).
- 🎯 **L'hébergement.** Où tourne le code : un **serveur** (mutualisé, VPS, cloud).
  Rappel : le serveur est une vraie machine quelque part (01.1).
- 🎯 **Le DNS.** Relier un **nom de domaine** à l'adresse du serveur (rappel 01.1) — ce
  qui rend le site accessible par son URL.
- 📌 **Services managés (PaaS) & serverless.** Déléguer l'infrastructure ; le *serverless*
  exécute du code à la demande sans gérer de serveur (notions).
- 📖 *(culture)* **Kubernetes** et l'orchestration de conteneurs à grande échelle.

## ✅ Critères de maîtrise

1. Expliquer **ce que résout Docker** (la reproductibilité de l'environnement).
2. Distinguer **image** et **conteneur**.
3. Expliquer le rôle du **DNS** dans l'accès à un site.

## ⚠️ Pièges courants

- Confondre **image** (modèle) et **conteneur** (instance qui tourne).
- Croire qu'un **conteneur = une VM** (ce n'est pas la même chose).
- Considérer l'**hébergement** comme « pas mon problème » de développeur.
- Oublier que le **DNS** prend un peu de temps à se propager.

## 🔗 Ressources

- Docker — *Get Started* : <https://docs.docker.com/get-started/>
- MDN — *Qu'est-ce qu'un serveur web ?* :
  <https://developer.mozilla.org/fr/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server>
