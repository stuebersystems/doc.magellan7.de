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

### 8.0.10 801 ()

#### MAGELLAN Schulverwaltung

* FIX: Problem beim Einschulen (Fachtafelhaken setzen ohne Auswahl einer Fachtafel) von Schülern behoben
* FIX: Anzeige von `Schüler > Merkmale > Bemerkungen` nach Datenübernahme aus MAGELLAN 7
* FIX: Anzeige `Bewerber > Daten3 > Fremdsprachen` auch bei Kürzeln mit 10 Zeichen
* FIX: Die Sammelzuweisung des Feldes `Schüler > Laufbahn > Abschluss > Abschlussdatum2` wurde korrigiert.
* FIX: Optimierung der Abfragen, die beim Aufruf des Schülermenüs und der einzelnen Unterkarten geladen werden
* FIX: Beim Neuanlegen eines Bewerbers wird die Liste der Vorlagen geladen
* FIX: Beim Neuanlegen eines Bewerbers werden die Schulformen unter `Daten2 > Bereits besuchte Schulen` geladen
* FIX: Anzeige der Einträge unter `Schüler > Daten1 > Familie` korrigiert
* FIX: Wechsel der Daten markiertem Klassenzeitraum (je Klassenzugehörigkeit) unter `Schüler > Laufbahn > Allgemein/Abschluss` korrigiert
* CHANGE: Beim Abändern des eigenen Passworts über die MAGELLAN-Oberfläche wird zusätzlich zu Umlauten und ß auch kein Leerzeichen mehr gespeichert, Sie erhalten eine entsprechende Meldung.

#### Schnittstellen

* CHANGE: [NRW] Für Nebenschullaufbahnen (Schüler mit IDIntern), deren Stammschullaufbahn außerhalb des Statistikzeitraumes liegt, wurde das Auslesen der Daten überarbeitet.
* NEW: [NRW] Freigabe Statistikschnittstelle zu ASDPC [Anleitung](https://doc.ls.stueber.de/nordrhein-westfalen/einstieg/)

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: BER-IBA-AS-2020.dws - Korrekturen
* FIX: NRW-APO-BK-2018.dws - Berechnung der Fachhochschulreife, die maximale Anzahl an Defiziten im GK-Bereich beträgt 4 [Vorab-Download](https://my.hidrive.com/lnk/vbSpi8cE)
* Fix: SAR-APO-2018.dws - Hinweis auf "Nichtbestehen des Abiturs" bei erfolgter mdl. Prüfung aufgrund der Abweichungsprüfung und erneutem Ausführen des Skriptes korrigiert [Vorab-Download](https://my.hidrive.com/lnk/DaypC5gW)
* FIX: SAC-APO-BGY-2017 (DUBAS).dws (Einbringung 26 GKs, Hinweis zusätzl. mdl. Prüfung)

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

##### Berlin

* FIX: BER-Schul Z 306 (04.21)(FG).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)
* FIX: BER-Schul Z 306 (04.21).rpt (Fach "Studium und Beruf" mit Aufgabenbereich "gesellschaftswiss." wird nun im Gesellschaftswissenschaftlichen Aufgabenfeld ausgegeben)

##### Saarland

* CHANGE: SAR-GY-ABI (GOS2.0).rpt (Bezeichnung der Sprachreferenz wird unter Fremdsprachen ausgelesen)

##### Sachsen

* FIX: SAC-BS-AS (A.02.05).rpt (Berechnung Durchschnittsnote)
* FIX: SAC-BS-JZ (A.02.01).rpt (Ausgabe von "---" wenn keine unentschuldigten Fehltage vorliegen)
* FIX: SAC-BS-AS (A.02.05).rpt (Berechnung Durchschnittsnote)
* FIX: SAC-BS-AZ (A.02.04).rpt (Zeugnisbemerkungen werden korrekt ausgegeben)

##### Niedersachsen

* CHANGE: NIE-GY-ABI (2021).rpt (Der Satz "Die Allgemeine Hochschulreife ist im Deutschen Qualitätsrahmen (DQR) dem Niveau 4 zugeordnet." wird standardmäßig auf dem Zeugnis unter Bemerkungen ausgegeben.

##### Deutsche Auslandsschulen

* CHANGE: DAS-ZZ (Q-Phase)(Anlage 1)(RiLi 1.6)(ab 2020).rpt (Geburtsland wird hinter Geburtsort mit ausgegeben) 
* CHANGE: DAS-ZZ (Q-Phase)(Anlage 1)(RiLi 1.6).rpt (Geburtsland wird hinter Geburtsort mit ausgegeben) 

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
* Fix: SAR-APO-2018.dws - Hinweis auf "Nichtbestehen des Abiturs" bei erfolgter mdl. Prüfung aufgrund der Abweichungsprüfung und erneutem Ausführen des Skriptes korrigiert [Vorab-Download](https://my.hidrive.com/lnk/DaypC5gW)
* FIX: SAC-APO-BGY-2017 (DUBAS).dws (Einbringung 26 GKs, Hinweis zusätzl. mdl. Prüfung)

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

##### Niedersachsen

* CHANGE: NIE-GY-ABI (2021).rpt (Der Satz "Die Allgemeine Hochschulreife ist im Deutschen Qualitätsrahmen (DQR) dem Niveau 4 zugeordnet." wird standardmäßig auf dem Zeugnis unter Bemerkungen ausgegeben.