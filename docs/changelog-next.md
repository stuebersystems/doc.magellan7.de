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
* FIX: Filterbezeichnungen korrigiert
* FIX: Die Zugriffsrechte für das Modul `Abitur` (damit für das Erfassen der schriftlichen Prüfungsnoten) wurden für die Rechtegruppen Schulleitung1, Sekretariat1 erweitert. Zusammengefasst haben hier Änderungsrechte: Kollegium5, Schulleitung1, Sekretariat1 und der sysdba. Bitte führen Sie das Synchronieren der Zugriffsrechte im MAGELLAN Administrator unter `Benutzerverwaltung > Menüleiste "Zugriffsrechte synchronisieren"` aus um die Rechte für bestehende Benutzerkonten zu erweitern.
* FIX: `Abitur > Prüfungen`: Wenn das Häkchen für "Lernleistungen einbringen" als letzte Aktion vor dem Auslösen der Berechnung gesetzt wird, wird es durch die Aktion des Berechnens nicht deaktiviert.

### MAGELLAN Schnittstellen

* FIX: SAXSVS: Problem beim Ausspielen der Förderschwerpunkte für Schüler mit IDIntern behoben.
* CHANGE: Hinweise,  wie mit erneut auftauchenden Schülern im Import umgegangen wird, überarbeitet: [https://doc.ls.stueber.de/sachsen/import_saxsvs/#prufung-von-schulerdaten](https://doc.ls.stueber.de/sachsen/import_saxsvs/#prufung-von-schulerdaten)

### MAGELLAN ADMINISTRATOR

* FIX: Beim Übertrag von MAGELLAN 6 nach MAGELLAN 7 wird die Datenstruktur 674 erwartet 

### MyMAGELLAN-CENTER

* FIX: Mym-Datei mit mit pauschalem Kennwort erstellen

### MyMAGELLAN

### MAGELLAN Bibliothek

* FIX: Beim Versuch eines mit "Dauerverleih" markierten Buches wird die nachfolgende Meldung ausgegeben. Exemplare können per Sammelzuweisung über das Feld "Bestandsstatus" mit `Dauerverleih` (Sie haben das Buch in eine andere Bibliohtek ausgeliehen) oder als `Dauerleihgabe` (Sie haben das Buch dauerhaft aus einer anderen Bibliothek ausgeliehen) markieren.

![Meldung bei der Ausleihe eines mit "Dauerverleih" markierten Exemplares](/assets/images/changelog/7.1.14.01.png)

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: `Synchronisiere Abi` wurde angepasst, es werden die Daten aus dem Feld `Bestanden` (aus Schüler > Zeugnis > Leistungen) mit ins Abitur synchronisiert

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: SAC-FS-AS mit FHReife (C.01.06).rpt (automatische Durchschnittsnoteberechnung korrigiert, die Durchschnittsnote ergibt sich aus allen Zeugnisnoten mit Ausnahme der Fächer Sport, Religion und Ethik sowie mit Ausnahme aller nachrichtlich ausgewiesenen Fächer (Noten))
