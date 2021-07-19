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

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## Version 8

### 8.0.11 802 ()

#### MAGELLAN Schulverwaltung

* FIX: 

#### Schnittstellen

* CHANGE: 

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: [Sachsen] `Skripte SAC-APO-BGY-2017 (DUBAS).dws` aktualisiert. Wichtig: Das Fach Englisch muss im Schlüsselverzeichnis "Fächer" im Feld "Zeugnismerkmal" den Wert "EN" bekommen, damit das Skript das Fach Englisch korrekt erkennt.
* FIX: [Sachsen]  `SAC-APO-BGY-2021.dws` aktualisiert

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: SAC-FO-FHReife (D.01.05)(ab 2017).rpt
* CHANGE: [SAC-BG-ABI (E.01.06).rpt] 
  * Die Hinweise für die Sprachreferenz der Fremdsprachen können ggfs. mit Umbruch gezeigt werden.
  * Namensanzeige (Vorname Vorname2 Zusatz Nachname) angepasst
  * Ausgabe Fachrichtung erweitert (Erst Fachrichtung des Schülerbildungsganges, dann Fachrichtung des Klassenbildungsganges)
* CHANGE: SAC-Fremdsprachenzertifikat (F.01.05).rpt
* Fix: Zeugnis SAC-BG-AZ (E.01.05).rpt
* CHANGE: SAC-BG-AZ (E.01.05).rpt - ergänzt um Ausgabe Namen SchulleiterIn/TutorIn
* FIX: SAC-FS-AS mit FHReife (C.01.06).rpt  (Korrektur der Anzeige der Durchschnittsnote in Zahl und Wort)

## Version 7

### 7.1.31 - 720 ()

#### MAGELLAN Schulverwaltung

* FIX: Problem beim Einschulen (Fachtafelhaken setzen ohne Auswahl einer Fachtafel) von Schülern behoben

#### Schnittstellen

* FIX: [Berlin] Für die Abiturdatenstatistik wurde ein Problem beim Ausspielen der Daten behoben. Wenn Sie die Version 7.1.30 von MAGELLAN einsetzen, können Sie am Arbeitsplatz von dem aus exportiert wird die MAGELLAN.exe tauschen. [Download MAGELLAN.exe](https://my.hidrive.com/lnk/85yJiIJU)

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: BER-IBA-AS-2020.dws - Korrekturen
* CHANGE: Aktualisierte Ausgaben der Skripte [BER-IBA-AS-2020](https://doc.la.stueber.de/03.ber/ber-iba-hj-2020dws/) und [BER-IBA-AS-2020](https://doc.la.stueber.de/03.ber/ber-iba-as-2020dws/) finden Sie unter folgendem [Vorab-Download](https://my.hidrive.com/lnk/IByJi3hD).
* FIX: SAR-APO-2018.dws - Hinweis auf "Nichtbestehen des Abiturs" bei erfolgter mdl. Prüfung aufgrund der Abweichungsprüfung und erneutem Ausführen des Skriptes korrigiert [Vorab-Download](https://my.hidrive.com/lnk/DaypC5gW)
* FIX: SAC-APO-BGY-2017 (DUBAS).dws (Einbringung 26 GKs, Hinweis zusätzl. mdl. Prüfung)
* FIX: [Sachsen] `Skripte SAC-APO-BGY-2017 (DUBAS).dws` aktualisiert. Wichtig: Das Fach Englisch muss im Schlüsselverzeichnis "Fächer" im Feld "Zeugnismerkmal" den Wert "EN" bekommen, damit das Skript das Fach Englisch korrekt erkennt.
* FIX: [Sachsen]  `SAC-APO-BGY-2021.dws` aktualisiert

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: SAC-BS-JZ (A.02.01).rpt (Ausgabe von "---" wenn keine unentschuldigten Fehltage vorliegen)

##### Berlin

* FIX: BER-Schul Z 306 (04.21)(FG).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)
* FIX: BER-Schul Z 306 (04.21).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)

##### Saarland

* CHANGE: SAR-GY-ABI (GOS2.0).rpt (Bezeichnung der Sprachreferenz wird unter Fremdsprachen ausgelesen)

##### Sachsen

* FIX: SAC-BS-AZ (A.02.04).rpt (Zeugnisbemerkungen werden korrekt ausgegeben)
* CHANGE: SAC-BG-AZ (E.01.05).rpt - ergänzt um Ausgabe Namen SchulleiterIn/TutorIn

##### Niedersachsen

* CHANGE: NIE-GY-ABI (2021).rpt (Der Satz "Die Allgemeine Hochschulreife ist im Deutschen Qualitätsrahmen (DQR) dem Niveau 4 zugeordnet." wird standardmäßig auf dem Zeugnis unter Bemerkungen ausgegeben.