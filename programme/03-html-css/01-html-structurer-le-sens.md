# 03.1 — HTML : structurer le sens

- **Thème :** 03 — HTML & CSS
- **Prérequis :** 01.3 (HTML/CSS/JS, le DOM)
- **Idée centrale :** le HTML décrit le **sens** d'un contenu (un titre, un paragraphe,
  une navigation), **pas** son apparence. Bien le penser, c'est déjà coder pour
  l'accessibilité et le référencement.

## 🎯 Objectifs

L'apprenant sait écrire un document HTML bien structuré et sémantique, et choisir
`id` ou `class` à bon escient.

## 📚 Notions à connaître

- 🎯 **HTML = structure + sens.** Chaque balise dit *ce qu'est* un contenu, pas comment
  il s'affiche (ça, c'est le CSS).
- 🎯 **Anatomie d'une balise.** Balise ouvrante/fermante, contenu, **attributs**
  (`<a href="...">`). Balises auto-fermantes (`<img>`, `<br>`).
- 🎯 **Structure d'un document.** `<!DOCTYPE html>`, `<html lang="fr">`, `<head>`
  (métadonnées, `<title>`, `<meta charset>`) et `<body>` (le contenu visible).
- 🎯 **Les balises sémantiques.** `header`, `nav`, `main`, `article`, `section`,
  `aside`, `footer` — *et pourquoi* : structure claire, accessibilité, SEO. Éviter le
  `<div>` partout (« divite »).
- 🎯 **La hiérarchie des titres.** Un seul `h1` par page, puis `h2`, `h3`… sans sauter
  de niveau. C'est un plan, pas une histoire de taille de texte.
- 🎯 **Liens et images.** `<a href>` (lien), `<img src alt>` (le `alt` décrit l'image
  pour l'accessibilité et si elle ne charge pas).
- 🎯 **`id` vs `class`.** `id` = **unique** dans la page (ancre `#`, cible de
  `label for`, hook JS précis) ; `class` = **réutilisable** (le hook normal du CSS).
- 📌 **Listes.** `<ul>` (non ordonnée), `<ol>` (ordonnée), `<li>` (élément). Une
  navigation est souvent une liste de liens.
- 📖 *(culture)* validation W3C, données structurées (schema.org), impact SEO.

## ✅ Critères de maîtrise

1. **Écrire la structure complète** d'une page HTML valide (doctype, head, body) avec
   des balises **sémantiques** adaptées.
2. Construire une **hiérarchie de titres** correcte sur un contenu donné.
3. Choisir et justifier **`id` ou `class`** sur des cas concrets.

## ⚠️ Pièges courants

- La **« divite »** : tout en `<div>` au lieu des balises sémantiques.
- Choisir un titre pour sa **taille** au lieu de son **niveau** (et casser la hiérarchie).
- Mettre **plusieurs fois le même `id`** dans une page (interdit, doit être unique).
- Oublier l'attribut **`alt`** sur les images, ou `lang` sur `<html>`.

## 🔗 Ressources

- MDN — *Les bases du HTML* :
  <https://developer.mozilla.org/fr/docs/Learn/Getting_started_with_the_web/HTML_basics>
- MDN — *HTML sémantique* :
  <https://developer.mozilla.org/fr/docs/Glossary/Semantics#sémantique_en_html>
