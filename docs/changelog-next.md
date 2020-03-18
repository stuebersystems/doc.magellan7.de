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

## 7.1.7 - 711

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE:  Änderung für die Anzeige des aktuellen Betriebes für Vagabunden

### MyMAGELLAN

* FIX: unter Fächer eingeblendete Personalnummer bleibt auch beim Fachwechsel erhalten
* CHANGE: beim ersten Aufruf der Fächeransicht ist standardmäßig die Filter für die Beurteilungsart auf `alle Beurteilungsarten` gestellt
* NEW: In der Ansicht `Schüler` ist in der rechte Fensterhälfte links vor der ersten Spaltenbezeichnung das Symbol zum Aufruf des Untermenüs zum Ein- und Ausblenden von Spalten.

![Symbol zum Ein- und Ausblenden von Spalten verfügbar](/assets/images/changelog/7.1.7.00.png)

### MAGELLAN

* NEW: in der Auswahlliste `Schüler` wird der aktuell belegte Bildungsgang eingeblendet
* NEW: `MAGELLAN > Daten2 > Abgangsart` Sammelzuweisung ergänzt
* NEW: Wird ein neuer Sorgeberechtigter von `Schüler > Daten1 > Familie` aus angelegt, wird für den Datensatz unter `Sorgeberechtigter > Daten` das Feld `Gemeindekennziffer` gefüllt.
* NEW: Für Vagabunden (Datensätze im Schülermenü, die noch keiner Klasse zugeordnet wurden, Anzeige per Statusfilterwert "Vagabunden") wurde das Feld "aktuelle Ausbildung" auf der Ausbildungskarte ergänzt. Die zuerst erfasste Ausbildung wird automatisch als aktuelle Ausbildung eingesetzt.
* CHANGE: Wechselt man von `Bewerber > Auswahl` in eine Datenkarte und zurück, sind die Gruppierungen im Anschluss so geöffnet oder geschlossen wie zuvor
* CHANGE: Verhalten des Meldungsfenster unter `Abitur > Qualifikation`
* CHANGE: Umgestaltung der Karte `Schüler > Laufbahn` (Hintergrund waren Skalierungsprobleme bei niedrigen Auflösungen)
* CHANGE: Unter `Datenbank > Optionen > Dokumente` wird bei der Eingabe geprüft, dass kein vollständiger Pfad (Beispiel: C:/...) eingegben wird, sondern lediglich ein Unterpfad, der die Ablage ausschließlich innerhalb der MAGELLAN-Verzeichnisstruktur sichert.

* FIX: Fehlermeldung bei Eingabe unter `Bewerber > Daten2 > ex.Empfehlung`  und Wechsel per "Nächster Datensatz" behoben
* FIX: `Bewerber > Merkmale` Kürzel werden angezeigt
* FIX: Schüler in andere Mandanten versetzen
* FIX: Ändern von Adressdaten über mehrere Mandanten hinweg (Sorgeberechtigte, Personen, Lehrer)
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


### SAXSVS

* FIX: 

### MAGELLAN Administrator

* FIX: 

### MyMAGELLAN-CENTER

* CHANGE: 

### MyMAGELLAN

* FIX:

### MAGELLAN Bibliothek

* CHANGE: Korrekturen für den Umgang mit MedienExemplare.BarcodeExtern

### Skripte

* FIX: NRW-APO-2012.dws - Überprüfung für das Fach Musik, ob mehr als 5 Kurse eingebracht wurden für den Fall: dass ein Schüler Musik außerhalb des Abiturbereiches belegt, es können von den 5 möglichen eingebrachten Grundkursen auch max. zwei instrumental- oder vokalpraktischen Kurse sein
* FIX: Korrektur von `Synchronisiere Abi.dws`. Die Zählung der Trimester für wiederholende Schüler wurde angepasst.

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* NEW: Berichte\Zeugnisse\Schüler (Zeitraumübergreifende Notenübersicht- nach FachID).rpt
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