# 10.5 — Observabilité, sécurité & performance

- **Thème :** 10 — Architecture & Ops *(sensibilisation)*
- **Prérequis :** 06.4 / 08.12 (sécurité), 08.11 (performance)
- **Idée centrale :** une fois en production, il faut **savoir ce qui se passe** (logs,
  monitoring) et garder des **réflexes** de sécurité et de performance. Un site livré
  n'est pas un site oublié.

## 🎯 Objectifs

L'apprenant comprend l'intérêt de l'observabilité et connaît les réflexes sécu/perf en
production.

## 📚 Notions à connaître

- 🎯 **Les logs.** Tracer ce qui se passe (erreurs, événements) pour **diagnostiquer** un
  problème *a posteriori*. Sans logs, déboguer en prod, c'est à l'aveugle.
- 🎯 **Monitoring & observabilité.** Surveiller la **santé** du système : disponibilité,
  taux d'erreurs, temps de réponse. Savoir si « tout va bien » en continu.
- 🎯 **Réflexes sécurité en prod.** HTTPS partout (01.5), tout **garder à jour**, secrets
  hors du code (10.2), **moindre privilège** (recap transverse 06.4 / 08.12).
- 🎯 **Réflexes performance.** **Mesurer** avant d'optimiser, mettre en **cache** ce qui
  peut l'être (recap transverse 08.11), surveiller les Core Web Vitals.
- 📌 **Les sauvegardes.** Des **backups** réguliers **et testés** (une sauvegarde qu'on ne
  sait pas restaurer ne vaut rien).
- 📌 **L'alerting.** Être **prévenu automatiquement** quand quelque chose casse, avant les
  utilisateurs.
- 📖 *(culture)* APM, **SLO/SLA**, *post-mortems* (apprendre des incidents sans blâmer).

## ✅ Critères de maîtrise

1. Expliquer à quoi servent **logs** et **monitoring** et leur différence.
2. Citer **trois réflexes de sécurité** en production.
3. Citer **trois réflexes de performance** et l'importance des **sauvegardes**.

## ⚠️ Pièges courants

- **Pas de logs** → impossible de comprendre un incident en production.
- **Pas de sauvegardes** (ou jamais testées) → perte de données irréversible.
- Découvrir une panne **par les utilisateurs** faute d'alerting.
- Laisser traîner du **HTTP**, des dépendances **obsolètes** ou des **secrets** en prod.

## 🔗 Ressources

- Google SRE — *Monitoring Distributed Systems* (en, culture) :
  <https://sre.google/sre-book/monitoring-distributed-systems/>
- web.dev — *Core Web Vitals* : <https://web.dev/articles/vitals?hl=fr>
