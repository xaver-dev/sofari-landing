# Sofari — Landingpage

Zweisprachige Produktseite (DE/EN) für die Android-App **Sofari**: Möbel per Foto oder AR
maßstabsgetreu im eigenen Raum platzieren.

- **App:** [Google Play](https://play.google.com/store/apps/details?id=app.sofari)
- **Browser-Fassung:** [sofari.expo.app](https://sofari.expo.app/)
- **Diese Seite:** https://xaver-dev.github.io/sofari-landing/

## Aufbau

Eine einzelne `index.html` — Markup, Styles und Skript in einer Datei, keine Build-Kette,
keine Abhängigkeiten außer GSAP über CDN.

```
index.html      komplette Seite
assets/         Illustrationen, Szenen, Blätter
shots/          App-Screenshots (01–05 deutsch, en-01–en-05 englisch)
```

Sprachumschaltung läuft über `data-i18n`-Attribute: Deutsch steht im Markup, Englisch im
`I18N.en`-Objekt. Alle externen Adressen stehen gesammelt im `CONFIG`-Objekt am Anfang des
Skripts.

## Lokal ansehen

```bash
python3 -m http.server 8000
```

Dann `http://localhost:8000` öffnen. Direkt per `file://` funktioniert die Seite ebenfalls,
nur ohne korrekte relative Pfadauflösung in allen Browsern.
