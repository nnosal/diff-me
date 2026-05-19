
# DiffMe

DiffMe est un petit outil client-side (page HTML + JS) pour comparer rapidement 2 textes et visualiser les différences (diffs) en local, sans serveur.

## Aperçu

- Interface à 2 panneaux : **Original** (gauche) et **Modified** (droite).
- Éditeur hybride WYSIWYG/texte (édition riche + source + aperçu Markdown).
- 2 modes d'affichage : *unified* (consolidé) et *split* (côte-à-côte).
- Diff ligne/word/char : options pour montrer les différences au niveau des mots ou des caractères.
- Appliquer des hunks (patchs) côté *Modified*, télécharger un fichier `.patch`.
- Partage via URL (encode le contenu dans le hash) et restauration de session via localStorage.

## Fonctionnalités clés

- Drag & drop / ouverture de fichiers (formats texte : .md, .txt, .json, .js, .py, etc.).
- Compter lignes et caractères par panneau.
- Copier une ligne complète ou uniquement les caractères modifiés (boutons sur chaque ligne).
- Basculer panels (swap), vider, copier, sauvegarder le contenu localement.
- Mode d'affichage inline char-diff (surlignage des caractères insérés / supprimés).
- Génération d'un patch unifié téléchargeable (`diff.patch`) et application sélective de hunks.
- Raccourcis clavier (ouvrir la fenêtre raccourcis avec `?`) :
	- `Ctrl+Enter` : calculer le diff
	- `Ctrl+Shift+D` : basculer thème dark/light
	- `Ctrl+Shift+S` : copier URL de partage
	- `Ctrl+Shift+X` : swap panels
	- `←` / `→` : naviguer entre les changements
	- `c` / `C` : copier ligne / copier uniquement delta

## Démarrage rapide

- Voir la page hébergée via GitHub Pages (si disponible).
- Ou télécharger / ouvrir localement le fichier `index.html` dans un navigateur moderne.

Options utiles dans l'interface : `Inline char diff`, `Word diff`, `context lines`, `Split View`.

## Développement / Exécution locale

- Le projet est purement statique : il suffit d'ouvrir [index.html](index.html).
- Pour servir localement (optionnel) : `bunx vite --open`

## Dépendances

- Chargées depuis CDN dans `index.html` :
	- `markdown-it` (render Markdown preview)
	- `diff-match-patch` (calcul des diffs)

## Structure

- `index.html` — interface + logique JS (tout en un fichier).

## Contribuer

1. Forkez le dépôt.
2. Créez une branche feature/fix.
3. Ouvrez une Pull Request décrivant les changements.

## Licence

Ce projet est distribué sous la licence MIT — voir le fichier `LICENSE`.

