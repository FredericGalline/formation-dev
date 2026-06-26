# Thème 07 — APIs & intégrations

> **Le but :** comprendre, **consommer** et **concevoir** des APIs. C'est le langage par
> lequel les applications se parlent — entre ton front React et ton back, avec des
> services tiers, et au cœur de WordPress (API REST).

## Pourquoi ce thème

On a déjà *consommé* une API au passage (`fetch` en 04.5, `useEffect` en 05.6). Mais les
APIs méritent un traitement à part entière : c'est la compétence pivot d'un profil
full-stack en 2026. Savoir lire une doc, s'authentifier, gérer erreurs et pagination,
puis **exposer** sa propre API proprement — voilà ce qui sépare un intégrateur d'un vrai
développeur d'applications connectées.

## Ce que l'apprenant saura faire à la fin

- Expliquer ce qu'est une **API REST** et ses conventions.
- S'**authentifier** auprès d'une API (clé, token/JWT, OAuth — notions).
- **Consommer** une API tierce de façon robuste (erreurs, pagination, *rate limit*).
- **Concevoir et exposer** une API REST cohérente (endpoints, statuts, versioning, CORS).
- Lire une **documentation** (OpenAPI/Swagger) et comprendre les **webhooks**.

## Chapitres

| # | Chapitre | Idée centrale |
|---|----------|---------------|
| 07.1 | Qu'est-ce qu'une API & REST | Le contrat d'échange entre programmes |
| 07.2 | L'authentification des APIs | Prouver qui appelle, protéger l'accès |
| 07.3 | Consommer une API tierce robustement | Gérer le réel : erreurs, pagination, limites |
| 07.4 | Concevoir & exposer sa propre API | Penser en ressources, répondre proprement |
| 07.5 | Documentation, webhooks & GraphQL | Contractualiser, être notifié, ouvrir l'horizon |

> Prérequis : HTTP & URL (01.2), `fetch`/async (04.5), et le côté serveur + sécurité
> (Thème 06). Ce thème prépare directement l'**API REST de WordPress** (Thème 08).
