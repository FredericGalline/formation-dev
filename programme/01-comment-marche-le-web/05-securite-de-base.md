# 01.5 — La sécurité de base (pourquoi HTTPS)

- **Thème :** 01 — Comment marche le web
- **Prérequis :** 01.2 (HTTP/HTTPS), 01.4
- **Idée centrale :** comprendre **pourquoi** le web doit être chiffré — sans entrer
  dans la cryptographie. Les réflexes sécu approfondis viennent en T06 et T09.

## 🎯 Objectifs

L'apprenant sait expliquer à quoi sert HTTPS, repérer un site non sécurisé, et a une
première conscience que des données peuvent être interceptées ou attaquées.

## 📚 Notions à connaître

- 🎯 **Pourquoi HTTPS.** En HTTP simple, les échanges circulent **en clair** : n'importe
  quel intermédiaire sur le chemin peut les lire ou les modifier. HTTPS **chiffre** la
  communication → confidentialité et intégrité.
- 🎯 **HTTP vs HTTPS, ce qui change concrètement.** Le cadenas dans la barre d'adresse,
  le `https://`, la confiance de l'utilisateur, et le fait que les données saisies
  (mot de passe, paiement) ne transitent plus en clair.
- 📌 **Cadenas & certificat.** Le certificat prouve l'**identité** du site (c'est bien
  `mabanque.fr`) et permet le chiffrement. Savoir que c'est délivré par une autorité.
- 📌 **Données sensibles.** Ne jamais faire transiter ou stocker un mot de passe en
  clair ; première intuition de « ce qui est sensible ».
- 📖 *(culture)* **Les grandes familles d'attaques web.** Juste **savoir qu'elles
  existent** : injection (ex. SQL), **XSS** (script injecté dans une page), hameçonnage.
  Le *comment s'en protéger* est détaillé en T06 (PHP/sécurité) et T07 (WordPress).

## ✅ Critères de maîtrise

1. Expliquer **avec ses mots** pourquoi un site, surtout avec formulaire/connexion,
   **doit** être en HTTPS.
2. **Repérer** un site non sécurisé (absence de cadenas / `http://`) et dire le risque
   concret.
3. Citer **au moins une** raison de ne jamais envoyer un mot de passe en clair.

## ⚠️ Pièges courants

- Croire que « le cadenas = le site est honnête / sans virus ». Le cadenas garantit le
  **chiffrement et l'identité du domaine**, pas la bonne foi de son propriétaire.
- Penser que HTTPS est « optionnel » pour un petit site (aujourd'hui c'est le standard,
  y compris pour le SEO et la confiance).
- Sous-estimer le risque du Wi-Fi public en HTTP simple.

## 🔗 Ressources

- MDN — *À propos de HTTPS / sécurité* :
  <https://developer.mozilla.org/fr/docs/Web/Security>
- MDN — *Transport Layer Security (TLS)* :
  <https://developer.mozilla.org/fr/docs/Web/Security/Transport_Layer_Security>
