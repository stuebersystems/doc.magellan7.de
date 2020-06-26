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

#### MAGELLAN Berichte

* NEW: Das Modul `MAGELLAN Berichte` fällt weg, die Dokumentation der Berichte erfolgt ab dieser Version ausschließlich im Bereich Berichte der Dokumentation [Landesanpassung unter https://doc.la.stueber.de/berichte/01_uebersicht/](https://doc.la.stueber.de/berichte/01_uebersicht/)!

### MAGELLAN ADMINISTRATOR

* FIX: `Datenaustausch > Kataloge importieren` 00_Raeume.keys importierbar

### Skripte

* FIX: SHL-APO-2018: Anpassung Fachanforderungen Sport: kaufmännische Rundung nur am Schluss: ((schr. Note des 3. Prüfungsfaches x 2) plus Note1 (Fachpraxis) plus Note2 (Fachpraxis)) geteilt durch 4.
* FIX: SAC-APO-BGY-2017: Mit den Änderungen durch Artikel 2 der Verordnung vom 24. Juli 2018 entfällt jegliche Unterscheidung nach den Fachrichtungen. Somit muss in MAGELLAN im `Schlüsselverzeichnis > Verordnungen` auch nicht mehr der Wert für "Typ" eingetragen werden. Das Skript berücksichtigt, dass die 2. Fremdsprache nicht mehr zwingend belegt werden muss. Beim Markieren werden nur 26 GKs (zuvor 28 GKs) gekennzeichnet. 
Aktualisierte Beschreibung zum Skript unter https://doc.la.stueber.de/11.sac/sac-apo-bgy-2017/.

### Schnittstellen

### MAGELLAN-Skripteditor

### MyMAGELLAN-CENTER

* FIX:

### MyMAGELLAN

* FIX: Installationspaket vervollständigt, bei reinen MyMAGELLAN-Installationen erschien beim Eintrag von Schülerbemerkungen eine Meldung, die auf eine fehlende Datei hinwies.

### MAGELLAN Bibliothek

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie ab sofort im Bereich "Berichte" der Dokumentation [Landesanpassung unter https://doc.la.stueber.de/berichte/01_uebersicht/](https://doc.la.stueber.de/berichte/01_uebersicht/)

#### Mecklenburg Vorpommern

* CHANGE:  

#### Berlin

* NEW: BER-Schul Z 255 (2019.2020).rpt
* FIX: BER-Schul Z 256 (2019.2020).rpt (Versetzungsart)
* FIX: BER-GY (Abi-18a - Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.12).rpt (Ausgabe Punktsumme 5 PK und Note für PK, Seite 2: Da im 4. und 5. Prüfungsfach keine Nachprüfungen möglich, wird auf Seite 2 in der 2. und 3. Tabelle im 4. PF (Spalte 2) das Ergebnis der absolvierten Prüfung ausgegeben, ebenso steht die Gesamtpunktzahl für diese Prüfungen fest und wird nun auch in Spalte 3 genauso wie bei der 5. PK ausgegeben)
* FIX: BER-GY (abi_4_berechnungsbogen)(10.16).rpt
* FIX: BER-Schul Z 300 (11.19).rpt (Versetzungsvermerk korrigiert, wird ein Schüler nicht versetzt, gibt des Zeugnis "Nicht versetzt...." aus)
* FIX: BER-Schul Z 306 (11.19).rpt (Leerzeichen auf Seite 4 in der Formel N = 5 2/3 eingefügt, fehlerhafte Linien enternt, Punktsumme aus 24 Grundkursen in einfacher Wertung korrigiert, wenn eines der Prüfungsfächer BLL oder PRS ist)
* FIX: BER-Schul Z 306 (11.19)(FG).rpt (Leerzeichen auf Seite 4 in der Formel N = 5 2/3 eingefügt, fehlerhafte Linien entfernt, Punktsumme aus 24 Grundkursen in einfacher Wertung korrigiert, wenn eines der Prüfungsfächer BLL oder PRS ist)

#### Sachsen

* FIX: SAC-BG-ABI (E.01.06).rpt (`Schüler > Daten 3 > 1./2./3./4. Fremdsprache`, haben Sie im Menü `Schüler > Daten 3` keine 2 Fremdsprache hinterlegt, wird folgender Satz unter den Bemerkungen auf dem Zeugnis unterdrückt: *"Das in *ZWEITE FREMDSPRACHE* erreichte Sprachniveau entspricht der Stufe <B1/B2> des Gemeinsamen europäischen Referenzrahmens."*)
* FIX: SAC-BS-AS (A.02.05).rpt (Formel zur Ausgabe der Berufsbezeichnung (männlich/weiblich) überarbeitet)
* FIX: SAC-BS-JZ (A.02.01).rpt (Fehltage unentschuldigt, hat ein Schüler "0", wird eine Entwertung auf dem Zeugnis ausgegeben "----")
* FIX:SAC-BG-JZ (E.01.02).rpt (Fehltage unentschuldigt, hat ein Schüler "0", wird eine Entwertung auf dem Zeugnis ausgegeben "----")
* FIX: SAC-FO-JZ (D.01.02).rpt (Zeilenumbruch Pflichtunterricht korrigiert)
* NEW: SAC-BF-JZ (B.02.02).rpt (B.02.02 Jahreszeugnis der Berufsfachschule)

#### Saarland

* NEW: SAR-FHReife (Nachweis)(GOS2.0) Zweitschrift.rpt
* NEW: SAR-FHReife (Nachweis)(GOS2.0).rpt
* NEW: SAR-GEMS-AS (Klasse 9 ohne Prüfung)(ab 2020).rpt
* NEW: SAR-GEMS-AS (Klasse 9 mit Prüfung)(ab 2020).rpt

#### Niedersachsen

* FIX:

### Auslandsschule

* FIX:

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: