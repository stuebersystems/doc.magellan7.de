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

### 8.0.6

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstruktur

* NEW: Neue Felder unter `Schüler > Daten 2` (Dokumentation [hier](https://doc.magellan7-toolbox.stueber.de/datenstruktur/version8/tabellen/Schueler/))
  * HoechsterAbschluss2ABS
  * HoechsterAbschluss2ABSSchulform
  * HoechsterAbschluss2BBS
  * HoechsterAbschluss2BBSSchulform

#### MAGELLAN Schulverwaltung

CHANGE: Die Anordnung der Felder unter `Schüler > Daten 2` wurde verändert

#### Schnittstellen

* NEW: SAXSVS => Schüler, die im vergangenen Jahr einen Abschluss an Ihrer Schule absolvierten und im aktuellen Schuljahr einen neuen Bildungsgang belegen, werden in der Abgängerdatei und in der Datei der aktuellen Schüler ausgegeben. Da in beiden Dateien Daten über die bisher erworbenen Abschlüsse ABS oder BBS und die Abschlussschulformen erwartet werden, gibt es unter `Schüler > Daten2` eine neue Aufteilung und auch neue Felder. Bitte erfassen Sie in den Feldern unter "Höchster Abschluss ABS/BBS (mitgebracht)" die Daten, die der Schüler aus Sicht des Vorjahres mit an die Schule brachte oder zuvor erworben hatte. Bitte erfassen Sie in den neuen Feldern unter "Höchster Abschluss ABS/BBS (erworben)" ggfs. Abschlüsse, die der Schüler inzwischen an Ihrer Schule erworben hat. 
Wir geben für die Abgängerdatei die Einträge aus dem Bereich "Höchster Abschluss ABS/BBS (mitgebracht)" aus. Für die Datei der aktuellen Schüler geben wir die Daten aus dem Bereich "Höchster Abschluss ABS/BBS (erworben)" aus, steht dort kein Wert, werden die Inhalte aus den Feldern "Höchster Abschluss ABS/BBS (mitgebracht)" ausgespielt.

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/).

* CHANGE: 

#### Berichte

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 250 Co (04.21).rpt
* NEW: BER-Schul Z 306 (04.21)(FG).rpt
* NEW: BER-Schul Z 306 (04.21).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt

### 7.1.30 - 720

#### Skripte

* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen mit der Option `nur geänderte Daten` aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 

#### Berichte

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 250 Co (04.21).rpt
* NEW: BER-Schul Z 306 (04.21)(FG).rpt
* NEW: BER-Schul Z 306 (04.21).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt