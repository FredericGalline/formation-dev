# 06.2 — PHP & le web (formulaires, superglobales)

- **Thème :** 06 — PHP & bases serveur
- **Prérequis :** 06.1, 01.2 (HTTP, GET/POST), 03.2 (formulaires HTML)
- **Idée centrale :** PHP **génère du HTML** et **reçoit les données** envoyées par le
  navigateur. C'est le moteur d'un site dynamique.

## 🎯 Objectifs

L'apprenant sait générer une page dynamique et traiter les données d'un formulaire côté
serveur.

## 📚 Notions à connaître

- 🎯 **Générer du HTML.** PHP s'intercale dans le HTML (`<h1><?php echo $titre; ?></h1>`)
  ou produit la page entière. Le navigateur ne reçoit que du HTML.
- 🎯 **Recevoir les données d'un formulaire.** Selon la `method` (01.2, 03.2) :
  **`$_GET`** (données dans l'URL) ou **`$_POST`** (dans le corps de la requête).
- 🎯 **Les superglobales.** Tableaux disponibles partout : `$_GET`, `$_POST`,
  `$_SERVER` (infos de la requête), `$_SESSION`, `$_COOKIE`, `$_FILES`.
- 🎯 **L'état entre les requêtes.** HTTP est *sans mémoire* ; **cookies** (stockés côté
  navigateur) et **sessions** (stockées côté serveur, identifiées par un cookie)
  permettent de « se souvenir » (ex. utilisateur connecté).
- 🎯 **Ne jamais faire confiance aux entrées.** Toute donnée de `$_GET`/`$_POST` est
  potentiellement malveillante → validation et échappement obligatoires (06.4).
- 📌 **En-têtes & redirections.** `header('Location: …')` (notion).
- 📖 *(culture)* le cycle requête → exécution PHP → réponse, côté serveur.

## ✅ Critères de maîtrise

1. **Traiter un formulaire** envoyé en `POST` (lire les champs, réagir).
2. **Lire une donnée** dans une superglobale et l'utiliser dans la page.
3. Expliquer la différence **session vs cookie** et à quoi sert chacun.

## ⚠️ Pièges courants

- **Faire confiance** à `$_GET`/`$_POST` sans valider (porte ouverte aux attaques).
- **Afficher directement** une saisie utilisateur sans l'échapper → faille **XSS** (06.4).
- Confondre **GET** (lecture, visible dans l'URL) et **POST** (envoi, dans le corps).
- Oublier de démarrer la session (`session_start()`) avant d'utiliser `$_SESSION`.

## 🔗 Ressources

- PHP — *Traiter les formulaires* :
  <https://www.php.net/manual/fr/tutorial.forms.php>
- PHP — *Les variables superglobales* :
  <https://www.php.net/manual/fr/language.variables.superglobals.php>
