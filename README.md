# TIPS-IA

Site statique du réseau TIPS-IA.

## Structure

- `index.html` : page d'accueil (bannière, logo, boutons)
- `reseau.html` : Réseau, avec `reseau-presentation.html`, `reseau-gouvernance.html`, `reseau-projets-finances.html`
- `actions.html` : Actions par année (`actions-2026.html`, `actions-2025.html`)
- `videos.html` : liens vers les vidéos
- `outils-tutos.html` : outils et tutoriels
- `rejoindre.html` : rejoindre TIPS-IA
- `css/style.css` : feuille de style commune
- `assets/` : logo (`logo.svg`) et images

## Ajouter une année d'actions

1. Copier `actions-2025.html` et renommer la copie (ex. `actions-2027.html`).
2. Mettre à jour le titre et le fil d'Ariane.
3. Ajouter un bouton dans `actions.html`.

## Mise en ligne (GitHub Pages)

Dans les paramètres du dépôt : **Settings → Pages**, source : branche `main`, dossier `/ (root)`.
