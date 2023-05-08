# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle veröffentlichte und noch unveröffentlichte Änderungen in MAGELLAN. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier:

  * [2022](https://doc.magellan.stueber.de/changelog/changelog2022/)
  * [2021](https://doc.magellan.stueber.de/changelog/changelog2021/)
  * [2020](https://doc.magellan.stueber.de/changelog/changelog2020/)
  * [2019](https://doc.magellan.stueber.de/changelog/changelog2019/)

## Wichtige Hinweise

!!! danger "Achtung"

    Das Vorgehen für die Installation hat sich seit der 9.5.0 geändert.<br/>
     - **MAGELLAN** gibt es jetzt die Varianten **64-Bit und 32-Bit**.<br/> 
     - Die für den Druck benötigte **Runtime-Version von Crystal Reports** ist nicht mehr Teil des Installationspaketes, sondern wird **gesondert auf allen Clients und dem Server installiert**. 
    
    Beim Update ab der 9.5.0 müssen Sie das korrekte MAGELLAN-Paket wählen (32- oder 64 Bit) und **zusätzlich** die korrekte Crystal Reports Runtimeversion (32- oder 64 Bit) installieren. Bitte lesen Sie hierfür die aktualisierten Updateanleitung für [MAGELLAN](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung) und die [Crystal Reports Runtime](https://doc.magellan.stueber.de/schulverwaltung/update/cr-aktualisieren/)!

!!! important "Wichtig"

    **Druckproblem mit Windows 11 22H2 und Crystal Reports Runtime** behoben mit der Version MAGELLAN 9.5.0.

    **OpenSSL-Schwachstelle**: In unseren Softwareprodukten setzen wir kein OpenSSL ein.

    **Log4Shell-Schwachstelle**: Unsere Software-Produkte ENBREA, DAVINCI, MAGELLAN, CONFIRE SHOWTIME und CONFIRE SHERLOCK sind alle nicht von der Log4Shell-Schwachstelle betroffen, da keines dieser Produkte Java verwendet oder von einer externen Java-Anwendung abhängig ist. Auch unsere öffentlich zugänglichen Dienste (z.B. Ticketsystem, Webseiten) nutzen alle kein Java. Bitte lesen Sie auch unseren [Blogeintrag](https://blog.stueber.de/posts/log4j-desaster).

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

## Version 10

### Version 10.0.3 101 (unveröffentlicht)

!!! danger "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte synchronisieren Sie im Anschluss die Zugriffsrechte. Eine genaue Anleitung finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstrukturänderung

* FIX: Bewerbungsziele-Kürzel auch für verwendete Einträge änderbar
* FIX: Problem beim Löschen von Bewerbern (auch mit Herkunftsschule)

#### MAGELLAN

* FIX: Für aus dem Seriendruck (Word oder Libre Office) exportieren Dokumente, für die die Ausgabe des Schülernamens (`Datenbank > Optionen > Dokumente > Dateinamenskonventionen`) gewählt wurde, wird das geklammerte Klassenkürzel hinter dem Schülernamen ausgegeben.
* FIX: Alle Ausgaben als Datei (ott, odt) oder als PDF für den Seriendruck mit LibreOffice überarbeitet
* FIX: Anbindung an Geräte (Kamera, Scanner) mit TWAIN-Schnittstelle
* NEW: Anbindung für eine Digitalquelle zur Dokumentenverwaltung per WIA-Schnittstelle, bitte beachten Sie die geänderte Dokumentation unter: [https://doc.magellan.stueber.de/schulverwaltung/admin/preferences/#digitalquelle](https://doc.magellan.stueber.de/schulverwaltung/admin/preferences/#digitalquelle)
* FIX: Abwesenheitsgründe für pausierende Schüler können erfasst und bearbeitet werden
* FIX: `Mittelstufe > Prüfung > Excelexport` möglich
* FIX: Problem beim Löschen von Bewerbern (auch mit Herkunftsschule) behoben
* FIX: Problem der Anzeige im Menü Schüler und des Neuanlegens eines Bewerbers, bei ausgeblendeten Sorgeberechtigten-Daten (`Datenbank > Optionen > Ein- und Ausblenden > Sorgeberechtigte`) behoben
* FIX: Bewerbungsziele-Kürzel auch für verwendete Einträge änderbar

#### MAGELLAN Administrator

* FIX: Korrektur beim Einlesen von Postleitzahlverzeichnissen

#### MyMAGELLAN

* FIX: Problem beim Eingeben in Verzeichnisfelder gelöst. Vorabversion unter: [https://my.hidrive.com/lnk/2URktJZv](https://my.hidrive.com/lnk/2URktJZv)
* FIX: Wechselnde Spalten-Reihenfolge 
* FIX: Eingabe der Vornote
* FIX: Problem fehlende Spalten in der Ansicht Schüler gelöst

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)
Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md)
Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* CHANGE: `SAC-BG-ABI (E.01.06).rpt` kleine Korrektur der Fußnote
* NEW: `Kursliste (Zensurerfassung nach Lehrer gruppiert) (KL3,KL4).rpt`
* CHANGE: `Kursliste (Zensurerfassung nach Lehrer gruppiert).rpt` inaktive Schüler werden nicht mit ausgegeben
* FIX: `BER-Schul Z 500 (09.19).rpt` (Ausgabe Kurshalbjahre)
* FIX: `NRW-BK-ABI (Anlage D33b - 2018).rpt` optische Korrekturen
* FIX: `DSND.DAS-GS (Klasse 2).rpt` kleine Korrekturen
* FIX: `DSND.DAS-GS (Klasse 1).rpt` kleine Korrekturen
* FIX: `DSND.DAS-GS (Klasse 3-10).rpt` kleine Korrekturen
* FIX: `BER-Schul Z 591 (03.20).rpt` (Aufruf Seite 2)
* FIX: `BER-Schul Z 592 (03.20).rpt` (Ausgabe des Themas der Präsentationsprüfung)
* FIX: `DSND.DAS-GY-ABI (DIA) (2019).rpt`  Leerzeichen in Leerzeilen eingefüft
* FIX: `DAS-GY-ABI (DIA)(2021).rpt` Leerzeichen in Leerzeilen eingefüft
* FIX: `DSND.DAS-GY-MSA (Versetzung) (ZKA)(Anlage 11)(§23).rpt` Qualifikationsbemerkung angepasst
* FIX: `BER-Schul Z 594 (12.19).rpt`Ausgabe des 2. Praktikums korrigiert
* NEW: `BER-Schul Z 256 (03.23)`
* NEW: `BER-Schul Z 306 (03.23)`
* NEW: `BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(01.23).rpt`
* FIX: `BER-Schul Z 590 (12.19).rpt` Überlagerung der Lernfelder korrigiert Ausgabe von 4 LF anstatt 2 LF; Thema betriebliche Lernaufgabe 2. Betriebspraktikum korrigiert

#### Skripte

* FIX: NRW-APO-BK-2018.dws Vorschlagsautomatik, Einbringen weitere Kurse zur Schnittverbesserung
* FIX: BER-BBS-Matrix-2016.dws
* FIX: BER-BBS-Matrix-2007.dws

### Version 10.0.2 100 (09.03.2023)

#### MAGELLAN Administrator

* FIX: Erzeugen von Passworten

#### MAGELLAN Bibliothek

* FIX: Aufruf Bücher/Medien
* FIX: Löschen von Schülern

#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in MAGELLAN einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

* CHANGE: [Download](https://my.hidrive.com/share/l332606dzw) | BER-Abi-3 – Angaben zur Abiturprüfung (VO GO)(05.20).rpt| Ergänzung des Nebenfaches bei Referenzfach für die Präsentationsprüfung
* NEW: [Download](https://my.hidrive.com/share/l332606dzw) | BER-Schul Z 256 (11.19).rpt | [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/ber/BER-Schul%20Z%20256%20%2811.19%29/)

* CHANGE: 

### Version 10.0.1 100 (14.02.2023)

Alle Neuerungen beschreiben wir [hier](https://doc.magellan.stueber.de/changelog/neu.mag10/).

## Version 9

### Version 9.5.4 902 (15.02.2023)

Diese Ausgabe ist die letzte von MAGELLAN 9, MAGELLAN 10 wurde parallel veröffentlicht, der Support für MAGELLAN 9 läuft Ende Juni 2023 aus.

#### MAGELLAN Bibliothek

* FIX: historische Vorgänge können gelöscht werden

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* NEW: BAW-APO-BGY-2021-G9.dws [Vorabdownload](https://my.hidrive.com/lnk/0sRkNVHj) | Umsetzung der aktuellen Verordnung Landesrecht BW Inhaltsverzeichnis BGVO, Landesnorm Baden-Württemberg, Verordnung des Kultusministeriums über die Beruflichen Gymnasien (Ausbildungs- und Prüfungsordnung Berufliche Gymnasien - BGVO) vom 27. August 2021, gültig ab: 01.08.2021 (landesrecht-bw.de)
  
#### Berichte

Hilfe für die Nutzung der Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de). Wie man die zum Download angebotenen Berichte in MAGELLAN einfügt, beschreiben wir [hier](https://doc.kb.stueber.de/support/bericht_einfuegen.md).

* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `NRW-BBS-JZ-HJ-AG-AS (A07).rpt` Daten von gewechselten Zeiträumen werden nicht berücksichtigt
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `SAC-FOS-HJZ (D.01.01).rpt`, `SAC-FO-HJI (D.01.01)(Fachpraktischer Unterricht).rpt`: Fachrichtung wird aus dem Berufsfeld des Bildungsgangs ausgelesen, das dem aktuellen Ausbildungsdatensatz des Schülers zuwiesen wurde
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `BER-Schul Z 302 (11.19).rpt`: kleinere Korrekturen
* NEW: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `Schueler (Verzeichnis der Prüflinge nach Prüfungsfächern).rpt`
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `BER-Schul Z 303 (11.19).rpt` Ausgabe Datum Eintritt in der Oberstufe
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `SAC-FOS-JZ (D.01.02).rpt` Korrektur Größe Textfeld Zeugnisbemerkungen
* FIX: [Download](https://my.hidrive.com/share/3pr60tsv6j) | `SAC-FOS-AZ (D.01.03).rpt` Fachrichtung wird aus dem Berufsfeld des Bildungsgangs ausgelesen, das dem aktuellen Ausbildungsdatensatz des Schülers zuwiesen wurde, Korrektur Größe Textfeld Zeugnisbemerkungen
* FIX: Kurslisten überarbeitet
