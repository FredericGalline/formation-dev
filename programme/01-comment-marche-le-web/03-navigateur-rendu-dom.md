# 01.3 — Le navigateur, le rendu et le DOM

- **Thème :** 01 — Comment marche le web
- **Prérequis :** 01.1, 01.2
- **Idée centrale :** le navigateur **reçoit du texte (HTML)** et le transforme en une
  **page vivante (le DOM)** qu'on voit et qu'on peut manipuler.

## 🎯 Objectifs

L'apprenant comprend le rôle du navigateur, distingue les trois langages du web et
sait ce qu'est le DOM — la notion qui reviendra sans cesse en JS et en React.

## 📚 Notions à connaître

- 🎯 **Le rôle du navigateur.** Il télécharge les fichiers, les **interprète** et
  **affiche** la page. C'est un programme qui lit du code et dessine un résultat.
- 🎯 **Les trois langages et leurs rôles.**
  - **HTML** = la **structure** et le **sens** (le squelette),
  - **CSS** = le **style** (l'apparence),
  - **JavaScript** = le **comportement** (l'interactivité).
- 🎯 **Le DOM (Document Object Model).** Quand le navigateur lit le HTML, il en
  construit une **représentation en arbre** en mémoire : le DOM. La page affichée est
  le rendu de cet arbre.
- 🎯 **HTML ≠ DOM.** Le HTML est le texte de départ ; le DOM est l'arbre vivant qui en
  résulte et que JavaScript peut modifier *après* le chargement.
- 📌 **Les devtools.** Savoir ouvrir l'inspecteur (clic droit → Inspecter), survoler un
  élément, repérer l'onglet **Réseau** (les requêtes) et la **Console**.
- 📖 *(culture)* **Le moteur de rendu.** Idée générale du chemin HTML → DOM → calcul du
  style → mise en page → peinture à l'écran.

## ✅ Critères de maîtrise

1. **Ouvrir les devtools** et **inspecter un élément** d'une vraie page.
2. Expliquer **avec ses mots** ce qu'est le DOM (un arbre construit à partir du HTML).
3. Donné un bout de page, **attribuer chaque responsabilité** au bon langage
   (structure → HTML, couleur → CSS, clic → JS).

## ⚠️ Pièges courants

- Confondre **HTML** (le texte source) et **DOM** (l'arbre en mémoire) — distinction
  clé pour comprendre plus tard pourquoi JS « modifie la page sans recharger ».
- Croire que le CSS ou le JS « font partie » du HTML : ce sont des couches distinctes.
- Ne pas savoir que les **devtools** existent → se priver du meilleur outil de débogage.

## 🔗 Ressources

- MDN — *Qu'est-ce que le DOM ?* :
  <https://developer.mozilla.org/fr/docs/Web/API/Document_Object_Model/Introduction>
- MDN — *Découvrir les outils de développement du navigateur* :
  <https://developer.mozilla.org/fr/docs/Learn/Common_questions/Tools_and_setup/What_are_browser_developer_tools>
