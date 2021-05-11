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

### 8.0.5

#### Allgemein

* NEW: Zum MSI-Paket für 32-Bit-Betriebssysteme gibt auf unserer Webseite eine eigene UpdatenInfo-Datei. Die installierte MAGELLAN-Version fragt aus der Registry den Wert je nach verwendetem Installationpaket ab (für Windows 32 Bit oder Windows 64 Bit) und greift auf geeignete UpdateInfo-Datei zu.

#### MAGELLAN Schulverwaltung

FIX: Die Funktionalität `Fahrstrecken` wurde überarbeitet

#### MAGELLAN Administrator

* FIX: Benutzer anlegen korrgigiert
* CHANGE: Beim Anlegen eines neuen Benutzers sind die Häkchen auf der Unterkarte `Ansichten` vorbelegt

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/).

* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 
* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik
* NEW:  DE-DIAP-2018 

### 7.1.30 - 720

#### Skripte

* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 