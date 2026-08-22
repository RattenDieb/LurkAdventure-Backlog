# Backlog- und Issue-Workflow

Diese Datei beschreibt die verbindliche Arbeitsweise für `LurkAdventure-Backlog`.

## 1. Grundprinzip

Das Repository enthält **Issues als einzelne Arbeitseinheiten**. Das GitHub Project zeigt deren Arbeitsstatus. Labels beschreiben Priorität, Typ und betroffene Bereiche.

Es gibt bewusst **kein paralleles WP-/TODO-System** mehr.

## 2. Wann wird etwas ein Issue?

Ein eigenes Issue ist sinnvoll, wenn mindestens eines davon zutrifft:

- ein reproduzierbarer Bug muss behoben werden
- ein Feature kann eigenständig umgesetzt oder reviewed werden
- eine Architekturentscheidung hat ein klares Ergebnis
- ein späteres Vorhaben soll bewusst im Backlog erhalten bleiben
- ein Thema hat genügend Umfang, dass es sonst in einer Sammelliste verloren geht

Kein eigenes Issue nötig für:

- reine QA-/Smoke-Test-Checklisten
- allgemeine Architekturgrundsätze
- kleine Unterpunkte, die sinnvoll Teil eines bestehenden Issues sind
- lose Ideen ohne konkreten Nutzen oder Zielzustand
- technische Detailnotizen, die direkt in das zugehörige Issue gehören

Wenn eine QA-Abnahme einen echten Fehler findet, entsteht daraus ein Bug-Issue.

## 3. Issue-Aufbau

Ein normales Issue sollte möglichst enthalten:

### Ziel

Was soll nach Abschluss anders oder möglich sein?

### Umfang

Welche wesentlichen Punkte gehören dazu?

### Nicht-Ziel

Nur ergänzen, wenn eine naheliegende Fehlinterpretation verhindert werden muss.

### Akzeptanz / Ergebnis

Bei größeren Themen sinnvoll: Woran erkennt man, dass das Issue abgeschlossen ist?

Priorität und Bereich werden **nicht nur im Text**, sondern über Labels gepflegt.

## 4. Typen

Vorhandene GitHub-Standardlabels werden bevorzugt weiterverwendet.

### `bug`

Reproduzierbarer Fehler im bestehenden Verhalten.

### `enhancement`

Feature, Verbesserung, technische Erweiterung oder neue gewünschte Fähigkeit.

### `documentation`

Dokumentation, Migration von Planungswissen oder vergleichbare Doku-Aufgaben.

Weitere Standardlabels nur verwenden, wenn ihre Bedeutung eindeutig passt.

## 5. Prioritäten

Jedes offene Issue hat **genau ein** Prioritätslabel.

### P0 — dringender Bug

P0 ist ausschließlich für Bugs reserviert.

Ein P0 muss ein bestehendes Verhalten so stark beeinträchtigen, dass eine zeitnahe Behebung Vorrang vor normaler Feature-Arbeit hat.

Nicht P0:

- wichtige Features
- Architekturthemen
- größere Zukunftsvorhaben
- „wäre gut bald zu machen“

### P1 — aktuell / next

Aktuell relevante oder als Nächstes sinnvolle Arbeit.

P1 bedeutet nicht automatisch, dass das Issue sofort bearbeitet wird. Dafür existiert der Boardstatus `Ready`.

### P2 — later

Geplant und erwünscht, aber aktuell nicht im Fokus.

Der Gameserver-Strang liegt derzeit überwiegend hier.

### P3 — parked

Langfristige Idee, Sideproject oder bewusst geparktes Vorhaben.

## 6. Bereiche

Bereiche werden über `area: ...` gekennzeichnet.

Aktuell vorgesehen:

- `area: global`
- `area: core`
- `area: studio`
- `area: web`
- `area: gameserver`
- `area: legacy`
- `area: streamer`
- `area: twitch`
- `area: cardstudio`
- `area: cardgame`
- `area: tools`
- `area: obs`
- `area: auth`
- `area: repo`

Mehrere Bereichslabels sind erlaubt, wenn das Issue tatsächlich mehrere Komponenten betrifft.

Bereiche werden **nicht zusätzlich als Präfix in den Titel geschrieben**.

Gut:

`Presence-Suche und Paginierung ergänzen`

Nicht nötig:

`[WEB] Presence-Suche und Paginierung ergänzen`

## 7. Boardstatus

Der Status wird im GitHub Project gepflegt.

### Backlog

Erfasst, aber aktuell nicht zur Bearbeitung ausgewählt.

### Ready

Ausreichend klar, um als Nächstes bearbeitet zu werden.

Ready soll klein bleiben. Das ist die eigentliche Auswahl „was kommt als Nächstes?“.

### In Progress

Wird tatsächlich bearbeitet.

### Review

Umsetzung ist fertig und wartet auf Prüfung oder Abnahme.

### Blocked

Ein konkreter Blocker verhindert die Weiterarbeit.

Blocked ist **kein Ersatz für Later**. Later ist P2 + Backlog.

### Done

Abgeschlossen. In der Regel ist das zugehörige Issue geschlossen.

## 8. Abhängigkeiten

Abhängigkeiten werden nur verwendet, wenn ein Issue **wirklich nicht sinnvoll fortgesetzt werden kann**, bevor ein anderes Ergebnis vorliegt.

Nicht jede thematische Beziehung ist eine Abhängigkeit.

Beispiel für echte Abhängigkeit:

- eine Implementierung benötigt zuerst eine festgelegte Schnittstelle

Kein Grund für eine Abhängigkeit:

- zwei Issues betreffen beide Web
- zwei Features gehören zur selben langfristigen Vision
- ein Issue wäre nach einem anderen „irgendwie logischer“

Ziel: keine neue Referenz-Spaghetti wie im alten WP-System.

## 9. Sammel-Issues und Sub-Issues

Sammel-Issues sind nur sinnvoll für kurzfristige Triage oder klar erkennbare größere Initiativen.

Ein Thema wird aufgeteilt, wenn die Teile:

- unabhängig umgesetzt werden können
- unabhängig reviewed werden können
- unterschiedliche Prioritäten erhalten können
- unterschiedliche Bereiche oder Zeitpunkte betreffen

Nicht künstlich aufteilen, wenn dadurch nur Verwaltungsarbeit entsteht.

Sub-Issues nur einsetzen, wenn die Hierarchie echten Mehrwert bringt.

## 10. Bugs

Ein Bug-Issue sollte möglichst enthalten:

- beobachtetes Verhalten
- erwartetes Verhalten
- reproduzierbare Schritte
- betroffene Komponente
- relevante Umgebung/Version, soweit nötig

P0 ist nur bei tatsächlicher Dringlichkeit erlaubt. Normale Bugs können P1 oder P2 sein.

## 11. Öffentlicher Backlog und sensible Informationen

Das Repository ist öffentlich.

Nicht hier dokumentieren:

- Passwörter
- Tokens oder Secrets
- private E-Mail-Adressen oder persönliche Daten
- interne oder vertrauliche URLs
- konkrete Zugangsdaten
- unnötige Server-IP-Adressen oder Betriebsdetails
- Security-Details, deren Veröffentlichung ein reales Risiko erzeugt

Öffentliche Issues sollen auf Produkt-, Entwicklungs- und Architekturebene formuliert bleiben.

## 12. Pflege des Backlogs

Regelmäßig prüfen:

- Gibt es offene Issues ohne Priorität?
- Gibt es offene Issues ohne Bereich?
- Ist `Ready` noch klein und realistisch?
- Stehen Issues auf `In Progress`, obwohl niemand daran arbeitet?
- Sind P2/P3 versehentlich in den aktiven Ansichten gelandet?
- Gibt es Sammel-Issues, die längst aufgeteilt werden müssten?
- Gibt es erledigte oder überholte Issues, die geschlossen werden sollten?

## 13. Lebenszyklus eines typischen Issues

1. Issue wird erstellt → **Backlog**
2. Priorität und Bereich werden gesetzt
3. Thema wird konkret als nächstes ausgewählt → **Ready**
4. Umsetzung startet → **In Progress**
5. Umsetzung fertig → **Review**
6. Prüfung erfolgreich → Issue schließen → **Done**

Bei echtem Hindernis: **Blocked**.

## 14. Was nicht wieder passieren soll

Das alte WP-System hatte zu viele Querverweise, Prioritäten verloren ihre Bedeutung und Planung verteilte sich über viele Dateien.

Deshalb gelten dauerhaft diese Leitplanken:

- ein zentraler Backlog
- klare Prioritäten
- Status nur im Board
- Bereiche über Labels
- echte statt dekorative Abhängigkeiten
- keine Planungsschattenwelt in Projektdateien
