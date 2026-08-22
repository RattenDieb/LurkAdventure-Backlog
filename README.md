# LurkAdventure Backlog

Öffentlicher Entwicklungs-Backlog für LurkAdventure.

Dieses Repository enthält Planung, Bugs, Features und technische Vorhaben. Sensible Betriebsdaten, Zugangsdaten, Secrets, private URLs oder persönliche Daten gehören **nicht** in dieses Repository.

## Struktur

Jedes offene Issue erhält mindestens:

- **Typ**: vorhandene GitHub-Labels wie `bug`, `enhancement` oder `documentation`
- **Priorität**: genau eines von `P0`, `P1`, `P2`, `P3`
- **Bereich**: mindestens ein `area: ...`-Label
- **Status** nur wenn nötig: `status: ready`, `status: in progress`, `status: blocked`, `status: review`

### Prioritäten

- `P0` — ausschließlich dringende Bugs
- `P1` — aktuelle oder als Nächstes geplante Arbeit
- `P2` — Later; geplant, aber aktuell nicht dran
- `P3` — Parked, Sideproject oder langfristige Idee

Ein offenes Issue ohne Statuslabel liegt einfach im Backlog.

### Status

- `status: ready` — konkret als Nächstes bearbeitbar
- `status: in progress` — wird aktuell umgesetzt
- `status: blocked` — kann wegen eines echten Blockers nicht weitergeführt werden
- `status: review` — Umsetzung liegt zur Prüfung/Abnahme vor
- geschlossen — erledigt oder bewusst verworfen

Nicht mehrere Arbeitsstatus gleichzeitig verwenden.

### Bereiche

Bereiche werden über `area: ...` gepflegt, z. B. Core, Studio, Web, Gameserver, Streamer, Twitch, CardGame, CardStudio, Tools, OBS, Auth, Repo, Legacy oder Global. Ein Issue darf mehrere Bereiche betreffen.

## Regeln

- Keine Bereichspräfixe wie `[WEB]` oder `[CORE]` im Titel; dafür gibt es Labels.
- Keine neuen WP-/TODO-Dateien als paralleles Planungssystem.
- Thematische Verwandtschaft ist keine Abhängigkeit. Nur echte Blocker verlinken.
- Große Sammel-Issues nur zur kurzfristigen Triage; anschließend in eigenständig bearbeitbare Themen schneiden.
- QA-/Abnahme-Checklisten werden nicht automatisch zu Issues. Erst ein reproduzierbarer Fehler wird zum Bug-Issue.
- `P0` wird nicht für Features, Architektur oder allgemeine Wichtigkeit verwendet.

## Arbeitsweise

Die Arbeitsreihenfolge ergibt sich primär aus **Status + Priorität**. `status: ready` soll bewusst klein bleiben. `status: in progress` nur setzen, wenn tatsächlich daran gearbeitet wird.
