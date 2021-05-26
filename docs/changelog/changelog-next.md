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

### 8.0.8 ()

#### MAGELLAN Schulverwaltung

* FIX: `Schüler > Daten1 > Familie` Neuanlage eines Sorgeberechtigten korrigiert

#### Schnittstellen

* NEW: 

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik, Fehlermeldung wenn ein Prüfungsergebnis fehlt
* FIX:  DE-DIAP-2018 diverse Korrekturen in der Vorschlagsautomatik,Fehlermeldung wenn ein Prüfungsergebnis fehlt

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

### 7.1.30 - 720

#### MAGELLAN Schulverwaltung

* FIX: Das Kürzel im Verzeichnis `Einschulmerkmale` wurde auf 20 Zeichen erhöht

#### Skripte

* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen mit der Option `nur geänderte Daten` aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 
* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik, Fehlermeldung wenn ein Prüfungsergebnis fehlt
* FIX:  DE-DIAP-2018 diverse Korrekturen in der Vorschlagsautomatik,Fehlermeldung wenn ein Prüfungsergebnis fehlt

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 250 Co (04.21).rpt
* NEW: BER-Schul Z 306 (04.21)(FG).rpt
* NEW: BER-Schul Z 306 (04.21).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt
* NEW: BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.21).rpt
