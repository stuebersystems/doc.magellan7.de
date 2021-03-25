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

    **OPAC-Anbindung der MAGELLAN Bibliothek**: Durch Änderungen der Schnittstelle durch die Deutsche Nationalbibliothek können aktuell keine Daten ausgelesen werden, die Funktion steht damit aktuell nicht zur Verfügung.
    
    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## Version 8

## Version 7

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
