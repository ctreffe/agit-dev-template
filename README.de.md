# AGIT Dev Template

![Lizenz](https://img.shields.io/github/license/ctreffe/agit-dev-template)
![Release](https://img.shields.io/github/v/tag/ctreffe/agit-dev-template)
![Letzter Commit](https://img.shields.io/github/last-commit/ctreffe/agit-dev-template)

[English documentation](README.md)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das AGIT Dev Template.
>
> Das AGIT Dev Template ist die entwicklungsorientierte Spezialisierung des generischen AGIT Project Template.
>
> Das Collaboration Model dokumentiert Engineering-Praktiken, KI-gestützte Entwicklungsworkflows und Repository-Konventionen für entwicklungsorientierte AGIT-Projekte.
>
> Das Collaboration Model wird in [ChatGPT.md](ChatGPT.md) gepflegt.

## Überblick

Das AGIT Dev Template ist der Startpunkt für entwicklungsorientierte AGIT-Projekte.

Es stellt eine wiederverwendbare Repository-Grundlage für Projekte mit Code, Skripten, Automatisierung, technischer Dokumentation, Validierung, Releases, Repository-Standards und retrospektivischer Prozessverbesserung bereit.

Dieses Repository ist kein Code-Framework. Es ist ein Entwicklungsprojekt-Template.

Das AGIT Dev Template baut auf dem generischen [AGIT Project Template](https://github.com/ctreffe/agit-project-template) auf. Für nicht entwicklungsorientierte Projekte sollte das generische Template verwendet werden; dieses Template ist für Projekte gedacht, in denen Software, Skripte, Automatisierung, Validierung, technische Architektur oder Release-Workflows zentral sind.

## AGIT Templateverse

Die öffentlichen AGIT Templates bilden ein kleines Templateverse: eine Familie zusammenhängender Templates, die ein repository-first, maintainer-geführtes Modell für Human-AI Collaboration teilen und für unterschiedliche Projekttypen spezialisieren.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Startpunkt für strukturierte Projektarbeit, Recherche, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte gedacht, etwa Benutzerhandbücher, Admin-Guides, Betriebsanweisungen, Tutorials, Migrationsguides und Dokumentationssites.

Das Dev Template passt, wenn Implementierungslebenszyklus, Validierung und Release-Disziplin von Anfang an Teil des Projekts sind. Das generische Project Template passt, wenn diese Anforderungen erst später entstehen können.

## Was das Template bereitstellt

Das Template definiert:

- ein Collaboration Model für KI-gestützte Softwareentwicklung
- eine lokale Codex Operating Policy
- ein Dokument für den aktuellen Projektkontext
- Guidance für Maintainer-Projektintent und Zielbild
- roadmap-first Meilenstein-Guidance
- Dokumentations- und Repository-Standards für Maintainer, Mitwirkende und Nutzer:innen
- Guidance für sensible lokale Inputs, anonymisierte Fixtures und generierte Artefakte
- eine gemeinsame Engineering-Philosophie
- Versions- und Release-Regeln
- einen Retrospektivenprozess zur Weiterentwicklung des Templates aus realer Projekterfahrung

## Projektkontext

Jedes AGIT-Projekt sollte eine Datei `PROJECT_CONTEXT.md` pflegen.

`PROJECT_CONTEXT.md` ist der zentrale Einstiegspunkt, um die Arbeit an einem Projekt wieder aufzunehmen. Die Datei beschreibt den aktuellen Projektstand, den aktuellen Fokus, den Repository-Baseline-Stand, abgeschlossene Meilensteine, den Validierungsstand, offene Entscheidungen und relevante Dokumentationslinks.

Die Datei ersetzt nicht README, Changelog, Architekturdokumentation oder Decision Records. Stattdessen hilft sie dabei zu verstehen, wo das Projekt heute steht und welche Dokumente aktuell relevant sind.

Zu Projektbeginn sollte `PROJECT_CONTEXT.md` außerdem den Projektintent aus Maintainer-Sicht festhalten: Problemkontext, gewünschtes Zielbild, wichtige Grenzen und Auswirkungen auf die Roadmap. Dieser Maintainer-eigene Kontext gibt der Roadmap Richtung, bevor Implementierung beschleunigt.

## Entwicklungsworkflow

AGIT-Projekte folgen einem repository-first Workflow.

Das Repository ist der maßgebliche Projektstand. Bei KI-gestützter Zusammenarbeit sollte die Arbeit von einem klaren Repository-Baseline-Stand ausgehen, zum Beispiel einem zugänglichen lokalen Arbeitsbaum, einem öffentlichen Repository-Stand oder einem aktuellen ZIP-Archiv.

Der bevorzugte Ablauf ist:

1. Aktuellen Repository-Baseline-Stand festlegen.
2. Maintainer-Projektintent und gewünschtes Zielbild festlegen oder prüfen.
3. Roadmap festlegen oder prüfen und den nächsten Meilenstein-Schritt vereinbaren.
4. Kleine, prüfbare Änderung umsetzen.
5. Änderung validieren, sofern praktisch möglich.
6. Während der Validierung gefundene Fehler beheben.
7. Betroffene Code-, Anwender:innen- und Projektdokumentation aktualisieren.
8. Repository-ready Beitrag in der vereinbarten Lieferform vorbereiten.
9. Validierten Schritt committen.
10. Meilensteine getrennt von Feature-Arbeit abschließen.

Aufforderungen wie „erstelle den Commit“ bedeuten, dass das angeforderte repository-ready Ergebnis vorbereitet und nicht nur beschrieben werden soll. Sie erlauben dem Assistant keine Git-History-Befehle, sofern die Anfrage kein anerkanntes Kontrollwort enthält. Artefaktintegrität ist Teil des Workflows: lokale Arbeitsbaumänderungen, erzeugte Archive und vorbereitete Repository-Aktualisierungen müssen tatsächlich existieren, bevor sie als abgeschlossen gemeldet werden.

## Kontrollwörter für Git-History-Aktionen

AI Assistants dürfen Git-History-Aktionen wie Staging, Commit, Tag, Push, Pull, Merge, Rebase, Reset oder Branch-Wechsel nur ausführen, wenn die Maintainer-Anweisung für genau diese Aktion ein anerkanntes Kontrollwort enthält.

Anerkannte Kontrollwörter sind `explicit` und `explicitly` in englischsprachigen Anweisungen sowie die deutsche Wortfamilie `explizit`, einschließlich gebeugter Formen wie `explizite`, `expliziten`, `expliziter` und `explizites`, in deutschsprachigen Anweisungen. Anfragen ohne eines dieser Kontrollwörter erlauben nur Vorbereitung und Anleitung.

## Verwendung des Templates

1. Neues Repository aus diesem Template erstellen.
2. Initialen Repository-Baseline-Stand aus dem lokalen Arbeitsbaum, dem öffentlichen Repository oder einem ZIP-Archiv festlegen.
3. `PROJECT_SETUP.md` lesen.
4. README-Dateien und Repository-Metadaten an das neue Projekt anpassen.
5. Eine AI Collaboration Note direkt unter den README-Badges beibehalten und projektspezifische Formulierungen bei Bedarf sachlich korrekt anpassen.
6. Projektintent, Kontext, gewünschtes Zielbild und Grenzen aus Maintainer-Sicht festhalten.
7. `PROJECT_CONTEXT.md` als Einstiegspunkt für den aktuellen Projektstand anlegen oder anpassen.
8. Initiale Roadmap aus dem Maintainer-Intent ableiten und in `PROJECT_CONTEXT.md` oder einem eigenen Roadmap-Dokument festhalten.
9. Kerndokumente prüfen.
10. `CODEX.md` prüfen, wenn Codex für lokale Projektarbeit verwendet wird.
11. Initialisierungsherkunft und Ausgangsstand des Templates dokumentieren.
12. Entwicklung gemäß `ChatGPT.md` fortsetzen.

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

## Initialisierungsnachweis

Die folgenden Dokumente unterstützen vor allem die Projekteinrichtung und
sollten als Nachweis des methodischen Ausgangspunkts erhalten bleiben:

- `PROJECT_SETUP.md`
- `INITIAL_PROMPT.md`

Initialisierungsstatus, ursprüngliche Template-Version und ursprünglicher
Template-Commit, spätere Harmonisierungsstände sowie bewusste Abweichungen
werden in `PROJECT_CONTEXT.md` festgehalten. Eine Initialisierungsdatei wird nur
als bewusste und dokumentierte Maintainer-Ausnahme entfernt.

`DOCUMENTATION.md` und `REPOSITORY.md` enthalten fortlaufend geltende
Projektregeln und werden im abgeleiteten Projekt angepasst und gepflegt.

## Kontinuierliche Weiterentwicklung

Das AGIT Dev Template entwickelt sich durch Collaboration-Retrospektiven weiter.

Der Maintainer entscheidet, wann eine Harmonisierung oder Retrospektive
ausgeführt wird und welchen Projektzeitraum oder Umfang sie betrachtet.

Retrospektivbefunde sind zunächst Template-Kandidaten. Der Assistant darf eine
konkrete Template-Änderung nur mit anerkannter Kontrollwortfreigabe umsetzen;
Git-History-Aktionen bleiben davon getrennt kontrolliert. Betrifft eine
autorisierte Änderung zentrale Prozessregeln, werden alle betroffenen Dokumente
harmonisiert, statt nur isolierte Notizen zu ergänzen.

## Kerndokumente des Templates

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) – aktueller Projektstand und zentraler Wiedereinstiegspunkt
- [PROJECT_SETUP.md](PROJECT_SETUP.md) – Anleitung zur Ersteinrichtung neuer Projekte
- [INITIAL_PROMPT.md](INITIAL_PROMPT.md) – erster Prompt für reproduzierbare Projektinitialisierung
- [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md) – Wiedereinstiegsprompt für ein neues Kontextfenster oder eine neue Assistant-Session
- [HARMONIZATION_PROMPT.md](HARMONIZATION_PROMPT.md) – Abgleich mit dem Quell-Template sowie Code-, Dokumentations- und Roadmap-Harmonisierung
- [RETROSPECTIVE_PROMPT.md](RETROSPECTIVE_PROMPT.md) – Maintainer-initiierter Review der Entwicklungszusammenarbeit
- [ChatGPT.md](ChatGPT.md) – Collaboration Model
- [CODEX.md](CODEX.md) – lokale Codex Operating Policy
- [PHILOSOPHY.md](PHILOSOPHY.md) – Projektphilosophie
- [DOCUMENTATION.md](DOCUMENTATION.md) – Dokumentationsstandards
- [REPOSITORY.md](REPOSITORY.md) – Repository-Standards
- [decisions/](decisions/) – Decision-Record-Templates für ADRs, PDRs und DDRs
- [CHANGELOG.md](CHANGELOG.md) – Versionshistorie
- [README.md](README.md) – englische Dokumentation
- [LICENSE](LICENSE) – MIT-Lizenz

## Lizenz

Dieses Projekt steht unter der MIT-Lizenz.
