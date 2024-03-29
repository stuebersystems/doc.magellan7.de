# MAGELLAN ↔ DAVINCI

Wenn Sie MAGELLAN und DAVINCI gemeinsam einsetzen, so haben Sie den Vorteil, dass viele Daten nur einmal eingegeben werden müssen. Dadurch können Doppelerfassungen von Daten minimiert bzw. vermieden werden.
Von MAGELLAN können die Abteilungen, die Lehrer, die Fächer, die Fachtafeln, die Klassen und die Schüler der Oberstufe an DAVINCI übergeben werden.

Von DAVINCI können die Abteilungen, die Lehrer, die Fächer, die Stundentafeln, die Kurswahlen der Schüler der Oberstufe und der Fach- bzw. Kurslehrer an MAGELLAN übergeben werden.

!!! info "Hinweis"

	Der Datenaustausch wird grundsätzlich (egal in welche Richtung) von DAVINCI aus gestartet.
Sie benötigen die MAGELLAN-Administrator-Kennung, da der Austausch nur mit Administrator-Rechten erfolgen kann.

	Wenn Sie MAGELLAN und DAVINCI einsetzen, sollten Sie wie folgt vorgehen:

1. Geben Sie die Klassen, Lehrer, Fächer und Schüler in MAGELLAN ein und übertragen Sie diese Daten anschließend nach DAVINCI.
2. Geben Sie die Unterrichtsverteilung in DAVINCI ein und erstellen Sie mit DAVINCI den Stundenplan.
3. eben Sie ggf. die Schülerfachwahlen in DAVINCI::Kursplan ein und übertragen Sie die Kurswahlen nach MAGELLAN. Wenn Sie Schüler-Fachwahlen nach MAGELLAN übertragen wollen und Sie neue Fächer in DAVINCI eingegeben haben, die noch nicht in MAGELLAN vorhanden sind, dann müssen Sie beim Datenabgleich neben den Schülerfachwahlen auch markieren, dass die Fächer übernommen werden sollen.

!!! info "Hinweis"

	Bitte beachten Sie beim Datenabgleich zwischen MAGELLAN und DAVINCI allgemein die folgenden Hinweise:
	Vor jedem Datenaustausch sollten Sie eine Datensicherung der MAGELLAN-Datenbank (MAGELLAN.fdb) und der DAVINCI-Plandatei (*.DAVINCI) durchführen. Ein versehentlicher Übertrag kann nicht rückgängig gemacht werden.

Was|Wichtige Hinweise
---|---
**Kürzel**| Beim Austausch über das Kürzel wird die Groß- und Kleinschreibung beachtet.<br/><br/>Bitte beachten Sie, dass das Kürzel einer Stundentafel in DAVINCI 20 Zeichen lang sein kann und das Kürzel einer Fachtafel (Stundentafel) in MAGELLAN nur 8 Zeichen lang sein kann. Sind die Kürzel in DAVINCI länger als 8 Zeichen, kommt es zu einer Fehlermeldung beim Datenabgleich. Daher sollten Sie darauf achten, wenn Sie die Stunden- bzw. Fachtafeln abgleichen wollen, dass die Kürzel jeweils maximal 8 Zeichen lang sind.
**Stammdaten**|Nicht alle Stammdatenfelder aus DAVINCI sind auch in MAGELLAN vorhanden und umgekehrt. Werden die vorhandenen Daten beim Austausch aktualisiert (überschrieben), können vorhandene Einträge verloren gehen, z.B. bei den Klassen der Klassenraum oder bei den Stundentafeln die Soll-Stunden. Bitte entscheiden Sie mit Bedacht, welche Daten Sie austauschen.
**Unterrichtsarten**<br/>**Fachstatus**|Für den Übertrag von Fachinformationen (z.B. Schülerfachwahlen) müssen die Unterrichtsarten und Fachstatus in beiden Programmen identisch angelegt sein.

## MAGELLAN → DAVINCI

Sie können die MAGELLAN-Daten in eine leere oder vorbefüllte DAVINCI-Datei übernehmen.
Wenn Sie einen bisher leeren Plan mit Daten aus MAGELLAN füllen möchten, müssen Sie in DAVINCI eine neue Plandatei anlegen.
Wenn in der DAVINCI-Datei bereits Daten enthalten sind, werden die vorhandenen Stammdaten ergänzt bzw. aktualisiert (mit den Daten aus MAGELLAN überschrieben).

### Schritte zum Übernehmen

Um Daten von MAGELLAN nach DAVINCI zu übertragen, gehen Sie bitte folgendermaßen vor:

 1. Klicken Sie im Menüband von `DAVINCI` des Programmfensters auf die Schaltfläche `Plan`. <br/>
 2. Wählen Sie im Planmenü den Befehl `Importieren und Exportieren`: der Assistent „Import/ Export-Assistent“ wird geöffnet.<br/>
 3. Markieren Sie auf der ersten Assistentenseite im Bereich „Import“ den Eintrag „Von MAGELLAN importieren.“<br/>
 4. Bestätigen Sie Ihre Auswahl mit `Weiter`.<br/>
 5. Geben Sie im erscheinenden Dialogfenster „MAGELLAN-Anmeldung“ Benutzername und Kennwort des Administratorkontos ein und bestätigen Sie Ihre Zugangsdaten mit OK: der Assistent „MAGELLAN-Datenaustausch“ wird geöffnet. ![ Hier sehen Sie die erste Seite des Assistenten "MAGELLAN-Datenaustausch".](/assets/images/datenaustausch_mit_magellan/01.png)
 6. Bestätigen Sie auf der ersten Seite des Assistenten die Option „Daten aus MAGELLAN in eine SDTF-Datei schreiben“ mit `Weiter`.<br/>
 7. Wählen Sie auf der folgenden Assistentenseite in den Feldern „Übertrage Daten aus folgendem Mandanten“ und „Übertrage Daten aus folgendem Zeitraum“ den gewünschten Mandanten und Zeitraum aus dem Aufklappmenü. ![ Hier legen Sie den Mandanten und den Zeitraum für den Datenübertrag fest.](/assets/images/datenaustausch_mit_magellan/02.png)
 8. Bestätigen Sie Ihre Auswahl mit `Weiter`.<br/>
 9. Setzen Sie auf der nächsten Assistentenseite den Haken vor den gewünschten Optionen für die Übernahme unterschiedlicher Datenbereich nach DAVINCI. ![ Hier wählen Sie die Daten aus, die aus MAGELLAN übernommen werden.](/assets/images/datenaustausch_mit_magellan/03.png)
10. Bestätigen Sie Ihre Auswahl mit `Weiter`. <br/>
11. Drücken Sie auf der nächsten Assistentenseite die Schaltfläche `Starten`.<br/>

Die Daten werden nun entsprechend der vorgenommenen Einstellungen in die DAVINCI-Datei übertragen. Den Fortschritt des Datenimports können Sie anhand der Meldungen im Dialogfenster „Datei in Schuldatentransferdatei “ erkennen.

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
**ID**<br/>**Kürzel**<br/>**Nachname**<br/>**Vorname**<br/>**Titel**<br/>**Schulnummer (`Mandant > Daten1 Schulnummer`)**<br/>**Abteilungen** [Abteilung.Kürzel]|Der Austausch erfolgt über ID und Kürzel.<br/> Bei gleicher ID wird aktualisiert.<br/> Ist in DAVINCI keine ID vorhanden, wird über das Kürzel ausgetauscht. <br/>Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird hinzugefügt.<br/>Es werden nur aktive Lehrer aus MAGELLAN beim Abgleich berücksichtigt.

### Übernehme Fächer

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Schlüssel**<br/>**Bezeichnung**<br/>**Kategorie**<br/>**Aufgabenbereich**|Der Austausch erfolgt über ID und Kürzel. <br/>Bei gleicher ID wird aktualisiert. <br/>Ist in DAVINCI keine ID vorhanden, wird über das Kürzel ausgetauscht.<br/> Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird das Fach hinzugefügt.

### Übernehme Fachtafeln

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**<br/>Fächer der Fachtafel: <br/>   **Kürzel** Unterrichtsart.Kürzel]|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird aktualisiert.<br/> Ist das Kürzel nicht vorhanden wird die Fachtafel hinzugefügt.<br/>Fachtafeln aus MAGELLAN entsprechen Stundentafeln in DAVINCI.

### Übernehme Klassen/Jahrgänge

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Klassenleiter 1**<br/>**Klassenleiter 2**<br/>**Klassenstufe**<br/>**Klassenart **(Kursmodus)<br/>**Anzahl der Schüler**<br/>**Schulnummer**<br/>**Bildungsgang.Kürzel**<br/>**Schulform.Kürzel**<br/>**Schulstelle.Kürzel**|Der Austausch erfolgt über ID und Kürzel.<br/> Bei gleicher ID wird aktualisiert.<br/> Ist in DAVINCI keine ID vorhanden, wird über das Kürzel ausgetauscht.<br/> Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird die Klasse/der Jahrgang hinzugefügt.<br/>Die Anzahl der Schüler wird nur für Oberstufenklassen übernommen.

### Übernehme Schüler

#### Nur der Oberstufe/ Aller Klassen

Felder|Hinweis
---|---
Stammdaten:<br/>**Vorname**<br/>**Nachname **<br/>**MAGELLAN.ID**<br/> **Geschlecht **<br/>**Geburtsdatum **<br/>**Klasse **<br/>**Stufe **<br/>**Tutor **<br/>**Email **<br/>**Schulnummer**<br/><br/>Schülerfächer:<br/>**Fach **<br/>**Fachstatus**<br/> **Unterrichtsart**|Es ist möglich nur einen Teil der Schüler zur Übernahme auszuwählen.<br/> Der Austausch erfolgt über ID, Nachname und Vorname.<br/> Bei gleicher Daten wird aktualisiert.<br/> Schülerfächer werden als Schülerfachwahlen übernommen. Werden Schüler erneut übernommen, werden die eventuell bestehenden Fachwahlen in DAVINCI gelöscht und mit den Daten aus MAGELLAN überschrieben.<br/><br/>Tutor und Klasse, genau wie die Fachwahlen können nur zugeordnet werden, wenn die zugrunde liegenden Daten in DAVINCI vorhanden sind (Lehrer.Kürzel, Klassen.Kürzel, Fach.Kürzel, Unterrichtsart.Kürzel, Fachstatus.Kürzel).

!!! info "Hinweis"

	Als Oberstufenklasse gelten Klassen mit der Klassenart (`MAGELLAN: Klassen > Daten > Klassenart`) "Oberstufenjahrgang (Nur Kurse)" oder "Oberstufenjahrgang (Grund- und Leistungskurse)"  mit dem Jahrgang 11-13 (`MAGELLAN: Klassen > Zeiträume > Zeitraum > Jahrgang`) .

## DAVINCI → MAGELLAN

Wenn Sie eine leere MAGELLAN-Datenbank mit Daten aus DAVINCI füllen möchten, müssen in MAGELLAN mindestens ein Mandant und ein Zeitraum eingerichtet sein.

### Schritte zum Übernehmen

Um Daten von DAVINCI nach MAGELLAN zu übertragen, gehen Sie bitte folgendermaßen vor:  

1. Klicken Sie im Menüband von `DAVINCI` des Programmfensters auf die Schaltfläche `Plan`.
2. Wählen Sie im Planmenü den Befehl `Importieren und Exportieren`: der Assistent „Import/ Export-Assistent“ wird geöffnet.
3. Markieren Sie auf der ersten Assistentenseite im Bereich „Import“ den Eintrag „Nach MAGELLAN exportieren.“
4. Bestätigen Sie Ihre Auswahl mit `Weiter`.
5. Geben Sie im erscheinenden Dialogfenster „MAGELLAN-Anmeldung“ Benutzername und Kennwort des Administratorkontos ein und bestätigen Sie Ihre Zugangsdaten mit `OK`: der Assistent „MAGELLAN-Datenaustausch“ wird geöffnet.
6. Bestätigen Sie auf der ersten Seite des Assistenten die Option „Daten aus einer SDTF-Datei nach MAGELLAN schreiben“ mit `Weiter`.
7. Wählen Sie in den Feldern „Übertrage Daten in folgenden Mandanten“ und „Übertrage Daten in folgendem Zeitraum“ den gewünschten Mandanten und Zeitraum aus dem Aufklappmenü. ![Hier wählen Sie den Mandanten und den Zeitraum aus, in den die Daten übertragen werden.](/assets/images/Datenaustausch_mit_magellan/04.png)
8. Bestätigen Sie Ihre Auswahl mit `Weiter`. <br/>
9. Setzen Sie auf der nächsten Assistentenseite den Haken vor den gewünschten Optionen für die Übernahme unterschiedlicher Datenbereiche nach MAGELLAN. ![ Hier wählen Sie die Daten aus, die nach MAGELLAN übertragen werden.](/assets/images/datenaustausch_mit_magellan/05.png)
10. Bestätigen Sie Ihre Auswahl mit `Weiter`.
11. Drücken Sie auf der nächsten Assistentenseite die Schaltfläche `Starten`.

Die Daten werden nun entsprechend der vorgenommenen Einstellungen in die DAVINCI-Datei übertragen. Den Fortschritt des Datenimports können Sie anhand der Meldungen im Dialogfenster „Datei in Schuldatentransferdatei “ erkennen.

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
**Kürzel**<br/>**Nachname**<br/>**Vorname**<br/>**Soll-Berechnung**|Der Austausch erfolgt über ID und Kürzel.<br/> Bei gleicher ID wird aktualisiert. <br/>Ist die ID in MAGELLAN nicht vorhanden, wird hinzugefügt.<br/> Ist in DAVINCI keine ID vorhanden, wird über das Kürzel ausgetauscht. <br/>Bei gleichem Kürzel wird aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird hinzugefügt.

### Übernehme Fächer

Felder|Hinweis
---|---
**ID**<br/>**Kürzel**<br/>**Schlüssel**<br/>**Bezeichnung**<br/>**Kategorie**<br/>**Aufgabenbereich**|Der Austausch erfolgt über ID oder Kürzel. <br/>Hat das Fach eine ID in DAVINCI, so wird ein entsprechendes Fach mit gleicher ID in MAGELLAN gesucht. <br/>existiert ein solches Fach in MAGELLAN, so wird es aktualisiert, andernfalls wird das Fach in MAGELLAN hinzugefügt.<br/>Hat das Fach keine ID in DAVINCI, so wird ein entsprechendes Fach mit gleichem Kürzel in MAGELLAN gesucht. <br/>Existiert ein solches Fach in MAGELLAN, so wird es aktualisiert, andernfalls wird das Fach in MAGELLAN hinzugefügt.

### Übernehme Schülerkurswahlen

Optionen:

* alle Daten
* nur geänderte Daten und Übertrag aus in die Fachwahlen
* nur geänderte Daten/Bestehende Schülerkurswahlen nicht zuvor löschen
* nur geänderte Daten/Fehlende Klassen anlegen

#### Tutor

Wurde der Tutor in DAVINCI unter `Stammdaten > Schüler > Tutor` verändert, wird dieser Wert in MAGELLAN unter `Schüler > Zeugnis > Details > Tutor` aktualisiert.

#### Import ohne weitere Zusatzoptionen

Wenn Sie keine weiteren Zusatzoptionen auswählen, erfolgt die Übernahme der Schülerkurswahlen nach folgender Regel:

Wird der in DAVINCI vorhandene Schüler in MAGELLAN gefunden, so werden diesem Schüler unter Ansicht `„Schüler“ > Zeugnis > Fächer` alle seine bestehenden Einträge gelöscht und diese durch die Werte aus DAVINCI ersetzt. Dabei werden die nachfolgenden Werte

* Fach,
* Unterrichtsart,
* Fachstatus,
* Kursummer und
* Position

in der unter Ansicht `„Schüler“ > Zeugnis > Fächer` pro erkanntem Schüler neu gefüllt. 

Ansicht „Schüler  > Zeugnis > Fächer“ je Schüler|Nach MAGELLAN übernommen|SDTF-Datensatz P1 Feld 
---|---|---
Fach|Neu|Feld 21: Fachkürzel
Unterrichtsart|Neu|Feld 34: Unterrichtsart-Kürzel
Fachstatus|Neu|Feld 35: Fachstatus-Kürzel
Kursummer|Neu|Feld 33: Kursnummer
Position|Neu|Wird automatisch inkrementell errechnet nach der Reihenfolge der importierten Fächer

#### Import mit Zusatzoptionen

##### Import mit „Übertrag auch in die Fachwahlen“

Wenn Sie die Zusatzoption `Übertrag auch in die Fachwahlen` auswählen, werden die Einträge unter Ansicht `„Abitur“ > Fachwahl` pro erkanntem Schüler zusätzlich aktualisiert. 
**Dabei gelten folgende Regeln:** ist das zu übertragende Fach mit seiner Unterrichtsart bereits in der Fachwahl in MAGELLAN vorhanden, so wird die gesamte Fachzeile mit den neuen Werte aus DAVINCI überschrieben. Andernfalls wird eine neue Fachzeile mit den Werten aus DAVINCI eingefügt.

##### Import mit „Bestehende Schülerkurswahlen zuvor nicht löschen“

Wenn Sie die Zusatzoption `Bestehende Schülerkurswahlen zuvor nicht löschen` auswählen, werden die Einträge unter Ansicht `„Schüler“ > Zeugnis > Fächer` pro erkanntem Schüler vor dem eigentliche Import nicht gelöscht. 

Für die Aktualisierung der Einträge unter Ansicht `„Schüler“ > Zeugnis > Fächer` gelten dann folgende Regeln:

 Was|Bedeutung
 ---|---
Ansicht `„Schüler“  > Zeugnis > Fächer`|Es werden folgende Werte aus der Stundenplansoftware nach MAGELLAN übernommen
Fach mit der Unterrichtsart ist bereits vorhanden|- Fachstatus (Schlüssel)<br/>- Kursnummer (<kein Eintrag  >  , 0, 1, 2…)  
Fach mit der Unterrichtsart ist neu |-Fach (Kürzel und Schlüssel)<br/>- Unterrichtsart (Schlüssel)<br/>- Fachstatus (Schlüssel)<br/>- Kursnummer (<kein Eintrag  >  , 0, 1, 2…)<br/>- Position (0, 1, 2…)

Mit der Zusatzoption können Klassen automatisch in MAGELLAN angelegt werden, wenn diese DAVINCI neu angelegt wurden aber noch nicht in MAGELLAN existieren. Der mit aus DAVINCI übertragene Schüler wird aber noch nicht mit seiner Kurswahl importiert, da er zuerst in MAGELLAN angelegt und in diese neue angelegte Klasse in MAGELLAN eingeschult werden muss.

!!! info "Hinweis"

	Klassen wie auch Schüler sollten grundsätzlich in MAGELLAN angelegt sein, da MAGELLAN hierzu das führende System ist.

##### Import mit „Nur geänderte Daten“

Mit der Option `Nur geänderte Daten` werden nur solche die Schüler für den Import berücksichtigt, deren Daten sich zwischen MAGELLAN und der zu importierenden Schuldatentransferdatei in der Kurswahl unterscheiden. Die Unterscheidung erfolgt auf Basis der Unterschiede

Bezeichnung|Inhalt
--|--
erste Variante|**Fachkombinationsnummer**
Programmstellen|`MAGELLAN > Schüler > Zeugnis > Details > Fachkombination`<br/><br/>`MAGELLAN > Schüler > Zeugnis > Details > Tutor`<br/>`DAVINCI > Kursplan > Fachwahl`<br/>`DAVINCI > Kursplan > Schüler > Schlüssel`
Ergebnis|Hat sich die Fachkombinationnummer durch die Fachwahlprüfung geändert, wird diese übertragen und der Tutor übertragen.
zweite Variante| **Unterschied in der Schülerkurswahl**
Programmstellen|`MAGELLAN > Schüler > Zeugnis > Fächer`<br/>`MAGELLAN > Schüler > Zeugnis > Leistungen`<br/>`DAVINCI > Kursplan > Schüler/Fachwahlen`
Ergebnis|Ein Unterschied in der Kombination aus:<br/>* Fach<br/>* Unterrichtsart<br/>* Fachstatus<br/>* Kursummer<br/>* Schwerpunkt<br/>* Merkmal <br/><br/> Hat sich eine Änderung bei den Schülerfachdaten (`Schüler > Zeugnis > Fächer`) ergeben und ist keinem Fach ein Eintrag unter `Leistungen > Endnote1` zugewiesen worden, werden die Fach- und Leistungsdaten des Zeitraums gelöscht und neu mit den Daten aus DAVINCI gefüllt.

!!! danger "Achtung"

	**Bis Version 8.0.4 galt:** Werden die Schülerfächer in MAGELLAN durch den Abgleich gelöscht können zwei Folgeprobleme entstehen.
	
	1. Die Schülerfächer sind die Grundlage für die Halbjahresnoten. Werden die Fächer durch den Übertrag entfernt, werden auch gegebenenfalls bereits erfasste Noten gelöscht.
	2. Für MyMagellan-Dateien werden die Inhalte aus `Schüler > Zeugnis > Fächer` verwendet. Dabei werden die Daten anhand der ID aus der Tabelle SchuelerFachdaten gespeichert. Werden die Fächer in MAGELLAN gelöscht und neu angelegt, wird auch eine neue ID für die Fachzeilen in der Tabelle SchuelerFachdaten vergeben. Damit können die Daten aus den zuvor erzeugten MyMagellan-Dateien nicht mehr zugeordnet werden.

    **Seit Version 8.0.5 gilt:** Die Schülerfachdaten werden nur noch gelöscht, wenn für kein Fach ein Eintrag unter `Leistungen > Endnote1` existiert. Existiert für ein Fach eine Note (Endnote1), bleiben die Schülerfachdaten in MAGELLAN für den Schüler erhalten, der Assistent gibt Ihnen den Schülernamen und die SchülerID in der Meldung mit aus.

#### Übernehme Stundentafeln

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**<br/>Fächer der Stundentafel: <br/>**Fachkürzel**<br/>**Unterrichtsart.Kürzel**|Der Austausch erfolgt über das Kürzel. <br/>Ist das Kürzel bereits vorhanden, wird aktualisiert.<br/> Ist das Kürzel nicht vorhanden wird die Stundentafel hinzugefügt. <br/>Die Fächer werden mit Kürzel und Unterrichtart hinzugefügt.<br/>Stundentafeln in DAVINCI werden als Fachtafeln nach MAGELLAN übertragen. <br/>Dabei gelten folgende Voraussetzungen:<br/>• Fächer in DAVINCI und MAGELLAN müssen identische ID’s und Kürzel haben.<br/>• Unterrichtsarten in DAVINCI müssen die gleichen Kürzel besitzen wie in MAGELLAN.

![ Übernahmeoptionen](/assets/images/datenaustausch_mit_magellan/07.png)

#### Übernehme Lehrer-Unterricht

Bei der Übernahme des Lehrer-Unterrichts aus DAVINCI werden durch den Import der Schuldatentransferdatei nach MAGELLAN aufgrund der Veranstaltungsliste pro Klasse in DAVINCI die Lehrer übernommen. Es werden bei allen Schülern einer Klasse, die Fächer in MAGELLAN haben, die in der Schuldatentransferdatei zugeordneten Lehrer der gleichen Klasse zugeordnet.

Durch die Übernahme des Lehrer-Unterrichts wird pro Schüler unter Ansicht `„Schüler“ > Zeugnis > Fächer` jedem Fach der unterrichtende Fachlehrer aus DAVINCI zugeordnet.

!!! danger "Achtung"

	Bei Veranstaltungszeilen aus DAVINCI, denen mehr als eine Klasse zugewiesen wurde, ist es wichtig, dass diese Veranstaltungen auch eine Blockbezeichnung erhalten um korrekt ausgewertet werden können.

Felder|Hinweis
---|---
**Zugewiesener Lehrer in der Veranstaltungsliste**|<br/>Dabei prüft MAGELLAN nach folgender Regel:<br/><br/>Unterrichtet der Lehrer<br/>- das gleiche Fach mit<br/>- gleichem Fachstatus und<br/>- gleicher Kursnummer in <br/>- der gleiche Klasse,  <br/> so wird er dem Schüler in diesem Fach zugeordnet.

!!! info "Hinweis"

	Der Lehrer-Unterrichts kann nur bei den Schülern in MAGELLAN zuordnet werden, denen bereits Fächer zugeordnet wurden. Die Schülerfächer in MAGELLAN und die Veranstaltungen der Veranstaltungsliste in DAVINCI müssen in Fach, Fachstatus und Unterrichtsart identisch sein.

Ansicht „Schüler > Zeugnis > Fächer“ je Schüler|Nach MAGELLAN übernommen|SDTF-Datensatz U1 Feld
---|---|---
Lehrer|Aktualisieren|Feld 4: Lehrerkürzel

Tabelle 3: Wertübernahme je Schüler nach MAGELLAN wenn der Lehrer-Unterricht übernommen wird in der Schuldatentransferdatei (SDTF)

!!! info "Hinweis"

	Es wird nicht nur der Lehrer-Unterricht der Oberstufe abgeglichen. Die Übernahme des Lehrer-Unterrichts erfolgt nicht nur für die Oberstufen-Klassen, sondern für alle Klassen des gewählte Import-Zeitraums.
	Die Übernahme des Lehrer-Unterrichts und der Schülerkurswahlen kann in einem Importschritt erfolgen.

##### Beifachlehrer im Datenübertrag

!!! info "Hinweis"

	Beim Übertrag der unterrichtenden Fachlehrer von DAVINCI nach MAGELLAN, kann es dazu kommen, dass beim Sonderfall "Beifächer" der verkehrte Kollege zugeordnet wird.

     Es ist logisch nicht anders zu lösen, da es sich **zweimal um die identische Kombination aus Fach, Fachstatus und Unterrichtsart** handelt.

     Gibt es in der Veranstaltungsliste in DAVINCI mehrere Veranstaltungen dieser Kombination mit unterschiedlichen Lehrern, ist es reiner Zufall, welcher Lehrer in MAGELLAN gespeichert. Das Schuldatentraferdatei wird sequenziell abgearbeitet. Kommt DEU/L1 vor DEU/L2 für den Schüler in der Datei vor, wird beim Schüler DEU/L2 in Magellan gespeichert.Man kann es nur lösen, wenn die Haupt- und Beifach getrennte Kürzel haben, also tatsächlich zwei Fächer sind.

#### Übernehme Räume

Felder|Hinweis
---|---
**Kürzel**<br/>**Bezeichnung**|Der Austausch erfolgt über das Kürzel.<br/> Ist das Kürzel bereits vorhanden, wird der Raum aktualisiert. <br/>Ist das Kürzel nicht vorhanden wird der Raum hinzugefügt.
