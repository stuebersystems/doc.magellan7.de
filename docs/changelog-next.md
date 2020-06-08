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

    Bitte beachten Sie, dass mit der letzten Version das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung .mymx an.

## 7.1.12 -

### Datenstruktur

### MAGELLAN

* FIX: `Betriebe > Auswahl > Betriebe zusammenführen`Anzeige der korrekten Datensätze
* FIX: `Schüler > Daten 1 > Familie` Anzeige des Verhältnisses
* FIX: `Bewerber > Daten 1` beim Anlegen eines neuen Sorgeberechtigten, wird die Gemeindekennziffer vorbelegt
* FIX: Nebenschüler mit Ausbildungsbtriebe werden als Auszubildende beim Betrieb angezeigt

### MAGELLAN ADMINISTRATOR

* FIX: `Datenaustausch > Kataloge importieren` 00_Raeume.keys importierbar

### Skripte

* FIX: SHL-APO-2018: Anpassung Fachanforderungen Sport: kaufmännische Rundung nur am Schluss: ((schr. Note des 3. Prüfungsfaches x 2) plus Note1 (Fachpraxis) plus Note2 (Fachpraxis)) geteilt durch 4.
* FIX: SAC-APO-BGY-2017: Mit den Änderungen durch Artikel 2 der Verordnung vom 24. Juli 2018 entfällt jegliche Unterscheidung nach den Fachrichtungen.Somit muss in MAGELLAN im Schlüsselverzeichnis > Verordnungen auch nicht mehr der Wert für "Typ" eingetragen werden.

### Schnittstellen

### MAGELLAN-Skripteditor

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

* FIX: Installationspaket vervollständigt, bei reinen MyMAGELLAN-Installationen erschien beim Eintrag von Schülerbemerkungen eine Meldung, die auf eine fehlende Datei hinwies.

### MAGELLAN Bibliothek

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Mecklenburg Vorpommern

* CHANGE:  

#### Berlin

* NEW: BER-Schul Z 255 (2019.2020).rpt
* FIX: BER-Schul Z 256 (2019.2020).rpt
* FIX: BER-GY (Abi-18a - Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.12).rpt
* FIX: BER-GY (abi_4_berechnungsbogen)(10.16).rpt

#### Sachsen

* FIX:

#### Niedersachsen

* FIX:

### Auslandsschule

* FIX:

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: