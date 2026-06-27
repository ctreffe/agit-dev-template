# AGIT Project Template

![Lizenz](https://img.shields.io/github/license/ctreffe/agit-project-template)
![Release](https://img.shields.io/github/v/tag/ctreffe/agit-project-template)
![Letzter Commit](https://img.shields.io/github/last-commit/ctreffe/agit-project-template)

[English documentation](README.md)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das aktuelle AGIT Collaboration Model.
>
> Das Collaboration Model dokumentiert Engineering-Praktiken, Kollaborations-Workflows und Repository-Konventionen, die in AGIT-Projekten verwendet werden.
>
> Es wird in [ChatGPT.md](ChatGPT.md) gepflegt.

## Überblick

Das AGIT Project Template ist der Startpunkt für neue AGIT-Softwareprojekte.

Es stellt eine wiederverwendbare Repository-Grundlage mit Dokumentations-, Kollaborations- und Repository-Standards bereit.

Dieses Repository ist kein Code-Framework. Es ist ein Engineering-Template.


## Projektkontext

Jedes AGIT-Projekt sollte eine Datei `PROJECT_CONTEXT.md` pflegen.

`PROJECT_CONTEXT.md` ist der zentrale Einstiegspunkt, um die Arbeit an einem Projekt wieder aufzunehmen. Die Datei beschreibt den aktuellen Projektstand, den aktuellen Fokus, abgeschlossene Meilensteine, offene Entscheidungen und relevante Dokumentationslinks.

Die Datei ersetzt nicht README, Changelog, Architekturdokumentation oder ADRs. Stattdessen hilft sie dabei zu verstehen, wo das Projekt heute steht und welche Dokumente aktuell relevant sind.

## Verwendung des Templates

1. Neues Repository aus diesem Template erstellen.
2. Das neu erstellte Repository als ZIP-Datei herunterladen.
3. Bei KI-gestützter Zusammenarbeit die ZIP-Datei hochladen, damit der vollständige Repository-Stand verfügbar ist.
4. `PROJECT_SETUP.md` lesen.
5. README-Dateien und Repository-Metadaten an das neue Projekt anpassen.
6. `PROJECT_CONTEXT.md` als Einstiegspunkt für den aktuellen Projektstand anlegen oder anpassen.
7. Kerndokumente prüfen.
8. Template-spezifische Setup-Dokumente entfernen, sobald die Projekteinrichtung abgeschlossen ist.

## Dokumente, die normalerweise bleiben

Die folgenden Dokumente bleiben normalerweise Teil eines abgeleiteten Projekts:

- `PROJECT_CONTEXT.md`
- `README.md`
- `README.de.md`, sofern sinnvoll
- `CHANGELOG.md`
- `ChatGPT.md`
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

Retrospektiven finden normalerweise am Ende eines Projekts statt, können aber auch während eines Projekts eingeschoben werden, wenn ausreichend praktische Erkenntnisse vorliegen. Änderungen am Template sollen ausschließlich im Rahmen einer solchen Retrospektive erfolgen, nicht beiläufig während der normalen Projektarbeit.

## Kerndokumente des Templates

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) – aktueller Projektstand und zentraler Wiedereinstiegspunkt
- [PROJECT_SETUP.md](PROJECT_SETUP.md) – Anleitung zur Ersteinrichtung neuer Projekte
- [ChatGPT.md](ChatGPT.md) – Collaboration Model
- [PHILOSOPHY.md](PHILOSOPHY.md) – Projektphilosophie
- [DOCUMENTATION.md](DOCUMENTATION.md) – Dokumentationsstandards
- [REPOSITORY.md](REPOSITORY.md) – Repository-Standards
- [CHANGELOG.md](CHANGELOG.md) – Versionshistorie
- [README.md](README.md) – englische Dokumentation
- [LICENSE](LICENSE) – MIT-Lizenz

## Lizenz

Dieses Projekt steht unter der MIT-Lizenz.
