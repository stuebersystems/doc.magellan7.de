# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle veröffentlichte und noch unveröffentlichte Änderungen in MAGELLAN. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier:

  * [2023](https://doc.magellan.stueber.de/changelog/changelog2023/)
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

    **TWAIN**: Windows unterstützt seit einer Weile die Twainschnittstelle nicht mehr, stellt also von Hause aus keinen Treiber dafür zur Verfügung. Wenn der Hersteller des Gerätes (Kamera, Scanner usw.) einen passenden Treiber entsprechend der Betriebssystemausgabe und der eingesetzten MAGELLAN Ausgabe (32 oder 64 Bit) anbietet, kann die Schnittstelle dennoch verwendet werden, alternativ könnte WIA genutzt werden. 

    **OpenSSL-Schwachstelle**: In unseren Softwareprodukten setzen wir kein OpenSSL ein.

    **Log4Shell-Schwachstelle**: Unsere Software-Produkte ENBREA, DAVINCI, MAGELLAN, CONFIRE SHOWTIME und CONFIRE SHERLOCK sind alle nicht von der Log4Shell-Schwachstelle betroffen, da keines dieser Produkte Java verwendet oder von einer externen Java-Anwendung abhängig ist. Auch unsere öffentlich zugänglichen Dienste (z.B. Ticketsystem, Webseiten) nutzen alle kein Java. Bitte lesen Sie auch unseren [Blogeintrag](https://blog.stueber.de/posts/log4j-desaster).

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

## Version 11

### Version 11.0.1 1100 (unveröffentlicht)

Alle Neuerungen beschreiben wir [hier](https://doc.magellan.stueber.de/changelog/neu.mag11/).

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* NEW: `Schülerliste (Prüfungsfächer Fachwahlkarte).rpt`
* NEW: `Schülerliste (Prüfungsfächer Qualifikationskarte).rpt`

## Version 10

### Version 10.0.12 103 (unveröffentlicht)

#### MAGELLAN

* FIX: SDTF-Synchronisation: Nur Daten des eigenen Mandanten sind sichtbar.

#### MyMAGELLAN Center

* FIX: Personalnummer (nicht editierbar) wird korrekt importiert. 

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* NEW: `Schülerliste (für CSV-Export).rpt`
* NEW: `Schülerliste (für CSV-Export) ohne Kopfzeile.rpt`

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: [SAC-APO-BGY-2021.dws](https://my.hidrive.com/lnk/sjxEtA5r) (Einbringung Geschichte in der Fachrichtung Gesundheit und Sozialwesen)

