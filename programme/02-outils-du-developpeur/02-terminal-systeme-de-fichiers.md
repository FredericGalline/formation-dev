# 02.2 — Le terminal & le système de fichiers

- **Thème :** 02 — Outils du développeur
- **Prérequis :** 02.1
- **Idée centrale :** le terminal, c'est **parler à la machine en direct**. Intimidant
  au début, indispensable ensuite.

## 🎯 Objectifs

L'apprenant sait se déplacer dans l'arborescence des fichiers et y créer, déplacer et
supprimer fichiers et dossiers en ligne de commande.

## 📚 Notions à connaître

- 🎯 **C'est quoi le terminal (le shell).** Un programme qui exécute des commandes
  texte. Le dev s'en sert pour Git, npm, lancer des serveurs… plus rapide et précis
  que la souris.
- 🎯 **Le système de fichiers.** Une arborescence de **dossiers** et **fichiers**.
  Savoir se représenter « où on est » dedans.
- 🎯 **Chemins absolus vs relatifs.** Absolu = depuis la racine (`/Users/moi/projet`) ;
  relatif = depuis l'endroit courant (`./src`, `../`). Connaître `.` (ici), `..`
  (dossier parent), `~` (dossier perso).
- 🎯 **Naviguer.** `pwd` (où suis-je ?), `ls` (lister), `cd` (se déplacer).
- 🎯 **Manipuler.** `mkdir` (créer un dossier), `touch` (créer un fichier), `cp`
  (copier), `mv` (déplacer/renommer), `rm` (supprimer — **prudence, pas de corbeille**).
- 📌 **Confort.** Auto-complétion avec `Tab`, rappel des commandes avec la flèche haut,
  lire l'aide (`man <cmd>` ou `<cmd> --help`).
- 📖 *(culture)* le pipe `|`, les redirections `>`, les variables d'environnement, la
  différence bash / zsh.

## ✅ Critères de maîtrise

1. **Se repérer et naviguer** : `pwd`, `ls`, `cd` pour aller dans un dossier donné.
2. **Créer une petite arborescence** (dossiers + fichiers), puis déplacer/renommer un
   fichier en ligne de commande.
3. Expliquer la différence **chemin absolu / relatif** sur un exemple.

## ⚠️ Pièges courants

- `rm -rf` : **destructeur et irréversible** (pas de corbeille). À manier avec respect.
- Confondre chemin **relatif** et **absolu** → « fichier introuvable ».
- Oublier les guillemets sur des noms **avec espaces** (`cd "Mon Dossier"`).
- Croire qu'on est « perdu » : `pwd` répond toujours où on est.

## 🔗 Ressources

- MDN — *Les bases de la ligne de commande* :
  <https://developer.mozilla.org/fr/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line>
- *The Missing Semester* (MIT, en anglais) : <https://missing.csail.mit.edu/>
