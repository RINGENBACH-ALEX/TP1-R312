# TP R3.12 — Astro & Observable Plot

**Nom Prénom :** RINGENBACH Alex

**Site déployé (Netlify) :** https://tp-r312.netlify.app/

**Dépôt GitHub :** https://github.com/RINGENBACH-ALEX/TP1-R312

## Description

Projet Astro reprenant le composant `PlotFigure.astro` vu en TD, qui rend des
graphiques [Observable Plot](https://observablehq.com/plot/) côté serveur à
l'aide de [JSDOM](https://github.com/jsdom/jsdom).

Pages :

- `/` — accueil
- `/penguins` — exemple des penguins (nuage de points + histogramme), données
  filtrées aux colonnes utiles dans `src/data/penguins.json`
- `/examples` — autres exemples de la galerie Plot (barres, courbe, nuage de
  points) avec `src/data/alphabet.json`, `src/data/aapl.json`,
  `src/data/mtcars.json`

Accessibilité : chaque graphique est entouré d'une balise `<figure>` /
`<figcaption>`, et chaque `Plot.plot` reçoit un `title`, un `subtitle` et un
`ariaLabel` (voir [features/accessibility](https://observablehq.com/plot/features/accessibility)).

## Commandes

| Commande          | Action                                       |
| :----------------- | :-------------------------------------------- |
| `npm install`       | Installe les dépendances                      |
| `npm run dev`       | Lance le serveur de dev sur `localhost:4321`  |
| `npm run build`     | Build de production dans `./dist/`            |
| `npm run preview`   | Prévisualise le build en local                |

## Déploiement

Adaptateur [`@astrojs/netlify`](https://docs.astro.build/en/guides/integrations-guide/netlify/)
installé et configuré dans `astro.config.mjs`. Sur Netlify :

- Build command : `npm run build`
- Publish directory : `dist`
