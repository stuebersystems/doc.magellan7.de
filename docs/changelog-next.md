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

## 7.1.14 - 714

### Datenstruktur

### MAGELLAN SCHULVERWALTUNG

* FIX: Unter `Schüler > Zeugnis > Details` werden für `Verhalten` und `Mitarbeit` Noten und Füllwerte gezeigt.
* NEW: NRW: Unter `Schüler > Zeugnis > Leistungen` gibt es das Feld `Bestanden`. In dem Feld ist festhaltbar, ob der Kurs bestanden, nicht bestanden oder nicht belegt wurde. Diese Eingabe wird beim Synchronisieren der Daten mit ins Menü `Abitur` übergeben und je Halbjahr (E1-Q4) abgebildet. Bitte beachten Sie den Abschnitt ["Bestanden" und "Leistungsart"](https://doc.magellan7.stueber.de/schulverwaltung/howto/Oberstufe/sync/#bestanden-und-leistungsart) im Kapitel [Schüler synchronisieren](https://doc.magellan7.stueber.de/schulverwaltung/howto/Oberstufe/sync/)
* FIX: `Schüler > Daten4` neue Fahrtstrecke kann gespeichert werden

### MAGELLAN Schnittstellen

FIX: SAXSVS: Problem beim Ausspielen der Förderschwerpunkte für Schüler mit IDIntern behoben.

### MAGELLAN ADMINISTRATOR

* FIX: Beim Übertrag von MAGELLAN 6 nach MAGELLAN 7 wird die Datenstruktur 674 erwartet 

### MyMAGELLAN-CENTER

* FIX: Mym-Datei mit mit pauschalem Kennwort erstellen

### MyMAGELLAN

### MAGELLAN Bibliothek

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: `Synchronisiere Abi` wurde angepasst, es werden die Daten aus dem Feld `Bestanden` (aus Schüler > Zeugnis > Leistungen) mit ins Abitur synchronisiert

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: SAC-FS-AS mit FHReife (C.01.06).rpt (automatische Durchschnittsnoteberechnung korrigiert, die Durchschnittsnote ergibt sich aus allen Zeugnisnoten mit Ausnahme der Fächer Sport, Religion und Ethik sowie mit Ausnahme aller nachrichtlich ausgewiesenen Fächer (Noten))
