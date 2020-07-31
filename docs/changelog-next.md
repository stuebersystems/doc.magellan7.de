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

    Bitte beachten Sie, dass mit der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## 7.1.15 - 715

### Datenstruktur

* NEW:

### MAGELLAN SCHULVERWALTUNG

* FIX:

### MAGELLAN Schnittstellen

* FIX: 

### MAGELLAN ADMINISTRATOR

* FIX: 

### MyMAGELLAN-CENTER

* FIX: 

### MyMAGELLAN

### MAGELLAN Bibliothek

* FIX: Problem bei der Rückgabe von Büchern behoben

![Meldung bei der Ausleihe eines mit "Dauerverleih" markierten Exemplares](/assets/images/changelog/7.1.14.01.png)

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: 

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Baden Württemberg

* NEW: BAW-GY-HJZ (Kursstufe mit BLL).rpt (Halbjahreszeugnisse der Kursstufe mit Ausgabe der Besonderen Lernleistung, Fach RELIGION / ETHIK wird nun im Bereich der gesellschaftswissenschaftlichen Fächer mit ausgegeben)
* NEW: BAW-GY-ABI (2019 mit KF-LK).rpt (Abiturzeugnis gültig ab Abitur 2019)
* NEW: BAW-GY-JZ (Mittelstufe).rpt
* NEW: BAW-GY-JZ (Mittelstufe mit GER)(A5).rpt (Jahreszeugnis für die Mittelstufe mit Ausgabe der Sprachreferenz, DIN A5)
* CHANGE: BAW-GY (Mitteilung Prüfungsergebnisse).rpt (Ausgabe Schuljahr)

#### Sachsen

* NEW: SAC-BVJ-HJI (A.01.03).rpt (A.01.03 Halbjahresinformation der Berufsschule - Berufsvorbereitungsjahr)
* CHANGE: SAC-BS-HJI (A.01.02).rpt
* CHANGE: SAC-BVJ-AS mit HS (A.01.09).rpt (Hauptschulabschluss wird nun beim `Schüler > Laufbahn > Abschluss` im Bereich „Abschluss1“ im Feld „Abschlussart“ abgefragt. Grundlage bildet das `Schlüsselverzeichnis > Abschlussarten`.)
* CHANGE: SAC-BF-JZ (B.02.02).rpt
* CHANGE: SAC-BS-BVB Maßnahme (A.01.05).rpt
* CHANGE: SAC-BS-HJI (A.01.04).rpt
* CHANGE: SAC-BS-AS (Vorbereitungsklasse) (A.01.06).rpt
* CHANGE: SAC-BS-JZ (A.02.01).rpt
* CHANGE: SAC-BS-JZ (A.02.01) 2spaltig.rpt