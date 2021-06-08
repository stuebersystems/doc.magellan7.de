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

### **8.0.9 801 ()**

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!
     Die Datenbankversionsnummer wird hierbei diesmal nicht erhöht, sondern bleibt auf der auf der Datenbankversion 801.

#### Anpassung

* CHANGE: Inhalte aus dem bis zur Version MAGELLAN 7 genutzten Feld `Schüler/Bewerber > Merkmal > Bemerkung` werden kopiert und als Datensatz in der Liste unter `Schüler/Bewerber > Merkmal > Bemerkungen` als Eintrag ergänzt. Der Inhalt des nicht mehr genutzten Feldes `Bemerkung` wird im Anschluss gelöscht.

#### Schnittstellen

* FIX: [BER] Problem beim Erstellen der Abiturdatenstatistik behoben

#### Skripte

* CHANGE: `Schüler fortschreiben`Strikteres Vorgehen beim Schüler fortschreiben; beim finden des SchülerZeitraum Datensatzes wird auch Gewechselt Status berücksichtigt. 
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: DE-DIAP-2015 diverse Korrekturen
* FIX: DE-DIAP-2018 diverse Korrekturen
* FIX: Schüler fortschreiben: Korrektur bei leeren Datenmengen (SchuelerKlassen)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, unsortiert).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, sortiert).rpt

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 255 (2020.2021).rpt
* NEW: BER-Schul Z 256 (2020.2021).rpt

##### Sachsen

* FIX: SAC-BS-AS (A.02.04).rpt (Berechnung Durchschnittsnote)
* CHANGE: SAC-BF-AS (A.02.07).rpt
* CHANGE: SAC-BF-AS (B.04.05).rpt
* CHANGE: SAC-BF-AZ (B.03.04).rpt
* CHANGE: SAC-BS-AS (A.02.05) 2spaltig.rpt
* CHANGE: Zertifikat (F.01.09).rpt

##### Auslandsschulen

CHANGE: DAS-GY-AZ ohne FHR (Anlage 9a).rpt
CHANGE: DAS-GY-AZ mit FHR (Anlage 9b).rpt


### **7.1.30 - 720**

#### MAGELLAN Schulverwaltung

* FIX: Das Kürzel im Verzeichnis `Einschulmerkmale` wurde auf 20 Zeichen erhöht

#### Skripte

* CHANGE: `Schüler fortschreiben`Strikteres Vorgehen beim Schüler fortschreiben; beim finden des SchülerZeitraum Datensatzes wird auch Gewechselt Status berücksichtigt. 
* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen mit der Option `nur geänderte Daten` aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 
* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik, Fehlermeldung wenn ein Prüfungsergebnis fehlt
* FIX:  DE-DIAP-2018 diverse Korrekturen in der Vorschlagsautomatik,Fehlermeldung wenn ein Prüfungsergebnis fehlt

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, unsortiert).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, sortiert).rpt

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 250 Co (04.21).rpt
* NEW: BER-Schul Z 306 (04.21)(FG).rpt
* NEW: BER-Schul Z 306 (04.21).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt
* NEW: BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.21).rpt
* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 255 (2020.2021).rpt
* NEW: BER-Schul Z 256 (2020.2021).rpt

##### Sachsen

* FIX: SAC-BS-AS (A.02.04).rpt (Berechnung Durchschnittsnote)
* CHANGE: SAC-BF-AS (A.02.07).rpt
* CHANGE: SAC-BF-AS (B.04.05).rpt
* CHANGE: SAC-BF-AZ (B.03.04).rpt
* CHANGE: SAC-BS-AS (A.02.05) 2spaltig.rpt
* CHANGE: Zertifikat (F.01.09).rpt

##### Auslandsschulen

CHANGE: DAS-GY-AZ ohne FHR (Anlage 9a).rpt
CHANGE: DAS-GY-AZ mit FHR (Anlage 9b).rpt