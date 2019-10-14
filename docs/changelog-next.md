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

## 7.0.21 - 708

### MAGELLAN

* CHANGE: SAXSVS: Für Sorgeberechtigte, die in der Schweiz wohnen, können Sie im Feld `Land` das Kürzel CH eingegeben, MAGELLAN übergibt diese Ausgabe dann als Schlüssel 158 in die Exportdatei.
* FIX: Wenn im Menü Sorgeberechtigte die Postleitzahl oder der Ort eingegeben werden und mit TAB oder ENTER bestätigt wird, wird das Feld Gemeinde entsprechend der hinterlegten Schlüssels befüllt.
* FIX: Ist die Postleitzahl oder der Ort beim Sorgeberechtigten nicht eindeutig, wird bei der Wahl eines Wertes aus dem Unterfenster auch die Gemeindekennziffer befüllt.
* CHANGE: Wird beim Schüler die Adresse geändert und für die Sorgeberechtigten soll die Änderung auch übernommen werden, wird auch die Gemeinde des Schülers für die Sorgeberechtigten übernommen.
* FIX: Bei der Übernahme einer Adressänderung eines Schülers, wird für den Sorgeberechtigten auch das Land korrekt befüllt.

### MAGELLAN Administrator

* FIX: Datenübernahme 6 => 7: Die Tabelle `Sponsoren` und das gleichnamige Feld in der Tabelle `Betriebe` wurden ergänzt

### MAGELLAN Bibliothek

* FIX:

### Skripte

* FIX: Schüler wechseln.dws => Beim Wechsel wird die aktuelle Ausbildung korrekt übernommen

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX:
