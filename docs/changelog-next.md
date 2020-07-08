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

    Bitte beachten Sie, dass mit der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung .mymx an.

## 7.1.13 - 714

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* NEW: Tabelle SchuelerFachdaten: `Durchschnitt` 
* NEW: Tabelle SchuelerFachdaten:

### SchuelerOnline

* INFO: Wir haben SchuelerOnline gemeldet, dass aktuell die beiden Felder Schulnr und Schulbez nicht korrekt übergeben werden. Es wird in Kürze in SchuelerOnline angepasst, bis dahin passen Sie bitte die Spaltenköpfe für dem Import per Hand an.

Verkehrt|Korrekt
--|--
Schulnummer|**Schulnr**
Schulbezeichnung|**SchulBez**

* FIX: `NRW > Import > SchuelerOnline > Betriebe aktualisieren`: Die Funktion wurde aktualisiert
* CHANGE: HTML-Breaks (`<br/>`) werden beim Einlesen aus SchülerOnline-Dateien ignoriert

### MAGELLAN

* CHANGE: Aus der Filterung der Schülerauswahliste nach Vagabunden steht `Rechtsklick > Status` nicht mehr zur Verfügung
* FIX: Rechtegruppe Kollegium5: Änderungen der Laufbahn werden auch beim Weiterschalten zum nächsten Datensatz gespeichert.
* FIX: Problem beim Anlegen `Unterpunkten` im Verzeichnis `Fächer (Themen)`behoben 

### MAGELLAN BIBLIOTHEK

* FIX: Passbilder, die für bereits als Medienausleiher angelegte Schüler in der Schulverwaltung aktualisiert wurden, werden auch in der Anzeige in der Bibliothek angepasst
* FIX: Klasse und Klassendaten werden nach Änderung in der Schulverwaltung auch für die Bibliothek übergeben.    

#### Statistik

* NEW: ABS-Nordrhein-Westfalen Statistikmodul 2020. Beachten Sie bitte die aktualisierten Schlüsselverzeichnisse und die aktualisierte Dokumentation ["Statistikdokumentation für NRW"](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/).

#### MAGELLAN Berichte

* NEW: 

### MAGELLAN ADMINISTRATOR

* FIX:

### Skripte

* NEW: BER-BFS-Matrix-2016 (Dokumentation hier: https://doc.la.stueber.de/03.ber/ber-bfs-matrix-2016dws/)
* NEW: BER-IBA-HJ-2020 (Dokumentation hier: https://doc.la.stueber.de/03.ber/ber-iba-hj-2020dws/)
* BER-IBA-AS-2020 (Dokumentation hier: https://doc.la.stueber.de/03.ber/ber-iba-as-2020dws/)

### Schnittstellen

### MAGELLAN-Skripteditor

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

* FIX: 

### MAGELLAN Bibliothek

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie ab sofort im Bereich "Berichte" der Dokumentation [Landesanpassung unter https://doc.la.stueber.de/berichte/01_uebersicht/](https://doc.la.stueber.de/berichte/01_uebersicht/)

* FIX: SAC-FS-JZ (C.01.02).rpt

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: