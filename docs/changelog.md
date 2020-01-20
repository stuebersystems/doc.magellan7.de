# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN 7. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan7.stueber.de/changelog/](https://doc.mymagellan7.stueber.de/changelog/).
Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN 6.

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier: [2019](changelog2019.md)

* Was wir für die nächste Ausgabe planen, sehen Sie im Kapitel ["Voraussichtliche Änderungen"](changelog-next.md).

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

!!! danger "Achtung"

    Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

## 7.1.3 - 710 (08.01.2020)

### MAGELLAN

* FIX: Bei der Übernahme eines Schüler zum Bewerber wird das "alte" Bewerbungsziel sowohl unter `Bewerber > Daten 1 > Für Ziel 1 als auch unter Bewerber > Auswahlliste > Bewerbungsziel 1`
* FIX: Ein unter `Schüler > Ausbildung` neu angelegter Praktikumsbetrieb wird auch gleich als neuer Praktikumsbetrieb für den Schüler übernommen.
* FIX: Beim Einschulen von Nebenschülern (also Stammschülern mit einer Nebenlaufbahn) wird der `ZugangAm` unter `Daten2` nicht verändert. Im Assistenten wird darauf hingewiesen.
* FIX: `Schüler > Zeugnis > Leistungen`: Note für Schüler1 eingeben und über die Pfeile zu Schüler2 wechseln speichert die Note
* FIX: `Extras > Schlüsselverzeichnisse > Zeugnisbemerkungen > Bemerkung`: bereits erfasste Texte sind editierbar
* FIX: `Extras > Schlüsselverzeichnisse > Zeugnisbemerkungen > Bemerkung`: Zeilenhöhe auf 5 erhöht, vertikaler Scrollbalken im Editiermodus
* FIX: Beim Einschulen von Vagabunden aus dem Vagabundenfilter heraus (aufgeschlagene Registerkarte `Ausbildung`) wird nach dem Einschulen die Ansicht korrekt aktualisiert.
* CHANGE: Anzeige der eingetragenen Wertes aus dem Feld `Schüler > Daten 4 > Bafög` in der Auswahlliste als Checkbox.
* FIX: Mehrere Durchläufe des Assistenten `Schüler ausschulen` wieder möglich

### MAGELLAN Willkommensassistent

* FIX: Verbindungseingabe beim Anlegen von Verbindungen zu einer entfernten Datenbank überarbeitet

### MAGELLAN Bericht

CHANGE: Das Modul wurde aktualisiert

### MyMAGELLAN

* NEW: Eingabe der Leistungen per Ziffernblock und Pfeiltasten möglich
* FIX: Sortierung von Umlauten korrigiert
* CHANGE: Fachansicht: Die zuletzt gewählte Sortierung wird beim Wechsel zum nächsten Datensatz für die neue Liste wieder ausgeführt
* CHANGE: Schüleransicht: Die zuletzt gewählte Sortierung wird beim Wechsel zum nächsten Datensatz für die neue Liste wieder ausgeführt
* CHANGE: Beim Start einer MyMAGELLAN-Datei wird die Beurteilungsart der Fächeransicht standardmäßig mit der Auswahl `Alle Beurteilungsarten` voreingestellt. 

### Skripte

* NEW: SAR-APO-2018.dws (diverse Korrekturen)
* FIX: SAR-APO-2017.dws (diverse Korrekturen)
* FIX: DE-DIAP-2015.dws Vorschlagsautomatik korrigiert (Einbringunsgverpflichtung mind. 2 HJ in Naturwissenschaften, optimale Punktzahl)
* FIX: `Synchronisiere Abi.dws`: Geänderte Auswertung des Eintrags aus `Extras > Schlüsselverzeichnisse > Verordnungen > Jahrgang` (10, 11 oder leer) 

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* NEW: DAS-GY-AZ mit FHR (Anlage 9b).rpt
* NEW: NIE-GY (Studienbuch - Einführungsphase) G9.rpt
* FIX: DAS-GY-ABI (DIA)(2019).rpt
* NEW: DAS-GY-ABI (DIA)(2020).rpt
* NEW: SHL-GY-ABI (2018).rpt

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

