# Voraussichtliche Änderungen

Sie erhalten hier einen Überblick über die voraussichtlichen Änderungen und Korrekturen für das nächste Serviceupdate. Die nachfolgend gelisteten Änderungen wurden noch nicht veröffentlicht.

## LEGENDE

Abkürzung | Bedeutung
--------- | ---------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

---

!!! danger "Achtung"

    Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

!!! danger "Achtung"

    Bitte beachten Sie, dass mit der letzten Version das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` aud die Dateiendung .mymx an.

## 7.1.11 - 713

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* NEW: Tabelle `Leistungsarten` 
* NEW: SchuelerAbiDetails: 
  *  `HJ1_Leistungsart` bis `HJ6_Leistungsart`
  *  `HJ1_Bestanden` bis `HJ6_Bestanden`
  *  NEW: Schuelerfachdaten: `Leistungsart`

### MAGELLAN

* NEW: Schlüsselverzeichnis `Leistungsarten` mit Arten (Schriftlich, mündlich, praktisch) und gleichnamiges Feld unter `Schüler > Zeugnis > Leistungen`.
  * Dieses Feld wird für die Oberstufe in NRW benötigt. Man legt sich seine Arten der Leistung an (Beispiel Vortrag, Klausur usw) und markiert sie mit der korrekten Art (Beispiel: Klausur = schriftlich). Bei den Schülern wird unter `Schüler > Zeugnis > Leistungen` jedes Fach mit der vom Schüler gewählten Leistungsart markiert. Diese Leistungsart wird je Kurshalbjahr beim Synchronisieren der Daten mit ins Menü `Abitur > Qualifikation` übernommen. Die Leistungsart wird nur für benotete Fächer übernommen.
* NEW: Unter `Abitur > Qualifikation` kann je Fach und Kurshalbjahr der Kurs als bestanden markiert werden. Diese Eingabe ist für die Oberstufe in NRW gedacht.

* CHANGE: `Bewerber > Bewerbungsdaten > Fachdaten > Externe Prüfung der Fremdsprache(n)` Aus der Checkbox wurde eine Werteliste mit den Werten `bereits absolviert` und `angestrebt` eingefügt. 
* CHANGE: `Bewerber > Bewerbungsdaten > Verfahren > Einschätzung` Die Benennung der rechten Spalte wurde von `Bewerber` in `Kollegiat/in` geändert.

* FIX: Unter `Extras > Schlüsselverzeichnisse > Fächer` kann ein versehentlich erfasster `Aufgabenbereich` entfernt werden.
* FIX: Import SchuelerOnline
* FIX: `Schüler > Laufbahnprozess > Schüler einschulen` bei der Kopie eines Schülers wird beim Einschulen die Herkunftsschule aktualisiert
* FIX: Bei der Änderung eines Schlüsselverzeichnisses während der Bereich `Schüler > Zeugnis` geöffnet war, erschien eine Meldung 
* FIX: Problem beim Synchronisieren von Schülern in die Berufsschulmatrix behoben (`Synchronisiere BBS.dws`)

### MAGELLAN ADMINISTRATOR

* FIX: Reihenfolge beim Einlesen der Dateien aus dem MAGELLAN Importformat korrigiert

### Skripte

* CHANGE: `Importe SDTF.dws` Beim Übertrag von Schülerkurswahlen (`nur geänderte Daten`) von DAVINCI nach MAGELLAN werden die Schülerfachdaten in MAGELLAN nicht mehr geändert, wenn die Fachkombinationsnummer in DAVINCI verändert wurde. Bitte beachten Sie die angepasste Dokumentation: [Abgleich mit DAVINCI: Schülerkurswahlen mit der Option "nur geänderte Daten" ](https://doc.magellan7.stueber.de/schulverwaltung/howto/abgleich_mit_dav/#import-mit-nur-geanderte-daten)
* CHANGE: `Synchronisiere Abi.dws`: Beim Synchronisieren der Schülerdaten wird für benotete Fächer der Eintrag aus `Schüler > Zeugnis > Leistungen > Leistungsart` übernommen. 

* FIX: `Importe SDTF.dws` Problem beim Zuordnen von P1-Daten beim Übertrag aus DAVINCI nach MAGELLAN (Schülerkurswahlen) behoben.
* FIX: `Schüler > Daten 1 > Familie` - Die Anzeige des `Verhältnis` zeigt jetzt zusätzliche Verhältnisse an
* FIX: `Sorgeberechtigte > Arbeitgeber` - Schaltflächen werden jetzt korrekt aktiviert
* FIX: `Klassen > Zeiträume > ENBREA Leistungsprofile > Dialogfenster Kurse definieren`  - Die Überschriften wurden überarbeitet, der blaue Hintergrund entfernt

### Skripte

* FIX: `Importe SDTF.dws` Problem beim Zuordnen von P1-Daten beim Übertrag aus DAVINCI nach MAGELLAN (Schülerkurswahlen) behoben.
* CHANGE: `Importe SDTF.dws` Beim Übertrag von Schülerkurswahlen (`nur geänderte Daten`) von DAVINCI nach MAGELLAN werden die Schülerfachdaten in MAGELLAN nicht mehr geändert, wenn die Fachkombinationsnummer in DAVINCI verändert wurde. Bitte beachten Sie die angepasste Dokumentation: [Abgleich mit DAVINCI: Schülerkurswahlen mit der Option "nur geänderte Daten"](https://doc.magellan7.stueber.de/schulverwaltung/howto/abgleich_mit_dav/#import-mit-nur-geanderte-daten)
* CHANGE: `Synchronisiere Abi.dws`: Beim Synchronisieren der Schülerdaten wird für benotete Fächer der Eintrag aus `Schüler > Zeugnis > Leistungen > Leistungsart` übernommen.
  
* FIX: BER-APO-KO-2017.dws: Anpassungen für MAGELLAN 7
* FIX: `Synchronisiere BBS.dws`

### Schnittstellen

* NEW: SAC - SAXSVS - Schnittstelle um Import erweitert. Dokumentation zu finden unter [Import von Daten aus SaxSVS nach MAGELLAN](https://doc.ls.stueber.de/sachsen/import_saxsvs/)
* NEW: SAC - SAXSVS - Schnittstelle um Exportdatei mit  Abgängern/Abschlüssen erweitert
* CHANGE: SAC - SAXSVS - Export der Betriebedaten auch, wenn nur Ausbildungs- oder Praxisbetrieb angegeben wurde.
* FIX: SAC - SAXSVS - Detailverbesserungen und Sonderfälle beim Export berücksichtigt
* NEW: SHL - Schulstatistik Schnittstelle 2020/2021 freigegeben

### MAGELLAN-Skripteditor

* CHANGE: überarbeitete Version

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

* FIX:

### MAGELLAN Bibliothek

* FIX: Löschen von Exemplaren funktioniert wieder

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Mecklenburg Vorpommern

* CHANGE:  

#### Sachsen

* FIX: SAC-BG-ABI (E.01.06).rpt (Zeugnisbemerkungen aus dem Menü Abitur > Zeugnisbemerkungen werden nun im Bericht angezeigt, Ausgabe der Fachrichtung des Schülers erweitert. Für die Ausgabe der Fachrichtung müssen Sie entweder das Berufsfeld einer Klasse definieren oder das des Schülers.)
* FIX: SAC-FOS-AZ (D.01.03).rpt (Umbruch bei den Fachbezeichnungen im Pflichtbereich korrigiert)

#### Niedersachsen

* FIX: NIE-GY (Studienbuch - Einführungsphase) G9.rpt (m Bereich Sport wird nun die Null beim Punktwert vorangestellt, Wahlb-Fächer werden wieder korrekt nur im Bereich der Wahlfächer ausgegeben)

### Auslandsschule

* FIX: DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt (Korrektur Seite 2, Ausgabe Schüler/In, Anpassungen gemäß der Vorgaben *Handreichungen für die Sekundarstufe I an Deutschen Schulen im Ausland für Zeugnisse und Statistik
(Beschluss des Bund-Länder-Ausschusses vom 25.09.2019)*)
* NEW: DAS-GY-ABI (DIA)(2020)(keine mdl. Prüfung möglich).rpt

### Nordrhein Westfalen

* CHANGE: 

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: Zeugnisse\Berlin\BER-RS-AS (Schul Z 241)(07.10).rpt
* CHANGE: Zeugnisse\Berlin\Schleswig-Holstein\SHL-GY-AS (Klasse 5-10)(G8).rpt