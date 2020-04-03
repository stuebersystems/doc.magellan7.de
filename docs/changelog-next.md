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

## 7.1.9 - 712

### MAGELLAN

* NEW: Für den Seriendruck `An den Betrieb des Schülers` wurden die Felder `Bildungsgang` und `Beruf` übergeben, damit kann innerhalb von Word nach Datensätzen  eines Bildungsgangs/Berufs gefiltert werden
* NEW: Für den Seriendruck `An den Betrieb des Bewerbers` wurden die Felder `Bildungsgang` und `Beruf` übergeben, damit kann innerhalb von Word nach Datensätzen  eines Bildungsgangs/Berufs gefiltert werden
* CHANGE: Spalte Bildungsgang wurde aus der Auswahlliste Schüler entfernt, damit wird eine Performanceverbesserung erzielt
* FIX: `Fachdaten kopieren` beim `Schüler versetzen`
* FIX: `Bewerber > Daten2`: Dateneingabe und dann Auswahl `nächster Datensatz` Fehlermeldung korrigiert
* FIX: `Schüler > Daten2 Abschluss` volle Zeichenlänge des Kürzels kann genutzt werden
* FIX: unter `Abitur > Qualifikation` ist das Feld `Abiturjahrgang` wieder gefüllt und auswählbar 
* FIX: Unter `Schueler > Daten2 > Abschluss` können Werte verwendet werden, für die unter `Extras > Schlüsselverzeichnisse > Abschlüsse (extern)` die volle Kürzellänge verwendet wurde

## SAXSVS

* CHANGE: 

### MAGELLAN Administrator

* FIX: Datapump (Datenübertragung von MAGELLAN 6 nach MAGELLAN 7) optimiert

### MyMAGELLAN-CENTER

* CHANGE: 

### MyMAGELLAN

* FIX: In der Ansicht  `Fächer` und  `Schüler` sind die Felder `schriftl.Note1` - `Endnote (gesamt)` beschreibbar.
* CHANGE: in der Ansicht `Schüler` und `Fächer` wird die Spalte `Kurs` eingeblendet, die das Fachkürzel plus die Kursnummer ausgibt.

### MAGELLAN Bibliothek

* CHANGE: Sämtliche Optionen in der Bibliothek sind von den Benutzern mit den Bibliothekts-Rechtegruppen `Schulleitung`, `Bibliothekar` oder dem `sysdba` anpassbar. Benutzer mit den Bibliotheks-Rechtegruppen `Kollegium` oder `Gast` können keine Änderungen vornehmen, sondern die Einstellungen nur ansehen. Bitte beachten Sie den neuen Abschnitt [Optionen](https://doc.magellan7.stueber.de/bibliothek/installation/optionen/).

### Skripte

* FIX: 

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* CHANGE:
  
#### Mecklenburg Vorpommern

* CHANGE:  MVP-GY-AS (Jahrgangsstufe 7-10).rpt

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: Berichte\Zeugnisse\Berlin\BER-GES-MSA (Schul Z 202)(02.08).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-FOS-MSA (Schul Z 512).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-FOS-HJZ (Schul Z 510)(05.06).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-FOS-AZ (Schul Z 513)(05.06).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-FHReife-Bescheinigung (Schul Z 350)(10.07).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BVJ-HJZ (Schul Z 505 b)(BQL FL).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BVJ-AZ (Schul Z 507 a)(BGL VZ).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BV-AS (Schul Z 508).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-AZ (Schul Z 503).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-AS (Schul Z 501).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-AS (Schul Z 500).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-AS (MSA  Schul Z 502c).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-AS (MSA  Schul Z 502).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BQL VZ-HJZ (Schul Z 505 a).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BQL VZ-FL-TZ (Schul Z 505 a-b-c).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BQL TZ-AZ (Schul Z 507 c).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BOS-AZ (Schul Z 534)(03.05).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BOS-AS (Schul Z 533)(03.05).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BFS-HJZ (Schul Z 520b)(07.09).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BFS-AZ (Schul Z 523a).rpt
* CHANGE: Berichte\Zeugnisse\Niedersachsen\NIE-GY-FHReife (Bescheinigung).rpt
* CHANGE: Berichte\Zeugnisse\Niedersachsen\NIE-GY (Studienbuch - Einführungsphase) G9.rpt
* CHANGE: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 3-4).rpt
* CHANGE: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 1-2).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-RS-AZ.rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-RS-AS.rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Mittelstufe).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Mittelstufe mit Beurteilung).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Klasse5).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Mittelstufe).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 13).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 12).rpt
* CHANGE: Berichte\Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 11).rpt
