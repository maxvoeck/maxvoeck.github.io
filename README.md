# Portfolio Website

Eine Jekyll-basierte Portfolio-Seite für GitHub Pages.

## Setup

### Lokale Entwicklung

1. Ruby installieren (falls noch nicht vorhanden)
2. Jekyll und Bundler installieren:
   ```bash
   gem install jekyll bundler
   ```
3. Dependencies installieren:
   ```bash
   bundle install
   ```
4. Site lokal starten:
   ```bash
   bundle exec jekyll serve
   ```
5. Im Browser öffnen: `http://localhost:4000`

### Auf GitHub Pages deployen

1. Erstelle ein neues Repository auf GitHub mit dem Namen `dein-username.github.io`
   (ersetze `dein-username` mit deinem GitHub-Nutzernamen)

2. Initialisiere Git und pushe den Code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/dein-username/dein-username.github.io.git
   git push -u origin main
   ```

3. Gehe zu den Repository-Einstellungen → Pages
4. Wähle "Deploy from a branch" und branch "main" mit folder "/(root)"
5. Deine Seite ist nach wenigen Minuten unter `https://dein-username.github.io` erreichbar

## Inhalte anpassen

### Persönliche Informationen
- Bearbeite `_config.yml` und trage deine E-Mail, GitHub- und LinkedIn-Namen ein
- Passe `about.md` mit deinen echten Informationen an

### Neue Analyse schreiben
Erstelle eine neue Datei in `_analysen/` mit folgendem Format:
```
_analysen/YYYY-MM-DD-titel.md
```

Beispiel-Struktur:
```yaml
---
layout: post
title: "Titel der Analyse"
date: 2025-11-17
categories: wirtschaft
excerpt: "Kurze Zusammenfassung"
---

Dein Inhalt hier...
```

### Neues Projekt hinzufügen
Erstelle eine neue Datei in `_projekte/`:
```
_projekte/YYYY-MM-DD-projektname.md
```

### Unterrichtsmaterialien hochladen
1. PDFs in den Ordner `assets/pdfs/` kopieren
2. In `teaching.md` Links hinzufügen:
   ```html
   <a href="/assets/pdfs/deine-datei.pdf" download>PDF herunterladen</a>
   ```

## Struktur

```
portfolio-site/
├── _config.yml          # Hauptkonfiguration
├── index.md            # Startseite
├── about.md            # Über mich
├── analysen.md         # Analysen-Übersicht
├── projekte.md         # Projekte-Übersicht
├── teaching.md         # Unterrichtsmaterialien
├── _analysen/          # Wirtschaftsanalysen (Posts)
├── _projekte/          # Code-Projekte (Posts)
├── assets/
│   ├── css/
│   │   └── style.scss  # Custom CSS
│   └── pdfs/           # PDF-Downloads
└── Gemfile             # Ruby dependencies
```

## Design anpassen

Das Design basiert auf dem "minima" Theme mit eigenem CSS in `assets/css/style.scss`.
Du kannst die Farben, Abstände etc. dort anpassen.

## Tipps

- Schreibe Markdown-Dateien mit deinem bevorzugten Editor
- Nutze `bundle exec jekyll serve` um Änderungen live zu sehen
- Committe regelmäßig und pushe auf GitHub
- GitHub Pages baut die Seite automatisch nach jedem Push

## Support

Bei Problemen siehe:
- [Jekyll Dokumentation](https://jekyllrb.com/docs/)
- [GitHub Pages Dokumentation](https://docs.github.com/pages)
