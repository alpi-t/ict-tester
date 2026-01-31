# ICT Tester Zuweisung

Web-App für die Zuweisung von ICT-Testern zu Aufträgen.

## 🌐 Live URL
https://alpi-t.github.io/ict-tester/

## ✨ Features

- ⚙️ **Fertigungsteuerer**: Aufträge laden, Tester zuweisen, speichern
- 👁️ **Mitarbeiter**: Tester-Zuweisung anzeigen (nur lesen)
- 📋 **Historie**: Alle gespeicherten Aufträge anzeigen
- 📊 **Export**: Historie als CSV/Excel exportieren
- ☁️ **GitHub Backend**: Daten permanent in GitHub gespeichert
- 🔄 **Geräteübergreifend**: Daten synchronisiert auf allen Geräten
- 💾 **Backup**: Automatisches lokales Backup im Browser

## 🔐 Setup (nur für Fertigungsteuerer)

Beim ersten Speichern wird nach einem GitHub Token gefragt.

### GitHub Token erstellen:
1. Gehe zu https://github.com/settings/tokens
2. Klicke auf "Generate new token" → "Generate new token (classic)"
3. Name: `ICT Tester App`
4. Expiration: `No expiration` (oder 90 days)
5. Scopes: Nur `repo` aktivieren
6. Klicke "Generate token"
7. Kopiere den Token (beginnt mit `ghp_...`)
8. Füge ihn in die App ein, wenn gefragt

**Der Token wird lokal im Browser gespeichert und nie weitergegeben.**

## 📱 Verwendung

### Fertigungsteuerer:
1. Linke Seite anklicken: "Fertigungsteuerer"
2. Auftragsnummer scannen oder eingeben
3. Tester zuweisen (Haupt + bis zu 3 Varianten)
4. Speichern klicken
5. **Historie-Button** oben rechts für alle Aufträge

### Mitarbeiter:
1. Rechte Seite anklicken: "Mitarbeiter"
2. Auftragsnummer scannen
3. Zugewiesene Tester werden angezeigt

## 🛠️ Technisch

- **Frontend**: Pure HTML/CSS/JS (keine Dependencies)
- **Storage**: GitHub API (data.json)
- **Hosting**: GitHub Pages
- **Backup**: Browser localStorage

## 📊 Datenstruktur

```json
{
  "AUFTRAG123": {
    "mainTester": "T01",
    "variant1": "T02",
    "variant2": "",
    "variant3": "",
    "updatedAt": "2026-01-31T21:00:00.000Z"
  }
}
```

---

Made with 🚗 by KITT
