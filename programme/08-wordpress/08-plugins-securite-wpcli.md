# 08.8 — Plugins, sécurité & WP-CLI

- **Thème :** 08 — WordPress
- **Prérequis :** 08.2 (hooks), 06.4 (sécurité serveur)
- **Idée centrale :** packager une fonctionnalité dans un **plugin** propre, et appliquer
  les **réflexes de sécurité WordPress** (nonces, capabilities, sanitization/escaping) —
  non négociables.

## 🎯 Objectifs

L'apprenant sait structurer un plugin simple et appliquer les pratiques de sécurité
WordPress.

## 📚 Notions à connaître

- 🎯 **La structure d'un plugin.** Un dossier dans `wp-content/plugins/`, un fichier
  principal avec l'**en-tête de plugin** (commentaire d'identité), et le code branché via
  les **hooks** (08.2).
- 🎯 **Activation / désactivation.** `register_activation_hook` /
  `register_deactivation_hook` (créer/nettoyer ce qu'il faut).
- 🎯 **La sécurité WordPress — les 4 réflexes.**
  - **Nonces** : jetons anti-CSRF (`wp_create_nonce` / `wp_verify_nonce`, lien 06.4).
  - **Capabilities** : vérifier les **droits** avant d'agir (`current_user_can`).
  - **Sanitization** : nettoyer les **entrées** (`sanitize_text_field`…).
  - **Escaping** : échapper les **sorties** (`esc_html`, `esc_attr`, `esc_url`).
- 🎯 **Charger scripts & styles proprement.** `wp_enqueue_script` / `wp_enqueue_style`
  (jamais en dur dans le HTML).
- 📌 **WP-CLI.** Gérer WordPress en **ligne de commande** (`wp plugin`, `wp user`,
  `wp search-replace`…) — précieux pour l'automatisation et l'ops (lien T02.2, T10).
- 📖 *(culture)* les **WordPress Coding Standards**, la distribution d'un plugin (.org),
  l'internationalisation (i18n).

## ✅ Critères de maîtrise

1. **Créer un plugin minimal** (en-tête + une fonctionnalité branchée sur un hook).
2. Appliquer les **4 réflexes de sécurité** (nonce, capability, sanitize, escape) sur un
   traitement de formulaire.
3. **Charger un script/style** proprement avec `wp_enqueue_*`.

## ⚠️ Pièges courants

- **Aucune vérification de droits** (`current_user_can`) avant une action sensible.
- **Sanitize** à l'entrée mais **oubli d'escape** à la sortie (ou l'inverse) — les deux
  comptent (lien 06.4).
- Insérer scripts/styles **en dur** au lieu de `wp_enqueue_*`.
- Mettre une **fonctionnalité dans le thème** plutôt que dans un plugin (lien 08.1).

## 🔗 Ressources

- WordPress — *Plugin Handbook (sécurité)* :
  <https://developer.wordpress.org/plugins/security/>
- WP-CLI — *Documentation* : <https://wp-cli.org/fr/>
