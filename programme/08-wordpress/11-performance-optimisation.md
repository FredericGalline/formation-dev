# 08.11 — Performance & optimisation WordPress

- **Thème :** 08 — WordPress *(approfondissement)*
- **Prérequis :** 08.4 (`WP_Query`), 08.9 (assets), 06.5 (BDD)
- **Idée centrale :** un site WordPress lent coûte cher (SEO, conversion, serveur). On
  optimise **avec méthode** : mesurer d'abord, puis agir sur les caches, les requêtes et
  les assets.

## 🎯 Objectifs

L'apprenant connaît les principaux leviers de performance WordPress et sait mesurer avant
d'optimiser.

## 📚 Notions à connaître

- 🎯 **Mesurer d'abord.** **Query Monitor** (requêtes SQL, hooks, temps, requêtes
  lentes), l'en-tête **Server-Timing**, les **Core Web Vitals**. On n'optimise pas « à
  l'œil ».
- 🎯 **Les caches.** **Page cache** (servir du HTML prêt), **object cache persistant**
  (Redis/Memcached, pour les requêtes), et l'**API Transients** (mettre en cache un
  résultat coûteux avec une expiration).
- 🎯 **Optimiser les requêtes.** `WP_Query` raisonnée (`posts_per_page`, `fields`,
  `no_found_rows` quand la pagination est inutile) ; **éviter les requêtes dans la
  Boucle** (problème **N+1**).
- 🎯 **Les options *autoloaded*.** Les options `autoload = yes` sont chargées **à chaque
  requête** : trop d'options autoloadées (souvent laissées par des plugins) plombent les
  perfs. À surveiller.
- 🎯 **Les assets & images.** Charger juste ce qu'il faut (08.9), **lazy loading** natif
  des images, bons formats/tailles, minimiser le nombre de requêtes HTTP.
- 📌 **Cron & appels externes.** Le **WP-Cron** (déclenché par le trafic) vs un vrai cron
  système ; attention aux **appels HTTP externes** bloquants dans le rendu.
- 📌 **Limiter & auditer les plugins.** Chaque plugin a un coût ; mesurer son impact.
- 📖 *(culture)* CDN, **cache de bord** (Varnish/edge) ; piège classique : un cache pleine
  page qui **ne varie pas selon le consentement** de l'utilisateur (cf. RGPD).

## ✅ Critères de maîtrise

1. **Identifier une requête coûteuse** ou une page lente avec Query Monitor.
2. **Mettre en cache** un résultat coûteux avec un **transient** (et gérer son expiration).
3. Expliquer le risque des **options *autoloaded*** et du problème **N+1**.

## ⚠️ Pièges courants

- **Requêtes lourdes dans la Boucle** (N+1) au lieu d'une requête groupée.
- **Transients** jamais expirés/invalidés (données périmées servies).
- Trop d'**options autoloadées** qui ralentissent **chaque** requête.
- Optimiser **sans mesurer** → effort gaspillé au mauvais endroit.

## 🔗 Ressources

- WordPress — *Optimization (performance)* :
  <https://developer.wordpress.org/advanced-administration/performance/optimization/>
- WordPress — *Transients API* :
  <https://developer.wordpress.org/apis/transients/>
