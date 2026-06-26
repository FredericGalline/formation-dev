# Programme — la carte complète

Parcours de **développeur web débutant** → **junior solide (~bac+2)**, spécialité
**WordPress + React**, teinte full-stack. Long et progressif, c'est assumé.

## Comment lire ce programme

- Le parcours est découpé en **11 thèmes** → chacun en **chapitres** (un fichier `.md`
  par chapitre) → chaque chapitre liste des **notions** taguées par importance.
- L'ordre des thèmes est pensé pour que chacun arme le suivant (JS arme React, PHP
  arme WordPress, l'API REST relie les deux).

### Tags d'importance des notions

| Tag | Sens | Bloque la progression ? |
|-----|------|--------------------------|
| 🎯 **Fondamental** | Obligatoire, cœur de métier | **Oui** |
| 📌 **Utile** | À pratiquer | Non |
| 📖 **Culture** | Sensibilisation | Non |

### Statuts de progression (voir `progression/etat.md`)

🔴 non commencé · 🟡 en cours · 🟢 acquis · 🔁 à revoir

---

## Les 11 thèmes

### Thème 01 — Comment marche le web  ✅ *(rédigé)*
Les fondations mentales avant d'écrire la moindre ligne.
- 01.1 Le web : client, serveur, requête/réponse
- 01.2 HTTP & les URL
- 01.3 Le navigateur, le rendu et le DOM
- 01.4 Statique vs dynamique, front vs back
- 01.5 La sécurité de base (pourquoi HTTPS)

### Thème 02 — Outils du développeur  ✅ *(rédigé)*
L'atelier du dev, à maîtriser avant d'écrire du code pour de vrai.
- 02.1 VSCode : l'éditeur du développeur
- 02.2 Le terminal & le système de fichiers
- 02.3 Git : versionner son travail (en local)
- 02.4 Git & GitHub : travailler à plusieurs (branches, PR, conflits)
- 02.5 Gestionnaires de paquets : npm & composer
- 02.6 Workflows Git & conventions (PR=MR, GitHub Flow / Git Flow, Conventional Commits, tags)
- *(les devtools du navigateur sont vus en 01.3 et approfondis au Thème 04)*

### Thème 03 — HTML & CSS  ✅ *(rédigé)*
Structurer (HTML) et mettre en forme (CSS), sens et accessibilité en tête.
- 03.1 HTML : structurer le sens (sémantique, titres, `id` vs `class`, a11y)
- 03.2 HTML : tableaux & formulaires (accessibles)
- 03.3 CSS : les fondamentaux (cascade, spécificité, nommage des classes)
- 03.4 CSS : le box model & les unités
- 03.5 CSS : la mise en page (Flexbox & Grid, responsive)
- 03.6 CSS : variables & design tokens *(culture : SCSS, Tailwind)*

### Thème 04 — JavaScript moderne  ✅ *(rédigé)*
Le langage du web, socle direct de React.
- 04.1 Les bases du langage
- 04.2 Tableaux & objets (`map`/`filter`/`reduce`)
- 04.3 JavaScript moderne (ES6+) & modules
- 04.4 Le DOM & les événements
- 04.5 L'asynchrone : promesses, `async/await` & `fetch` (API REST)
- 04.6 Déboguer & outiller son JS *(devtools ; culture : TypeScript, ESLint/Prettier)*

### Thème 05 — React *(cœur de la spécialité)*  ✅ *(rédigé)*
Construire des interfaces interactives et réutilisables.
- 05.1 Pourquoi React, composants & JSX
- 05.2 Props & composition
- 05.3 Le state & l'interactivité (`useState`)
- 05.4 Listes & rendu conditionnel
- 05.5 Les formulaires contrôlés
- 05.6 Les effets & consommer une API (`useEffect`) — pont vers WordPress
- 05.7 Aller plus loin *(useContext/useRef/useMemo, routing ; culture : Next.js, état global, React Query)*

### Thème 06 — PHP & bases serveur  ✅ *(rédigé)*
Le côté serveur, socle direct de WordPress.
- 06.1 PHP : les bases du langage
- 06.2 PHP & le web (formulaires, superglobales)
- 06.3 La POO en PHP
- 06.4 La sécurité serveur (valider, échapper, requêtes préparées)
- 06.5 Bases de données & SQL (intro)

### Thème 07 — APIs & intégrations  ✅ *(rédigé)*
Le langage par lequel les applications se parlent.
- 07.1 Qu'est-ce qu'une API & REST
- 07.2 L'authentification des APIs (clés, tokens/JWT, OAuth)
- 07.3 Consommer une API tierce robustement (erreurs, pagination, *rate limit*)
- 07.4 Concevoir & exposer sa propre API (endpoints, statuts, versioning, CORS)
- 07.5 Documentation, webhooks & GraphQL

### Thème 08 — WordPress *(la spécialité)*  ✅ *(rédigé)*
Le cœur du métier : développer WordPress proprement et en sécurité.
- 08.1 L'écosystème WordPress (core / thèmes / plugins)
- 08.2 Les hooks : actions & filtres
- 08.3 Le contenu : posts, CPT & taxonomies
- 08.4 La Boucle & la hiérarchie de templates
- 08.5 Block themes & `theme.json`
- 08.6 Développer un bloc Gutenberg (en React)
- 08.7 L'API REST WordPress & le pont React (headless)
- 08.8 Plugins, sécurité & WP-CLI
- *Approfondissement :* 08.9 *enqueue* avancé · 08.10 `theme.json` & variations (`/styles/*.json`) · 08.11 performance & optimisation · 08.12 sécurité approfondie

### Thème 09 — Qualité & méthode  ✅ *(rédigé)*
Passer de « ça marche » à « c'est bien fait ».
- 09.1 Écrire du code lisible
- 09.2 La revue de code
- 09.3 Les tests : pourquoi & les types (unitaire / intégration / E2E)
- 09.4 Écrire ses premiers tests (JS & PHP)
- 09.5 Déboguer & se débrouiller

### Thème 10 — Architecture & Ops *(sensibilisation)*  ✅ *(rédigé)*
Prendre de la hauteur : concevoir, et comprendre où tourne le code.
- 10.1 Penser avant de coder : architecture (responsabilités, dette technique)
- 10.2 Les environnements (local/staging/prod, config & secrets)
- 10.3 Build, intégration & déploiement (CI/CD)
- 10.4 Docker & l'hébergement (conteneurs, serveur, DNS)
- 10.5 Observabilité, sécurité & performance

### Thème 11 — Développer à l'ère de l'IA : MCP & assistants  ✅ *(rédigé)*
Utiliser l'IA comme accélérateur, en restant responsable et lucide.
- 11.1 Travailler avec un assistant de code (garde-fous)
- 11.2 Qu'est-ce que le MCP (Model Context Protocol)
- 11.3 Serveurs & clients MCP
- 11.4 Agents IA & *tool use*
- 11.5 Sécurité, coûts & limites de l'IA

---

> Thèmes **01 → 05 rédigés** ; ils servent de gabarit de référence. Les thèmes 06 → 11
> seront écrits au même grain au fur et à mesure.
