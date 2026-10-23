# Modifications apportées (audit ui-ux-pro-max)

## Accessibilité
- Lien « Aller au contenu principal » (clavier) ; une seule balise `<h1>` (celle du hero ; le nom dans la barre est devenu un `<p>`).
- `lang` de la page suit la langue choisie (EN/FR) ; boutons de langue avec `aria-pressed` et libellés.
- Menu mobile : `aria-expanded` / `aria-controls`, fermeture avec Échap.
- Cartes projets : vrais `<button>` (utilisables au clavier / lecteur d'écran) avec `aria-pressed`.
- Graphique radar : description textuelle (`role="img"` + `aria-label`, mise à jour selon la langue).
- Icônes décoratives masquées aux lecteurs d'écran ; emoji 🚀 remplacé par une icône.
- `prefers-reduced-motion` respecté (animations, survols, défilement lissé, animation du graphique).
- Focus clavier visible et cohérent ; `scroll-padding-top` pour que les ancres ne passent plus sous la barre fixe.
- Formulaire : `autocomplete`, champs en 16 px (pas de zoom automatique sur iPhone), statut annoncé (`aria-live`), bouton désactivé pendant l'envoi, champ anti-spam `_gotcha` (Formspree).
- Bloc `<noscript>` avec e-mail et CV.

## Zones de toucher (≥ 44×44 px)
- Boutons EN/FR, bouton menu, liens du menu, « Live Demo », « View Code », liens e-mail / LinkedIn / téléphone / GitHub (pied de page et bloc contact).
- Sur téléphone (< 640 px) la tuile « M » est masquée pour que le nom + les contrôles tiennent (testé de 320 à 1280 px).

## Contrastes (WCAG AA)
- Libellés `slate-400` → `slate-500`, `teal-600` en petit texte → `teal-700`, bouton « Book a Call » `teal-600` → `teal-700`, bouton FR/EN inactif plus foncé.
- Bannières de projets (texte blanc) assombries : teal 700→900, amber 700→900 (était 500→700, ~2:1), indigo 600→800.
- Dégradé du titre : `teal-700 → emerald-600`.

## Performance
- Tailwind : `cdn.tailwindcss.com` (≈300 Ko de JS exécuté à chaque visite) → `assets/tailwind.css` compilé (≈22 Ko).
- Phosphor : 6 feuilles de style (thin/light/bold/fill/duotone…) → 1 seule (regular), hébergée localement.
- Chart.js : version non épinglée via CDN → v4.4.7 hébergée localement, chargée en `defer`.
- `preconnect` vers Google Fonts, `preload` de la police d'icônes.

## Partage / référencement
- Balises Open Graph + Twitter Card, `images/og-image.png` (1200×630), URL canonique, `theme-color`, favicon, données structurées JSON-LD (Person).

## Divers
- Le projet sélectionné est conservé quand on change de langue.
- Titre du hero : `text-balance` + 52 px en bureau (plus de « & » seul sur une ligne).

## Non modifié (à votre appréciation)
- `styles.css` n'est référencé par aucune page (reste d'un ancien design) ; `images/photo.JPG` (625 Ko) n'est pas utilisé.
- Les scores du radar de compétences sont des auto-évaluations (le texte alternatif le précise).
