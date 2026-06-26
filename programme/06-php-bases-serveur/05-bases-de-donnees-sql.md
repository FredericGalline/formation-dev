# 06.5 — Bases de données & SQL (intro)

- **Thème :** 06 — PHP & bases serveur
- **Prérequis :** 06.1, 06.4 (sécurité)
- **Idée centrale :** une **base de données** stocke durablement les données d'une
  application (utilisateurs, articles, commandes). On l'interroge avec **SQL**. C'est ce
  que WordPress utilise sous le capot.

## 🎯 Objectifs

L'apprenant comprend une base relationnelle et sait écrire les requêtes SQL de base, de
façon sécurisée.

## 📚 Notions à connaître

- 🎯 **Une base relationnelle.** Des **tables** (comme des feuilles de calcul) avec des
  **colonnes** (champs) et des **lignes** (enregistrements). Ex. une table `articles`.
- 🎯 **Les requêtes de base (CRUD).** **`SELECT`** (lire), **`INSERT`** (créer),
  **`UPDATE`** (modifier), **`DELETE`** (supprimer), avec **`WHERE`** pour cibler.
- 🎯 **Clé primaire & relations.** Chaque ligne a un identifiant unique (**clé
  primaire**) ; les tables se relient par des **clés étrangères** (ex. un article
  appartient à un auteur).
- 🎯 **Les requêtes préparées.** Depuis PHP (**PDO** ou mysqli), on passe les valeurs
  **séparément** de la requête → protège de l'**injection SQL** (lien 06.4). **Jamais**
  de concaténation.
- 📌 **Se connecter depuis PHP.** Notion de connexion PDO et d'exécution d'une requête.
- 📖 *(culture)* les **jointures** (`JOIN`), les **index**, les SGBD
  (MySQL/MariaDB/PostgreSQL), et les **ORM** (manipuler la base en objets).

## ✅ Critères de maîtrise

1. **Écrire des requêtes** `SELECT` (avec `WHERE`), `INSERT` et `UPDATE` correctes.
2. Décrire ce qu'est une **clé primaire** et une relation entre deux tables.
3. Expliquer **pourquoi** on utilise des **requêtes préparées**.

## ⚠️ Pièges courants

- Faire **`SELECT *`** par réflexe au lieu de cibler les colonnes utiles.
- Oublier le **`WHERE`** sur un `UPDATE`/`DELETE` → toute la table est touchée.
- **Concaténer** des valeurs dans la requête (injection SQL).
- Confondre **base de données** et **table** (la base contient plusieurs tables).

## 🔗 Ressources

- *SQL* — tutoriel d'introduction (ex. SQLZoo, en) : <https://sqlzoo.net/>
- PHP — *PDO (accès aux bases de données)* :
  <https://www.php.net/manual/fr/book.pdo.php>
