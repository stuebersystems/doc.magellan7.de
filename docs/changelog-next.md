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

## 7.1.3 - 710

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE: Umstellen des Feldes "Sites" auf Memofeld zur besseren Speicherung der Opac-Daten.

!!! warning "Wichtig"

    Bei der Umstellung gehen bisherige Opac-Server verloren und müssen neu eingetragen werden. Eine Anleitung finden Sie [hier](https://doc.magellan7.stueber.de/bibliothek/tutorial/opac/).

* CHANGE: Korrigieren der Feldlängen für die Eingabeparameter der Prozeduren.  
* CHANGE: Neues setzen der SchuelerZeitraumID in der Tabelle "SchuelerZeugnisbemerkungen".
* CHANGE: Setzen von Bewerberinformationen aus dem Stammschüler bei kopierten Bewerbern.

### MAGELLAN

* FIX: Bei der Übernahme eines Schüler zum Bewerber wird das "alte" Bewerbungsziel sowohl unter `Bewerber > Daten 1 > Für Ziel 1 als auch unter Bewerber > Auswahlliste > Bewerbungsziel 1`
* FIX: Ein unter `Schüler > Ausbildung` neu angelegter Praktikumsbetrieb wird auch gleich als neuer Praktikumsbetrieb für den Schüler übernommen.

### MAGELLAN Willkommensassistent

* FIX: Verbindungseingabe beim Anlegen von Verbindungen zu einer entfernten Datenbank überarbeitet

### MAGELLAN Bericht

CHANGE:das Modul wurde aktualisiert

### MAGELLAN Administrator

* FIX:

### MyMAGELLAN-CENTER

* CHANGE:

### MyMAGELLAN

* NEW: Eingabe der Leistungen per Ziffernblock und Pfeiltasten möglich
* FIX: Sortierung von Umlauten korrigiert
* CHANGE: Fachansicht: Die zuletzt gewählte Sortierung wird beim Wechsel zum nächsten Datensatz für die neue Liste wieder ausgeführt
* CHANGE: Schüleransicht: Die zuletzt gewählte Sortierung wird beim Wechsel zum nächsten Datensatz für die neue Liste wieder ausgeführt
* CHANGE: Beim Start einer MyMAGELLAN-Datei wird die Beurteilungsart der Fächeransicht standardmäßig mit der Auswahl `Alle Beurteilungsarten` voreingestellt. 
  
### MAGELLAN Bibliothek

* CHANGE: Die Opac-Funktionalität wurde überarbeitet

### Skripte

* NEW: SAR-APO-2018.dws (diverse Korrekturen)
* FIX: SAR-APO-2017.dws (diverse Korrekturen)

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* NEW: DAS-GY-AZ mit FHR (Anlage 9b).rpt
* NEW: NIE-GY (Studienbuch - Einführungsphase) G9.rpt
* FIX: DAS-GY-ABI (DIA)(2019).rpt
* NEW: DAS-GY-ABI (DIA)(2020).rpt

### Neu Berichte für Berlin

* NEW: BER-Schul Z 620 (09.18).rpt (Beiblatt zum Zeugnis für ergänzende Bemerkungen (09.18), Bitte beachten Sie, dass Sie dieses Formular gesondert ausgedruckt werden muss. Die Zeugnisbemerkung muss in MAGELLAN das Merkmal "Beiblatt" erhalten)

![Zeugnisbemerkungen](/assets/images/changelog/7.1.3.01.png)

Folgende Berichte wurden um den Bemerkungstext zum Beiblatt Schul Z 620 ergänzt.

* NEW: BER-Schul Z 250 (11.19).rpt
* NEW: BER-Schul Z 351 (11.19)_Oberstufe.rpt
* NEW: BER-Schul Z 351 (11.19)_Kolleg.rpt
* NEW: BER-Schul Z 306 (11.19)(FG).rpt
* NEW: BER-Schul Z 306 (11.19).rpt
* NEW: BER-Schul Z 301 (11.19).rpt
* NEW: BER-Schul Z 300 (11.19).rpt
* NEW: BER-Schul Z 302 (11.19).rpt
* NEW: BER-Schul Z 303 (11.19).rpt

!!! info "Hinweis"
  
      Die Ausgabe des Bemerkungstextes: "Ein Beiblatt (Schul Z 620) ist Bestandteil dieses Zeugnisses:     ☐ ja     ☐ nein)." wird wie folgt gesteuert: Liegt eine Zeugnisbemerkung mit dem Merkmal "Beiblatt" beim Schüler vor, kommt der Text in der Bemerkung: “Ein Beiblatt (Schul Z 620) ist Bestandteil dieses Zeugnisses.” Liegt dieses Merkmal nicht vor, kommt der Text in der Bemerkung: “Ein Beiblatt (Schul Z 620) ist nicht Bestandteil dieses Zeugnisses.”