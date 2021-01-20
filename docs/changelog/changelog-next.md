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

## 7.1.23 - 718

### Datenstruktur

* CHANGE:

### MAGELLAN SCHULVERWALTUNG

* FIX: 

### MYMAGELLAN

* CHANGE: Zeugnisbemerkungen werden in voller Länge aus MAGELLAN übergeben
* FIX: Eingabe von Noten/Punkten über Fächer, korrekter Filter gesetzt

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

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: BER-Schul Z 303 (11.19).rpt (Entwertung unter Zeugnisbemerkung entfernt, max. Anzahl von Fächern des Sprachlich-literarisch-künstlerisches Aufgabenfeld (Aufgabenfeld I): auf 8 erhöht)
* FIX: BER-Schul Z 350 (10.07).rpt (eingebrachte Kurshalbjahre werden entsprechend der Eintragung der Halbjahre unter `Abitur > Qualifikation` im Feld "eingebrachte Halbjahre" auf dem Bericht ausgelesen
* NEW: SAR-GY-ABI (GOS2.0).rpt
* NEW: SAR-GY-AZ (GOS2.0).rpt
