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

## 7.1.6 - 711 (14.02.2020)

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

### MAGELLAN Administrator

* FIX: Im Dialog `Datenaustausch > Postleitzahlen und Banken importieren` wurden die Ergebnisanzeigen ergänzt
* FIX: `Datenaustausch > Daten über das Magellan-Importformat importieren`:
  * Import der `schueler_fachdaten.import.csv` wurde überarbeitet
  * Beim Import von `schueler_import.csv` werden erkannte Doubletten als Nebenlaufbahn des Schülers erkannt, die Stammdaten des Stammschülers werden mit den Daten des Nebenschülers aktualsiert. Bitte beachten Sie den Abschnitt ["Nebenlaufbahn erzeugen"](https://doc.magellan7-toolbox.stueber.de/importe/MagImp/schuelerimportcsv/).
  * Beim Import von `schueler_import.csv` wird ein leerer Eintrag im Feld `InDeutschlandSeit` korrekt übergeben
* FIX: `Benutzerverwaltung > Administratoren`: Ändern des DBAdmin-Passwortes korrigiert

### MAGELLAN Bibliothek

* CHANGE: `Bibliothek > Ausleihe`: Medium suchen mit Umlaut klappt wieder
* NEW: unter `Bücher/Medien > Vorgänge` wird die Spalte `Klasse` gezeigt
* FIX: Klasseninformationen beim Schüler werden korrekt angezeigt
* FIX: `Medien/Bücher (genau auch für Schüler, Mahnungen,  Vorgänge, Personen, Lehrer, Lieferanten, Mandanten, Verlage) > Auswahl > Nächster/Vorheriger Datensatz` Sortierung wird berücksichtigt
* Mahnungen Vorgänge Personen Lehrer Lieferanten Mandanten Verlage
* FIX: Schüler > Auswahl > Ausleihen: das Symbol wird nur noch bei aktiven Ausleihen dargestellt

### Skripte

* FIX: DE-DIAP-2015.dws > Vorschlagsautomatik für FHR-Berechnung korrigiert, es werden nun die zulässigen 14 Kurse aus 7 Fächern im Vorschlag markiert

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
* CHANGE: Bibliothek > Berichte\Mahnungen\Mahnungen.rpt (kleinere Anpassungen)
* CHANGE: Bibliothek > Berichte\Medienausleiher\Bibliotheksausweis (Standard).rpt (Druckreihenfolge korrigiert)
* CHANGE: Bibliothek > Berichte\Medienausleiher\Bibliotheksausweis (Avery-Zweckfom-Etikett 3658).rpt (Druckreihenfolge korrigiert)
* CHANGE: Bibliothek > Berichte\Medienausleiher\Bibliotheksausweis (klein).rpt (Druckreihenfolge korrigiert)
* CHANGE: Bibliothek > Berichte\Medienausleiher\Bibliotheksausweis (mit Passfoto).rpt (Druckreihenfolge korrigiert)

## 7.1.5 - 710 (05.02.2020)

### MyMAGELLAN

* FIX: Listenfelder unter `Schüler > Zeugnisdaten` sind auswählbar
* Change: Mym7-Datei kann nicht mehrfach geöffnet werden

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-AS (Variante 2).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-AS (Variante 1).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-AZ (Klasse 7-10).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-JZ (Hauptschulabschluss).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-HJZ (Klasse 7-10).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-JZ (Klasse 7-10).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-JZ (Sekundarabschluss I).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-RS-ÜZ (Klasse 7-10).rpt
* CHANGE: Zeugnisse\Nordrhein-Westfalen\NRW-BF-FHReife (Anlage C17 schulischer Teil).rpt

## 7.1.4 - 710 (03.02.2020)

### MAGELLAN

* FIX: Feldlänge in der Oberfläche für `Bewerber > Daten 1 > Geburtsland` an die Zeichenzahl des Kürzels aus dem Schlüsselverzeichnis `Staatsangehörigkeiten` angepasst
* FIX: Neue oder geänderte Einträge unter `Klassen > Zeiträume` werden korrekt in der Klassenauswahlliste aktualisiert
* FIX: Verzeichnis `Fächer > Fachgruppe` editierbar
* FIX: Verzeichnis `Fachtafel > Fachtafel - Fächer > Lehrer` editierbar
* CHANGE: Spaltenbezeichung für die Religionsteilnahme in den Auswahllisten für Bewerber und Schüler angeglichen
* FIX: Autoupdate korrigiert
* FIX: bei vom Stammschüler kopierten Bewerber werden die Bewerberungsdaten unter `Bewerber > Daten1` und `Bewerber > Auswahl` gleich gezeigt
* FIX: Unter `Menü Abitur > Abitur > Simulation > Prüfung` werden neu berechnete Durchschnittswerte und -noten angezeigt
* FIX: `Extras > Schlüsselverzeichnisse > Fachtafeln`: Fachwahltafeln kopieren

### SAXSVS

* FIX: Ausgabe der Klasse für Nebenschüler

### MAGELLAN Administrator

* NEW: Der Punkt `Datenaustausch > Daten über das MAGELLAN-Importformat importieren` wurde umgestaltet. Bitte beachten Sie die aktualisierte [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/admin/datenaustausch/#daten-uber-das-magellan-importformat-importieren)!

### MyMAGELLAN-CENTER

* CHANGE: Standardsortierung der Liste nach `Kennung`

### MyMAGELLAN

* FIX: versehentlich eingetragene Mahnung kann wieder gelöscht werden
* FIX: zuletzt eingetragene Note wird vor dem Datensatzwechsel gespeichert
* FIX: Eingabe von Noten mit oder ohne Tendenz per Tastatur korrigiert
* FIX: Funktion der Vor- und Zurückschaltfläche im Bereich `Schüler` und `Fächer` überarbeitet

### Skripte

* CHANGE: Importiere SDTF.dws (Unterrichtsart-Schlüssel "L" ist hinzugekommen)
* CHANGE: Zuweisen von Bewerberstammdaten.dws (Sammelzuweisungen aus dem Bewerber- oder Schüler-Menü): Debugmeldungen wurden unterbunden

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
* FIX: SAC-BG-HJZ (E.01.01) Verknüpfungen korrigiert

## 7.1.3 - 710 (08.01.2020)

### MAGELLAN

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

