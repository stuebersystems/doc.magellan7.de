# Datenaustausch

![Das Fenster `Datenaustausch`](/assets/images/magellan.administrator/datenaustausch.png)

## Kataloge (Schlüsselverzeichnisse) importieren

Mit dieser Option können Sie die Schlüsselverzeichnisse Ihrer Region in die MAGELLAN-Datenbank importieren. Sie können diesen Import jederzeit wiederholen, um beispielsweise bestehende Schlüsselverzeichnisse auf den neuesten Stand zu bringen.

Für MAGELLAN existieren Anpassungen an die Bestimmungen einzelner Bundesländer bzw. bestimmter Schularten. Diese Anpassungen richten sich u. a. danach, ob die jeweiligen Stellen der Statistikämter, Kultusministerien bzw. Schulträger entsprechende Datentransferformate usw. anbieten. Durch die Landesanpassung werden die Bereiche Statistik und Oberstufenverwaltung, als auch die Zeugnisse abgedeckt. Um eine MAGELLAN-Datenbank mit neuen Schlüsselverzeichnissen zu aktualisieren bzw. Schlüssel in eine leere MAGELLAN-Datenbank zu importieren, müssen Sie die Option „Schlüsselverzeichnisse importieren“ wählen.

Feld                                     | Bedeutung
---------------------------------------- | ---------
Importiere für folgendes Land/Bundesland | Wählen Sie Ihr Bundesland oder Land aus.<br/>Der Assistent bietet Schlüsselverzeichniskataloge aus dem gleichnamigen Verzeichnis im Verzeichnis Importe (standardmäßig auf Ihrem MAGELLAN-Serverrechern). Ein Spezieller Wert stellt `Benutzer` dar. Dieser wird im weiteren Verlauf näher beschrieben.
Importiere folgende Schlüssel            | Es gibt die Auswahl Schlüssel für allgemeinbildende Schulen oder berufsbildende Schulen.<br/>Katalogedateien können mit 00_, AS_ oder BS_ beginnen. Für allgemeinbildende Schulen werden Dateien mit 00_ und AS_ importiert, für berufsbildende Schulen werden Dateien mit 00_ und BS_ importiert.
Importiere für den folgenden Mandanten   | Wählen Sie den Zielmandanten aus
Importiere folgenden Katalog             | Sie können eine einzelne Datei oder alle zutreffenden Datei einlesen lassen.

![Assistent zum Importieren von Katalogen](/assets/images/magellan.administrator/kataloge.importieren.png)

### Eigene Kataloge importieren (`Benutzer`)

Damit Sie eigene oder bearbeitete Katalogdateien (*.keys) importieren können, haben Sie die Möglichkeit ein gesondertes Unterverzeichnis `Benutzer` anzulegen. Auf dem Serverrechner unter `C:\Users\Public\Documents\Stueber Systems\Magellan 7\Importe` (Dokumentenpfad gegebenenfalls abweichend) erstellen Sie das Unterverzeichnnis `Benutzer` und legen dort Ihre Katalogdateien ab. Im Assistenten wählen Sie dann den Eintrag `Benutzer` für `Importiere für folgendes Land/Region`. Das Unterverzeichnis `Benutzer`wird bei Updates nicht verändert. Wenn Sie den Wert im Assistenten auswählen und Sie zuvor den Unterpfad nicht angelegt haben, erhalten Sie eine entsprechende Fehlermeldung.

[Kataloge aus dem Verzeichnis `Benutzer`importieren](/assets/images/magellan.administrator/kataloge.importieren1.png)

![Wählen Sie Bundesland, Art der Schlüssel und den Mandanten](/assets/images/Import_Export.Schluesselimport.png)

### Benennung der Kataloge

Beispiele:

* 00_Faecher.keys
* AS_Faecher.keys
* BS_Faecher.keys

Benennung                                     | Anmerkung
--------------------------------------------- | ---------
Dateinamenanfang "AS_"                        | Schlüsseldateien die mit "AS_" bezeichnet sind, werden beim Aufruf `für allgemeinbildende Schulen` zum Import angeboten
Dateinamenanfang "BS_"                        | Schlüsseldateien die mit "BS_" bezeichnet sind, werden beim Aufruf `für berufsbildende Schulen` zum Import angeboten
Dateinamenanfang "00_"                        | Schlüsseldateien die mit "00_" bezeichnet sind, werden beim Aufruf `für allgemeinbildende Schulen` und beim Aufruf `für berufsbildende Schulen` zum Import angeboten
Text ab Zeichen 4<br/>(im Beispiel "Faecher") | Anhand dieser Bezeichnung wird das Schlüsselverzeichnis identifiziert. Eine vollständige Aufzählung der Schlüsselverzeichnisse, inklusive der Beschreibung für den Aufbau der Katalogdateien finden Sie im Abschnitt [Referenz > keys-Dateien](https://doc.magellan.stueber.de/schulverwaltung/reference/keys-dateien).

### Importiere folgenden Katalog

Es können entweder alle keys-Dateien (AS_xxx und 00_xxx oder BS_xxx und 00_xxx ) importiert werden oder Sie wählen eine bestimmte Datei aus.

### Aufbau der Dateien

!!! info "Hinweis"

    Den Aufbau der einzelnen Importdatei beschreiben wir im Abschnitt [Referenz > keys-Dateien](https://doc.magellan.stueber.de/schulverwaltung/reference/keys-dateien).

Jede dieser Dateien muss als CSV-Datei aufgebaut sein, d.h. sie besteht jeweils aus einer Kopfzeile und
ein oder mehreren Zeilen mit den zu importierenden Inhalten. Die einzelnen Felder sind durch
Semikolon getrennt und mit Anführungszeichen abgegrenzt.

Die Importdatei für Fachstatus (00_Fachstati.keys) kann z.B. folgenden Aufbau haben

```csv
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
"1PF";"1PF";"1. Prüfungsfach";"01.08.2006";""
"2PF";"2PF";"2. Prüfungsfach";"01.08.2006";""
"3PF";"3PF";"3. Prüfungsfach";"01.08.2006";""
"1PFBLL";"1PFBLL";"1. Prüfungsfach und Besondere Lernleistung";"01.08.2006";""
```

Die Felder entsprechen dem sogenannten System Data Format (SDF), d.h. bei einem Semikolon, Komma, Sonderzeichen oder einem Leerzeichen im String wird der String in Anführungszeichen gesetzt, z.B. die Bezeichnung "1. Prüfungsfach und Besondere Lernleistung " wird ;“ 1. Prüfungsfach und Besondere Lernleistung“;... und nicht ; 1. Prüfungsfach und Besondere Lernleistung;... geschrieben.
Besitzt der Inhalt selbst Anführungszeichen, so sind doppelte Anführungszeichen anzugeben. Welche Felder pro Datei eingelesen werden, ist den nachfolgenden Abschnitten pro Datei zu entnehmen.

!!! info "Hinweis"

    Zeilenumbrüche sind in einer CSV-Datei nicht erlaubt. Das Datenformat bestimmt jede Zeile als einen Datensatz. Ein Umbruch mitten in der Zeile kann nicht verarbeitet werden.
    Ändern Sie bitte vor dem Import die Dateiendung in *.keys.

### Was passiert beim Schlüssel importieren

Beim Einlesen von Schlüsselverzeichnissen wird folgendes der Reihe nach durchgeführt:

1. Alle noch nie verwendeten Schlüssel werden in den Zielverzeichnissen der Datenbank gelöscht.

2. Alle übrigen Schlüssel werden in der Datenbank mit einem älteren Datum versehen und damit als ungültig (graue Raute) markiert.

3. Nun wird geprüft welche Schlüssel eingelesen werden sollen, entscheidend ist dabei lediglich der Wert in der Spalte Schlüssel:

* Wird ein Schlüssel erkannt, wird nur das Gültig-Bis-Datum entfernt (Schlüssel ist wieder aktiv). Das gilt auch, wenn der Schlüsselwert mehrfach im Verzeichnis existiert.
* Wird ein Schlüssel nicht im Verzeichnis erkannt, wird er eingelesen und aktiv gesetzt.
Als Ergebnis haben Sie damit nur die korrekten Schlüssel als aktive Werte markiert. Verkehrte, aber bereits verwendete Schlüssel, bleiben in der Datenbank bestehen, werden aber als inaktiv gekennzeichnet.

!!! info "Hinweis"

    Bei bestehenden Schlüsselzeilen in den Zielverzeichnissen wird weder Bezeichnung, noch Kürzel oder Schlüssel verändert, lediglich das Gültig-von- und das Gültig-bis-Datum wird angepasst.

Feld                  | Hinweis
--------------------- | -------
Kuerzel               | dieser Wert muss pro Zeile gefüllt werden, darf aber nur einmalig innerhalb eines Verzeichnisses verwendet werden.
Zeichenlänge pro Feld | Die Gesamtzeichenlänge darf nicht überschritten werden. Bitte beachten Sie hierzu das Dokument [MAGELLAN 7 - Datenstruktur](https://doc.magellan7-toolbox.stueber.de/datenstruktur/).

## Postleitzahlen und Banken importieren

Mit dieser Option können Sie Ihr bestehendes Postleitzahlverzeichnis gegen ein neues austauschen oder erstmalig in Ihre Datenbank importieren. Folgende Verzeichnisse werden eingelesen oder ersetzt:

* Bundesländer
* Bezirke
* Kreise
* Gemeinden
* Stadtbezirke
* Postleitzahlen

Feld                          | Anmerkung
----------------------------- | ---------
Importiere für folgendes Land | Aktuell bieten wir Kataloge für folgende Regionen an:<br/>* Deutschland<br/>* Schweiz<br/>* Rheinland-Pfalz <br/>* Berlin
Importiere folgenden Katalog  | Alle Kataloge

![Das Fenster `Importiere Postleitzahlen`](/assets/images/magellan.administrator/importiere.plz.png)

## Daten über das MAGELLAN-Importformat importieren

!!! warning "Wichtig"

    Die nachstehende Beschreibung setzt mindestens die MAGELLAN-Ausgabe 7.1.4 voraus.

Das MAGELLAN-Importformat ist die allgemeine Importschnittstelle für die Übernahme von Fremddaten in die MAGELLAN-Datenbank.

### Vorbereitung

Bereiten Sie Ihre einzulesenden Daten bitte entsprechend unserer Beschreibung im [MAGELLAN-Importformat](https://doc.magellan-toolbox.stueber.de/importe/) vor.

!!! tip "Tipp"

    Sie können den Dateinamen der *.csv-Dateien frei wählen, es ist aber sinnvoll die vorgeschlagenen Namen je Importdatei zu verwenden, der Assistent erkennt die Namen und sortiert diese automatisch in die inhaltlich aufeinander aufbauende Reihenfolge.

Empfohlener Dateiname|Beschreibung
--|--
schulen.import.csv | Enthält die Stammdaten der Schulen
betriebe.import.csv | Enthält die Stammdaten der Betriebe
lehrer.import.csv | Enthält die Stammdaten der Lehrer
schueler.import.csv | Enthält die Stammdaten der Schüler und Bewerber
sorgebe.import.csv | Enthält die Stammdaten der Sorgeberechtigten
verlage.import.csv | Enthält die Stammdaten der Verlage
lieferanten.import.csv | Enthält die Stammdaten der Lieferanten
medien.import.csv | Enthält die Stammdaten der Medien
exemplare.import.csv | Enthält die Exemplardaten zu den Medien
klassen.import.csv | Enthält die Stamm- und Zeitraumdaten der Klassen
schueler_laufbahn.import.csv | Enthält die Laufbahndaten der Schüler
schueler_fachdaten.import.csv | Enthält die Fachdaten der Schüler
schueler_sorgebe.import.csv | Enthält die Zuordnung der Sorgeberechtigten zu den Schülern
schueler_schulen.import.csv | Enthält die bereits besuchten Schulen der Schüler (Stichwort: Herkunftsschulen)
schueler_ausbildung.import.csv | Enthält die Ausbildungsdaten der Schüler

### Einlesen oder Prüfen der Daten

|So gehen Sie vor:|
|--|
|**Importformatdatei wählen**<br/><br/>Klicken Sie auf das `Plus`-Symbol und verweisen auf eine oder mehrere zu importierende csv-Dateien. Erkennt der Assistent die Dateinamen, ordnet er in der ersten Spalte `Importart` die entsprechende Bezeichnung zu. Ist der Dateiname nicht zuzuordnen, erhält die Zeile den Wert `unbekannt`, die Schaltfläche `Weiter` bleibt in diesem Fall deaktiviert. Bitte ordnen Sie in diesem Fall die korrekte Auswahl zu. <br/>Sobald Sie die Auswahl vollständig getroffen haben, sortiert der Assistent die Dateien in die korrekte Reihenfolge für das Einlesen, die `Weiter`-Schaltfläche wird aktiviert.<br/>Eine versehentlich ausgewählte Datei können Sie über das `Minus`-Symbol wieder entfernen.<br/>Klicken Sie auf `Weiter`!|
|**Abbildung:**<br/><img src="/assets/images/magellan.administrator/import01.png">|
|**Auswahl der Importparameter**<br/><br/>Wählen Sie bitte Ihren Zielmandanten im Feld `Importiere für den folgenden Mandanten` aus!<br/><br/>Je nach Dateiauswahl (Medien-Exemplare) auf der vorangegangenen Karte, kann das Feld `Importiere für den folgenden Medienkatalog` gezeigt werden, treffen Sie hier bitte Ihre Auswahl!<br/><br/>**Datenprüfung und Import**<br/><br/>Setzen Sie den Haken um Ihre gewählten Dateien im Anschluss prüfen zu lassen. Ist der Haken nicht aktiviert, wird versucht die Daten in Ihre Datenbank einzulesen.<br/>Treffen Sie Ihre Auswahl und klicken bitte auf `Weiter`!|
|**Abbildung:**<br/><img src="/assets/images/magellan.administrator/import02.png">|
|Klicken Sie auf `Fertigstellen`! <br/>Das Einlesen oder Prüfen, je nach Ihrer Auswahl auf der vorangegangenen Seite, geschieht dateiweise. Es werden im Fenster die Meldungen des Einlesens oder des Prüfens für die Dateien gezeigt. Im Anschluss erscheint ein Fenster, in dem Sie entscheiden können, die nächste Datei einlesen oder prüfen zu lassen. Die eventuell zuvor ausgegebenen Meldungen bleiben in der Liste bestehen und werden ggfs. durch weitere Meldungen ergänzt.<br/>Entstandene Meldungen können Sie exportieren.<br/>Nach Abschluss der Prüfung oder des Einlesens schließen Sie den Assistenten.|
|**Abbildung:**<br/><img src="/assets/images/magellan.administrator/import03.png">|

## MAGELLAN DataCenter starten

**Derzeit nicht veröffentlich**

Das MAGELLAN DataCenter ermögicht Ihnen die Konvertierung von Daten fremder Anbieter in das MAGELLAN-Importformat. Es werden verschiedene Quelldatenbank- und Quellsysteme untestützt.
Anhand von Prüfungs- und Konvertierungsregeln können Sie nicht konforme Daten entweder ersetzen oder überspringen. Zusätzlich können komplexe Konvertierungsroutinen per JavaScript-Technologie implementiert werden.
