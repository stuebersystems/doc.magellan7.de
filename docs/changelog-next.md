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

## 7.1.10 - 712

### MAGELLAN

* NEW:
* CHANGE:
* FIX: Fertigstellen-Button im `Extras > Exporte > Untis` wird aktiviert  
* FIX: Beim Anlegen eines neuen Bewerbers, wird die Anzeige der Herkunftsschule unter `Daten2` korrekt aktualisiert.
* FIX: Anzeigbare Kürzellänge korrigiert für:
  * `Bewerber > Höchster Abschluss ABS > Abschluss`
  * `Bewerber > Höchster Abschluss ABS > Bildungsgang`
  * `Bewerber > Höchster Abschluss BBS > Abschluss`
  * `Bewerber > Höchster Abschluss BBS > Beruf`
  * `Bewerber > Höchster Abschluss BBS > Bildungsgang`
  * FIX: Bearbeiten von `Schüler > Zeugnis > ENBREA Leistungen`und `Schüler > Zeugnis > ENBREA Kurse` mit Kollegiums, Sekretariats- und Schulleitungsrechten möglich

### MAGELLAN Administrator

* FIX: Synchronisiere Zugriffsrechte.dws Fehlermeldung "Mit Fehlern abgeschlossen" bei korrektem Durchlauf entfernt
* FIX: Zuweisen von Zugriffsrechten.dws `Klassen > Klassen übernehmen` mit dem Recht Schulleitung 1 und Mandanten Administrator

### MyMAGELLAN-CENTER

* FIX: MyMagellan Dateien werden zum Einlesen korrekt (mym7 oder mymx) erkannt

### MyMAGELLAN

* FIX: Anzeige der Inhalte der Verzeichnisfelder unter `Schüler > Zeugnisdaten korrgiert`
  * CHANGE: Die Anzeige der `Beurteilungsarten` unter `Fächer` ist angepasst worden. Statt des Drop-Downfeldes, sind jetzt Radio-Buttons verwendet worden, die dem Benutzer die gefilterte Darstellung der Liste nach der Beurteilungsart verdeutlichen. Bitte beachten Sie die angepasste Dokumentation unter [https://doc.mymagellan7.stueber.de/noteneingabe/#eingabe-nach-fachern](https://doc.mymagellan7.stueber.de/noteneingabe/#eingabe-nach-fachern)
* CHANGE: Beim Öffnen der Ansicht `Fächer` ist wie bisher die Vorauswahl so getroffen, dass alle Schülerzeilen zum Fach gezeigt werden. In dieser Ansicht ist kein Editieren möglich. Bitte wählen Sie vor der Eingabe der Ergebnisse die gewünschte Beurteilungsart aus.


### MAGELLAN Bibliothek

* FIX: Problem beim Übernehmen von Personen als Ausleiher behoben

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Mecklenburg Vorpommern

* CHANGE:  

#### Sachsen

* FIX: SAC-FOS-FHReife (D.01.04).rpt (weitere Zeugnisbemerkungen werden wieder korrekt ausgegeben)

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: 