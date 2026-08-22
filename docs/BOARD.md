# GitHub Project Board

Das GitHub Project **`LurkAdventure Backlog`** ist die führende Arbeitsansicht für offene Issues.

Die Issues selbst bleiben die inhaltliche Quelle. Labels beschreiben Typ, Priorität und Bereich. Der **Arbeitsstatus** wird ausschließlich im Project gepflegt.

## Ziel

Das Board soll auf einen Blick beantworten:

- Was ist aktuell dran?
- Was ist als Nächstes bereit?
- Was wartet auf Review?
- Was ist blockiert?
- Was liegt bewusst später?

Es soll **kein zweites Planungssystem** neben den Issues entstehen.

## Project anlegen

Das Project muss einmalig in der GitHub-Oberfläche angelegt werden:

1. GitHub-Profil öffnen.
2. **Projects** öffnen.
3. **New project** wählen.
4. Unter **Start from scratch** `Board` wählen.
5. Projektname: **`LurkAdventure Backlog`**.
6. Project erstellen.
7. Das Repository `RattenDieb/LurkAdventure-Backlog` als Quelle anbinden bzw. die bestehenden Issues importieren.

## Statusfeld

Das Project verwendet genau ein Statusfeld mit diesen Werten:

1. **Backlog** — erfasst, aber aktuell nicht zur direkten Bearbeitung vorgesehen
2. **Ready** — ausreichend klar und als Nächstes bearbeitbar
3. **In Progress** — wird tatsächlich umgesetzt
4. **Review** — Umsetzung ist fertig und wartet auf Prüfung/Abnahme
5. **Blocked** — echter Blocker verhindert die Fortsetzung
6. **Done** — abgeschlossen

### Regeln zum Status

- Neue Issues starten grundsätzlich in **Backlog**.
- **Ready** soll bewusst klein bleiben.
- Ein Issue wird erst **In Progress**, wenn tatsächlich daran gearbeitet wird.
- **Blocked** nur bei einem konkreten Hindernis, nicht für „später“ verwenden.
- Geschlossene Issues landen in **Done**.
- P2/P3 bleiben normalerweise in Backlog, bis sie aktiv hochgezogen werden.

## Empfohlene Views

### 1. Board

Standardansicht im Board-Layout, gruppiert nach **Status**.

Zweck: tägliche Arbeitsübersicht.

### 2. NOW

Zeigt nur:

- Ready
- In Progress
- Review
- Blocked

Zweck: alles ausblenden, was aktuell keine Aufmerksamkeit braucht.

### 3. P1

Filter auf `P1`.

Zweck: nächste relevante Arbeit unabhängig vom Bereich.

### 4. Web

Filter auf `area: web`.

### 5. Core & Studio

Filter auf `area: core` und/oder `area: studio`.

### 6. Gameserver

Filter auf `area: gameserver`.

Der Gameserver-Bereich ist aktuell Later und sollte überwiegend P2 bleiben.

### 7. Parked

Filter auf `P3`.

Zweck: Ideen und Sideprojects sichtbar halten, ohne sie im Tagesgeschäft zu zeigen.

## Automatisierung

Unter **Project → Menü → Workflows** sollten folgende Automatisierungen eingerichtet werden:

### Auto-add to project

- Repository: `RattenDieb/LurkAdventure-Backlog`
- Filter: `is:issue`
- Aktivieren

Damit landen neue Issues automatisch im Project.

### Item added to project

Beim Hinzufügen eines Issues:

- `Status = Backlog`

### Item closed

GitHubs Standardworkflow soll geschlossene Issues automatisch auf **Done** setzen.

### Reopened

Falls ein geschlossenes Issue wieder geöffnet wird:

- Status zurück auf **Backlog** oder bewusst auf **Ready**, wenn es direkt wieder aufgenommen wird.

### Auto-archive

Optional später:

- abgeschlossene Items nach einer gewissen Zeit automatisch archivieren
- Empfehlung: frühestens nach 30 Tagen

So bleibt Done kurzfristig sichtbar, ohne das Board dauerhaft aufzublähen.

## Labels im Board

Das Board ersetzt **nicht** die bestehenden Labels.

Labels bleiben zuständig für:

- **Typ**: `bug`, `enhancement`, `documentation`, ...
- **Priorität**: `P0` bis `P3`
- **Bereich**: `area: ...`

Das Project ist zuständig für:

- **Status**
- Views und Arbeitsübersicht

Die Übergangslabels `status: ready`, `status: in progress`, `status: review` und `status: blocked` werden entfernt, sobald das Project eingerichtet und die bestehenden Issues dort einsortiert sind.

## Initiale Einsortierung

Nach dem Erstellen des Boards:

- alle offenen Issues zunächst **Backlog**
- Issue #9 `Rebranding von LootAdventure zu LurkAdventure` → **Ready**
- keine anderen Issues automatisch auf In Progress setzen
- P0 bleibt leer, solange kein dringender Bug existiert

## Grundsatz

**Issues enthalten die Arbeit. Labels beschreiben die Arbeit. Das Project zeigt den Arbeitsfluss.**

Damit gibt es genau eine Quelle pro Information und keine parallelen WP-, TODO- oder Statussysteme.
