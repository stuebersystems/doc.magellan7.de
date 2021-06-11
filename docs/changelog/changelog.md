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

## **Version 8**

### 8.0.9 801 (11.06.2021)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!
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

##### Auslandsschulen

CHANGE: DAS-GY-AZ ohne FHR (Anlage 9a).rpt
CHANGE: DAS-GY-AZ mit FHR (Anlage 9b).rpt

### 8.0.8 801 (27.05.2021)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

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

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

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
  
## **Version 7**

### 7.1.30 - 720 (11.06.2021)

#### MAGELLAN Schulverwaltung

* FIX: Das Kürzel im Verzeichnis `Einschulmerkmale` wurde auf 20 Zeichen erhöht

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

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

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

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

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

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

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
