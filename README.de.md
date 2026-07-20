# AGIT Dev Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/agit-dev-template?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/agit-dev-template)](LICENSE)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das AGIT Dev Template.
>
> Das AGIT Dev Template ist die entwicklungsorientierte Spezialisierung des generischen AGIT Project Template.
>
> Das Kollaborationsmodell dokumentiert Engineering-Praktiken, KI-gestützte Entwicklungsworkflows und Repository-Konventionen für entwicklungsorientierte AGIT-Projekte.
>
> Das Kollaborationsmodell wird in [ChatGPT.md](ChatGPT.md) gepflegt.

<br>

**[Link to the English README](README.md)**

<br>

## Inhalt

- [Überblick](#überblick)
- [Kernprinzip](#kernprinzip)
- [AGIT Templateverse](#agit-templateverse)
- [Wann dieses Template geeignet ist](#wann-dieses-template-geeignet-ist)
- [Projektinitialisierung](#projektinitialisierung)
- [Empfohlener Workflow](#empfohlener-workflow)
- [Git-Index und geschützte Git-Aktionen](#git-index-und-geschützte-git-aktionen)
- [Decision Records](#decision-records)
- [Repository-Struktur](#repository-struktur)
- [Template- und abgeleitete Projektdateien](#template--und-abgeleitete-projektdateien)
- [Verwendung dieses Templates](#verwendung-dieses-templates)
- [Tool-Setup für Maintainer](#tool-setup-für-maintainer)
- [Kontinuierliche Verbesserung](#kontinuierliche-verbesserung)
- [Lizenz](#lizenz)

## Überblick

Das AGIT Dev Template ist der Ausgangspunkt für entwicklungsorientierte Projekte mit Code, Skripten, Automatisierung, technischer Architektur, Validierung, Releases und benutzerorientierter technischer Dokumentation. Es stellt eine wiederverwendbare Repository-Grundlage und Kollaborationsmethode bereit, kein Programmierframework oder Anwendungsgerüst.

Das Template verbindet die vom Maintainer definierte Intention mit Roadmap-orientierter Implementierung, kleinen prüfbaren Änderungen, expliziter Validierung, dauerhaftem Projektkontext, dokumentierten technischen Entscheidungen und repository-fertiger Übergabe. Es baut auf dem generischen AGIT Project Template auf und ergänzt Engineering-spezifische Anforderungen an Codelesbarkeit, sensible Inputs, erzeugte Artefakte und Release-Disziplin.

## Kernprinzip

Der Maintainer verantwortet Projektrichtung, Architektur und Release-Entscheidungen. Der Assistant kann beim Entwerfen, Implementieren, Testen, Dokumentieren und Prüfen helfen, muss aber die Autorität des Maintainers wahren, Annahmen und Einschränkungen sichtbar machen und darf abgeschlossenen Code, Validierungen, Commits oder Artefakte niemals simulieren.

Das Repository ist der maßgebliche Engineering-Zustand. Code und Dokumentation sollen für künftige Maintainer ohne private Chatverläufe verständlich sein, und eine Änderung ist nicht abgeschlossen, nur weil sie einmal funktioniert hat.

## AGIT Templateverse

Die öffentlichen AGIT-Templates bilden ein kleines Templateverse: eine Familie verwandter Templates, die ein Repository-zentriertes, vom Maintainer geführtes Modell der Mensch-KI-Zusammenarbeit teilen und es für unterschiedliche Projekttypen spezialisieren.

- Das [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Ausgangspunkt für strukturierte Projektarbeit, Forschung, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- Das [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- Das [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte wie Benutzer- und Administrationshandbücher, Betriebsanweisungen, Tutorials, Migrationsleitfäden und Dokumentationswebsites gedacht.

## Wann dieses Template geeignet ist

Verwende das Dev Template, wenn Implementierungslebenszyklus, Validierung und Release-Disziplin von Beginn an zentral sind. Typische Projekte sind Kommandozeilenwerkzeuge, Skripte, Automatisierung, Integrationshilfen, Deployment-Tools, Bibliotheken, Prototypen mit validiertem Erkenntnisziel und Repositories mit technischer Konfiguration oder operativen Workflows.

Verwende das generische Project Template, wenn das Projekt noch überwiegend Discovery, Planung oder gemischte nicht-technische Arbeit ist. Ein generisches Projekt kann bewusst zu diesem Template migrieren, sobald Code, Tests, Architektur oder Releases zentral werden.

## Projektinitialisierung

Nach dem Erzeugen des Repositorys muss der Maintainer nur [INITIAL_PROMPT.md](INITIAL_PROMPT.md) aufrufen. Der Agent liest das Repository und seine Setup-Leitlinien und führt anschließend durch die vollständige Initialisierung. Der Maintainer muss `PROJECT_SETUP.md` nicht selbst öffnen oder ausführen.

Die einfachste Anweisung an den Agenten lautet:

> Lies `INITIAL_PROMPT.md` vollständig und führe den darin enthaltenen Initialisierungs-Prompt aus.

Die Datei muss dafür nicht geöffnet und ihr Prompt nicht in die Unterhaltung kopiert werden.

Der Agent:

1. liest die Kollaborations-, Engineering-, Setup-, Dokumentations-, Repository- und Entscheidungsregeln;
2. prüft die Repository-Baseline, ohne die Git-Historie zu verändern;
3. legt kompakte Fragen zu Problem, gewünschtem Endzustand, Nutzer:innen, Umgebung, Grenzen, Roadmap, Validierungsmodell und Code-Leserschaft vor;
4. fragt vom Maintainer zu treffende Architektur-, sensible Input- und Projektentscheidungen ab, statt sie zu erfinden;
5. passt nach den Antworten README-Dateien, Projektkontext, Repository-Regeln und Projektstruktur an;
6. legt Regeln für Secrets, Logs, Dumps, Screenshots, Fixtures und erzeugte Artefakte fest;
7. validiert die initiale technische Baseline und bereitet die erste kleine projektspezifische Änderung vor; und
8. übergibt den initialisierten Stand mit Prüfergebnissen, offenen Entscheidungen und vorgeschlagenen Commit-Metadaten.

`PROJECT_SETUP.md` bleibt die ausführliche Checkliste des Agenten und ein Provenienzartefakt der Initialisierung. `INITIAL_PROMPT.md` ist der einzige benutzerorientierte Einstiegspunkt, der sie aktiviert.

## Empfohlener Workflow

Entwicklung erfolgt in kleinen, validierten Schleifen:

```text
Intention -> Roadmap -> Implementieren -> Validieren -> Anpassen -> Dokumentieren -> Commit vorbereiten -> Fortsetzen
```

1. Ermittle die aktuelle Repository- und Working-Tree-Baseline.
2. Bestätige den aktiven Roadmap-Schritt und was er nachweisen oder liefern soll.
3. Implementiere eine logische, prüfbare Änderung.
4. Führe relevante Tests, Skripte, Linter, Renderer oder Maintainer-lokale Validierungen aus.
5. Behebe gefundene Probleme, bevor der Schritt als bereit dargestellt wird.
6. Aktualisiere Code-Kommentare, technische Dokumentation und benutzerorientierte Leitlinien, die vom Verhalten betroffen sind.
7. Dokumentiere folgenreiche Architektur-, Projekt- oder Dokumentationsentscheidungen.
8. Bereite einen regulären Arbeits-Commit mit passendem Conventional-Commit-Präfix vor.
9. Schließe einen erfüllten Milestone separat ab, indem Version, Changelog, Projektkontext und validierter Status harmonisiert werden.

Verwende [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md) für einen reproduzierbaren Wiedereinstieg, [HARMONIZATION_PROMPT.md](HARMONIZATION_PROMPT.md) für die Abstimmung von Projektinhalt und Roadmap und [RETROSPECTIVE_PROMPT.md](RETROSPECTIVE_PROMPT.md) für eine separate Bewertung der Maintainer-Agent-Zusammenarbeit.

## Git-Index und geschützte Git-Aktionen

Der Maintainer kontrolliert die Git-Historie, normalerweise über GitHub Desktop. Assistants dürfen Status, Diffs und Logs prüfen, Working-Tree-Änderungen vorbereiten, Commit-Grenzen vorschlagen sowie Zusammenfassungen und Beschreibungen bereitstellen.

Staging und Unstaging sind Indexoperationen. Sie benötigen kein Kontrollwort, dürfen aber nur nach einer konkreten Maintainer-Anweisung oder Autorisierung des zugehörigen Commits erfolgen. Bestehende Staging-Auswahlen und nicht zusammenhängende Änderungen müssen erhalten bleiben.

Geschützte Aktionen umfassen Commits, Amendments, Tags, Pushes, Pulls, Merges, Rebases, Resets, Branch-Wechsel, Stash-Manipulationen und andere Operationen an der Git-Historie. Ein Assistant darf eine bestimmte geschützte Aktion nur ausführen, wenn die Anweisung für genau diese Aktion `explicit` oder `explicitly` auf Englisch oder die deutsche Wortfamilie `explizit` enthält. Die Freigabe von Dateiänderungen autorisiert keine Änderung der Git-Historie; die Freigabe einer geschützten Aktion autorisiert keine andere.

Reguläre Engineering-Commits verwenden Präfixe wie `feat:`, `fix:`, `docs:`, `refactor:` oder `test:`. Milestone-Commits verzichten auf das Präfix, nennen die abgeschlossene Version und schließen Arbeit ab, die bereits durch reguläre Commits implementiert und validiert wurde.

## Decision Records

Wähle den Record-Typ nach dem Entscheidungsgegenstand:

- **ADR — Architecture Decision Record:** Architektur, Schnittstellen, Konfigurationsformate, Lebenszyklusverhalten, Deployment, Sicherheitsgrenzen, Behandlung sensibler Inputs, Fixture-Versionierung oder Richtlinien für erzeugte Artefakte.
- **PDR — Project Decision Record:** Umfang, Roadmap, Zusammenarbeit, Datenschutz, Repository-Struktur, Release-Modell oder Governance.
- **DDR — Documentation Decision Record:** Benutzerdokumentation, Referenzstruktur, Terminologie, Beispiele, Screenshots oder Dokumentations-QA.

Vorlagen befinden sich in [decisions/](decisions/). Erstelle einen Record, wenn künftige Maintainer Kontext, Begründung und Konsequenzen benötigen; routinemäßige Implementierungsdetails gehören stattdessen in Code, Tests oder gewöhnliche Dokumentation.

## Repository-Struktur

### Einstiegspunkte und Projektgedächtnis

- **`README.md` und `README.de.md`** führen auf Englisch und Deutsch in das Softwareprojekt ein und erklären Setup, Konfiguration, Nutzung und Navigation.
- **`PROJECT_CONTEXT.md`** ist der primäre Wiedereinstiegspunkt für aktuelle Intention, Status, Roadmap, Baseline, Validierung und nächste Schritte. Die Datei soll den gegenwärtigen Engineering-Zustand beschreiben, nicht Changelog oder Architekturhistorie duplizieren.
- **`CHANGELOG.md` und `VERSION`** halten abgeschlossene Änderungen und die letzte abgeschlossene Version fest. Sie sind Milestone-Artefakte und dürfen keinen noch nicht validierten Release-Zustand suggerieren.

### Zusammenarbeit und Engineering-Regeln

- **`ChatGPT.md`** definiert das Entwicklungskollaborationsmodell, den Roadmap-Rhythmus, die Validierungspartnerschaft und Erwartungen an repository-fertige Übergaben.
- **`CODEX.md`** definiert lokale Tool-, Netzwerk-, Offenlegungs-, Multi-Repository- und Git-Regeln für Codex auf dem Maintainer-System.
- **`PHILOSOPHY.md`** hält die Engineering-Werte hinter dem Template fest, darunter Einfachheit, Wartbarkeit, Transparenz, validiertes Lernen und Integrität.
- **`DOCUMENTATION.md`** definiert Rollen und Qualitätsanforderungen der Projekt-, Code- und Benutzerdokumentation. Sie behandelt Dokumentation als Teil der Software.
- **`REPOSITORY.md`** definiert Benennung, Git-Workflow, Commits, Versionierung, Releases, sensible Inputs und repository-fertige Übergaben. Die Datei bleibt nach dem Setup eine aktive Projektregel.

### Setup, Fortsetzung und Review

- **`PROJECT_SETUP.md` und `INITIAL_PROMPT.md`** leiten die erste Initialisierung an und bewahren ihre methodische Baseline. Abgeleitete Projekte behalten sie normalerweise unter ihren ursprünglichen Namen.
- **`CONTINUATION_PROMPT.md`** rekonstruiert Git-, Implementierungs-, Validierungs- und Dokumentationszustand, bevor die Arbeit in einer neuen Sitzung fortgesetzt wird.
- **`HARMONIZATION_PROMPT.md`** vergleicht ein abgeleitetes Projekt mit seiner aufgezeichneten Source-Template-Baseline und gleicht Code, Tests, Dokumentation und Roadmap ab, ohne Änderungen blind zu kopieren.
- **`RETROSPECTIVE_PROMPT.md`** bewertet Kollaborationspraktiken getrennt vom Projektinhalt und erzeugt kontrollierte Kandidaten für Projekt- oder Template-Verbesserungen.

### Entscheidungen und projektspezifischer Code

- **`decisions/`** enthält wiederverwendbare ADR-, PDR- und DDR-Vorlagen und in abgeleiteten Projekten akzeptierte dauerhafte Entscheidungen. Der Ordner soll nicht zum Protokoll jeder kleinen Implementierungsentscheidung werden.
- **Projektspezifische Quellen, Tests, Skripte und Konfigurationen** werden während der Initialisierung entsprechend der vom Maintainer gewählten Technologie und Architektur ergänzt. Ihre Struktur sollte dokumentiert werden, wenn Namen und Aufbau allein für neue Mitwirkende nicht ausreichend verständlich sind.
- **Projektlokale Umgebungen und erzeugte Artefakte** verwenden normalerweise ignorierte Orte wie `.venv/`, `node_modules/`, `artifacts/` oder `deliverables/`. Dokumentiere, ob erzeugte Outputs reproduzierbare lokale Dateien, Review-Artefakte oder Release-Deliverables sind.

## Template- und abgeleitete Projektdateien

In einem abgeleiteten Entwicklungsprojekt:

- ersetze Template-Identität und Platzhalterinhalte durch konkreten Projektnamen, Zweck, Setup und Nutzung;
- fülle `PROJECT_CONTEXT.md` aus und pflege die Datei kontinuierlich;
- passe `DOCUMENTATION.md` und `REPOSITORY.md` als laufende Regeln an;
- behalte normalerweise `ChatGPT.md`, `CODEX.md` und `PHILOSOPHY.md`;
- behalte `PROJECT_SETUP.md`, `INITIAL_PROMPT.md` und die drei Prompts für spätere Sitzungen als Provenienz und wiederholbare Betriebswerkzeuge;
- ergänze die vom Projekt benötigte Quellen-, Test-, Konfigurations- und Dokumentationsstruktur;
- erstelle echte Decision Records nur für folgenreiche Entscheidungen;
- halte die standardisierte KI-Kollaborationsnotiz sichtbar und sachlich korrekt.

Halte Source-Template-Version und -Commit, Initialisierungsstatus, letzte Harmonisierungs-Baseline und beabsichtigte Abweichungen in `PROJECT_CONTEXT.md` fest. Das getestete Verhalten und die akzeptierten Entscheidungen eines abgeleiteten Projekts bleiben gegenüber späteren generischen Template-Änderungen maßgeblich.

## Verwendung dieses Templates

1. Erzeuge ein Repository aus dem Template und gib dem Agenten die Anweisung aus `INITIAL_PROMPT.md`.
2. Beantworte die nummerierten Fragen des Agenten; er liest und verarbeitet `PROJECT_SETUP.md` und die übrigen Setup-Leitlinien automatisch.
3. Prüfe den initialisierten Repository-Stand, die Validierungsergebnisse und den vorgeschlagenen ersten Commit.
4. Lass den Agenten die Maintainer-Intention erfassen und eine validierungsorientierte Roadmap ableiten.
5. Richte die für das konkrete Projekt benötigte Code-, Test-, Dokumentations- und lokale Toolstruktur ein.
6. Halte private Inputs außerhalb von Git und bevorzuge bereinigte Fixtures, die Verhalten ohne unnötige Offenlegung reproduzieren.
7. Implementiere jeweils eine logische Änderung und validiere sie vor einer Commit-Empfehlung.
8. Dokumentiere öffentliches Verhalten, Konfiguration, Befehle, Risiken und Fehlerbehebung, wenn sie die Nutzung beeinflussen.
9. Dokumentiere dauerhafte Entscheidungen, halte `PROJECT_CONTEXT.md` aktuell und nutze die Prompts für Fortsetzung, Harmonisierung und Retrospektive nach Bedarf.
10. Schließe Milestones erst ab, wenn Implementierung, Validierung, Dokumentation und Versionsmetadaten einen kohärenten Zustand bilden.

## Tool-Setup für Maintainer

Installiere nur die Werkzeuge, die das abgeleitete Projekt benötigt. Eine praktische Baseline für lokale Codex-gestützte Entwicklung ist:

- [Git for Windows](https://gitforwindows.org/) und [GitHub Desktop](https://desktop.github.com/download/);
- [PowerShell](https://learn.microsoft.com/powershell/scripting/install/installing-powershell-on-windows);
- [ripgrep (`rg`)](https://github.com/BurntSushi/ripgrep/releases) oder ein anderes schnelles lokales Suchwerkzeug;
- [Python](https://www.python.org/downloads/) mit einer projektlokalen virtuellen Umgebung, falls benötigt;
- [Node.js](https://nodejs.org/en/download/) mit projektlokalen Abhängigkeiten, falls benötigt;
- projektspezifische Test-, Lint-, Render- oder Build-Werkzeuge.

Bevorzuge lokale Umgebungen wie `.venv/` und `node_modules/` gegenüber globaler Installation. Halte Umgebungsdateien, Caches, Logs, Rohinputs und erzeugte Arbeitsartefakte ignoriert, sofern das Projekt nicht bewusst ein geprüftes Artefakt versioniert.

## Kontinuierliche Verbesserung

Entwicklungsprojekte sollten bewährte Praktiken bewahren und unnötige Komplexität entfernen. Validierte negative Ergebnisse, wiederkehrende Validierungsprobleme und Wartbarkeitserkenntnisse sind legitimes Projektwissen.

Nutze Harmonisierung, um Projektinhalt, Implementierung und Roadmap abzugleichen. Nutze Retrospektiven, um Zusammenarbeit zu bewerten und übertragbare Template-Verbesserungen vorzuschlagen. Template-Änderungen sollen betroffene Leitlinien kohärent aktualisieren und nicht eine einzelne Projekterfahrung überpassen.

## Lizenz

Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).
