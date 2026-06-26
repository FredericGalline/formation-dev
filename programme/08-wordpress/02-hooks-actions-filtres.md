# 08.2 — Les hooks : actions & filtres

- **Thème :** 08 — WordPress
- **Prérequis :** 08.1, 06.1 (fonctions PHP)
- **Idée centrale :** les **hooks** sont le mécanisme central d'extensibilité de
  WordPress : ils permettent de **se brancher** sur le déroulement de WP pour exécuter
  son code, **sans jamais modifier le core**.

## 🎯 Objectifs

L'apprenant comprend et sait utiliser les actions et les filtres pour étendre WordPress.

## 📚 Notions à connaître

- 🎯 **Le principe.** WordPress déclenche des **points d'accroche** (hooks) tout au long
  de son exécution ; ton code s'y « accroche » pour intervenir.
- 🎯 **Les actions.** *Faire quelque chose* à un moment donné : `add_action('init',
  'ma_fonction')`. Ne renvoient rien, exécutent un effet.
- 🎯 **Les filtres.** *Modifier une valeur* qui transite : `add_filter('the_content',
  'ma_fonction')`. **Reçoivent une valeur, en retournent une** (transformée).
- 🎯 **Des hooks courants.** `init`, `wp_enqueue_scripts` (charger CSS/JS),
  `the_content`, `save_post`… Savoir qu'il en existe des centaines, et où chercher.
- 🎯 **Priorité & arguments.** Le 3e param (priorité) ordonne l'exécution ; le 4e
  (nombre d'arguments) précise ce que la fonction reçoit.
- 📌 **Créer ses propres hooks.** `do_action()` / `apply_filters()` pour rendre **son**
  code extensible à son tour.
- 📖 *(culture)* le « plugin API » de WP, pourquoi ce design rend WordPress si extensible.

## ✅ Critères de maîtrise

1. **Brancher une action** sur un hook (ex. charger un script via `wp_enqueue_scripts`).
2. **Modifier une valeur via un filtre** (et bien **retourner** la valeur).
3. Expliquer la différence **action vs filtre**.

## ⚠️ Pièges courants

- Confondre **action** (effet) et **filtre** (transforme et **retourne** une valeur).
- **Oublier le `return`** dans un filtre → la valeur devient vide/cassée.
- Mauvaise **priorité** → le code s'exécute trop tôt/tard.
- Modifier le core « parce que c'est plus simple » au lieu d'utiliser un hook.

## 🔗 Ressources

- WordPress — *Hooks (Plugin Handbook)* :
  <https://developer.wordpress.org/plugins/hooks/>
- WordPress — *Actions vs Filters* :
  <https://developer.wordpress.org/plugins/hooks/actions/>
