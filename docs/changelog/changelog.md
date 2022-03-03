# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle veröffentlichte und noch unveröffentlichte Änderungen in MAGELLAN. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier:

  * [2021](changelog/changelog2021.md)
  * [2020](changelog/changelog2020.md)
  * [2019](changelog/changelog2019.md)

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

### Version 9.0.2 901 (unveröffentlicht)

#### MAGELLAN Schulverwaltung

* CHANGE: ...

### Version 9.0.1 901 (03.03.2022)

!!! warning "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

* NEW: EnbreaID für die Tabellen: `Banken`, `Besonderheiten`, `BetriebeKontakte`, `KlassenBesonderheiten`, `KlassenZeitraeume`, `Medien`, `MedienKataloge`, `MedienVorgaenge`, `MedizinArten`, `MedizinKategorien`, `Noten`, `SchuelerAusbildung`, `SchuelerBesonderheiten`, `SchuelerFachdaten`, `SchuelerFehlzeiten`, `SchuelerFoerderungen`, `SchuelerSchulen`, `SchuelerSorgebe`, `SchuelerZeitraeume`, `SchuelerZeugnisbemerkungen`, `SchuelerZeugnisformulare`, `Schulen`, `Zeitraeume`
  
#### MAGELLAN Schulverwaltung

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

#### MyMAGELLAN

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

##### Berichte

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
