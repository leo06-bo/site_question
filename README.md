# Lueur — Quelque chose à se dire

Application romantique de questions pour couple. PWA mobile-first.

## Lancer localement

```bash
# Option 1 : Python (le plus simple)
python3 -m http.server 8080
# puis ouvrir http://localhost:8080

# Option 2 : Node.js (npx)
npx serve .
# puis ouvrir l'URL affichée

# Option 3 : VS Code
# Installer l'extension "Live Server" et cliquer sur "Go Live"
```

## Installer comme PWA sur iPhone

1. Ouvrir dans Safari sur iPhone
2. Appuyer sur l'icône de partage ⬆
3. "Sur l'écran d'accueil"
4. Lueur apparaît comme une vraie app

## Installer sur Android

1. Ouvrir dans Chrome
2. La bannière d'installation apparaît automatiquement
3. Appuyer "Installer"

## Icônes

Remplacez `icon-192.png` et `icon-512.png` par vos vraies icônes
(fond terracotta #C4714A, flamme blanche centrée).
Des outils comme realfavicongenerator.net permettent de les générer.

## Structure

```
lueur/
├── index.html      ← app complète (HTML + CSS + JS)
├── manifest.json   ← config PWA
├── sw.js           ← service worker (offline)
├── icon-192.png    ← icône à créer
├── icon-512.png    ← icône à créer
└── README.md
```

## Personnalisation

Dans `index.html`, section `const MODES = [...]` :
- Ajoutez vos propres questions dans n'importe quel mode
- Chaque question a un texte `t` et une intensité `i` (1, 2 ou 3)

## Données

Tout est stocké en localStorage : favoris, questions vues, streak, paramètres.
Aucune donnée n'est envoyée nulle part. Tout reste sur l'appareil.
