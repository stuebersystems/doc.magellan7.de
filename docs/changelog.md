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

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## 7.1.21 - 716 und 717 (04.12.2020)

### Datenstruktur

* CHANGE: SchuelerZeitraeume.BU um Statistikadmin als Recht erweitert
* CHANGE: Constrain für Dienstbez ergänzt

### MAGELLAN SCHULVERWALTUNG

* FIX: Sammelzuweisung unter `Schüler > Zeugnis > Details`
* FIX: Emailversand aus `Extras > Benachrichtigungen` korrigiert
* CHANGE: Aktualisierung auf Crystal Reports Runtime 13.0.29

### MYMAGELLAN

* CHANGE: Filteransicht `Fächer`/`Schüler`: Spaltenposition und Gruppierungen bleiben bei Datensatzwechsel innerhalb der Ansicht erhalten (nicht bei Ansichtswechsel). Bei der Ansicht `Schüler` gibt es noch die Besonderheit, dass die Spalte `Kurs` immer die erste Spalte ist.

### MAGELLAN Bibliothek

* FIX: Exportieren von Dokumenten nach `C:\Users\Public\Documents\Stueber Systems\Magellan 7\Dokumente\Schueler\SchuelerID\Bibliothek` korrigiert
* CHANGE: STRG+D für den Aufruf des Dokumenteverzeichnisses im Menü `Schüler` ergänzt

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: `Importiere sdtf.dws` Problem beim Zuweisen von Lehrerunterricht für Veranstaltungen denen mehrer Klassen zugewiesen wruden (Zusatzunterricht U6-Datensatz) gelöst

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: SAR-GEMS-HJZ-JZ (Klasse 5-10).rpt wurde Für MAGELLAN 7 angpasst
* FIX: SAR-GY-ABI (GOS2.0).rpt (Ausgabe Seminarfach, Sprachniveau)
* NEW: Schülerbericht "KV09b_Masernschutz.rpt", Anleitung unter [https://doc.la.stueber.de/berichte/02_schueler/#kv09b-masernschutzrpt](https://doc.la.stueber.de/berichte/02_schueler/#kv09b-masernschutzrpt)
* FIX: BAW-BG-ABI (DIN A4 doppelseitig 2018 - Abschrift).rpt
* FIX: BAW-BG-ABI (DIN A4 doppelseitig 2018).rpt
* FIX: BAW-BG-ABI (DIN A4 doppelseitig 2018 - Neuausstellung).rpt
* NEW: BAW-BG-ABI (DIN A4 doppelseitig 2021 - Abschrift).rpt
* NEW: BAW-BG-ABI (DIN A4 doppelseitig 2021).rpt
* NEW: BAW-BG-ABI (DIN A4 doppelseitig 2021 - Neuausstellung).rpt
* CHANGE: Unfallbericht.rpt (Aufteilung für Sichtfensterumschlag, SB-Vornamen ergänzt, Schulleiter Vor- und Nachname wird ausgegeben)
* FIX: Schülerliste (mit Sorgeberechtigten).rpt
* FIX: Schülerliste (mit Sorgeberechtigten französisch).rpt
* FIX: Schülerliste (mit Sorgeberechtigten deutsch).rpt
* FIX: BER-KO-AS (Schul Z 322)(03.11).rpt

## 7.1.20 - 715 (29.10.2020)

### MAGELLAN SCHULVERWALTUNG

* CHANGE: Optimierung der Abfragen beim Aufruf der Schülerregister: Der Aufruf von `Schüler > Daten1` dauerte länger als die Aufrufe der weiteren Registerkarten, da bei diesem Aufruf bereits Daten für weitere Karten geladen wurden. Die jeweils aufgerufenen Daten wurden jetzt je Register verteilt. 
* NEW: neue Felder in der Sammelzuweisung der `Schüler` und `Bewerber`:
  * `Daten2 > höchster Abschluss > Schulform`
  * `Daten2 > höchster Abschluss > Abschluss`

## 7.1.19 - 715 (22.10.2020)

### MAGELLAN SCHULVERWALTUNG

* FIX: Anlegen eines neuen Sorgeberechtigten aus `Schüler > Daten1` und `Bewerber > Daten1`
* FIX: Anlegen eines neuen Sorgeberechtigten aus `Schüler > Daten1` und `Bewerber > Daten1`, wenn keine Gemeindekennziffern und Postleitzahlen im Verzeichnis vorhanden sind
* CHANGE: Die Größe des Schülerfehlzeiten-Fenster kann verändert werden
* FIX: Unter `Schüler > Laufbahn > Allgemein` wurde die Anzeige der Bezeichnungen der Verzeichnisfelder überarbeitet
* FIX: Unter `Schulen > Daten` werden Änderungen beim Datensatzwechsel oder Ansichtswechsel gespeichert
* FIX: Sammelzuweisung unter `Schüler > Laufbahn > Allgemein/Abschluss` überarbeitet
* FIX: Sammelzuweisung unter `Schüler > Zeugnis > Details` überarbeitet
* NEW: Beim Seriendruck an Sorgeberechtigte vom Schüler aus kann auf das Feld Ergänzungen (`Sorgeberechtigte > Daten > Ergänzungen`) mit dem Seriendruckfeld «Sorgebe_Adresszusatz» zugegriffen werden
* NEW: Unter `Schüler/Bewerber/Lehrer/Personen/Sorgeberechtige/Mandanten/Betriebe/Schulen > Daten > PLZ` können auch Postleitzahlen erfasst werden, die nicht im Verzeichnis Postleitzahlen gespeichert wurden oder die dort gespeichert wurden, für die aber kein Verweis auf eine passende Gemeindekennziffer existiert
* CHANGE: Unter `Berufsschule > Matrix > Sammelzuweisung` wird standardmäßig das Häkchen zum `Fächer kopieren` nicht gesetzt angezeigt
* NEW: Wenn Betriebe gelöscht werden sollen, erscheint ein Fenster, das die Möglichkeiten bietet aus der markierten Auswahl alle Betriebe zu löschen oder nur die Betriebe, denen keine Auszubildenden zugeordnet wurden. Wird ein Betrieb gelöscht, dem Auszubildende zugeordnet waren, bleibt die Schülerausbildung (`Schüler > Ausbildung`) bestehen, wenn hier weitere Informationen hinterlegt wurden (bspw. Bildungsgang, Beruf usw.)
* FIX: Unter `Schüler > Merkmal > MerkmalA1` können Merkmale genutzt werden, die bis zu 20 Zeichen im Feld Kürzel verwenden.
* FIX: Anzeigeverhalten des Feldes und der Verzeichnisliste `Schüler/Bewerber > Daten2 > Bereits besuchte Schule > letzte Klassenstufe` korrigiert
* FIX: `Menü Bewerber > Register Bewerber > Sammelzuweisung > Ausbildungsdaten`: Ein neuer oder geänderter Ausbildungsdatensatz wird unter `Bewerber > Ausbildung` als aktuelle Ausbildung gesetzt
* FIX: Schreibfehler im benutzerdefinierten Filter korrigiert
* FIX: `Schüler > Daten2 > Bereits besuchte Schulen > Herkunftsschule`: Die Auswahl einer neuen Herkunftsschule wird beim Wechsel in ein anderes Register gespeichert

### MAGELLAN Schnittstellen

#### NRW

* CHANGE: Für Berufskollegs: Wenn der Schüler nicht Status `Neuzugang von einer anderen Schule` hat und keine `Versetzungsart` gewählt ist, wird immer eine `0` ausgegeben, auch wenn die Versetzung nicht gefüllt ist.

### MAGELLAN ADMINISTRATOR

* CHANGE: `Benutzerverwaltung > Zugriffsrechte synchronisieren` Der Assistent endet mit `Schließen`.

### MAGELLAN Bibliothek

* CHANGE: Geändertes Verfahren zur Erstellung von Barcodes
* NEW: Im Menü `Mahnwesen` stehen für den Seriendruck der Name und die Adressdaten des Schülers zur Auswahl. Alle verfügbaren Seriendruckfelder je Menüpunkt listen wir hier auf: [https://doc.magellan7.stueber.de/bibliothek/tutorial/referenzen/](https://doc.magellan7.stueber.de/bibliothek/tutorial/referenzen/)
* FIX: Ausleihe ohne Bestätigung unterbunden
* FIX: Buchung falscher Medien unterbunden

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: NRW-ABI-AZ  (Anlage D42).rpt (Korrektur Ausbildung zeitraumbezogen)
* NEW: BER-Schul Z 251 (11.19).rpt (Schul Z 251 – Zeugnis des Gymnasiums, Jahrgangsstufen 5 und 6 – (11.19))

## 7.1.18 - 715 (30.09.2020)

### MAGELLAN SCHULVERWALTUNG

* CHANGE: Crystal Reports Runtime-Version aktualisiert
* FIX: Korrekturen beim Versetzen von Schülern in Nachbarmandanten (Herkunfstschule wird übertragen, Prüfung ob Sorgeberechtigte bereits vorhanden sind)
* NEW: Schüler, die in Nachbarmandanten versetzt werden, können optional statt als Vagabunden (Standard) als Bewerber übertragen werden. 

![Schüler als Bewerber in Nachbarmandanten versetzen](/assets/images/changelog/7.1.18.01.png)

### MAGELLAN Schnittstellen

#### SAXSVS

* FIX: erweiterte Fehlerausgabe beim Export, ID und Klasse des betroffenen Schülers werden ausgegeben
* NEW: Neue Meldungen, siehe Tabelle

Art|Feld|Meldung|Hintergrund
--|--|--|--
Fehler|<aau_ausbetr><staat> (Ausland)|Vorname Nachname (SchülerID): Das Feld "<aau_ausbetr><staat> (Ausland)" darf nicht leer sein.|Erscheint wenn das `Land` und die `Gemeindekennziffer` des Ausbildungsbetriebs nicht gefüllt sind. Ein nicht gefülltes Land beim Betrieb wird automatisch als `De` interpretiert, es wird für Betriebe aus Deutschland aber der Eintrag einer Gemeindekennziffer erwartet.
Fehler|	<al_abschl_dat>|Vorname Nachname (SchülerID): Das Feld "<al_abschl_dat>" unterscheitet den Mindestwert von 01.01.2016|Erscheint wenn das Bis-Datum der Ausbildung (`MAGELLAN > Schüler > Ausbildung > Ausbildung editieren > Ausbildung bis`) nicht korrekt ist.
Fehler|	<sorgeberechtigte>|"Der Sorgebe Vorname Nachname hat fehlerhafte Wohnortangaben (Gemeinde, Land) eingetragen. <br/>Bei Wohnort in Deutschland, muss eine Gemeindekennziffer angegeben werden."|Erscheint für Sorgeberechtigte, denen keine Gemeindekennziffer zugewiesen wurde, der Eintrag im Feld `Land` aber D, De oder Deu ist.

* NEW: <as_staat> (Land des Sorgeberechtigten): Hier werden bisland die Einträge D, De, Deu, CZ, PL, CH in die richtigen Schlüsselwerte umgesetzt. Ergänzt wurde für Österreich der Wert AT.
* NEW: Neue Prüfung für Sorgeberechtigte (aus Deutschland, also Land D, De oder Deu) ohne Gemeindekennziffer.
* NEW: Neue Betriebeprüfung: Gemeldet werden Betriebe ohne Eintrag im Feld `Land` und `Gemeinde`
* NEW: Hat ein Betrieb nur einen Eintrag im Feld `Gemeinde` und das Feld `Land` leer, wird für SaxSVS das Land automatisch als `De` ausgespielt.

## SHL

* FIX: Ausgabe der Exportdateien

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Allgemein

* FIX: Schüler > Drucken > Berichte > Schülerliste (Fehlzeiten nach Schüler gruppiert).rpt
* FIX: Abitur > Drucken > Prüfungslisten drucken > Prüfungsliste (Abitur).rpt

#### Berlin

CHANGE: BER-KO-ABI (Schul Z 323)(03.11).rpt (Ausdruck aus MAGELLAN 7 jetzt möglich)
CHANGE: BER-KO-AZ (Schul Z 321)(03.11).rpt (Ausdruck aus MAGELLAN 7 jetzt möglich)
CHANGE: BER-KO-AS (Schul Z 320a-b)(03.11).rpt (Ausdruck aus MAGELLAN 7 jetzt möglich)
NEW: BER-Schul Z 324 (11.19).rpt (Bericht war bereits in MAGELLAN 6 Auslieferung enthalten, nun auch für MAGELLAN 7 verfügbar)

## 7.1.17 - 715 (08.09.2020)

### MAGELLAN SCHULVERWALTUNG

* FIX: `Schüler > Laufbahnprozess` "Schüler in  Mandanten versetzen"

### MAGELLAN Schnittstellen

#### Statistik NRW

* FIX: SIM.TXT: Schüler einer Klasse ohne Statistikkürzel werden beim Export nicht berücksichtigt
* FIX: SIM.TXT: wenn in `Schüler > Extras > Betreuungsarten > Innerschulisch 1` [Betreuungen innerschulisch (Schüler)] kein Eintrag vorhanden ist, ist das das Feld Betreuung leer
* FIX: SIM.TXT: Ausgabe von Foerderschwerp, VOfoerderschwerp, VOschwerstbeh, Foerderschwerp2, VOfoerderschwerp2 ohne Eintrag des BIS Datums. Der Eintrag eines BIS-Datum ist nicht zwingend erforderlich, das VON-Datum muss kleiner oder dem dem Anfangsdatum des jeweiligen Zeitraumes sein.
* CHANGE: ABI.TXT (ABS) um Schüler aus gemischten Jahrgängen G8 und G9 korrekt auszuspielen, ist eine Eintrag unter `Klassen > Zeiträume > Klassenstufe` (Schlüssel) Q2 notwendig
* FIX: ABS + BBS: Ausgabe aus dem Feld `Versetzung` angepasst. Auszug aus der Dokumentation unter [https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/](https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/)

![Feld Versetzung](/assets/images/changelog/7.1.16.01.png)

#### Schüler (Berlin)

* FIX: Schüler (ABS und BBS) bewerber > schueler)_sorgebe.export.csv - bei mehreren eingetragenen Sorgeberechtigten werden auch mehrere Sorgeberechtigte ausgespielt

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Auslandsschulen

* CHANGE: DAS-HJZ-JZ (3-12).rpt
* CHANGE: DAS-GS-GY (Klasse 3-10).rpt
* CHANGE: DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23).rpt

#### Saarland

* Change: SAR-GEMS-AZ (Klasse 5-10).rpt (folgendes ist nun berücksichtigt und wird durch Setzen oder Nicht-Setzen des Hakens im Menü `Schüler > Daten 3` im Feld "Schulpflicht erfüllt" gesteuert:

Fälle | Auswirkung im Bericht
-- |--
1) Abgang vor Erfüllung der Vollzeitschulpflicht | AZ mit Angabe der Fehlzeiten (entschuldigt und unentschuldigt), Noten in Verhalten und Mitarbeit
2) Abgang nach Erfüllung der Vollzeitschulpflicht |  AZ ohne Verhalten und Mitarbeit und ohne Fehlzeiten, diese erscheinen dann im Verhaltenszeugnis.

![Feld "Schulpflicht erfüllt"](/assets/images/changelog/7.1.17.01.png)
   


## 7.1.16 - 715 (26.08.2020)

### MAGELLAN Schnittstellen

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: SAR-APO-DFG-2014.dws: PreCheckPruefungsbereichFehler

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Allgemein

* CHANGE: `Klassenliste mit Schülersummendaten.rpt` Jahrgang der Klasse wird mit ausgegeben

## 7.1.15 - 715 (20.08.2020)

### MAGELLAN SCHULVERWALTUNG

* FIX: Korrekturen beim Versetzen von Schülern in Nachbarmandanten

### MAGELLAN Schnittstellen

#### SAXSVS

* FIX: Korrektur beim Erzeugen einer SAXSVS-Datei Abschlüsse/Abgänger: doppeltes Ausspielen von Schülern bei gleichzeitigem Abgang und Abschluss in verschiedenen Zeiträumen behoben

#### Statistik NRW

* FIX: Ausgabe in das Feld `Versetzung` korrigiert

#### SchülerOnline

* NEW: Die importierte Ausbildung der Bewerber wird automatisch als aktuelle Ausbildung markiert.
* CHANGE: Beim Importieren wird der Bildungsgang als Bildungsgang gesetzt

### MAGELLAN ADMINISTRATOR

* FIX: `schueler_laufbahn.import.csv` Zuordnen zu Klassen korrigiert
* FIX: Auffüllen von leeren Datumsfeldern korrigiert

### MAGELLAN Bibliothek

* FIX: Problem bei der Rückgabe von Büchern behoben

![Meldung bei der Ausleihe eines mit "Dauerverleih" markierten Exemplares](/assets/images/changelog/7.1.14.01.png)

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Allgemeine Berichte

* NEW: Mandant (Liste der Schüler ohne aktuelle Ausbildung - trotz gefüllter Ausbildungsliste - im Zeitraum).rpt
* CHANGE: Abi (Gesamtschnitt nach Punktzahl sortiert).rpt

#### Baden Württemberg

* NEW: BAW-GY-HJZ (Kursstufe mit BLL).rpt (Halbjahreszeugnisse der Kursstufe mit Ausgabe der Besonderen Lernleistung, Fach RELIGION / ETHIK wird nun im Bereich der gesellschaftswissenschaftlichen Fächer mit ausgegeben)
* NEW: BAW-GY-ABI (2019 mit KF-LK).rpt (Abiturzeugnis gültig ab Abitur 2019)
* NEW: BAW-GY-JZ (Mittelstufe).rpt
* NEW: BAW-GY-JZ (Mittelstufe mit GER)(A5).rpt (Jahreszeugnis für die Mittelstufe mit Ausgabe der Sprachreferenz, DIN A5)
* CHANGE: BAW-GY (Mitteilung Prüfungsergebnisse).rpt (Ausgabe Schuljahr)

#### Sachsen

* NEW: SAC-BVJ-HJI (A.01.03).rpt (A.01.03 Halbjahresinformation der Berufsschule - Berufsvorbereitungsjahr)
* CHANGE: SAC-BS-HJI (A.01.02).rpt
* CHANGE: SAC-BVJ-AS mit HS (A.01.09).rpt (Hauptschulabschluss wird nun beim `Schüler > Laufbahn > Abschluss` im Bereich „Abschluss1“ im Feld „Abschlussart“ abgefragt. Grundlage bildet das `Schlüsselverzeichnis > Abschlussarten`.)
* CHANGE: SAC-BF-JZ (B.02.02).rpt
* CHANGE: SAC-BS-BVB Maßnahme (A.01.05).rpt
* CHANGE: SAC-BS-HJI (A.01.04).rpt
* CHANGE: SAC-BS-AS (Vorbereitungsklasse) (A.01.06).rpt
* CHANGE: SAC-BS-JZ (A.02.01).rpt
* CHANGE: SAC-BS-JZ (A.02.01) 2spaltig.rpt
* CHANGE: SAC-BS-AZ (A.02.04).rpt

#### Saarland

* CHANGE: SAR-GEMS-AS (Klasse 9 mit Prüfung)(ab 2020).rpt
* CHANGE: SAR-GEMS-AS (Klasse 9 ohne Prüfung)(ab 2020).rpt
* CHANGE: SAR-AS-Verhaltenszeugnis.rpt
* CHANGE: SAR-AZ-Verhaltenszeugnis.rpt

## 7.1.14 - 715 (16.07.2020)

### Datenstruktur

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* NEW: Tabelle SchuelerFachdaten: `HJ1_Bestanden` bis `HJ6_Bestanden` entfernt und durch `Bestanden` ersetzt

### MAGELLAN SCHULVERWALTUNG

* FIX: Unter `Schüler > Zeugnis > Details` werden für `Verhalten` und `Mitarbeit` Noten und Füllwerte gezeigt.
* NEW: NRW: Unter `Schüler > Zeugnis > Leistungen` gibt es das Feld `Bestanden`. In dem Feld ist festhaltbar, ob der Kurs bestanden, nicht bestanden oder nicht belegt wurde. Diese Eingabe wird beim Synchronisieren der Daten mit ins Menü `Abitur` übergeben und je Halbjahr (E1-Q4) abgebildet. Bitte beachten Sie den Abschnitt ["Bestanden" und "Leistungsart"](https://doc.magellan7.stueber.de/schulverwaltung/howto/Oberstufe/sync/#bestanden-und-leistungsart) im Kapitel [Schüler synchronisieren](https://doc.magellan7.stueber.de/schulverwaltung/howto/Oberstufe/sync/)
* FIX: `Schüler > Daten4` neue Fahrtstrecke kann gespeichert werden
* FIX: Filterbezeichnungen korrigiert
* FIX: Die Zugriffsrechte für das Modul `Abitur` (damit für das Erfassen der schriftlichen Prüfungsnoten) wurden für die Rechtegruppen Schulleitung1, Sekretariat1 erweitert. Zusammengefasst haben hier Änderungsrechte: Kollegium5, Schulleiter1, Schulleiter2, Sekretariat1, Sekretariat2, MandantenAdmin und der sysdba. Bitte führen Sie das Synchronieren der Zugriffsrechte im MAGELLAN Administrator unter `Benutzerverwaltung > Menüleiste "Zugriffsrechte synchronisieren"` aus um die Rechte für bestehende Benutzerkonten zu erweitern.
* FIX: `Abitur > Prüfungen`: Wenn das Häkchen für "Lernleistungen einbringen" als letzte Aktion vor dem Auslösen der Berechnung gesetzt wird, wird es durch die Aktion des Berechnens nicht deaktiviert.

### MAGELLAN Schnittstellen

* FIX: SAXSVS: Problem beim Ausspielen der Förderschwerpunkte für Schüler mit IDIntern behoben.
* CHANGE: Hinweise,  wie mit erneut auftauchenden Schülern im Import umgegangen wird, überarbeitet: [https://doc.ls.stueber.de/sachsen/import_saxsvs/#prufung-von-schulerdaten](https://doc.ls.stueber.de/sachsen/import_saxsvs/#prufung-von-schulerdaten)

### MAGELLAN ADMINISTRATOR

* FIX: Beim Übertrag von MAGELLAN 6 nach MAGELLAN 7 wird die Datenstruktur 674 erwartet 

### MyMAGELLAN-CENTER

* FIX: Mym-Datei mit mit pauschalem Kennwort erstellen

### MAGELLAN BIBLIOTHEK

* FIX: Beim Versuch eines mit "Dauerverleih" markierten Buches wird die nachfolgende Meldung ausgegeben. Exemplare können per Sammelzuweisung über das Feld "Bestandsstatus" mit `Dauerverleih` (Sie haben das Buch in eine andere Bibliohtek ausgeliehen) oder als `Dauerleihgabe` (Sie haben das Buch dauerhaft aus einer anderen Bibliothek ausgeliehen) markieren.

![Meldung bei der Ausleihe eines mit "Dauerverleih" markierten Exemplares](/assets/images/changelog/7.1.14.01.png)

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: `Synchronisiere Abi` wurde angepasst, es werden die Daten aus dem Feld `Bestanden` (aus Schüler > Zeugnis > Leistungen) mit ins Abitur synchronisiert
* CHANGE: `Synchronisiere Zugriffsrechte` wurde angepasst, siehe Hinweise im Abschnitt MAGELLAN SCHULVERWALTUNG:

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: SAC-FS-AS mit FHReife (C.01.06).rpt (automatische Durchschnittsnoteberechnung korrigiert, die Durchschnittsnote ergibt sich aus allen Zeugnisnoten mit Ausnahme der Fächer Sport, Religion und Ethik sowie mit Ausnahme aller nachrichtlich ausgewiesenen Fächer (Noten))


## 7.1.13 - 714 (08.07.2020)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* NEW: Tabelle SchuelerFachdaten: neues Feld `Durchschnitt` 
* NEW: Tabelle SchuelerFachdaten: neue Felder `HJ1_Bestanden` bis `HJ6_Bestanden`

### SchuelerOnline

* INFO: Wir haben SchuelerOnline gemeldet, dass aktuell die beiden Felder Schulnr und Schulbez nicht korrekt übergeben werden. Es wird in Kürze in SchuelerOnline angepasst, bis dahin passen Sie bitte die Spaltenköpfe für dem Import per Hand an.

Verkehrt|Korrekt
--|--
Schulnummer|**Schulnr**
Schulbezeichnung|**SchulBez**

* FIX: `NRW > Import > SchuelerOnline > Betriebe aktualisieren`: Die Funktion wurde aktualisiert
* CHANGE: HTML-Breaks (`<br/>`) werden beim Einlesen aus SchülerOnline-Dateien ignoriert

### MAGELLAN

* CHANGE: Aus der Filterung der Schülerauswahliste nach Vagabunden steht `Rechtsklick > Status` nicht mehr zur Verfügung
* FIX: Rechtegruppe Kollegium5: Änderungen der Laufbahn werden auch beim Weiterschalten zum nächsten Datensatz gespeichert.
* FIX: Problem beim Anlegen `Unterpunkten` im Verzeichnis `Fächer (Themen)`behoben 

### MAGELLAN BIBLIOTHEK

* FIX: Passbilder, die für bereits als Medienausleiher angelegte Schüler in der Schulverwaltung aktualisiert wurden, werden auch in der Anzeige in der Bibliothek angepasst
* FIX: Klasse und Klassendaten werden nach Änderung in der Schulverwaltung auch für die Bibliothek übergeben.    

#### Statistik

* NEW: ABS-Nordrhein-Westfalen Statistikmodul 2020. Beachten Sie bitte die aktualisierten Schlüsselverzeichnisse und die aktualisierte Dokumentation ["Statistikdokumentation für NRW"](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/).

#### MAGELLAN Berichte

Die Dokumentation unserer Berichtsdateien finden Sie unter [https://doc.la.stueber.de/berichte/01_uebersicht/](https://doc.la.stueber.de/berichte/01_uebersicht/).

* CHANGE: In den nachfolgend genannten Berichten wurde die Ausgabe der Fremdsprachenreferenzen ergänzt.

  * Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Mittelstufe mit Beurteilung).rpt
  * Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 11).rpt
  * Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 13).rpt
  * Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 13).rpt

![Ausgabe der Fremdsprachen und Referenzen](/assets/images/changelog/7.1.13.01.png)

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: BER-BFS-Matrix-2016 
* NEW: BER-IBA-HJ-2020 
* NEW: BER-IBA-AS-2020 
* CHANGE: SAC-APO-BGY-2017 (Schulfremde).dws
* CHANGE: SAC-APO-BGY-2017.dws

## 7.1.12 - 713 (30.06.2020)

### MAGELLAN

* FIX: `Betriebe > Auswahl > Betriebe zusammenführen`Anzeige der korrekten Datensätze
* FIX: `Schüler > Daten 1 > Familie` Anzeige des Verhältnisses
* FIX: `Bewerber > Daten 1` beim Anlegen eines neuen Sorgeberechtigten, wird die Gemeindekennziffer vorbelegt
* FIX: Nebenschüler mit Ausbildungsbetriebe werden als Auszubildende beim Betrieb angezeigt
* FIX:  Bei Änderungen der Laufbahn (ohne Speicherung über den laufbahnkarten-bezogenen Speicherhaken) und auf den nächsten Datensatz weiterschalten. Hier erschien die Meldung "Kein Änderungsrecht"

#### Statistik

* NEW: BBS-Nordrhein-Westfalen Statistikmodul 2020. Beachten Sie bitte die aktualisierten Schlüsselverzeichnisse und die aktualisierte Dokumentation ["Statistikdokumentation für NRW"](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/).

#### MAGELLAN Berichte

* NEW: Das Modul `MAGELLAN Berichte` fällt weg, die Dokumentation der Berichte erfolgt ab dieser Version ausschließlich im Bereich Berichte der Dokumentation [Landesanpassung unter https://doc.la.stueber.de/berichte/01_uebersicht/](https://doc.la.stueber.de/berichte/01_uebersicht/)!

### MAGELLAN ADMINISTRATOR

* FIX: `Datenaustausch > Kataloge importieren` 00_Raeume.keys importierbar

### Skripte

* FIX: SHL-APO-2018: Anpassung Fachanforderungen Sport: kaufmännische Rundung nur am Schluss: ((schr. Note des 3. Prüfungsfaches x 2) plus Note1 (Fachpraxis) plus Note2 (Fachpraxis)) geteilt durch 4.
* FIX: SAC-APO-BGY-2017: Mit den Änderungen durch Artikel 2 der Verordnung vom 24. Juli 2018 entfällt jegliche Unterscheidung nach den Fachrichtungen. Somit muss in MAGELLAN im `Schlüsselverzeichnis > Verordnungen` auch nicht mehr der Wert für "Typ" eingetragen werden. Das Skript berücksichtigt, dass die 2. Fremdsprache nicht mehr zwingend belegt werden muss. Beim Markieren werden nur 26 GKs (zuvor 28 GKs) gekennzeichnet. 
Aktualisierte Beschreibung zum Skript unter https://doc.la.stueber.de/11.sac/sac-apo-bgy-2017/.
* CHANGE: NRW-APO-BK-2012: Neben der Unterrichtsart DB iwrd nun auch die Unterrichtsart Diff berücksichtigt. Aktualisierte Beschreibung zum Skript unter https://doc.la.stueber.de/08.nrw/nrw-apo-bk-2012/

### MyMAGELLAN

* FIX: Installationspaket vervollständigt, bei reinen MyMAGELLAN-Installationen erschien beim Eintrag von Schülerbemerkungen eine Meldung, die auf eine fehlende Datei hinwies.

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie ab sofort im Bereich "Berichte" der Dokumentation [Landesanpassung unter https://doc.la.stueber.de/berichte/01_uebersicht/](https://doc.la.stueber.de/berichte/01_uebersicht/)


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
* NEW: SAC-FS-AZ (C.01.04).rpt (C.01.04 Abgangszeugnis Fachschule)
* NEW: SAC-FS-AS mit FHReife (C.01.06).rpt (C.01.06 Abschlusszeugnis Fachschule mit FHReife)
* NEW: SAC-FS-AS (C.01.05).rpt (C.01.05 Abschlusszeugnis Fachschule)

#### Saarland

* NEW: SAR-FHReife (Nachweis)(GOS2.0) Zweitschrift.rpt
* NEW: SAR-FHReife (Nachweis)(GOS2.0).rpt
* NEW: SAR-GEMS-AS (Klasse 9 ohne Prüfung)(ab 2020).rpt
* NEW: SAR-GEMS-AS (Klasse 9 mit Prüfung)(ab 2020).rpt

## 7.1.11 - 713 (02.06.2020)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* NEW: Tabelle `Leistungsarten`
* NEW: SchuelerAbiDetails:
  * `HJ1_Leistungsart` bis `HJ6_Leistungsart`
  * `HJ1_Bestanden` bis `HJ6_Bestanden`
* NEW: Schuelerfachdaten: `Leistungsart`

### MAGELLAN

* NEW: Schlüsselverzeichnis `Leistungsarten` mit Arten (Schriftlich, mündlich, praktisch) und gleichnamiges Feld unter `Schüler > Zeugnis > Leistungen`.
  * * Dieses Feld wird für die Oberstufe in NRW benötigt. Man legt sich seine Arten der Leistung an (Beispiel Vortrag, Klausur usw) und markiert sie mit der korrekten Art (Beispiel: Klausur = schriftlich). Bei den Schülern wird unter `Schüler > Zeugnis > Leistungen` jedes Fach mit der vom Schüler gewählten Leistungsart markiert. Diese Leistungsart wird je Kurshalbjahr beim Synchronisieren der Daten mit ins Menü `Abitur > Qualifikation` übernommen. Die Leistungsart wird nur für benotete Fächer übernommen.
* NEW: Unter `Abitur > Qualifikation` kann je Fach und Kurshalbjahr der Kurs als bestanden markiert werden. Diese Eingabe ist für die Oberstufe in NRW gedacht.

* CHANGE: `Bewerber > Bewerbungsdaten > Fachdaten > Externe Prüfung der Fremdsprache(n)` Aus der Checkbox wurde eine Werteliste mit den Werten `bereits absolviert` und `angestrebt` eingefügt.
* CHANGE: `Bewerber > Bewerbungsdaten > Verfahren > Einschätzung` Die Benennung der rechten Spalte wurde von `Bewerber` in `Kollegiat/in` geändert.

* FIX: Unter `Extras > Schlüsselverzeichnisse > Fächer` kann ein versehentlich erfasster `Aufgabenbereich` entfernt werden.
* FIX: `Schüler > Extras > Import`Import SchuelerOnline Betriebe und Ausbildungsdaten
* FIX: `Schüler > Laufbahnprozess > Schüler einschulen` bei der Kopie eines Schülers wird beim Einschulen die Herkunftsschule aktualisiert
* FIX: Bei der Änderung eines Schlüsselverzeichnisses während der Bereich `Schüler > Zeugnis` geöffnet war, erschien eine Meldung
* FIX: Problem beim Synchronisieren von Schülern in die Berufsschulmatrix behoben (`Synchronisiere BBS.dws`)
* FIX:Eintrag unter `Sorgeberechtigte > Arbeitgeber` wieder möglich
* FIX: `Sorgeberechtigte > Arbeitgeber` - Schaltflächen werden jetzt korrekt aktiviert
* FIX: `Klassen > Zeiträume > ENBREA Leistungsprofile > Dialogfenster Kurse definieren`  - Die Überschriften wurden überarbeitet, der blaue Hintergrund entfernt  


### MAGELLAN ADMINISTRATOR

* FIX: Reihenfolge beim Einlesen der Dateien aus dem MAGELLAN Importformat korrigiert

### Skripte

* CHANGE: `Importier SDTF.dws` Beim Übertrag von Schülerkurswahlen (`nur geänderte Daten`) von DAVINCI nach MAGELLAN werden die Schülerfachdaten in MAGELLAN nicht mehr geändert, wenn die Fachkombinationsnummer in DAVINCI verändert wurde. Bitte beachten Sie die angepasste Dokumentation: [Abgleich mit DAVINCI: Schülerkurswahlen mit der Option "nur geänderte Daten" ](https://doc.magellan7.stueber.de/schulverwaltung/howto/abgleich_mit_dav/#import-mit-nur-geanderte-daten)
* CHANGE: `Synchronisiere Abi.dws`: Beim Synchronisieren der Schülerdaten wird für benotete Fächer der Eintrag aus `Schüler > Zeugnis > Leistungen > Leistungsart` übernommen.

* FIX: `Exportiere SDTF.dws` beim Übertrag von Schülerkurswahlen Auswahl nur bestimmter Schüler
* FIX: `Importiere SDTF.dws` Problem beim Zuordnen von P1-Daten beim Übertrag aus DAVINCI nach MAGELLAN (Schülerkurswahlen) behoben.
* FIX: `BER-APO-KO-2017.dws`: Anpassungen für MAGELLAN 7
* FIX: `Synchronisiere BBS.dws`

### Schnittstellen

* NEW: SHL - Schulstatistik Schnittstelle 2020/2021 freigegeben
* NEW: SAC - SAXSVS - Schnittstelle um Import erweitert. Dokumentation zu finden unter [Import von Daten aus SaxSVS nach MAGELLAN](https://doc.ls.stueber.de/sachsen/import_saxsvs/)
* NEW: SAC - SAXSVS - Schnittstelle um Exportdatei mit  Abgängern/Abschlüssen erweitert
  
* CHANGE: SAC - SAXSVS - Export der Betriebedaten auch, wenn nur Ausbildungs- oder Praxisbetrieb angegeben wurde.
  
* FIX: SAC - SAXSVS - Detailverbesserungen und Sonderfälle beim Export berücksichtigt
* NEW: In SAXSVS wird jeweils der Eintrag des Einstellungsbetriebs (MAGELLAN-Ausbildungsbetrieb) UND der Ausbildungsbetriebs (MAGELLAN-Praxisbetrieb) erwartet. Ist einer der beiden Betriebe nicht erfasst, wird alternativ immer der jeweils andere Betrieb ausgegeben. Sie müssten also, wenn der Einstellungs- und der Ausbildungsbetrieb identisch sind, nur einen der beiden Betriebe erfassen.  

### MAGELLAN-Skripteditor

* CHANGE: überarbeitete Version

### MAGELLAN Bibliothek

* FIX: Löschen von Exemplaren funktioniert wieder
* FIX: Optionen können von Benutzern mit Rechten für die Bibliothek geändert werden

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* CHANGE: Schülerpersonalblatt (Überprüfung Stammdaten).rpt (PraxisBetrieb Name 1 und Name 2 werden ausgegeben)

#### Berlin

* NEW: BER-Schul Z 256 (2019.2020).rpt

#### Sachsen

* FIX: SAC-BG-ABI (E.01.06).rpt (Zeugnisbemerkungen aus dem Menü Abitur > Zeugnisbemerkungen werden nun im Bericht angezeigt, Ausgabe der Fachrichtung des Schülers erweitert. Für die Ausgabe der Fachrichtung müssen Sie entweder das Berufsfeld einer Klasse definieren oder das des Schülers.)
* FIX: SAC-FOS-AZ (D.01.03).rpt (Umbruch bei den Fachbezeichnungen im Pflichtbereich korrigiert)
* NEW: SAC-BVJ-AS (A.01.10).rpt (Zeugnis der Berufsschule Berufsvorbereitungsjahr)
* NEW: SAC-BGJ-AS (A.01.11).rpt (Zeugnis der Berufsschule Berufsgrundbildungsjahr)

#### Niedersachsen

* FIX: NIE-GY (Studienbuch - Einführungsphase) G9.rpt (im Bereich Sport wird nun die Null beim Punktwert vorangestellt, Wahlb-Fächer (Fachstatus = Wahlb) werden wieder korrekt nur im Bereich der Wahlfächer ausgegeben)

### Auslandsschule

* FIX: DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt (Korrektur Seite 2, Ausgabe Schüler/In, Anpassungen gemäß der Vorgaben *Handreichungen für die Sekundarstufe I an Deutschen Schulen im Ausland für Zeugnisse und Statistik (Beschluss des Bund-Länder-Ausschusses vom 25.09.2019)*)
* NEW: DAS-GY-ABI (DIA)(2020)(keine mdl. Prüfung möglich).rpt

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: Zeugnisse\Berlin\BER-RS-AS (Schul Z 241)(07.10).rpt
* CHANGE: Zeugnisse\Berlin\Schleswig-Holstein\SHL-GY-AS (Klasse 5-10)(G8).rpt

## 7.1.10 - 712 (05.05.2020)

### MAGELLAN

* FIX: Fertigstellen-Button im `Extras > Exporte > Untis` wird aktiviert  
* FIX: Beim Anlegen eines neuen Bewerbers, wird die Anzeige der Herkunftsschule unter `Daten2` korrekt aktualisiert.
* FIX: Anzeigbare Kürzellänge korrigiert für:
  * `Bewerber > Höchster Abschluss ABS > Abschluss`
  * `Bewerber > Höchster Abschluss ABS > Bildungsgang`
  * `Bewerber > Höchster Abschluss BBS > Abschluss`
  * `Bewerber > Höchster Abschluss BBS > Beruf`
  * `Bewerber > Höchster Abschluss BBS > Bildungsgang`
* FIX: Bearbeiten von `Schüler > Zeugnis > ENBREA Leistungen`und `Schüler > Zeugnis > ENBREA Kurse` mit Kollegiums, Sekretariats- und Schulleitungsrechten möglich
* FIX: `Import > Untis` (korrigiertes Skript `Importiere SDTF.dws`)
* FIX: `EXport > Untis` (korrigiertes Skript `Exportiere SDTF.dws`)
* FIX: `Schueler > Extras > Importe > SchuelerOnline` Betriebedaten werden importiert

### MAGELLAN Administrator

* FIX: Synchronisiere Zugriffsrechte.dws Fehlermeldung "Mit Fehlern abgeschlossen" bei korrektem Durchlauf entfernt
* FIX: Zuweisen von Zugriffsrechten.dws `Klassen > Klassen übernehmen` mit dem Recht Schulleitung 1 und Mandanten Administrator
  
### MyMAGELLAN-CENTER

* FIX: MyMagellan Dateien werden zum Einlesen korrekt (mym7 oder mymx) erkannt

### MyMAGELLAN

* FIX: Anzeige der Inhalte der Verzeichnisfelder unter `Schüler > Zeugnisdaten korrgiert`
  * CHANGE: Die Anzeige der `Beurteilungsarten` unter `Fächer` ist angepasst worden. Statt des Drop-Downfeldes, sind jetzt Radio-Buttons verwendet worden, die dem Benutzer die gefilterte Darstellung der Liste nach der Beurteilungsart verdeutlichen. Bitte beachten Sie die angepasste Dokumentation unter [https://doc.mymagellan7.stueber.de/noteneingabe/#eingabe-nach-fachern](https://doc.mymagellan7.stueber.de/noteneingabe/#eingabe-nach-fachern)
* CHANGE: Beim Öffnen der Ansicht `Fächer` ist wie bisher die Vorauswahl so getroffen, dass alle Schülerzeilen zum Fach gezeigt werden. In dieser Ansicht ist kein Editieren möglich. Bitte wählen Sie vor der Eingabe der Ergebnisse die gewünschte Beurteilungsart aus.
* FIX: Problem bei der Anzeige der Beurteilungsart in der Ansicht `Fächer` behoben.
* FIX: Problem bei der Eingabe in der Fächeransicht und Anzeige in der Schüleransicht behoben.
* FIX: Anzeige von Füllwerten korrigiert
* FIX: spaltenbezogene Filterkriterien in der Ansicht `Fächer` sichtbar

### MAGELLAN Bibliothek

* FIX: Problem beim Übernehmen von Personen als Ausleiher behoben

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Sachsen

* FIX: SAC-FOS-FHReife (D.01.04).rpt (weitere Zeugnisbemerkungen werden wieder korrekt ausgegeben)

### Nordrhein Westfalen

* CHANGE: NRW-APO-BK-2012 und NRW-APO-2012 Abschaffung der so genannten „Abweichungsprüfungen“, (d.h. verpflichtende mündliche Prüfungen im ersten bis dritten Abiturfach bei einer Abweichung der Prüfungsnote von der Vornote von vier oder mehr Punkten)


## 7.1.9 - 712 (07.04.2020)

### MAGELLAN

* NEW: Für den Seriendruck `An den Betrieb des Schülers` wurden die Felder `Bildungsgang` und `Beruf` übergeben, damit kann innerhalb von Word nach Datensätzen  eines Bildungsgangs/Berufs gefiltert werden
* NEW: Für den Seriendruck `An den Betrieb des Bewerbers` wurden die Felder `Bildungsgang` und `Beruf` übergeben, damit kann innerhalb von Word nach Datensätzen  eines Bildungsgangs/Berufs gefiltert werden
* NEW: Überarbeitung der Funktionalitäten für den Gemeindekennziffer- Automatismus in den Bereichen `Bewerber`, `Schüler`, `Sorgeberechtigte`.
* NEW: Für aus dem Familienmenü unter `Schüler > Daten1` heraus angelegte neue Sorgeberechtigte gibt es das Feld `Gemeindekennziffer`
* NEW: Wird unter `Schüler > Daten1 > Familie` ein neuer Sorgeberechtigter angelegt, wird die Gemeindekennziffer des Schülers übernommen.
* NEW: Bei Adressänderungen des Schülers, die auch die Gemeindekennziffer betreffen, wird die Gemeindekennziffer mit zu den zur Änderung markierten verknüpften Datensätzen Schülern oder Sorgeberechtigten übernommen.
  
* CHANGE: Spalte Bildungsgang wurde aus der Auswahlliste Schüler entfernt, damit wird eine Performanceverbesserung erzielt

* FIX: `Fachdaten kopieren` beim `Schüler versetzen`
* FIX: `Bewerber > Daten2`: Dateneingabe und dann Auswahl `nächster Datensatz` Fehlermeldung korrigiert
* FIX: `Schüler > Daten2 Abschluss` volle Zeichenlänge des Kürzels kann genutzt werden
* FIX: unter `Abitur > Qualifikation` ist das Feld `Abiturjahrgang` wieder gefüllt und auswählbar 
* FIX: Unter `Schueler > Daten2 > Abschluss` können Werte verwendet werden, für die unter `Extras > Schlüsselverzeichnisse > Abschlüsse (extern)` die volle Kürzellänge verwendet wurde
* FIX: das Versetzen von Schülern in Mandanten wurde überarbeitet, dabei wurde auch die Übergabe der Fremdsprache wieder mit eingebunden. Existiert die Fremdsprache (Prüfung anhand des Kürzels) nicht im anderen Mandanten, wird ein neues Fach im Verzeichnis `Fächer` angelegt und dem kopierten Schüler zugewiesen.
* FIX: Länge der Bezeichnung `Lehrämter` (Überschrift) unter `Lehrer > Daten3` angepasst
* FIX: Assistent "ENBREA-Leistungen übernehmen" - Textlänge angepasst

### MAGELLAN Administrator

* FIX: Datapump (Datenübertragung von MAGELLAN 6 nach MAGELLAN 7) optimiert

### MyMAGELLAN-CENTER

* NEW: Neues Format für mym-Dateien (*.mymx). Neu erzeugte mym-Dateien werden als verschlüsselte XML-Dateien gespeichert. Zuvor exportierte Dateien im alten Format können aber weiterhin eingelesen werden.

!!! warning "Wichtig"

    Die Dateiendung im MyMagellan-Center muss bitte vor dem neuen Export angepasst werden. Um die Änderung für viele zu machen, nutzen Sie bitte die Möglichkeit des Exports und Imports der Benutzerdaten und ersetzen bitte mit "Suchen und Ersetzen" (z.b. in Excel per STRG+H aufrufbar) in der exportierten Datei und ersetzen ".mym7" (oder ".mym") durch ".mymx".

### MyMAGELLAN

* NEW: Neues Format für mym-Dateien (*.mymx). Neu erzeugte mym-Dateien werden als verschlüsselte XML-Dateien gespeichert. Zuvor exportierte Dateien im alten Format können aber weiterhin eingelesen werden
* FIX: In der Ansicht  `Fächer` und  `Schüler` sind die Felder `schriftl.Note1` - `Endnote (gesamt)` beschreibbar.
* FIX: Filter im Bereich
* CHANGE: in der Ansicht `Schüler` und `Fächer` wird die Spalte `Kurs` als erste Spalte eingeblendet, die das Fachkürzel plus die Kursnummer ausgibt.

### MAGELLAN Bibliothek

* CHANGE: Sämtliche Optionen in der Bibliothek sind von den Benutzern mit den Bibliothekts-Rechtegruppen `Schulleitung`, `Bibliothekar` oder dem `sysdba` anpassbar. Benutzer mit den Bibliotheks-Rechtegruppen `Kollegium` oder `Gast` können keine Änderungen vornehmen, sondern die Einstellungen nur ansehen. Bitte beachten Sie den neuen Abschnitt [Optionen](https://doc.magellan7.stueber.de/bibliothek/installation/optionen/).

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

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
* CHANGE: Zeugnisse\Baden-Württemberg\BAW (Notenkonferenzliste).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-ABI (2014 - Kontrolle vor mündlichen Abi).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 11).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 12).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Jahrgangsstufe 13).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-HJZ (Mittelstufe).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Klasse5).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Mittelstufe mit Beurteilung).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-JZ (Mittelstufe).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-RS-AS.rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-RS-AZ.rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-ABI (2014 - Kontrolle vor mündlichen Abi - 2 Seite).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-ABI (2014 - Abschrift).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY-ABI (2014 - Abschrift SuS).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY (Stammkarte).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GY (Mitteilung Prüfungsergebnisse).rpt
* CHANGE: Zeugnisse\Baden-Württemberg\BAW-GS-AS.rpt

## 7.1.8 - 712 (23.03.2020)

### SAXSVS

* CHANGE:  Bedingungen zum Ausspielen des Abbruchknotens und Status angepasst

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Sachsen

* CHANGE: Berichte\Zeugnisse\BER-GY-JZ (Schul Z 251)(07.10).rpt
* CHANGE: Berichte\Zeugnisse\BER-GY-AZ (Schul Z 252) (01.07)rpt
* CHANGE: Berichte\Zeugnisse\BER-GY-FHreife Bescheinigung (Schul Z 350).rpt

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* CHANGE: Berichte\Schueler\Schülerpersonalblatt (mit Fremdsprachen) A5.rpt
* CHANGE: Berichte\Schueler\Unfallanzeige.rpt
* CHANGE: Berichte\Schueler\Unfallanzeige (mit Erläuterungen).rpt
* CHANGE: Berichte\Schueler\Unfallanzeige (in word ausfüllbar).rpt
* CHANGE: Berichte\Schueler\Schulzeitenbescheinigung (in word ausfüllbar).rpt
* CHANGE: Berichte\Schueler\Schülerstammblatt (Belegung der Arbeitsgemeinschaften).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt incl. Schuleintritt (mit Vorbildung).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt incl. Schuleintritt (Betriebe).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt incl. Schuleintritt (Betriebe -Querformat).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt (ohne Vorbildung).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt (nur mit Eltern und Vorbildung).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt (mit Vorbildung).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt (mit Vorbildung und Herkunftsschule).rpt
* CHANGE: Berichte\Schueler\Schülerpersonalblatt (mit Fremdsprachenfolge).rpt
* CHANGE: Berichte\Klassen\Zeugnisliste nach Schülerfächern (Kopfnoten).rpt
* CHANGE: Berichte\Klassen\Klassen (Fax an Betriebe der Schueler).rpt
* CHANGE: Berichte\Klassen\Jahresnotenliste-BVJ.rpt
* CHANGE: Berichte\Klassen\Anwesenheitsliste für ganzen Monat.rpt
* CHANGE: Berichte\Klassen\Anwesenheitsliste für den Tag.rpt
* CHANGE: Berichte\Klassen\Klassenliste (Zensurenstatistik nach Noten).rpt

## 7.1.7 - 712 (20.03.2020)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE: Anzeige der aktuellen Vagabunden-Ausbildung möglich
* CHANGE: Nicht erfasste Fehlzeiteneinträge werden für bereits erfasste Schüler nicht mehr mit 0 sondern leer gezeigt (Zeugnisse können 0 darstellen, egal ob eine 0 oder kein Eintrag vorliegt)
* CHANGE: Für neu eingeschulte Schüler werden diese Felder nicht mehr mit einer 0 vorbelegt

### MAGELLAN

* NEW: in der Auswahlliste `Schüler` wird der aktuell belegte Bildungsgang eingeblendet
* NEW: `MAGELLAN > Daten2 > Abgangsart` Sammelzuweisung ergänzt
* NEW: Wird ein neuer Sorgeberechtigter von `Schüler/Bewerber > Daten1 > Familie` aus angelegt, wird für den Datensatz unter `Sorgeberechtigter > Daten` das Feld `Gemeindekennziffer` gefüllt.
* NEW: Für Vagabunden (Datensätze im Schülermenü, die noch keiner Klasse zugeordnet wurden, Anzeige per Statusfilterwert "Vagabunden") wurde das Feld `aktuelle Ausbildung` auf der Ausbildungskarte ergänzt. Die zuerst erfasste Ausbildung wird automatisch als aktuelle Ausbildung eingesetzt.
* NEW: Die MAGELLAN-Mailschnittstelle kann für 32 Bit- und 64 Bit-Mailclients verwendet werden. Sollte nicht der von Ihnen erwartete Mailclient aufgerufen werden, schauen Sie bitte folgenden Artikel an [Welcher Mailclient wird aufgerufen?](https://doc.kb.stueber.de/sonstiges/mapi2.html).

* CHANGE: Wechselt man von `Bewerber > Auswahl` in eine Datenkarte und zurück, sind die Gruppierungen im Anschluss so geöffnet oder geschlossen wie zuvor
* CHANGE: Verhalten des Meldungsfenster unter `Abitur > Qualifikation`
* CHANGE: Umgestaltung der Karte `Schüler > Laufbahn` (Hintergrund waren Skalierungsprobleme bei niedrigen Auflösungen)
* CHANGE: Unter `Datenbank > Optionen > Dokumente > Crystal Reports/Word-Seriendruck` wird bei der Eingabe geprüft, dass kein vollständiger Pfad (Beispiel: C:/...) eingegben wird, sondern lediglich ein Unterpfad, der die Ablage ausschließlich innerhalb der MAGELLAN-Verzeichnisstruktur sichert.
* CHANGE: Darstellung der Verzeichnisfelder unter `Berufsschule > Matrix` und `Berufsschule > Abschluss` aktualisiert 

* FIX: Fehlermeldung bei Eingabe unter `Bewerber > Daten2 > ex.Empfehlung`  und Wechsel per "Nächster Datensatz" behoben
* FIX: `Bewerber > Merkmale` Kürzel werden angezeigt
* FIX: Schüler in andere Mandanten versetzen
* FIX: Ändern von Adressdaten über mehrere Mandanten hinweg (Sorgeberechtigte, Personen, Lehrer)
* FIX: Für Schüler, die in einen anderen Mandanten versetzt werden, deren Sorgeberechtigte dort bereits einem Schüler zugeordnet wurden, klappt die Verbindung zwischen Schüler und Sorgeberechtigten
* FIX: Schüler können nicht erneut in einen Mandanten versetzt werden, in des sie bereits versetzt wurden
* FIX: Korrektur beim Import NRW-SchuelerOnline [EZ2-Felder für wiederkehrende Schüler](https://doc.magellan7.stueber.de/schulverwaltung/regionales/nrw/schueleronline/#importierte-felder)
* FIX: `Schüler > Zeugnis > Arbeits- und Sozialverhalten`Zuweisen von Kategorietafeln
* FIX: `Abitur > Fachwahl`Anzeige der belegten Kurse
* FIX: `Lehrer > Soll-Berechnung`Auswahl aus dem Schlüsselverzeichnis Lehrer-Sollschlüssel möglich
* FIX: `Lehrer > Merkmale` Auswahl aus dem Schlüsselverzeichniss Lehrer Merkmale möglich
* FIX: `Abitur > Fachwahl`:Aktualisierungsproblem behoben
* FIX: `MAGELLAN > Schüler`Aktualisieren der Ansicht nach Schüler korrigieren
* FIX: `Schüler > Daten1` Reihenfolge bei Nutzung der Tabulatorentaste angepasst
* FIX: `Abitur > Prüfungen > Prüfungsnoten eingeben`: Layout anpassen ist inaktiv
* FIX: `Lehrer > Merkmale` Auswahl der im Schlüsselverzeichnis Merkmale (Lehrer) eingetragenen Werte korrigiert
* FIX: `Schüler > Zeugnis > Arbeits- und Sozialverhalten`: Kategorietafel zuweisen
* FIX: Korrektur beim Auswahlfilter der Gemdeinden für Schüler/Sorgeberechtigte/Betriebe bei Auswahl Sachsen und NRW 
* FIX: `MAGELLAN > Extras > Exporte > Landesstatistik Berlin`
* FIX: `NRW > Extras > Export > SchülerOnline`: Hier wurde versehentlich die Statistiklizenz mit abgefragt
* FIX: Wenn ein Bewerber einen weiteren Ausbildungsdatensatz bekommt, fehlte das Häkchen für `als neue Ausbildung übernehmen`.  
* FIX: Beim Import aus SchuelerOnline wird das Feld Schulnr korrekt eingelesen
* FIX: `Schüler > Laufbahnprozess > ENBREA Leistungen übernehmen`
* FIX: Für `Extras > Schlüsselverzeichnisse > Bewerbungsziele > Hauptfachnote` ist die Priorität auswählbar

### SAXSVS

* CHANGE: Fehlermeldung falls der Zeitraum nicht passend zum heutigen Datum in MAGELLAN existiert und damit kein Export stattfinden kann

### MyMAGELLAN

* FIX: unter Fächer eingeblendete Personalnummer bleibt auch beim Fachwechsel erhalten
* FIX: Filterung der Klassen in der linken Spalte der Schüleransicht korrigiert
* FIX: Ausgeblendete Spalten werden auch beim Datensatzwechsel beibehalten
* NEW: veränderter Umgang mit Fehlzeiten und der Option "beim Importieren überschreiben"

!!! danger "Achtung"

    Bitte beachten Sie die Abschnitt [Importlogik > Fehlzeiten](https://doc.magellan7.stueber.de/mymagellancenter/importlogik/#fehlzeiten)

* CHANGE: beim ersten Aufruf der Fächeransicht ist standardmäßig die Filter für die Beurteilungsart auf `alle Beurteilungsarten` gestellt
* NEW: In der Ansicht `Schüler` ist in der rechte Fensterhälfte links vor der ersten Spaltenbezeichnung das Symbol zum Aufruf des Untermenüs zum Ein- und Ausblenden von Spalten.

![](/assets/images/changelog/7.1.7.00.png)

### MAGELLAN Bibliothek

* CHANGE: Korrekturen für den Umgang mit MedienExemplare.BarcodeExtern

### Skripte

* FIX: NRW-APO-2012.dws - Überprüfung für das Fach Musik, ob mehr als 5 Kurse eingebracht wurden für den Fall: dass ein Schüler Musik außerhalb des Abiturbereiches belegt, es können von den 5 möglichen eingebrachten Grundkursen auch max. zwei instrumental- oder vokalpraktischen Kurse sein
* FIX: Korrektur von `Synchronisiere Abi.dws`. Die Zählung der Trimester für wiederholende Schüler wurde angepasst.

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

#### Optimierungen

Die nachfolgenden Berichte sind nach unseren aktuellen Empfehlungen optimiert worden, ggfs. gab es kleinere Korrekturen. Sie finden unsere Empfehlungen unter [https://doc.kb.stueber.de/cr/verknuepfung.html](https://doc.kb.stueber.de/cr/verknuepfung.html). Alle Berichte unserer Auslieferung werden nach und nach darauf angepasst.

* NEW: Berichte\Zeugnisse\Schüler (Zeitraumübergreifende Notenübersicht- nach FachID).rpt
* CHANGE: SAC-FS-HJI (C.01.01).rpt (Berichtsverknüpfungen aktualisiert)
* CHANGE: SAC-FS-JZ (C.01.02).rpt
* CHANGE: SAC-FS-HJZ (C.01.03).rpt.
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Schul Z 250 (11.19).rptB
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-HJZ (Schul Z 500).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BS-AZ (Schul Z 503).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-AZ (Anlage D35).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-AZ (E01-0A).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-JZ (Anlage C14 - 1 Seitig).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-JZ (Anlage C14 - 2 Seitig).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-ABI (Anlage D33).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-ABI (Bescheinigung Schullaufbahn).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-ABI (Bescheinigung Schullaufbahn)_Zeugnisbemerkung_Fachdaten.rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-ABI.rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-AS (2007).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-AZ (2007).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-AZ (E01-0A).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BKO-FHReife (E01-6J).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BS-AS (A01).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-E01-6A-J (Fachschulabschluss +- FHR).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-GES-AS (A3, 10.2).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-GES-JZ-HJZ (5-9.1_10.1).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-GY-ABI (Anlage 12).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-GY-HJZ (Klasse 5-8).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-GY-JZ-HJZ (5-9).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-Zertifikat.rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-ÜZ (Klasse 7-10).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-JZ (Sekundarabschluss I).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-JZ (Klasse 7-10).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-HJZ (Klasse 7-10).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-JZ (Hauptschulabschluss).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-AZ (Klasse 7-10).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-AS (Variante 1).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-AS (Anlage E4).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D 34).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-ABI-AZ  (Anlage D42).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BBS-AG-AS-JZ-HZ (A01-A04).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BBS-JZ-HJ-AG-AS (A05-A06).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BBS-JZ-HJ-AG-AS (A07).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-RS-AS (Variante 2).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-Bescheinigung (Nichtzulassung Abitur D37).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BG-AS (Anlage D 48).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BG-HJZ VZ Jahrgangsstufe 11 (Anlage D32).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D33a).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D33b - 2014).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BF-FHReife (Anlage C17 schulischer Teil).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D33b).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D34).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D41 - 2012).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-ABI (Anlage D41).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-AZ (Anlage D 31).rpt
* CHANGE: Berichte\Zeugnisse\Nordrhein-Westfalen\NRW-BK-AZ (Anlage D30).rpt
* CHANGE: Berichte\Schueler\Niedersachsen\Schulbescheinigung (Elternwunsch Schulform).rpt
* CHANGE: Berichte\Schueler\Niedersachsen\Schulbescheinigung (Schullaufbahnempfehlung).rpt
* CHANGE: Berichte\Schueler\Niedersachsen\Schulbescheinigung (Empfangsbestätigung).rpt
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\Schullastenausgleich Vollzeit-mit ÜA.rpt
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\Schullastenausgleich Vollzeit.rpt
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\Schullastenausgleich Teilzeit-ohne ÜA.rpt
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\Schullastenausgleich Teilzeit.rpt
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt"
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\MVP-Schullastenausgleich-Vollzeit (nicht im Landkreis Mecklenburgische Seenplatte).rpt
* CHANGE: Berichte\Schueler\Mecklenburg-Vorpommern\MVP-Schullastenausgleich-Teilzeit (nicht im Landkreis Mecklenburgische Seenplatte).rpt
* CHANGE: Berichte\Schueler\Berlin\Schülerliste Berufsschulmatrix BS-BER mit Meldungen.rpt
* CHANGE: Berichte\Schueler\Berlin\Bescheinigung über den Schulbesuch zweifach.rpt
* CHANGE: Berichte\Schueler\Berlin\BBS-Schulbescheinigung.rpt
* CHANGE: Berichte\Schueler\Baden-Württemberg\Schülerkarteikarte.rpt
* CHANGE: Berichte\Schueler\Baden-Württemberg\Bescheinigung über Schulbesuch.rpt
* CHANGE: Berichte\Schueler\Baden-Württemberg\Schülerkarteikarte (DIN A5).rpt
* CHANGE: Berichte\Schueler\Baden-Württemberg\Bescheinigung über Schülerübergabe.rpt
* CHANGE: Berichte\Schueler\Auslandsschulen\DAS-Übersicht über Prüfungsfächer Abitur (Anlage 6).rpt
* CHANGE: Berichte\Schueler\Auslandsschulen\DAS-Ergebnisliste Abitur (Anlage 8)(§39_2).rpt
* CHANGE: Berichte\Schueler\Niedersachsen\Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* CHANGE: Berichte\Schueler\Niedersachsen\Schulbescheinigung zweifach.rpt
* CHANGE: Berichte\Schueler\Niedersachsen\Schulbescheinigung (Überweisung).rpt
* CHANGE: Berichte\Schueler\Schleswig-Holstein\Schulbescheinigung (SHL).rpt
* CHANGE: Berichte\Schueler\Schleswig-Holstein\Schulbescheinigung.rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung BBS (mit Zugang-Abgang der Klasse).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung für die Vergangenheit.rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\RLP-BBS (Bescheinigung Niveaustufen).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schulbescheinigung zweifach.rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt WG12-13 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schulbescheinigung.rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Unfallbericht.rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt BGJ 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt BS 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt FO 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt WG12-13 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt FS 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt WG11 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Rheinland-Pfalz\Schülerstammblatt BF 2seitig (mit Zensuren blanko).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung BBS (mit Zugang-Abgang der Klasse).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung für die Vergangenheit.rpt
* CHANGE: Berichte\Schueler\Schüler (Anzahl Schüler je Herkunftsschulen).rpt
* CHANGE: Berichte\Schueler\Schüler (Anzeige Schulpflichtverletzung).rpt
* CHANGE: Berichte\Schueler\Schüler (Bescheinigung-Laufbahn).rpt
* CHANGE: Berichte\Schueler\Abiturergebnisse.rpt
* CHANGE: Berichte\Schueler\Anmeldeschein (weiterführende Schulen).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Standard).rpt
* CHANGE: Berichte\Schueler\Schülerausweis ABS.rpt
* CHANGE: Berichte\Schueler\Fachwahl-Kursliste.rpt
* CHANGE: Berichte\Schueler\Bescheinigung Schulbesuch (mit Wochenstunden-Schul II 912).rpt
* CHANGE: Berichte\Schueler\Bescheinigung über den Schulbesuch zweifach mit 31 Wochenstunden.rpt
* CHANGE: Berichte\Schueler\Bescheinigung über den Schulbesuch zweifach(mit Wochenstunden).rpt
* CHANGE: Berichte\Schueler\Bescheinigung über Schülerübergabe.rpt
* CHANGE: Berichte\Schueler\Bescheinigung zur Rentenversicherung (V0510 - 26.06.2017).rpt
* CHANGE: Berichte\Schueler\Notfallzettel (A5).rpt
* CHANGE: Berichte\Schueler\Notfallzettel.rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Anmeldung weiterführende Schule).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Elternwunsch Schulform).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Empfangsbestätigung).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (mit Klasse und Ausbildungsdauer).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (mit Klasse und vorauss. Ende einfach).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (mit Klasse und vorauss. Ende zweifach).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (mit Klasse).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Schullaufbahnempfehlung).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (SHL - in word ausfüllbar).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Überweisung).rpt
* CHANGE: Berichte\Schueler\Schulbescheinigung (Vergangenheit mit Klasse).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-GY-ZAS (Schul II 929-9)(12.08).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-GY-JZ (Schul Z 251)(07.10).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Schul Z 620 (09.18).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Schul Z 510 (12.13).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Schul Z 508.rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-GY-ZAZ (Schul II 929-12)(12.08).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-GY-ZAS (Schul II 929-11a)(01.09).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-HS-AS (Schul Z 210)(05.08).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Schul Z 513a (12.13).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-GY-ZAS (Schul Z 600).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-KO-ABI (Schul Z 323)(03.11).rpt
* CHANGE: Berichte\Klassen\Klassenlehrerliste.rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Summendaten.rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Summendaten(akt.FS-Folge).rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Summendaten (DIN A5).rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülerzahl.rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülersummendaten.rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülersummendaten Ausländer.rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülersummendaten (Var 1).rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülersummendaten (Religion).rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülersummendaten (Religion und Fremdsprachen).rpt
* CHANGE: Berichte\Klassen\Klassenliste mit Schülersummendaten (Klassenstufe und Klassenlehrer).rpt
* CHANGE: Berichte\Mandanten\Schülerliste (inaktive Schüler mit Ausleihvorgängen).rpt (letzte Klasse ergänzt)
* CHANGE: Berichte\Schueler\Schülerliste (inaktive Schüler mit Felder min. 1 Feld leer AbgangAm Abschluss1 Abschluss1Datum Abgangsart).rpt (letzte Klasse ergänzt)
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-BS-AS-Lernfeld A3 MBK.rpt
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-BS-AGZ Lernfeld MBK.rpt
* CHANGE: Berichte\Schueler\Schülerliste (Anwesenheit Ags).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Abitur).rpt
* CHANGE: Berichte\Schueler\Schülerliste ( Klasse, Tutor, Merkmal B1, B2, B3, B4).rpt
* CHANGE: Berichte\Schueler\Schülerliste ( Klasse, Geburtsdaten, Konfession, Geschlecht).rpt
* CHANGE: Berichte\Schueler\Schüler-BBS (Bescheinigung-Laufbahn).rpt
* CHANGE: Berichte\Schueler\Schülerkarteikarte (DIN A5).rpt
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-BS-HJZ-Lernfeld MBK.rpt
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-Verhaltenszeugnis.rpt
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-HJZ-JZ (Klassenstufen 5-10)+GEMS-HJZ-JZ (Einführungsphase).rpt
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-AZ (modifiziert Klassenstufen 9 und 10).rpt
* CHANGE: Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-AZ (Klassenstufen 5-10)+GEMS-AZ (Einführungsphase).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER Abi-1a – Übersichtsplan über die Schullaufbahn ab 2010 – 12jähriger Bildungsgang (VO-GO) (01.12).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-AbdGy abi_4b_berechnungsbogen_abendgym (03.12.).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-AbdGy-ABI (Schul Z 325)(02.11).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-ABI (Schul II 929-3(01.09).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Abi 8 (01.12)mit Logo.rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Abi 8 (01.12)mit Logo2.rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-Abi 8 (01.12).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BF-AS(einjährig).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BF-AS (Schul Z 522c)(05.06).rpt
* CHANGE: Berichte\Zeugnisse\Berlin\BER-BF-AS(Z 522-542).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Praxisbetrieben und Geburtsdatum).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Prüfungsfächern inkl. Lehrer).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Sorgeberechtigten deutsch).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Sorgeberechtigten französisch).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Bafög).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Einschulmerkmal1 sortiert nach Bewerber-Gesamtnote, Punkte, HF-Note).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Fehlzeiten nach Klasse gruppiert).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Fehlzeiten nach Schüler gruppiert).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Förderung).rpt
* CHANGE: Berichte\Schueler\Schülerliste (gruppiert nach Berufen mit Wohnort).rpt
* CHANGE: Berichte\Schueler\Schülerliste (gruppiert nach Berufen).rpt
* CHANGE: Berichte\Schueler\Schülerliste (gruppiert nach Betrieben).rpt
* CHANGE: Berichte\Schueler\Schülerliste (gruppiert nach Bildungsgängen).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Klasse, Geburtsdaten, Adresse, Telefon, sortiert nach Klasse).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Klasse, Geburtsdaten, Adresse, Telefon, sortiert nach Schüler).rpt
* CHANGE: Berichte\Schueler\Schülerliste (Klasse, Geburtsdatum und Geburtsland).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Ausbildungsbetrieben und Geburtsdatum).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Betrieben und Geburtsdatum).rpt
* CHANGE: Berichte\Schueler\Schülerliste (mit Betrieben).rpt
* CHANGE: Berichte\Zeugnisse\BER-BFS-AS (Z 522a)(04.11).rpt
* CHANGE: Berichte\Zeugnisse\BER-BFS-AZ (Schul Z 523a).rpt
* CHANGE: Berichte\Zeugnisse\BER-BFS-HJZ (Schul Z 520b)(07.09).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 202 (07.10).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 102 (11.10).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 351 (11.19)_Kolleg.rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 350 (10.07).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 303 (11.19).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 302 (11.19).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 300 (11.19).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 255 (09.17).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 251b (05.16).rpt
* CHANGE: Berichte\Zeugnisse\BER-Schul Z 240 (09.17).rpt
* CHANGE: Berichte\Zeugnisse\BER-RS-AZ (Schul Z 242)(06.08).rpt
* CHANGE: Berichte\Zeugnisse\BER-RS-AS (Schul Z 241)(07.10).rpt
* CHANGE: Berichte\Zeugnisse\BER-RS-AS (Schul Z 240)(03.08).rpt
* CHANGE: Berichte\Zeugnisse\BER-KO-ZAS (Schul Z 371)(02.12).rpt
* CHANGE: Berichte\Zeugnisse\BER-KO-ZAS (Schul Z 371)(02.12).rpt
* CHANGE: Berichte\Zeugnisse\BER-GY (abi_4_berechnungsbogen)(10.16)
* CHANGE: Berichte\Zeugnisse\BER-GS-JZ (Schul Z 103)(11.05)
* CHANGE: Berichte\Zeugnisse\BER-GS-JZ (Schul Z 103)(11.05) (französ. Gymn)

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

