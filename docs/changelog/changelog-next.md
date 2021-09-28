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

### 8.0.13 802 ()

#### MAGELLAN Schulverwaltung

* FIX: 

#### MAGELLAN Bibliothek

* FIX: 

#### Schnittstellen

 * Change: [SHL] Schlüsselverzeichnis Unterrichtsarten
 * CHANGE: [NRW] SIM.TXT - Im Falle eines Bildungsgangwechslers wird künftig nur noch eine Datensatz als Neuzugang an neuer Schule ausgespielt, die alte Laufbahn wird in die VO-Felder eingetragen, zusätzlich müssen noch die Felder LSQual, Zeugnis, Berufsabschluss und Versetzung gefüllt sein

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: [Synchronisieren BBS.dws] Ausbildungsparameter wird gesetzt, damit die Fachliste gefüllt und übertragen werden kann

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Auslandsschulen

* FIX: DSND.DAS-GS (Klasse 3).rpt 

##### Berlin

* FIX: BER-Schul Z 520 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 526 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 503 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 501 (09.19).rpt (Ausgabe Ausbildungsberuf)

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