# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle veröffentlichte und noch unveröffentlichte Änderungen in Magellan. Änderungen im Modul MyMagellan Center werden hier veröffentlicht, Änderungen im Modul MyMagellan veröffentlichen wir im MyMagellan Handbuch unter [https://doc.mymagellan.stueber.de/changelog/](https://doc.mymagellan.stueber.de/changelog/).

Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier: [2023](https://doc.magellan.stueber.de/changelog/changelog2023/), [2022](https://doc.magellan.stueber.de/changelog/changelog2022/), [2021](https://doc.magellan.stueber.de/changelog/changelog2021/), [2020](https://doc.magellan.stueber.de/changelog/changelog2020/), [2019](https://doc.magellan.stueber.de/changelog/changelog2019/)

## Wichtige Hinweise

!!! important "Wichtig"

    **TWAIN**: Windows unterstützt seit einer Weile die Twainschnittstelle nicht mehr, stellt also von Hause aus keinen Treiber dafür zur Verfügung. Wenn der Hersteller des Gerätes (Kamera, Scanner usw.) einen passenden Treiber entsprechend der Betriebssystemausgabe und der eingesetzten Magellan Ausgabe (32 oder 64 Bit) anbietet, kann die Schnittstelle dennoch verwendet werden, alternativ könnte WIA genutzt werden. 

    **OpenSSL-Schwachstelle**: In unseren Softwareprodukten setzen wir kein OpenSSL ein.

    **Log4Shell-Schwachstelle**: Unsere Software-Produkte Enbrea, DaVinci, Magellan, CONFIRE SHOWTIME und CONFIRE SHERLOCK sind alle nicht von der Log4Shell-Schwachstelle betroffen, da keines dieser Produkte Java verwendet oder von einer externen Java-Anwendung abhängig ist. Auch unsere öffentlich zugänglichen Dienste (z.B. Ticketsystem, Webseiten) nutzen alle kein Java. Bitte lesen Sie auch unseren [Blogeintrag](https://blog.stueber.de/posts/log4j-desaster).

!!! danger "Support für Magellan 10 endet"

    Bitte beachten Sie, dass die Unterstützung für Magellan 10 am 30.06.2024 ausläuft, bitte setzen Sie stattdessen Magellan 11 ein!

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

## Version 11

### Version 11.0.8 1101 (unveröffentlicht)

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/> Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)<br/>

* NEW: `Schülerliste (für CSV-Export) Ausbildungsbetrieb und -E-Mail (Var2).rpt`
* NEW: `Schülerliste (für CSV-Export) mit Elterndaten.rpt`
* CHANGE `BER-Schul Z 523 (09.19).rpt` Notenfelder geben auch Füllwerte aus
* CHANGE: `BER-Schul Z 526 (09.19).rpt` Notenfelder zeigen Füllwerte an

### Version 11.0.7 1101 (16.07.2024)

#### Allgemein

* CHANGE: Icons, Symbole und Splashscreens

#### Magellan

* NEW: Unter `Datenbank > Optionen > Digitalquelle > WIA` können Geräte als Digitalquelle für die Aufnahme von Passfotos erfasst werden.
* NEW: Unter `Schüler > Daten1 > Rechtsklick auf Passfoto > Passfoto von Web-Kamera` können Sie auf eine Web-Kamera zugreifen oder auf in Ihrem Notebook integrierte Kamera. Bitte lesen Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/howto/schueler/#passfoto) die erweiterte Anleitung!
* FIX: Problem bei der Anzeige der Fachwahl und dem Öffnen von Verzeichnislisten im Abitur-Modul behoben
* CHANGE: Neuen Schnittstelle mit der [Berliner LUSD](https://doc.ls.stueber.de/berlin/06.lusd/)

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/> Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)<br/>

* NEW: `MVP-FG-AZ (Qualifikationsphase)(A3)(2024)`
* CHANGE: `MVP-FG-AZ (Qualifikationsphase)(2024)`: Ausgabe des 1.PF, 2.PF, BSF berücksichtigt die Unterrichtsarten HF oder LK
* CHANGE: `MVP-FG-AZ (Qualifikationsphase)(A3)(2024).rpt`, `MVP-FG-AZ (Qualifikationsphase)(2024).rpt`: 
    * Summe Facharbeitsnote
    * Korrektur der Ausgabe für Fach und Thema für FA und BLL
* CHANGE: `Quittung(DIN A4).rpt` Klasse für Schülerquittung ergänzt
* CHANGE: `BER-Schul Z 320a–b (04.23).rpt` VU-Fächer werden nicht mehr ausgewiesen, stattdesen höchstens 4 Fächer mit dem Fachstatus WahlPF. Für die Ausgabe ist die Position der Fächer wichtig, auf der linken Seite erscheinen die Fächer mit ungerader Position, auf der rechten Seite die Fächer mit gerader Position.
* CHANGE: `BER-GY-AZ (Schul Z 252)(01.07).rpt` Platz für Bemerkungen optimiert

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.<br/>Sie finden alle Berechnungsskripte und die Verweise zu deren Anleitungen im [Skripteüberblick](https://doc.la.stueber.de/skriptueberblick/#schleswig-holstein)!

* FIX: `MVP-APO-FG-2019` Korrektur: § 12(4) ....und die zweite Naturwissenschaft durch Informatik ersetzt werden.

### Version 11.0.6 1101 (01.07.2024)

#### Magellan Administrator

* FIX: Problem beim Synchronsieren der Zugriffsrechte bei gelöschten Benutzern behoben
* FIX: Problem beim gesammelten Erzeugen von Passworten gelöst

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.<br/>Sie finden alle Berechnungsskripte und die Verweise zu deren Anleitungen im [Skripteüberblick](https://doc.la.stueber.de/skriptueberblick/#schleswig-holstein)!

* FIX: `SHL-APO-2020.dws`
    * Nur 3* Sport, wenn es nicht Prüfungsfach ist
    * 4 Kurse aus einer Naturwissenschaft
    * Optimierung beim Vorschlag
* NEW: `MVP-APO-FG-2019` Diese Datei ersetzt das Skript `MVP-APO-FG-2017` und bildet neu den Umgang mit Facharbeit (als Kursleistung in BlockI) und BLL in BlockII als mdl. Prüfung ab. Die Anleitung finden Sie [hier](https://doc.la.stueber.de/06.mvp/mvp-apo-fg-2019/)!

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/> Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)<br/>

* CHANGE: `SHL-GY-ABI (2020)` Nummerierung der Prüfungsfächer auf Seite 3 ausgeschrieben
* CHANGE: `MVP-FG-AZ (Qualifikationsphase)(2024).rpt` Ausgabe Berufliches Schwerpunktfach und Leistungskurs

### Version 11.0.5 1101 (20.06.2024)

#### Magellan

* FIX: Eintrag `Klasse > Klassenart` wird korrekt übernommen in `Auswahlliste Schüler > Klassenart`
* FIX: `Bewerber > Suche`
* NEW: erste Version der neuen Schnittstelle mit der [Berliner LUSD](https://doc.ls.stueber.de/berlin/06.lusd/)

#### Magellan Administrator

* NEW: Die Import der `*.keys` ist für den Import der Verzeichnisse `Muttersprachen` und `Staatsangehörigkeiten` für Berliner Schulen ergänzt worden. Die Anleitung finden Sie [hier](https://doc.ls.stueber.de/berlin/06.lusd/).

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.<br/>Sie finden alle Berechnungsskripte und die Verweise zu deren Anleitungen im [Skripteüberblick](https://doc.la.stueber.de/skriptueberblick/#schleswig-holstein)!

* FIX: Skript `NRW-APO-BK-2018.dws` 
    * Rundung
    * Vorschlagsautomatik allgemein
    * Markierung Fremdsprachen
* FIX: Skript `NRW-APO-OS-2020.dws` 
    * Durchschnittsnoten aktualisiert
    * Rundung bei mdl. Prüfung besser als schriftl.Prüfung geändert
    * Berücksichtigung Facharbeit
    * Meldung wenn Praktikumsbescheinigung nicht erfasst ist, die Anleitung finden Sie [hier.](https://doc.la.stueber.de/08.nrw/nrw-apo-os-2020/#prufung-praktikumsbescheinigung)
    * Anpassungen für den Sammelvorschlag, die Anleitung finden Sie [hier.](https://doc.la.stueber.de/08.nrw/nrw-apo-os-2020/#sammelaktion-vorschlag-zuweisen)
    * Note 0 und 4.Prüfungsfach korrigiert  
    * Meldung "nicht bestanden" wird erst ab 3 nicht bestandenen SFs gezeigt
    * Pflichtkurse dürfen nicht Füllkurse sein (korrigiert für Projekt, neueinsetzende FS wenn Englisch SF ist, 4*Sport)
    * mind. die Hälfte der BLNWs muss schriftlich sein
    * verkehrte Meldung, dass eine fortgeführte FS fehlt, wenn neueinsetzende FS fehlt, korrigiert
* FIX: Skript `BER-IBA-AS-2020.dws` Berücksichtigung des Füllwerte `n.e.` für nicht erreicht

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/> Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)<br/>

* NEW: `BER-Schul Z 259 (03.23).rpt`
* NEW: `BER-Abi-8a – Mitteilung der Noten und Punkte des 4. Kurshalbjahres (VO-KA) – (05.20).rpt`
* CHANGE: `BER-Schul Z 322 (04.23).rpt` Leerzeichen bei Tutor/Tutorin und Leiter/Leiterin der Einrichtung ergänzt
* FIX: `DAS-Prüfungsbogen (Anlage 7 zu DIA-PO)(2018).rpt`
* FIX: `BER-Schul Z 320a–b (04.23).rpt` Layoutanpassungen
* FIX: `BER-Schul Z 324 (04.23).rpt` Layoutanpassungen
* FIX: `BER SchulZ 591 (03.20).rpt` Notenausgabe Berufsfeldübergreifender Unterricht korrigiert
* FIX: `DAS-HS-MSA-AS (Anlage8und9).rpt`Ausgabe der Fremdsprachen auf Seite 2
* New: `MVP-FG-AZ (Qualifikationsphase)(2024).rpt`
* New: `MVP-FG-AZ  (Vorstufe DINA4)(2024).rpt`
* NEW: `BER-Schul Z 213 – Zeugnis der Integrierten SekundarschuleGemeinschaftsschule über den mittleren Schulabschluss (05.23).rpt`
* NEW: `BER-Schul Z 104 – Zeugnis der Jahrgangsstufen 3 und 4 – (04.23).rpt`
* NEW: `BER-Schul Z 106 – Zeugnis der Jahrgangsstufen 5 und 6 – (04.23).rpt`
* NEW: `BER-Schul Z 200 (04.23).rpt`
* NEW: `NRW-OS-Qualifikationsübersicht.rpt`

#### Schnittstellen

* NEW: `SAC` Freigabe der Statistikschnittstelle für 2024 [Anleitung](https://doc.ls.stueber.de/sachsen/einstieg/)
* NEW: `NIE` Freigabe der Statistikschnittstelle für 2024 [Anleitung](https://doc.ls.stueber.de/niedersachsen/einstieg/)

### Version 11.0.4 1101 (27.03.2024)

#### Magellan

* CHANGE: `Bewerber/Schüler > Bewerber > Sammelzuweisung`: In der Auswahl des Assistenten wurden die Spalten Einschulmerkmal1-3 ergänzt
* NEW: In den Sammelzuweisungen unter `Bewerber > Bewerber > Sammelzuweisung` und `Schüler > Schüler > Sammelzuweisung` wurde für die Auswahl am unteren Rand die Schaltfläche zum Einstellen der optimalen Spaltenbreite ergänzt
* CHANGE: Unter `Schüler > Daten1 > Familie` wird für Kontakte, denen eine E-Mail-Adresse hinterlegt wurde, die E-Mail-Adresse eingeblendet.

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/> Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)<br/>

* CHANGE: Schülerpersonalblatt (mit Fremdsprachenfolge).rpt: Als Zu- und Abgangsdaten für die Laufbahn werden die Zu- und Abgänge zu den Klassen unter `Schueler > Laufbahn` verwendet
* CHANGE: Schülerliste (zeitraumübergreifende Fehlzeiten).rpt: Als Zu- und Abgangsdaten für die Laufbahn werden die Zu- und Abgänge zu den Klassen unter `Schueler > Laufbahn` verwendet
* NEW: `Schülerliste (für CSV-Export) Ausbildungsbetrieb und -E-Mail`
* CHANGE: `SAR-GEMS-HJZ-JZ (Klasse 5-10).rpt`: Im Pflichtbereich kann Informatik mit ausgegeben werden
* CHANGE: `SAR-GEMS-AZ (Klasse 5-10).rpt`: Im Pflichtbereich kann Informatik mit ausgegeben werden
* NEW: `BER-Abi-18b (Meldung zur weiteren mdl Pruefung)(12.23).rpt`
* NEW: `BER-Abi-18a (Mitteilungen zu den schriftlichen und mündlichen Prüfungen)(12.23).rpt`
* CHANGE: `BER-Abi 8 (05.20).rpt` umbenannt
* NEW: `BER-Abi-5 – Mitteilung zur Abiturprüfung (VO-GO  VO-KA) (03.24).rpt`
* NEW: `Abi-1b – Übersichtsplan über die Schullaufbahn ab 2010 – 13jähriger Bildungsgang (VO-GO) (05.20)).rpt`
* NEW: `BER-Abi-3 – Angaben zur Abiturprüfung (VO GO)(05.20).rpt`

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.<br/>Sie finden alle Berechnungsskripte und die Verweise zu deren Anleitungen im [Skripteüberblick](https://doc.la.stueber.de/skriptueberblick/#schleswig-holstein)!

* FIX: Skript `NRW-APO-BK-2018.dws` neu einsetzende Fremdsprache, Korrektur zu optimalen Punktzahl, [Download hier!](https://my.hidrive.com/lnk/FqWnMJhAY)

#### MyMagellan

* FIX: Die Sortierung in der Ansicht "Kontrolle nach Klassen" wurde korrigiert.

### Version 11.0.3 1101 (05.03.2024)

!!! danger "Wichtig"

     Die Datenstruktur wird angepasst. Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner. Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte synchronisieren Sie im Anschluss die Zugriffsrechte. Eine genaue Anleitung finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

#### Datenstrukturänderung

* FIX: Trigger in `SchuelerABIDetails` für die Felder `HJ1_Bestanden_Eingebracht`-`HJ6_Bestanden_Eingebracht`

#### Magellan

* CHANGE: Sammelzuweisung Schüler/Bewerber:  Bei der Auswahl der Datensätze wurden folgende Spalten ergänzt: `Rel.Teilnahme`, `Staatsangeh1`
* FIX: Problem im Skript `Schüler korrigieren` behoben (`Schüler korrigieren` nach `Schüler wechseln` in die Ausgangsklasse, Schüler wird nicht angezeigt)
* FIX: Anzeige von Fachtafeln mit voller Kürzellänge unter `Klassen > Zeiträume > Fachtafel` ermöglicht
* FIX: Export/Import SAXSVS mit Lizenz Landesstatistik 2023 ermöglicht
* NEW: `Extras > Import > Schnittstelle SchülerOnline` mit der Bundeslandeinstellung Niedersachsen ermöglicht [Abgleich SchülerOnline](https://doc.magellan.stueber.de/schulverwaltung/regionales/nrw/schueleronline/?h=sch%C3%BCler)

#### MyMagellan

* FIX: Wenn noch keine Zeugnisbemerkung für einen Schüler angelegt wurde, ist das Editiersymbol (Stift) deaktiviert. [Vorabdownload](https://my.hidrive.com/lnk/DpREtWUH)

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* FIX: `NRW-BKO-ABI.rpt` Filterung der Abiturzeugnisbemerkungen nach dem ausgewählten Halbjahr
* FIX: `DAS-ZZ (Q-Phase)(Anlage 1)(RiLi 1.6)(ab 2020).rpt` (Anzeige des Faches Landessprache unter "2.Fächer auf grundlegendem Anforderungsniveau" korrigiert)
* FIX: `BER-Schul Z 300 (03.23).rpt` (Zeilenzahl der Bemerkung erhöht)
* CHANGE: `Schul Z 500 (09.19).rpt` (für Wiederholer ist die Ausgabe des Schulhalbjahres 7 und 8 für den Einstieg im Frühjahr oder Herbst möglich)
* FIX: `BER-Schul Z 250 (03.23).rpt`:
    * Klammer im Namen entfernt
    * Tendenznotenkürzel werden um + und - gekürzt
    * Füllwerte werden ausgegeben
* FIX: `Schülerliste (mit Sorgeberechtigten).rpt` Korrektur für gewechselte Schüler
* NEW: `Sorgeberechtigte (mit SchuelerID)`
* NEW: `SHL-GY-FHReife (2020).rpt`
* NEW: `SHL-GY-AZ (A4)(2020).rpt`
* NEW: `SHL-GY-ABI (2020).rpt`
* CHANGE: `SAR-GY-ABI (GOS2.0).rpt` Platzhalter für Logodateien ergänzt, bitte beachten Sie unsere [Anleitung](https://doc.la.stueber.de/berichte/zeugnisse/sar/SAR-GY-ABI%20%28GOS2.0%29/)!
* FIX: `Schülerpersonalblatt (A5 - Laufbahn).rpt` Korrektur Bildungsgang

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.<br/>Sie finden alle Berechnungsskripte und die Verweise zu deren Anleitungen im [Skripteüberblick](https://doc.la.stueber.de/skriptueberblick/#schleswig-holstein)!

* CHANGE: SQLUpdate-Skripte aus Version 10 ergänzt, damit kann ausgehend von einer beliebigen Ausgabe von Magellan 10 der Umstieg erfolgen.
* FIX: Skript `NRW-APO-BK-2018.dws` fehlerhafte Zulassungsberechnung (zu wenige Kurse) bei vielen Defiziten
* NEW: `SHL-APO-2020.dws`

#### Schnittstellen

* FIX: Niedersachsen, Klimp.txt: Ausgabe der Teilnahme an "Werte und Normen" korrigiert

### Version 11.0.2 1100 (22.01.2024)

Alle Neuerungen beschreiben wir [hier](https://doc.magellan.stueber.de/changelog/neu.mag11/).

#### Berichte

Berichte für Magellan 11 zum Download vorab: [hier](https://my.hidrive.com/share/w5.76kcqhe)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* NEW: `Schülerliste (Prüfungsfächer Fachwahlkarte).rpt`
* NEW: `Schülerliste (Prüfungsfächer Qualifikationskarte).rpt`

## Version 10

!!! danger "Support für Magellan 10 endet"

    Bitte beachten Sie, dass die Unterstützung für Magellan 10 am 30.06.2024 ausläuft, bitte setzen Sie stattdessen Magellan 11 ein!

#### MyMagellan

* FIX: Wenn noch keine Zeugnisbemerkung für einen Schüler angelegt wurde, ist das Editiersymbol (Stift) deaktiviert. [Download](https://my.hidrive.com/lnk/c6xEN821)

### Version 10.0.12 1003 (24.01.2024)

!!! warning "Letzte Ausgabe von Magellan 10"

    Dieses Update ist die letzte Ausgabe von Magellan 10, weitere Änderungen stellen wir ggfs. als Download zur Verfügung oder veröffentlichen sie innerhalb der nachfolgenden Ausgabe Magellan 11.

#### Magellan

* FIX: SDTF-Synchronisation: Nur Daten des eigenen Mandanten sind sichtbar.
* CHANGE: Sammelzuweisung Schüler/Bwerber:  Bei der Auswahl der Datensätze wurden folgende Spalten ergänzt: `Rel.Teilnahme`, `Staatsangeh1`

#### MyMagellan Center

* FIX: Personalnummer (nicht editierbar) wird korrekt importiert. 

#### Berichte

Berichte zum Download vorab: [hier](https://my.hidrive.com/share/l332606dzw)<br/>Anleitung zum Einfügen der Berichte: [hier](https://doc.kb.stueber.de/support/bericht_einfuegen/)<br/>Anleitungen zum Nutzen der Berichtsdateien: [hier](https://doc.la.stueber.de)

* NEW: `Schülerliste (für CSV-Export).rpt`
* NEW: `Schülerliste (für CSV-Export) ohne Kopfzeile.rpt`
* FIX: `NRW-BKO-ABI.rpt` Filterung der Abiturzeugnisbemerkungen nach dem ausgewählten Halbjahr

#### Skripte

Bieten wir vorab Skripte zum Download an (Downloadlink dann je Eintrag), beschreiben wir [hier](https://doc.kb.stueber.de/support/skript_tauschen/), wie Sie beim Austausch des Skriptes vorgehen können.

* FIX: [SAC-APO-BGY-2021.dws](https://my.hidrive.com/lnk/sjxEtA5r) (Einbringung Geschichte in der Fachrichtung Gesundheit und Sozialwesen)
