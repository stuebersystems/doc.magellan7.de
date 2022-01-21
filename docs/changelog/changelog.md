# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle veröffentlichte und noch unveröffentlichte Änderungen in MAGELLAN. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier: 

  * [2021](changelog2021.md)
  * [2020](changelog2020.md)
  * [2019](changelog2019.md)

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

!!! danger "Achtung"

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.


## Version 9

### Version 9.0.1 (unveröffentlicht)

#### MAGELLAN Schulverwaltung

* FIX: Wenn Sie mehrere Unfallanzeigen für einen Schüler angelegt haben und eine gezielte in der Vorschau betrachten möchten, wird die gewählte Unfallanzeige gezeigt

#### MyMAGELLAN

* FIX: Beim 'Speichern unter' wird die Datei mit `Dateiname.mymx` an der gewählten Stelle gespeichert.

#### Schnittstellen

##### SAXSVS

* FIX: Wenn unter `Schüler > Daten3 > FS1-FS4 > Erteilt` kein Wert erfasst wurde, wird es als `nicht erteilt` ausgegeben.
* FIX: Die Prüfroutine auf doppelte GUIDs beim Import von Daten wurden überarbeitet
* FIX: Prüfung für `Schüler > Daten 2> Höchster AbschlussABS > Schulform`

#### Skripte

* FIX: das Skript "Synchronisiere BBS.dws" wurde überarbeitet

##### Berichte

* FIX: DAS-GS-GY (Klasse 3-10).rpt (Ausgabe der Detailinformationen, Tabellenverknüpfungen optimiert)

### Version 9.0.0 900 (04.01.2022)

Version 9 wurde veröffentlicht!

Eine Übersicht der Neuerungen finden Sie hier: [https://doc.magellan.stueber.de/changelog/neu.mag9/](https://doc.magellan.stueber.de/changelog/neu.mag9/)

Eine Umstiegsanleitung von Version 8 auf Version 9 finden Sie hier: [https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-8-auf-9/](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-8-auf-9/)
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
