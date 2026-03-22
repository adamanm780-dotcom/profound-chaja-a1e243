# CLAUDE.md – profound-chaja (RepairStation Wiesbaden)

## Projekt-Überblick
Statische One-Page-Website für **RepairStation Wiesbaden** – ein Reparaturservice für Smartphones, Laptops und MacBooks in Wiesbaden.

- **URL:** https://adamanm780-dotcom.github.io/profound-chaja-a1e243/
- **Repo:** https://github.com/adamanm780-dotcom/profound-chaja-a1e243
- **Hosting:** GitHub Pages (Branch `main`, Root `/`)
- **Sprache:** Deutsch

## Dateistruktur
```
index.html        – gesamte Website (HTML + CSS + JS in einer Datei)
logo.png          – Logo
favicon.svg       – Favicon
superr.png        – weiteres Logo/Icon (wird als favicon genutzt)
ohio.glb          – 3D-Modell (auf Handy & Desktop sichtbar)
sigma1.glb        – 3D-Modell (auf Handy & Desktop sichtbar)
gui.glb           – 3D-Modell (nur auf Desktop sichtbar)
```

## Technologie-Stack
- Reines HTML/CSS/JS – kein Build-Tool, kein Framework
- **Google Fonts:** Inter + Plus Jakarta Sans
- **3D-Modelle:** `<model-viewer>` via Google CDN (v3.5.0)
- **Deployment:** direkter `git push` auf `main` → GitHub Pages baut automatisch

## Design-Token (CSS-Variablen)
| Variable | Wert | Verwendung |
|---|---|---|
| `--brand` | `#1D4ED8` | Primärfarbe Blau |
| `--brand-light` | `#3B82F6` | Hellblau |
| `--brand-dark` | `#1E3A8A` | Dunkelblau |
| `--accent` | `#F97316` | Orange CTA |
| `--dark` | `#0F172A` | Hintergrund dunkel |

## 3D-Modell Regeln
- `ohio.glb` / `sigma1.glb` → sichtbar auf **Handy + Desktop**
- `gui.glb` → **nur Desktop** (CSS: `display: none` auf Mobile via Media Query)
- Alle `<model-viewer>` Elemente brauchen `touch-action: pan-y` damit Scrollen auf Mobile nicht blockiert wird
- Hintergrund der Viewer ist immer `transparent`

## Deployment
```bash
git add <dateien>
git commit -m "Beschreibung"
git push
```
GitHub Pages aktualisiert sich automatisch nach ~1 Minute.

## Wichtige Hinweise
- Alle Texte auf der Website sind auf **Deutsch**
- Telefonnummer: **0611–58589987**
- Keine externen Build-Scripts – alles läuft direkt aus `index.html`
- Neue 3D-Modelle (.glb) immer in das Root-Verzeichnis des Repos legen
