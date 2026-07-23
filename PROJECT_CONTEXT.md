# Projektkontext: ChatGPT Pets

## Zuerst lesen

Neue Chats lesen zuerst diese Datei und danach [NEXT_STEPS.md](NEXT_STEPS.md). Für Veröffentlichungen ist zusätzlich [PORTFOLIO_UPDATE.md](PORTFOLIO_UPDATE.md) maßgeblich. Die öffentlichen Beschreibungen der einzelnen Pets liegen jeweils in deren Ordnern.

## Zweck

Dieses Repository enthält eigene, importierbare animierte Pets für ChatGPT und Codex. Jedes Pet ist als eigener Ordner mit einer Beschreibung, einer Vorschau, einem Manifest und einem Sprite-Sheet abgelegt.

## Struktur und Datenformat

- `README.md` und `README.en.md`: deutsche und englische Übersicht aller Pets sowie Import-Hinweise.
- `<Pet-Ordner>/pet.json`: Manifest des jeweiligen Pets.
- `<Pet-Ordner>/*.webp`: das im Manifest referenzierte Sprite-Sheet.
- `<Pet-Ordner>/preview-transparent.png`: Vorschau für die Übersichts- und Pet-Seiten.
- `<Pet-Ordner>/README.md` und `README.en.md`: deutsche und englische Pet-Beschreibung.
- `LICENSE`: MIT-Lizenz.
- `PORTFOLIO_UPDATE.md`: Prüfungspflicht vor öffentlicher Veröffentlichung oder erheblicher Erweiterung.

Das Manifest verwendet diese Felder:

```json
{
  "id": "stabile-kleinschreibung",
  "displayName": "Sichtbarer Pet-Name",
  "description": "Kurze englische Beschreibung",
  "spriteVersionNumber": 2,
  "spritesheetPath": "datei.webp"
}
```

Alle aktuell enthaltenen Pet-Manifeste nutzen `spriteVersionNumber: 2`.

## Build, Test und Release

Es gibt keinen Build-Schritt, kein Lockfile, keine CI-Konfiguration und keine automatisierten Tests im Repository. Die veröffentlichbaren Artefakte sind die eingecheckten Manifest-, Sprite-Sheet- und Vorschaudateien.

Vor einer Änderung an einem Pet mindestens prüfen:

1. `pet.json` verweist auf die vorhandene Sprite-Sheet-Datei.
2. Die Vorschau und die deutschen sowie englischen Beschreibungen passen zum Pet.
3. Beide Übersichtsseiten verlinken korrekt auf das Pet.
4. Bei einer öffentlichen Veröffentlichung zusätzlich `PORTFOLIO_UPDATE.md` prüfen.

## Umgesetzter Stand

Enthalten sind Woodi, WonderCube, Delta, Byte, Whiskers & Squeak, Inky und Finder Guy. Jedes dieser Pets besitzt ein V2-Manifest und ein referenziertes WebP-Sprite-Sheet.

## Entscheidungen und feste Regeln

- Das Manifest ist die technische Quelle für Pet-ID, sichtbaren Namen, Beschreibung und Sprite-Sheet-Datei.
- `id` und Ordnername werden nicht ohne bewusst geplante Kompatibilitätsprüfung geändert.
- Öffentliche Pet-Beschreibungen bleiben auf Deutsch und Englisch gepflegt.
- Die Übersichtsseiten bleiben inhaltlich gleichwertig und verwenden die zugehörigen Sprachseiten als Ziele.
- Bestehende Pets und deren Dateien nur ändern, wenn der Auftrag dies ausdrücklich umfasst.

## Bekannte Grenzen

Die aktuelle Funktionsfähigkeit der Sprite-Sheets in jeder ChatGPT- oder Codex-Version ist im Repository nicht automatisiert dokumentiert. Konkrete offene Bugs oder fehlende Pets sind derzeit nicht dokumentiert.

## Datenschutz und Veröffentlichung

- Keine privaten Dateien, Logs, Backups, Zugangsdaten, Tokens oder Screenshots mit echten Daten ins Repository aufnehmen.
- Nur öffentliche Assets und Demo-Inhalte veröffentlichen.
- Bei öffentlichen Namen ausschließlich `Schrotty74` verwenden.
- Vor einer öffentlichen Veröffentlichung oder bedeutenden Erweiterung die Portfolio-Regel beachten.
