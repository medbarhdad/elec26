# Élections législatives marocaines — projet modulaire

## Organisation

- `index.html` : structure et contenu de la page.
- `assets/css/styles.css` : styles CSS séparés.
- `assets/js/config.js` : **paramètres JavaScript principaux du taux, des inscrits et du compteur**.
- `assets/js/app.min.js` : logique JavaScript minifiée, chargement des configurations et alimentation des graphiques.
- `config/participation.json` : données JSON complémentaires des graphiques et de la participation.
- `config/age.json` : données du graphique des tranches d’âge.
- `config/representation.json` : données sexe et milieu de résidence.
- `config/votes.json` : voix par parti et par année.
- `config/seats.json` : sièges par parti et variations.

## Mise à jour du taux de participation

Modifier `assets/js/config.js` : `participationRate` règle le taux ; `inscrits` sert au calcul ; `votersMode: "auto"` calcule automatiquement `votants = inscrits × taux / 100` ; `electionDate`, `openingTime` et `closingTime` configurent le compteur. Pour 23 %, 15 801 162 inscrits, le site calcule automatiquement environ 3 634 267 votants. Pour un hébergement, conserver la structure des dossiers et recharger la page avec Ctrl + F5.

## Protection du code

Un navigateur doit recevoir le HTML, le CSS, le JavaScript et les données pour afficher la page ; il est donc impossible de rendre le code réellement secret ou impossible à copier côté client. La distribution peut toutefois être durcie avec minification, obfuscation et un serveur qui protège les fichiers de configuration. Cette version reste lisible et maintenable pour permettre la mise à jour des données.

## Déploiement

Téléverser tout le dossier en conservant sa structure, puis ouvrir `index.html` depuis le domaine ou le serveur web.
