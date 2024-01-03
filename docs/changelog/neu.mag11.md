# Was ist neu?

[1]:/assets/images/neues/11.001.png "Prüfungslistenfilter"
[2]:/assets/images/neues/11.002.png "Suche ergänzt um Geburtsdatum"
[3]:/assets/images/neues/11.003.png "Endnote des vorangegangenen Halbjahres"
[4]:/assets/images/neues/11.004.png "Ausleiherlaubnis verlängern"
[5]:/assets/images/neues/11.005.png "Kontaktverhältnis"
[6]:/assets/images/neues/11.006.png "Elternsprecher, Schülersprecher"
[7]:/assets/images/neues/11.007.png "Neue Spalten in der Schülerauswahlliste"
[8]:/assets/images/neues/11.008.png "Signatur wird unter Bücher/Medien > Vorgänge gezeigt"
[9]:/assets/images/neues/11.009.png "Vorhalbjahresnote"
[10]:/assets/images/neues/11.010.png "Sortierung Schulen"


**Dieser Teil ist aktuell in Vorbereitung. <br/>MAGELLAN 11 erscheint voraussichtlich im 1. Quartal 2024**

Die nachfolgenden Abschnitte richten sich an die Nutzer von MAGELLAN 10. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen in MAGELLAN 11 geben.

## Crystal Reports

Um für Berichte die Inhalte der Tabelle Wortersetzungen verwenden zu können (beispielsweise um selbstgewählte Verhältnisse zwischen Schülern und Sorgeberechtigten), wurde die Datenstruktur um ein View Wortersetzungen erweitert. Für eigene Berichte können Sie unseren angepassten Bericht "Sorgeberechtigte mit Kindern.rpt" als Vorlage verwenden.

## MAGELLAN Administrator

### schueler_import.csv

Der Import für Schüler- oder Bewerberdaten wurde um folgende Felder ergänzt:

Importfeld|MAGELLAN-Feld
:--|:--
 `Fremdsprache1Referenz`|`Schüler/Bewerber/Vagabunden > Daten3 > Fremdsprachenfolge > FS.1 > Referenz`
 `Fremdsprache2Referenz`|`Schüler/Bewerber/Vagabunden > Daten3 > Fremdsprachenfolge > FS.2 > Referenz`
 `Fremdsprache3Referenz`|`Schüler/Bewerber/Vagabunden > Daten3 > Fremdsprachenfolge > FS.3 > Referenz`
 `Fremdsprache4Referenz`|`Schüler/Bewerber/Vagabunden > Daten3 > Fremdsprachenfolge > FS.4 > Referenz`
 `VoraussichtlichesEnde`|`Schüler/Bewerber/Vagabunden > Daten2 > Abgang > voraus. Ende`

## MAGELLAN Schulverwaltung

### Menü Schüler

* Beim Einschulen einer Schülerkopie wird die Herkunftsschule aktualisiert.
* Die Suche wurde ergänzt um den Suchparameter Geburtsdatum.

![Suche ergänzt um das Geburtsdatum](/assets/images/neues/11.002.png)

* Auf der Karte `Schüler > Zeugnis > Leistungen` gibt es die neue Spalte `Vorhalbjahresnote`, die für ausgewählte Schüler per Assistent aus dem Vorhalbjahr gefüllt werden kann. Den Aufruf für den Assistenten finden Sie im Menübandunterpunkt `Schüler > Endnote Vorzeitraum zuweisen`. Der Assistent kopiert die Note des vorangegangenen Halbjahres und zeigt sie nicht editierbar im neuen Feld an. Dieses Feld kann auch in die MyMAGELLAN-Dateien mit zur Information ausgegeben werden.

![Endnote des vorangegangenen Halbjahres](/assets/images/neues/11.003.png)

* Unter `Schüler > Daten 2` wurde beim Zuweisen der Herkunftschule die Liste der Schulen ergänzt um den Status und die Anzeige nach Status, Favorit und alphabetisch geordnet.

![Sortierung der Schulen unter "Daten2 > Herkunftsschulen"](/assets/images/neues/11.010.png)

* Die Sammelzuweisungen unter `Schüler > Schüler > Sammelzuweisung` wurden für die Filterung der Schüler um die Anzeige der Felder `Geburtsort` und `Geburtsland` erweitert.
* Neues Feld `Rufname` unter `Schüler > Daten1` und in der Auswahlliste für Schüler und Vagabunden.

### Menü Bewerber

* Die Sammelzuweisungen unter `Schüler > Schüler > Sammelzuweisung` wurden für die Filterung der Bewerberdatensätze um die Anzeige der Felder `Geburtsort` und `Geburtsland` erweitert.
* Neues Feld `Rufname` unter `Bewerber > Daten1` und in der Auswahlliste.

### Menü Klassen

* Unter `Klassen > Zeiträume` gibt es zwei neue Felder für den `3.Schülersprecher` und den `3.Elternsprecher`.

![neue Felder für Elternsprecher und Schülersprecher](/assets/images/neues/11.006.png)

### Menü Sorgeberechtigte

* Da die Bezeichnung "Sorgeberechtigte" nicht alles umfasste, was in diesem Menü an Daten verwaltbar ist, wurde die neue Bezeichnung "Kontakte" gewählt. Die Unterkarte "Kinder" wurde in "Schüler" umbenannt.
* Auf der Unterkarte "Schüler" wird für jeden Eintrag auch das Verhältnis eingeblendet. Sollte ein Kontakt für Schüler Ihrer Schule als "Vater" und als "Ansprechpartner des Jugendamts" hinterlegt sein, wird die Rolle dem Schüler gegenüber aus dieser Ansicht transparent.

![Kontakt-Schüler-Verhältnis](/assets/images/neues/11.005.png)

### Menü Abitur

### Filterung nach Fachkategorie, Aufgabenbereich

In der Ansicht `Abitur > Qualifikation` kann die Liste der Schülerfächer nach dem Aufgabenbereich oder der Fachkategorie gefiltert werden. Die Aufgabenbereiche und Fachkategorien ergeben sich aus der Zuordnung der Werte unter `Extras > Schlüsselverzeichnisse > Fächer`. 

### Prüfungslisten drucken

Der Vorfilter für die Befüllung der Prüfungslisten wurde erweitert um das Feld Lehrer, zusätzlich ist es auch möglich statt eines gezielt gewählten Faches ein `*` als Platzhalter für alle Fächer zu verwenden.

![Prüfungslistenfilter](/assets/images/neues/11.001.png)

### Prüfungsnoten erfassen erweitert

Im Menü `Abitur` wurde die Liste zur Eingabe der Prüfungsnoten (Fächer, die auf die Karte Prüfungen übertragen wurde) erweitert. Sie können die gewohnte Ansicht nutzen oder das Häkchen vor `Alle Prüfungsfächer` aktivieren. Die Anzeige lädt im Anschluss alle Prüfungsfachzeilen der Prüflinge eines Abiturjahrgangs in eine filterbare und nach Excel exportierbare Liste.

### Aufrufe verschoben

Die Aufrufe für die Aktionen `Prüfungsliste` und `Sammelzuweisung` wurde ins Menüband verschoben.

## MAGELLAN Bibliothek

* Neue Sammelzuweisung um Medienausleihern eine verlängerte Ausleihdauer gesammelt zuweisen zu können.

![Ausleiherlaubnis verlängern](/assets/images/neues/11.004.png)

* Neue Felder in der Auswahlliste `Schüler`:  ID, Geburtsdatum, Volljährig.

![Neue Spalten in der Schülerauswahlliste](/assets/images/neues/11.007.png)

* Unter `Bücher/Medien > Vorgänge` wird in der Liste die Signatur des Exemplares gezeigt.

![Signatur wird unter Bücher/Medien > Vorgänge gezeigt](/assets/images/neues/11.008.png)

* Die Reihenfolge des angezeigten Schülernamens in mehreren Aktionen im Menü `Ausleihe` wurde im kombinierten Namensfeld von `Vorname Nachname` auf `Nachname, Vorname` geändert.

![Anzeige des Ausleihernamens geändert](/assets/images/neues/11.011.png)

* Unter `Vorgänge > Aktuell/Historie` wird die Signaturnummer der Exemplare für eine bessere Sortierbarkeit eingeblendet.

![Anzeige der Signaturnummer](/assets/images/neues/11.012.png)

## MyMAGELLAN

* Das neue Feld `Vorhalbjahresnote` kann im MyMAGELLAN Center mit in die MyMAGELLAN-Dateien übergeben werden. In MyMAGELLAN kann die Spalte in den Ansichten `Schüler` und `Fächer` sichtbar (zur Information, nicht editierbar) gezeigt werden.

![Vorhalbjahresnote](/assets/images/neues/11.009.png)
