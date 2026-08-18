# Calculateur de protéines — installation sur Android

Cette app est une PWA (web app installable). Pour l'avoir comme une vraie icône sur ton téléphone, avec sauvegarde fiable des données, il faut l'héberger quelque part (le simple fait d'ouvrir le fichier `index.html` depuis le stockage du téléphone ne suffit pas : Android a besoin d'une adresse `https://` pour installer l'icône et activer le mode hors-ligne).

## Le plus simple : Netlify Drop (gratuit, 2 minutes, sans compte)

1. Va sur https://app.netlify.com/drop depuis un ordinateur.
2. Fais glisser le dossier `prot-app` (celui qui contient `index.html`, `manifest.json`, etc.) dans la page.
3. Netlify te donne une adresse du type `https://un-nom-au-hasard.netlify.app`.
4. Ouvre cette adresse sur ton téléphone Android, dans Chrome.
5. Chrome propose "Ajouter à l'écran d'accueil" ou "Installer l'application" (icône ⋮ en haut à droite → "Installer l'application"). Accepte.
6. L'icône apparaît sur ton écran d'accueil, l'app s'ouvre en plein écran comme une vraie app.

## Alternative : GitHub Pages

Si tu as déjà un compte GitHub : crée un dépôt, mets-y les fichiers de `prot-app`, active GitHub Pages dans les paramètres du dépôt, puis ouvre l'adresse fournie sur ton téléphone et installe comme ci-dessus.

## Données

Tout est stocké **uniquement sur ton téléphone** (dans le stockage local du navigateur), rien n'est envoyé sur un serveur. Si tu changes de téléphone ou vides le cache du navigateur, l'historique sera perdu — pense à ne pas nettoyer les données du site depuis les réglages Chrome.

## Fichiers du dossier

- `index.html` — l'app (calendrier, profil, repas, shaker, bonhomme)
- `manifest.json` — nom, icône et couleurs pour l'installation Android
- `service-worker.js` — permet le fonctionnement hors-ligne une fois installée
- `icons/` — icônes de l'app
