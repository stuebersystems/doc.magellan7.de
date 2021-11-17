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

* FIX: `Klasse > Zeitraum` löschen eines Zeitraum mit `Entf`nicht mehr möglich
* FIX: `Schüler > Daten1`Eintrag im Feld Vorname wird beim Ansichtenwechsel gespeichert
* FIX: `Schüler > Ausbildung > Ausbildungsdaten`: Tabreihenfolge korrigiert
* NEW: Für den Bewerberseriendruck wurde das neue Feld `Bewerber_ID` eingefügt
* NEW: Unter `Bewerber > Daten3` kann analog `Schueler > Daten3` eine freie Bemerkung erfasst werden.
* CHANGE: Unter `Extras > Schlüsselverzeichnisse > Bewertungsprofile` wird auf den Unterkarten `Bewertungsgruppen` und `Bewertungseinträge` am oberen Ende das `Kürzel` (statt der `Bezeichnung`) des gewählten Bewertungsprofils eingeblendet.
* FIX: [SAXSVS] Beim Anlegen einer neuen Ausbildung kann gewählt werden, ob eine neue Ausbildungs-GUID vergeben wird, je nach Auswahl wird die bisherige GUID der aktuellen Ausbildung übernommen oder eine neue GUID generiert. **Wichtig: Um die bisherige GUID beizubehalten muss die aktuelle Ausbildung markiert sein**.
* FIX: Unter `Schüler > Daten1 > Familie` wird die Mobilnummer, wenn sie als `Telefonpriorität` markiert ist, korrekt mit gelb unterlegt dargestellt.

#### MAGELLAN Schulverwaltung

* FIX: Mit der Aktion `Datenbankpflege > Code 128 generieren` wird auch das Feld `BarcodePrint` für Lehrer befüllt.
* FIX: Unter `Benutzerverwaltung > Doppelklick auf Benutzer > Unterkarte "Rechte" > Bibliothek und Lernmittelverwaltung` wird die Liste der Kataloge korrekt für die Auswahl geladen

#### MAGELLAN Bibliothek

* FIX: 

#### MYMAGELLAN

* FIX: Schlüsselverzeichnis Zeugnisbemerkungen wird in voller Länge aus MAGELLAN übergeben
* FIX: `Schüler > Ausbildung > Editieren` Tabulatorreihenfolge korrigiert
* FIX: Speichern der Eingaben auf der Karte `Zeugnisdaten` (besonderer Fall: nur eine Eingabefeld auf der Karte)) 
  
#### Schnittstellen

 * Change: [SHL] Schlüsselverzeichnis Unterrichtsarten
 * CHANGE: [NRW] SIM.TXT - Im Falle eines Bildungsgangwechslers wird künftig nur noch eine Datensatz als Neuzugang an neuer Schule ausgespielt, die alte Laufbahn wird in die VO-Felder eingetragen, zusätzlich müssen noch die Felder LSQual, Zeugnis, Berufsabschluss und Versetzung gefüllt sein
* CHANGE: [SAXSVS] `<sorgeberechtigter><as_beziehung>`: Wenn für den Schülern die Verhältnisse Eltern, Erziehungsberechtigte(r) oder Sorgeberechtigte(r) zugewiesen wurden und den Sorgeberechtigten das Geschlecht (weiblich/männlich) zugeordnet wurden, wird das Verhältnis als Mutter (20) oder Vater (10) ausgespielt. Bitte beachten Sie die geänderte Anleitung unter [https://doc.ls.stueber.de/sachsen/export_saxsvs/#sorgeberechtigte](https://doc.ls.stueber.de/sachsen/export_saxsvs/#sorgeberechtigte).

#### Skripte
  
Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de/skriptueberblick/](https://doc.la.stueber.de/skriptueberblick/)

* FIX: [Synchronisieren BBS.dws] Ausbildungsparameter wird gesetzt, damit die Fachliste gefüllt und übertragen werden kann
* FIX: DE-DIAP-2015 diverse Korrekturen Vorschlagsautomatik
* FIX: DE-DIAP-2018 diverse Korrekturen
* FIX: DE-DIAP-2018 Eibringungsverprflichtung einer Naturwissenschaft mit allen 4 Halbjahren

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: Klassenliste (Schüler und Sorgeberechtige Email).rpt
* NEW: Notfallzettel (Bemerkungsliste).rpt
* NEW: Mandant (Schüler des aktuellen Halbjahres ohne aktuelle Ausbildung)
* CHANGE: Mandant (Schüler des aktuellen Halbjahres ohne Fächer)
* CHANGE: Anwesenheitsliste für den Tag.rpt (Klassenleiter1 + 2)
* FIX: Schülerliste (Förderung).rpt

##### Auslandsschulen

* FIX: DSND.DAS-GS (Klasse 3).rpt 

##### Berlin

* FIX: BER-Schul Z 520 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 526 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 503 (09.19).rpt (Ausgabe Ausbildungsberuf)
* FIX: BER-Schul Z 501 (09.19).rpt (Ausgabe Ausbildungsberuf)

##### Saarland

* NEW: ...Berichte\Zeugnisse\Saarland\Ministerium\SAR-GY-ABI (GOS2.0) mit Parametern.rpt (über Parametereingabe kann gesteuert werden, ob es sich um ein Abiturzeugnis, Zweitschrift, Zweitausfertigung oder Zweitausfertigung (Ministerium) handelt)

![Paramterwert für Zeugnisdruck](/assets/images/changelog/8.0.13.01.png)

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