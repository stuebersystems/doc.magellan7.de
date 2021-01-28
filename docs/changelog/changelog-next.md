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

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## 7.1.23 - 719

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE: Zusätzlich zum kleinen und großen Latinum wurde ein Feld zum Erfassen des mittleren Latinum eingebunden. Das Feld heißt in der Datenstruktur `LatinumMittel` und wird in der Tabelle `SchuelerAbi` gespeichert. In der Oberfläche finden Sie das Feld unter `Abitur > Prüfung > Sprachkenntnisse`.

### MAGELLAN SCHULVERWALTUNG

* FIX: Beim Drucken von Zeugisformularen für Nebenschüler wird der PDF-Export (falls aktiviert) nicht in das Dokumentenverzeichnis des Nebenschülers, sondern in das Dokumentenverzeichnis des Stammschülers abgelegt.

### MYMAGELLAN

* CHANGE: Zeugnisbemerkungen werden in voller Länge aus MAGELLAN übergeben
* FIX: Eingabe von Noten/Punkten über Fächer, korrekter Filter gesetzt
* CHANGE: Ein bereits für die Bearbeitung geöffnete Datei kann nicht erneut geöffnet werden, es erscheint eine Meldung.

### MAGELLAN Schnittstellen

#### NRW

* CHANGE: 

### MAGELLAN ADMINISTRATOR

* CHANGE: 

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

### MAGELLAN Bibliothek

* FIX: 

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: SAR-APO-2018.dws (gemäß Gymnasialen Oberstufe Saar (GOS) vom vom 17. April 2018.)
* NEW: NIE-APO-G9-2018.dws 

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Klassen

FIX: Zeugnisliste nach Schülerfächern (Kopfnoten).rpt

#### Berlin

* FIX: BER-Schul Z 303 (11.19).rpt (Entwertung unter Zeugnisbemerkung entfernt, max. Anzahl von Fächern des Sprachlich-literarisch-künstlerisches Aufgabenfeld (Aufgabenfeld I): auf 8 erhöht)
* FIX: BER-Schul Z 350 (10.07).rpt (eingebrachte Kurshalbjahre werden entsprechend der Eintragung der Halbjahre unter `Abitur > Qualifikation` im Feld "eingebrachte Halbjahre" auf dem Bericht ausgelesen
* Fix: BER-KO-AS (Schul Z 320a-b)(03.11).rpt (Tendenznoten werden ausgegeben)

#### Saarland

* NEW: SAR-GY-ABI (GOS2.0).rpt
* NEW: SAR-GY-AZ (GOS2.0).rpt
* NEW: SAR-GEMS-AS (Klasse 9 mit Prüfung)(ab 2021).rpt
* NEW: SAR-GEMS-AS (Klasse 9 ohne Prüfung)(ab 2021).rpt

#### Niedersachsen

* NEW: NIE-GY-ABI (2021).rpt
