# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle veröffentlichte und noch unveröffentlichte Änderungen in Magellan. Änderungen im Modul MyMagellan Center werden hier veröffentlicht, Änderungen im Modul MyMagellan veröffentlichen wir im MyMagellan Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier:

  * [2022](https://doc.magellan.stueber.de/changelog/changelog2022/)
  * [2021](https://doc.magellan.stueber.de/changelog/changelog2021/)
  * [2020](https://doc.magellan.stueber.de/changelog/changelog2020/)
  * [2019](https://doc.magellan.stueber.de/changelog/changelog2019/)

## Wichtige Hinweise

!!! danger "Achtung"

    Das Vorgehen für die Installation hat sich seit der 9.5.0 geändert.<br/>
     - **Magellan** gibt es jetzt die Varianten **64-Bit und 32-Bit**.<br/> 
     - Die für den Druck benötigte **Runtime-Version von Crystal Reports** ist nicht mehr Teil des Installationspaketes, sondern wird **gesondert auf allen Clients und dem Server installiert**. 
    
    Beim Update ab der 9.5.0 müssen Sie das korrekte Magellan-Paket wählen (32- oder 64 Bit) und **zusätzlich** die korrekte Crystal Reports Runtimeversion (32- oder 64 Bit) installieren. Bitte lesen Sie hierfür die aktualisierten Updateanleitung für [Magellan](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung) und die [Crystal Reports Runtime](https://doc.magellan.stueber.de/schulverwaltung/update/cr-aktualisieren/)!

!!! important "Wichtig"

    **TWAIN**: Windows unterstützt seit einer Weile die Twainschnittstelle nicht mehr, stellt also von Hause aus keinen Treiber dafür zur Verfügung. Wenn der Hersteller des Gerätes (Kamera, Scanner usw.) einen passenden Treiber entsprechend der Betriebssystemausgabe und der eingesetzten Magellan Ausgabe (32 oder 64 Bit) anbietet, kann die Schnittstelle dennoch verwendet werden, alternativ könnte WIA genutzt werden. 

    **OpenSSL-Schwachstelle**: In unseren Softwareprodukten setzen wir kein OpenSSL ein.

    **Log4Shell-Schwachstelle**: Unsere Software-Produkte Enbrea, DaVinci, Magellan, CONFIRE SHOWTIME und CONFIRE SHERLOCK sind alle nicht von der Log4Shell-Schwachstelle betroffen, da keines dieser Produkte Java verwendet oder von einer externen Java-Anwendung abhängig ist. Auch unsere öffentlich zugänglichen Dienste (z.B. Ticketsystem, Webseiten) nutzen alle kein Java. Bitte lesen Sie auch unseren [Blogeintrag](https://blog.stueber.de/posts/log4j-desaster).

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

### Version 10.0.11 103 (11.12.2023)

### Installation

* FIX: Das Installationspaket enthält alle neuen Berichte.

### Version 10.0.10 103 (11.12.2023)

### Magellan Schulverwaltung

* CHANGE: Eingebbare Zeichenlänge auf 100 Zeichen für die Felder unter `Bewerber/Vagabunden/Schüler > Merkmal > MerkmalB1-MerkmalB4` und `Bewerber/Vagabunden/Schüler > Merkmal > MerkmalT1-MerkmalT4` erhöht. Anzeige in den dazugehörigen Auswahlliste angepasst.
* FIX: Problem beim Versetzen von Schülern in Mandanten behoben

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* NEW: `Kursliste (Kontrolle Fachstatus).rpt`
* NEW: `Lehrer (Tutor und Schüler aller Klassen).rpt`
* NEW: `Mahnungen (ISBN, Signatur, Barcode).rpt`
* CHANGE: `BER-Schul Z 302 (03.23).rpt` Freiwilliger Unterricht wird gefüllt mit Bemerkungen, die das Merkmal `AG` oder `freiw` haben.
* CHANGE: `BER-Schul Z 250 (03.23).rpt` Wenn im Notenkürzel für Tendenznoten ein `+` oder ein `-` angegeben ist, wird es für die Anzeige der Noten unterdrückt.
* FIX: `RLP-BG (Punktekreditkarte-2010).rpt`
* FIX: `RLP-GY-Punktekreditkarte-2012.rpt`
* FIX: `SAC-BG (Punktekreditkarte-2010).rpt`
* FIX: `SAC-BG-ABI (E.01.06).rpt`

### Version 10.0.9 103 (26.09.2023)

!!! danger "Wichtig"

     Die Datenstruktur wird angepasst. 
     * Bitte aktualisieren Sie als erstes Ihren Serverrechner. Beim anschließenden Start von Magellan wird die Datenstruktur angepasst. 
     * Synchronisieren Sie im Anschluss die Zugriffsrechte. 
     * Aktualisieren Sie anschließend alle Arbeitsplatzrechner. 
      
     Eine genaue Anleitung finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!
     Die Datenstrukturbeschreibung finden [hier](https://stuebersystems.github.io/sql.magellan.de/v10/)!

### Datenstrukturänderung

* NEW: Neue Felder in der Tabelle `SchuelerABIDetails` (`HJ1_Bestanden_Eingebracht` bis `HJ6_Bestanden_Eingebracht`)

### Installation

* FIX: fehlende Firebirdsystemdateien (VS2017 CRT Libraries) in den Magellan-Installationspaketen ergänzt

### Schnittstellen

* CHANGE: NRW => SIM.TXT  `LSQual` je nach Schulform der Herkunftsschule erfolgte die Ausgabe aus `Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss [Abschlüsse (Extern)]` oder `Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss [Abschlüsse (Extern)]`
* CHANGE: NRW => ABI.TXT die ausgelesenen Halbjahre geändert 1.und 2. HJ. des vorangegangenen Schuljahres
* FIX: NRW => ABI.TXT Ausgabe der Felder LK1, LK2, GKS und GKM für die Schulform WB ergänzt
* FIX: NRW => LEHRER.TXT 
  * Aufbau überarbeitet
  * neue Lehrer-Sollschlüssel-Verzeichnisse ([Download](https://my.hidrive.com/share/u2fb42eu4v)) zum Import in DaVinci stehen zur Verfügung. Wenn Sie die Schlüsselverzeichnisse erneut importieren (Änderungen an den Schlüsselwerten), dann geben Sie bitte beim Import in DaVinci an, dass über das Kürzel abgelichen werden soll.

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: [Importiere SDTF.dws](https://my.hidrive.com/lnk/sdRkN0sW) (Übertrag von DaVinci nach Magellan)
* CHANGE: `NRW-APO-OS-2020`: 
  * automatisches Markieren der Füllkurse
  * Optimierung der Berechnung
  * Einbau der Vorschlagsautomatik
  * Berücksichtigung von 2 Fächern mit unterschiedlichem Aufgabenbereich und gleichem Fachstatus (2 Zeilen 3PF und/oder 2 Zeilen 4PF)
  * Bitte berücksichtigen Sie die angepasste [Anleitung](https://doc.la.stueber.de/08.nrw/nrw-apo-os-2020/)).

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* CHANGE: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt: Verknüpfung zu den Ausbilderdaten korrigiert

#### Bibliothek

* CHANGE: Zum Ändern des Status eines Schülers, Lehrers oder einen Person wechseln Sie bitte auf den Reiter `Daten` und wählen dort im Menüband die Option `Status ändern`.

### Version 10.0.8 102 (16.08.2023)

### Installation

* FIX: Beim Update einer Serverinstallation, die für die Datenordner von den Standardpfaden abweichende Speicherorte gewählt wurden, werden jetzt die neuen Ablagestellen aktualsiert.

### Magellan Schulverwaltung

* FIX: Ändern des Passwortes für Benutzer mit Groß- und Kleinschreibung oder `.`, `,`, `-` oder `_` im Kürzel behoben
* FIX: Problem beim Drucken für Benutzer mit Groß- und Kleinschreibung oder `.`, `,`, `-` oder `_` im Kürzel behoben

### Magellan Administrator

* FIX: Löschen von Benutzern mit Groß- und Kleinschreibung oder `.`, `,`, `-` oder `_` im Kürzel behoben

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* CHANGE: `NRW-ABI-OS (2021).rpt`
* NEW: `Schülerpersonalblatt mit Angehörigen und Vorbildung).rpt`

### Version 10.0.7 102 (18.07.2023)

#### Magellan Schulverwaltung

* NEW: `SAC` Freigabe der Statistikschnittstelle für 2023 [Anleitung](https://doc.ls.stueber.de/sachsen/einstieg/)
* NEW: `NIE` Freigabe der Statistikschnittstelle für 2023 [Anleitung](https://doc.ls.stueber.de/niedersachsen/einstieg/)

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* NEW: `BAW-GY-JZ (Birklehof).rpt`

### Version 10.0.6 102 (13.07.2023)

#### Magellan Schulverwaltung

* NEW: `NRW` Freigabe der Statistikschnittstelle für 2023 [Anleitung](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/)
* NEW: `SHL` Freigabe der Statistikschnittstelle für 2023 [Anleitung](https://doc.ls.stueber.de/schleswig-holstein/einstieg/)

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* FIX: `Kursliste Namen.rpt` Sortierung korrigiert
* FIX: `Kursliste Namen, Endnote, Bestanden, Leistungsart.rpt` Sortierung korrigiert
* FIX: `Kursliste (Schüler-Kursart-Klasse-Lehrer).rpt` Sortierung korrigiert
* FIX: `Anwesenheitsliste (Schüler nach Fach).rpt` Sortierung korrigiert
* FIX: `Anwesenheitsliste (Schüler einer Klasse nach Fach).rpt` Sortierung korrigiert
* FIX: `Kursliste mit Namen, Endnote und Niveau.rpt` Sortierung korrigiert
* FIX: `Kursliste Namen und Endnote.rpt` Sortierung korrigiert
* FIX: `BER-Schul Z 256 (03.23).rpt`, `BER-Schul Z 255 (03.23).rpt` Die verwendeten Fachpositionen wurden vereinheitlicht, Vorlage ist `BER-Schul Z 250.rpt`, bitte beachten Sie die angepassten Dokumentation!
* FIX: `SAR-GEMS-AS (Klasse 9 mit Prüfung)(ab 2021).rpt` Schreibfehler korrigiert

### Version 10.0.5 102 (07.07.2023)

!!! danger "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte synchronisieren Sie im Anschluss die Zugriffsrechte. Eine genaue Anleitung finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstrukturänderung

* FIX: Update für Passfotos aus der Schulverwaltung in die Bibliothek

#### Magellan Skripteditor

* FIX: Fehlerkorrektur beim Ausführen von Skripten

#### MyMagellan-Center

* FIX: Die Felder auf der Unterkarte `Schüler anzeigen > Schüler auswählen > Zeugnisdaten` werden werden mit den aus Magellan übergebenen Werten aber inaktiviert dargestellt, wenn beim Erzeugen der Dateien für die Felder `sichtbar` und `nicht editierbar` gewählt wurde. Wird die Sichtbarkeit für kein Felder der Unterkarte gewählt, wird die Karte ausgeblendet.

#### Magellan Schulverwaltung

* FIX: `Abitur > Qualifikation` Filter der Skriptauswahl geändert
* FIX: Menü `Schüler` und Menü `Bewerber`: Eingebbare Feldlänge in der Oberfläche für die Felder `Geburtsort` (100 Zeichen) und `Geburtsname` (50 Zeichen) erhöht

#### Magellan Administrator

* FIX: DBAdmin-Funktionalitäten überarbeitet, bitte beachten Sie die erweitere Beschreibung unter: [https://doc.magellan.stueber.de/schulverwaltung/admin/users/#sysdba-und-dbadmin](https://doc.magellan.stueber.de/schulverwaltung/admin/users/#sysdba-und-dbadmin).
* FIX: `MyMagellan Center`: Beim Verteilen ist das Markieren einer beliebigen Menge von Klassen möglich

#### Magellan Bibliothek

* FIX: Aktualisierung der Passfotos für Schüler /Lehrkräfte/Personen

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: `Zuweisen von Zugriffsrechten.dws` Meldung nach Skriptdurchlauf korrigiert
* FIX: `Zuweisen von Bewerberstammdaten.dws`  `Schüler > Sammelzuweisung > Merkmale > D1`
* FIX: `NRW-APO-OS-2020.dws`Punktetabelle Durchschnittsnote Gesamtqualifikation
* FIX: `BER-APO-2017`Sport Referenzfach der 5. Prüfungskomponente; Einbringung Politik
* FIX: `NRW-APO-OS-2020.dws` Leistungsarten Klausur, Facharbeit und Projekt auf KL, FA und PR geändert
* FIX: `NRW-APO-OS-2020.dws` Meldungen über die erreichte Punktzahl EI geändert
* FIX. `SAC-APO-BGY-2021.dws` Anpassung für die Fachrichtung ER - Ernährungswissenschaft 

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* CHANGE: `DSND.DAS-GS (Klasse 3) ohne Unterschrift Seite 1.rpt` Formkorrekturen
* CHANGE: `DSND.DAS-GY-ABI (DIA) (2019).rpt` Formkorrekturen
* CHANGE: `NRW-ABI-OS (2021).rpt ` Ausgabe der Projekte geändert, kleinere optische Änderungen
* CAHNGE: `NRW-OS-Halbjahresinformation.rpt ` Ausgabe der Projekte geändert
* CHANGE: `BER-Schul Z 591 (03.20)Variante2.rpt` Ausgabe 3 Praktikum, Ausgabe Praktikum 2 im 2.HJ
* CHANGE: `BER-Schul Z 591 (03.20).rpt` Ausgabe 3 Praktikum, Ausgabe Praktikum 2 im 2.HJ
* CHANGE: `BER-Schul Z 590 (12.19).rpt` Ausgabe Praktikum 2 im 2.HJ
* NEW: `BER-GY-18b (Meldung zur weiteren mdl Pruefung)(22.23).rpt`
* FIX: `BER-Schul Z 593 (10.20).rpt` Verknüpfungen korrigiert für Übergangsbemerkung (SchuelerKlassen), kleinere Korrekturen
* FIX: `BER-Schul Z 256 (03.23).rpt` Ausgabe Prüfungsfachnoten "d.", Ausgaben Beiblattbemerkung, Ausgabe der Verordnungsinformationen
* FIX: `SAC-BG-ABI (E.01.06).rpt` Korrekturen bei Leerzeilen
* FIX: `BER-Schul Z 592 (03.2020).rpt` kleinere Korrekturen
* FIX: `BER-Schul Z 302 (03.23).rpt` Name 2 und Name 3 in verschiedenen Zeilen
* CHANGE: `NRW-ABI-OS (2021).rpt` Optische Anpassungen
* FIX: `BER-Schul Z 256 (03.23)` Änderung an der Ausgabe unter "IV. Teilnahme an ergänzenden Angeboten" und "V. Bemerkungen"
* FIX: `SAC-BS-JZ (A.02.01) 2spaltig.rpt` Ausgabe unentschuldigte Fehltage korrigiert
* FIX: `SAC-BS-JZ (A.02.02)(zweiseitig).rpt` Ausgabe unentschuldigte Fehltage korrigiert
* FIX: `BER-Schul Z 300 (03.23).rpt` Name 2 und Name 3 in verschiedenen Zeilen
* CHANGE: `SAC-BVJ-AS ohne HS (A.01.09).rpt` Klassenleiter und Schulleiter werden je nach hinterlegtem Geschlecht als Klassenleiter oder Klassenleiterin, Schulleiter oder Schulleiterin ausgegeben.
* FIX: `BER-Schul Z 250 (03.23).rpt` kleine optische Korrekturen
* FIX: `BER-Schul Z 500.rpt.` leere Seite ausgeblendet
* FIX: `BER-Schul Z 513 – Zeugnis der Fachhochschulreife (zweij. FOS– (4 S.) (12.19).rpt` Korrektur Endnotenberechnung
* FIX: `BER-Schul Z 303 (03.23).rpt` Kopf angepasst
* FIX: `BER-Schul Z 500 (09.19)` Zeugnisdatum ergänzt
* NEW: `BER-ABI-17 (Protokoll der 5.PK) (08.16).rpt`
* NEW: `BER-ABI-17 (Protokoll der 5.PK - DS) (09.19).rpt`
* NEW: `BER-ABI-16 (Protokoll der 5.PK - BLL) (08.16).rpt`
* NEW: `BER-ABI-11 (Protokoll der mdl. Einzelprüfung) (08.16).rpt`
* FIX: `DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23).rpt` Schreibfehler korrigiert
* FIX: `BER-Schul Z 256 (03.23).rpt` Herkunft Deutschnote allgemeiner Teil, siehe Dokumentation
* FIX: `BER-Schul Z 255 (03.23).rpt` Herkunft Deutschnote allgemeiner Teil, siehe Dokumentation

### Version 10.0.4 101 (19.05.2023)

#### MyMagellan Center

* NEW: Der Assistent zum Verteilen von Daten in die Mymx-Dateien wurde um eine Filteroption nach Unterrichtsarten erweitert. Sie können wie gewohnt alle Fachzeilen übertragen oder zwischen einer bestimmten Unterrichtsart (entsprechend Ihres Verzeichnisses aus `Magellan > Extras > Schlüsselverzeichnisse > Unterrichtsarten`) oder der Auswahl "ohne Unterrichtsart" wählen. Bitte beachten Sie die Anleitung unter [https://doc.magellan.stueber.de/mymagellancenter/verteilen/#karte-unterrichtsart-auswahlen](https://doc.magellan.stueber.de/mymagellancenter/verteilen/#karte-unterrichtsart-auswahlen).

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: `NRW-APO-BK-2018`Einbringung Fremdsprache Anfänger korrigiert

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* FIX: `DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt` (Leerzeichen Seite 1)
* NEW: `BER-Schul Z 515 (12.19).rpt`
* CHANGE: `NRW-BLNW-OS.rpt` Fächer werden nur ausgegeben, wenn in Q1-Q4 Bestanden oder in Q1-Q4 Punkte erfasst wurden
* NEW: `BER-Schul Z 256 (03.23).rpt`
* NEW: `BER-Schul Z 325 (04.23).rpt`
* NEW: `BER-Schul Z 324 (04.23).rpt`
* NEW: `BER-Schul Z 323 (04.23).rpt`
* NEW: `BER-Schul Z 322 (04.23).rpt`
* NEW: `BER-Schul Z 321 (04.23).rpt`
* NEW: `BER-Schul Z 320a–b (04.23).rpt`
* NEW: `BER-Schul Z 306 (03.23).rpt`
* NEW: `BER-Schul Z 371a (04.23).rpt`
* NEW: `BER-Schul Z 371b (04.23).rpt`
* NEW: `BER-Schul Z 250 (03.23).rpt`
* NEW: `BER-Schul Z 251 (03.23).rpt`
* NEW: `BER-Schul Z 255 (03.23).rpt`
* NEW: `BER-Schul Z 300 (03.23).rpt`
* NEW: `BER-Schul Z 301 (03.23).rpt`
* NEW: `BER-Schul Z 302 (03.23).rpt`
* NEW: `BER-Schul Z 351 (11.19)_Kolleg.rpt`
* NEW: `BER-Schul Z 351 (11.19)_Oberstufe.rpt`
* NEW: `BER-Schul Z 620 (03.23).rpt`
* CHANGE: `DAS-ZZ (Q-Phase)(Anlage 1)(RiLi 1.6)(ab 2020).rpt` Sortierung der Fächer auf erhöhten Anforderungsniveau nach Position
* CHANGE: `DSND.DAS-ZZ (Q-Phase) (Anlage 1) RiLi 1.6 (G8).rpt` Sortierung der Fächer auf erhöhten Anforderungsniveau nach Position
* CHANGE: `DSND.DAS-GS (Klasse 1).rpt` Abstände für AGs, Bemerkungen, Fehlzeiten, Versetzungsvermerk angepasst
* FIX: `DSND.DAS-GS (Klasse 3).rpt` Linien Seite 2 angepasst

#### Version 10.0.3 101 (09.05.2023)

!!! danger "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte synchronisieren Sie im Anschluss die Zugriffsrechte. Eine genaue Anleitung finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstrukturänderung

* FIX: Bewerbungsziele-Kürzel auch für verwendete Einträge änderbar
* FIX: Problem beim Löschen von Bewerbern (auch mit Herkunftsschule)

#### Magellan

* FIX: Für aus dem Seriendruck (Word oder Libre Office) exportieren Dokumente, für die die Ausgabe des Schülernamens (`Datenbank > Optionen > Dokumente > Dateinamenskonventionen`) gewählt wurde, wird das geklammerte Klassenkürzel hinter dem Schülernamen ausgegeben.
* FIX: Alle Ausgaben als Datei (ott, odt) oder als PDF für den Seriendruck mit LibreOffice überarbeitet
* FIX: Anbindung an Geräte (Kamera, Scanner) mit TWAIN-Schnittstelle
* NEW: Anbindung für eine Digitalquelle zur Dokumentenverwaltung per WIA-Schnittstelle, bitte beachten Sie die geänderte Dokumentation unter: [https://doc.magellan.stueber.de/schulverwaltung/admin/preferences/#digitalquelle](https://doc.magellan.stueber.de/schulverwaltung/admin/preferences/#digitalquelle)
* FIX: Abwesenheitsgründe für pausierende Schüler können erfasst und bearbeitet werden
* FIX: `Mittelstufe > Prüfung > Excelexport` möglich
* FIX: Problem beim Löschen von Bewerbern (auch mit Herkunftsschule) behoben
* FIX: Problem der Anzeige im Menü Schüler und des Neuanlegens eines Bewerbers, bei ausgeblendeten Sorgeberechtigten-Daten (`Datenbank > Optionen > Ein- und Ausblenden > Sorgeberechtigte`) behoben
* FIX: Bewerbungsziele-Kürzel auch für verwendete Einträge änderbar

#### Magellan Administrator

* FIX: Korrektur beim Einlesen von Postleitzahlverzeichnissen

#### MyMagellan

* FIX: Problem beim Eingeben in Verzeichnisfelder gelöst. Vorabversion unter: [https://my.hidrive.com/lnk/2URktJZv](https://my.hidrive.com/lnk/2URktJZv)
* FIX: Wechselnde Spalten-Reihenfolge 
* FIX: Eingabe der Vornote
* FIX: Problem fehlende Spalten in der Ansicht Schüler gelöst

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)
Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)
Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* CHANGE: `SAC-BG-ABI (E.01.06).rpt` kleine Korrektur der Fußnote
* NEW: `Kursliste (Zensurerfassung nach Lehrer gruppiert) (KL3,KL4).rpt`
* CHANGE: `Kursliste (Zensurerfassung nach Lehrer gruppiert).rpt` inaktive Schüler werden nicht mit ausgegeben
* FIX: `NRW-BK-ABI (Anlage D33b - 2018).rpt` optische Korrekturen
* FIX: `DSND.DAS-GY-ABI (DIA) (2019).rpt`  Leerzeichen in Leerzeilen eingefüft
* FIX: `DSND.DAS-GS (Klasse 2).rpt` kleine Korrekturen
* FIX: `DSND.DAS-GS (Klasse 1).rpt` kleine Korrekturen
* FIX: `DSND.DAS-GS (Klasse 3-10).rpt` kleine Korrekturen
* FIX: `DSND.DAS-GY-MSA (Versetzung) (ZKA)(Anlage 11)(§23).rpt` Qualifikationsbemerkung angepasst
* FIX: `DAS-GY-ABI (DIA)(2021).rpt` Leerzeichen in Leerzeilen eingefüft
* FIX: `BER-Schul Z 591 (03.20).rpt` (Aufruf Seite 2)
* FIX: `BER-Schul Z 592 (03.20).rpt` (Ausgabe des Themas der Präsentationsprüfung)
* FIX: `BER-Schul Z 594 (12.19).rpt`Ausgabe des 2. Praktikums korrigiert; Thema betriebliche Lernaufgabe
* NEW: `BER-Schul Z 256 (03.23)`
* NEW: `BER-Schul Z 306 (03.23)`
* NEW: `BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(01.23).rpt`
* NEW: `BER-Schul Z 590 (12.19).Variante2` Überlagerung der Lernfelder korrigiert Ausgabe erweitert auf 4 LF anstatt 2 LF; Thema betriebliche Lernaufgabe 2. Betriebspraktikum korrigiert
* FIX: `BER-Schul Z 500 (09.19).rpt`(Ausgabe Kurshalbjahre) und Formatierung der Entwertung bei nicht belegten Fächer zentriert
* FIX: `SAC-BS-AS (A.02.05).rpt`: Ausgabe Zusatz Hauptschulabschluss
* FIX: `SAC-BS-AS (A.02.05) 2spaltig.rpt`: Ausgabe Zusatz Hauptschulabschluss
* FIX: `BER-Schul Z 501 (09.19).rpt`: Formatierung der Entwertung bei nicht belegten Fächer und Gesamtstundenanzahl zentriert 

#### Skripte

* FIX: NRW-APO-BK-2018.dws Vorschlagsautomatik, Einbringen weitere Kurse zur Schnittverbesserung
* FIX: BER-BBS-Matrix-2016.dws
* FIX: BER-BBS-Matrix-2007.dws

### Version 10.0.2 100 (09.03.2023)

#### Magellan Administrator

* FIX: Erzeugen von Passworten

#### Magellan Bibliothek

* FIX: Aufruf Bücher/Medien
* FIX: Löschen von Schülern

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/).

* CHANGE: [Download](https://my.hidrive.com/share/l332606dzw) | BER-Abi-3 – Angaben zur Abiturprüfung (VO GO)(05.20).rpt| Ergänzung des Nebenfaches bei Referenzfach für die Präsentationsprüfung
* NEW: [Download](https://my.hidrive.com/share/l332606dzw) | BER-Schul Z 256 (11.19).rpt | [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-Schul%20Z%20256%20%2811.19%29/)

* CHANGE: 

### Version 10.0.1 100 (14.02.2023)

Alle Neuerungen beschreiben wir [hier](https://doc.magellan.stueber.de/changelog/neu.mag10/).

## Version 9

### Version 9.5.4 902 (15.02.2023)

Diese Ausgabe ist die letzte von Magellan 9, Magellan 10 wurde parallel veröffentlicht, der Support für Magellan 9 läuft Ende Juni 2023 aus.

#### Magellan Bibliothek

* FIX: historische Vorgänge können gelöscht werden

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* NEW: BAW-APO-BGY-2021-G9.dws [Vorabdownload](https://my.hidrive.com/lnk/0sRkNVHj) | Umsetzung der aktuellen Verordnung Landesrecht BW Inhaltsverzeichnis BGVO, Landesnorm Baden-Württemberg, Verordnung des Kultusministeriums über die Beruflichen Gymnasien (Ausbildungs- und Prüfungsordnung Berufliche Gymnasien - BGVO) vom 27. August 2021, gültig ab: 01.08.2021 (landesrecht-bw.de)
  
#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in Magellan einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/).

* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `NRW-BBS-JZ-HJ-AG-AS (A07).rpt` Daten von gewechselten Zeiträumen werden nicht berücksichtigt
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `SAC-FOS-HJZ (D.01.01).rpt`, `SAC-FO-HJI (D.01.01)(Fachpraktischer Unterricht).rpt`: Fachrichtung wird aus dem Berufsfeld des Bildungsgangs ausgelesen, das dem aktuellen Ausbildungsdatensatz des Schülers zuwiesen wurde
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `BER-Schul Z 302 (11.19).rpt`: kleinere Korrekturen
* NEW: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `Schueler (Verzeichnis der Prüflinge nach Prüfungsfächern).rpt`
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `BER-Schul Z 303 (11.19).rpt` Ausgabe Datum Eintritt in der Oberstufe
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `SAC-FOS-JZ (D.01.02).rpt` Korrektur Größe Textfeld Zeugnisbemerkungen
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `SAC-FOS-AZ (D.01.03).rpt` Fachrichtung wird aus dem Berufsfeld des Bildungsgangs ausgelesen, das dem aktuellen Ausbildungsdatensatz des Schülers zuwiesen wurde, Korrektur Größe Textfeld Zeugnisbemerkungen
* FIX: Kurslisten überarbeitet
