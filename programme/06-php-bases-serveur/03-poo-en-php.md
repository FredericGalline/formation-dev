# 06.3 — La POO en PHP

- **Thème :** 06 — PHP & bases serveur
- **Prérequis :** 06.1
- **Idée centrale :** la **programmation orientée objet** (POO) organise le code en
  **classes** et **objets**. C'est **indispensable** pour comprendre WordPress moderne,
  écrire des plugins et utiliser des bibliothèques via Composer.

## 🎯 Objectifs

L'apprenant sait définir et utiliser une classe, et comprend les notions de POO
nécessaires pour la suite.

## 📚 Notions à connaître

- 🎯 **Pourquoi la POO.** Regrouper des données et les fonctions qui les manipulent,
  réutiliser, structurer. WordPress, les plugins et Composer en sont remplis.
- 🎯 **Classe & objet.** La **classe** est le moule (`class Produit { … }`), l'**objet**
  est une instance (`$p = new Produit();`).
- 🎯 **Propriétés & méthodes.** Variables (`$this->nom`) et fonctions (`$this->afficher()`)
  d'un objet ; **`$this`** désigne l'objet courant.
- 🎯 **La visibilité.** `public` (accessible partout), `private` (interne à la classe),
  `protected` (classe + filles). Encapsuler ce qui doit l'être.
- 🎯 **Le constructeur.** `__construct()` initialise l'objet à sa création.
- 📌 **Héritage & interfaces.** Une classe peut **étendre** une autre (`extends`) ou
  s'engager à respecter un **contrat** (`implements`) — notions.
- 📌 **Namespaces & autoload.** Organiser les classes en espaces de noms et les charger
  automatiquement via Composer (lien 02.5).
- 📖 *(culture)* traits, classes abstraites, quelques design patterns courants.

## ✅ Critères de maîtrise

1. **Définir une classe** avec propriétés, constructeur et méthodes, puis l'**instancier**.
2. Utiliser **`$this`** et choisir la bonne **visibilité** pour une propriété.
3. Expliquer la différence **classe / objet** et l'intérêt de la POO pour WordPress.

## ⚠️ Pièges courants

- Confondre **classe** (le moule) et **objet** (l'instance).
- Oublier **`$this->`** pour accéder à une propriété/méthode de l'objet.
- Confondre **`->`** (membre d'objet) et **`::`** (membre statique / de classe).
- Tout mettre en `public` au lieu d'encapsuler.

## 🔗 Ressources

- PHP — *Les classes et les objets* :
  <https://www.php.net/manual/fr/language.oop5.php>
- PHP — *Espaces de noms* :
  <https://www.php.net/manual/fr/language.namespaces.php>
