# Kopier-Hilfe für Handy (send.html)

SharePoint führt **kein JavaScript** in HTML-Dateien aus — deshalb funktioniert `today_briefing.html` auf SharePoint nicht zum Kopieren.

Diese Seite (`send.html`) wird auf **GitHub Pages** gehostet. Der Mail-Link enthält den Text bereits im Link — kein SharePoint nötig.

## Einrichtung (einmalig, ~5 Min.)

1. Code auf GitHub pushen (Repo mit diesem Ordner)
2. GitHub → **Settings** → **Pages** → Source: **GitHub Actions**
3. Workflow `.github/workflows/copy-helper-pages.yml` läuft automatisch bei Push
4. Pages-URL notieren, z. B. `https://IHR-ORG.github.io/IHR-REPO/send.html`
5. In `config.yaml` eintragen:

```yaml
copy_helper_url: "https://IHR-ORG.github.io/IHR-REPO/send.html"
```

## Lokal testen (PC)

```powershell
python tools/marketing-leadtrichter/test_copy_link.py --contact-id LI0291 --serve --open
```

Browser öffnet Hilfsseite → **„Text kopieren & LinkedIn öffnen“** tippen → Text in Zwischenablage.

## Ablauf in der Mail (Handy)

1. Button **„LinkedIn: Nachricht schreiben“** in der Mail
2. Hilfsseite öffnet sich → **einmal tippen**
3. Text kopiert, LinkedIn öffnet sich
4. **Einfügen** und senden
