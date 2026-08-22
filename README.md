# LurkAdventure Backlog

Öffentlicher Entwicklungs-Backlog für **LurkAdventure**.

Dieses Repository ist die zentrale Issue-Sammlung für Bugs, Features, Architekturthemen und spätere Vorhaben. Die tägliche Arbeitsübersicht soll über ein **GitHub Project Board** erfolgen.

> Sensible Betriebsdaten, Zugangsdaten, Secrets, private URLs, persönliche Daten oder konkrete vertrauliche Infrastrukturinformationen gehören nicht in dieses Repository.

## Wo finde ich was?

- **Issues** — einzelne Bugs, Features und technische Vorhaben
- **GitHub Project `LurkAdventure Backlog`** — Arbeitsboard und Status der Issues
- [`docs/BOARD.md`](docs/BOARD.md) — Aufbau, Spalten, Views und Automatisierung des Boards
- [`docs/WORKFLOW.md`](docs/WORKFLOW.md) — Regeln für Issues, Prioritäten, Bereiche und Abhängigkeiten

## Grundstruktur

Jedes offene Issue erhält:

1. einen **Typ**, normalerweise eines der vorhandenen GitHub-Labels wie `bug`, `enhancement` oder `documentation`
2. **genau eine Priorität**: `P0`, `P1`, `P2` oder `P3`
3. **mindestens einen Bereich** über `area: ...`

Der **Arbeitsstatus** wird im GitHub Project gepflegt und nicht dauerhaft über Labels dupliziert.

### Prioritäten

- `P0` — ausschließlich dringende Bugs
- `P1` — aktuell oder als Nächstes relevant
- `P2` — Later; geplant, aber aktuell nicht dran
- `P3` — Parked, Sideproject oder langfristige Idee

### Bereiche

Aktuell vorgesehen sind unter anderem:

`area: global`, `area: core`, `area: studio`, `area: web`, `area: gameserver`, `area: legacy`, `area: streamer`, `area: twitch`, `area: cardstudio`, `area: cardgame`, `area: tools`, `area: obs`, `area: auth` und `area: repo`.

Ein Issue darf mehrere Bereiche betreffen.

## Wichtigste Regeln

- Keine Bereichspräfixe wie `[WEB]` oder `[CORE]` im Titel; dafür gibt es Labels.
- Keine neuen WP-/TODO-Dateien als paralleles Planungssystem.
- Thematische Verwandtschaft ist keine Abhängigkeit. Nur echte Blocker verlinken.
- Große Sammel-Issues nur kurzfristig für Triage verwenden und anschließend auflösen.
- QA-/Abnahme-Checklisten werden nicht automatisch zu Issues. Erst ein reproduzierbarer Fehler wird zum Bug-Issue.
- `P0` wird nicht für Features, Architektur oder allgemeine Wichtigkeit verwendet.

Weitere Details stehen in [`docs/WORKFLOW.md`](docs/WORKFLOW.md).
