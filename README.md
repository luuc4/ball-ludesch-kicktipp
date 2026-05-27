# Ball Ludesch · WM 2026 Kicktipp

Statische Website (2 Seiten) für das firmeninterne Kicktipp-Turnier zur WM 2026.

## Dateien

- `index.html` – Landing Page: Kurz-Anleitung, QR-Code, Preise, Punkteverteilung, App-Links
- `anleitung.html` – Detaillierte Schritt-für-Schritt-Anleitung inkl. Erklärung der Kicktipp-Bereiche
- `styles.css` – komplettes Styling (Inter, Hauptfarbe `#1140fe`, mobile-first)
- `site.webmanifest` – Web-App-Manifest für Android-Icons
- `assets/` – Logo, QR-Code und alle Favicon-Varianten

## Lokal anschauen

Wegen des `manifest`-Links die Seite über einen kleinen lokalen Webserver öffnen:

```bash
python3 -m http.server 8000
# dann http://localhost:8000
```

(`index.html` direkt im Browser öffnen funktioniert auch, manche Browser warnen
dann nur wegen der Manifest-Datei.)

## Hosting via GitHub Pages

Ein Deploy-Workflow liegt unter `.github/workflows/pages.yml` und veröffentlicht
auf `https://luuc4.github.io/ball-ludesch-kicktipp/`.

Einmalige Aktivierung:

1. GitHub → Repo → **Settings** → **Pages**
2. Bei **Source** auswählen: **GitHub Actions**
3. Beim nächsten Push auf `main` oder die aktuelle Entwicklungs-Branch deployt
   der Workflow automatisch.

Falls die finale URL (Custom Domain o.ä.) abweicht, sollten die absoluten
URLs in den `<meta property="og:*">`-Tags in `index.html` und `anleitung.html`
angepasst werden.

## Alternative Hostings

Kann auch überall sonst statisch gehostet werden (Netlify, Intranet-Webserver) –
alle Pfade sind relativ und kommen ohne Build-Step aus.
