# Thème 08 — WordPress *(la spécialité)*

> **Le but :** maîtriser WordPress en **développeur**, pas en simple utilisateur :
> comprendre son architecture, l'étendre proprement (hooks, plugins), développer des
> **blocs Gutenberg**, travailler en **block theme**, et le connecter à React via son
> **API REST**. C'est le cœur du métier visé.

## Pourquoi ce thème est l'aboutissement de la spécialité

Tout ce qui précède converge ici : PHP (T06) fait tourner WordPress, les APIs (T07)
expliquent son API REST, React (T05) **est** la techno de l'éditeur Gutenberg, et HTML/CSS
(T03) structure ses thèmes. WordPress fait tourner une part énorme du web — savoir le
développer **proprement et en sécurité** est une compétence très demandée.

## Ce que l'apprenant saura faire à la fin

- Comprendre l'**architecture** WordPress (core / thèmes / plugins) et l'étendre via les **hooks**.
- Modéliser du contenu avec **CPT** et **taxonomies**.
- Lire un thème classique (**la Boucle**, hiérarchie de templates) et travailler en **block theme** (`theme.json`).
- Développer un **bloc Gutenberg** (statique et dynamique).
- Consommer et étendre l'**API REST WordPress**, y compris en **headless** avec React.
- Écrire un **plugin** sécurisé (nonces, capabilities, sanitization/escaping).
- **Optimiser** un site (chargement des assets, caches, requêtes) et le **durcir** côté sécurité.

## Chapitres

| # | Chapitre | Idée centrale |
|---|----------|---------------|
| 08.1 | L'écosystème WordPress | Core, thèmes, plugins : qui fait quoi |
| 08.2 | Les hooks : actions & filtres | Étendre WP sans toucher au core |
| 08.3 | Le contenu : posts, CPT & taxonomies | Modéliser ses données |
| 08.4 | La Boucle & la hiérarchie de templates | Comment un thème classique affiche |
| 08.5 | Block themes & `theme.json` | Le WordPress moderne (FSE) |
| 08.6 | Développer un bloc Gutenberg | Créer ses propres blocs (en React) |
| 08.7 | L'API REST WordPress & le pont React | Connecter WP et React (headless) |
| 08.8 | Plugins, sécurité & WP-CLI | Étendre proprement et en sécurité |

### Approfondissement *(avancé — au-delà des fondamentaux)*

| # | Chapitre | Idée centrale |
|---|----------|---------------|
| 08.9 | Optimiser le chargement des assets (*enqueue* avancé) | Charger juste ce qu'il faut, sans bloquer |
| 08.10 | `theme.json` & variations de style (`/styles/*.json`) | Piloter le design, décliner par overrides partiels |
| 08.11 | Performance & optimisation WordPress | Mesurer, cacher, optimiser requêtes & assets |
| 08.12 | Sécurité WordPress approfondie | Durcir sur tous les fronts (BDD, sorties, REST, config) |

> Prérequis : PHP & sécurité (T06), APIs/REST (T07), React (T05), HTML/CSS (T03).
> Les chapitres 08.9 → 08.12 approfondissent les fondamentaux (08.1 → 08.8).
