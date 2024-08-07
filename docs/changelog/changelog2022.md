# Änderungen 2022

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

## Wichtige Hinweise

!!! danger "Achtung"

    Das Vorgehen für die Installation hat sich seit der 9.5.0 geändert.<br/>
     - **Magellan** gibt es jetzt die Varianten **64-Bit und 32-Bit**.<br/> 
     - Die für den Druck benötigte **Runtime-Version von Crystal Reports** ist nicht mehr Teil des Installationspaketes, sondern wird **gesondert auf allen Clients und dem Server installiert**. 
    
    Beim Update ab der 9.5.0 müssen Sie das korrekte Magellan-Paket wählen (32- oder 64 Bit) und **zusätzlich** die korrekte Crystal Reports Runtimeversion (32- oder 64 Bit) installieren. Bitte lesen Sie hierfür die aktualisierten Updateanleitung für [Magellan](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung) und die [Crystal Reports Runtime](https://doc.magellan.stueber.de/schulverwaltung/update/cr-aktualisieren/)!

!!! important "Wichtig"

    **Druckproblem mit Windows 11 22H2 und Crystal Reports Runtime** behoben mit der Version Magellan 9.5.0.

    **OpenSSL-Schwachstelle**: In unseren Softwareprodukten setzen wir kein OpenSSL ein.

    **Log4Shell-Schwachstelle**: Unsere Software-Produkte Enbrea, DaVinci, Magellan, CONFIRE SHOWTIME und CONFIRE SHERLOCK sind alle nicht von der Log4Shell-Schwachstelle betroffen, da keines dieser Produkte Java verwendet oder von einer externen Java-Anwendung abhängig ist. Auch unsere öffentlich zugänglichen Dienste (z.B. Ticketsystem, Webseiten) nutzen alle kein Java. Bitte lesen Sie auch unseren [Blogeintrag](https://blog.stueber.de/posts/log4j-desaster).

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus Magellan Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMagellan**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `Magellan Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## Version 9

### Version 9.5.3 902 (21.11.2022)

#### Magellan Schulverwaltung

* FIX: Vagabund/Bewerber: Beim Erzeugen eines neuen Ausbildungsdatensatzes wird "GUID beibehalten", wenn die Standardoption beibehalten wird. 
* FIX: Korrektur beim Aufruf der Druckvorschau für 32-Bit-Betriebssysteme

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: [Vorabdownload](https://my.hidrive.com/lnk/0sRkNVHj) | Im Skript "Zugriffsrechte zuweisen" wurde der Zugriff für die Rechtegruppe `Sekretariat1` auf die neue Tabelle `FremdsprachenNoten` ergänzt. 

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `NRW-BLNW-OS.rpt` 
* FIX: `SAC-FOS-FHReife (D.01.04).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `SAC-FOS-JZ (D.01.02)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `SAC-FOS-HJZ (D.01.01).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `SAC-FO-HJI (D.01.01)(Fachpraktischer Unterricht).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)

### Version 9.5.2 902 (10.11.2022)

#### Magellan Schulverwaltung

* FIX: Unter `Schüler > Daten2` ergab der Aufruf einiger Felder eine Zugriffsverletzung und zeigten auch keine Inhalte:
    * Höchster Abschluss ABS: Abschluss, Bildungsgang
    * Höchster Abschluss (erworben): Abschluss ABS, Abschluss BBS
    * Höchster Abschluss BBS: Abschluss, Beruf, Bildungsgang


### Version 9.5.1 902 (09.11.2022)

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: [Vorabdownload](https://my.hidrive.com/lnk/0sRkNVHj) | Im Skript "Zugriffsrechte zuweisen" wurde der Zugriff auf die neue Tabelle `FremdsprachenNoten` ergänzt.

### Version 9.5.0 902 (08.11.2022)

!!! danger "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte synchronisieren Sie im Anschluss die Zugriffsrechte. Eine genaue Anleitung finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

!!! danger "Wichtig"

    Das Vorgehen für die Installation von Magellan hat sich geändert.<br/><br/>
     - Magellan gibt es jetzt die Varianten 64-Bit und 32-Bit.<br/> 
     - Die für den Druck benötigte Runtime-Version von Crystal Reports ist nicht mehr Teil des Installationspaketes, sondern wird gesondert auf Clients und Servern installiert. 
    
    Beim Update auf die 9.5.0 müssen Sie das korrekte Magellan-Paket wählen (32- oder 64 Bit) und **zusätzlich** die korrekte Crystal Reports Runtimeversion (32- oder 64 Bit) installieren. Bitte lesen Sie hierfür die aktualisierten Updateanleitung für [Magellan](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung) und die [Crystal Reports Runtime](https://doc.magellan.stueber.de/schulverwaltung/update/cr-aktualisieren/)!

#### Datenstrukturänderung

* NEW: neue Verzeichnis `Fremdsprachennoten`.
* NEW: neue Felder zum Erfassen der Fremdsprachennote (Bewerbungsnote) unter `Schüler/Bewerber > Daten3 > Fremdsprachenfolge1-4`

#### Magellan Schulverwaltung

* FIX: RLP-FW-APO-2010.js berücksichtigt den Fachstatus "AufgstGK" für aufgestockte Grundkurse
* NEW: `Extras > Vorlagen organisieren` Open Office Dokumente *.odt und *.ott werden angezeigt
* FIX: Focus beim Anlegen eines Bewerbers auf der Karte Daten1 dem Feld "Anrede"
* FIX: [BER] unter Extras > Export > Schüler (Berlin)  > Schüler (ABS und BBS) wurde der Export für Schüler mit Status in der 2.FS korrigiert.
* CHANGE: `Abitur > Qualifikation`: Umbenennung der Spalten `LeistungsartQ1`-`LeistungsartQ6` und `BestandeQ1`-`BestandenQ6` in `LeistungsartE1`- `LeistungsartQ6` und `BestandenQ1`- `BestandenQ6`

#### Magellan Administrator

* CHANGE: Unter `Benutzerverwaltung > Extras` wurden die Punkte zur Replikation ausgeblendet

#### Schnittstellen

* FIX: NRW => SIM.TXT SchülerInnen, die im letzten Jahr bei uns einen Abschluss erworben haben und dieses Jahr einen neuen Bildungsgang besuchen, werden auch als Ausgeschulte Schüler übergebn
* FIX: NRW => SIM.TXT ist ein Schüler zugleich Nebenschüler und Stammschüler wird er in der SIM.txt mit zwei Datensätzen mit den unterschiedlichen Klassen ausgegeben
* FIX: NRW => SIM.TXT Herkunftschule bei Schülerstatus Neuzugang
* FIX: NRW => SIM.TXT Schüler wird als Abgänger erkann, wenn Schüler > Laufbahn > Abschluss > Abschluss 1 ein Wert eingetragen ist und nicht mehr nur wenn der Wert auf 0A gesetzt ist
* FIX: SAXSVS => Import mit Lizenz Landestatistik 2022 möglich
* CHANGE: SAXSVS => neues Schlüsselverzeichnis `Bildungsgaenge.keys`
* FIX: `Expotiere SDTF.dws` Die Schulnummer beim Datensatz L1 wird jetzt korrekt ausgegeben. Es handelt sich um die Schulnummer des Mandanten in Magellan `Mandant > Daten1 > Schulnummer`
* CHANGE: BER => Beim Export `Schüler (CSV) schueler_sorgebe.export.csv` werden Sorgeberechtigten-Verhältnis1-Verhältnis10 leer ausgegeben.
* FIX: BER => Beim Export `Schüler (CSV) schueler.export.csv` werden die Klassenkürzel korrekt ausgegeben.

#### Importe

CHANGE: [NRW] Zeichensatzcodierung und Umlaute + ß einzelner *.keys für NRW-Importschlüssel korrigiert
CHANGE: [BER] Bezeichnung der Dateien `00_Lehraemter.keys` und `00_Lehrerausbildungen.keys` getauscht

#### Skripte

FIX: [NRW-APO-OS-2020] Ist Deutsch als SF (LK) vorhanden, wird nicht Literatur gesondert gefordert
CHANGE: [NRW-APO-OS-2020] Meldung zum Vorschlag angepasst
CHANGE: [NRW-APO-OS-2020] Die Berechnung der Besondere Lernleistung wurde angepasst, bitte beachten Sie die [Beschreibung zum Skript](https://doc.la.stueber.de/08.nrw/nrw-apo-os-2020/#besondere-lernleistung). 

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

* FIX: `Unfallanzeige.rpt` einseitig
* FIX: `Schülerliste (mit Sorgeberechtigten).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `Schülerüberweisung.rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `NRW-ABI-OS (2021).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `NRW-BLNW-OS.rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `SAC-BS-AS (Vorbereitungsklasse) (A.01.06)V1.rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `Klassenliste (Sorgeberechtigte Adresse, Mobil, Email).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `Klassenliste (mit Elternsprechern und Mail- und Postadressen).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `Mandant (Prüfung der Schüler des aktuellen Halbjahres auf doppelte AusbildungsGUID).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* CHANGE: `NRW-ABI-OS (2021).rpt`:
  * Texte unter "IV.Fremdspachen" aktualsiert, bitte beachten Sie die Anleitung
  * Ausgabe und Berechnung der "Besonderen Lernleistung" aktualisiert
  * Tendenzen werden geklammert ausgegeben
* NEW: `Mandant (Wiederholerliste)`, bitte beachten Sie die Anleitung. [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `Sorgeberechtigte ohne Kinder im aktuellen Zeitraum.rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: Sorgeberechtigte ohne Kinder im aktuellen Zeitraum.rpt
* FIX: `BER-Schul Z 502 (09.19).rpt`[Download](https://my.hidrive.com/share/3pr60tsv6j)
* FiX: `BER-Schul Z 501 (09.19).rpt`[Download](https://my.hidrive.com/share/3pr60tsv6j)
* FiX: `BER-Schul Z 523 (09.19).rpt`[Download](https://my.hidrive.com/share/3pr60tsv6j)


### Version 9.0.7 901 (23.08.2022)

#### Magellan Schulverwaltung

* FIX: Wenn das Anlegen eines Ausbildungsdatensatzes abgebrochen wird, wird kein neuer Datensatz angelegt
* NEW: Um das versehentliche Löschen von Schülern zu verhindern, wurde eine Bestätigung per Checkbox vor dem endgültigen Löschen eingebunden.
* CHANGE: Beim Aufruf der Unterkarten `Daten1` für die Menüpunkte `Lehrer` und `Personen` ist kein Feld markiert um versehentliche Eingaben zu verhindern.
* CHANGE: Für `Personen > Daten1` und für `Lehrer > Daten1` sitzt der Focus beim Aufruf der Karte auf keinem Feld um versehentliche Fehleingabe zu verhindern
* CHANGE: Schlüsselverzeichniss `Lehrämter` geänderter Schlüssel

#### Schnittstellen

* FIX: NRW => Ausspielen der Grundschulempfehlung für GE und GY korrigiert
* NEW: NRW ABS => Neuer Katalog: `AS_Bewerbungsempfehlungen.keys`

#### Magellan Administrator

* FIX: Funktionalität zum Anlegen der Benutzer überarbeitet

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

* NEW: Lehrer (Abwesenheitsstatistik gruppiert je Jahr-nach Lehrer und Grund).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: Lehrer (Abwesenheitsstatistik je Jahr).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: Lehrer (Abwesenheitsstatistik von-bis).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: Schülerliste (Fehlzeiten nach Klasse gruppiert).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)

### Version 9.0.6 901 (19.08.2022)

#### Magellan Schulverwaltung

* FIX: Wenn das Anlegen eines Ausbildungsdatensatzes abgebrochen wird, wird kein neuer Datensatz angelegt
* NEW: Um das versehentliche Löschen von Schülern zu verhindern, wurde eine Bestätigung per Checkbox vor dem endgültigen Löschen eingebunden.
* CHANGE: Beim Aufruf der Unterkarten `Daten1` für die Menüpunkte `Lehrer` und `Personen` ist kein Feld markiert um versehentliche Eingaben zu verhindern.
* CHANGE: Für `Personen > Daten1` und für `Lehrer > Daten1` sitzt der Focus beim Aufruf der Karte auf keinem Feld um versehentliche Fehleingabe zu verhindern

#### Schnittstellen

* FIX: NRW => Ausspielen der Grundschulempfehlung für GE und GY korrigiert
* NEW: NRW ABS => Neuer Katalog: `AS_Bewerbungsempfehlungen.keys`

#### Magellan Administrator

* FIX: Funktionalität zum Anlegen der Benutzer überarbeitet

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

* NEW: Lehrer (Abwesenheitsstatistik gruppiert je Jahr-nach Lehrer und Grund).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: Lehrer (Abwesenheitsstatistik je Jahr).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: Lehrer (Abwesenheitsstatistik von-bis).rpt [Download](https://my.hidrive.com/share/3pr60tsv6j)

### Version 9.0.5 901 (26.07.2022)

#### Magellan Schulverwaltung

* FIX: Problem beim Anzeigen von Schülerdaten auf Karten Daten1-3 gelöst

#### Skripte

#### Schnittstellen

* FIX: `Zuweisen von Zugriffsrechten` => Kleinere Korrektur für `SchuelerFamilie`

* NEW: **Niedersachsen** => aktuelle Schnittstelle freigegeben

### Version 9.0.4 901 (21.07.2022)

#### Magellan Schulverwaltung

* CHANGE: Wordseriendruckvorlagen überarbeitet (Schuladresse und ggfs. Seriendruckquelle entfernt)
* FIX: PDF-Ablage für den Seriendruck aus dem Schülermenü (Betriebe, Sorgeberechtigte)

#### MyMagellan Center

* FIX: Problem beim Einlesen (bspsw. bei Fehltagen, Fehltagen unentschuldigt, Fehlstunden, Fehlstunden unentschuldigt) aus `*.mymx` behoben. [Vorabdownload der MagellanAdmin.exe](https://my.hidrive.com/share/9mtntyk820) und [Anleitung](https://doc.kb.stueber.de/support/exe_tauschen/)

#### Schnittstellen

* NEW: **SHL** => Schnittstelle und importierbare Kataloge aktualisiert
* NEW: **MVP** => Schnittstelle aktualisiert
* NEW: **NRW** => Schnittstelle aktualisiert, aktuelle Schlüssel als importierbare Kataloge hinterlegt, Lehrer-Soll-Schlüssel werden mit DaVinci veröffentlicht, können aber [hier](https://my.hidrive.com/share/6g6u80eu18) vorab heruntergeladen werden.

#### Skripte

Eine Anleitung zum Austausch von Skripten finden Sie [hier](https://doc.kb.stueber.de/support/skript_tauschen/).

* FIX: `BER-FW-APO-2017.js` Korrektur der Regel zur Prüfungsfachkombination 33

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

##### Ausland

* NEW: `DAS-Verzeichnisliste der Prüflinge Abitur (Anlage 7) mit Fachkürzeln.rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `DAS-Verzeichnis der Prüflinge (§ 14 Absatz (5) DIA-PO).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23).rpt` (Korrektur Hinweis Qualiphase/MSA) [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23)_Pandemie.rpt` (Korrektur Hinweis Qualiphase/MSA) [Download](https://my.hidrive.com/share/3pr60tsv6j)

##### Berlin

* NEW: `BER-GY (abi_4_berechnungsbogen)(05.20).rpt` [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-GY%20%28abi_4_berechnungsbogen%29%2805.20%29/) und [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 513 – Zeugnis der Fachhochschulreife (zweij. FOS– (4 S.) (12.19).rpt` [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-Schul%20Z%20513%20%E2%80%93%20Zeugnis%20der%20Fachhochschulreife%20%28zweij.%20FOS%E2%80%93%20%284%20S.%29%20%2812.19%29/) und [Download](https://my.hidrive.com/share/3pr60tsv6j) herunterladen.
* CHANGE: `BER-Abi-18b (Meldung zur weiteren muendlichen Pruefung (12.21).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 592 (03.2020).rpt` Schreibfehler korrigiert [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 256 (2021.2022).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 306 (03.22).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 213(2021.2022)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 255 (2021.2022).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 324 (03.22).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 212 (2021-2022)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 320 a–b (11.19)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 591 (03.20)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 594 (12.19)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 593 (2019.2020)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 593 (10.20)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 592 (03.2020)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 590 (12.19)` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* NEW: `BER-Schul Z 322 (11.19).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `BER-Schul Z 513 – Zeugnis der Fachhochschulreife (zweij. FOS– (4 S.) (12.19).rpt` (Endnotenumrechnung bei 4 Punkten) [Download](https://my.hidrive.com/share/3pr60tsv6j)

##### Baden-Württemberg

* NEW: `BAW-BG (Schülerzeugnisblatt).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j) und [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/baw/BAW-BG%20%28Sch%C3%BClerzeugnisblatt%29/)

##### Sachsen

* FIX: `SAC-BS-AS (A.01.07)(Einstiegsqualifizierung).rpt` (Ausgabe unentschuldigter Fehltage). [Download](https://my.hidrive.com/share/3pr60tsv6j)
* FIX: `SAC-FOS-JZ (D.01.02).rpt` [Download](https://my.hidrive.com/share/3pr60tsv6j)

##### Nordrhein-Westfalen

* CHANGE: `NRW-BK-AZ (E01-0A).rpt` Korrektur der Namensformel für das Zusammensetzen von Vorname, 2.Vorname, Zusatz und Nachname [Download](https://my.hidrive.com/share/3pr60tsv6j)

### Version 9.0.3 901 (16.06.2022)

#### Magellan Schulverwaltung

* FIX: Im Menü `Bewerber` wurde für den Seriendruck an Sorgeberechtigte die Ausgabe der Sorgeberechtigtendaten für kopierte Bewerber (Bewerber mit gefüllter IDIntern) korrigiert.
* FIX: Excelexport aus dem Menüpunkt `Mittelstufe`
* CHANGE: In der `MAGELLAN9_BEISPIEL.FDB` wurde die Daten (Schülerdaten, Zeitraumdaten usw.) um ein Jahr erhöht.

#### MyMagellan

* FIX: Problem beim `Speichern unter` behoben

#### Magellan Bibliothek

* NEW: Unter `Schüler` wurden bisher die Spalten `Zeitraum` und `Klasse` gezeigt, im Ausleih-Assistenten unter `Ausleihe` wurde die Spalte `Klasse` gezeigt. Die Spalten `Klasse` und `Zeitraum` enthielten jeweils die höchste Klasse und den höchsten Zeitraum des Schülers. Wurde ein Bestandsschüler beispielsweise bereits ins Folgehalbjahr versetzt, wurde die neue Klasse und das Folgehalbjahr gezeigt. Diese beiden Spalten wurden umbenannt:
     * `Klasse` heißt jetzt `höchste Klasse` und `Zeitraum` heißt jetzt `höchster Zeitraum`.
     * Zusätzlich gibt es zwei berechnete neue Spalten, mit den Titeln `aktuelle Klasse` und `aktueller Zeitraum`, die sich am Stand je Systemdatum orientieren. Mit Hilfe dieser Änderungen können Sie Medien für die aktuelle und auch die kommende Klassensituation verleihen. Alle vier Spalten werden im Menü `Ausleihe` im Ausleihassistenten und im Menü `Schüler` gezeigt. Bitte beachten Sie die Dokumentation für das Menü [Menü `Schüler`](https://doc.magellan.stueber.de/bibliothek/howto/schueler/#hochste-vs-aktuelle-klasse) und für den [Assistenten im Menü `Ausleihe`](https://doc.magellan.stueber.de/bibliothek/howto/ausleihe/#hochste-vs-aktuelle-klasse).

#### Skripte

Eine Anleitung zum Austausch von Skripten finden Sie [hier](https://doc.kb.stueber.de/support/skript_tauschen/).

* FIX: `Synchronisiere BBS.dws` procedure SynchronizeBBSDetails_BER_BS(Schueler: TSchueler)
* FIX: `Synchronisiere BBS.dws`  Spezielle Variante für Saarland unter `Ihr Server\...\Stueber Systems\Magellan 9\Skripte\Saarland`.<br/>Anleitung utner [https://doc.la.stueber.de/12.sar/sar-synchronisiere-bbs/](https://doc.la.stueber.de/12.sar/sar-synchronisiere-bbs/)
* FIX: SAR-APO-2018.dws: Einbringung fortgeführte Fremdsprache korrigiert
* CHANGE: NRW-APO-BK-2018.dws: Schreibweise `DIFF` für Unterrichtsart ergänzt (zusätzlich zu Diff)
* FIX: `DE-DIAP-2018.dws` Optimale Markierung bei mehreren Naturwissenschaften
* FIX: `NRW-APO-BK-2018.dws ` optimale Markierung bei Sport
* FIX: `SAC-APO-BGY-2021.dws`: §40(2)4.: ...mindestens ein Kurshalbjahresergebnis in jedem sonstigen belegten Grundkursfach. [Vorabdownload hier](https://my.hidrive.com/lnk/YfRkNFGb)
* FIX: `BER-FW-APO-2017.js` Für Prüfungskombination 33 weitere Tauschmöglichkeiten für PF3-5 ergänzt

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Allgemein

* NEW: `Bewerberliste mit Ausbildungsbetrieb.rpt` [Anleitung hier](https://doc.la.stueber.de/berichte/bewerber/Bewerberliste%20mit%20Ausbildungsbetrieb/)

##### Berlin

* CHANGE: `BER-Schul Z 510 (12.13).rpt` (Noten-Punkte-Tabelle angepasst)
* NEW: `BER-Schul Z 256 (2021.2022).rpt`[Anleitung hier](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-Schul%20Z%20256%20%282020.2021%29/) 
* NEW: `BER-Abi-18b (Meldung zur weiteren muendlichen Pruefung (12.21).rpt`
* NEW: `BER-Abi-5 Mitteilung Abipruefung (12.21).rpt`
* NEW: `BER-Schul Z 306 (03.22)(FG).rpt`
* NEW: `BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(03.22).rpt`

##### Deutsche Auslandsschulen

* CHANGE: DAS-GY-ABI (DIA)(2021).rpt (Schullogodatei) Anleitung unter [https://doc.la.stueber.de/berichte/zeugnisse/das/DAS-GY-ABI%20%28DIA%29%282021%29/#logo](https://doc.la.stueber.de/berichte/zeugnisse/das/DAS-GY-ABI%20%28DIA%29%282021%29/#logo).

### Version 9.0.2 901 (01.04.2022)

#### Magellan Schulverwaltung

* FIX: Serienbrief an Sorgeberechtigte mit paralleler Ablage in Schülerunterordner
* FIX: Zeichenlänge für neues Kürzel beim Fachtafel extrahieren auf 20 erhöht
* FIX: Die Umbenennung der neuen Merkmalsfelder MerkmalA7-MerkmalA10 werden auch in der Auswahlliste Bewerber und Schüler gezeigt
* FIX: Bewerberpassbild löschen
* NEW: Fachtafel zuweisen:
    * Neue Option "Abweichende Fächer hinzufügen" beim "Optionen zum Verändern bestehender Fachtafeln" unter `Schüler > Fächer > Fachtafel zuweisen`.
    * NEW: Beim Nutzen der "Optionen zum Verändern bestehender Fachtafeln" unter `Schüler > Fächer > Fachtafel zuweisen` wird automatisch das Häkchen "Vorhandende Fachdaten der Schüler" gesetzt und ausgegraut. 
    * Bitte beachten Sie die geänderte [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/howto/zeugnisdaten1/#optionen-zum-verandern-bestehender-fachdaten)!
* FIX: `Klasse > Zeiträume > Leistungsprofile`: Anlegen neuer Leistungsprofile
* FIX: Problem der Anzeige der Werte aus dem Verzeichnis Fahrkarte unter `Schüler/Bewerber > Daten 4 > Fahrkarte` gelöst
* CHANGE: Ändern, Neuanlegen (auch ohne Status `Pausieren`) und Löschen von Schülerabwesenheiten unter `Schüler > Laufbahn` möglich.

#### Magellan Bibliothek

* FIX: `Schüler > Vorgänge > Mahngebühr` ausgeblendet

#### Schnittstellen

* FIX: Die Prüfroutine auf doppelte GUIDs beim Import von Daten wurden überarbeitet

#### Skripte

* FIX: NRW-APO-BK-2018: Markierung der neu einsetzenden Fremdsprache geändert
* FIX: SAR-APO-2018.dws: Der Eintrag (Beispiel Ziffern für die Ausgabe von Wochenstunden in Berichten) unter `Abitur > Qualifikation > Merkmal` wird ignoriert, es sei denn, es ist der Eintrag `A`.
* FIX: BER-BFS-Matrix-2016.dws (Fehler beim Synchronisieren)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: SAR-Antrag auf Zulassung (Antrag 5).rpt
    * Der Bericht wurde in zwei Varianten aufgeteilt:<br/>`SAR-Antrag auf Zulassung (Antrag 5) G8.rpt`<br/>`SAR-Antrag auf Zulassung (Antrag 5) G9.rpt`
    * Der Bericht gibt jeweils als Oberstufeneintrittsklasse fest eine 10 (G8) und 11 (G9) aus.
    * Zusätzlich wurde die Ausgabe des Eintrittsdatums in die Oberstufe an die Anleitung (Ausgabe des Datumswertes auch `Schüler > Merkmal > Merkmal D1`) angepasst.
    * Im Bericht wurde die Formel zur Ausgabe des Namens überarbeitet.
    * Eine Anleitung finden Sie [hier](https://doc.la.stueber.de/berichte/zeugnisse/sar/SAR-Antrag_Zulassung_Abitur%20%28Anlage%205%29), den Download der Berichtsdateien finden Sie [hier](https://my.hidrive.com/lnk/L7REt3aq)
* NEW: BER-Schul Z 213(11.19).rpt. Eine Anleitung finden Sie [hier](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-Schul%20Z%20213%2811.19%29/)
* NEW: BER-Schul Z 213(2020.2021).rpt, eine Anleitung finden Sie [hier](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-Schul%20Z%20213%282020.2021%29/)
* FIX: Bewerberpersonalblatt: Der Unterbericht "Eltern.rpt" wurde angepasst um die Sorgeberechtigten auch für Schülerkopien ausgeben zu können. Eine Anleitung für eigenen Berichte finden Sie hier: [https://doc.kb.stueber.de/cr/sb/](https://doc.kb.stueber.de/cr/sb/)
* FIX: BER-Schul Z 513a (12.13).rpt
* FIX: DSND.DAS-GY-ABI (DIA) (2019).rpt: Seitengröße angepasst

### Version 9.0.1 901 (04.03.2022)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

* NEW: EnbreaID für die Tabellen: `Banken`, `Besonderheiten`, `BetriebeKontakte`, `KlassenBesonderheiten`, `KlassenZeitraeume`, `Medien`, `MedienKataloge`, `MedienVorgaenge`, `MedizinArten`, `MedizinKategorien`, `Noten`, `SchuelerAusbildung`, `SchuelerBesonderheiten`, `SchuelerFachdaten`, `SchuelerFehlzeiten`, `SchuelerFoerderungen`, `SchuelerSchulen`, `SchuelerSorgebe`, `SchuelerZeitraeume`, `SchuelerZeugnisbemerkungen`, `SchuelerZeugnisformulare`, `Schulen`, `Zeitraeume`
  
#### Magellan Schulverwaltung

* CHANGE: Die für den Druck und die Vorschau integrierte Runtimeversion von Crystal Reports wurde aktualisiert auf Version `CR SP31`
* FIX: Wenn Sie mehrere Unfallanzeigen für einen Schüler angelegt haben und eine gezielte in der Vorschau betrachten möchten, wird die gewählte Unfallanzeige gezeigt
* FIX: Eingabemaske für den Assistenten unter `Schüler > Laufbahnprozesse > Schüler ausschulen` überarbeitet.
* CHANGE: Textänderung unter `Datenbank > Optionen > Dokumente > Berichte`
* FIX: `Extras > Schlüsselverzeichnisse|Tafel (ASV) > neuer Eintrag` erzeugte Fehlermeldung
* FIX: `Betriebe > Betrieb markieren > Rechtsklick > Betriebe zusammenführen und filtern`: `Weiter` wurde inaktiv
* FIX: Unter `Bewerber > Daten 3` werden die Felder `1. FS`, `2. FS` und `Krankenkasse` beim Menüwechsel gespeichert
* FIX: Seriendruck aus dem Menü `Klassen`
* NEW: neue Vorlage für den Seriendruck aus dem Menü `Klassen` (`Liste aller Klassen.dotx`)
* FIX: `Schüler > Zeugnis > ASV > Kategorietafel exportieren`
* FIX: Der Assistent zum `Schüler ausschulen` wurde überarbeitet
* FIX: `Bewerber > Merkmal > Merkmal A1` Kürzel mit Feldlänge 20 Zeichen kann ausgelesen werden.
* CHANGE: Auf der Unterkarte `Schüler > Zeugnis > Leistungen > Durchschnitte` werden die Felder `Durchschnitt 1-3` leer (keine 0) dargestellt, solange kein Wert erfasst ist.
* FIX: Bewerber- und Gruppenformular behalten die Anzeigegröße des Hauptfensters bei

#### MyMagellan

* FIX: Beim 'Speichern unter' wird die Datei mit `Dateiname.mymx` an der gewählten Stelle gespeichert.

#### Schnittstellen

##### SAXSVS

* FIX: Wenn unter `Schüler > Daten3 > FS1-FS4 > Erteilt` kein Wert erfasst wurde, wird es als `nicht erteilt` ausgegeben.
* FIX: Die Prüfroutine auf doppelte GUIDs beim Import von Daten wurden überarbeitet
* FIX: Prüfung für `Schüler > Daten 2> Höchster AbschlussABS > Schulform`

#### Skripte

* FIX: das Skript "Synchronisiere BBS.dws" wurde überarbeitet
* CHANGE: Beim Synchronisieren von Zugriffsrechten wurden Debug-Meldungen gezeigt, diese sind deaktiviert worden.
* FIX: SAC-FW-APO-2014.js
* FIX: NRW-APO-BK-2018.dws Vorschlag überarbeitet

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: DAS-GS-GY (Klasse 3-10).rpt (Ausgabe der Detailinformationen, Tabellenverknüpfungen optimiert)
* FIX: BER-Schul Z 300 (11.19).rpt (Bericht überarbeitet, Mehrfachausgabe von Zeugnisbemerkungen korrigiert)
* NEW: DAS-Verzeichnisliste der Prüflinge Abitur (Anlage 7).rpt )Bitte beachten Sie die [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/das/DAS-Verzeichnisliste%20der%20Pr%C3%BCflinge%20Abitur%20%28Anlage%207%29/)!)
* FIX: SAC-BG-JZ (E.01.02).rpt (unentschuldigete Fehlzeiten entfernt)
* FIX: SAC-BG-HJZ (E.01.04).rpt (unentschuldigete Fehlzeiten entfernt)
* FIX: SAC-BG-HJZ (E.01.03).rpt (unentschuldigete Fehlzeiten entfernt)
* FIX: SAC-FOS-HJZ (D.01.01).rpt: Ausgabelänge der Fächer
* FIX: SAC-FOS-HJZ (D.01.01)(Fachpraktuscher Unterricht).rpt: Ausgabelänge der Fächer
* FIX: SAC-FS-HJI (C.01.01).rpt => Zeichenlängeformel für Fächerzeichenlänge deaktiviert
* FIX: SAC-FS-HJZ (C.01.03).rpt (Zeichenlänge in Unterbericht BerufS angepasst, Textkorrekturen)
* CHANGE: SAC-FS-HJZ (C.01.03).rpt (Textänderung: hat in der gesamten bisherigen Ausbildung folgende Leistungen erreicht) 
* FIX: Drucker entfernt, Abmaße unter Datei > Seite einrichten ergänzt: Etiketten (508x254).rpt, Etiketten (Dymo 99010, 28x89).rpt, Etiketten (Dymo 99012, 36x89).rpt, Etiketten (89x36).rpt, Etiketten (254x508).rpt
* FIX: BER-FOS-FHReife (Schul Z 511)(05.06).rpt (Aufruf zweite Seite)

### Version 9.0.0 900 (04.01.2022)

Version 9 wurde veröffentlicht!

Eine Übersicht der Neuerungen finden Sie hier: [https://doc.magellan.stueber.de/changelog/neu.mag9/](https://doc.magellan.stueber.de/changelog/neu.mag9/)

Eine Umstiegsanleitung von Version 8 auf Version 9 finden Sie hier: [https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-8-auf-9/](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-8-auf-9/)
Eine Installationsanleitung finden Sie hier: [https://doc.magellan.stueber.de/schulverwaltung/installation/](https://doc.magellan.stueber.de/schulverwaltung/installation/)

## Version 8

### 8.0.15 802 (11.01.2022)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: SAC-FOS-HJZ (D01.01).rpt
* CHANGE: DSKL.DAS-ZZ (Q-Phase 11-12)(2018).rpt
* CHANGE: DSKL.DAS-JZ (3-12)(2018).rpt

#### Schnittstellen

##### SAXSVS

* FIX: Die Prüfroutine auf doppelte GUIDs beim Import von Daten wurden überarbeitet
* FIX: Prüfung für `Schüler > Daten 2> Höchster AbschlussABS > Schulform`

#### Skripte

* CHANGE: BER-FW-APO-2017.js/BER-FW-APO-2011.js: [§25 (2)]Umgesetzt wurde das Entfallen der Pflichtbelegung für die Fächer Musik, Bildende Kunst oder Darstellendes Spiel, wenn die zweite Fremdsprache erst in der Einführungsphase begonnen wurde. Die neu einsetzende FS muss dafür unter `Abitur > Fachwahlkarte > Merkmal` mit `A` gekennzeichnet werden.
