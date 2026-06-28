# AGIT Project Template

![Lizenz](https://img.shields.io/github/license/ctreffe/agit-project-template)
![Release](https://img.shields.io/github/v/tag/ctreffe/agit-project-template)
![Letzter Commit](https://img.shields.io/github/last-commit/ctreffe/agit-project-template)

[English documentation](README.md)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das AGIT Collaboration Model.
>
> Das Collaboration Model dokumentiert Engineering-Praktiken, Kollaborations-Workflows und Repository-Konventionen, die in AGIT-Projekten verwendet werden.
>
> Es wird in [ChatGPT.md](ChatGPT.md) gepflegt.

## Überblick

Das AGIT Project Template ist der Startpunkt für neue AGIT-Softwareprojekte.

Es stellt eine wiederverwendbare Repository-Grundlage für Dokumentation, Zusammenarbeit, Projektkontext, Repository-Standards und retrospektivische Prozessverbesserung bereit.

Dieses Repository ist kein Code-Framework. Es ist ein Engineering-Template.

## Was das Template bereitstellt

Das Template definiert:

- ein Collaboration Model für KI-gestützte Softwareentwicklung
- eine lokale Codex Operating Policy
- ein Dokument für den aktuellen Projektkontext
- roadmap-first Meilenstein-Guidance
- Dokumentations- und Repository-Standards für Maintainer, Mitwirkende und Nutzer:innen
- eine gemeinsame Engineering-Philosophie
- Versions- und Release-Regeln
- einen Retrospektivenprozess zur Weiterentwicklung des Templates aus realer Projekterfahrung

## Projektkontext

Jedes AGIT-Projekt sollte eine Datei `PROJECT_CONTEXT.md` pflegen.

`PROJECT_CONTEXT.md` ist der zentrale Einstiegspunkt, um die Arbeit an einem Projekt wieder aufzunehmen. Die Datei beschreibt den aktuellen Projektstand, den aktuellen Fokus, den Repository-Baseline-Stand, abgeschlossene Meilensteine, den Validierungsstand, offene Entscheidungen und relevante Dokumentationslinks.

Die Datei ersetzt nicht README, Changelog, Architekturdokumentation oder ADRs. Stattdessen hilft sie dabei zu verstehen, wo das Projekt heute steht und welche Dokumente aktuell relevant sind.

## Entwicklungsworkflow

AGIT-Projekte folgen einem repository-first Workflow.

Das Repository ist der maßgebliche Projektstand. Bei KI-gestützter Zusammenarbeit sollte die Arbeit von einem klaren Repository-Baseline-Stand ausgehen, zum Beispiel einem zugänglichen lokalen Arbeitsbaum, einem öffentlichen Repository-Stand oder einem aktuellen ZIP-Archiv.

Der bevorzugte Ablauf ist:

1. Aktuellen Repository-Baseline-Stand festlegen.
2. Roadmap festlegen oder prüfen und den nächsten Meilenstein-Schritt vereinbaren.
3. Kleine, prüfbare Änderung umsetzen.
4. Änderung validieren, sofern praktisch möglich.
5. Während der Validierung gefundene Fehler beheben.
6. Betroffene Code-, Anwender:innen- und Projektdokumentation aktualisieren.
7. Repository-ready Beitrag in der vereinbarten Lieferform vorbereiten.
8. Validierten Schritt committen.
9. Meilensteine getrennt von Feature-Arbeit abschließen.

Explizite Aufforderungen wie „erstelle den Commit“ bedeuten, dass das angeforderte repository-ready Ergebnis erzeugt und nicht nur beschrieben werden soll. Artefaktintegrität ist Teil des Workflows: lokale Arbeitsbaumänderungen, erzeugte Archive, Commits und Repository-Aktualisierungen müssen tatsächlich existieren, bevor sie als abgeschlossen gemeldet werden.

## Verwendung des Templates

1. Neues Repository aus diesem Template erstellen.
2. Initialen Repository-Baseline-Stand aus dem lokalen Arbeitsbaum, dem öffentlichen Repository oder einem ZIP-Archiv festlegen.
3. `PROJECT_SETUP.md` lesen.
4. README-Dateien und Repository-Metadaten an das neue Projekt anpassen.
5. Eine AI Collaboration Note direkt unter den README-Badges beibehalten und projektspezifische Formulierungen bei Bedarf sachlich korrekt anpassen.
6. `PROJECT_CONTEXT.md` als Einstiegspunkt für den aktuellen Projektstand anlegen oder anpassen.
7. Initiale Roadmap festlegen und in `PROJECT_CONTEXT.md` oder einem eigenen Roadmap-Dokument festhalten.
8. Kerndokumente prüfen.
9. `CODEX.md` prüfen, wenn Codex für lokale Projektarbeit verwendet wird.
10. Template-spezifische Setup-Dokumente entfernen, sobald die Projekteinrichtung abgeschlossen ist.
11. Entwicklung gemäß `ChatGPT.md` fortsetzen.

## Dokumente, die normalerweise bleiben

Die folgenden Dokumente bleiben normalerweise Teil eines abgeleiteten Projekts:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md`, sofern sinnvoll
- `CHANGELOG.md`
- `ChatGPT.md`
- `CODEX.md`, wenn Codex für lokale Projektarbeit verwendet wird
- `PHILOSOPHY.md`
- `LICENSE`

## Template-spezifische Dokumente

Die folgenden Dokumente unterstützen vor allem die Projekteinrichtung:

- `PROJECT_SETUP.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

Nach Abschluss der Ersteinrichtung können diese Dokumente aus dem abgeleiteten Projekt entfernt werden, sofern sie dort nicht weiterhin nützlich sind.

## Kontinuierliche Weiterentwicklung

Das AGIT Project Template entwickelt sich durch Projektretrospektiven weiter.

Retrospektiven finden normalerweise am Ende eines Projekts statt, können aber auch während eines Projekts eingeschoben werden, wenn ausreichend praktische Erkenntnisse vorliegen.

Änderungen am Template sollen ausschließlich im Rahmen einer solchen Retrospektive erfolgen. Wenn eine Retrospektive zentrale Prozessregeln verändert, sollen betroffene Dokumente harmonisiert werden, statt nur isolierte Notizen zu ergänzen.

## Kerndokumente des Templates

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) – aktueller Projektstand und zentraler Wiedereinstiegspunkt
- [PROJECT_SETUP.md](PROJECT_SETUP.md) – Anleitung zur Ersteinrichtung neuer Projekte
- [ChatGPT.md](ChatGPT.md) – Collaboration Model
- [CODEX.md](CODEX.md) – lokale Codex Operating Policy
- [PHILOSOPHY.md](PHILOSOPHY.md) – Projektphilosophie
- [DOCUMENTATION.md](DOCUMENTATION.md) – Dokumentationsstandards
- [REPOSITORY.md](REPOSITORY.md) – Repository-Standards
- [CHANGELOG.md](CHANGELOG.md) – Versionshistorie
- [README.md](README.md) – englische Dokumentation
- [LICENSE](LICENSE) – MIT-Lizenz

## Lizenz

Dieses Projekt steht unter der MIT-Lizenz.
