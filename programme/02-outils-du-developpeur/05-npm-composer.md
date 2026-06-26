# 02.5 — Gestionnaires de paquets : npm & composer

- **Thème :** 02 — Outils du développeur
- **Prérequis :** 02.2 (terminal), 02.3 (`.gitignore`)
- **Idée centrale :** on ne réinvente pas la roue. Un **gestionnaire de paquets**
  installe et met à jour le code écrit par d'autres, proprement et de façon reproductible.

## 🎯 Objectifs

L'apprenant comprend ce qu'est une dépendance, sait installer les dépendances d'un
projet et lancer un script, en JS (npm) comme en PHP (composer).

## 📚 Notions à connaître

- 🎯 **Une dépendance, c'est quoi.** Un bout de code externe (une « librairie ») dont
  ton projet a besoin. Plutôt que de le copier-coller, on le **déclare** et l'outil
  l'installe.
- 🎯 **npm (côté JavaScript).** Le fichier **`package.json`** déclare les dépendances et
  les **scripts** ; `npm install` les télécharge dans **`node_modules/`** ; `npm run
  <script>` lance une tâche (ex. `npm run build`).
- 🎯 **composer (côté PHP).** Le fichier **`composer.json`** déclare les dépendances ;
  `composer install` les télécharge dans **`vendor/`** ; l'**autoload** rend les classes
  disponibles automatiquement.
- 🎯 **Ne pas versionner les dépendances.** `node_modules/` et `vendor/` vont dans le
  `.gitignore` : ils se **réinstallent** depuis le fichier de déclaration. En revanche,
  le **lockfile** (`package-lock.json` / `composer.lock`), lui, **se versionne** (il
  fige les versions exactes).
- 📌 **Versions sémantiques (semver).** Lire `^1.2.3` / `~1.2.3` : major.minor.patch et
  ce que les symboles autorisent comme mises à jour.
- 📌 **Dépendances de prod vs de dev** (`dependencies` vs `devDependencies`).
- 📖 *(culture)* les registres (npmjs.com, Packagist), la sécurité des dépendances
  (`npm audit`), l'idée de monorepo.

## ✅ Critères de maîtrise

1. **Lire un `package.json` / `composer.json`** : repérer dépendances et scripts.
2. **Installer** les dépendances d'un projet existant et **lancer un script npm**.
3. Expliquer **pourquoi `node_modules/` n'est pas versionné** mais le lockfile, si.

## ⚠️ Pièges courants

- **Committer `node_modules/` / `vendor/`** (des milliers de fichiers, inutiles).
- **Supprimer le lockfile** → versions qui divergent entre machines.
- Confondre `dependencies` (nécessaires en prod) et `devDependencies` (outillage).
- Lancer `npm install` dans le mauvais dossier (pas celui du `package.json`).

## 🔗 Ressources

- npm — *Documentation* : <https://docs.npmjs.com/>
- Composer — *Getting Started* : <https://getcomposer.org/doc/00-intro.md>
