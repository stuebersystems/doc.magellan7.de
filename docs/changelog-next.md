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

## 7.1.1 - 709


### MAGELLAN

* NEW: 

* CHANGE: 

* FIX: 

### MAGELLAN Administrator

* FIX: Datenübernahme 6 => 7: Die Tabelle `Sponsoren` und das gleichnamige Feld in der Tabelle `Betriebe` wurden ergänzt
* CHANGE: Das MAGELLAN-Importformat wurde an die Datenstruktur von MAGELLAN 7 angepasst. Bitte lesen hierzu die aktualisierte [Dokumentation](https://doc.magellan7-toolbox.stueber.de/importe/)!
* CHANGE: Das Skript hinter der Funktion `Synchronisiere Zugriffsrechte` wurde optimiert

### MAGELLAN Bibliothek

* FIX: `Ausleihe > Sammelaktion > Klassensatz auswählen` und Ausleiher auswählen
* NEW: Wenn im Medienfilter ein Wert eingegeben wird, der zu einer leeren Liste führen würde, dann wird eine entsprechende Meldung ausgegeben.
* CHANGE: Im Medienfilter wird nach dem erneuten Aufruf das zuletzt gewählte Filterkriterium gezeigt.
* CHANGE: Die Titelzeilen in den Menüpunkten wurden überarbeitet und den Titelzeilen in MAGELLAN angeglichen (Beispiel: Menü `Lieferant`, Anzeige des in der Liste ausgewählten Lieferanten am oberen Fensterrand)
* CHANGE: Seriendruck aus dem Menü `Mahnwesen` überarbeitet
* CHANGE: `Datenbank > Optionen > Autoupdate`: Anzeige überarbeitet

### Skripte

* FIX: Schüler wechseln.dws => Beim Wechsel wird die aktuelle Ausbildung korrekt übernommen

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: DAS-Zeugnis Gymnasium - Mittlerer Schulabschluss (Anlage 10)(§23).rpt
* FIX: DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt
* FIX: DAS-GY-ABI (DIA)(2019).rpt
* FIX: DAS-GS (Klasse 1-2).rpt
* FIX: DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt (ergänzt um das Feld "Ausbilder" im Bereich der Ausbildung)
* FIX: Schulbescheinigung für die Vergangenheit.rpt
* FIX: Schulbescheinigung (Vergangenheit mit Klasse).rpt
* FIX: Schulbescheinigung (mit Klasse und vorauss. Ende zweifach).rpt
* FIX: Schulbescheinigung (mit Klasse und vorauss. Ende einfach).rpt
* FIX: RLP-GES-JZ (Klassen 5 und 6).rpt
* FIX: RLP-GES-HJZ (Klassen 5 und 6).rpt
* FIX: RLP-GES-HJZ (Klassen 7-10).rpt
* FIX: Schülerpersonalblatt (mit Vorbildung).rpt
