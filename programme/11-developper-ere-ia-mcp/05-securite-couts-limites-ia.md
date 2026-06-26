# 11.5 — Sécurité, coûts & limites de l'IA

- **Thème :** 11 — Développer à l'ère de l'IA *(capstone)*
- **Prérequis :** 11.1, 06.4 (sécurité), 10.2 (secrets)
- **Idée centrale :** l'IA est un outil formidable **et** faillible. Garder l'**esprit
  critique**, vérifier, et connaître ses limites est ce qui sépare un usage professionnel
  d'un usage naïf.

## 🎯 Objectifs

L'apprenant connaît les principales limites et risques de l'IA et adopte les réflexes pour
les gérer.

## 📚 Notions à connaître

- 🎯 **Les hallucinations.** L'IA peut **inventer** avec aplomb : une fonction qui n'existe
  pas, une API imaginaire, une « source » fausse. Toujours **vérifier**, surtout sur du
  code critique ou de la sécurité.
- 🎯 **Vérifier systématiquement.** Lire, exécuter, **tester** (Thème 09). La confiance se
  donne au résultat vérifié, pas à l'outil.
- 🎯 **Secrets & données sensibles.** Ne jamais confier de mots de passe, clés, ou données
  confidentielles à un service IA externe sans précaution (lien 06.4, 10.2).
- 📌 **Le coût.** Les appels IA se paient (à l'usage, en « tokens ») : un agent qui boucle
  ou un contexte énorme coûtent vite. En avoir conscience.
- 📌 **Responsabilité & éthique.** Qui est responsable du code généré ? Quelle **licence** ?
  Quels **biais** ? Attention aussi à la **dépendance** : savoir faire **sans** l'IA reste
  la base (d'où tout ce parcours).
- 📖 *(culture)* la régulation de l'IA, l'évolution très rapide du domaine (les outils
  d'aujourd'hui changeront — les **principes**, eux, restent).

## ✅ Critères de maîtrise

1. Expliquer ce qu'est une **hallucination** et donner un réflexe pour s'en prémunir.
2. Citer **ce qu'on ne confie jamais** à une IA externe et pourquoi.
3. Avoir conscience du **coût** (tokens) et de la question de **responsabilité** du code généré.

## ⚠️ Pièges courants

- **Faire confiance aveuglément** à une réponse plausible mais fausse.
- **Coller du code** non vérifié en production (lien 11.1).
- **Exposer des secrets** ou du code confidentiel à un service externe.
- **Dépendre** de l'IA au point de ne plus savoir faire soi-même — l'IA augmente un
  développeur compétent, elle ne le remplace pas.

## 🔗 Ressources

- *Limites des LLM / hallucinations* — documentation des fournisseurs d'IA.
- Renvoi interne : [06.4 — La sécurité serveur](../06-php-bases-serveur/04-securite-serveur.md),
  [10.2 — Les environnements](../10-architecture-ops/02-les-environnements.md).
