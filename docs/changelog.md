# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN 7. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan7.stueber.de/changelog/](https://doc.mymagellan7.stueber.de/changelog/).

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

!!! danger "Achtung"

    Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

## 7.1.0 - 709 (30.10.2019)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### MAGELLAN

* NEW: In allen mit Schlüsselverzeichnissen hinterlegten Eingabefeldern (mit eingeblendeter Bezeichnung) wird hinter der Bezeichnung eine Klammer gezeigt. In der Klammer wird der Wert aus der Spalte Schlüssel gezeigt. Ist im Schlüssel kein Wert enthalten, wird stattdessen ein Strich "(-)" gezeigt. Damit können Sie auch ohne direkt im jeweiligen Schlüsselverzeichnis nachzusehen erkennen, ob ein Schlüsselwert und ob der korrekte Schlüsselwert für ggfs. statistische Auswertungen hinterlegt wurde.
* NEW: Für die Sammelzuzweisung unter `Schüler > Laufbahn > Allgemein und Abschluss` wurden zur einfacheren Auswahl der Schüler die Spalten `Beruf` und `Bildungsgang` eingeblendet.
* NEW: Neues Fenster mit Zusatzinformationen unter `Schüler > Schüler > Weitere Informationen`, über `STRG+I` oder über das schwarze Infosymbol aufrufbar! Dieses Fenster (aus jeder Unterkarte im Menü `Schüler` aufrufbar, auch in der Auswahlliste) enthält Informationen aus der Bewerbungsphase, über die aktuell besuchte Klasse und über die Ausbildung. Bitte beachten Sie die aktualisierte [Dokumentation](https://doc.magellan7.stueber.de/schulverwaltung/howto/schueler/#weitere-informationen)!
* NEW: Beim Synchronisieren der Schülerfachdaten ins Modul `Berufsschule` werden nur die Daten übertragen, die zur im gewählten Halbjahr aktuellen Ausbildung gehören. Schülerfachdaten (also Fächer und Noten), die nicht für die aktuelle Ausbildung erworben wurden, werden nicht mit synchronisiert.
* NEW: Layout aktualisiert
* NEW: Icons vervollständigt
* NEW: Alle Menüpunkte haben in der Statusleiste der Auswahlliste eine Schaltfläche um die optimale Spaltenbreite einzustellen.
* NEW: Fensterposition links und rechts per `Windows + Pfeil links/rechts` steuerbar

* CHANGE: SAXSVS: Für Sorgeberechtigte, die in der Schweiz wohnen, können Sie im Feld `Land` das Kürzel CH eingegeben, MAGELLAN übergibt diese Ausgabe dann als Schlüssel 158 in die Exportdatei.
* CHANGE: Wird beim Schüler die Adresse geändert und für die Sorgeberechtigten soll die Änderung auch übernommen werden, wird auch die Gemeinde des Schülers für die Sorgeberechtigten übernommen.
* CHANGE: Felder, die bislang nur in der Bundeslandauswahl Berlin sichtbar waren, sind in die Standardansichten integriert worden. Eine Übersicht, welches bislang nur für Berlin gezeigte Feld an welcher Stelle der Oberfläche zu finden ist, finden Sie im Abschnitt [https://doc.magellan7.stueber.de/schulverwaltung/regionales/berlin/schluesselverzeichnisse/](https://doc.magellan7.stueber.de/schulverwaltung/regionales/berlin/schluesselverzeichnisse/).
* CHANGE: Die Karte `Schüler > Statistik` ist zur Karte `Schüler > Merkmale` zusammengefasst worden.
* CHANGE: `Modul MAGELLAN ABITUR` => Pro Halbjahr anlegbare Klassen auf 9 Klassen erhöht.
* CHANGE: Filtern des Feldes `Status` in den Verzeichnisfeldern unter `Schüler > Daten2 > Höchster Abschluss ABS/BBS`  ergänzt.
* CHANGE: Der Style sämtlicher Verzeichnisfelder unter `Schüler > Zeugnis > Fächer/Leistungen` wurde aktualisiert.
* CHANGE: Der Punkt `Schuljahreswechsel` ist vollständig überarbeitet worden und unter der Karte `Laufbahnprozesse > Klassen übernehmen` aufrufbar.   Bitte beachten Sie die aktualisierte [Dokumentation](https://doc.magellan7.stueber.de/schulverwaltung/howto/schuljahreswechsel/#assistent-klassen-ubernehmen-erstellt-neue-klassen)!
* CHANGE: CSV-Export für Berlin (Extras > Exporte > Export > Schüler (Berlin)) wurde überarbeitet

* FIX: Leere Fehlermeldung  und Fensterbeschriftung beim Start des Updates direkt auch MAGELLAN heraus behoben.
* FIX: Das Ablegen von Dokumenten beim Seriendruck für Nebenschüler wurde korrigiert.
* FIX: Das Ablegen von Dokumenten beim Druck für Nebenschüler wurde korrigiert.
* FIX: Trägt man eine neue Herkunftsschule unter `Schüler > Daten2 > Bereits besuchte Schulen` ein wird der Speicherung der Eintrag und die Herkunftsschule direkt aktualisiert.
* FIX: Das Feld `Sprache` [Kurssprachen] ist eingebbar unter `Schüler > Zeugnis > Fächer`.
* FIX: Unter `Datenbank > Optionen > Ein- und Ausblenden > Schüler/Bewerber Extras ausblenden` wird bei gesetztem Haken die Karte ausgeblendet
* FIX: Wenn im Menü Sorgeberechtigte die Postleitzahl oder der Ort eingegeben werden und mit TAB oder ENTER bestätigt wird, wird das Feld Gemeinde entsprechend der hinterlegten Schlüssels befüllt.
* FIX: Ist die Postleitzahl oder der Ort beim Sorgeberechtigten nicht eindeutig, wird bei der Wahl eines Wertes aus dem Unterfenster auch die Gemeindekennziffer befüllt.
* FIX: Bei der Übernahme einer Adressänderung eines Schülers oder Sorgeberechtigten, werden die Änderungen für den jeweils anderen korrekt übernommen.
* FIX: Ändern eines Kürzels im Verzeichnis `Unterrichtsart` für bereits verwendete Werte.
* FIX: Vorlagenfunktion im Menü `Bewerber` ist überarbeitet worden
* FIX: Fensterbezeichnung korrigiert beim Bearbeiten von `Bereits besuchten Schulen` unter `Schüler > Daten2`.

### MAGELLAN Administrator

* FIX: Datenübernahme 6 => 7: Die Tabelle `Sponsoren` und das gleichnamige Feld in der Tabelle `Betriebe` wurden ergänzt
* CHANGE: Das MAGELLAN-Importformat wurde an die Datenstruktur von MAGELLAN 7 angepasst. Bitte lesen hierzu die aktualisierte [Dokumentation](https://doc.magellan7-toolbox.stueber.de/importe/)!
* CHANGE: Das Skript hinter der Funktion `Synchronisiere Zugriffsrechte` wurde optimiert

### MAGELLAN Bibliothek

* FIX: `Ausleihe > Sammelaktion > Klassensatz auswählen` und Ausleiher auswählen
* NEW: Wenn im Medienfilter ein Wert eingegeben wird, der zu einer leeren Liste führen würde, dann wird eine entsprechende Meldung ausgegeben.
* CHANGE: Im Medienfilter wird nach dem erneuten Aufruf das zuletzt gewählte Filterkriterium gezeigt.
* CHANGE: Die Titelzeilen in den Menüpunkten wurden überarbeitet und den Titelzeilen in MAGELLAN angeglichen (Beispiel: Menü `Lieferant`, Anzeige des in der Liste ausgewählten Lieferanten am oberen Fensterrand)
* CHANGE: Seriendruck aus dem Menü `Mahnwesen` überarbeitet
* CHANGE: `Datenbank > Optionen > Autoupdate`: Anzeige überarbeitet

### Skripte

* FIX: Schüler wechseln.dws => Beim Wechsel wird die aktuelle Ausbildung korrekt übernommen

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: DAS-Zeugnis Gymnasium - Mittlerer Schulabschluss (Anlage 10)(§23).rpt
* FIX: DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt
* FIX: DAS-GY-ABI (DIA)(2019).rpt
* FIX: DAS-GS (Klasse 1-2).rpt
* FIX: DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt (ergänzt um das Feld "Ausbilder" im Bereich der Ausbildung)
* FIX: Schulbescheinigung für die Vergangenheit.rpt
* FIX: Schulbescheinigung (Vergangenheit mit Klasse).rpt
* FIX: Schulbescheinigung (mit Klasse und vorauss. Ende zweifach).rpt
* FIX: Schulbescheinigung (mit Klasse und vorauss. Ende einfach).rpt
* FIX: RLP-GES-JZ (Klassen 5 und 6).rpt
* FIX: RLP-GES-HJZ (Klassen 5 und 6).rpt
* FIX: RLP-GES-HJZ (Klassen 7-10).rpt
* FIX: Schülerpersonalblatt (mit Vorbildung).rpt

## 7.0.20 - 708 (27.09.2019)

### MAGELLAN Administrator

* FIX: Problem beim Einlesen des Schlüsselverzeichnisses `Schulformen` [Schüler > Daten 2 > Höchster Abschluss ABS/BBS > Schulform] gelöst

## 7.0.19 - 708 (26.09.2019)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstrukturänderung

* FIX: Fehlende Trigger für die Ansicht "MedizinDaten" hinzugefügt. Damit können diese Felder wieder bearbeitet werden.

### MAGELLAN

* NEW: Die Berliner CSV-Exporte sind unter `Exporte > Exporte` verfügbar. Voraussetzung ist die Bundeslandauswahl Berlin für die verwendete Verbindung.
* FIX: Anzeige des Kürzels unter `Daten2 > Bereits besuchte Schulen` für die Felder `Schule` und `Schulform` angepasst.
* FIX: Unter `Abitur > Qualifikation` und unter `Abitur > Fachwahl` wird für den Aufruf des Excelexports der Listeninhalte das korrekte Symbol verwendet.
* FIX: Unter `Abitur > Qualifikation` und unter `Abitur > Fachwahl` wird für den Aufruf des Excelexports der Listeninhalte das korrekte Symbol verwendet.
* FIX: Unter `Abitur > Qualifikation` und unter `Abitur > Fachwahl` wird für den Aufruf des Excelexports der Listeninhalte das korrekte Symbol verwendet.
* FIX: Beim Blättern zwischen Schülern von der Unterkarte `Daten2 > Bereits besuchte Schulen` wird für den nächsten Schüler die korrekte zuletzt besuchte Herkunftsschule geladen.
* FIX: Fehlende Aktualisierung beim Ausführen von `Laufbahnprozess > Als Bewerber kopieren` während man in der Ansicht `Bewerber` ist korrigiert
* CHANGE: Die Schaltfläche `Weiter` im Dialog `Laufbahnprozess > Schüler wechseln > Weitere Angaben` wird erst nach dem Eintrag der Daten für `Bisherige Klasse beendet am` und `Eintritt in die neue Klasse am` aktiv
* CHANGE: In den Menüs `Personen`, `Lehrer` und `Sorgeberechtigte` wurden die Reiter `Nativ` und `Latein` umbenannt in `Standard` und `Alternativ`
* FIX: Aufruf des Punktes `Abitur > Prüfung > Schriftliche Prüfungsnoten` überarbeitet
* FIX: Aktualsierung der Anzeige der Schüler beim Aufruf und beim Blättern zur nächsten Klasse unter `Klassen > Zeiträume > Schüler` überarbeitet
* FIX: Zuweisen von Klassenleitern ohne Eintrag im Feld `Vorname` als `Klassenleiter` unter `Klasse > Zeiträume > Klassenleiter 1/2` korrigiert
* FIX: Menü `Schüler > Daten 2` - das Filtern von Aktiv und Inaktiv in den Feldern »Höchster Abschluss ABS - Abschluss« und auch in »Höchster Abschluss BBS - Abschluss« ist wieder gegeben
* FIX: Korrigiert wurde der Eintrag für Daten unter `Betriebe > Daten 2` für neu angelegte Betriebe
* FIX: Wird ein inaktiver Schüler als Bewerber kopiert, als Vagabund übernommen und in einem späteren Zeitraum wieder eingeschult, dann wird er mit dem inaktiven Schüler verbunden und (das ist die Änderung) der * Status auf aktiv geändert.
* FIX: Im Assistenten unter `Laufbahnprozess > Schüler wechseln` wurde die Schaltfläche `Weiter` nicht beim erneuten Ausführen aktiv.
* FIX: Beim Anpassen von Werten unter `Extras > Schlüsselverzeichnisse > Zeiträume` wird beim Speichern nicht mehr der Inhalt der Schülerliste gewechselt.
* FIX: Beim Einschulen eines Nebenschülers wird der aktuelle Ausbildungsbetrieb wie folgt gesetzt:
    * Ein Nebenschüler wird im selben Zeitraum eingeschult, indem der Stammschüler existiert: In diesem Fall werden Stamm- und Nebenschüler nicht miteinander verbunden, beide haben die gleiche Liste an Ausbildungen, aber individuelle Einträge als aktuelle Ausbildung.
    * Ein Nebenschüler wird nicht im selben Zeitraum eingeschult, indem der Stammschüler existiert: In diesem Fall werden Stamm- und Nebenschüler  miteinander verbunden, beide haben die gleiche Liste an Ausbildungen und denselben Eintrag als aktuelle Ausbildung.

* FIX: Beim Einschulen eines Vagabunden (kein Nebenschüler), wird die unter `Bewerber > Ausbildung > Ausbildung` gewählte aktuelle Ausbildung für den Schüler übernommen.
* FIX: Der Postleitzahlautomatismus und das Speichern der Daten wurde für das Menü Betriebe überarbeitet.
* FIX: Die Nutzung eines eigenen Unterverzeichnisses (Benutzer) als Quelle für den Schlüsselimport wurde überarbeitet. Bitte beachten Sie in unserer Dokumentation den Punkt [Eigene Kataloge importieren](https://doc.magellan7.stueber.de/schulverwaltung/admin/datenaustausch/#eigene-kataloge-importieren-benutzer)!

### MAGELLAN Bibliothek

* FIX: Anzeige der Daten in Ansicht `Medien > Exemplare` Felder `Zustand` und `Kataloge` wurde korrigiert.

### Skripte

* FIX: Zuweisen von Zugriffsrechten.dws (für Gast2 fehlte die Aussage über den Zugriff auf SchuelerAbwesenheiten), bitte synchronisieren Sie die Zugriffsrechte erneut, um Benutzern mit dieser Rechtegruppe die korrekten Rechte zuzuweisen.

### MAGELLAN Administrator

### Statistik

* FIX: SAC - SAXSVS Export Leerzeichen in Namen werden nicht mehr in die XMl Datei übergeben
* FIX: NRW - ABI.TXT - Die Abiturnote wird jetzt mit einem Punkt, nicht wie versehentlich mit einem Komma ausgegeben
* FIX: NRW - SIM.TXT - LSSchulform wurde nicht korrekt ausgelesen, das führte zu Leereinträgen in der Spalte.
* FIX: NRW - SIM.TXT - LSKlassenart wurde nicht ausgespielt, sondern nur ausgelesen. Das führte bei den Datensatzsarten: "Neuzugang" und "Neuzugang an gleicher Schule" dazu, dass eine Spalte in der Zeile fehlte.
* FIX: NRW - SIM.TXT - Adressmerkmal wird zwar nicht benötigt wurde aber auch nicht als Leerfeld (Nur Trennzeichen) ausgespielt.
* FIX: NRW - SIM.TXT - Die Kopfzeilen für Adressmerkmal und Internat am Ende der SIM.TXT haben gefehlt
* CHANGE: NRW - SIM.TXT - Die beiden Spalten `Produktname` und `Produktversion` dienen lediglich Supportzwecken. Beide Informationen wurden in die Spalte Produktname verschoben. In der Spalte `Produktversion` geben wir jetzt die Datensatzart aus, dies hilft dem Support bei der Suche nach Problemlösungen.
* CHANGE: NRW - SIM.TXT - Kein Fehler aber eine Eingabehilfe. Einige Kunden geben keine Versetzungart ein, sondern setzen lediglich das Merkmal Versetzt. Wir tragen dem Folge und berechnen entsprechend die Versetzung anders als zuvor. Nachzulesen in der Dokumentation unter [SIM.TXT - Dateneingabe - Feld "Versetzung"](https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/#dateneingabe).

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: Klassenlehrerliste mit Räumen (Variante 2).rpt
* FIX: Klassenlehrerliste mit Räumen.rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt (Betriebe).rpt
* FIX: SAR-GEMS-AZ (Klasse 5-10).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* FIX: SAR-GEMS-AZ (Klasse 5-10)
* FIX: Lehrerliste mit Geburtstagen.rpt
* FIX: Lehrerliste mit Geburtstagen (ohne Geburtsjahr).rpt
* FIX: Lehrerliste (Email und Funktion 1-8).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* FIX: NRW-BK-JZ (Anlage C14 - 2 Seitig).rpt

## 7.0.18 - 707 (12.09.2019)

### MAGELLAN

* NEW: Import SchülerOnline freigeschaltet
* FIX: Standardardpfad zur Updateinfo korrigiert
* FIX: Abspreichern von Schülerdatensätzen mit Leerzeichen unterbunden

### Statistik

* NEW: Nordrhein-Westfalen Statistikmodul 2019. Beachten Sie bitte die aktualisierten Schlüsselverzeichnisse. Bitte beachten Sie die aktualisierte Statistikdokumentation für NRW ["Statistikdokumentation für NRW"](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/).

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAR-GEMS-AZ (Klasse 5-10).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* FIX: Lehrerliste mit Geburtstagen.rpt
* FIX: Lehrerliste mit Geburtstagen (ohne Geburtsjahr).rpt
* FIX: Lehrerliste (Email und Funktion 1-8).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* FIX: NRW-BK-JZ (Anlage C14 - 2 Seitig).rpt
* FIX: SAC-BF-JZ (B.03.02).rpt (Unterbericht Zeugnisbemerkungen)
* FIX: SAC-BS-JZ (A.02.01) 2spaltig.rpt (Unterbericht Zeugnisbemerkungen)
* FIX: SAC-BS-JZ (A.02.01).rpt (Unterbericht Zeugnisbemerkungen)

## 7.0.17 - 707 (04.09.2019)

### MAGELLAN

* FIX: Korrektur bei Durchlauf der SAXSVS Statistik
* FIX: Unter `Klassen > Zeiträume` wird die Anzeige der einzublendenen Zusatzklasse beim Weiterschalten aktualisiert
* FIX: Korrektur der Auswahl eines weiteren Mandanten
* FIX: Angezeigte Anzahl der Schüler (gesamt, aktiv, inaktiv) in der Schülerauswahlliste überarbeitet
* FIX: Bezeichnung des Tabs `Datenbank` wird wieder korrekt dargestellt
* FIX: Ablage von PDF-Dokumenten in Schülerunterverzeichnissen parallel zum Druck (oder auch ohne Druck) für Schüler mit Nebenlaufbahn angepasst
* FIX: Die erste dem Schüler unter `Daten2` zugewiesene `Bereits besuchte Schule` wird standardmäßig als `Herkunftsschule` übernommen
* FIX: `Schüler > Daten1` Kontextmenü Passfoto ergänzt um Passfoto aus Digitalquelle
* FIX: für Schüler mit Status N können Zeugnisse, Berichte etc. als PDF Dateien im Dokumente Ordner gespeichert werden

### Skripte  

* FIX: `Exportiere SDTF.dws` und `Importiere SDTF.dws` an neue `MagSDTFSync.exe` angepasst
* FIX: Am Skript `Schüler einschulen.dws` wurde das Einschulen von Schülern korrigiert, die bereits in älteren Halbjahren Schüler der Schule waren

### MAGELLAN Administrator

* FIX: Übernahme MAGELLAN 6 nach MAGELLAN 7: `SchuelerUnfallberichte` und `Beschäftigungsarten`
* FIX: SHL > 00_Klassenstufen.keys

### Statistik

* NEW: Schleswig-Holstein Statistikmodul 2019. Beachten Sie bitte die aktualisierten Schlüsselverzeichnisse. Bitte beachten Sie die aktualisierte Statistikdokumentation für SHL ["Statistikdokumentation für SHL"](https://doc.ls.stueber.de/schleswig-holstein/einstieg/).

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAR-GEMS-AZ (Klasse 5-10)
* FIX: Lehrerliste mit Geburtstagen.rpt
* FIX: Lehrerliste mit Geburtstagen (ohne Geburtsjahr).rpt
* FIX: Lehrerliste (Email und Funktion 1-8).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* FIX: NRW-BK-JZ (Anlage C14 - 2 Seitig).rpt

## 7.0.16 - 707 (16.08.2019)

### MAGELLAN

* FIX: `Betriebe > Kontakte > Neuer Kontakt`
* FIX: `Schüler > Laufbahnprozess > "Schüler wechseln"` die neue Klasse wird wieder angezeigt
* CHANGE: importierbares PLZ-Verzeichnis ergänzt: D 39615 Aland, 15090003 ergänzt
* CHANGE: Beispieldaten in Beispieldatenbank reduziert und aktualisiert
* FIX: Anzeige, Speicherung und Auswahl von neu angelegten Gemeinden beim Zuweisen vom Schüler aus (PLZ und Enter) korrigiert

### MAGELLAN Bibliothek

* FIX: Auswahldialog zur Übernhame neuer Schüler als Medienausleiher korrigiert
* FIX: Neue Medien anlegen: Schaltflächenbenennung korrigiert
* FIX: Neue Medien anlegen: `Jahrgang bis` korrigiert
* FIX: Zur Übernahme als Medienausleiher angebotene Schülermenge angepasst
* FIX: Unter `Datenbank > Optionen > Start` wurde der Zeitraum entfernt (die Bibliothek hat keinen Zeitraumbezug mehr, insofern ist eine Startzeitraum überflüssig)
* FIX: Wechsel zu einem anderen Mandanten korrigiert

### Skripte  

* FIX: `Schüler wechseln.dws`

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: Schülerliste (mit Ausbildungsbetrieben und Geburtsdatum).rpt

## 7.0.15 - 707 (12.08.2019)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstrukturänderung

* CHANGE: Aktualisierung eines Triggers für ENBREA-Leistungen
* FIX: Korrektur des Schülerstatus zu Vagabund (Status 2), wenn der Schüler keine Laufbahndaten hat und der Status 3 ist
* FIX: Setzen der SchuelerZeitraum.ID bei SchuelerZeugnisBemerkungen, falls diese fehlt

### MAGELLAN

* FIX: Durchblättern der Datensätze funktioniert auch mit PgUp und PageDown
* FIX: Befehl "Änderungen verwerfen" ist aktiv
* FIX: Skalierungsproblem beim Vergrößern und Verkleinern der Ansicht behoben
* FIX: Eingabe eines Leerzeichens unter `Schüler > Daten1 > Straße`
* FIX: Anzeige eines Berufes oder Bildungsgangs ohne Betrieb/Praxisbetriebs auf `Ausbildung` und `Daten1` beim Schüler
* FIX: Abfrage für angezeigte Datensätze unter `Schüler > Auswahl` angepasst
* FIX: Downloadpfad unter `Hilfe > auf Aktualisierung prüfen` angepasst
* FIX: Eingabe der PLZ und des Ortes bei Betrieben

### Skripte

* FIX: Anpassung von `Schueler wechseln` (um Haupt- und Nebenklasse für Schüler in der Anzeige alter Zeiträume zu setzen)
* FIX: Anpassung von `Schueler korrigieren` (Status für Vagabunden wird korrekt gesetzt)
* FIX: Anpassung von `Schueler einschulen` (Setzen des aktuellen Ausbildungsbetriebes beim Einschulen von Vagabunden)
* FIX: Anpassung von `Schueler einschulen` (Setzen des aktuellen Ausbildungsbetriebes beim Einschulen und Zusammenführen von Vagabunden und Stammschüler)
* FIX: Anpassung von `Schueler einschulen` (Beim eventuellen Zusammenführen von Vagabunden und Stammschüler wird der Status des Schülers ggfs. auf Status 3 (aktiv) gesetzt)

### MAGELLAN Administrator

* FIX: Restore (Wiederherstellen) einer Sicherungskopie korrigiert
* FIX: Übernahme der Daten von MAGELLAN 6 nach MAGELLAN 7:
    * Klassenzeitraeume.NaechsteKlasse und Klassenzeitraeume.NaechsteKlasseZeitraum werden ignoriert
    * Setzen der SchuelerZeitraum.ID bei SchuelerZeugnisBemerkungen, falls diese fehlt

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAC-BVJ-AS mit HS (A.01.08).rpt (Ausgabe der Klassenmerkmale - Merkmal 1 und Merkmal 2)
* FIX: Schueler\Nordrhein-Westfalen\Schülerstammblatt.rpt
* FIX: Schueler\Nordrhein-Westfalen\NRW-Schülerstammblatt.rpt

Für folgende Berichte wurde die Verknüpfung zwischen SchuelerZeitraeume und SchuelerAusbildung geprüft und ggfs. korrigiert:

* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.05).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-HJI (A.01.02).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-Bescheinigung (F.01.01).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.04).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.04) 2spaltig.rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.03).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.02).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (2 seitig).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (Vorbereitungsklasse) (A.01.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.05) 2spaltig.rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.04).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.01.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (2 seitig).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-HJZ (1 seitig).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-JZ1 (C.01.02).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-JZ2 (C.01.02).rpt
* FIX: Zeugnisse\Sachsen\Zertifikat (F.01.09).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-AZ (C.01.04)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-Fremdsprachenzertifikat (F.01.05).rpt
* FIX: Zeugnisse\Sachsen\SAC-Fremdsprachenzertifikat (F.01.05)(DIN A3)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-Fremdsprachenzertifikat (F.01.05)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-JZ (A.02.01).rpt
* FIX: Zeugnisse\Sachsen\SAC-FOS-FHReife (D.01.04).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-HJI (C.01.01).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-HJI (C.01.01)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-BVJ-JZ (A.01.08)(2 jähriges BVJ).rpt
* FIX: Zeugnisse\Sachsen\SAC-BVJ-AS mit HS (A.01.08).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.01.07)(Einstiegsqualifizierung).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.01.07)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-BG-ABI (E.01.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BF-AS (A.02.07).rpt
--
 
## 7.0.14 - 706 (19.07.2019)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### MAGELLAN

* FIX: `Betriebe > Daten2`: Berufe und Bildungsgänge (mit voller Zeichenlänge Kürzel und Bezeichnung) können gespeichert werden
* FIX: Schüler, die in einem vergangenen Zeitraum mehrfach eine Klasse besucht haben (Beispiel Klasse 1a, Wechsel in Klasse 1b, erneuter Wechsel in Klasse 1a) werden korrekt in den Auswahlliste gezeigt
* FIX: pausierende Schüler werden über die F3-Suche (zeitraumübergreifende Suche) gefunden
* FIX: Unter `Klassen > Zeiträume` können Klassenzeiträume, denen noch kein Schüler zugewiesen wurde, gelöscht werden.

### MAGELLAN BIBLIOTHEK

* FIX: `Bücher/Medien > Daten2 > Erscheinungsland`: Problem beim Speichern behoben
* FIX: `Bücher/Medien > Daten2 > Format`: Problem beim Speichern behoben
* CHANGE: Link unter `Hilfe > Handbuch` aktualisiert
* FIX: Das Verhalten beim Markieren in Schülerauswahlliste wurde überarbeitet (Markierungen bleiben nicht nur funktionell, sondern auch sichtbar bestehen)

### MAGELLAN Administrator

* FIX: Korrektur der Datenübernahme von 6 -> 7 (`Datenbankpflege > Mandanten kopieren`). Wer vorher bereits Schüler übernommen hat, kann die Korrektur auch in der bestehenden MAGELLAN 7-Datenbank mit dem Punkt `Datenbankpflege > Verwaiste Stammschüler-Verweise entfernen` ausführen.

## 7.0.13 - 705 (28.06.2019)

### Allgemein

* NEW: Neue Nachrichtenfunktion: Die MAGELLAN-Willkommensseite wurde neu gestaltet und enthält jetzt zu den wichtigsten Aufrufen (Dokumentation, Newsletter, Ticketsystem usw.) einen Nachrichtenbereich, über den wir Sie auf dem Laufenden halten werden. Sie erhalten diesen Überblick beim Aufruf von MAGELLAN, des MAGELLAN ADMINISTRATORs und der MAGELLAN BIBLIOTHEK.

![Willkommenseite mit Nachrichten](/assets/images/neues/13.png)
  
### MAGELLAN BIBLIOTHEK

* FIX: Problem beim Aufruf des Menüpunkts `Schüler` behoben

### MAGELLAN Administrator

* CHANGE: Ergänzung in der Datenübernahme: Für Schüler (Status 3 und 4), die in Version 6 kopiert, aber trotzdem nicht wieder zu einem Datensatz beim Einschulen zusammengeführt wurden, werden bei der Datenübernahme nach MAGELLAN 7 die Einträge aus `IDIntern` entfernt.

!!! warning "Wichtig"

    Die Funktion `Datenaustausch > Daten über das MAGELLAN-Importformat importieren` wird aktuell überarbeitet und wurde daher vorübergehend deaktiviert.

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAC-FOS-FHReife (D.01.04).rpt (Satz am Seitenende von Seite 2 aktualisiert)
* NEW: SAC-BS-AS (A.01.07)neu.rpt

## 7.0.12 - 705 (24.06.2019)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!


!!! warning "Wichtig"

    Bitte beachten Sie, dass Sie dieses Update nicht einspielen durfen, wenn Sie im MyMAGELLAN-Prozess sind, also mym7-Dateien verteilt haben, diese aber noch nicht wieder nach MAGELLAN importiert wurden! 
    Wenn die Dateien über den Aufruf im MAGELLAN ADMINISTRATOR wieder eingesammelt wurden, kann MAGELLAN auf die neue Ausgabe aktualisiert werden.
    

### MAGELLAN

* FIX: `Schüler > Laufbahnprozesse > Schüler korrigieren` mit abgestuften Benutzerrechten wurde angepasst
  
!!! info "Hinweis"
  
      Bitte beachten Sie, dass das `Zugriffsrechte synchronisieren` im Modul MAGELLAN ADMINISTRATOR (Menüpunkt Benutzerverwaltung) vorab durchgeführt werden muss!

* FIX: Passfotofunktion unter `Bewerber > Daten1` und unter `Lehrer > Daten1` ergänzt
* FIX: im Lehrermenü kann `Auswahlliste > Lehrer markieren > Rechtsklick` das Fehlzeitenfenster aufgerufen werden
* FIX: Die Funktionalitäten unter `Schüler > Zeugnis > Bemerkungen` wurden überarbeitet
* FIX: `Abitur > Bemerkungen > Sammelzuweisung`: zur Auswahl stehende Schüler werden korrekt gefiltert
* FIX: Unter das Schnittstellenfenster unter `Extras > Export > Export` gibt entsprechende Meldungen aus oder lässt Sie den Assistenten nicht weiterbedienen, wenn keine Schnittstelle oder kein Zeitraum gewählt wurde.
* FIX: Speichern von Schülerfehlzeiten
* FIX: Erste bereits besuchte Schule des Bewerbers (`Bewerber > Daten2`) wird standardmäßig als Herkunftsschule gesetzt
* FIX: Beschriftung des Doublettenprüfungsfensters für Lehrer korrigiert
* FIX: Korrektur der Anzeige des Status (S und N statt H und N für Stamm- und Nebenschüler) unter `Sorgeberechtigte > Kinder`
* FIX: Aufruf der Serienmail aus dem Menü `Bewerber` ergänzt
* FIX: Aufruf `Abitur > Drucken > Zeugnisse` ergänzt
* FIX: `Schüler > Daten2 > Abgangsart` Kürzellänge von 20 Zeichen wird akzeptiert
* FIX: `Schüler > Laufbahnprozesse > Ausschulen > Abgangsart` Kürzellänge von 20 Zeichen wird akzeptiert
* FIX: Geschwindigkeit beim Zuweisen des Status (aktiv, inaktiv, pausierend) in der Schülerauswahlliste optimiert
* FIX: `Klassen > Daten > Abteilung` Problem beim Speichern behoben
* FIX: Unter `Extras > Schlüsselverzeichnisse > Noten` wurden die Spalten `Von` und `Bis` ergänzt.
* FIX: Korrektur der Sammelzuweisung unter `Schüler > Abitur > Zeugnisbemerkung`
* NEW: Auf den Registerkarten im Menü `Schüler` werden jeweils am oberen Rand Symbole für den Status (aktiv, inaktiv, pausierend), ggfs. die Volljährigkeit (Berechnet anhand des Tagesdatums und des Geburtsdatums) und/oder der Status `Geheim` (Häkchen von Daten 3) eingeblendet.

![Symbole auf den Schülerregisterkarten](/assets/images/changelog/7.0.12.02.png)

* FIX: Löschen von PDF-Dateien aus Dokumenteverzeichnissen der Schüler/Bewerber korrigiert
* CHANGE: Unter `Schüler > Dokumente` ist als Standardansicht die Sortierung nach Details und die optimale Spaltenbreite vorbelegt
* FIX: Anzeige der Daten unter `Klassen > Zeiträume` korrigiert
* FIX: Schaltfläche `Fertigstellen` wird beim erneuten Korrigieren von Schülern aktiviert
* FIX: gewählte Größe des Druckvorschaufensters wird gespeichert
* FIX: `Datenbank > Optionen > Ein-/Ausblenden` Beschriftung angepasst
* FIX: Versionsanzeige unter `Hilfe > Version und Lizenz` angepasst
* FIX: `Betriebe > Daten 2` Berufe zuzuweisen korrigiert
* FIX: Unter `Schüler > Laufbahn > Abschluss` wurde die akzeptierte Kürzellänge der Felder `Abschluss1`, `Abschlussart1`, `Abschluss2` und `Abschlussart2` angepasst.
* FIX: In der Sammelzuweisung unter `Schüler > Laufbahn > Abschluss` wurde die akzeptierte Kürzellänge der Felder `Abschluss1`, `Abschlussart1`, `Abschluss2` und `Abschlussart2` angepasst.
* FIX: Im Menü `Abitur` kann die Simulation nicht mehr aus der Auswahlliste aufgerufen werden, sondern aus den Unterkarten `Qualifikation`, `Prüfung`, `Zeugnisbemerkungen` und `Fachwahl`.
* FIX: Querverweise auf weitere Verzeichnisse unter `Extras > Schlüsselverzeichnisse > Berufe` (Berufsfelder, Fachrichtungen, Qualifikationsniveau) korrigiert
* FIX: Querverweise auf weitere Verzeichnisse unter `Extras > Schlüsselverzeichnisse > Bildungsgänge` (Berufsfelder, Schwerpunkte, Fachrichtungen, Qualifikationsniveau ) korrigiert
* FIX: Verzeichnisfelder im Assistenten `Schüler ausschulen` korrigiert: `Abgangsart`, `Übergang`, `An Schule`, `An Schulform`
* FIX: Die Bezeichnung der Fachspalte unter `Abitur > Qualifikation` wurde angepasst.
* FIX: Die Anzeige des am unteren Rand eingeblendeten Skriptnamens im Menü `Abitur` auf den Karten `Qualifikation`, `Prüfung`, `Zeugnisbemerkungen` und `Fachwahl` wurde angepasst.
* FIX: Unter `Extras > Schlüsselverzeichnisse > Zeugnisformular > Datei` wird im Bearbeitenmodus die Schaltfläche zum Auswählen per Verzeichnisbaum gezeigt
* FIX: Bei der Auswahl einer Formulardatei unter `Extras > Schlüsselverzeichnisse > Zeugnisformular > Datei` wird das Öffnen von Crystal Reports unterbunden
* FIX: Beim Verschieben der Fenstergröße der zweigeteilten Ansicht unter `Schüler > Laufbahn` erscheinen keine "Schatten" mehr.
* FIX: Hilfeverweise auf neue Dokumentationspfade angepasst
* FIX: Meldung beim Umschalten mit nicht korrekt hinterlegtem Fachwahlskript von `Abitur > Fachwahl` eine andere Unterkarte behoben

### SAXSVS

* CHANGE: Wenn bei einem Schüler der Haken unter `Schüler > Daten 2 > NdH` aktiviert/wieder deaktiviert wird, wird entsprechend der Knoten für Migration erzeugt/nicht erzeugt.

### MAGELLAN BIBLIOTHEK

* NEW: Die Ansicht `Schüler` hat keine Zeitraumauswahl mehr und zeigt alle aktiven und inaktiven Ausleiher mit der aktuellen oder zuletzt besuchten Klasse an. Sie können Ihre Liste über die Spalten `Status` und `Zeitraum` individuell filtern.
* NEW: Ausleiher, die nicht mehr als Schüler in MAGELLAN existieren, werden mit einem eigenen Status (roter Kreis) dargestellt. Durch die Anzeige der offenen Vorgänge und diesem Status oder des Status inaktiv können Sie diese Ausleiher gezielt aus der Liste löschen.
* CHANGE: neue Symbole in der Medienansicht
* FIX: Verschieben in anderen Katalog korrigiert
* FIX: Text im Assistenten zum manuellen Anlegen eines neuen Mediums korrigiert
* FIX: Assistent zur Übernahme neuer Lehrer korrigiert
* FIX: neue Symbole für die Auswahl der Exemplare in der Ausleihe
* FIX: Rückgabe per eingescanntem Buch korrigiert
* FIX: angezeigte Punkte unter `Extras > Berichte organisieren` und `Extras > Vorlagen organisieren` angepasst
* FIX: Schüler ( = Ausleiher aus Bibliothek) löschen korrigiert
* FIX: Personen hinzufügen korrigiert
* NEW: in der Auswahlliste der `Schüler`  werden am unteren Rand zwei Ziffern eingeblendet, die linke zeigt alle (auch ehemalige) Ausleiher, die rechte zeigt je nach Filterung der Liste die gezeigte Anzahl der Ausleiher.
* FIX: Sammelzuweisung für Exemplare überarbeitet
* FIX: `Bücher/Medien` Anzahlen und Symbole in der Statusleiste angepasst
* FIX: die gewählten Filterungen in den Menüpunkten werden gespeichert
* NEW: Unter `Ausleihe > Ausleiher > alle auswählen (*)` wird die Klasse und der Status eingeblendet, zusätzlich kann die Liste gefiltert werden

### MyMAGELLAN

* NEW: Die Bemerkung, die zum Start gezeigt wird, hat eine Scrollbar erhalten, um auch längere Texte bequem lesen zu können
* NEW: In den Auswahlen (Fächer, Schüler) und in den Eingabeübersichten (Fächer, Schüler) wird die jeweils letzte Sortierung in der Registry des verwendeten Rechners gespeichert.
* NEW: Die Spaltenreihenfolge der Eingabeübersichten (Fächer, Schüler) wird in der Registry des verwendeten Rechners gespeichert.
* FIX: Öffnen einer bereits zuvor genutzten Datei über `Datei > Zuletzt geöffnete Dokumente` behoben.
* NEW: `Datei > Öffnen` speichert das zuletzt geöffnete Verzeichnis für den nächsten Zugriff.
* FIX: Problem beim Öffnen per Doppelklick auf Passwort-geschützte mym-Dateien behoben.
* CHANGE: Startfenstergröße vorgegeben

### MyMAGELLAN CENTER

* NEW: In die MyMAGELLAN-Dateien ausschließlich Verzeichniswerte (Noten, Fachstatus, Unterrichtsarten, Abschlüsse usw.) übergeben werden, deren Bis-Datum im MAGELLAN-Verzeichnis (MAGELLAN > Extras > Schlüsselverzeichnisse) leer ist oder ein Datum enthält, dass vom Tag der Erstellung aus gesehen in der Zukunft liegt. Ungültige Werte stehen somit den Kollegen bei der Eingabe in MyMAGELLAN nicht mehr zur Verfügung.
* FIX: Problem mit passwortgeschützten Dateien behoben

### MAGELLAN Administrator


!!! warning "Wichtig"

    Die Funktion `Datenaustausch > Daten über das MAGELLAN-Importformat importieren` wird aktuell überarbeitet und wurde daher vorübergehend deaktiviert.

* CHANGE: Die Skriptdatei `Zugriffsrechte zuweisen` wurde um neue Bestandteile der Datenbank ergänzt. Bitte synchronisieren Sie die Zugriffsrechte über die Schaltfläche im `MAGELLAN-ADMINISTRATOR > Benutzerverwaltung > Zugriffsrechte` synchronisieren.
  
![Zugriffsrechte synchronisieren](/assets/images/changelog/7.0.12.01.png)

* NEW: `Datenbankpflege > Gemeinden synchronisieren` wurde ergänzt um Sorgeberechtigte, damit können nachträglich Gemeindekennziffern für Sorgeberechtigte ergänzt werden, wenn die PLZ und der Ort einem Eintrag im Verzeichnis der Postleitzahlen zugeordnet werden können.
* FIX: Anzeige der Rechtegruppe `Statistikadmin` in der Übersicht der Benutzer
* FIX: Unter `Datenbankverbindung > Wiederherstellen` wird beim Öffnen eines Pfades (Schaltfläche am Ende des Pfadfeldes) direkt der eingestellte Zielpfad geöffnet.
* FIX: `Datenbankpflege > Code 128` generieren korrigiert.
* FIX: Problem beim Abruch des nachträglichen Anmelden in den Menüs `Datenbankpflege` und `Datenaustausch` behoben.

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX:

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur von MAGELLAN 7 angepasst:

* FIX: Klassenliste mit Klassendaten.rpt
* FIX: Klassenliste (Sorgeberechtigte und Geburtsdatum).rpt
* FIX: Klassenliste inkl. ausgeschulter Schüler.rpt
* FIX: Klassenliste mit Eltern2.rpt
* FIX: Klassenliste mit Endnoten.rpt
* FIX: Klassenliste Schüler-Notenmatrix (mit Verhalten und Mitarbeit).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat).rpt
* FIX: Klassenliste Schüler-Notenmatrix.rpt
* FIX: Prüfungsliste.rpt
* FIX: Berichte\Klassen\Klassenliste (Sorgeberechtigte und Geburtsdatum).rpt
* FIX: Berichte\Klassen\Saarland\SAR-Klassen-Notenliste Halbjahr Lernfeld MBK.rpt
* FIX: Berichte\Klassen\Saarland\SAR-Klassen-Notenliste Abgeschlossene Lernfelder MBK.rpt
* FIX: Berichte\Klassen\Rheinland-Pfalz\Klassenliste mit Endnoten.rpt
* FIX: Berichte\Klassen\Nordrhein-Westfalen\Zeugnisliste BBS (nur für Minderjährige).rpt
* FIX: Berichte\Klassen\Nordrhein-Westfalen\Zeugnisliste BBS.rpt
* FIX: Berichte\Schueler\Bescheinigung über Schülerübergabe.rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GY-FHReife (Bescheinigung).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 1-2).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 3-4).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GY-ABI (2014).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-Studienbuch (Qualifikationsphase - zweite Seite).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-ABI-Meldung-MdlAbitur (Profil 2011).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-ABI (2015).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-Abi (Leistungskarte 2011).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AS (Klasse 5-10)(G8).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AS (Klasse 5-10)(G9).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AZ (A3)(2015).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AZ (A3).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-FHReife (2011).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-FHReife (2015).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-HJZ (2008).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-HJZ (Profil).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 3-4).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 1-2)
* FIX: Berichte\Zeugnisse\Schweiz\CH-Notenausweis-E-Profil-2003.rpt
* FIX: Berichte\Zeugnisse\Auslandsschulen\DAS-GY-ABI-Reifepruefung 2017.rpt
* FIX: Berichte\Zeugnisse\Auslandsschulen\DAS-GY-AZ mit FHR (Anlage 9b).rpt
* FIX: Berichte\Zeugnisse\Auslandsschulen\DAS-GY-AZ mit FHR (Anlage 9b).rpt
* FIX: Berichte\Klassen\Jahresnotenliste-BVJ.rpt
* FIX: Berichte\Schueler\Unfallanzeige (mit Erläuterungen).rpt
* FIX: Berichte\Schueler\Schülerstammblatt (Belegung der Arbeitsgemeinschaften).rpt
* FIX: Berichte\Schueler\Schülerpersonalblatt incl. Schuleintritt (Betriebe -Querformat).rpt
* FIX: Berichte\Schueler\Schülerpersonalblatt (nur mit Eltern und Vorbildung).rpt
* FIX: Berichte\Schueler\Schülerliste (zeitraumübergreifende Fehlzeiten).rpt
* FIX: Berichte\Schueler\Schülerausweis ohne Photo.rpt
* FIX: Berichte\Schueler\Schüler-Abi (Antrag mündliche Prüfung).rpt
* FIX: Berichte\Schueler\Schüler mit Herkunftsschulen.rpt
* FIX: Berichte\Schueler\Schüler mit Herkunftsschulen u. letzte Klasse.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BBS (Bescheinigung Niveaustufen).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BF-AS.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BF-AZ.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BF-HJZ (1. Variante).rpt
* FIX: Berichte\Zeugnisse\heinland-Pfalz\RLP-BF-HJZ (2. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BF-HJZ (3. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BF-JZ (Oberstufe).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BF-JZ (Unterstufe).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BG (Punktekreditkarte-2010).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BG-ABI (2010).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BG-ABI (2010)A4.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BG-AS (Anlage D 48).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGJ-AS.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGJ-AZ (mit Zusatzbemerkung).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGJ-AZ (ohne Zusatzbemerkung).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGJ-HJZ (Variante 2).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-Punktekreditkarte.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-HJZ 13-2.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-HJZ 13-1.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-HJZ 12-2.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-HJZ 12-1.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-HJZ 11-2.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-FHReife (Jahrgangstufe 13).rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-HJZ 11-1.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-FHReife (Jahrgangstufe 12).rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-FHReife (Jahrgangstufe 11).rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-AZ 13-1.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-AZ 12-2.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-AZ 12-1.rpt"
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-WG-AZ 11-1.rpt"
* FIX: RLP-BS-AZ (neue Form 1. Variante).rpt
* FIX: RLP-BGJ-HJZ.rpt
* FIX: RLP-BGJ-JZ.rpt
* FIX: RLP-BGYM-ABI (2010).rpt
* FIX: RLP-BS (Zwischenzeugnis mit Wahlpflicht Variante 1).rpt
* FIX: RLP-BS (Zwischenzeugnis mit Wahlpflicht Variante 2).rpt
* FIX: RLP-BS (Zwischenzeugnis ohne Wahlpflicht Variante 1).rpt
* FIX: RLP-BS (Zwischenzeugnis ohne Wahlpflicht Variante 2).rpt
* FIX: RLP-BS-AS (1. Variante).rpt
* FIX: RLP-BS-AS (2. Ausdruck).rpt
* FIX: RLP-BS-AS (2. Variante).rpt
* FIX: RLP-BS-AS (neue Form 1. Variante ohne Wahlpflicht).rpt
* FIX: RLP-BS-AS (neue Form 1. Variante).rpt
* FIX: RLP-BS-AS (neue Form 2. Variante ohne Wahlpflicht).rpt
* FIX: RLP-BS-AS (neue Form 2. Variante).rpt
* FIX: RLP-BS-AS (ohne Wahlpflicht).rpt
* FIX: RLP-BS-AZ (2. Ausdruck alte Form 1. Variante).rpt
* FIX: RLP-BS-AZ (alte Form 1. Variante).rpt
* FIX: RLP-BS-AZ (alte Form 2. Variante).rpt
* FIX: RLP-BS-AZ (alte Form nf ohne Wahlpflicht).rpt
* FIX: RLP-BS-AZ (alte Form nf).rpt
* FIX: RLP-BS-AZ (alte Form ohne Wahlpflicht).rpt
* FIX: RLP-BS-JZ (ohne Wahlpflicht Ziel erreicht).rpt
* FIX: RLP-BS-AZ (neue Form 2. Variante).rpt
* FIX: RLP-BS-JZ (mit Wahlpflicht Ziel erreicht).rpt
* FIX: RLP-BS-JZ (mit Wahlpflicht Ziel nicht erreicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (neue Form 1. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGJ-HJZ.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGJ-JZ.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BGYM-ABI (2010).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS (Zwischenzeugnis mit Wahlpflicht Variante 1).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS (Zwischenzeugnis mit Wahlpflicht Variante 2).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS (Zwischenzeugnis ohne Wahlpflicht Variante 1).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS (Zwischenzeugnis ohne Wahlpflicht Variante 2).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (1. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (2. Ausdruck).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (2. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (neue Form 1. Variante ohne Wahlpflicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (neue Form 1. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (neue Form 2. Variante ohne Wahlpflicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (neue Form 2. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AS (ohne Wahlpflicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (2. Ausdruck alte Form 1. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (alte Form 1. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (alte Form 2. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (alte Form nf ohne Wahlpflicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (alte Form nf).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (alte Form ohne Wahlpflicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-JZ (ohne Wahlpflicht Ziel erreicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-AZ (neue Form 2. Variante).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-JZ (mit Wahlpflicht Ziel erreicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-JZ (mit Wahlpflicht Ziel nicht erreicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-HJZ (Klassen 7-10).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-BS-JZ (ohne Wahlpflicht Ziel nicht erreicht).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-FO (HJZ-JZ-AZ).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-FO-FHReife (DIN A3).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-FS-AS (Sozialpädagogik DIN A3).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES (Abschlussprognose).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES (Beiblatt).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-AS (9.Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-AS (10.Klasse mit Ü 11).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-AS (10.Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-AS (10.Klasse).rpt.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-AS (Zeugnis für die Realschule).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-AZ.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-HJZ (Klassen 5 und 6).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (2010).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-JZ (Klassen 5 und 6).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GES-JZ (Klassen 7-10).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS (Abgangszeugnis 1. Klasse – 1 seitig - dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS (Abgangszeugnis 2. und 3. Klasse – 2 seitig - ohne Noten dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS (Abschlusszeugnis – 2 seitig- dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS (HJZ und JZ - 3. und 4. Klasse - 2 seitig dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS (Jahreszeugnis 1. Klasse – 1 seitig - dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS (Jahreszeugnis 2. und 3. Klasse – 2 seitig - ohne Noten dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AS (1. Klasse – 1 seitig - dynamisch 2012).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AS (1. und 2. Klasse - 1 oder 2 seitig).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AS.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AZ (1. Klasse – 1 seitig - dynamisch 2012).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AZ (3. und 4. Klasse - 2 seitig - dynamisch 2012).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AZ (3. und 4. Klasse - 2 seitig - dynamisch).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AZ (3. und 4. Klasse - 2 seitig).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-AZ.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-HJZ (2. Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-HJZ (3. und 4. Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-HJZ_JZ (3. und 4. Klassen-2 seitig dynamisch 2012).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-JZ (1. und 2. Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-JZ (2. Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GS-JZ (3. und 4. Klasse).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A3 - 2. Seite)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (2010-G8-G9) (2).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (2010-G8-G9) (A4 Seite 1) (ohne Wappen).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (2010-G8-G9) (A4 Seite 1).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (2010-G8-G9) (A4 Seite 2).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (2010-G8-G9).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A3 - 1. Seite ohne Wappen)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A3 - 2. Seite ohne Wappen)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-HJZ 11-1.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A3 ohne Logo)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A3 ohne Wappen)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A3)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A4 - 1. Seite ohne Logo)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A4 - 1. Seite)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A4 - 2. Seite)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A4 ohne Wappen und Rand)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A4)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-ABI (DIN A4-altsprachlich)2006.rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-AS (11-13).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-AZ (2006).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-AZ (2016).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-FHReife (Jahrgangstufe 11-13).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-HJZ (2spaltig mit FSP).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-HJZ (2spaltig ohne FSP).rpt
* FIX: Berichte\Zeugnisse\Rheinland-Pfalz\RLP-GY-HJZ (11-13).rpt

## 7.0.11 - 704 (03.06.2019)


### SAXSVS

* CHANGE: <bzsort_neu> `Übergang an Schule` wird ausgespielt, wenn eine Schule unter `Schüler > Daten2 > An Schule` erfasst wurde, die unter `Schule > Daten > Schulnummer` einen Eintrag (7-stellige Schulnummer) hat.
* NEW: Für das Feld <an_geschlecht> wird zusätzlich für `weiblich` und `männlich` auch die Auswahl `divers` mit der Ziffer 3 für SAXSVS übergeben.

### MyMAGELLAN

* NEW: Mit dieser Version veröffentlichen wir die erste Ausgabe von MyMAGELLAN. 
  * Das MyMAGELLAN CENTER finden Sie nicht mehr als gesonderten Programmaufruf, sondern als Teil des Administrators. Für das MyMAGELLAN CENTER ist keine gesonderte Installation nötig. Die Dokumentation des MyMAGELLAN CENTERs finden Sie [hier](https://doc.magellan7.stueber.de/mymagellancenter/einfuehrung/).
  * Die Dokumentation des Eingabemoduls MyMAGELLAN (aus Sicht des eingebenden Kollegen) finden Sie [hier](https://doc.mymagellan7.stueber.de/).

### MAGELLAN Administrator

* NEW: Neuer Aufruf für das MyMAGELLAN CENTER

## 7.0.10 - 704 (24.05.2019)

### MAGELLAN

* FIX: Beim Seriendruck an Betriebe wird der aktuelle Ausbildungsbetrieb korrekt ermittelt

### SAXSVS

* CHANGE: Bei den erweiterten Prüfungen Land/PLZ/Gemeindekennziffer für Betriebe, Schüler und Sorgeberechtigte werden ausländische Adressen berücksichtigt
* FIX: Bei Nebenschülern wird das Abgangsdatum zum Auswerten eines eventuellen Abbruchs korrekt berücksichtigt

### Importe

* CHANGE: Postleitzahlverzeichnis geändert, nach dem Import des Verzeichnisses stehen Ihnen folgende Änderungen für neue Zuweisungen zur Verfügung. Bereits erfolgte Zuweisungen werden nicht geändert, sondern müssten bitte manuell angepasst werden.
 
  Alt | Neu
  --|--
  02727 Neugersdorf|02727 Ebersbach-Neugersdorf
  02730 Ebersbach |02730 Ebersbach-Neugersdorf
  01738 Klingenberg | 01774 Klingenberg


### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: Klassenlehrerliste.rpt (Summen korrigiert)
* FIX: SAC-BS-JZ (A.02.01).rpt



## 7.0.9 - 704 (17.05.2019)


### SAXSVS

* CHANGE: Neue Prüfungen für Schüler, Betriebe und Sorgeberechtigte für die Felder Land und Gemeinde
* FIX: Laufbalken wird beim Durchlauf von Beginn an gezeigt, nicht erst bei der Anzeige der Meldungen
* FIX: beim Auslesen der Ausbildungs-GUID von Nebenschülern


### Skripte

* FIX: Änderung des Skriptes ``Zuweisen von Zugriffsrechten`` (Fehlende Rechte in der Ansicht SchuelerFamilie auf tblLehrer ergänzt)

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAC-BS-AS (A.02.05) 2spaltig.rpt (Ausgabe des Ausbildungsberufes)
* FIX: SAC-BS-AS (A.02.04).rpt (Ausgabe des Ausbildungsberufes)
* FIX: SAC-BS-AS (A.02.04).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FOS-JZ (D.01.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FOS-JZ (D.01.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FOS-AZ (D.01.03).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FO-JZ (D.01.02)(bis 2017).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FO-AZ (D.01.04)(bis 2017).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BVJ-AS mit HS (A.01.08).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-JZ (A.02.01) 2spaltig.rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (A.02.05).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-JZ (E.01.02).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-BG-HJZ (E.01.03).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-JZ (E.01.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-HJZ (E.01.01).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AZ (B.03.04).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (A.02.05) 2spaltig.rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AS (A.02.07).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AZ (A.02.04).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AZ (A.02.04) 2spaltig.rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (2 seitig).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BGJ-AS mit HS (A.01.10).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-AZ (E.01.05).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-ABI (E.01.09).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG (Punktekreditkarte-2010).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-JZ (B.07.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-JZ (B.04.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-JZ (B.03.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJZ (B.04.03).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJI (B.05.01).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AS (B.01.03).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FS-JZ (C.01.02).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FS-JZ (C.01.02)(bis 2017).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FS-AS_(C.01.09).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FS-AS (C.01.11).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FS-AS (C.01.09).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-FS-AS (C.01.08).rpt (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-JZ (A.02.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-HJZ (1 seitig).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-HJI (A.01.04).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-HJI (A.01.02).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-BVB Maßnahme (A.01.05).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-Bescheinigung (F.01.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AZ (A.02.03).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AZ (A.02.02).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AZ (2 seitig).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (Vorbereitungsklasse) (A.01.06).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (A.02.06).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (A.01.07).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BS-AS (A.01.06).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BGJ-AS ohne HS (A.01.11).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BGJ-AS mit HS (A.01.09).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-HJZ (E.01.04).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-HJZ (2010).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-HJZ (2008)2.rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-ABI (E.01.08).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-ABI (E.01.08)(SF).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-ABI (E.01.06).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BG-ABI (E.01.06)(bis 2017).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-ZAS (B.04.04).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJZ (B.07.03).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJZ (B.02.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJI (B.04.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJI (B.03.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJI (B.02.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-HJI (B.01.01).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AZ (B.01.02).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AS (B.07.05).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AS (B.04.06).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AS (B.04.05).rpt  (Kontrolle, ggfs. Korrektur)
* FIX: SAC-BF-AS (B.03.05).rpt  (Kontrolle, ggfs. Korrektur)  
* FIX: Zertifikat (F.01.09).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-JZ2 (C.01.02).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-JZ1 (C.01.02).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-HJZ (C.01.03).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-HJI (C.01.01).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AZ (C.01.06).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AZ (C.01.05).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AZ (C.01.04).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AS mit FHR (C.01.14).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AS mit FHR (C.01.13).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AS mit FHR (C.01.12).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AS (C.01.15).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FS-AS (C.01.13).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-Fremdsprachenzertifikat (F.01.05).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-Fremdsprachenzertifikat (F.01.05)(DIN A3).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FOS-HJZ (D.01.01).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FOS-FHReife (D.01.04).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FO-HJZ (D.01.03)(bis 2017).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FO-HJI (D01.01).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FO-HJI (D.01.01)(Fachpraktischer Unterricht).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FO-HJI (D.01.01)(bis 2017).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FO-FHReife (D.01.06)(bis 2017).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-FO-FHReife (D.01.05)(bis 2017).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-BVJ-HJI (A.01.03).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-BVJ-AS ohne HS (A.01.10).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-BVJ-AS ohne HS (A.01.09).rpt (Kontrolle, ggfs. Korrektur) 
* FIX: SAC-BV-HJI (A.01.01).rpt (Kontrolle, ggfs. Korrektur)   


## 7.0.8 - 703 (07.05.2019)

### SAXSVS

* FIX: Besondere Berücksichtigung von Stamm- und Nebenschülern

## 7.0.7 - 703 (29.04.2019)

### MAGELLAN

* FIX: Seriendruck an Praxisbetriebe in den Menüpunkten `Bewerber` und `Schüler` überarbeitet
* FIX: Problem beim Aktualisieren (F5) einer neuen Eingabe behoben 

### SAXSVS

* FIX: Export von Sorgeberechtigten angepasst

### MAGELLAN Administrator

* CHANGE: Export und Import von Benutzern unter `Benutzerverwaltung > Benutzer importieren/Benutzer exportieren` angepasst

## 7.0.6 - 703 (26.04.2019)

### MAGELLAN

* FIX: "Zuweisen von Zugriffsrechten.dws":  Fehlende Rechte auf "BewerberVerfahren", "BewerberFachdaten" und "BewerberUnterlagen" berücksichtigt , bitte führen Sie im MAGELLAN ADMINISTRATOR das "Zugriffsrechte synchronisieren" im Menüpunkt `Benutzerverwaltung` aus.

![Zugriffsrechte synchronisieren](/assets/images/changelog/7.0.7.01.png)

* FIX: Zeichenlänge auf 20 für die Kürzel der Verzeichnisse Anschluesse Extern und Abschluesse Intern erhöht.
FIX: Die ausführliche Anzeige wurde korrigiert für `Bewerber/Schüler > Daten 4 > Adresse/Förderung`
* FIX: `MAGELLAN > Daten4 > Verkehrsmittel`: Anzeige und Sortierung der Verzeichniswerte
* FIX: Bewerber-Serienmail integriert
* FIX: Schüler-Serienmail korrigiert
* FIX: Schüler- und Lehrerfehlzeitenfunktionalität korrigiert
* NEW: neue Verhältnisse Schüler-/Bewerber-Familien: Onkel, Tante, Bruder, Schwester, Erzieher, Notfall, Gasteltern
* FIX: Alle Kürzel auf 20 Zeichen in den Schlüsselverzeichnissen und in allen Ansichten angepasst
* FIX: Unter `Daten2 > Höchster Abschluss ABS/BBS > Abschluss` wurde jeweils die Anzeige im Verzeichnisfeld auf das Kürzel geändert.

### SAXSVS

* FIX: Problem beim Prüfen des Schülerbetriebes behoben
* CHANGE: In Absprache mit dem LASUB wurde Folgendes geändert: Bei unseren Sorgeberechtigtenprüfungen und beim Erzeugen der XML-Datei werden nur noch Schüler berücksichtigt, die ausgehend vom im Assistenten eingegebenen Stichtag und dem Geburtsdatum nicht volljährig sind. Bitte beachten Sie den Abschnitt [Sorgeberechtigte](https://doc.magellan7.stueber.de/schulverwaltung/regionales/sachsen/datenpflege/#sorgeberechtigte--saxsvs-bbsschuelersorgeberechtigte)!
* NEW: Im Statistikassistenten unter `MAGELLAN > Extras > Exporte > Export` wird Ihnen beim Erstellen der XML-Datei für die Meldungen eine neue gesonderte Spalte mit dem jeweiligen Feld oder Bereich gezeigt. Damit können Sie nach dem Export der Meldungen diese sortieren und gezielter die Daten nachpflegen.


!!! info "Hinweis"

  Bitte öffnen Sie `MAGELLAN > Extras > Schlüsselverzeichnisse > Schulformen (Herkunft)`. Wechseln Sie zur Zeile mit dem Schlüssel 115 und schalten den Bearbeitenmodus über das Stiftsymbol am oberen Fensterrand ein. Ändern Sie die Bezeichnung bitte auf das Wort **"Berufsvorbereitungsjahr"** und speichern diese Änderung.

![Bitte die Bezeichnung des Schlüssels 115 anpassen!](/assets/images/changelog/7.0.6.01.png)

### Importe

* CHANGE: Im Verzeichnis der `Abschluesse (Extern)` unter `MAGELLAN > Extras > Schlüsselverzeichnisse` wurde die Bezeichnung für den Schlüssel 115 geändert, korrekt ist die Bezeichnung: Berufsvorbereitungsjahr


### Skripte

* FIX: "Zuweisen von Zugriffsrechten.dws":  Fehlende Rechte auf "BewerberVerfahren", "BewerberFachdaten" und "BewerberUnterlagen" berücksichtigt  


### MAGELLAN Administrator

* NEW: Unter `Datenbankpflege` wurden die Funktionen  `Anrede setzen` und  `Passfoto löschen`ergänzt. Alle Aktionen werden in der [Dokumentation im Abschnitt Datenbankpflege](https://doc.magellan7.stueber.de/schulverwaltung/admin/datenbankpflege.html) beschrieben.
* FIX: Duplizieren von Benutzern angepasst
* NEW: Neue Funktionalität unter `Datenpflege`. Es können die Einträge im Feld IDIntern geleert werden, wenn der Stammschüler, auf den verwiesen wird nicht mehr existiert. Diese Situation kann in MAGELLAN 7 nicht mehr entstehen, kann aber aus MAGELLAN 6 mit übernommen worden sein. Bitte beachten Sie den Abschnitt [Verwaiste Stammschüler-Verweise entfernen](https://doc.magellan7.stueber.de/schulverwaltung/admin/datenbankpflege/#verwaiste-stammsch%C3%BCler-verweise-entfernen)!

### MAGELLAN Bibliothek

* Fix: Datenbankanmeldung beim Druck von Quittungen korrigiert
* CHANGE: die Abfragen beim Aufruf der Menüpunkte `Schüler` und `Vorgänge` wurden optimiert, damit die Daten in den Menüpunkten schneller aufrufbar sind

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur von MAGELLAN 7 angepasst:

* FIX: Quittung(DIN A4).rpt
* FIX: Quittung(DIN A4).rpt
* FIX: Zeugnisse\Nordrhein-Westfalen


## 7.0.5 - 703 (11.04.2019)

### MAGELLAN

* FIX: SAXSVS: Problem für `al_abschl_dat` und `al_laufb_kl` behoben
* CHANGE: SAXSVS: Neue Meldungen und in allen Meldungen werden mehr Detailinformationen gezeigt
* CHANGE: SAXSVS: Neue Prüfungen, wenn ein Wert ohne Schlüssel vergeben wurde (Beispiel: Staatsangehörigkeit mit Kürzel D zugeordnet, aber kein Schlüssel im Verzeichnis hinterlegt)
* CHANGE: SAXSVS: XML-Fehlermeldungen werden erst ausgegeben, wenn keine MAGELLAN-Meldungen mehr ausgegeben werden.

Beispiel für eine MAGELLAN-Meldungen:

Art	|Message
--|--
Fehler|	Ina Müller (549): Das Feld "<abs><av_abs_schart>" darf nicht leer sein.
Fehler|	Otto Meyer (549): Das Feld "<bbs><av_bbs_schart>" darf nicht leer sein.
Fehler|	Sebastian Schmidt (2043): Das Feld "<abs><av_abs_schart>" darf nicht leer sein.

Beispiel für eine XML-Meldung:

```
In Zeile "1" an Position "xxx"
Begründung: 
  Fehler beim Analysieren von '' als date-Datentyp.
Analyse des Elements 'al_abschl_dat' mit dem Wert '' fehlgeschlagen.
 
XML-Auszug: ....
```
* FIX: Problem beim Ändern von Staatsangehörigkeiten behoben, bitte synchronisieren Sie die Zugriffsrechte im Modul `MAGELLAN Administrator > Benutzerverwaltung`.
* FIX: Der Aufruf für `Status ändern` wurde in den Menüpunkten `Personen`, `Sorgeberechtigte`, `Betriebe`, `Schulen` unter `Auswahlliste > Datensatz auswählen > Rechtsklick` ergänzt.


### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* NEW:`Berichte\Klassen` Klassenliste mit Schülersummendaten Ausländer.rpt
* NEW:`Berichte > Klassen` Klassenliste mit Schülersummendaten Ausländer.rpt
* NEW: `Berichte > Zeugnisse > Berlin` BER-Schul Z 302 (10.18).rpt

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur von MAGELLAN 7 angepasst:

* CHANGE: `Berichte > Schüler > RLP/NIE/BAW/BER`
* CHANGE: `Berichte > Mandanten > Allgemein`
* CHANGE: `Berichte > Zeugnisse > Auslandsschulen`
* CHANGE: `Berichte > Zeugnisse > Baden-Württemberg`
* CHANGE: `Berichte > Zeugnisse > Demo`
* CHANGE: `Berichte > Zeugnisse > Mecklenburg-Vorpommern`
* CHANGE: `Berichte > Zeugnisse > Hessen`
* CHANGE: `Berichte > Zeugnisse > Niedersachsen`


## 7.0.4 - 703 (01.04.2019)

### MAGELLAN

* FIX: Datenstrukturanpassungsassistent: Eine Sicherung muss vor der Anpassung erstellt werden
* FIX: Datenstrukturanpassungsassistent: Sicherungspfad wird aus den eigenen Einstellungen im Willkommensassistenten oder aus dem MAGELLAN Administrator vorbelegt. Sollte die Sicherung nicht lokal erfolgen, muss der Pfad vorab existieren.
* FIX: Datenstrukturanpassungsassistent: Schaltfläche zum Erstellen der Sicherung eingeblendet.

![Sicherung erstellen](/assets/images/changelog/7.0.4.00.png)

* FIX: Datenstrukturanpassungsassistent: Assistent kann nur als sysdba gestartet werden
* FIX: Problem beim Eintragen von Schülerfehlzeiten korrigiert
* FIX: Anzeige der Statistikmerkmale für Schüler und Bewerber in der Unterkarte `Statistik` behoben.
* FIX: In den Zugriffsrechten der Benutzern wurden die Rechte für die Tabellen `Medienausleiher` (Änderungen bei Lehrerdatensätzen) und `SchuelerAbwesenheiten` korrigiert. Bitte führen Sie im MAGELLAN Administrator einmal den Punkt `Benutzerverwaltung > Zugriffsrechte synchronisieren` aus, das Skriptdatum im Ergebnisfenster müsste den 26.03.2019 zeigen.

![`MAGELLAN Administrator > Benutzerverwaltung > Zugriffsrechte synchronisieren`](/assets/images/changelog/7.0.4.04.png)

* FIX: Mehrfachdarstellung von Schülern beim Fachtafel-zuweisen behoben.
* FIX: Ein neuer Eintrag unter `Bewerber > Ausbildung` wird automatisch als aktueller Ausbildungsdatensatz übernommen. Das gilt nur für den ersten Eintrag, ab dem zweiten Eintrag ändern Sie ggfs. den Eintrag über das Feld `aktuelle Ausbildung` am unteren Menürand.
* FIX: `Mandanten > Daten2 > Schulformen`, hier können auch Werte mit mehr als 8-Zeichen Kürzellänge verwendet werden.
* FIX: Korrektur für den Seriendruck an den Betrieb des Schülers
* CHANGE: Der Eintrag der aktuellen Ausbildung (`Schüler > Ausbildung > Ausbildung`) wird bei Schülerkopien pro Kopie gespeichert. 
* CHANGE: Beim Einschulen wird der `Zugang am` für Schüler oder Schülerkopien wie folgt übernommen:

Feld|Schüler (ohne IDIntern)|Schülerkopie (mit IDIntern)
--|--|--
aktualisiert das Feld `Daten2 > ZugangAm`|Ja|Nein
aktualisiert das Feld `Laufbahn > Zugang`|Ja|Ja
aktualisiert das Feld `Laufbahn > Schulformeintritt`|Ja|Ja

![Zugang am](/assets/images/changelog/7.0.4.02.png)

* NEW: Neue Sammelzuweisungsmöglichkeit zum Aktivieren oder Deaktivieren des Feldes `Schüler > Ausbildung > Ausbildung editieren > Neuanfänger im Bildungsgang`

![Neuanfänger im Bildungsgang](/assets/images/changelog/7.0.4.03.png)

* FIX: Verzeichnisfelder unter ´Schüler > Daten 2` aktualisiert
* CHANGE: Von- und Bis-Datum der Ausbildung auf `Schüler > Daten1` eingeblendet
* CHANGE: Gruppierung im Verzeichnis `Bildungsgänge` entfernt
* FIX: Beim Anlegen eines neuen Schülers wechselt der Auswahllistefilter automatisch auf von `Eingeschult` auf `Vagabunden`.
* FIX: Beim Zuweisen einer neuen Schulform unter `Mandanten > Daten2 > Schulformen` werden Werte mit bis zu 20 Zeichen im Kürzel akzeptiert
* FIX: Editierbarkeit unter `Schüler > Zeugnis > Details > Tutor und Prüfungsvorsitz` korrigiert

### MAGELLAN Bibliothek

* FIX: `Datenbank > Optionen > Quittungen`: es gibt keinen vorbelegten Bericht mehr
* FIX: `Datenbank > Optionen > Quittungen`: `Quittungen/Bestätigungen automatisch drucken` wird korrekt gespeichert
* FIX: Vor dem Anlegen eines Mediums wird geprüft, ob mindestens ein Katalog angelegt und ausgewählt ist


### MAGELLAN Administrator

* NEW: Neue Funktionalität, um Bewerbern, wenn sie nur eine Ausbildung haben, diese als aktuelle Ausbildung zuzuweisen. Hintergrund: die Zuweisung als aktuelle Ausbildung ist die Voraussetzung für den Seriendruck an diesen Betrieb.

![Bewerberausbildung als aktuelle Ausbildung hinterlegen](/assets/images/changelog/7.0.4.01.png)

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur in MAGELLAN 7 angepasst:

* CHANGE: `Berichte > Klassen > allgemeine Berichte`
* CHANGE: `Berichte > Klassen > Baden-Württemberg`
* CHANGE: `Berichte > Klassen > Berlin`
* CHANGE: `Berichte > Klassen > Mecklenburg-Vorpommern`
* CHANGE: `Berichte > Klassen > Nordrhein-Westfalen`
* CHANGE: `Berichte > Klassen > Rheinland-Pfalz`
* CHANGE: `Berichte > Schüler > allgemeine Berichte`
* CHANGE: `Berichte > Schüler > Auslandsschulen`
* CHANGE: `Berichte > Schüler > Baden-Württemberg`
* CHANGE: `Berichte > Schüler > Berlin`
* CHANGE: `Berichte > Schüler > Mecklenburg-Vorpommern`
* CHANGE: `Berichte > Schüler > Niedersachsen`
* CHANGE: `Berichte > Schüler > Nordrhein-Westfalen`
* CHANGE: `Berichte > Schüler > Rheinland-Pfalz`
* CHANGE: `Berichte > Schüler > Schleswig-Holstein` 
* CHANGE: `Berichte > Bewerber > allgemeine Berichte`
* CHANGE: `Berichte > Bewerber > Baden-Württemberg`
* CHANGE: `Berichte > Betriebe > allgemeine Berichte`
* CHANGE: `Berichte > Adressen > allgemeine Berichte`
* CHANGE: `Berichte > Buchungen > allgemeine Berichte`
* CHANGE: `Berichte > Kurslisten > allgemeine Berichte`
* CHANGE: `Berichte > Haushaltsstellen > allgemeine Berichte`
* CHANGE: `Berichte > Inventar > allgemeine Berichte`
* CHANGE: `Berichte > Lehrer > allgemeine Berichte`
* CHANGE: `Berichte > Lehrer > Rheinland-Pfalz`
* CHANGE: `Berichte > Lieferanten > allgemeine Berichte`
* CHANGE: `Berichte > Verlage > allgemeine Berichte`
* CHANGE: `Berichte > Sorgeberechtigte > allgemeine Berichte`
* CHANGE: `Berichte > Schulen > allgemeine Berichte`
* CHANGE: `Berichte > Quittungen > allgemeine Berichte`
* CHANGE: `Berichte > Prüfungslisten > Baden-Württemberg`
* CHANGE: `Berichte > Prüfungslisten > allgemeine Berichte`
* CHANGE: `Berichte > Personen > allgemeine Berichte`
* CHANGE: `Berichte > Medienvorgaenge > allgemeine Berichte`
* CHANGE: `Berichte > Medien > allgemeine Berichte`
* CHANGE: `Berichte > Mandanten > allgemeine Berichte`
* CHANGE: `Berichte > Mandanten > Rheinland-Pfalz`
* CHANGE: `Berichte > Mahnungen > allgemeine Berichte`
* CHANGE: `Berichte > Zeugnisse > allgemeine Berichte`

## 7.0.3 - 703 (15.03.2019)

### MAGELLAN

* NEW: `Schüler/Bewerber > Daten 2 > Aufenthalt > Aufenthaltserlaubnis` - MAGELLAN um Aufenthaltserlaubnis Von- und Bis- Datum erweitert. Im Zuge dessen die Aufteilung der Eingaben auf der Maske angepasst. 
* CHANGE: Unterkarte `Bewerber` ist nur noch in der Sammelzuweisung aus dem Menü `Bewerber` sichtbar
* FIX: Alle Neu-Dialoge der Hauptansichten: Abfrage nach Gast1- und Gast2-Rechten, mit entsprechender Meldung
* FIX: Datenstrukturversion auf 703 angepasst und Skript korrigiert
* FIX: Bewerber/Schueler: Nach Anlegen neuer Herkunftsschule und gesetztem Haken wird jetzt auch die gesetzte Herkunftsschule in der Combobox dargestellt (Aktualisierungsfehler)
* FIX: Sammelzuweisung Bewerber/Schüler : Aus- und Einblenden der Bewerberdaten > Karte im Dialogfenster korrigiert
* FIX: Serienbrief b. Schüler - Ändern der Empfänger (Betrieb/Sorgeberechtigte) hat sich nicht ausgewirkt
* FIX: Beim Wechsel aus der Auswahlliste `Schüler` nach einer Filterung werden auf `Daten 1` die Ausbildungsdaten und Familiendaten des korrekten Schülers gezeigt.
* FIX: Seriendruck aus dem Menü `Bewerber`.
* FIX: Beim Seriendruck aus dem Menü `Schüler` werden die Datenmengen (nur Schüler- und Klassendaten, zusätzlich Sorgeberechtigtendaten oder zusätzlich Betriebedaten) korrekt an Word übergeben.
* FIX: Die Ausgabe der Datenmenge `An den aktuellen Betrieb der markierten Schüler` für den Seriendruck wurde korrigiert
* CHANGE: Unter `Bewerber > Ausbildung` wurde die Eingabe des aktuellen Betriebes ergänzt
* FIX: Aufruf `Drucken > Zeugnisse` wurde im Menü `Berufsschule` eingeblendet


### MAGELLAN Bibliothek

* FIX: Berichte werden in der Vorschau gefüllt
* FIX: Meldung beim Aufruf der Ausleihe behoben (Cannot focus a disabled or invisible window)
* FIX: Ausleihe und Rückgabe angepasst
* FIX: Zuordnung des Berichteverzeichnisses zum Menü `Mahnwesen`


### MAGELLAN Administrator

* NEW: Verbindungen können per Kopieren dupliziert werden (Rechtsklick auf die Verbindung > Verbindung kopieren) 
* NEW: Ansicht `Benutzerverwaltung` > Neue Registerkarte `Administratoren`:  
  * Fehlende Administratoren können nachträglich angelegt werden
  * bei bestehenden Administratoren kann das Passwort geändert werden
  * Aufruf der Funktionalitäten per Doppelklick auf den Administratorendatensatz oder über den Punkt `Extras`
  
![nachträgliches Anlegen eines sysdba-Nutzers](/assets/images/changelog/sysdba.anlegen.png)  

* FIX: `Datenbankpflege > Mandanten kopieren > 6 nach 7`: (Gilt für Umstiege mit MAGELLAN bis zur 7.0.2, für spätere Versionen nicht mehr nötig.) Die IDIntern bei Schülern zu denen das Original nicht mehr existiert, wird entfernt.
* NEW: Unter `Datenbankpflege` finden Sie den neuen Punkt `Korrektur Mandanten kopieren`. Die Korrektur überträgt Ausbildungsdaten eines Nebenschülers in die Liste des Stammschülers. Die gesamte Liste wird für Stamm- und Nebenschüler gezeigt.

 ![Neue Korrekturmöglichkeit im MAGELLAN ADMINISTRATOR](/assets/images/changelog/mandanten.korr.png) 


### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: DAS-GY-ABI (Anlage 7).rpt (Bericht war versehentlich nur für die Darstellung am Bildschirm eingestellt)
* CHANGE: Klassen\Klassenliste (Betriebe mit Auszubildenden nach Gemeinden).rpt
* CHANGE: Klassen\Anwesenheitsliste für den Tag.rpt
* CHANGE: Klassen\Anwesenheitsliste für ganzen Monat.rpt
* CHANGE: Klassen\Jahresnotenliste-BVJ.rpt
* CHANGE: Klassen\Klassen (Fax an Betriebe der Schueler).rpt
* CHANGE: Klassen\Klassenlehrerliste mit Räumen (Variante 2).rpt
* CHANGE: Klassen\Klassenlehrerliste mit Räumen.rpt
* CHANGE: Klassen\Klassenlehrerliste.rpt
* CHANGE: Klassen\Klassenliste (Adressen Schüler und Eltern).rpt
* CHANGE: Klassen\Klassenliste (ausländische Schüler).rpt


## 7.0.2 - 702 (19.02.2019 - 13.30 Uhr) - Achtung erneute Veröffentlichung!!


!!! info "Hinweis"

  Aufgrund von Problemen beim Erstellungsprozess mussten wir die Version erneut veröffentlichen.
  Sollten Sie die Version 7.0.2 bereits installiert haben. Wiederholen Sie bitte den Download und Installation.

## 7.0.2 - 702 (19.02.2019 - 10.00 Uhr)

!!! info "Hinweis"

  Die Datenstruktur von MAGELLAN ist erweitert worden!  
  Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Eine genaue Anleitung zum Serviceupdate finden Sie [**hier**](http://doc.magellan7.stueber.de/installation/update.html). Sollten Probleme auftreten, schauen Sie bitte [**hier**](http://doc.magellan7.stueber.de/installation/troubleshootingupdate.html).


### MAGELLAN

* NEW: `Schüler > Daten 2 > Höchster Abschluss ABS > Schule`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss ABS > Schule`

* NEW: `Schüler > Daten 2 > Höchster Abschluss ABS > Schulform`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss ABS > Schulform`

* NEW: `Schüler > Daten 2 > Höchster Abschluss BBS > Schule`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Schule`

* NEW: `Schüler > Daten 2 > Höchster Abschluss BBS > Schulform`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Schulform`

* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Beruf`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Erreicht am`

* CHANGE: `Schüler > Zugang/Abgang` komplett nach `Schüler > Daten 2` verschoben, Registerkarte entfernt
* CHANGE: `Bewerber > Zugang/Abgang` komplett nach `Bewerber > Daten 2` verschoben, Registerkarte entfernt

* NEW: SAXSVS - "Vollständige" Abbildung der Schnittstelle
* NEW: SAXSVS - Schüler zum Löschen (in SAXSVS) vormerken oder 
                Schüler vom Export in die XML-Datei ausschließen                
* CHANGE: SAXSVS - Schlüsselverzeichnisse für die Schnittstelle aktualisiert. Bitte neu einlesen! 


### MAGELLAN Administrator

* FIX: 


### MAGELLAN Bibliothek

* FIX: 


### MAGELLAN Skripteditor

* FIX: 


### Skripte


### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* CHANGE: SAC: Die mitgelieferten Zeugnisse für Sachsen wurden den neuen Gegebenheiten in MAGELLAN 7 angepasst. Zur Anpassung Ihrer eigenen Berichte lesen Sie bitte den Abschnitt <a href="https://doc.magellan7-kb.stueber.de/cr/berichte_fuer_7_anpassen.html" target="_blank">Berichte für MAGELLAN 7 anpassen</a> in unserer Knowledge Base.

---

## 7.0.1 - 701 (04.01.2019)



!!! info "Hinweis"

  Die Datenstruktur von MAGELLAN ist erweitert worden! 
  Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Eine genaue Anleitung zum Serviceupdate finden Sie [**hier**](http://doc.magellan7.stueber.de/installation/update.html). Sollten Probleme auftreten, schauen Sie bitte [**hier**](http://doc.magellan7.stueber.de/installation/troubleshootingupdate.html).

### MAGELLAN

* NEW: Status "Abwesend" mit Speicherung von längerfristigen Abwesenheiten 
       (z.B. Elternzeit, Auslandsjahr, etc.). Gespeichert werden die Daten in 
       der Tabelle "SchuelerFehlzeiten", die über das neue Feld "Art" zwischen 
       Abwesenheit und der bisherigen Fehlzeit unterschieden werden kann. 
       Dargestellt und bearbeitet können die Abwesenheiten unter 
       Schueler > Laufbahn. Weitere Infos können der Dokumentation entommen 
       werden.
* NEW: Anzeige des Schülerstatus auf den Registerkarten. Aktuell nur Daten 1. 
       Wird in den kommenden Serviceupdates auf alle Registerkarten erweitert.      
* FIX: SAXSVS: Auf das neues Schema 2.3 umgestellt. Aktuell wird noch die 
       Minimalanforderung unterstützt. Wir arbeiten an der vollständigen Umsetzung,
       siehe, z.B. die neue Funktion "Abwesenheit", die einen Teil der Umsetzung 
       darstellt, mehr Daten für die Schnittstelle in MAGELLAN erheben zu können.
       

### MAGELLAN Administrator

* FIX: 


### MAGELLAN Bibliothek

* FIX: 


### MAGELLAN Skripteditor

* FIX: 


### Skripte


### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

---

## 7.0.0 - 700 (21.12.2018)

### MAGELLAN

* FIX: Fehlermeldung bei der Installation, wenn kein Crystal Reports installiert ist \#1024921
* FIX: Fehler bei der Sammelzuweisung \#1024899
* FIX: Field Merkmal S1 not found Export SAXSVS \#1024971
* NEW: Die aktuelle Ausbildung des Schülers wird jetzt pro Schulhalbjahr gespeichert
* NEW: \#1019480 - Deutsche Auslandsschule als Region im Willkommensassistent wählbar
* CHANGE: Die bisherige beim Schüler gespeicherte Ausbildung wird nur noch beim Bewerber genutzt und wird bei der Einschulung eines Schülers berücksichtigt.
* CHANGE: Hinzufügen von Datensätzen in den Schlüsselverzeichnissen wieder mit Pfeiltaste unten auf dem letzten Datensatz möglich


### MAGELLAN Administrator

* FIX: Aktualisierte Schlüsselverzeichnisse für Sachsen
* CHANGE: \#1019441 - Neuer Unterordner `\Benutzer` im Importverzeichnis. Benutzer können dort angepasste Importdateien hineinlegen, die von der Installation nicht überschrieben werden.
* NEW: \#1019480 - Deutsche Auslandsschule als Region wählbar
* NEW: Nachträgliches Anmelden an die Datenbank über Menü `Datenbank > Anmelden...` möglich.


### MAGELLAN Bibliothek

* FIX: 


### MAGELLAN Skripteditor

* FIX: 


### Skripte


### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.