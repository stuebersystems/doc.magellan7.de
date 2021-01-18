# Was ist neu?

Die nachfolgenden Abschnitte richten sich an die Nutzer von MAGELLAN 7. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen geben.

## MAGELLAN Schulverwaltung

### Verzeichnis Staatsangehörigkeiten

Die Angaben aus dem Verzeichnis `Extras > Schlüsselverzeichnisse > Staatsangehörigkeiten` werden für die Felder `Geburtsland`, `Staatsangehörigkeit1` und `Staatsangehörigkeit2` verwendet, bislang gab es hierfür nur eine Bezeichnung. Neu die Spalte `Bezeichnung2`, damit kann in der Spalte `Bezeichnung1` weiterhin die Bezeichnung des Landes geführt werden, in der Spalte `Bezeichnung2` wird die Staatsangehörigkeit geführt. Die `Bezeichnung2` wird auch in den Listenfeldern in der Oberfläche gezeigt.
Für eigene Berichte können Sie die Werte gaben damit gezielt ausgeben.

Bei der Anpassung der Datenbank von der Version 7 auf die Version 8 füllen wir die Werte in der zweiten Spalte auf. Erkannt wird die Zeile anhand des Schlüssels, die Schlüssel sind bundeslandübergreifend einheitlich.

![Extras > Schlüsselverzeichnisse > Staatsangehörigkeiten](/assets/images/changelog/aenderungen8/01.png)

### Hauptversicherter

Jedem Schüler können mehrere Familienangehörige zugeordnet werden. Zusätzlich kann gezielt ein Familienmitglied als `Hauptversicherter` markiert werden. Diese Möglichkeit finden Sie unter `Schüler > Daten1 > Familie`. Markieren Sie den gewünschten Eintrag, klicken Sie auf das Editiersymbol im Folgefenster kann per Haken die Auswahl `Hauptversicherter` getroffen werden. Diese Auswahl wird unter `Daten1 > Familie` für das Familienmitglied in blau hervorgehoben.

![Schüler > Daten1 > Familie](/assets/images/changelog/aenderungen8/04.png)

### Registerkarte Abschluss
 
`Schüler > Laufbahn > Abschluss` die Bezeichnung der `Abschlussart` lautet nun `Abschlussart1`  und `Abschlussart2`.

![ `Schüler > Laufbahn > Abschluss`](/assets/images/changelog/aenderungen8/03.png)

### Fachthema

Unter `Schüler > Zeugnis > Fächer` kann je Fachzeile ein Thema vergeben werden. Klicken Sie doppelt für das gewünschte Fach auf das Feld `Thema`, es öffnet sich ein Bearbeitungsfenster. 

![Schüler > Zeugnis > Fächer > Thema](/assets/images/changelog/aenderungen8/05.png)

### Auswahlliste Bewerber
 
Die Auswahlliste der Bewerber `Bewerber > Auswahl`wurde um die Spalten der Fremdsprachenfolge, `Fremdsprache1`,  `Fremdsprache2`,  `Fremdsprache3`,  `Fremdsprache4` erweitert.
 
![ `Bewerber > Auswahl`](/assets/images/changelog/aenderungen8/02.png)

## MAGELLAN ADMINISTRATOR

### Benutzerrechte

Sie können für jeden Benutzer individuell den Zugriff auf Menüpunkte in der Schulverwaltung unterbinden. Melden Sie sich als Administrator (`sysdba`) MAGELLAN ADMINISTRATOR an. Im Menüpunkt `Benutzerverwaltung` wählen Sie per Doppelklick den anzupassenden Benutzeraccount aus. Auf der neuen Registerkarte `Ansichten` können Sie per Häkchen den Zugriff gewähren oder unterbinden.

![Benutzerverwaltung > Ansichten ausblenden](/assets/images/changelog/aenderungen8/02.png)
