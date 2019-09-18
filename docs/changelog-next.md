# Voraussichtliche Änderungen

Sie erhalten hier einen Überblick über die voraussichtlichen Änderungen und Korrekturen für das nächste Serviceupdate. Die nachfolgend gelisteten Änderungen wurden noch nicht veröffentlicht.

## LEGENDE

Abkürzung | Bedeutung
--------- | ---------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

---

## 7.0.19 - 708

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstrukturänderung

* FIX: Fehlende Trigger für die Ansicht "MedizinDaten" hinzugefügt. Damit können diese wieder bearbeitet werden.

### MAGELLAN

FIX: SAXSVS Export Leerzeichen in Namen werden nicht mehr in die XMl Datei übergeben

### MAGELLAN Bibliothek

* FIX: Anzeige der Daten in Ansicht `Medien > Exemplare` Felder `Zustand` und `Kataloge` wurde korrigiert.

### Skripte  

### MAGELLAN Administrator

### Statistik

* FIX: SIM.TXT - LSSchulform wurde nicht korrekt ausgelesen. Das führte zu Leereinträgen in der Spalte.
* FIX: NRW - SIM.TXT - LSKlassenart wurde nicht ausgespielt, sondern nur ausgelesen. Das führte bei den Datensatzsarten: "Neuzugang" und "Neuzugang an gleicher Schule" dazu, dass eine Spalte in der Zeile fehlte.
* FIX: NRW - SIM.TXT - Adressmerkmal wird zwar nicht benötigt wurde aber auch nicht als Leerfeld (Nur Trennzeichen) ausgespielt.
* FIX: NRW - SIM.TXT - Die Kopfzeilen für Adressmerkmal und Internat am Ende der SIM.TXT haben gefehlt
* CHANGE: NRW - SIM.TXT - Die beiden Spalten `Produktname` und `Produktversion` dienen lediglich Supportzwecken. Beide Informationen wurden in die Spalte Produktname verschoben. In der Spalte `Produktversion` geben wir jetzt die Datensatzart aus, dies hilft dem Support bei der Suche nach Problemlösungen.
* CHANGE: NRW - SIM.TXT - Kein Fehler aber eine Eingabehilfe. Einige Kunden geben keine Versetzungart ein, sondern setzen lediglich das Merkmal Versetzt. Wir tragen dem Folge und berechnen entsprechend die Versetzung anders als zuvor. Nachzulesen in der Dokumentation unter [SIM.TXT - Dateneingabe - Feld "Versetzung"](https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/#dateneingabe).

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: Klassenlehrerliste mit Räumen (Variante 2).rpt 
* FIX: Klassenlehrerliste mit Räumen.rpt 
