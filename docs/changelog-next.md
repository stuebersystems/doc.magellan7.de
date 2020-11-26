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

## 7.1.21 - 716

### Datenstruktur

* CHANGE: SchuelerZeitraeume.BU um Statistikadmin als Recht erweitert
* CHANGE: Constrain für Dienstbez ergänzt

### MAGELLAN SCHULVERWALTUNG

* FIX: Sammelzuweisung unter `Schüler > Zeugnis > Details`
* FIX: Emailversand aus `Extras > Benachrichtigungen` korrigiert

### MYMAGELLAN

* CHANGE: Filteransicht `Fächer`/`Schüler`: Spaltenposition und Gruppierungen bleiben bei Datensatzwechsel innerhalb der Ansicht erhalten (nicht bei Ansichtswechsel). Bei der Ansicht `Schüler` gibt es noch die Besonderheit, dass die Spalte `Kurs` immer die erste Spalte ist.

### MAGELLAN Schnittstellen

#### NRW

* CHANGE: 

### MAGELLAN ADMINISTRATOR

* CHANGE: 

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

### MAGELLAN Bibliothek

* FIX: Exportieren von Dokumenten nach `C:\Users\Public\Documents\Stueber Systems\Magellan 7\Dokumente\Schueler\SchuelerID\Bibliothek` korrigiert
* CHANGE: STRG+D für den Aufruf des Dokumenteverzeichnisses im Menü `Schüler` ergänzt

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE:

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: SAR-GEMS-HJZ-JZ (Klasse 5-10).rpt wurde Für MAGELLAN 7 angpasst
* FIX: SAR-GY-ABI (GOS2.0).rpt (Ausgabe Seminarfach, Sprachniveau)
* NEW: Schülerbericht "KV09b_Masernschutz.rpt", Anleitung unter [https://doc.la.stueber.de/berichte/02_schueler/#kv09b-masernschutzrpt](https://doc.la.stueber.de/berichte/02_schueler/#kv09b-masernschutzrpt)
* FIX: BAW-BG-ABI (DIN A4 doppelseitig 2018 - Abschrift).rpt
* FIX: BAW-BG-ABI (DIN A4 doppelseitig 2018).rpt
* FIX: BAW-BG-ABI (DIN A4 doppelseitig 2018 - Neuausstellung).rpt
* NEW: BAW-BG-ABI (DIN A4 doppelseitig 2021 - Abschrift).rpt
* NEW: BAW-BG-ABI (DIN A4 doppelseitig 2021).rpt
* NEW: BAW-BG-ABI (DIN A4 doppelseitig 2021 - Neuausstellung).rpt