# 06.4 — La sécurité serveur

- **Thème :** 06 — PHP & bases serveur
- **Prérequis :** 06.2 (entrées utilisateur), 06.5 (SQL, en parallèle)
- **Idée centrale :** **ne jamais faire confiance aux entrées.** La sécurité n'est pas une
  option de fin de projet : c'est un réflexe à acquérir dès la première ligne côté serveur.

## 🎯 Objectifs

L'apprenant connaît les principales failles web côté serveur et les réflexes pour s'en
prémunir.

## 📚 Notions à connaître

- 🎯 **Le principe fondamental.** Toute donnée venant de l'extérieur (`$_GET`, `$_POST`,
  URL, API…) est **suspecte** jusqu'à preuve du contraire.
- 🎯 **Valider / assainir / échapper.** Trois gestes distincts :
  - **valider** (la donnée est-elle conforme ? un e-mail, un entier…),
  - **assainir** (nettoyer ce qui ne devrait pas être là),
  - **échapper à la sortie** (rendre une donnée inoffensive là où elle est utilisée).
- 🎯 **Injection SQL.** Insérer du SQL malveillant via une saisie → parade : les
  **requêtes préparées** (06.5), **jamais** de concaténation de variables dans une requête.
- 🎯 **XSS (Cross-Site Scripting).** Du HTML/JS injecté dans la page → parade :
  **échapper en sortie** (`htmlspecialchars`) toute donnée affichée.
- 🎯 **Mots de passe.** **Jamais en clair** : on les **hash** (`password_hash` /
  `password_verify`).
- 📌 **CSRF.** Forcer un utilisateur à exécuter une action à son insu → parade : les
  **jetons** (lien avec les *nonces* de WordPress, Thème 08).
- 📖 *(culture)* l'**OWASP Top 10**, la gestion des **secrets** (clés, mots de passe hors
  du code), les en-têtes de sécurité.

## ✅ Critères de maîtrise

1. **Valider une entrée** puis **l'échapper en sortie** sur un cas concret.
2. Expliquer l'**injection SQL** et sa parade (requêtes préparées).
3. **Hasher et vérifier** un mot de passe (et dire pourquoi jamais en clair).

## ⚠️ Pièges courants

- Échapper **à l'entrée** au lieu **de la sortie** (l'échappement dépend du contexte
  d'usage).
- **Concaténer** des variables dans une requête SQL (injection garantie).
- Stocker un mot de passe **en clair** ou avec un hachage obsolète (md5/sha1).
- Croire que « valider côté client (JS) » suffit : la validation **serveur** est
  obligatoire (le client est contournable).

## 🔗 Ressources

- OWASP — *Top 10* : <https://owasp.org/www-project-top-ten/>
- PHP — *Hachage des mots de passe* :
  <https://www.php.net/manual/fr/faq.passwords.php>
