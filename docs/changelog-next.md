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

## 7.1.6 - 711

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE:  Änderungen von Bewerbungsdaten müssen sich auf den kopierten Bewerber auswirken.

### MAGELLAN

* CHANGE: Unter `Schüler > Ausbildung` wird in der Filterung `Vagabunden` die Leiste "aktueller Ausbildungsbetrieb/akuteller Praxisbetrieb" gezeigt
* CHANGE: Wechselt man von Auswahlliste in eine Datenkarte und zurück, sind die Gruppierungen im Anschluss so geöffnet oder geschlossen wie zuvor
* FIX: Problem beim Fortschreiben von Schülern mit gruppierter Liste (doppelter Eintrag des Schülerzeitraums) gelöst
* FIX: Problem bei Schülern (Eintrag unter `Schüler > Zeugnis > Details`), die mehrfach innerhalb des selben Zeitraums die selbe Klasse besuchen gelöst
* FIX: erneuten Fortschreiben (`Laufbahnprozesse > Schüler fortschreiben`) wird die "Weiter"-Schaltfläche aktiv
* FIX: Bei der Übernahme eines Schüler zum Bewerber wird das "alte" Bewerbungsziel sowohl unter `Bewerber > Daten 1 > Für Ziel 1 als auch unter Bewerber > Auswahlliste > Bewerbungsziel 1`
* FIX: Wechselt man im Schülermenü auf einer Datenkarte mit den Tastenkombination `STRG+BildAuf` oder `STRG+BildAb` wird der nächste Datensatz auch beim Wechsel über einen Gruppierungskopf in der Auswahlliste korrekt gezeigt
* FIX: Zeugnis als PDF exportieren aus dem Menü `Abitur` korrigiert
* FIX: Bericht als PDF exportieren aus dem Menü `Abitur` korrigiert
* FIX: Wechselt man von `Schüler > Daten3 > Fremdsprachen` zu `Bewerber > Daten3 > Fremdsprachen` werden die Inhalte und Verzeichnisliste wieder angezeigt
* FIX: Beim erneuten `Schüler fortschreiben` wird die Schaltfläche `Weiter` aktiviert
* FIX: Schreibfehler im Filter in der Auswahlliste `Schüler` korrigiert
* FIX: das Zuweisen von `Kategorietafeln` unter `Schüler > Zeugnis > Arbeits- und Sozialverhalten` wurde überarbeitet

### SAXSVS

* FIX: 

### MAGELLAN Administrator

* FIX: Im Dialog `Datenaustausch > Postleitzahlen und Banken importieren` wurden die Ergebnisanzeigen ergänzt
* FIX: `Datenaustausch > Daten über das Magellan-Importformat importieren`:
  * Import der `schueler_fachdaten.import.csv` wurde überarbeitet
  * Beim Import von `schueler_import.csv` werden erkannte Doubletten als Nebenlaufbahn des Schülers erkannt, die Stammdaten des Stammschülers werden mit den Daten des Nebenschülers aktualsiert. Bitte beachten Sie den Abschnitt ["Nebenlaufbahn erzeugen"](https://doc.magellan7-toolbox.stueber.de/importe/MagImp/schuelerimportcsv/).
  * Beim Import von `schueler_import.csv` wird ein leerer Eintrag im Feld `InDeutschlandSeit` korrekt übergeben

### MyMAGELLAN-CENTER

* CHANGE: 

### MyMAGELLAN

* FIX:

### MAGELLAN Bibliothek

* CHANGE: `Bibliothek > Ausleihe`: Medium suchen mit Umlaut klappt wieder
* NEW: unter `Bücher/Medien > Vorgänge` wird die Spalte `Klasse` gezeigt
* FIX: Klasseninformationen beim Schüler werden korrekt angezeigt
* FIX: `Schüler > Auswahl > Nächster/Vorheriger Datensatz` Sortierung wird berücksichtigt

### Skripte

* FIX: DE-DIAP-2015.dws > Vorschlagsautomatik für FHR-Berechnung korrigiert, es werden nun die zulässigen 14 Kurse aus 7 Fächern im Vorschlag markiert

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: Klassen\Klassenliste (Zensurenstatistik nach Punkten).rpt
* FIX: Klassen\Klassenliste (Zensurenstatistik nach Noten).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt (es werden nur Wahlpflichtfächer ausgegeben, die eine Note im Feld "Endnote" eingetragen haben, Wahlpflichtfächer ohne Benotung werden nun auch in der Fachbezeichnung entwertet auf dem Zeugnis ausgegeben)
* FIX: Bescheinigung über den Schulbesuch zweifach.rpt
* FIX: BER-Schul Z 300 (11.19).rpt (Leerzeichen vor Datumsangabe eingefügt)
* FIX: Berichte\Zeugnisse\Saarland\Ministerium\SAR-BS-AGZ Lernfeld MBK.rpt
* FIX: Berichte\Zeugnisse\Saarland\Ministerium\SAR-BS-AS-Lernfeld A3 MBK.rpt
* FIX: Berichte\Zeugnisse\Saarland\Ministerium\SAR-BS-HJZ-Lernfeld MBK.rpt
* NEW: SAC-BF-HJZ (B.01.03).rpt (Halbjahreszeugnis Berufsfachschule)
* FIX: SAC-FOS-HJZ (D.01.01).rpt (Umbruch bei langen Fachbezeichnung korrigiert)
* FIX: SAC-BVJ-HJI (A.01.03).rpt (Umbruch bei langen Fachbezeichnung korrigiert)
* FIX: SAC-FS-HJZ (C.01.03).rpt (Umbruch bei langen Fachbezeichnung im Pflichbereich korrigiert, Layout optimiert)
* NEW: SAC-BF-HJZ (B.01.03).rpt (Halbjahreszeugnis Berufsfachschule)
* NEW: SAC-BF-HJI (B.02.01).rpt (Halbjahresinformation der Berufsfachschule für ...)
* FIX: SAC-FS-HJI (C.01.01).rpt (Zeugnisbemerkung "keine" wird nun richtig ausgegeben, wenn dem Schüler keine Bemerkung zugewiesen wurde)
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-BG-ABI (Ergebnisliste).rpt
* NEW: Zeugnisse\Nordrhein-Westfalen\NRW-RS-AS (Variante 2).rpt: Der Bericht gibt als Schwerpunkt den beim aktuellen Schüler-Bildungsgang hinterlegten Schwerpunkt (Bezeichnung) aus, ist kein Bildungsgang dem Schüler zugeordnet, würde der Schwerpunkt (Bezeichnung) des der Klasse zugeordneten Bildungsgang ausgegeben werden.
* NEW: Bibliothek > Berichte\Mahnungen\Mahnungen (mit ISBN).rpt
* CHANGE: Bibliothek > Berichte\Mahnungen\Mahnungen.rpt
