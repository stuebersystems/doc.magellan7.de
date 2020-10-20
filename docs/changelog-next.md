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

## 7.1.19 - 715

### MAGELLAN SCHULVERWALTUNG

* FIX: Anlegen eines neuen Sorgeberechtigten aus `Schüler > Daten1` und `Bewerber > Daten1`
* FIX: Anlegen eines neuen Sorgeberechtigten aus `Schüler > Daten1` und `Bewerber > Daten1`  wenn keine Gemeindekennziffern und Postleitzahlen im Verzeichnis vorhanden sind
* CHANGE: Die Größe des Schülerfehlzeiten-Fenster kann verändert werden
* FIX: Unter `Schüler > Laufbahn > Allgemein` wurde die Anzeige der Bezeichnungen der Verzeichnisfelder überarbeitet
* FIX: Unter `Schulen > Daten` werden Änderungen beim Datensatzwechsel oder Ansichtswechsel gespeichert
* FIX: Sammelzuweisung unter `Schüler > Laufbahn > Allgemein/Abschluss` überarbeitet
* FIX: Sammelzuweisung unter `Schüler > Zeugnis > Details` überarbeitet
* NEW: Beim Seriendruck an Sorgeberechtigte vom Schüler aus kann auf das Feld Ergänzungen (`Sorgeberechtigte > Daten > Ergänzungen`) mit dem Seriendruckfeld «Sorgebe_Adresszusatz» zugrgriffen werden
* NEW: Unter `Schüler/Bewerber/Lehrer/Personen/Sorgeberechtige/Mandanten/Betriebe/Schulen > Daten > PLZ` können auch Postleitzahlen erfasst werden, die nicht im Verzeichnis Postleitzahlen gespeichert wurden oder die dort gespeichert wurden, für die aber kein Verweis auf eine passende Gemeindekennziffer existiert
* CHANGE: Unter `Berufsschule > Matrix > Sammelzuweisung` wird standardmäßig das Häkchen zum `Fächer kopieren` nicht gesetzt angezeigt
* NEW: Wenn Betriebe gelöscht werden sollen, erscheint ein Fenster, das die Möglichkeiten bietet aus der markierten Auswahl alle Betriebe zu löschen oder nur die Betriebe, denen keine Auszubildenden zugeordnet wurden. Wird ein Betrieb gelöscht, dem Auszubildende zugeordnet waren, bleibt die Schülerausbildung (`Schüler > Ausbildung`) bestehen, wenn hier weitere Informationen hinterlegt wurden (bspw. Bildungsgang, Beruf usw.)
* FIX: Unter `Schüler > Merkmal > MerkmalA1` können Merkmale genutzt werden, die bis zu 20 Zeichen im Feld Kürzel verwenden.
* FIX: Anzeigeverhalten des Feldes und der Verzeichnisliste `Schüler/Bewerber > Daten2 > Bereits besuchte Schule > letzte Klassenstufe` korrigiert
* FIX: `Menü Bewerber > Register Bewerber > Sammelzuweisung > Ausbildungsdaten`: Ein neuer oder geänderter Ausbildungsdatensatz wird unter `Bewerber > Ausbildung` als aktuelle Ausbildung gesetzt
* FIX: Schreibfehler im benutzerdefinierten Filter korrigiert
* FIX: `Schüler > Daten2 > Bereits besuchte Schulen > Herkunftsschule`: Die Auswahl einer neuen Herkunftsschule wird beim Wechsel in ein anderes Register gespeichert

### MAGELLAN Schnittstellen

#### NRW

* CHANGE: Für Berufskollegs: Wenn der Schüler nicht Status `Neuzugang von einer anderen Schule` hat und keine `Versetzungsart` gewählt ist, wird immer eine `0` ausgegeben, auch wenn die Versetzung nicht gefüllt ist.

### MAGELLAN ADMINISTRATOR

* CHANGE: `Benutzerverwaltung > Zugriffsrechte synchronisieren` Der Assistent endet mit `Schließen`.

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

### MAGELLAN Bibliothek

* CHANGE: Geändertes Verfahren zur Erstellung von Barcodes
* NEW: Im Menü `Mahnwesen` stehen für den Seriendruck der Name und die Adressdaten des Schülers zur Auswahl. Alle verfügbaren Seriendruckfelder je Menüpunkt listen wir hier auf: [https://doc.magellan7.stueber.de/bibliothek/tutorial/referenzen/](https://doc.magellan7.stueber.de/bibliothek/tutorial/referenzen/)
* FIX: Ausleihe ohne Bestätigung unterbunden
* FIX: Buchung falscher Medien unterbunden

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE:

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: NRW-ABI-AZ  (Anlage D42).rpt (Korrektur Ausbildung zeitraumbezogen)
* NEW: BER-Schul Z 251 (11.19).rpt (Schul Z 251 – Zeugnis des Gymnasiums, Jahrgangsstufen 5 und 6 – (11.19))

