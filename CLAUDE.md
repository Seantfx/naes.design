# Portfolio Sean — naes.design

Portfolio personnel de product designer (Sean Tiffonnet).

## Localisation & déploiement
- Dossier local : `C:\Users\seant\Documents\Portfolio-Sean`
- Repo GitHub : https://github.com/Seantfx/naes.design (branche `main`, public)
- Domaine live : https://naes.design (GitHub Pages + DNS Namecheap, HTTPS actif)
- OS : Windows, shell PowerShell

## Stack
- Un seul fichier `index.html` : CSS dans `<style>`, JS dans `<script>`
- Pas de framework, pas de build, pas de dépendances
- Font Inter chargée depuis Google Fonts
- SPA : toutes les "pages" sont des `<main class="page">` cachés/affichés en JS, routing par hash (`#about`, `#project-nodale`, etc.)
- JS en syntaxe ES5 (pas d'arrow functions) pour la compatibilité

## Structure des fichiers
```
Portfolio-Sean/
├── 360learning/  (THUMBNAIL.png, 1.png à 5.png)
├── About/        (profil_picture.png)
├── Alto/         (THUMBNAIL.png, 1.png à 4.png)
├── Claap/        (THUMBNAIL.png, 1.png à 6.png)
├── Nodale/       (THUMBNAIL.png, 1.png à 4.png)
├── Zeliq/        (THUMBNAIL.png, 1.png à 6.png)
├── CNAME         (contient "naes.design")
├── favicon.png
├── index.html
├── llms.txt      (description du site pour les crawlers LLM)
├── og-image.png  (1200×630)
├── robots.txt    (autorise explicitement les bots IA, pointe vers le sitemap)
└── sitemap.xml
```

## Design system
- Fond `#0a0a0a`, surface `#161616`, bordures `#222`, texte `#f0f0f0`, texte secondaire `#777`, accent `#d4ff00` (vert lime)
- Typo légère (weight 300) sur les grands titres, italiques en accent pour les mots mis en avant
- Curseur custom avec follower, loader bar au chargement, animations reveal au scroll via IntersectionObserver, effet magnétique sur les cartes projet, nav sticky avec backdrop blur
- Responsive : breakpoints à 1024px et 768px, curseur custom désactivé en mobile

## Pages
- Home : hero + 5 cartes projet (Nodale, Zeliq, Claap, Alto, 360Learning)
- About me : nom, bio en 4 paragraphes avec liens sortants, liste d'expériences, tags de skills
- 5 pages projet : back link, titre, meta (rôle/durée/outils), texte d'intro, galerie d'images, lien vers le projet suivant
- 404
- Footer : nav + icônes LinkedIn/Dribbble/X + copyright

## Liens de Sean
- LinkedIn : https://linkedin.com/in/seantiffonnet
- Dribbble : https://dribbble.com/SeanTiffonnet
- X : https://x.com/SeanTiffonnet

## Règles de travail
- Pour une modif : éditer directement `index.html` et indiquer quoi vérifier
- Déploiement : proposer les commandes `git add` / `commit` / `push`, ou les lancer si demandé
- ⚠️ Les liens externes doivent garder `target="_blank"` ; le handler de clic du JS les ignore explicitement (check sur `a[target="_blank"]`) pour ne pas être interceptés par le routing SPA
