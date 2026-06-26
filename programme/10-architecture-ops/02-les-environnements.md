# 10.2 — Les environnements

- **Thème :** 10 — Architecture & Ops *(sensibilisation)*
- **Prérequis :** 02.2 (terminal), 06.4 (secrets)
- **Idée centrale :** un projet ne vit pas qu'« en local ». Il passe par plusieurs
  **environnements** (local, staging, production) qui doivent se ressembler, avec une
  **config** et des **secrets** gérés proprement.

## 🎯 Objectifs

L'apprenant comprend le rôle des différents environnements et sait gérer config et
secrets sans les exposer.

## 📚 Notions à connaître

- 🎯 **Local / staging / production.** **Local** : ta machine (développement) ;
  **staging** (recette) : une copie proche de la prod pour valider ; **production** : le
  site réel, vu par les utilisateurs.
- 🎯 **La parité des environnements.** Plus les environnements se ressemblent, moins on a
  de surprises du type « ça marche chez moi » en arrivant en prod.
- 🎯 **Les variables d'environnement.** La configuration qui **change selon
  l'environnement** (URL de base de données, clés…) vit dans des variables, pas dans le
  code (lien 02.2).
- 🎯 **Ne jamais committer de secrets.** Clés, mots de passe → dans un `.env` **ignoré
  par Git** (lien 02.3) ou un gestionnaire de secrets, **jamais** dans le dépôt (lien
  06.4 / 08.12).
- 📌 **Config par environnement.** Une même base de code, des réglages différents selon
  l'endroit où elle tourne.
- 📖 *(culture)* la méthode **12-factor app**, les *feature flags* (activer/désactiver une
  fonctionnalité sans redéployer).

## ✅ Critères de maîtrise

1. Expliquer le **rôle** de local, staging et production.
2. Utiliser une **variable d'environnement** pour un paramètre/secret.
3. Dire **pourquoi** un fichier de secrets n'est jamais versionné.

## ⚠️ Pièges courants

- **Tester directement en production** (au lieu de staging).
- **Secrets dans le code** ou commités dans le dépôt.
- Configuration **en dur** au lieu de variables d'environnement.
- Un environnement local **trop différent** de la prod → bugs uniquement en ligne.

## 🔗 Ressources

- *The Twelve-Factor App* (en) : <https://12factor.net/fr/>
- *Variables d'environnement* (guides généraux des hébergeurs / frameworks).
