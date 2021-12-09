# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier: 

  * [2020](changelog2020.md)
  * [2019](changelog2019.md)

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

## Version 8

### 8.0.14 802 (unveröffentlicht)

#### MyMAGELLAN-CENTER

* FIX: Beim Erstellen von MyMAGELLAN-Dateien für des Schülers denen derselbe Lehrer als Fachlehrer und als Tutor zugeordnet ist, wird nur der Tutor in die Datei gespielt.

#### MyMAGELLAN

* FIX: Für Dateien, die mit der Version MAGELLAN 8.0.13 oder früher erstellt wurden, wird für Schüler denen derselbe Lehrer als Tutor und als Fachlehrer zugeordnet wurde, die Rolle des Fachlehrers ignoriert. Ab mit der Version MAGELLAN 8.0.14 oder höher erstellten MyMAGELLAN-Dateien tritt diese Problematik nicht mehr auf. Eine Vorabversion von MyMAGELLAN, die diese Problematik korrekt verarbeitet, finden Sie unter: [https://my.hidrive.com/lnk/ncSJCFHd](https://my.hidrive.com/lnk/ncSJCFHd)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: BER-Schul Z 590 (12.19).rpt (Verknüpfungen überarbeitet)

### 8.0.13 802 (30.11.2021)

#### MAGELLAN Schulverwaltung

* FIX: `Klasse > Zeitraum` löschen eines Zeitraum mit `Entf`nicht mehr möglich
* FIX: `Schüler > Daten1` Eintrag im Feld `Vorname` wird beim Ansichtenwechsel gespeichert
* FIX: `Schüler > Ausbildung > Ausbildungsdaten`: Tabreihenfolge korrigiert
* NEW: Für den Bewerberseriendruck wurde das neue Feld `Bewerber_ID` eingefügt
* NEW: Unter `Bewerber > Daten3` kann analog `Schueler > Daten3` eine freie Bemerkung erfasst werden.
* CHANGE: Unter `Extras > Schlüsselverzeichnisse > Bewertungsprofile` wird auf den Unterkarten `Bewertungsgruppen` und `Bewertungseinträge` am oberen Ende das `Kürzel` (statt der `Bezeichnung`) des gewählten Bewertungsprofils eingeblendet.
* FIX: [SAXSVS] Beim Anlegen einer neuen Ausbildung kann gewählt werden, ob eine neue Ausbildungs-GUID vergeben wird, je nach Auswahl wird die bisherige GUID der aktuellen Ausbildung übernommen oder eine neue GUID generiert. Hierbei ist wichtig: Um die bisherige GUID beizubehalten, muss die aktuelle Ausbildung gekennzeichnet sein.
* FIX: Unter `Schüler > Daten1 > Familie` wird die Mobilnummer, wenn sie als `Telefonpriorität` markiert ist, korrekt mit gelb unterlegt dargestellt.
* FIX: Reiter `Dateinamenskonventionen` umbenannt unter `Datenbank > Optionen > Dokumente`
* FIX: Die Anzeige des Status (aktiv, inaktiv) der Kürzel unter `Abitur > Fachwahl > Unterrichtsart` wurde korrigiert
* FIX: Die Anzeige des Symbols für "Parallele Laufbahn des Schülers" unter `Schüler > Laufbahn` wurde korrigiert
* FIX: [Gruppen] Beim Anlegen neuer Gruppenmitglieder wird der `Mitglied (Typ)` (Lehrer, Schüler, Person oder Sorgeberechtigter) korrekt übergeben.
* FIX: Aufruf des Seriendrucks an Personen korrigiert
* CHANGE: Für den Seriendruck mit MS Word können mehrere Seriendruckdokumente parallel geöffnet werden.
* FIX: [ENBREA] Unter `Schüler > Zeugnis > ENBREA Leistungen` wird in der Spalte `Note` die Auswahl entsprechend der Eingabe unter `Klassen > Zeiträume > ENBREA Leistungsprofile > Leistungsprofile definieren > Notensystem` gefiltert.

#### MAGELLAN ADMINISTRATOR

* FIX: Mit der Aktion `Datenbankpflege > Code 128 generieren` wird auch das Feld `BarcodePrint` für Lehrer befüllt.
* FIX: Unter `Benutzerverwaltung > Doppelklick auf Benutzer > Unterkarte "Rechte" > Bibliothek und Lernmittelverwaltung` wird die Liste der Kataloge korrekt für die Auswahl geladen
* FIX: Unter `Datenaustausch > Daten über das MAGELLAN-Importformat importieren` wird für den Import der Datei `betriebe.import.csv` eine Meldung für das Feld `Telefon` ausgegeben, wenn der Feldinhalt 30 Zeichen überschreitet. Der Betrieb wird in diesem Fall ohne Telefonnummer importiert.

#### MYMAGELLAN

* FIX: Schlüsselverzeichnis Zeugnisbemerkungen wird in voller Länge aus MAGELLAN übergeben
* FIX: `Schüler > Ausbildung > Editieren` Tabulatorreihenfolge korrigiert
* FIX: Speichern der Eingaben auf der Karte `Zeugnisdaten` (besonderer Fall: nur eine Eingabefeld auf der Karte)) 
  
#### Schnittstellen

 * Change: [SHL] Schlüsselverzeichnis Unterrichtsarten
 * CHANGE: [NRW] SIM.TXT - Im Falle eines Bildungsgangwechslers wird künftig nur noch eine Datensatz als Neuzugang an neuer Schule ausgespielt, die alte Laufbahn wird in die VO-Felder eingetragen, zusätzlich müssen noch die Felder LSQual, Zeugnis, Berufsabschluss und Versetzung gefüllt sein
* FIX: [SAXSVS]  `<al_fremd_fs1 >` wird ausgegeben, Eingabe muss unter `Schüler > Zeugnis > Fächer`erfolgen

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: [Synchronisieren BBS.dws] Ausbildungsparameter wird gesetzt, damit die Fachliste gefüllt und übertragen werden kann
* FIX: DE-DIAP-2015 diverse Korrekturen Vorschlagsautomatik
* FIX: DE-DIAP-2018 diverse Korrekturen
* FIX: DE-DIAP-2018 Eibringungsverprflichtung einer Naturwissenschaft mit allen 4 Halbjahren

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: Klassenliste (Schüler und Sorgeberechtige Email).rpt
* NEW: Notfallzettel (Bemerkungsliste).rpt
* NEW: Mandant (Schüler des aktuellen Halbjahres ohne aktuelle Ausbildung)
* CHANGE: Mandant (Schüler des aktuellen Halbjahres ohne Fächer)
* CHANGE: Anwesenheitsliste für den Tag.rpt (Klassenleiter1 + 2)
* FIX: Schülerliste (Förderung).rpt

##### Auslandsschulen

* FIX: DSND.DAS-GS (Klasse 3).rpt

##### Berlin

* FIX: BER-Schul Z 520 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 526 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 503 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 501 (09.19).rpt (Ausgabe Ausbildungsberuf)

##### Saarland

* NEW: ...Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-ABI (GOS2.0) mit Parametern.rpt (über Parametereingabe kann gesteuert werden, ob es sich um ein Abiturzeugnis, Zweitschrift, Zweitausfertigung oder Zweitausfertigung (Ministerium) handelt)

![Paramterwert für Zeugnisdruck](/assets/images/changelog/8.0.13.01.png)

### 8.0.12 802 (09.09.2021)

#### MAGELLAN Schulverwaltung

* NEW: Unter `Sorgeberechtigte > Kinder` werden zusätzlich zu aktiven oder pausierenden Schülern auch inaktive Schüler eingeblendet.
* FIX: `Schüler > Zeugnis > ENBREA Lernleistungen` Aktualisierungsproblem behoben
* FIX: `Schüler > Ausbildung > Beruf` Editierungsproblem nach Import aus SAXSVS behoben
* FIX: `Bewerber > Daten2 > Schulform` Aktualisierungsproblem behoben
* FIX: `Schüler > Daten 1 > Staatangehörigkeiten` Aktualisierungsproblem behoben

#### Schnittstellen

* FIX: [Alle]: Konvertierungsproblem Statistikdialogfenster beim Auslesen der Zeiträume gelöst
* CHANGE: [NRW]: Geschwindigkeitsverbesserung SIM.TXT, ABI.TXT, LEHRER.TXT
* FIX: [NRW]: SIM.txt - Ausgabe VoFachklasse
* FIX: [NRW]: SIM.txt - Ausgabe von ABG, BAG, AKT, NZG, NGS, AKT, NZG
* FIX: [NRW]: SIM.txt - integer Fehlermeldung beim Erzeugen behoben
* FIX: [NRW]: SIM.TXT - Ausgabe Zeugnis für BAG
* FIX: [NRW]: ABI.TXT - Ausgabe von Daten

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: [Importiere SDTF.dws] Korrektur des Auslesens von Nullwerten der Schuelerfachdaten aus MAGELLAN im P1-Datensatz 

* FIX: [Zuweisen von Zugriffsrechten.dws] Korrektur beim ENBREA Kurse, ENBREA Leistungen
* FIX: [Importiere SDTF.dws für Import aus SDTF/Untis] Korrektur des Auslesens von Nullwerten der Schuelerfachdaten aus MAGELLAN im P1-Datensatz

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### DAS

* CHANGE: DAS-Zeugnis Gymnasium - Mittlerer Schulabschluss (Anlage 10)(§23).rpt (Layoutanpassungen)
* CHANGE: DAS-GS-GY (Klasse 3-10).rpt (Layoutanpassungen)

##### Berlin

* FIX: Schülerliste (Klasse, Geburtsdaten, Adresse, Telefon, sortiert nach Klasse).rpt - Ausgabe doppelter Schüler korrigiert
* FIX: BER-Schul Z 500 (09.19).rpt
* NEW: BER-BBS (Zeugniskarte).rpt (jetzt auch in Auslieferung von MAGELLAN 8)
* FIX: BER-Schul Z 520 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 522 (09.19).rpt (Ausgabe Ausbildungsberuf, Layoutanpassungen)
* FIX: BER-Schul Z 523 (09.19).rpt (Ausgabe Ausbildungsberuf, Layoutanpassungen)
* FIX: BER-Schul Z 526 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 503 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 502 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 501 (09.19).rpt (Ausgabe Ausbildungsberuf)

### 8.0.11 802 (12.08.2021)

#### MAGELLAN Schulverwaltung

* FIX: Aktualisierung der Anzeige unter `Schüler > Daten2 > bereits besuchte Schulen`
* FIX: Unter `Personen > Dokumente` wird das Kontextmenü bei Rechtsklick gezeigt
* FIX: Aktualisierung der Laufbahnkarte korrigiert, wenn der Schüler per Doppelklick aus der Auswahlliste aufgerufen wurde
* FIX: Problem beim Ändern eines Passwortes für Benutzer mit Umlauten im Namen behoben
* FIX: Einblenden der Schüler-Zusatzkarte korrigiert
* FIX: Anzahl der belegten Fachwahlen wird unter `Abitur > Fachwahl` bei Änderung aktualisiert
* INFO: [NRW-SchuelerOnline] Die `BetriebIdExtern` hat den Aufbau: `MAGELLAN-BetriebID`-`MAGELLAN-Betriebekürzel`und kann aus `SchuelerOnline` übernommen werden, wenn Sie Ihre Betriebeliste vorab nach `SchuelerOnline` übergeben haben. Kann der Betrieb an diesen Daten erkannt werden, wird der Bewerber dem Betrieb hinzugefügt. Sollte es Abweichungen in der Adresse oder Name1 geben, schlägt Ihnen der Assistent einen Aktualisierung des MAGELLAN-Betriebes vor. 

#### MAGELLAN Bibliothek

* FIX: Problem beim Anlegen des ersten Mediums und Exemplares gesamt behoben
* FIX: [Zuweisen von Zugriffsrechten.dws] Die Zuweisung von Zugriffsrechten für die Benutzergruppen `Gast1` und `Gast2` wurden überarbeitet

#### Schnittstellen

* CHANGE: [SAXSVS] Für die Berechnung des vorangegangenen Schuljahres wird das Systemdatum verwendet, es sei denn, das Datum des Stichtages im Assistenten wird auf einen abweichenden Wert gesetzt.

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: [Sachsen] `Skripte > SAC-APO-BGY-2017 (DUBAS).dws`
  * Einbringung 26 GKs, Hinweis zusätzl. mdl. Prüfung
  * Wichtig: Das Fach Englisch muss im Schlüsselverzeichnis "Fächer" im Feld "Zeugnismerkmal" den Wert "EN" bekommen, damit das Skript das Fach Englisch korrekt erkennt.
  * es werden nun mindestens zwei Kurse in der neu begonnenen Fremdsprache eingebracht (BGySO §72 Abs. 2 Punkt 2b)

* FIX: [Sachsen] `Skripte > SAC-APO-BGY-2017.dws`
  * Einbringung 26 GKs, Hinweis zusätzl. mdl. Prüfung
  * Wichtig: Das Fach Englisch muss im Schlüsselverzeichnis "Fächer" im Feld "Zeugnismerkmal" den Wert "EN" bekommen, damit das Skript das Fach Englisch korrekt erkennt.
  * es werden nun mindestens zwei Kurse in der neu begonnenen Fremdsprache eingebracht (BGySO §72 Abs. 2 Punkt 2b)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Sachsen

* NEW: SAC-FO-FHReife (D.01.05)(ab 2017).rpt
* CHANGE: [SAC-BG-ABI (E.01.06).rpt] 
   * Die Hinweise für die Sprachreferenz der Fremdsprachen können ggfs. mit Umbruch gezeigt werden.
   * Namensanzeige (Vorname Vorname2 Zusatz Nachname) angepasst
   * Ausgabe Fachrichtung erweitert (Erst Fachrichtung des Schülerbildungsganges, dann Fachrichtung des Klassenbildungsganges)
* CHANGE: SAC-Fremdsprachenzertifikat (F.01.05).rpt
* Fix: Zeugnis SAC-BG-AZ (E.01.05).rpt
* CHANGE: SAC-BG-AZ (E.01.05).rpt - ergänzt um Ausgabe Namen SchulleiterIn/TutorIn
* FIX: SAC-FS-AS mit FHReife (C.01.06).rpt  (Korrektur der Anzeige der Durchschnittsnote in Zahl und Wort)
* CHANGE: ergänzt um 2. Vorname und Namenszusatz
   * SAC-Fremdsprachenzertifikat (F.01.05).rpt 
   * SAC-BS-HJI (A.01.02).rpt 
   * SAC-BS-JZ (A.02.01).rpt
   * SAC-FO-FHReife (D.01.05)(ab 2017).rpt
   * SAC-BS-AZ (A.02.04).rpt
   * SAC-BS-AS (A.02.05).rpt
   * SAC-BF-AZ (B.03.04).rpt

* CHANGE: SAC-BF-AS (B.04.05).rpt (ergänzt um Ausgabe Prüfungsvorsitz, SchulleiterIn)
* CHANGE: SAC-BF-HJI (B.01.01).rpt
* CHANGE: SAC-BS-AS (A.02.06).rpt (pers. Zeugnisbemerkungen, Ausgabe SchulleiterIn, KlassenlehrerIn)
* NEW: SAC-BS-AZ (A.02.04)(zweiseitig).rpt
* NEW: SAC-BS-JZ (A.02.02)(zweiseitig).rpt
* CHANGE: SAC-BS-AS (A.01.07)(Einstiegsqualifizierung).rpt (ergänzt um Schulleiter, Klassenlehrer, textl. Anpassungen lt. VwV)

##### Saarland

* FIX: SAR-GY-ABI (GOS2.0).rpt (Ergänzung: 2. Vornamen, Namenszusatz, wenn 2. Fremdsprache / Feststellungsprüfung, Ausgabe Name und Amtsbezeichnung des/der Prüfungsvorsitzenden)
* FIX: SAR-GY-AZ (GOS2.0).rpt (ergänzt um 2. Vorname, Namenszusatz)
* FIX: SAR-Antrag auf Zulassung (Anlage 5).rpt (ergänzt um 2. Vorname, Namenszusatz)
* FIX: SAR-FHReife (Nachweis)(GOS2.0).rpt (ergänzt um 2. Vorname, Namenszusatz)

### 8.0.10 802 (08.07.2021)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Anpassung

* CHANGE: Inhalte aus dem bis zur Version MAGELLAN 7 genutzten Feld `Bewerber > Merkmal > Bemerkung` werden kopiert und als Datensatz in der neuen Liste unter `Bewerber > Merkmal > Bemerkungen` als Eintrag ergänzt. Der Inhalt des nicht mehr genutzten Feldes `Bemerkung` wird im Anschluss gelöscht.

#### MAGELLAN Schulverwaltung

* FIX: Problem beim Einschulen (Fachtafelhaken setzen ohne Auswahl einer Fachtafel) von Schülern behoben
* FIX: Anzeige von `Schüler > Merkmale > Bemerkungen` nach Datenübernahme aus MAGELLAN 7
* FIX: Anzeige `Bewerber > Daten3 > Fremdsprachen` auch bei Kürzeln mit 10 Zeichen
* FIX: Die Sammelzuweisung des Feldes `Schüler > Laufbahn > Abschluss > Abschlussdatum2` wurde korrigiert.
* FIX: Optimierung der Abfragen, die beim Aufruf des Schülermenüs und der einzelnen Unterkarten geladen werden
* FIX: Beim Neuanlegen eines Bewerbers wird die Liste der Vorlagen geladen
* FIX: Beim Neuanlegen eines Bewerbers werden die Schulformen unter `Daten2 > Bereits besuchte Schulen` geladen
* FIX: Anzeige der Einträge unter `Schüler > Daten1 > Familie` korrigiert
* FIX: Wechsel der Daten markiertem Klassenzeitraum (je Klassenzugehörigkeit) unter `Schüler > Laufbahn > Allgemein/Abschluss` korrigiert
* CHANGE: Beim Abändern des eigenen Passworts über die MAGELLAN-Oberfläche wird zusätzlich zu Umlauten und ß auch kein Leerzeichen mehr gespeichert, Sie erhalten eine entsprechende Meldung.
* CHANGE: Beim Start des Seriendrucks wird nur noch das Seriendruckdokument geöffnet, kein zweites bereits verbundenes Dokument
* CHANGE: Wenn die Option unter `Datenbank > Optionen > Dokumente > Seriendruck` für keinen Menüpunkt aktiviert ist, dann wird im Seriendruckassistenten die Option ausgegraut dargestellt, der nachfolgende Punkt ist aktiviert.
* CHANGE: Der `Name 1` und das `Kürzel` eines Betriebes wurden unter `Schüler/Bewerber > Ausbildung` nur für den Ausbildungsdatensatz eingeblendet, wenn auch das Betriebekürzel im Menü `Betriebe` gefüllt war. Durch eine Änderung genügt jetzt auch der Eintrag unter `Betriebe > Daten > Name1`.
* CHANGE: [NRW-SchuelerOnline] Beim Import aus `SchuelerOnline` wird der Wert aus dem Feld "Beratung" nicht mehr übertragen. Aktuell erfolgte der Übertrag (Wert: 0,1,2) nach `Bewerber > Merkmale > Bemerkung` und hatte hier keine Aussagekraft.
* NEW: Unter `Bewerber > Merkmal` wurde das Bemerkungsfeld (Memo) durch eine Liste ersetzt, Bemerkungen werden übertragen.
* NEW: Unter `Bewerber > Daten4` wurden die Felder `Bildungskarte` und `Bildungskarte bis` ergänzt.

#### Schnittstellen

* CHANGE: [NRW] Für Nebenschullaufbahnen (Schüler mit IDIntern), deren Stammschullaufbahn außerhalb des Statistikzeitraumes liegt, wurde das Auslesen der Daten überarbeitet.
* NEW: [NRW] Freigabe Statistikschnittstelle zu ASDPC [Anleitung](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/)

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: BER-IBA-AS-2020.dws - Korrekturen
* FIX: NRW-APO-BK-2018.dws - Berechnung der Fachhochschulreife, die maximale Anzahl an Defiziten im GK-Bereich beträgt 4 [Vorab-Download](https://my.hidrive.com/lnk/vbSpi8cE)
* Fix: SAR-APO-2018.dws - Hinweis auf "Nichtbestehen des Abiturs" bei erfolgter mdl. Prüfung aufgrund der Abweichungsprüfung und erneutem Ausführen des Skriptes korrigiert [Vorab-Download](https://my.hidrive.com/lnk/DaypC5gW)
* FIX: SAC-APO-BGY-2017 (DUBAS).dws (Einbringung 26 GKs, Hinweis zusätzl. mdl. Prüfung)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Berlin

* FIX: BER-Schul Z 306 (04.21)(FG).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)
* FIX: BER-Schul Z 306 (04.21).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)

##### Saarland

* CHANGE: SAR-GY-ABI (GOS2.0).rpt (Bezeichnung der Sprachreferenz wird unter Fremdsprachen ausgelesen)

##### Sachsen

* FIX: SAC-BS-AS  (A.02.05).rpt (Berechnung Durchschnittsnote)
* FIX: SAC-BS-JZ  (A.02.01).rpt (Ausgabe von "---" wenn keine unentschuldigten Fehltage vorliegen)
* FIX: SAC-BS-AS  (A.02.05).rpt (Berechnung Durchschnittsnote)
* FIX: SAC-BS-AZ  (A.02.04).rpt (Zeugnisbemerkungen werden korrekt ausgegeben)
* FIX: SAC-BG-ABI (E.01.06).rpt (Thema der BLL kann vierzeilig sein)

##### Niedersachsen

* CHANGE: NIE-GY-ABI (2021).rpt (Der Satz "Die Allgemeine Hochschulreife ist im Deutschen Qualitätsrahmen (DQR) dem Niveau 4 zugeordnet." wird standardmäßig auf dem Zeugnis unter Bemerkungen ausgegeben.

##### Deutsche Auslandsschulen

* CHANGE: DAS-ZZ (Q-Phase)(Anlage 1)(RiLi 1.6)(ab 2020).rpt (Geburtsland wird hinter Geburtsort mit ausgegeben) 
* CHANGE: DAS-ZZ (Q-Phase)(Anlage 1)(RiLi 1.6).rpt (Geburtsland wird hinter Geburtsort mit ausgegeben) 

### 8.0.9 801 (11.06.2021)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!
     Die Datenbankversionsnummer wird hierbei diesmal nicht erhöht, sondern bleibt auf der auf der Datenbankversion 801.

#### Anpassung

* CHANGE: Inhalte aus dem bis zur Version MAGELLAN 7 genutzten Feld `Schüler/Bewerber > Merkmal > Bemerkung` werden kopiert und als Datensatz in der Liste unter `Schüler/Bewerber > Merkmal > Bemerkungen` als Eintrag ergänzt. Der Inhalt des nicht mehr genutzten Feldes `Bemerkung` wird im Anschluss gelöscht.

#### MAGELLAN Schulverwaltung

* FIX: Unter `Extras > Schlüsselverzeichnisse` werden alle Eintragungen für Merkmalsfelder (Lehrer, Schüler, Klassen, Mandanten und Schulen) nur für den gewählten Mandanten gezeigt.

#### Schnittstellen

* FIX: [BER] Problem beim Erstellen der Abiturdatenstatistik behoben

#### Skripte

* CHANGE: `Schüler fortschreiben`Strikteres Vorgehen beim Schüler fortschreiben; beim finden des SchülerZeitraum Datensatzes wird auch Gewechselt Status berücksichtigt. 
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: DE-DIAP-2015 diverse Korrekturen
* FIX: DE-DIAP-2018 diverse Korrekturen
* FIX: Schüler fortschreiben: Korrektur bei leeren Datenmengen (SchuelerKlassen)
* CHANGE: Aktualisierte Ausgaben der Skripte [BER-IBA-AS-2020](https://doc.la.stueber.de/03.ber/ber-iba-hj-2020dws/) und [BER-IBA-AS-2020](https://doc.la.stueber.de/03.ber/ber-iba-as-2020dws/) finden Sie unter folgendem [Vorab-Download](https://my.hidrive.com/lnk/IByJi3hD).
* NEW: SAC-APO-BGY-2021.dws *(Änderung 01/2021 gemäß Rundschreiben "Regelung der Einbringungs- und Belegverpflichtung im Kurshalbjahr 12/II bzw. 13/II" vom 29.01.2021)* Eine Anleitung zum Skript finden Sie [hier](https://doc.la.stueber.de/11.sac/sac-apo-bgy-2021/).

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, unsortiert).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, sortiert).rpt

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 255 (2020.2021).rpt
* NEW: BER-Schul Z 256 (2020.2021).rpt

##### Sachsen

* FIX: SAC-BS-AS (A.02.04).rpt (Berechnung Durchschnittsnote)
* CHANGE: SAC-BF-AS (A.02.07).rpt
* CHANGE: SAC-BF-AS (B.04.05).rpt
* CHANGE: SAC-BF-AZ (B.03.04).rpt
* CHANGE: SAC-BS-AS (A.02.05) 2spaltig.rpt
* CHANGE: Zertifikat (F.01.09).rpt

##### Niedersachsen

* FIX: NIE-GY-ABI (2021).rpt (Nicht-Ausgabe von Punkten, die nicht auf dem Zeugnis ausgegeben werden sollen, Punktssumme P aus Schulhalbjahresergebnissen)

##### Auslandsschulen

CHANGE: DAS-GY-AZ ohne FHR (Anlage 9a).rpt
CHANGE: DAS-GY-AZ mit FHR (Anlage 9b).rpt

### 8.0.8 801 (27.05.2021)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### MAGELLAN Schulverwaltung

* FIX: Problem beim Bearbeiten von Familiendaten unter `Schüler > Daten1` behoben

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik, Fehlermeldung wenn ein Prüfungsergebnis fehlt
* FIX:  DE-DIAP-2018 diverse Korrekturen in der Vorschlagsautomatik,Fehlermeldung wenn ein Prüfungsergebnis fehlt

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: Schülerpersonalblatt (mit Vorbildung und Herkunftsschule).rpt 
* FIX: Schülerpersonalblatt (aktive Schüler mit Eltern und Vorbildung).rpt

### 8.0.7 801 (20.05.2021)

#### Schnittstellen

* FIX: SAXSVS - SQL Fehlermeldung behoben

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

### 8.0.6 801 (19.05.2021)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstruktur

* NEW: Neue Felder unter `Schüler > Daten 2` (Dokumentation [hier](https://doc.magellan7-toolbox.stueber.de/datenstruktur/version8/tabellen/Schueler/))
  * HoechsterAbschluss2ABS
  * HoechsterAbschluss2ABSSchulform
  * HoechsterAbschluss2BBS
  * HoechsterAbschluss2BBSSchulform
* FIX: Vagabunden View, fehlende Felder (Schüler-Merkmale A7-A10) hinzugefügt

#### MAGELLAN Schulverwaltung

* FIX: Problem beim Neuanlegen eines Schülers wurde behoben
* CHANGE: Die Anordnung der Felder unter `Schüler > Daten 2` wurde verändert
* FIX: Das Kürzel im Verzeichnis `Einschulmerkmale` wurde auf 20 Zeichen erhöht
* FIX: Unter `Extras > Schlüsselverzeichnisse > Fachtafeln` kann für `Fachwahltafeln` die `Kurssprache` in den Spalten `Q1 Sprache` bis `Q4 Sprache` ausgewählt werden.
* FIX: Spaltenbenennung unter `Abitur > Zeugnisbemerkungen > Sammelzuweisung` korrigiert

#### Schnittstellen

* NEW: SAXSVS => Schüler, die im vergangenen Jahr einen Abschluss an Ihrer Schule absolvierten und im aktuellen Schuljahr einen neuen Bildungsgang belegen, werden in der Abgängerdatei und in der Datei der aktuellen Schüler ausgegeben. 
Da in beiden Dateien Daten über die bisher erworbenen Abschlüsse ABS oder BBS und die Abschlussschulformen erwartet werden, gibt es unter `Schüler > Daten2` eine neue Aufteilung und auch neue Felder. Bitte erfassen Sie in den Feldern unter "Höchster Abschluss ABS/BBS (mitgebracht)" die Daten, die der Schüler aus Sicht des Vorjahres mit an die Schule brachte oder zuvor erworben hatte. Bitte erfassen Sie in den neuen Feldern unter "Höchster Abschluss ABS/BBS (erworben)" ggfs. Abschlüsse, die der Schüler inzwischen an Ihrer Schule erworben hat. 
Wir geben für die Abgängerdatei die Einträge aus dem Bereich "Höchster Abschluss ABS/BBS (mitgebracht)" aus. Für die Datei der aktuellen Schüler geben wir die Daten aus dem Bereich "Höchster Abschluss ABS/BBS (erworben)" aus, steht dort kein Wert, werden die Inhalte aus den Feldern "Höchster Abschluss ABS/BBS (mitgebracht)" ausgespielt.
* NEW: SAXSVS: `al_abschl_dat` wird in der Erstprüfung berücksichtigt und ggfs. als Meldung je Schüler ausgegeben.
* NEW: Landesstatitik Schleswig-Holstein veröffentlicht (Eine Anleitung finden Sie unter [https://doc.ls.stueber.de/schleswig-holstein/einstieg/](https://doc.ls.stueber.de/schleswig-holstein/einstieg/).)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 250 Co (04.21).rpt
* NEW: BER-Schul Z 306 (04.21)(FG).rpt
* NEW: BER-Schul Z 306 (04.21).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt
* NEW: BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.21).rpt

### 8.0.5 800 (12.05.2021)

#### Allgemein

* NEW: Zum MSI-Paket für 32-Bit-Betriebssysteme gibt auf unserer Webseite eine eigene UpdatenInfo-Datei. Die installierte MAGELLAN-Version fragt aus der Registry den Wert je nach verwendetem Installationpaket ab (für Windows 32 Bit oder Windows 64 Bit) und greift auf die geeignete UpdateInfo-Datei zu.

#### MAGELLAN Schulverwaltung

FIX: Die Funktionalität `Fahrstrecken` wurde überarbeitet

#### MAGELLAN Administrator

* FIX: Benutzer anlegen korrigiert
* CHANGE: Beim Anlegen eines neuen Benutzers sind die Häkchen auf der Unterkarte `Ansichten` vorbelegt

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/).

* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen mit der Option `nur geänderte Daten` aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 
* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik
* NEW:  DE-DIAP-2018 

### Version 8.0.4 800 (07.05.2021)

* NEW: Es gibt zwei Installationspakete für MAGELLAN. MAGELLAN ist weiterhin eine 32 Bit Anwendung und wird mit der auf unserer Webseite verfügbaren 32 Bit Ausgabe von Firebird (aktuell 2.5.9) eingesetzt. Wenn Sie Crystal Reports 2020 einsetzen möchten, muss bitte das Setuppaket [MAGELLAN-Setup für Windows 64 Bit](https://download.stueber.de/bin/de/magellan/v8/magellan8.msi) verwendet werden. Setzen Sie MAGELLAN auf einem 64 Bit Betriebssystem ein, verwenden Sie bitte das Setuppaket [MAGELLAN-Setup für Windows 32 Bit](https://download.stueber.de/bin/de/magellan/v8/magellan8_32.msi).

### Version 8.0.3 800 (06.05.2021)

#### MAGELLAN und Crystal Reports 2020

* NEW: Mit dieser Version unterstützen wir Crystal Reports 2020. Hintergrund ist, dass Crystal Reports 2020 eine reine 64 Bit Anwendung ist und MAGELLAN eine reine 32 Bit Anwendung ist. Es werden zusätzliche 64 Bit Treiber mitgeliefert und installiert, die es Crystal Reports ermöglichen per ODBC auf die MAGELLAN-Datenbank zuzugreifen.

### Version 8.0.1 800 (30.04.2021)

#### Veröffentlichung

* NEW: Unsere neue Version 8 wurde veröffentlicht, Schulen mit Supportvertrag wird in den kommenden Tagen die neue Lizenz zugesandt.
  * Alle Neuerungen können Sie hier nachlesen: [https://doc.magellan.stueber.de/changelog/neu.mag8/](https://doc.magellan.stueber.de/changelog/neu.mag8/)
  * Eine Anleitung für den Umstieg finden Sie hier: [https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-7-auf-8/](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-7-auf-8/)
  
## Version 7

### 7.1.31 - 720 (unveröffenticht)

#### MAGELLAN Schulverwaltung

* FIX: Problem beim Einschulen (Fachtafelhaken setzen ohne Auswahl einer Fachtafel) von Schülern behoben

#### Schnittstellen

* FIX: [Berlin] Für die Abiturdatenstatistik wurde ein Problem beim Ausspielen der Daten behoben. Wenn Sie die Version 7.1.30 von MAGELLAN einsetzen, können Sie am Arbeitsplatz von dem aus exportiert wird die MAGELLAN.exe tauschen. [Download MAGELLAN.exe](https://my.hidrive.com/lnk/85yJiIJU)

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: BER-IBA-AS-2020.dws - Korrekturen
* CHANGE: Aktualisierte Ausgaben der Skripte [BER-IBA-AS-2020](https://doc.la.stueber.de/03.ber/ber-iba-hj-2020dws/) und [BER-IBA-AS-2020](https://doc.la.stueber.de/03.ber/ber-iba-as-2020dws/) finden Sie unter folgendem [Vorab-Download](https://my.hidrive.com/lnk/IByJi3hD).
* FIX: SAR-APO-2018.dws - Hinweis auf "Nichtbestehen des Abiturs" bei erfolgter mdl. Prüfung aufgrund der Abweichungsprüfung und erneutem Ausführen des Skriptes korrigiert [Vorab-Download](https://my.hidrive.com/lnk/DaypC5gW)
* FIX: [Sachsen] `Skripte SAC-APO-BGY-2017 (DUBAS).dws` 

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: Klassenliste (Sorgeberechtigte Mobil und Geburtsdatum).rpt
* FIX: Schülerliste (Förderung).rpt

##### Berlin

* FIX: BER-Schul Z 306 (04.21)(FG).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)
* FIX: BER-Schul Z 306 (04.21).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)

##### Saarland

* CHANGE: SAR-GY-ABI (GOS2.0).rpt (Bezeichnung der Sprachreferenz wird unter Fremdsprachen ausgelesen)

##### Sachsen

* FIX: SAC-BS-AZ (A.02.04).rpt (Zeugnisbemerkungen werden korrekt ausgegeben)
* CHANGE: SAC-BG-AZ (E.01.05).rpt - ergänzt um Ausgabe Namen SchulleiterIn/TutorIn
* FIX: SAC-BS-JZ (A.02.01).rpt (Ausgabe von "---" wenn keine unentschuldigten Fehltage vorliegen)

##### Niedersachsen

* CHANGE: NIE-GY-ABI (2021).rpt (Der Satz "Die Allgemeine Hochschulreife ist im Deutschen Qualitätsrahmen (DQR) dem Niveau 4 zugeordnet." wird standardmäßig auf dem Zeugnis unter Bemerkungen ausgegeben.

### 7.1.30 - 720 (11.06.2021)

#### MAGELLAN Schulverwaltung

* FIX: Das Kürzel im Verzeichnis `Einschulmerkmale` wurde auf 20 Zeichen erhöht

#### Schnittstellen

* FIX: [Berlin] Für die Abiturdatenstatistik wurde ein Problem beim Ausspielen der Daten behoben. Wenn Sie die Version 7.1.30 von MAGELLAN einsetzen, können Sie am Arbeitsplatz von dem aus exportiert wird die MAGELLAN.exe tauschen. [Download MAGELLAN.exe](https://my.hidrive.com/lnk/85yJiIJU)

#### Skripte

* CHANGE: `Schüler fortschreiben`Strikteres Vorgehen beim Schüler fortschreiben; beim Finden des SchülerZeitraum Datensatzes wird auch der Gewechselt-Status berücksichtigt. 
* CHANGE: `Importiere SDTF.dws` Beim Übertrag der Schülerkurswahlen mit der Option `nur geänderte Daten` aus DAVINCI nach MAGELLAN wird vorab geprüft, ob unter `Schüler > Fächer > Leistungen > Endnote` für ein Fach eine Note erfasst wurde. Ist eine Note bei einem Fach erfasst, werden die Schülerfachdaten des Schülers nicht geändert oder ergänzt. Das Skript gibt zum Hinweis den `Schülernamen` und die `SchülerID` mit aus. 
* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik, Fehlermeldung wenn ein Prüfungsergebnis fehlt
* FIX:  DE-DIAP-2018 diverse Korrekturen in der Vorschlagsautomatik,Fehlermeldung wenn ein Prüfungsergebnis fehlt

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, unsortiert).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat-Durchschnitt, sortiert).rpt

##### Berlin

* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 250 Co (04.21).rpt
* NEW: BER-Schul Z 306 (04.21)(FG).rpt
* NEW: BER-Schul Z 306 (04.21).rpt
* CHANGE: BER-Schul Z 250 (11.19).rpt
* NEW: BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.21).rpt
* FIX: BER-Schul Z 324 (11.19).rpt
* NEW: BER-Schul Z 255 (2020.2021).rpt
* NEW: BER-Schul Z 256 (2020.2021).rpt

##### Sachsen

* FIX: SAC-BS-AS (A.02.04).rpt (Berechnung Durchschnittsnote)
* CHANGE: SAC-BF-AS (A.02.07).rpt
* CHANGE: SAC-BF-AS (B.04.05).rpt
* CHANGE: SAC-BF-AZ (B.03.04).rpt
* CHANGE: SAC-BS-AS (A.02.05) 2spaltig.rpt
* CHANGE: Zertifikat (F.01.09).rpt

##### Auslandsschulen

CHANGE: DAS-GY-AZ ohne FHR (Anlage 9a).rpt
CHANGE: DAS-GY-AZ mit FHR (Anlage 9b).rpt

### 7.1.29 - 720 (06.05.2021)

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX:  DE-DIAP-2015 diverse Korrekturen in der Vorschlagsautomatik
* NEW:  DE-DIAP-2018 

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

FIX: Schülerpersonalblatt (mit Fremdsprachen) A5.rpt Ausgabe der Sorgeberechtigten
FIX: Schülerpersonalblatt (mit Fremdsprachen).rpt Ausgabe der aktuellen Klassen
NEW: NRW-BK-ABI (Anlage D41)(2018)(GeR).rpt

### 7.1.28 - 720 (21.04.2021)

#### Datenmanipulation

* Fix: Beim ersten Start von MAGELLAN (Anmeldung muss als sysdba erfolgen) läuft ein Skript durch, dass die SchülerzeitraumID für alle SchuelerZeugnisbemerkungen neu vergibt. Die Datenbankversionsnummer wird hierdurch nicht verändert.

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW:  `NRW-APO-BK-2018` Dieses Skript prüft ab, dass nicht mehr als 32 Grundkurse eingebracht werden. Die Beschreibung des Skriptes finden Sie [hier](https://doc.la.stueber.de/08.nrw/nrw-apo-bk-2018/).
Falls Sie die Datei einzeln herunterladen möchten: [[hier herunterladen](https://my.hidrive.com/lnk/3qSpCCDo)](https://my.hidrive.com/lnk/3qSpCCDo) Bitte legen Sie die Dateu auf Ihrem Serverrechner im Verzeichnis `Skripte > Nordrhein-Westfalen` ab.

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

NEW: Passend zum neuen Skript `NRW-APO-BK-2018` wurde der Bericht `NRW-BK-ABI (Anlage D33b - 2018).rpt` veröffentlicht.
Falls Sie die Datei einzeln herunterladen möchten: Bitte laden Sie die Datei unter folgendem Link herunter und legen ihn über die MAGELLAN-Oberfläche unter `Extras > Berichte organisieren > Zeugnisse > Nordrhein-Westfalen` ab: [https://my.hidrive.com/lnk/RPyJiXKR](https://my.hidrive.com/lnk/RPyJiXKR).
Bitte beachten Sie die Anleitung unter [https://doc.la.stueber.de/berichte/zeugnisse/nrw_zeugnisse/#nrw-bk-abi-anlage-d33b-2018rpt](https://doc.la.stueber.de/berichte/zeugnisse/nrw_zeugnisse/#nrw-bk-abi-anlage-d33b-2018rpt)!

### 7.1.27 - 720 (19.04.2021)

#### Installation

* FIX: Problem der Registrierung eines Teils der Crystal Reports-Runtimeversion behoben

#### MAGELLAN SCHULVERWALTUNG

* FIX: `Klassen > Zeiträume > ENBREA Leistungsprofile` beim Anlegen neuer Kurse bleibt der im Zeitraum eingetragene Klassenlehrer sichtbar
* FIX: Für Bewerber mit Nebenlaufbahn (Schülerkopien) kann mit Sekretariatsrechten per Bewerberverfahren den Bewerbungsstatus unter `Daten1` angepasst werden.
  
#### Schnittstellen

##### SAXSVS

* FIX: Verarbeitung der Extern-ID aus SAXSVS überarbeitet, damit können Daten für importierte Schüler korrekt bearbeitet werden

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: NRW-APO-BK-2018 Dieses Skript prüft ab, dass nicht mehr als 32 Grundkurse eingebracht werden. Die Beschreibung des Skriptes finden Sie [hier](https://doc.la.stueber.de/08.nrw/nrw-apo-bk-2018/). Sie können es auch vor der Veröffentlichung [hier herunterladen](https://my.hidrive.com/lnk/3qSpCCDo) und auf Ihrem Serverrechner im Verzeichnis `Skripte > Nordrhein-Westfalen` ablegen.

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Nordrhein-Westfalen

* NEW: Passend zum neuen Skript `NRW-APO-BK-2018` wurde der Bericht `NRW-BK-ABI (Anlage D33b - 2018).rpt` veröffentlicht. Bitte laden Sie die Datei unter folgendem Link herunter und legen ihn über die MAGELLAN-Oberfläche unter `Extras > Berichte organisieren > Zeugnisse > Nordrhein-Westfalen` ab: [https://my.hidrive.com/lnk/RPyJiXKR](https://my.hidrive.com/lnk/RPyJiXKR). Bitte beachten Sie die Anleitung unter [https://doc.la.stueber.de/berichte/zeugnisse/nrw_zeugnisse/#nrw-bk-abi-anlage-d33b-2018rpt](https://doc.la.stueber.de/berichte/zeugnisse/nrw_zeugnisse/#nrw-bk-abi-anlage-d33b-2018rpt)!


##### Berlin

* NEW: BER-Schul Z 593 (2019.2020).rpt
* NEW: BER-Schul Z 592 (03.2020).rpt
* NEW: BER-Schul Z 594 (12.19).rpt
* NEW: BER-Schul Z 591 (03.20).rpt
* CHANGE: BER-KO (abi_4a_berechnungsbogen_kollegs)(03.12).rpt
* NEW: BER-Abi-8 (05.20).rpt

##### Saarland

Im Unterordner `Berichte\Zeugnisse\Saarland\Ministerium` finden Sie ab sofort auch Zeugnisse für Allgemeinbildende Schulen, die parallel auch auf dem BSCW Server veröffentlicht werden. Eine Anleitung zu diesen Zeugnisse steht auf dem BSCW Server bereit. Sollten Rückfragen zu den Zeugnisse auftreten, wenden Sie sich bitte an den Urheber.

* NEW: Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-AZ (Hauptphase).rpt
* NEW: Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-HJZ (Hauptphase).rpt

##### Mecklenburg-Vorpommern

* NEW: MVP-FG-ABI (2021).rpt

### 7.1.26 - 720 (06.04.2021)

!!! danger "Achtung"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstruktur

* CHANGE: ggfs. werden durch Fortschreiben übernommene Zeugnisbemerkungen korrigiert, damit die Anzeige in der Oberfläche korrigiert
* CHANGE: aus anderen Programmen übernommene externe IDs (SchuelerAusbildungen) werden geprüft, das Format wird ggfs. angepasst
* FIX: Änderung des Triggers, der Bewerbungsdaten eines vom Stammschüler kopierten Bewerbers aktualisiert

#### MAGELLAN SCHULVERWALTUNG

* CHANGE: Aktualisierung auf Crystal Reports Runtime 13.0.30
* FIX: Anzeige von fortgeschriebenen Zeugnisbemerkungen (Korrektur im Skript und auch Korrektur der bereits fortgeschriebenen Zeugnisbemerkungen)
* FIX: Zuweisen des Bewerbungsstatus per Sammelzuweisung für Bewerber, die per Kopie vom Stammschüler erzeugt wurden, wurde korrigiert. Bitte weisen Sie die Werte für die betroffenen Bewerber auf `Daten1` oder per Sammelzuweisung erneut zu.

#### Schnittstellen

##### SAXSVS

* CHANGE: Verarbeitung der Extern-ID aus SAXSVS überarbeitet, damit können Daten für importierte Schüler korrekt bearbeitet werden
* NEW: Für sächsische Schulen wird die GUID der Ausbildung in der Liste der Ausbildungen eingeblendet

#### MAGELLAN Bibliothek

* FIX: Eintrag "Ausleihe bis" bei Schülern

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: NRW-APO-2012: Das Markieren von Fächern der Kategorie `Sozialkunde` wurde korrigiert
* NEW: NRW-APO-BK-2018 (vorerst nur als Download): Dieses Skript prüft ab, dass nicht mehr als 32 Grundkurse eingebracht werden. Die Beschreibung des Skriptes finden Sie [hier](https://doc.la.stueber.de/08.nrw/nrw-apo-bk-2018/). Sie können es auch vor der Veröffentlichung [hier herunterladen](https://my.hidrive.com/lnk/3qSpCCDo) und auf Ihrem Serverrechner im Verzeichnis `Skripte > Nordrhein-Westfalen` ablegen.

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: MVP-FG-FHReife (Bescheinigung 2020).rpt *(Anlage 09 / FG (Mitteilungsblatt Nr. 5/2019)*

##### Berlin

* NEW: BER-Schul Z 500 (09.19).rpt
* NEW: BER-Schul Z 501 (09.19).rpt
* NEW: BER-Schul Z 502 (09.19).rpt
* NEW: BER-Schul Z 503 (09.19).rpt

* NEW: BER-Schul Z 520 (09.19).rpt
* NEW: BER-Schul Z 521 (09.19).rpt
* NEW: BER-Schul Z 522 (09.19).rpt
* NEW: BER-Schul Z 523 (09.19).rpt
* NEW: BER-Schul Z 526 (09.19).rpt

* NEW: BER-Schul Z 593 (10.20).rpt
* NEW: BER-Schul Z 590 (12.19).rpt

### 7.1.25 - 719 (05.03.2021)

#### MAGELLAN SCHULVERWALTUNG

* FIX: Ladeverhalten des Feldes `Verkehrsmittel` im Menü `Bewerber`
* FIX: Ladeverhalten des Feldes  `Krankenkasse` im Menü `Bewerber`
* CHANGE: Seriendruck aus dem Menü `Schüler` an deren Sorgeberechtigte auch für inaktive Schüler möglich
* FIX: Tabreihenfolge (Feldwechsel per Tabulatortaste) auf der Karte `Schüler > Zeugnis > Details` korrigiert
* FIX: Unter `Bewerber > Daten1 > Bewerbung` wurden die Felder `2.Wunsch` und `3.Wunsch` wieder eingeblendet, dort kann auf eine Schule aus der Liste Schulen verwiesen werden.
* CHANGE: Die Anzeige für hohe Auflösungen wurden überarbeitet
* FIX: Beim Anlegen eines neuen Sorgeberechtigten vom Schüler/Bewerber/Vagabunden aus, kann die Postleitzahl auch gefüllt werden, wenn man nur den Ort erfasst und die Tabtaste drückt.
* FIX: Beim Anlegen eines neuen Bewerbers werden die frisch erfassten Daten in dem Moment gespeichert, indem man das Untermenü `Familie` aufruft.
* FIX: Kopiert man einen Stammschüler als Bewerber, werden für die Bewerberkopie im Seriendruck die Sorgeberechtigten (des Stammschülers, die für die Bewerberkopie auch in Daten1 gezeigt werden) ausgegeben.
* FIX: Unter `Abitur > Qualifikation > Layout` anpassen können Felder ein- und ausgeblendet werden.
* FIX: Alle Dropdown-Felder auf der Karte `Schüler > Zeugnis > Details` erkennen eine Eingabe, wenn die Auswahl per Return bestätigt wird, damit werden die Felder beim Wechsel der Karte gespeichert

#### MAGELLAN BIBLIOTHEK

* FIX: Das Feld `Gültig bis` unter `Lehrer > Daten` kann geändert oder geleert werden

#### MYMAGELLAN

* FIX: Problem beim Speichern behoben

#### MYMAGELLAN Center

* CHANGE: Wenn ein Lehrer für einen Schüler als Fachlehrer und Tutor erfasst ist, können jetzt Zeugnisbemerkungen erfasst werden. Für diese Änderung muss die *.mymx neu erstellt werden.

#### MAGELLAN Schnittstellen

##### NRW

* FIX: `SchülerOnline > Schüler Sorgeberechtigte`: Korrektur der Kopfzeile

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: SAR-APO-2018.dws = Notenbuffer erhöht
* FIX: Importiere SDTF.dws = Umgang mit nicht gesetzter Fachkursnummer beim Übertrag des Lehrerunterrichts.
* FIX: NRW-APO-2012
  * Die Prüfung auf die Einbringung von Zusatzkursen wurde angepasst
  * Neuer Fachstatus "Projekt" zur Markierung von Projektfächern

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Berlin

* CHANGE: BER-GY-ZAS (Schul II 929-9)(12.08).rpt (Berechnung des Kurshalbjahres für G8 angepasst)
* NEW: BER-Abi-3 – Angaben zur Abiturprüfung (VO GO)(05.20).rpt

##### Saarland

* NEW: SAR-Antrag auf Zulassung (Anlage 5).rpt

##### Niedersachsen

* FIX: NIE-GY-ABI (2021).rpt 

##### Auslandsschulen

* FIX: DAS-Prüfungsbogen (Anlage 7 zu DIA-PO)(2018).rpt (Im gesellschaftswiss. Bereich können nun bis zu 4 Fächer angezeigt werden. Da sich üblicherweise die Bilinguale Sprache im Abitur nicht ändert, lesen wir einfach rückwärts von Q4 aus nach den Eintrag aus den zugewiesenen Kurssprachen aus und verwende diese dann im Bericht.)
* NEW: DAS-GY-ABI (DIA)(2021).rpt (Anpassungen gemäß Richtlinien für die Ausweisung der Sprachen auf den Abschlusszeugnissen der Deutschen Schulen im Ausland (Zeugnisse über die Allgemeine Hochschulreife, den Mittleren Schulabschluss und den Hauptschulabschluss)
Beschluss der Kultusministerkonferenz vom 25.09.2019 vorgenommen)

### 7.1.24 - 719 (02.02.2021)

#### MAGELLAN SCHULVERWALTUNG

* FIX: "Schüler fortschreiben.dws" Informationen aus `Klassen > Zeiträume` werden übernommen

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: "Schüler fortschreiben.dws" Informationen aus `Klassen > Zeiträume` werden übernommen

### 7.1.23 - 719 (29.01.2021)

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstruktur

* CHANGE: Zusätzlich zum kleinen und großen Latinum wurde ein Feld zum Erfassen des mittleren Latinum eingebunden. Das Feld heißt in der Datenstruktur `LatinumMittel` und wird in der Tabelle `SchuelerAbi` gespeichert. In der Oberfläche finden Sie das Feld unter `Abitur > Prüfung > Sprachkenntnisse`.

#### MAGELLAN SCHULVERWALTUNG

* FIX: Beim Drucken von Zeugisformularen für Nebenschüler wird der PDF-Export (falls aktiviert) nicht in das Dokumentenverzeichnis des Nebenschülers, sondern in das Dokumentenverzeichnis des Stammschülers abgelegt.

#### MYMAGELLAN

* CHANGE: Zeugnisbemerkungen werden in voller Länge aus MAGELLAN übergeben
* FIX: Eingabe von Noten/Punkten über Fächer, korrekter Filter gesetzt
* CHANGE: Ein bereits für die Bearbeitung geöffnete Datei kann nicht erneut geöffnet werden, es erscheint eine Meldung.
* FIX: Anzeige der `schriftlichen Note4` in der Schüleransicht korrigiert

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: SAR-APO-2018.dws (gemäß Gymnasialen Oberstufe Saar (GOS) vom vom 17. April 2018.)
* NEW: NIE-APO-G9-2018.dws 

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Klassen

FIX: Zeugnisliste nach Schülerfächern (Kopfnoten).rpt

##### Berlin

* FIX: BER-Schul Z 303 (11.19).rpt (Entwertung unter Zeugnisbemerkung entfernt, max. Anzahl von Fächern des Sprachlich-literarisch-künstlerisches Aufgabenfeld (Aufgabenfeld I): auf 8 erhöht)
* FIX: BER-Schul Z 350 (10.07).rpt (eingebrachte Kurshalbjahre werden entsprechend der Eintragung der Halbjahre unter `Abitur > Qualifikation` im Feld "eingebrachte Halbjahre" auf dem Bericht ausgelesen
* Fix: BER-KO-AS (Schul Z 320a-b)(03.11).rpt (Tendenznoten werden ausgegeben)

##### Saarland

* NEW: SAR-GY-ABI (GOS2.0).rpt
* NEW: SAR-GY-AZ (GOS2.0).rpt
* NEW: SAR-GEMS-AS (Klasse 9 mit Prüfung)(ab 2021).rpt
* NEW: SAR-GEMS-AS (Klasse 9 ohne Prüfung)(ab 2021).rpt

##### Niedersachsen

* NEW: NIE-GY-ABI (2021).rpt

### 7.1.22 - 718 (08.01.2021)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstruktur

* CHANGE: Trigger "Schueler_BD" (Hinzufügen fehlender Tabellen "BewerberVerfahren", "BewerberFachdaten" und
  "BewerberUnterlagen")

#### MAGELLAN SCHULVERWALTUNG

* FIX: `Schüler > Zeugnis > Details > Sammelzuweisung > Tutor` =>  die Zuweisung des Tutors für mehrere Schüler ist wieder gegeben.
* FIX: Für den Seriendruck an Nebenschüler werden die Sorgeberechtigtendaten korrekt ausgegeben
* FIX: erneutes Versetzen von Schülern in einen anderen Mandanten korrigiert
* FIX: Versetzen von Schülern in einen anderen Mandanten mit Daten aus den Tabellen "BewerberVerfahren", "BewerberFachdaten" und  "BewerberUnterlagen korrigiert
* FIX: Beim Versetzen von Schülern in einen anderen Mandanten wurde versucht für die Schülerkopie die gleiche ID (mit neuen MandantenID) zu verwenden.
* FIX: Beim Versetzen von Schülern als Vagabund oder Bewerber in einen anderen Mandanten werden die zugewiesenen Sorgeberechtigten im neuen Mandanten stets aktiviert.

#### MAGELLAN ADMINISTRATOR

* CHANGE: Lesen der Magellan.paths beim Programmstart korrigiert

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: BER-IBA-HJ-2020.dws - Korrekturen
* FIX: BER-IBA-AS-2020.dws - Berechnung des Abschluss für das 1. HJ, Korrekturen

* NEW: SAR-APO-2018.dws - Basierend auf der Verordnung zur Änderung der Verordnung – Schul-und Prüfungsordnung über die gymnasiale Oberstufe und die Abiturprüfung im Saarland vom 17. April 2018

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: DAS-GY-ABI (DIA)(2020).rpt => Ausgabe der Kurssprachen ( nicht bilingual)
* FIX: Zeugnisliste BBS.rpt (überflüssige Tabellen entfernt, Verknüpfungen optimiert)
* FIX: BER-KO-AS (Schul Z 320a-b)(03.11).rpt (Bemerkungen werden ausgegeben)
* FIX: BER-KO-AS (Schul Z 322)(03.11).rpt (Unterberichtsverknüpfung Geografie korrigiert)
