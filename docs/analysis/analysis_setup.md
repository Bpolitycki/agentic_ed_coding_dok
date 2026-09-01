# Versuchsanordnung

Basierend auf den formulierten Erwartungen wird die Auswertung des Experiments mittels verschiedener, aufeinander aufbauender Beobachtungs- und Vergleichstabellen vorgenommen. Ziel ist es, die Ergebnisse nicht unmittelbar anhand ihrer gestalterischen oder technischen Qualität zu bewerten, sondern nachvollziehbar zu beschreiben, wie die untersuchten Coding-Agenten die bereitgestellten editorischen Informationen erfassen, auswählen, hierarchisieren und in konkrete Interfaceformen übersetzen.

Dabei werden drei analytische Ebenen unterschieden:

1. **Datengrundlage:** Welche editorischen Informationen und Relationen stehen den Agenten überhaupt zur Verfügung?

2. **Modellrekonstruktion und Arbeitsprozess:** Wie verstehen die Agenten die Edition, welche Strukturen erkennen sie und welche Gestaltungsentscheidungen leiten sie daraus ab?

3. **Interface und epistemische Ordnung:** Welche der erkannten Informationen werden tatsächlich dargestellt, wie werden sie hierarchisiert und in welche Nutzungs- und Darstellungsformen werden sie überführt?


Die Trennung dieser Ebenen soll insbesondere verhindern, dass aus einer fehlenden oder marginalen Darstellung unmittelbar auf ein mangelndes Verständnis der Editionsdaten geschlossen wird.  Die Tabellen dienen aber nicht als quantitatives Bewertungsschema und sollen insbesondere keine Rangfolge der untersuchten Systeme erzeugen.

## 1. Gegenstand des Experiments

Als Fallbeispiel dient die [digitale Edition der Tagebücher von Andreas Okopenko](https://edition.onb.ac.at/okopenko/context:okopenko/methods/sdef:Context/get). Die Edition eignet sich für das Experiment insbesondere deshalb, weil neben den eigentlichen TEI-kodierten Editionsdaten auch das zugrunde liegende Schema, Editionsrichtlinien, extrahierte Registerdaten und ergänzende Materialien zugänglich sind. Zusätzlich werden sind die im Projekt verwendeten Faksimiles – die Teil der Edition sind – via IIIF zur Verfügung gestellt und lassen sich für den hier beschriebenen Zweck nachnutzen.

Die Daten können über das öffentlich zugängliche GitLab-Repo bezogen werden: [https://labs.onb.ac.at/gitlab/digital-editions/okopenko-public](https://labs.onb.ac.at/gitlab/digital-editions/okopenko-public)

Damit liegt ein überschaubares, zugleich aber hinreichend komplexes Editionsmodell vor, das unterschiedliche editorische Dimensionen umfasst. Hierzu gehören insbesondere:

- Tagebuchtexte und deren interne Struktur,

- dokumentarische bzw. materielle Bezüge,

- Datierungen und chronologische Relationen,

- Personen, Orte, Werke und weitere Registerinformationen,

- editorische Annotationen und Eingriffe,

- Metadaten und Editionsrichtlinien,

- Faksimiles und deren Verknüpfung mit den Editionsdaten.


Für das Experiment wird der Commit mit der SHA `263354ee3d5875614e4074a9514d43b67ad839b1` verwendet. Um die Rahmenbedingungen zur vereinfachen, werden aus für das Experiment verwendete Repo die XML-Datensätzen entfernt, die sich auf die sog. Publikationen beziehen. Zudem wird der Verweis auf die eigentliche digitale Edition entfernt. Die Coding-Agenten sollen ihre Benutzeroberflächen ausschließlich aus den bereitgestellten Daten, dem Schema und der Dokumentation entwickeln.

## 2. Untersuchungsgegenstand und Systeme

Untersucht werden mehrere aktuelle Coding-Agenten bzw. agentische Programmierumgebungen. Vorgesehen sind:

- OpenAI Codex bzw. ChatGPT Codex,

- Claude Code,

- OpenCode in Verbindung mit einem sog. Open Weight Modell.


Für alle Systeme sollen möglichst vergleichbare Ausgangsbedingungen hergestellt werden. Dazu gehören:

- identische Ausgangsdaten,

- identische Aufgabenstellung,

- identische bzw. funktional vergleichbare Zugriffsrechte,

- dokumentierte Modell- und Versionsangaben,

- dokumentierter Zeitpunkt der Durchführung,

- definierter Umgang mit Internetzugriff und externen Ressourcen,

- dokumentierter Umgang mit Rückfragen, Fehlern und notwendigen menschlichen Interventionen.


Nach Möglichkeit werden pro System mehrere unabhängige Durchläufe durchgeführt, um unterscheiden zu können, ob beobachtete Unterschiede eher zwischen den Modellen oder bereits zwischen einzelnen Runs desselben Modells auftreten. <!-- Noch unklar -->

## 3. Ablauf des Experiments

Das Experiment wird in mehreren aufeinanderfolgenden Schritten durchgeführt.

### 3.1 Vorbereitung

Vor Beginn der eigentlichen Runs werden:

1. die Erwartungen an das Experiment festgehalten,

2. die bereitgestellten Editionsdaten anhand von Tabelle 1 inventarisiert,

3. die technischen Versuchsbedingungen definiert,

4. die verwendeten Prompts festgelegt,

5. ein Pilotdurchlauf durchgeführt.


Der Pilotdurchlauf dient ausschließlich der Prüfung des Versuchsdesigns. Dabei soll insbesondere geklärt werden, ob der Umfang der Daten geeignet ist, die Agenten die relevanten Dateien auffinden und externe Ressourcen wie IIIF grundsätzlich verarbeitet werden können. Ergebnisse des Pilotdurchlaufs fließen nicht in die eigentliche vergleichende Auswertung ein.

### 3.2 Analysephase

In einem ersten Schritt erhält jeder Coding-Agent die Aufgabe, das bereitgestellte Repository zu untersuchen.

Dabei soll der Agent zunächst noch keine Benutzeroberfläche implementieren, sondern sein Verständnis der Edition dokumentieren. Er soll insbesondere beschreiben:

- welche Arten von Daten und Dokumenten vorliegen,

- welche editorischen Entitäten und Relationen er erkennt,

- welche Bestandteile er für zentral hält,

- welche möglichen Nutzungsszenarien er aus den Daten ableitet,

- welche Anforderungen sich daraus für eine Benutzeroberfläche ergeben.


Die Ergebnisse werden anhand von Tabelle 2 dokumentiert.

### 3.3 Implementierungsphase

Anschließend erhält der Agent die Aufgabe, auf Grundlage seiner Analyse eine funktionsfähige Weboberfläche für die Edition zu entwickeln.

Der Prompt soll möglichst wenige konkrete gestalterische Vorgaben enthalten. Insbesondere soll nicht festgelegt werden,

- welche Ansicht als primär gelten soll,

- wie Faksimile und Transkription zueinander anzuordnen sind,

- wie Registerinformationen darzustellen sind,

- welche Navigationselemente verwendet werden,

- welche Informationen prominent oder sekundär erscheinen.


Die Ergebnisse werden anhand von Tabelle 3 dokumentiert.

### 3.4 Dokumentation

Für jede Ausführung werden mindestens gesichert:

- verwendeter Prompt,

- vollständiges Agenten- bzw. Chatprotokoll, soweit verfügbar,

- Modell- und Versionsangabe,

- Datum und technische Umgebung,

- verwendeter Ausgangscommit,

- erzeugter Quellcode,

- finaler Commit der generierten Anwendung,

- notwendige menschliche Interventionen,

- Fehler und Abbrüche,

- Screenshots definierter Ansichten und Zustände.


---

# Tabelle 1: Inventar der bereitgestellten Editionsinformationen

Die erste Tabelle beschreibt nicht die Ergebnisse der Coding-Agenten, sondern die ihnen zur Verfügung stehende Ausgangsbasis. Die hier aufgenommenen Informationen bilden die Grundlage, um nachvollziehbar beurteilen zu können, welche Informationsbestandteile wie von den Modellen ausgewählt wurden.

| Bereich     | Information / Feature      | Vorkommen in den Daten | Repräsentation / Quelle | Zentrale Relationen           | Anmerkungen |
| ----------- | -------------------------- | ---------------------: | ----------------------- | ----------------------------- | ----------- |
| Text        | Tagebucheintrag            |                        |                         |                               |             |
| Text        | Absätze / interne Struktur |                        |                         |                               |             |
| Dokument    | Seitenstruktur             |                        |                         |                               |             |
| Dokument    | Faksimile                  |                        | IIIF                    | Faksimile ↔ Transkription     |             |
| Chronologie | Datierung                  |                        |                         | Datum ↔ Tagebucheintrag       |             |
| Chronologie | Reihenfolge der Einträge   |                        |                         | vorheriger ↔ nächster Eintrag |             |
| Register    | Personen                   |                        | Register / TEI          | Erwähnung ↔ Person            |             |
| Register    | Orte                       |                        | Register / TEI          | Erwähnung ↔ Ort               |             |
| Register    | Werke                      |                        | Register / TEI          | Erwähnung ↔ Werk              |             |
| Register    | Institutionen              |                        | Register / TEI          |                               |             |
| Editorik    | Streichungen               |                        | TEI                     |                               |             |
| Editorik    | Ergänzungen                |                        | TEI                     |                               |             |
| Editorik    | Korrekturen                |                        | TEI                     |                               |             |
| Editorik    | unsichere Lesungen         |                        | TEI                     |                               |             |
| Editorik    | editorische Anmerkungen    |                        | TEI                     | Annotation ↔ Textstelle       |             |
| Metadaten   | Dokumentbeschreibung       |                        | TEI                     |                               |             |
| Metadaten   | Editionsrichtlinien        |                        | Dokumentation           |                               |             |
| Metadaten   | Verantwortlichkeiten       |                        |                         |                               |             |
| Metadaten   | Zitierinformationen        |                        |                         |                               |             |
| Datenmodell | ODD / Schema               |                        |                         |                               |             |
| weitere     |                            |                        |                         |                               |             |

---

# Tabelle 2: Modellrekonstruktion und Arbeitsprozess des Agenten

Die zweite Tabelle dokumentiert, wie der jeweilige Coding-Agent die bereitgestellte Edition analysiert und welche expliziten Annahmen bzw. Entscheidungen er vor und während der Implementierung formuliert. So soll unterschieden werden zwischen Informationen, die ein Agent nicht erkannt hat, und Informationen, die er zwar erkannt, in der späteren Oberfläche jedoch nicht oder nur nachrangig genutzt bzw. umgesetzt hat.

| Kategorie               | Leitfrage                                                      | Beobachtung | Evidenz / Protokollstelle |
| ----------------------- | -------------------------------------------------------------- | ----------- | ------------------------- |
| Repositoryanalyse       | Welche Dateien und Verzeichnisse untersucht der Agent?         |             |                           |
| Dokumentation           | Werden README und Editionsrichtlinien berücksichtigt?          |             |                           |
| Datenmodell             | Wird ODD bzw. Schema untersucht?                               |             |                           |
| TEI                     | Werden repräsentative TEI-Dateien analysiert?                  |             |                           |
| Faksimiles              | Wird die IIIF-Struktur erkannt?                                |             |                           |
| Register                | Werden Register und ihre Relationen erkannt?                   |             |                           |
| Grundmodell             | Wie beschreibt der Agent die Edition insgesamt?                |             |                           |
| Text                    | Was identifiziert der Agent als primäres Textobjekt?           |             |                           |
| Dokument                | Welche Bedeutung weist er Dokument und Materialität zu?        |             |                           |
| Chronologie             | Welche Bedeutung weist er der zeitlichen Struktur zu?          |             |                           |
| Entitäten               | Welche Bedeutung weist er Personen, Orten, Werken etc. zu?     |             |                           |
| Editorische Phänomene   | Welche textkritischen / editorischen Strukturen erkennt er?    |             |                           |
| Nutzungsszenarien       | Welche Formen der Nutzung nimmt der Agent an?                  |             |                           |
| Nutzer:innen            | Welche Nutzergruppen werden explizit oder implizit adressiert? |             |                           |
| Informationsarchitektur | Welche Hauptbereiche plant der Agent?                          |             |                           |
| Priorisierung           | Welche Informationen bezeichnet er als besonders wichtig?      |             |                           |
| UI-Muster               | Welche Interfaceformen plant er vor der Implementierung?       |             |                           |
| Alternativen            | Werden alternative Gestaltungsformen erwogen?                  |             |                           |
| Auslassungen            | Welche vorhandenen Bereiche werden nicht erwähnt?              |             |                           |
| Abweichungen            | Was wird erkannt, später aber nicht umgesetzt?                 |             |                           |
| Interventionen          | Wo war menschliches Eingreifen notwendig?                      |             |                           |
|                         |                                                                |             |                           |

---

# Tabelle 3: Interfacevergleich und epistemische Ordnung

Die dritte Tabelle bildet den Kern der Auswertung. Für zentrale Bestandteile der Edition wird untersucht, was die generierte Anwendung mit der jeweils vorhandenen editorischen Information macht.

Vier Operationen stehen dabei im Mittelpunkt:

- **Selektion:** Wird eine vorhandene Information im Interface berücksichtigt?

- **Hierarchisierung:** Welche relative Sichtbarkeit bzw. Bedeutung erhält sie?

- **Relationierung:** Wie wird diese mit anderen Elementen verbunden?

- **Transformation:** In welche konkrete Interface- und Interaktionsform wird sie übersetzt?


Die Auswertung dieser vier Ebenen erfolgt wiefolgt:
- Selektion: 0 / 1
- Hierachisierung: deskriptive Skala
	- **0:** nicht vorhanden
	- **1:** nur indirekt bzw. verborgen erreichbar
	- **2:** regulär zugänglich
	- **3:** prominent
	- **4:** strukturprägend für die Gesamtanwendung
- Relationierung: Auflistung der verbundenen Bestandteile; Markierung von Unsicherheit durch `?`
- Transformation (Darstellung): Auflistung der UI-Elemente

| Gegenstand              | Selektion | Hierarchisierung (0–4) | Relationierung                      | Transformation / UI-Form                | Belegstelle |
| ----------------------- | --------- | ---------------------: | ----------------------------------- | --------------------------------------- | ------- |
| Tagebuchtext            |           |                        |                                     | Reader / andere Form                    |         |
| Faksimile               |           |                        | Text ↔ Faksimile?                   | Viewer / Thumbnail / Split View / …     |         |
| Seitenstruktur          |           |                        |                                     |                                         |         |
| Datierung               |           |                        | Datum ↔ Einträge?                   | Textkopf / Kalender / Timeline / …      |         |
| Chronologie             |           |                        |                                     | Navigation / Kalender / Timeline / …    |         |
| Personen                |           |                        | Text ↔ Register ↔ weitere Einträge? | Link / Tooltip / Card / Detailseite / … |         |
| Orte                    |           |                        |                                     | Link / Karte / Register / …             |         |
| Werke                   |           |                        |                                     |                                         |         |
| weitere Entitäten       |           |                        |                                     |                                         |         |
| Streichungen            |           |                        |                                     | Inline / Tooltip / ausgeblendet / …     |         |
| Ergänzungen             |           |                        |                                     |                                         |         |
| Korrekturen             |           |                        |                                     |                                         |         |
| Unsicherheiten          |           |                        |                                     |                                         |         |
| editorische Anmerkungen |           |                        |                                     | Fußnote / Sidebar / Tooltip / …         |         |
| Dokumentmetadaten       |           |                        |                                     |                                         |         |
| Editionsrichtlinien     |           |                        |                                     |                                         |         |
| Verantwortlichkeiten    |           |                        |                                     |                                         |         |
| Zitierinformationen     |           |                        |                                     |                                         |         |
| globale Suche           |           |                        | Suchergebnis ↔ Edition?             | Suchfeld / Command Palette / …          |         |
| Filter                  |           |                        |                                     |                                         |         |
| Registerzugang          |           |                        |                                     |                                         |         |
| Datenzugriff / Download |           |                        |                                     |                                         |         |

---------
## Analyse

### 4.1 Interpretation

Die Einzelbeobachtungen werden abschließend – je Coding-Agent – in eine Gesamtauswertung überführt. Dabei wird zur Orientierung auf den nachfolgenden Fragenkatalog zurückgegriffen:

- Startansicht -> Was sieht eine Nutzer:in zuerst?
- Primäres Objekt -> Was erscheint als Zentrum der Edition?
- Ordnungsprinzip -> Text, Dokument, Chronologie, Entitäten, Suche etc.?
- Navigation -> Welche Zugänge strukturieren die Anwendung?
- Interaktion -> Lesen, Suchen, Browsen, Vergleichen, Erkunden?
- Faksimiles -> Zentral, gleichrangig, ergänzend, marginal?
- Register -> Kontextinformation oder eigenständiger Zugang?
- Suche -> Hilfsmittel oder primärer Zugang?
- Editorische Komplexität -> Sichtbar, gestaffelt, reduziert oder ausgeblendet?
- Materialität -> Welche Bedeutung erhält das Dokument als materielles Objekt?
- Textbegriff -> Welcher Textbegriff wird durch die Oberfläche nahegelegt?
- Nutzer:innenrolle -> Welche Form von Nutzer:innen wird implizit adressiert?
- Interface-Gestaltung -> Archiv, Forschungsportal, Reader etc.?
- Editorische-Transparenz -> Wie sichtbar bleiben editorische Eingriffe und Verantwortlichkeiten?

Ziel ist nicht, aus einem einzelnen Interface unmittelbar auf ein festes „Editionsverständnis“ eines Sprachmodells zu schließen. Untersucht wird vielmehr, welche editorische Ordnung sich in einem konkreten, unter dokumentierten Bedingungen erzeugten Interface manifestiert und ob sich über mehrere Systeme hinweg wiederkehrende Muster feststellen lassen.

### 4.2 Verhältnis zu den formulierten Erwartungen

Die formulierten Erwartungen werden nicht als starre Bewertungskriterien in die Tabellen eingeschrieben. Stattdessen werden zunächst möglichst deskriptive Beobachtungen erhoben. Erst im Anschluss wird geprüft, inwiefern sich beispielsweise folgende Erwartungen bestätigen, differenzieren oder widerlegen lassen.