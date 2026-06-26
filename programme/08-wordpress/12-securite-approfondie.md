# 08.12 — Sécurité WordPress approfondie

- **Thème :** 08 — WordPress *(approfondissement)*
- **Prérequis :** 08.8 (les 4 réflexes), 06.4 (sécurité serveur), 08.7 (API REST)
- **Idée centrale :** au-delà des bases, durcir un site WordPress sur tous les fronts :
  base de données, échappement contextuel, droits, API REST, configuration. La sécurité
  est **transverse et permanente**.

## 🎯 Objectifs

L'apprenant sait appliquer les pratiques de sécurité WordPress avancées et durcir une
installation.

## 📚 Notions à connaître

- 🎯 **Requêtes BDD sûres.** Toujours **`$wpdb->prepare()`** : jamais de concaténation de
  variables dans une requête (injection SQL, lien 06.4/06.5). Privilégier les API WP
  (`WP_Query`, `get_posts`) quand c'est possible.
- 🎯 **L'échappement contextuel.** Choisir le **bon** `esc_*` selon **où** la donnée
  sort : `esc_html` (texte), `esc_attr` (attribut), `esc_url` (URL), `esc_js` (JS),
  **`wp_kses`** (HTML autorisé limité). Le contexte décide.
- 🎯 **Valider & assainir les entrées.** `sanitize_text_field`, `absint`, etc. ;
  **valider les arguments** d'un endpoint REST (`args` + `validate_callback`/`sanitize_callback`).
- 🎯 **Droits & moindre privilège.** `current_user_can()` avant toute action sensible ;
  ne donner que les **capabilities** strictement nécessaires.
- 🎯 **Nonces bien faits.** Un nonce lié à une **action précise** (pas générique), créé et
  **vérifié** ; nonce REST pour les appels d'un utilisateur connecté (lien 08.7).
- 🎯 **Durcissement (*hardening*).** `DISALLOW_FILE_EDIT` (couper l'éditeur de l'admin),
  permissions de fichiers correctes, **secrets hors du code** (`wp-config`/variables
  d'environnement), **garder WP, thèmes et plugins à jour**.
- 📌 **Sécuriser l'API REST.** `permission_callback` **systématique**, n'exposer que le
  strict nécessaire (lien 08.7).
- 📌 **En-têtes & uploads.** En-têtes de sécurité (dont CSP), contrôle des types de
  fichiers téléversés.
- 📖 *(culture)* audit de sécurité, plugins dédiés, OWASP appliqué à WordPress.

## ✅ Critères de maîtrise

1. Écrire une requête BDD sûre avec **`$wpdb->prepare()`**.
2. Choisir le **bon `esc_*`** selon le contexte de sortie, sur plusieurs exemples.
3. **Sécuriser un endpoint REST** (permission + validation) et citer **3 mesures de
   hardening**.

## ⚠️ Pièges courants

- Mauvais `esc_*` selon le contexte (ex. `esc_html` dans un attribut, ou rien du tout).
- **Concaténer** des variables dans une requête au lieu de `prepare()`.
- Nonce **générique** (non lié à l'action) ou jamais vérifié.
- Endpoint REST **sans `permission_callback`** ; **secrets** commités dans le dépôt.

## 🔗 Ressources

- WordPress — *Security (Plugin Handbook)* :
  <https://developer.wordpress.org/plugins/security/>
- WordPress — *Hardening WordPress* :
  <https://developer.wordpress.org/advanced-administration/security/hardening/>
