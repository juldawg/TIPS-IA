# TIPS-IA

Site du réseau TIPS-IA, généré avec Jekyll (intégré à GitHub Pages) et alimenté par le CMS Décap.

## Ajouter ou modifier du contenu (éditeurs)

Ouvrir `https://juldawg.github.io/TIPS-IA/admin/` et se connecter avec un compte GitHub ayant accès au dépôt.

- **Actions** : titre, année, date, image, résumé, texte. Les actions sont classées par année automatiquement.
- **Vidéos**, **Outils et Tutos**, **Projets financés** : titre, lien, résumé.
- **Accueil** : bannière et bloc « À la une ».
- **Pages** : Rejoindre TIPS-IA, Présentation et Gouvernance.

Chaque enregistrement crée un fichier dans le dépôt. Le site se met à jour après la publication (quelques minutes).

## Structure

- `_config.yml` : titre, adresse du site et collections.
- `_layouts/` : gabarits des pages (`default`, `page`, `entree`).
- `_includes/` : en-tête et pied de page.
- `_actions/`, `_videos/`, `_outils/`, `_projets/` : contenus gérés par le CMS.
- `_data/accueil.yml` : textes de la page d'accueil.
- `index.html`, `actions.md`, `videos.md`, `outils-tutos.md`, `rejoindre.md`, `reseau.md`, `reseau/` : pages du site.
- `admin/` : interface d'administration Décap (`config.yml` définit les champs).
- `assets/uploads/` : images envoyées depuis le CMS.
- `css/style.css` : feuille de style.

## Mise en service (une fois, côté responsable du site)

1. **Compte GitHub** : chaque éditeur doit créer un compte GitHub gratuit et être ajouté comme collaborateur du dépôt (Settings → Collaborators).
2. **Authentification** : créer une « OAuth App » sur GitHub (Settings développeur → OAuth Apps), avec pour URL de rappel l'adresse du service d'authentification. Déployer ensuite un petit service d'authentification gratuit (par exemple sur Vercel ou Netlify Functions, projet « decap-proxy »). Renseigner son adresse dans `admin/config.yml` (`base_url`).
3. **Pages** : Settings → Pages, source : la branche `main`, dossier `/ (root)`.
4. **Branche** : le site se publie depuis `main`. Les modifications actuelles sont sur `claude/changes` et doivent être fusionnées dans `main` pour être publiées.

Tant que l'étape 2 n'est pas faite, la page `/admin/` affiche la connexion mais ne peut pas se connecter à GitHub.

## Développement local (facultatif)

Nécessite Ruby. Depuis le dossier du projet :

```bash
gem install bundler jekyll
jekyll serve --baseurl ""
```

Le site est alors visible sur `http://localhost:4000`.
