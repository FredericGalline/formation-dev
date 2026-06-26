# 06.1 — PHP : les bases du langage

- **Thème :** 06 — PHP & bases serveur
- **Prérequis :** 01.4 (côté serveur), 04.1 (bases de prog. — beaucoup se transpose)
- **Idée centrale :** les mêmes briques qu'en JS (variables, conditions, boucles,
  fonctions), mais côté serveur et avec la syntaxe PHP — dont les **tableaux
  associatifs**, omniprésents dans WordPress.

## 🎯 Objectifs

L'apprenant sait écrire un script PHP avec variables, conditions, boucles, fonctions et
tableaux.

## 📚 Notions à connaître

- 🎯 **Où s'exécute PHP.** Côté **serveur** (rappel 01.4) : le code tourne sur le serveur
  et envoie du HTML au navigateur. Délimité par `<?php … ?>`.
- 🎯 **Variables et types.** Les variables commencent par **`$`** (`$nom`). Types :
  `string`, `int`, `float`, `bool`, `array`, `null`.
- 🎯 **Opérateurs.** Arithmétiques, comparaison (`===`/`==`), logiques, et surtout la
  **concaténation avec `.`** (pas `+` comme en JS).
- 🎯 **Afficher.** `echo`, et `var_dump()` / `print_r()` pour déboguer.
- 🎯 **Conditions & boucles.** `if/else`, `switch`, ternaire ; `for`, `while`, et surtout
  **`foreach`** pour parcourir un tableau.
- 🎯 **Les fonctions.** Déclaration, paramètres, `return` ; déclarations de **types**
  (`function somme(int $a, int $b): int`).
- 🎯 **Les tableaux.** **Indexés** (`[1, 2, 3]`) et surtout **associatifs**
  (`['nom' => 'Léa', 'age' => 30]`) — le format roi en PHP et dans WordPress.
- 📖 *(culture)* l'évolution de PHP (8.x : typage, performances), différences notables
  avec JavaScript.

## ✅ Critères de maîtrise

1. **Écrire une fonction** PHP avec condition et/ou boucle qui retourne un résultat.
2. **Manipuler un tableau associatif** (créer, lire, parcourir avec `foreach`).
3. Afficher des valeurs avec `echo` et inspecter une variable avec `var_dump`.

## ⚠️ Pièges courants

- Oublier le **`$`** devant une variable ou le **`;`** en fin d'instruction.
- Utiliser **`+`** pour concaténer des chaînes (en PHP, c'est **`.`**).
- Confondre `=` (affectation) et `==`/`===` (comparaison).
- Oublier que `foreach` peut donner **clé ET valeur** (`foreach ($t as $cle => $val)`).

## 🔗 Ressources

- *PHP : Le tutoriel* (manuel officiel) : <https://www.php.net/manual/fr/tutorial.php>
- *PHP The Right Way* (bonnes pratiques, fr) : <https://phptherightway.com/>
