# 🎓 Formation Dev Web — WordPress + React (pilotée par IA)

Une formation de développeur web qui ne vit que dans des fichiers Markdown, et dont
le **formateur est une IA**. Pas de logiciel à installer, pas de plateforme, pas de
vidéos : tu ouvres ce dépôt dans **VSCode**, tu parles à ton assistant IA, et il
devient ton **tuteur personnel**. Il sait où tu en es, ce que tu maîtrises, ce qui
coince, et il t'accompagne pas à pas.

**Objectif :** partir de **zéro** et atteindre un niveau **junior solide (~bac+2)**,
spécialisé **WordPress + React**, avec une teinte full-stack. Le parcours est long et
progressif — c'est assumé.

> 💡 **L'idée de départ :** pendant que l'IA travaille pour toi sur tes autres projets,
> profite de ce temps pour **monter en compétence** — plutôt que d'aller scroller sur
> Instagram. 😏

## À quoi ça sert

Faire monter en compétence un développeur, à son rythme, avec un accompagnement
**personnalisé** et **persistant**. Contrairement à un cours figé :

- l'IA **se met à ta portée** : elle connaît le programme et apprend peu à peu *ton*
  niveau ;
- elle **se souvient** de tout d'une session à l'autre (notions acquises, points
  fragiles) grâce à des fichiers de mémoire ;
- elle **te fait pratiquer** (exercices, QCM, débogage, questions) au lieu de te faire
  lire ;
- on **n'avance que quand une notion est acquise**, pas quand le chrono le dit.

## Comment ça marche

Le dépôt sépare deux choses :

- **`programme/`** — le référentiel de la formation : thèmes → chapitres → notions à
  acquérir, chacune marquée 🎯 fondamentale / 📌 utile / 📖 culture. C'est figé : *le
  manuel*. La carte complète est dans [`programme/00-index.md`](programme/00-index.md).
- **`progression/`** — **ta** mémoire d'apprenant : ton profil, ton état d'avancement,
  ton journal de bord. L'IA y lit **et y écrit** à chaque séance.

L'IA improvise la pédagogie à partir du référentiel ; ta progression, elle, est
sauvegardée dans des fichiers que tu gardes (et que tu peux commiter).

## Installation

### Prérequis

- un compte **GitHub** ;
- **git** et **VSCode** installés ;
- un **assistant IA dans VSCode** — ce dépôt est optimisé pour **Claude Code**
  (le fichier `CLAUDE.md` est lu automatiquement), mais il fonctionne avec n'importe
  quel assistant qui lit `AGENTS.md`.

### Étapes

1. **« Use this template » → Create a new repository**, et coche **Private**.
   Tu obtiens **ta** copie personnelle et privée (ton carnet de progression rien qu'à
   toi). *(Le bouton « Fork » marche aussi, mais un fork de dépôt public reste public :
   préfère « Use this template » pour rester en privé.)*
2. **Clone** ta copie privée sur ta machine :
   ```bash
   git clone https://github.com/<ton-compte>/<ton-repo>.git
   cd <ton-repo>
   ```
3. **Ouvre le dossier dans VSCode.**
4. **Lance ton assistant IA** (Claude Code) dans ce dossier.

## Utilisation

Une fois dans VSCode avec ton assistant, dis simplement :

> **« Regarde où on en est de mon accompagnement, et continuons. »**

L'IA lit ta mémoire de progression, fait le point, et reprend là où vous vous étiez
arrêtés. C'est tout.

- **Première séance :** l'IA fait un court **entretien de positionnement** (prénom,
  objectif, niveau, dispo) pour remplir ton profil, puis démarre le Thème 01.
- **Séances suivantes :** elle reprend le fil, te propose la suite, t'enseigne, te fait
  pratiquer, t'évalue, **met à jour ta mémoire**, et annonce la prochaine étape.

## Conseils

- **Sois honnête** avec l'IA : c'est en butant qu'on apprend. Demande des indices
  plutôt que la réponse toute faite.
- **Régularité > intensité.** Mieux vaut 30 min régulières que 4 h une fois par mois.
- **Commite ta progression** de temps en temps : ton journal raconte ton parcours.

## Structure du dépôt

```
CLAUDE.md       → le « cerveau » du tuteur (lu automatiquement par Claude Code)
AGENTS.md       → mêmes instructions, pour tout autre assistant IA
programme/      → le référentiel figé (00-index.md = la carte complète)
progression/    → ta mémoire (profil.md · etat.md · competences.md · journal.md)
```

---

*Bonne montée en compétence. Et n'oublie pas : l'IA bosse, toi tu apprends. 🚀*
