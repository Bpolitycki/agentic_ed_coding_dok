# Prompts

## Prompt 1 – Analyse des Editionsrepositories

Analysiere die unter `/data` bereitgestellten Editionsdaten und Dokumentationen. Versuche, ein möglichst präzises Verständnis des zugrunde liegenden Editionsmodells zu entwickeln.

Implementiere in diesem Schritt noch keine Benutzeroberfläche und verändere keine Editionsdaten oder sonstigen bestehenden Dateien.

Untersuche insbesondere:

- welche Arten von Daten und Dokumenten im Repository vorhanden sind,
- wie die Editionsdaten strukturiert sind,
- welche zentralen Entitäten und Relationen modelliert werden,
- welche Rolle Text, Dokument, Faksimile, Chronologie, Registerdaten und editorische Annotationen spielen,
- welche Informationen aus Schema, Editionsrichtlinien und weiteren ergänzenden Texten hervorgehen,
- welche Aspekte oder Relationen explizit modelliert und welche nur aus der Struktur der Daten ableitbar sind,
- welche Nutzungsszenarien sich aus den vorhandenen Daten und Strukturen ableiten lassen,
- welche Anforderungen und Nutzungsmöglichkeiten sich daraus grundsätzlich ergeben.

Dokumentiere deine Analyse anschließend strukturiert und knapp. Benenne dabei auch Unsicherheiten oder Aspekte, deren Funktion sich aus dem Repository nicht eindeutig erschließen lässt. Halte die zentralen Ergebnisse zusätzlich in `analysis.md` fest, damit sie in späteren Arbeitsschritten als Referenz genutzt werden können.

Treffe in dieser Phase noch keine endgültigen Gestaltungsentscheidungen.

Lege nach Abschluss dieser Phase einen Git-Commit mit einer aussagekräftigen Commit-Message an. Verändere keine anderen Branches.

## Prompt 2 – Entwicklung der digitalen Edition

Entwickle auf Grundlage deiner vorangegangenen Analyse (vgl. `analysis.md`) des Repositories eine funktionsfähige webbasierte Benutzeroberfläche für eine digitale Edition. Die Webanwendung soll als Präsentationsschicht die bereitgestellten Daten sinnvoll zugänglich und nutzbar machen.

Entscheide selbstständig über:

- Informationsarchitektur,
- Navigation,
- Ansichten,
- Darstellungsformen,
- Interaktionsmöglichkeiten,
- Gewichtung und Anordnung der vorhandenen Informationen,
- technische Umsetzung.

Berücksichtige dabei sowohl die Gesamtstruktur der Edition als auch die in den Daten vorhandenen editorischen Details.

Es gibt keine vorgegebene Referenzoberfläche. Entwickle auf Grundlage der bereitgestellten Daten, des Schemas und der Dokumentation eine eigenständige Lösung.

Nutze die unter `/data` bereitgestellten Materialien als Grundlage für deine editorischen und gestalterischen Entscheidungen.

Arbeite selbstständig und implementiere eine funktionsfähige Anwendung. Lege nach Abschluss dieser Phase einen Git-Commit mit einer aussagekräftigen Commit-Message an. Verändere keine anderen Branches.

## Prompt 3 Überprüfung und Überarbeitung

Überprüfe die von dir entwickelte Anwendung erneut auf Grundlage der bereitgestellten Editionsdaten, des Schemas, der Dokumentation und deiner vorangegangenen Analyse.

Überarbeite die Anwendung dort, wo du auf Grundlage dieser Prüfung Verbesserungsbedarf erkennst.

Dokumentiere anschließend knapp, welche Änderungen du vorgenommen hast.

Lege nach Abschluss dieser Phase einen Git-Commit mit einer aussagekräftigen Commit-Message an. Verändere keine anderen Branches.