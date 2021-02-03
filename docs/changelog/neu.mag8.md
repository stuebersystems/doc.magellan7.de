# Was ist neu?

Die nachfolgenden Abschnitte richten sich an die Nutzer von MAGELLAN 7. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen geben.

## Datenstrukturänderungen

Die Neuerungen in der Datenstruktur finden Sie als Zusammenfassung hier:[https://doc.magellan7-toolbox.stueber.de/datenstruktur/version8/neuerungen/](https://doc.magellan7-toolbox.stueber.de/datenstruktur/version8/neuerungen/).

## MAGELLAN Schulverwaltung

### Verzeichnis Staatsangehörigkeiten

Die Angaben aus dem Verzeichnis `Extras > Schlüsselverzeichnisse > Staatsangehörigkeiten` werden für die Felder `Geburtsland`, `Staatsangehörigkeit1` und `Staatsangehörigkeit2` verwendet, bislang gab es hierfür nur eine Bezeichnung. Neu ist die Spalte `Bezeichnung2`, damit kann in der Spalte `Bezeichnung1` weiterhin die Bezeichnung des Landes geführt werden, in der Spalte `Bezeichnung2` wird die Staatsangehörigkeit geführt. Die `Bezeichnung2` wird auch in den Listenfeldern in der Oberfläche gezeigt.
Für eigene Berichte können Sie die Werte damit gezielt ausgeben.

Bei der Anpassung der Datenbank von der Version 7 auf die Version 8 füllen wir die Werte in der zweiten Spalte auf. Erkannt wird die Zeile anhand des Schlüssels, die Schlüssel sind bundeslandübergreifend einheitlich.

![Extras > Schlüsselverzeichnisse > Staatsangehörigkeiten](/assets/images/changelog/aenderungen8/01.png)

### Hauptversicherter

Jedem Schüler können mehrere Familienangehörige zugeordnet werden. Zusätzlich kann gezielt ein Familienmitglied als `Hauptversicherter` markiert werden. Diese Möglichkeit finden Sie unter `Schüler > Daten1 > Familie`. Markieren Sie den gewünschten Eintrag, klicken Sie auf das Editiersymbol im Folgefenster. Hier kann per Haken die Auswahl `Hauptversicherter` getroffen werden. Diese Auswahl wird unter `Daten1 > Familie` für das Familienmitglied in blau hervorgehoben.

![Schüler > Daten1 > Familie](/assets/images/changelog/aenderungen8/04.png)

### Registerkarte Abschluss

`Schüler > Laufbahn > Abschluss`: Die Bezeichnung der `Abschlussart` lautet nun `Abschlussart1`  und `Abschlussart2`.

![ `Schüler > Laufbahn > Abschluss`](/assets/images/changelog/aenderungen8/03.png)

### Fachthema

Unter `Schüler > Zeugnis > Fächer` kann je Fachzeile ein Thema vergeben werden. Klicken Sie doppelt für das gewünschte Fach auf das Feld `Thema`, es öffnet sich ein Bearbeitungsfenster.

![Schüler > Zeugnis > Fächer > Thema](/assets/images/changelog/aenderungen8/05.png)

### Tastenkürzel im Berichtefenster

Neue Tastenkürzel erleichtern den Druck, Export und den Aufruf der Vorschau in allen Menüs für die Aufrufe `Berichte drucken` oder `Zeugnisse drucken`.

Tastenkürzel| Aktion
--|--
STRG + V | Ruft die Vorschau auf
STRG + P | Druckt den markierten Bericht aus
STRG + E | Exportiert den gewählten Bericht als PDF ins Dokumentenverzeichnis<br/>(abhängig von den Voreinstellungen unter `Datenbank > Optionen > Dokumente`)

### Schülerausweisdatum gesammelt zuweisen

Das Feld `Daten3 > Sonstige Daten > Schülerausweise > Ausgestellt am` kann per Sammelzuweisung den Schülern zugeordnet werden.

### Noten aus alten Halbjahren übernehmen

1. Wählen Sie den Zeitraum, in den die Note fortgeschrieben werden soll!
2. Starten Sie den Aufruf `Laufbahnprozess > Noten Fortschreiben`!
3. Wählen Sie den Schüler aus!
4. Bitte den alten Zeitraum auswählen, ggf. Option "eingetragene Noten überschreiben" auswählen
5. Anschließend die Fächer auswählen und fertigstellen!

Es werden die Noten für die ausgewählten Schüler und ausgewählten Fächer kopiert. Wenn die Option übers`Bereits eingetragene Noten überschreiben` angehakt ist, werden Noten überschrieben, ansonsten wird das Fach übersprungen.

### Neue Schüler-Merkmale

Unter `Schüler > Merkmale` stehen vier neue Felder zur Verfügung (`MerkmalA7`-`MerkmalA10`). Diese Merkmale können per Sammelzuweisung befüllt werden.

### Bemerkungsliste

Unter `Schüler > Merkmale` gibt es eine neue Liste für die Erfassung der unterschiedlichesten Textinhalte. Um die Inhalte zu strukturieren gibt es die `Kategorie`. Der Feldtyp der Kategorie lässt es zu, dass eingetippte Werte gemerkt und für die nächste Zeile bereits zur Auswahl angeboten werden.

![ `Bemerkungsliste`](/assets/images/changelog/aenderungen8/07.png)

### Besonderheitenliste Schüler

Unter `Schüler > Merkmale` gibt es eine neue Liste für die Erfassung von statistisch auszuwertenden Schüler-Besonderheiten.
Jeder Zeile kann aus dem neuen Schlüsselverzeichnis `Besonderheiten` ein Schlüsselwert zugewiesen werden.
Um die Inhalte zu strukturieren gibt es die `Kategorie`. Der Feldtyp der Kategorie lässt es zu, dass eingetippte Werte gemerkt und für die nächste Zeile bereits zur Auswahl angeboten werden.

![`Besonderheitenliste`](/assets/images/changelog/aenderungen8/09.png)

### Besonderheitenliste Klasse

Unter `Klassen > Merkmale` gibt es eine neue Liste für die Erfassung von statistisch auszuwertenden Klassen-Besonderheiten.
Jeder Zeile kann aus dem neuen Schlüsselverzeichnis `Besonderheiten` ein Schlüsselwert zugewiesen werden.
Um die Inhalte zu strukturieren gibt es die `Kategorie`. Der Feldtyp der Kategorie lässt es zu, dass eingetippte Werte gemerkt und für die nächste Zeile bereits zur Auswahl angeboten werden.

![`Besonderheitenliste`](/assets/images/changelog/aenderungen8/10.png)

### Schlüsselverzeichnis Besonderheiten

Unter `Extras > Schlüsselverzeichnisse > Besonderheiten` können als Grundlage für die Eintragungen der Besonderheitenlisten für Schüler und Klassen Schlüsselwerte angelegt werden. In welcher der beiden Listen Ihre Eintragung gezeigt wird, muss mit der Auswahl im Feld `Kategorie` festgelegt werden.

![`Besonderheitenliste`](/assets/images/changelog/aenderungen8/08.png)

### Thema der BLL auf 300 Zeichen erhöht

Unter `Abitur > Prüfungen > Besondere Lernleistung > Thema` können 300 Zeichen für das Thema gespeichert werden.

### Auswahlliste Bewerber

Die Auswahlliste der Bewerber `Bewerber > Auswahl` wurde um die Spalten der Fremdsprachenfolge, `Fremdsprache1`,  `Fremdsprache2`,  `Fremdsprache3`,  `Fremdsprache4` erweitert.

![ `Bewerber > Auswahl`](/assets/images/changelog/aenderungen8/02.png)

### Bewerberstatus Ablehnungsbescheid

Im Menü `Bewerber` gibt es den neuen Wert `Ablehnungsbescheid` im Feld `Status`.

### Bewerber mit Sorgeberechtigten löschen

Beim Löschen eines Bewerbers erscheint ein Optionsfenster, über das man die Sorgeberechtigten mit derselben Aktion löschen kann, wenn keine anderen Schüler oder Bewerber mit dem Sorgeberechtigten verknüpft sind.

![ `Sorgeberechtigte optional mitlöschen`](/assets/images/changelog/aenderungen8/11.png)

### Anrede für Ausbilderkontakt

Die Möglichkeit einen Kontakt für Betrieb zu hinterlegen `Betriebe > Kontakte` wurde um das Feld `Anrede`erweitert.

### Seriendruck

#### Schüler

Erweiterung des Seriendruckes für Schülers um das Feld `Betriebe > Kontakte > Anrede`.

#### Lehrer

Erweiterung des Seriendruckes für die Lehrkraft um die Felder `Lehrkraft > Daten2 > Amtsbez` und die `Lehrkraft > Daten2 > Dienstbez`.

## MAGELLAN ADMINISTRATOR

### Benutzerrechte

Sie können für jeden Benutzer individuell den Zugriff auf Menüpunkte in der Schulverwaltung unterbinden. Melden Sie sich als Administrator (`sysdba`) MAGELLAN ADMINISTRATOR an. Im Menüpunkt `Benutzerverwaltung` wählen Sie per Doppelklick den anzupassenden Benutzeraccount aus. Auf der neuen Registerkarte `Ansichten` können Sie per Häkchen den Zugriff gewähren oder unterbinden.

![Benutzerverwaltung > Ansichten ausblenden](/assets/images/changelog/aenderungen8/02.png)

## MAGELLAN BIBLIOTHEK

### Ausleihen

Die Auswahllisten der Lehrer und Personen `Lehrer > Auswahl`und `Personen > Auswahl`wurden um das Feld `Ausleihe`erweitert.

## Statistiken

### Sachsen

#### Fremdsprachen

Es wird unterschieden zwischen

  *  Ausspielen abgegangene Schülerdatei (Quelle: `Daten3 > Fremdsprachenfolge`)
  * Ausspielen aktuelle Schülerdatei (Quelle: Vergleich zwischen den `Schüler > Zeugnis > Fächer` des 1. und ggfs. 2.Halbjahres und den Einträgen unter `Daten3 > Fremdsprachenfolge`)

Rufen Sie die Erstellung der Statistikdatei für aktuelle Schüler aus dem zweiten Halbjahr auf, vergleichen wir im ersten Schritt die Fachdaten des 1.Halbjahres mit der Fremdsprachenfolge. Werden passende Einträge gefunden, werden diese gemerkt und die Fachdaten des 2.Halbjahres mit der Fremdsprachenfolge verglichen. Werden weitere passende Einträge gefunden, werden die Treffer (Beispiel: Eng als 1.Fremdsprache unter `Daten3` und auch Eng unter `Schüler > Zeugnis > Fächer`) aus dem 1. und dem 2. Durchlauf als Fremdsprachen ausgespielt.
Ein aktueller Nutzungsvertrag wird vorausgesetzt.

### Niedersachsen

Eine neue Schnittstelle für die Übergabe nach IZN-Stabil Niedersachsen wurde eingebunden, ein aktueller Nutzungsvertrag wird vorausgesetzt.
