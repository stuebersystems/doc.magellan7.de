# Was ist neu?

[1]:/assets/images/neues/10.001.png "Abitur: Fachkategorie, Aufgabenbereich"
[2]:/assets/images/neues/10.002.png "Kurs und Lehrer"
[3]:/assets/images/neues/10.003.png "Bestanden, Leistungsart"
[4]:/assets/images/neues/10.004.png "Aktionsaufrufe in der Gruppe Fächer"
[5]:/assets/images/neues/10.005.png "Fach löschen nach Kursnummer"
[6]:/assets/images/neues/10.006.png "Lehrerserien-E-Mail"
[7]:/assets/images/neues/10.007.png "Endnote fortschreiben"
[8]:/assets/images/neues/10.008.png "Personen-Serien-E-Mail"
[9]:/assets/images/neues/10.009.png "Sorgeberechtigten-Serien-E-Mail"
[10]:/assets/images/neues/10.010.png "Beurteilungsart"

**Dieser Teil ist aktuell in Vorbereitung. <br/>MAGELLAN 11 erscheint voraussichtlich im 1. Quartal 2024**

Die nachfolgenden Abschnitte richten sich an die Nutzer von MAGELLAN 10. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen in MAGELLAN 11 geben.

## Crystal Reports

Um für Berichte die Inhalte der Tabelle Wortersetzungen verwenden zu können (beispielsweise um selbstgewählte Verhältnisse zwischen Schülern und Sorgeberechtigten), wurde die Datenstruktur um ein View Wortersetzungen erweitert. Für eigene Berichte können Sie unseen angepassten Bericht "Sorgeberechtigte mit Kindern.rpt" als Vorlage verwenden.

## MAGELLAN Administrator

### schueler_import.csv 

Der Import für Schüler- oder Bewerberdaten wurde um folgende Felder ergänzt:

* `Fremdsprache1Referenz`
* `Fremdsprache2Referenz`
* `Fremdsprache3Referenz`
* `Fremdsprache4Referenz`
* `voraussichtliches Ende`

## MAGELLAN Schulverwaltung

### Sammelzuweisung

Die Sammelzuweisungen in den Menüs `Bewerber > Bewerber > Sammelzuweisung` und `Schüler > Schüler > Sammelzuweisung` wurden für die Filterung der Schüler- oder Bewerberdatensätze um die Anzeige der Felder `Geburtsort` und `Geburtsland` erweitert.

### Allgemein

### Menü Schüler

* Beim Einschulen einer Schülerkopie wird die Herkunftsschule aktualisiert
* Die Suche wurde ergänzt um den Suchparameter Geburtsdatum
* Auf der Karte `Schüler > Zeugnis > Leistungen` gibt es die neue Spalte `Vorhalbjahresnote`, die für ausgewählte Schüler per Assistent aus dem Vorhalbjahr gefüllt werden kann. Den Aufruf für den Assistenten finden Sie im Menübandunterpunkt `Schüler > Endnote Vorezitraum zuweisen`. Diese Note dient der 
* Unter `Schüler > Daten 2` wurde beim Zuweisen der Herkunftschule die Liste der Schulen ergänzt um den Status und die Anzeige nach Status, Favorit und alphabetisch geordnet.
* Die Sammelzuweisungen unter `Schüler > Schüler > Sammelzuweisung` wurden für die Filterung der Schüler um die Anzeige der Felder `Geburtsort` und `Geburtsland` erweitert.

### Menü Bewerber

* Die Sammelzuweisungen unter `Schüler > Schüler > Sammelzuweisung` wurden für die Filterung der Bewerberdatensätze um die Anzeige der Felder `Geburtsort` und `Geburtsland` erweitert.

### Menü Klassen

* Unter `Klassen > Zeiträume` gibt es zwei neue Felder für den `3.Schülersprecher` und den `3.Elternsprecher`


### Menü Sorgeberechtigte

* Da die Bezeichnung "Sorgeberechtigte" nicht alles umfasste, was in diesem Menü an Daten verwaltbar ist, wurde die neue Bezeichnung "Kontakte" gewählt. Die Unterkarte "Kinder" wurde in "Schüler" umbenannt.
* Auf der Unterkarte "Schüler" wird für jeden Eintrag auch das Verhältnis eingeblendet. Sollte ein Kontakt für Schüler Ihrer Schule als "Vater" und als "Ansprechpartner des Jugendamts" hinterlegt sein, wird die Rolle dem Schüler gegenüber aus dieser Ansicht transparent.

### Menü Abitur

### Prüfungslisten drucken

Der Vorfilter für die Befüllung der Prüfungslisten wurde erweitert um das Feld Lehrer, zusätzlich ist es auch möglich statt eines gezielt gewählten Faches ein `*` als Platzhalter für alle Fächer zu verwenden.

### Prüfungsnoten erfassen erweitert

Im Menü `Abitur` wurde die Liste zur Eingabe der Prüfungsnoten erweitert. Sie können die gewohnte Ansicht nutzen oder das Häkchen vor `Alle Prüfungsfächer` aktivieren. Die Anzeige lädt im Anschluss alle Prüfungsfachzeilen der Prüflinge in eine filterbare und nach Excel exportierbare Liste.

### Aufrufe verschoben

Die Aufrufe für die Aktionen `Prüfungsliste` und `Sammelzuweisung` wurde ins Menüband verschoben.

## MAGELLAN Bibliothek

* Neue Sammelzuweisung um Medienausleihern eine verlängerte Ausleihdauer gesammelt zuweisen zu können
* Neue Felder in der Auswahlliste `Schüler`:  ID, Geburtsdatum, Volljährig
* Unter `Bücher/Medien > Vorgänge` wird in der Liste die Signatur des Exemplares gezeigt

## MyMAGELLAN

* das neue Feld `Vorhalbjahresnote` kann im MyMAGELLAN Center mit in MyMAGELLAN-Dateien übergeben werden und in MyMAGELLAN für den Eingebenden sichtbar sein.