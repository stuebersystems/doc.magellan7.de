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

    Bitte beachten Sie, dass mit der letzten Version das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` aud die Dateiendung .mymx an.

## 7.1.11 - 713

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!


### MAGELLAN

* CHANGE: `Bewerber > Bewerbungsdaten > Fachdaten > Externe Prüfung der Fremdsprache(n)` Aus der Checkbox wurde eine Werteliste mit den Werten `bereits absolviert` und `angestrebt` eingefügt. 
* CHANGE: `Bewerber > Bewerbungsdaten > Verfahren > Einschätzung` Die Benennung der rechten Spalte wurde von `Bewerber` in `Kollegiat/in` geändert.

### MAGELLAN Administrator

* FIX: 
  
### MyMAGELLAN-CENTER

* FIX: 

### MyMAGELLAN

* FIX: 

### MAGELLAN Bibliothek

* FIX: 

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Mecklenburg Vorpommern

* CHANGE:  

#### Sachsen

* FIX: SAC-BG-ABI (E.01.06).rpt (Zeugnisbemerkungen aus dem Menü Abitur > Zeugnisbemerkungen werden nun im Bericht angezeigt, Ausgabe der Fachrichtung des Schülers erweitert. Für die Ausgabe der Fachrichtung müssen Sie entweder das Berufsfeld einer Klasse definieren oder das des Schülers.)
* FIX: SAC-FOS-AZ (D.01.03).rpt (Umbruch bei den Fachbezeichnungen im Pflichtbereich korrigiert)

#### Niedersachsen

* FIX: NIE-GY (Studienbuch - Einführungsphase) G9.rpt (m Bereich Sport wird nun die Null beim Punktwert vorangestellt, Wahlb-Fächer werden wieder korrekt nur im Bereich der Wahlfächer ausgegeben)

### Auslandsschule

* FIX: DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt (Korrektur Seite 2, Ausgabe Schüler/In, Anpassungen gemäß der Vorgaben *Handreichungen für die Sekundarstufe I an Deutschen Schulen im Ausland für Zeugnisse und Statistik
(Beschluss des Bund-Länder-Ausschusses vom 25.09.2019)*)
* NEW: DAS-GY-ABI (DIA)(2020)(keine mdl. Prüfung möglich).rpt

### Nordrhein Westfalen

* CHANGE: 

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: Zeugnisse\Berlin\BER-RS-AS (Schul Z 241)(07.10).rpt