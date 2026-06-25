# Mario Bros — jeu navigateur (single-file)

Jeu de plateforme type Mario, codé en un seul fichier `index.html`
(HTML + CSS + JavaScript, sprites en pixel-art dessinés au canvas).

## Emplacements

- **Code local** : `/Users/gabrielaltin/Documents/GitHub/Codex/mario-bros/`
- **Dépôt GitHub** : https://github.com/gabi-go/mario-bros
- **En ligne (GitHub Pages)** : https://gabi-go.github.io/mario-bros/

## Lancer en local

Ouvrir `index.html` dans un navigateur, ou servir le dossier :

```bash
cd /Users/gabrielaltin/Documents/GitHub/Codex/mario-bros
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Déployer une modification

GitHub Pages publie automatiquement la branche `main` :

```bash
cd /Users/gabrielaltin/Documents/GitHub/Codex/mario-bros
git add index.html
git commit -m "Décrire le changement"
git push origin main
# le site se met à jour en ~30 s sur https://gabi-go.github.io/mario-bros/
```

## Notes techniques

- Tout est dans `index.html` (aucune dépendance, aucun build).
- Sprites : Mario, Fire Mario, Luigi générés depuis des palettes de couleurs.
  Les alias Fire/Luigi se construisent avec `key.slice(2)` (retire le préfixe
  `mb`) → clés `f0/f1/f2/fJ/fC` qui doivent correspondre aux lookups de `Mario.draw`.
