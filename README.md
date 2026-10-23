# medcos.github.io

Portfolio de Médico DIOMANDE — Energy Data Scientist & Infrastructure Intelligence.
Site statique (GitHub Pages) : `index.html` + `assets/` + `cv/` + `images/`.

## Modifier le contenu
Tout le texte (EN/FR), les projets, l'expérience et la config de contact sont dans le
bloc `<script>` en bas de `index.html` (objet `content`, `CONTACT_CONFIG`, `CV_FILES`).

## Si vous ajoutez/changez des classes Tailwind
Les styles ne sont plus générés dans le navigateur (le CDN `cdn.tailwindcss.com` est
déconseillé en production) : ils sont compilés dans `assets/tailwind.css`.
Après avoir modifié des classes Tailwind dans `index.html`, régénérez le fichier :

```bash
npx tailwindcss@3.4.17 -c _build/tailwind.config.js -i _build/input.css -o assets/tailwind.css --minify
```

(Le dossier `_build/` n'est pas publié par GitHub Pages. Si vous ne touchez qu'au texte, rien à faire.)

## Dépendances hébergées localement (`assets/vendor/`)
- Chart.js 4.4.7 (MIT) — graphique radar
- Phosphor Icons 2.1.2 (MIT) — poids « regular » uniquement (toutes les icônes regular sont déjà incluses)

## Aperçu LinkedIn / réseaux sociaux
`images/og-image.png` (1200×630). Après publication, forcez LinkedIn à relire la page :
https://www.linkedin.com/post-inspector/
