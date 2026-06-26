# 05.2 — Props & composition

- **Thème :** 05 — React
- **Prérequis :** 05.1, 04.3 (déstructuration)
- **Idée centrale :** un composant reçoit des données de son parent via les **props**, et
  une UI se construit en **assemblant** des composants. Les données circulent du haut
  vers le bas.

## 🎯 Objectifs

L'apprenant sait passer des données à un composant via les props et composer des
composants entre eux.

## 📚 Notions à connaître

- 🎯 **Les props.** Des paramètres passés du **parent à l'enfant** :
  `<Carte titre="Bonjour" />`. À l'intérieur, on les **lit** (elles sont en **lecture
  seule** — on ne les modifie jamais).
- 🎯 **Déstructurer les props.** `function Carte({ titre, prix }) { … }` (lien 04.3).
- 🎯 **Composer.** Un composant en **utilise** d'autres ; on construit un **arbre**
  (`App` → `Liste` → `Carte`).
- 🎯 **`children`.** Le contenu placé *entre* les balises d'un composant
  (`<Panneau>contenu</Panneau>`) est reçu via `props.children`.
- 🎯 **Le flux unidirectionnel.** Les données descendent (parent → enfant) ; pour
  « remonter », l'enfant appelle une **fonction reçue en prop** (callback).
- 📌 **Props par défaut** et props de type **fonction** (pour réagir à un événement
  enfant).
- 📖 *(culture)* le **prop drilling** (passer une prop à travers plusieurs niveaux) et
  pourquoi `useContext` existera (05.7).

## ✅ Critères de maîtrise

1. **Créer un composant paramétré** par des props et l'utiliser plusieurs fois avec des
   valeurs différentes.
2. **Composer** au moins deux niveaux de composants.
3. Expliquer pourquoi les props sont **en lecture seule** et comment « remonter » une
   info au parent (callback).

## ⚠️ Pièges courants

- **Modifier une prop** dans l'enfant (interdit : lecture seule).
- Confondre **props** (viennent du parent) et **state** (interne au composant, 05.3).
- Oublier de **déstructurer** et écrire `props.props.x`.
- Passer trop de props à travers de nombreux niveaux (signal de revoir la structure).

## 🔗 Ressources

- React — *Passer des props à un composant* :
  <https://fr.react.dev/learn/passing-props-to-a-component>
- React — *Penser en React* : <https://fr.react.dev/learn/thinking-in-react>
