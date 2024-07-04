# Magellan ↔ DaVinci

Wenn Sie Magellan und DaVinci gemeinsam einsetzen, so haben Sie den Vorteil, dass viele Daten nur einmal eingegeben werden müssen. Dadurch können Doppelerfassungen von Daten minimiert bzw. vermieden werden.
Von Magellan können die Abteilungen, die Lehrer, die Fächer, die Fachtafeln, die Klassen und die Schüler der Oberstufe an DaVinci übergeben werden.

Von DaVinci können die Abteilungen, die Lehrer, die Fächer, die Stundentafeln, die Kurswahlen der Schüler der Oberstufe und der Fach- bzw. Kurslehrer an Magellan übergeben werden.

!!! info "Hinweis"

	Der Datenaustausch wird grundsätzlich (egal in welche Richtung) von DaVinci aus gestartet.
Sie benötigen die Magellan-Administrator-Kennung, da der Austausch nur mit Administrator-Rechten erfolgen kann.

	Wenn Sie Magellan und DaVinci einsetzen, sollten Sie wie folgt vorgehen:

1. Geben Sie die Klassen, Lehrer, Fächer und Schüler in Magellan ein und übertragen Sie diese Daten anschließend nach DaVinci.
2. Geben Sie die Unterrichtsverteilung in DaVinci ein und erstellen Sie mit DaVinci den Stundenplan.
3. eben Sie ggf. die Schülerfachwahlen in DaVinci::Kursplan ein und übertragen Sie die Kurswahlen nach Magellan. Wenn Sie Schüler-Fachwahlen nach Magellan übertragen wollen und Sie neue Fächer in DaVinci eingegeben haben, die noch nicht in Magellan vorhanden sind, dann müssen Sie beim Datenabgleich neben den Schülerfachwahlen auch markieren, dass die Fächer übernommen werden sollen.

!!! info "Hinweis"

	Bitte beachten Sie beim Datenabgleich zwischen Magellan und DaVinci allgemein die folgenden Hinweise:
	Vor jedem Datenaustausch sollten Sie eine Datensicherung der Magellan-Datenbank (Magellan.fdb) und der DaVinci-Plandatei (*.DaVinci) durchführen. Ein versehentlicher Übertrag kann nicht rückgängig gemacht werden.

Was|Wichtige Hinweise
---|---
**Kürzel**| Beim Austausch über das Kürzel wird die Groß- und Kleinschreibung beachtet.<br/><br/>Bitte beachten Sie, dass das Kürzel einer Stundentafel in DaVinci 20 Zeichen lang sein kann und das Kürzel einer Fachtafel (Stundentafel) in Magellan nur 8 Zeichen lang sein kann. Sind die Kürzel in DaVinci länger als 8 Zeichen, kommt es zu einer Fehlermeldung beim Datenabgleich. Daher sollten Sie darauf achten, wenn Sie die Stunden- bzw. Fachtafeln abgleichen wollen, dass die Kürzel jeweils maximal 8 Zeichen lang sind.
**Stammdaten**|Nicht alle Stammdatenfelder aus DaVinci sind auch in Magellan vorhanden und umgekehrt. Werden die vorhandenen Daten beim Austausch aktualisiert (überschrieben), können vorhandene Einträge verloren gehen, z.B. bei den Klassen der Klassenraum oder bei den Stundentafeln die Soll-Stunden. Bitte entscheiden Sie mit Bedacht, welche Daten Sie austauschen.
**Unterrichtsarten**<br/>**Fachstatus**|Für den Übertrag von Fachinformationen (z.B. Schülerfachwahlen) müssen die Unterrichtsarten und Fachstatus in beiden Programmen identisch angelegt sein.

## Magellan → DaVinci

Sie können die Magellan-Daten in eine leere oder vorbefüllte DaVinci-Datei übernehmen.
Wenn Sie einen bisher leeren Plan mit Daten aus Magellan füllen möchten, müssen Sie in DaVinci eine neue Plandatei anlegen.
Wenn in der DaVinci-Datei bereits Daten enthalten sind, werden die vorhandenen Stammdaten ergänzt bzw. aktualisiert (mit den Daten aus Magellan überschrieben).

### Schritte zum Übernehmen

Um Daten von Magellan nach DaVinci zu übertragen, gehen Sie bitte folgendermaßen vor:

 1. Klicken Sie im Menüband von `DaVinci` des Programmfensters auf die Schaltfläche `Plan`. <br/>
 2. Wählen Sie im Planmenü den Befehl `Importieren und Exportieren`: der Assistent „Import/ Export-Assistent“ wird geöffnet.<br/>
 3. Markieren Sie auf der ersten Assistentenseite im Bereich „Import“ den Eintrag „Von Magellan importieren.“<br/>
 4. Bestätigen Sie Ihre Auswahl mit `Weiter`.<br/>
 5. Geben Sie im erscheinenden Dialogfenster „Magellan-Anmeldung“ Benutzername und Kennwort des Administratorkontos ein und bestätigen Sie Ihre Zugangsdaten mit OK: der Assistent „Magellan-Datenaustausch“ wird geöffnet. ![ Hier sehen Sie die erste Seite des Assistenten "Magellan-Datenaustausch".](/assets/images/datenaustausch_mit_magellan/01.png)
 6. Bestätigen Sie auf der ersten Seite des Assistenten die Option „Daten aus Magellan in eine SDTF-Datei schreiben“ mit `Weiter`.<br/>
 7. Wählen Sie auf der folgenden Assistentenseite in den Feldern „Übertrage Daten aus folgendem Mandanten“ und „Übertrage Daten aus folgendem Zeitraum“ den gewünschten Mandanten und Zeitraum aus dem Aufklappmenü. ![ Hier legen Sie den Mandanten und den Zeitraum für den Datenübertrag fest.](/assets/images/datenaustausch_mit_magellan/02.png)
 8. Bestätigen Sie Ihre Auswahl mit `Weiter`.<br/>
 9. Setzen Sie auf der nächsten Assistentenseite den Haken vor den gewünschten Optionen für die Übernahme unterschiedlicher Datenbereich nach DaVinci. ![ Hier wählen Sie die Daten aus, die aus Magellan übernommen werden.](/assets/images/datenaustausch_mit_magellan/03.png)
10. Bestätigen Sie Ihre Auswahl mit `Weiter`. <br/>
11. Drücken Sie auf der nächsten Assistentenseite die Schaltfläche `Starten`.<br/>

Die Daten werden nun entsprechend der vorgenommenen Einstellungen in die DaVinci-Datei übertragen. Den Fortschritt des Datenimports können Sie anhand der Meldungen im Dialogfenster „Datei in Schuldatentransferdatei “ erkennen.

### Was kann übernommen werden

Sie können folgende Daten übernehmen:

![Übernahmeoptionen](/assets/images/datenaustausch_mit_magellan/06.png)

### Übernehme Abteilungen

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird die Abteilung aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird die Abteilung hinzugefügt.

### Übernehme Räume

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird der Raum aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird der Raum hinzugefügt.

### Übernehme Lehrer

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Nachname**<br/>**Vorname**<br/>**Titel**<br/>**Schulnummer (`Mandant > Daten1 Schulnummer`)**<br/>**Abteilungen** [Abteilung.Kürzel]|Der Austausch erfolgt über ID und Kürzel.<br/> Bei gleicher ID wird aktualisiert.<br/> Ist in DaVinci keine ID vorhanden, wird über das Kürzel ausgetauscht. <br/>Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird hinzugefügt.<br/>Es werden nur aktive Lehrer aus Magellan beim Abgleich berücksichtigt.

### Übernehme Fächer

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Schlüssel**<br/>**Bezeichnung**<br/>**Kategorie**<br/>**Aufgabenbereich**|Der Austausch erfolgt über ID und Kürzel. <br/>Bei gleicher ID wird aktualisiert. <br/>Ist in DaVinci keine ID vorhanden, wird über das Kürzel ausgetauscht.<br/> Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird das Fach hinzugefügt.

### Übernehme Fachtafeln

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**<br/>Fächer der Fachtafel: <br/>   **Kürzel** Unterrichtsart.Kürzel]|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird aktualisiert.<br/> Ist das Kürzel nicht vorhanden wird die Fachtafel hinzugefügt.<br/>Fachtafeln aus Magellan entsprechen Stundentafeln in DaVinci.

### Übernehme Klassen/Jahrgänge

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Klassenleiter 1**<br/>**Klassenleiter 2**<br/>**Klassenstufe**<br/>**Klassenart **(Kursmodus)<br/>**Anzahl der Schüler**<br/>**Schulnummer**<br/>**Bildungsgang.Kürzel**<br/>**Schulform.Kürzel**<br/>**Schulstelle.Kürzel**|Der Austausch erfolgt über ID und Kürzel.<br/> Bei gleicher ID wird aktualisiert.<br/> Ist in DaVinci keine ID vorhanden, wird über das Kürzel ausgetauscht.<br/> Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird die Klasse/der Jahrgang hinzugefügt.<br/>Die Anzahl der Schüler wird nur für Oberstufenklassen übernommen.

### Übernehme Schüler

#### Nur der Oberstufe/ Aller Klassen

Felder|Hinweis
---|---
Stammdaten:<br/>**Vorname**<br/>**Nachname **<br/>**Magellan.ID**<br/> **Geschlecht **<br/>**Geburtsdatum **<br/>**Klasse **<br/>**Stufe **<br/>**Tutor **<br/>**Email **<br/>**Schulnummer**<br/><br/>Schülerfächer:<br/>**Fach **<br/>**Fachstatus**<br/> **Unterrichtsart**|Es ist möglich nur einen Teil der Schüler zur Übernahme auszuwählen.<br/> Der Austausch erfolgt über ID, Nachname und Vorname.<br/> Bei gleicher Daten wird aktualisiert.<br/> Schülerfächer werden als Schülerfachwahlen übernommen. Werden Schüler erneut übernommen, werden die eventuell bestehenden Fachwahlen in DaVinci gelöscht und mit den Daten aus Magellan überschrieben.<br/><br/>Tutor und Klasse, genau wie die Fachwahlen können nur zugeordnet werden, wenn die zugrunde liegenden Daten in DaVinci vorhanden sind (Lehrer.Kürzel, Klassen.Kürzel, Fach.Kürzel, Unterrichtsart.Kürzel, Fachstatus.Kürzel).

!!! info "Hinweis"

	Als Oberstufenklasse gelten Klassen mit der Klassenart (`Magellan: Klassen > Daten > Klassenart`) "Oberstufenjahrgang (Nur Kurse)" oder "Oberstufenjahrgang (Grund- und Leistungskurse)"  mit dem Jahrgang 11-13 (`Magellan: Klassen > Zeiträume > Zeitraum > Jahrgang`) .

## DaVinci → Magellan

Wenn Sie eine leere Magellan-Datenbank mit Daten aus DaVinci füllen möchten, müssen in Magellan mindestens ein Mandant und ein Zeitraum eingerichtet sein.

### Schritte zum Übernehmen

Um Daten von DaVinci nach Magellan zu übertragen, gehen Sie bitte folgendermaßen vor:  

1. Klicken Sie im Menüband von `DaVinci` des Programmfensters auf die Schaltfläche `Plan`.
2. Wählen Sie im Planmenü den Befehl `Importieren und Exportieren`: der Assistent „Import/ Export-Assistent“ wird geöffnet.
3. Markieren Sie auf der ersten Assistentenseite im Bereich „Import“ den Eintrag „Nach Magellan exportieren.“
4. Bestätigen Sie Ihre Auswahl mit `Weiter`.
5. Geben Sie im erscheinenden Dialogfenster „Magellan-Anmeldung“ Benutzername und Kennwort des Administratorkontos ein und bestätigen Sie Ihre Zugangsdaten mit `OK`: der Assistent „Magellan-Datenaustausch“ wird geöffnet.
6. Bestätigen Sie auf der ersten Seite des Assistenten die Option „Daten aus einer SDTF-Datei nach Magellan schreiben“ mit `Weiter`.
7. Wählen Sie in den Feldern „Übertrage Daten in folgenden Mandanten“ und „Übertrage Daten in folgendem Zeitraum“ den gewünschten Mandanten und Zeitraum aus dem Aufklappmenü. ![Hier wählen Sie den Mandanten und den Zeitraum aus, in den die Daten übertragen werden.](/assets/images/Datenaustausch_mit_magellan/04.png)
8. Bestätigen Sie Ihre Auswahl mit `Weiter`. <br/>
9. Setzen Sie auf der nächsten Assistentenseite den Haken vor den gewünschten Optionen für die Übernahme unterschiedlicher Datenbereiche nach Magellan. ![ Hier wählen Sie die Daten aus, die nach Magellan übertragen werden.](/assets/images/datenaustausch_mit_magellan/05.png)
10. Bestätigen Sie Ihre Auswahl mit `Weiter`.
11. Drücken Sie auf der nächsten Assistentenseite die Schaltfläche `Starten`.

Die Daten werden nun entsprechend der vorgenommenen Einstellungen in die DaVinci-Datei übertragen. Den Fortschritt des Datenimports können Sie anhand der Meldungen im Dialogfenster „Datei in Schuldatentransferdatei “ erkennen.

### Was kann übernommen werden

Sie können folgende Daten übernehmen:

![ Übernahmeoptionen](/assets/images/datenaustausch_mit_magellan/07.png)

### Übernehme Abteilungen

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird die Abteilung aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird die Abteilung hinzugefügt.

### Übernehme Lehrer

Felder|Hinweis
---|---
**Kürzel**<br/>**Nachname**<br/>**Vorname**<br/>**Soll-Berechnung**|Der Austausch erfolgt über ID und Kürzel.<br/> Bei gleicher ID wird aktualisiert. <br/>Ist die ID in Magellan nicht vorhanden, wird hinzugefügt.<br/> Ist in DaVinci keine ID vorhanden, wird über das Kürzel ausgetauscht. <br/>Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird hinzugefügt.

### Übernehme Fächer

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Schlüssel**<br/>**Bezeichnung**<br/>**Kategorie**<br/>**Aufgabenbereich**|Der Austausch erfolgt über ID oder Kürzel. <br/>Hat das Fach eine ID in DaVinci, so wird ein entsprechendes Fach mit gleicher ID in Magellan gesucht. <br/>existiert ein solches Fach in Magellan, so wird es aktualisiert, andernfalls wird das Fach in Magellan hinzugefügt.<br/>Hat das Fach keine ID in DaVinci, so wird ein entsprechendes Fach mit gleichem Kürzel in Magellan gesucht. <br/>Existiert ein solches Fach in Magellan, so wird es aktualisiert, andernfalls wird das Fach in Magellan hinzugefügt.

### Übernehme Schülerkurswahlen

Optionen:

* alle Daten
* nur geänderte Daten und Übertrag aus in die Fachwahlen
* nur geänderte Daten/Bestehende Schülerkurswahlen nicht zuvor löschen
* nur geänderte Daten/Fehlende Klassen anlegen

#### Tutor

Wurde der Tutor in DaVinci unter `Stammdaten > Schüler > Tutor` verändert, wird dieser Wert in Magellan unter `Schüler > Zeugnis > Details > Tutor` aktualisiert.

#### Import ohne weitere Zusatzoptionen

Wenn Sie keine weiteren Zusatzoptionen auswählen, erfolgt die Übernahme der Schülerkurswahlen nach folgender Regel:

Wird der in DaVinci vorhandene Schüler in Magellan gefunden, so werden diesem Schüler unter Ansicht `„Schüler“ > Zeugnis > Fächer` alle seine bestehenden Einträge gelöscht und diese durch die Werte aus DaVinci ersetzt. Dabei werden die nachfolgenden Werte

* Fach,
* Unterrichtsart,
* Fachstatus,
* Kursummer und
* Position

in der unter Ansicht `„Schüler“ > Zeugnis > Fächer` pro erkanntem Schüler neu gefüllt. 

Ansicht „Schüler  > Zeugnis > Fächer“ je Schüler|Nach Magellan übernommen|SDTF-Datensatz P1 Feld 
---|---|---
Fach|Neu|Feld 21: Fachkürzel
Unterrichtsart|Neu|Feld 34: Unterrichtsart-Kürzel
Fachstatus|Neu|Feld 35: Fachstatus-Kürzel
Kursummer|Neu|Feld 33: Kursnummer
Position|Neu|Wird automatisch inkrementell errechnet nach der Reihenfolge der importierten Fächer

#### Import mit Zusatzoptionen

##### Import mit „Übertrag auch in die Fachwahlen“

Wenn Sie die Zusatzoption `Übertrag auch in die Fachwahlen` auswählen, werden die Einträge unter Ansicht `„Abitur“ > Fachwahl` pro erkanntem Schüler zusätzlich aktualisiert. 
**Dabei gelten folgende Regeln:** ist das zu übertragende Fach mit seiner Unterrichtsart bereits in der Fachwahl in Magellan vorhanden, so wird die gesamte Fachzeile mit den neuen Werte aus DaVinci überschrieben. Andernfalls wird eine neue Fachzeile mit den Werten aus DaVinci eingefügt.

##### Import mit „Bestehende Schülerkurswahlen zuvor nicht löschen“

Wenn Sie die Zusatzoption `Bestehende Schülerkurswahlen zuvor nicht löschen` auswählen, werden die Einträge unter Ansicht `„Schüler“ > Zeugnis > Fächer` pro erkanntem Schüler vor dem eigentliche Import nicht gelöscht. 

Für die Aktualisierung der Einträge unter Ansicht `„Schüler“ > Zeugnis > Fächer` gelten dann folgende Regeln:

 Was|Bedeutung
 ---|---
Ansicht `„Schüler“  > Zeugnis > Fächer`|Es werden folgende Werte aus der Stundenplansoftware nach Magellan übernommen
Fach mit der Unterrichtsart ist bereits vorhanden|- Fachstatus (Schlüssel)<br/>- Kursnummer (<kein Eintrag  >  , 0, 1, 2…)  
Fach mit der Unterrichtsart ist neu |-Fach (Kürzel und Schlüssel)<br/>- Unterrichtsart (Schlüssel)<br/>- Fachstatus (Schlüssel)<br/>- Kursnummer (<kein Eintrag  >  , 0, 1, 2…)<br/>- Position (0, 1, 2…)

Mit der Zusatzoption können Klassen automatisch in Magellan angelegt werden, wenn diese DaVinci neu angelegt wurden aber noch nicht in Magellan existieren. Der mit aus DaVinci übertragene Schüler wird aber noch nicht mit seiner Kurswahl importiert, da er zuerst in Magellan angelegt und in diese neue angelegte Klasse in Magellan eingeschult werden muss.

!!! info "Hinweis"

	Klassen wie auch Schüler sollten grundsätzlich in Magellan angelegt sein, da Magellan hierzu das führende System ist.

##### Import mit „Nur geänderte Daten“

Mit der Option `Nur geänderte Daten` werden nur solche die Schüler für den Import berücksichtigt, deren Daten sich zwischen Magellan und der zu importierenden Schuldatentransferdatei in der Kurswahl unterscheiden. Die Unterscheidung erfolgt auf Basis der Unterschiede

Bezeichnung|Inhalt
--|--
erste Variante|**Fachkombinationsnummer**
Programmstellen|`Magellan > Schüler > Zeugnis > Details > Fachkombination`<br/><br/>`Magellan > Schüler > Zeugnis > Details > Tutor`<br/>`DaVinci > Kursplan > Fachwahl`<br/>`DaVinci > Kursplan > Schüler > Schlüssel`
Ergebnis|Hat sich die Fachkombinationnummer durch die Fachwahlprüfung geändert, wird diese übertragen und der Tutor übertragen.
zweite Variante| **Unterschied in der Schülerkurswahl**
Programmstellen|`Magellan > Schüler > Zeugnis > Fächer`<br/>`Magellan > Schüler > Zeugnis > Leistungen`<br/>`DaVinci > Kursplan > Schüler/Fachwahlen`
Ergebnis|Ein Unterschied in der Kombination aus:<br/>* Fach<br/>* Unterrichtsart<br/>* Fachstatus<br/>* Kursummer<br/>* Schwerpunkt<br/>* Merkmal <br/><br/> Hat sich eine Änderung bei den Schülerfachdaten (`Schüler > Zeugnis > Fächer`) ergeben und ist keinem Fach ein Eintrag unter `Leistungen > Endnote1` zugewiesen worden, werden die Fach- und Leistungsdaten des Zeitraums gelöscht und neu mit den Daten aus DaVinci gefüllt.

!!! danger "Achtung"

	**Bis Version 8.0.4 galt:** Werden die Schülerfächer in Magellan durch den Abgleich gelöscht können zwei Folgeprobleme entstehen.
	
	1. Die Schülerfächer sind die Grundlage für die Halbjahresnoten. Werden die Fächer durch den Übertrag entfernt, werden auch gegebenenfalls bereits erfasste Noten gelöscht.
	2. Für MyMagellan-Dateien werden die Inhalte aus `Schüler > Zeugnis > Fächer` verwendet. Dabei werden die Daten anhand der ID aus der Tabelle SchuelerFachdaten gespeichert. Werden die Fächer in Magellan gelöscht und neu angelegt, wird auch eine neue ID für die Fachzeilen in der Tabelle SchuelerFachdaten vergeben. Damit können die Daten aus den zuvor erzeugten MyMagellan-Dateien nicht mehr zugeordnet werden.

    **Seit Version 8.0.5 gilt:** Die Schülerfachdaten werden nur noch gelöscht, wenn für kein Fach ein Eintrag unter `Leistungen > Endnote1` existiert. Existiert für ein Fach eine Note (Endnote1), bleiben die Schülerfachdaten in Magellan für den Schüler erhalten, der Assistent gibt Ihnen den Schülernamen und die SchülerID in der Meldung mit aus.

#### Übernehme Stundentafeln

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**<br/>Fächer der Stundentafel: <br/>**Fachkürzel**<br/>**Unterrichtsart.Kürzel**|Der Austausch erfolgt über das Kürzel. <br/>Ist das Kürzel bereits vorhanden, wird aktualisiert.<br/> Ist das Kürzel nicht vorhanden wird die Stundentafel hinzugefügt. <br/>Die Fächer werden mit Kürzel und Unterrichtart hinzugefügt.<br/>Stundentafeln in DaVinci werden als Fachtafeln nach Magellan übertragen. <br/>Dabei gelten folgende Voraussetzungen:<br/>• Fächer in DaVinci und Magellan müssen identische ID’s und Kürzel haben.<br/>• Unterrichtsarten in DaVinci müssen die gleichen Kürzel besitzen wie in Magellan.

![ Übernahmeoptionen](/assets/images/datenaustausch_mit_magellan/07.png)

#### Übernehme Lehrer-Unterricht

Bei der Übernahme des Lehrer-Unterrichts aus DaVinci werden durch den Import der Schuldatentransferdatei nach Magellan aufgrund der Veranstaltungsliste pro Klasse in DaVinci die Lehrer übernommen. Es werden bei allen Schülern einer Klasse, die Fächer in Magellan haben, die in der Schuldatentransferdatei zugeordneten Lehrer der gleichen Klasse zugeordnet.

Durch die Übernahme des Lehrer-Unterrichts wird pro Schüler unter Ansicht `„Schüler“ > Zeugnis > Fächer` jedem Fach der unterrichtende Fachlehrer aus DaVinci zugeordnet.

!!! danger "Achtung"

	Bei Veranstaltungszeilen aus DaVinci, denen mehr als eine Klasse zugewiesen wurde, ist es wichtig, dass diese Veranstaltungen auch eine Blockbezeichnung erhalten um korrekt ausgewertet werden können.

Felder|Hinweis
---|---
**Zugewiesener Lehrer in der Veranstaltungsliste**|<br/>Dabei prüft Magellan nach folgender Regel:<br/><br/>Unterrichtet der Lehrer<br/>- das gleiche Fach mit<br/>- gleichem Fachstatus und<br/>- gleicher Kursnummer in <br/>- der gleiche Klasse,  <br/> so wird er dem Schüler in diesem Fach zugeordnet.

!!! info "Hinweis"

	Der Lehrer-Unterrichts kann nur bei den Schülern in Magellan zuordnet werden, denen bereits Fächer zugeordnet wurden. Die Schülerfächer in Magellan und die Veranstaltungen der Veranstaltungsliste in DaVinci müssen in Fach, Fachstatus und Unterrichtsart identisch sein.

Ansicht „Schüler > Zeugnis > Fächer“ je Schüler|Nach Magellan übernommen|SDTF-Datensatz U1 Feld
---|---|---
Lehrer|Aktualisieren|Feld 4: Lehrerkürzel

Tabelle 3: Wertübernahme je Schüler nach Magellan wenn der Lehrer-Unterricht übernommen wird in der Schuldatentransferdatei (SDTF)

!!! info "Hinweis"

	Es wird nicht nur der Lehrer-Unterricht der Oberstufe abgeglichen. Die Übernahme des Lehrer-Unterrichts erfolgt nicht nur für die Oberstufen-Klassen, sondern für alle Klassen des gewählte Import-Zeitraums.
	Die Übernahme des Lehrer-Unterrichts und der Schülerkurswahlen kann in einem Importschritt erfolgen.

##### Beifachlehrer im Datenübertrag

!!! info "Hinweis"

	Beim Übertrag der unterrichtenden Fachlehrer von DaVinci nach Magellan, kann es dazu kommen, dass beim Sonderfall "Beifächer" der verkehrte Kollege zugeordnet wird.

     Es ist logisch nicht anders zu lösen, da es sich **zweimal um die identische Kombination aus Fach, Fachstatus und Unterrichtsart** handelt.

     Gibt es in der Veranstaltungsliste in DaVinci mehrere Veranstaltungen dieser Kombination mit unterschiedlichen Lehrern, ist es reiner Zufall, welcher Lehrer in Magellan gespeichert. Das Schuldatentraferdatei wird sequenziell abgearbeitet. Kommt DEU/L1 vor DEU/L2 für den Schüler in der Datei vor, wird beim Schüler DEU/L2 in Magellan gespeichert.Man kann es nur lösen, wenn die Haupt- und Beifach getrennte Kürzel haben, also tatsächlich zwei Fächer sind.

#### Übernehme Räume

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird der Raum aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird der Raum hinzugefügt.
