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

## Design system (v2 — éditorial clair, en prod depuis août 2026)
- Fond papier `#FAF9F6`, encre `#141414`, muted `#7A776E`, filets `#E4E2DA`, accent bleu `#2B4BF2` (utilisé avec parcimonie : hover des liens de la bio)
- Typo : Instrument Serif (400 + italic) pour tous les titres et les emphases `<em>`, Inter (400/500) pour le corps et l'UI
- Home : hero typographique géant, liste de projets indexée (01–05) — au survol le titre glisse et la vignette flotte (rotation -2°, ombre portée) ; vignettes masquées ≤1024px
- Pages projet : colonne éditoriale max 1080px, méta en petites capitales, galeries 16/9 et 4/3, lien "next" avec flèche
- About : portrait N&B (About/profil_picture_bw.png), skills en phrase serif séparée par des puces
- Pas de curseur custom, pas de loader — seule animation : fade-up au changement de page
- Responsive : breakpoints à 1024px et 768px
- L'ancienne DA dark (#0a0a0a / accent lime #d4ff00) est dans l'historique git avant le commit "New editorial design"

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
