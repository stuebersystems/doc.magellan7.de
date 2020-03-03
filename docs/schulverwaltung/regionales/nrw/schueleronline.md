# Abgleich mit SchülerOnline

MAGELLAN unterstützt das SchülerOnline-Verfahren des Kommunalen Rechenzentrums (krz) Minden-Ravensberg/Lippe in Lemgo.

|MAGELLAN unterstützt:|
|:--|
|1. den Export der aktiven Betriebe für den Import in SchülerOnline bei der aufnehmenden Schulen|
|2. den Export markierter Schüler für den Import in SchülerOnline|
|3. den Import der angemeldeten Schüler aus SchülerOnline nach MAGELLAN.|

## Bundeslandeinstellung

!!! info "Hinweis"

    Der Aufruf zum Import und Export der SchülerOnline-Daten wird nur gezeigt, wenn die Bundeslandeinstellung Ihrer MAGELLAN-Verbindung auf `Nordrhein-Westfalen` gestellt ist.

Die Einstellung wird pro MAGELLAN-Verbindung im Modul MAGELLAN ADMINISTRATOR unter `Datenbankverbindungen > Doppelklick auf Ihre Verbindung > Unterpunkt Datenbank >  Feld Region` vorgenommen. Während Sie diese Einstellung ändern, muss MAGELLAN auf Ihrem Rechner geschlossen sein. Dieser Einstellung wird in der Regel pro MAGELLAN Installation in der Optionsdatei gespeichert. Wenn Sie diese Einstellung (und auch andere) für alle oder eine Gruppe von Anwenderrechnern festlegen wollen, schauen Sie bitte diese Anleitung an:  [Die Paths-Datei](https://doc.magellan7.stueber.de/schulverwaltung/installation/die-pathsdatei/).

![Wählen Sie die Region aus!](/assets/images/regionales/nrw00.png)

## Export der Betriebe

Für den Export der Betriebe aus MAGELLAN und den Import der Daten in die aufnehmende Schule in SchülerOnline müssen Sie in folgenden Schritten vorgehen:

1. Schritt: Export der Betriebe aus MAGELLAN
2. Schritt: Import der Exportdatei in SchülerOnline

### Export der Betriebe aus MAGELLAN

Um die aktiven Betriebe aus MAGELLAN zu exportieren, müssen Sie wie folgt vorgehen:

1. Wählen Sie den Menüpunkt `Extras > Export > Export > SchülerOnline` und haken die  Option `Betriebedaten (ABS+BBS)` an.
2. Klicken Sie im Export-Assistenten auf `Weiter`.
3. Geben Sie den Pfad für eine Exportdatei an, an welche Sie die Daten exportieren wollen, den Dateinamen vergibt MAGELLAN automatisch. Die Datumseingaben sind hierbei nicht relevant.
4. Klicken Sie auf `Fertigstellen`. Die Datensätze aller aktiven Betriebe werden jetzt exportiert.

![Betriebeexport für SchülerOnline ](/assets/images/regionales/nrw01.png)

## Import der Betriebedatei nach SchülerOnline

Um die zuvor exportierte Betriebedatei in SchülerOnline zu importieren, müssen Sie in SchülerOnline wie folgt vorgehen:

1. Melden Sie sich in SchülerOnline an.
2. Wählen Sie in der Navigation die Option `Aufnehmende Schule`.
3. Wählen Sie in der Navigation den Menüpunkt `Administration > Import Betriebe`.
4. Wählen Sie das `Import-Schema MAGELLAN` aus.
5. Wählen Sie unter Auswahl `Importdatei` die zuvor aus MAGELLAN exportierte Betriebedatei über die Schaltfläche `Durchsuchen` aus und laden Sie dies über `Upload`.
6. Klicken Sie zum Import jetzt auf `Import der Daten`.

## Export von Schülern

Für den Export von Schülern aus MAGELLAN und den Import der Daten in die abgebende Schule in SchülerOnline müssen Sie in folgenden Schritten vorgehen:

1. Schritt: Export von Schülern aus MAGELLAN
2. Schritt: Import der Exportdatei in SchülerOnline

### Export von Schülern aus MAGELLAN

Um die Schüler aus MAGELLAN für SchülerOnline zu exportieren, müssen Sie wie folgt vorgehen:

1. Wählen Sie den Menüpunkt `Extras > Export > Export > SchülerOnline` und haken die  Option `Schüler- und Sorgeberechtigte (ABS+BBS)` an.
2. Wählen Sie Schüler aus oder markieren alle Schüler mit STRG+A, klicken Sie anschließend auf `Weiter`.
3. Geben Sie den Pfad für eine Exportdatei an, an welche Sie die Daten exportieren wollen, den Dateinamen vergibt MAGELLAN automatisch. Die Datumseingaben sind hierbei nicht relevant.
4. Klicken Sie auf `Fertigstellen`. Die Datensätze der markierten Schüler werden jetzt exportiert.

![Schülerexport für SchülerOnline ](/assets/images/regionales/nrw02.png)

## Import der Schülerdatei nach SchülerOnline

Um die zuvor exportierte Schülerdatei in SchülerOnline zu importieren, müssen Sie in SchülerOnline wie folgt vorgehen:

1. Melden Sie sich in SchülerOnline an.
2. Wählen Sie in der Navigation die Option `Abgebende Schule`.
3. Wählen Sie in der Navigation den Menüpunkt `Datenimport > Datenimport (2013)`.
4. Wählen Sie das Import-Schema `MAGELLAN Standard` aus.
5. Wählen Sie unter Auswahl `Importdatei` die zuvor aus MAGELLAN exportierte Schülerdatei über die Schaltfläche `Durchsuchen` aus und laden Sie dies über `Upload`.
6. Klicken Sie zum Import jetzt auf `Import der Daten`.

## Import der Schüleranmeldungen aus SchülerOnline

Für den Import der Schüleranmeldungen aus SchülerOnline nach MAGELLAN müssen Sie in folgenden Schritten vorgehen:

1. Schritt: Export der Schüleranmeldungen aus SchülerOnline
2. Schritt: Prüfen der Exportdatei bzgl. der eingetragenen Schlüssel in MAGELLAN
3. Schritt: Import der Exportdatei in MAGELLAN

### Export der Schüleranmeldungen aus SchülerOnline

Um die Schüleranmeldungen aus SchülerOnline zu exportieren, müssen Sie in SchülerOnline wie folgt vorgehen:

1. Melden Sie sich in SchülerOnline an.
2. Wählen Sie in der Navigation die Option `Abgebende Schule`.
3. Wählen Sie in der Navigation den Menüpunkt `Administration > Datenexport MAGELLAN`
4. Klicken Sie in der erscheinenden Maske rechts oben auf das Symbol neben `Daten exportieren`.
5. Die Datei wird dann standardmäßig mit dem Namen `MAGELLAN_Export.csv` gespeichert.

### Prüfen der Exportdatei

Bevor Sie den eigentlich Import der zuvor erzeugten Datei `MAGELLAN-Export.csv` vornehmen, sollten Sie zunächst eine Prüfung der Daten vornehmen. Dabei wird geprüft, ob diese Schlüssel auch in den entsprechenden Schlüsselverzeichnissen von MAGELLAN enthalten sind und ob die Inhalte der Felder den maximalen Feldlängen in MAGELLAN entsprechen.

Gehen Sie dazu wie folgt vor:

1. Wählen Sie den Menüpunkt `Import > Import > SchülerOnline`.
2. Klicken Sie auf das Plus neben `Importdateien` und verweisen auf die aus SchülerOnline exportierte Datei.
3. Wählen Sie die `Art der Erstellung` (Datenprüfung) und einen Wert unter `Bildungsgang/Klasse`aus.
4. Führen Sie die Prüfung aus.

!!! info "Hinweis"

      Alle Datensätze werden jetzt geprüft, ob die enthalten Schlüsselwerte auch in MAGELLAN vorhanden sind. Existiert ein Wert in der Exportdatei, der nicht in MAGELLAN vorhanden ist bzw. der in seine Stelligkeit nicht nach MAGELLAN importiert werden kann, so wird dazu eine Hinweismeldung unter Hinweise ausgeben.
      Im Rahmen der Prüfung werden noch keine Daten importiert

Jede Hinweiszeile beinhaltet:

* die Zeilennummer der Exportdatei (Spalte Zeile),
* das Feld der Exportdatei (Spalte Feld) und
* die eigentliche Meldung (Spalte Meldung)

Diese Hinweise können Sie nach Abschluss der Prüfung über die Schaltfläche `Export der Hinweise` nach Excel zu weiteren Auswertung exportieren. Liegen keine Hinweise vor, wird im Bereich Hinweise kein Eintrag ausgegeben.

!!! info "Hinweis"

     Alle im Rahmen der Prüfung festgestellten fehlenden Schlüsselwerte in MAGELLAN werden beim späteren Import automatisch erzeugten. Die Prüfung soll Ihnen die Möglichkeit geben, unterschiedliche Schlüsselwerte in SchülerOnline und MAGELLAN für ein und denselben Sachverhalt in MAGELLAN vor dem Import anzupassen. Dies kann beispielweise leicht durch die Umbenennung von Kürzeln für Schlüsselwerte in MAGELLAN erfolgen.

### Import der Exportdatei

Um die Exportdatei aus SchülerOnline zu exportieren, gehen Sie wie folgt vor:

1. Wählen Sie den Menüpunkt `Import > Import > SchülerOnline`.
2. Klicken Sie auf das Plus neben `Importdateien` und verweisen auf die aus SchülerOnline exportierte Datei.
3. Wählen Sie die `Art der Erstellung` (Datenprüfung) und einen Wert unter `Bildungsgang/Klasse`aus.
4. Führen Sie den Import aus.

Alle Datensätze werden jetzt importiert. Werden fehlende Schlüssel in den Schlüsselverzeichnissen ergänzt, so wird dazu eine Hinweismeldung unter Hinweise ausgeben.

![Legen Sie hier die Art des Imports fest. ](/assets/images/regionales/nrw03.png)

!!! info "Hinweis"

     Beim erstmaligen Import der Betriebedaten aus der Exportdatei aus SchülerOnline prüft MAGELLAN über die Felder Name, Strasse, Postleitzahl und Ort, ob der Betrieb schon in MAGELLAN existiert, damit dieser nicht neu angelegt wird.

Ein einmalig aus SchülerOnline übernommener Betrieb ist in MAGELLAN eindeutig gekennzeichnet, damit zukünftige Betriebsdatenänderung in SchülerOnline mit nach MAGELLAN übernommen werden können.
Wird im Rahmen des Imports ein Betrieb als schon vorhanden erkannt, werden die in SchülerOnline eingetragenen Daten nicht automatisch übernommen. Schon vorhandene Betriebe werden im Anschluss an den Import in einer gesonderten Registerkarte `Betriebe aktualisieren` aufgelistet.

![Legen Sie hier in der Spalte „Aktualisieren“ fest, ob und welche Betriebe Sie aktualisieren wollen. ](/assets/images/regionales/nrw04.png)

Um eine Aktualisierung der Betriebe nun explizit durchzuführen, gehen Sie wie folgt auf der Registerkarte `Betriebe aktualisieren` vor:

1. Prüfen Sie jede der angezeigten Zeilen, welche Daten pro Betrieb dort genau geändert worden sind. Der jeweils bisherige Wert ist jeweils nachfolgende in eckigen Klammern angegeben.
2. Soll ein Betrieb nicht aktualisiert werden, dann entfernen Sie die Markierung in der Zeile für die Spalte `Aktualisieren`.
3. Nach Prüfung alle Betriebe können Sie über die Schaltfläche `Betriebe aktualisieren` die eigentliche Aktualisierung durchführen lassen.

Die Exportdatei aus SchülerOnline kann mehrfach nach MAGELLAN importiert werden. MAGELLAN erkennt beim erneuten Import, ob der Bewerber bereits importiert wurde und überschreibt dessen bisherigen Daten durch den Import.

Beim erstmaligen Import der Betriebedaten aus der Exportdatei aus SchülerOnline prüft MAGELLAN über die Felder Name, Strasse, Postleitzahl und Ort, ob der Betrieb schon in MAGELLAN existiert, damit dieser nicht neue angelegt wird.
Ein einmalig aus SchülerOnline übernommener Betrieb ist in MAGELLAN eindeutig gekennzeichnet, damit zukünftige Betriebsdatenänderung in SchülerOnline mit nach MAGELLAN übernommen werden können.
Welche Felder der Exportdatei aus SchülerOnline genau nach MAGELLAN eingelesen werden, können Sie dem nachfolgenden Abschnitt entnehmen.

### Importierte Felder

Der nachfolgende Übersicht können Sie entnehmen, in welcher Reihenfolge welche Felder der Exportdatei `MAGELLAN-Export.csv` in welche Felder in MAGELLAN übernommen werden.

!!! info "Hinweis"

      Bereits in MAGELLAN vorhandene Schüler können anhand der SchuelerID (MAGELLANID) und der Schulnummer erkannt werden. Bei Übereinstimmung wird der bestehende Schülerdatensatz als Bewerberdatensatz dupliziert und das Feld IDExtern wird gefüllt, um ein anschließendes Zusammenführen beim Einschulen zu ermöglichen. 
      Voraussetzung dafür ist, dass Sie Ihre Abgänger vorab nach SchülerOnline übergeben haben, dabei wird die MAGELLANID im Programm mit gespeichert.
      
      Das Einlesen und Prüfen der Inhalte erfolgt anhand der Position der Spalten (Beispiel: der Nachname wird als zweites erwartet), bitte verändern Sie die Anordnung nicht.
      
      Auch wichtig: einige Angaben aus SchülerOnline haben keine Entsprechung in MAGELLAN, die Spalten müssen aber dennoch in der Importdatei enthalten sein, damit die Zuordnung gelingt. 

Nr.|Feldname<br/>Magellan-Name|Verwendet <br/>in Ansicht|Schlüssel-<br/>wert
:--|:--|:--|:--
1.|**SchuelerID**<br/>Schueler.ID|Siehe Hinweis über der Tabelle|-
2.|**Nachname**<br/>Schueler.Nachname|`Bewerber > Daten 1 > Nachname`|-
3.|**Vorname**<br/>Schueler.Vorname|`Bewerber > Daten 1 > Vorname`|-
4.| **Geburtsort**<br/> Schueler.Geburtsort| `Bewerber > Daten1 > Geburtsort`| Nein
5.|**Geburtsdatum**<br/>Schueler.Geburtsdatum|`Bewerber > Daten 1 > Geboren am`|  Nein
6.| **Strasse**<br/>Schueler.Strasse|`Bewerber > Daten 1 > Straße`| Nein
7.| **Land**<br/>Schueler.Land|`Bewerber > Daten 1 > Land`| Nein
8.| **Plz**<br/>Schueler.PLZ|`Bewerber > Daten 1 > Postleitzahl`| Nein
9.| **Wohnort**<br/> Schueler.Ort| `Bewerber > Daten 1 > Ort`| Nein
10.| **Ortsteil**<br/> Schueler.Ortsteil| `Bewerber > Daten 1 > Ortsteil`| Nein
11.| **Telefon**<br/> Schueler.Telefon| `Bewerber > Daten 1 > Telefon`| Nein
12.| **Telefon2**<br/> Schueler.Mobil| `Bewerber > Daten 1 > Mobil`| Nein
13.| **Email**<br/> Schueler.Email| Bewerber > Daten 1 > E-Mail| Nein
14.| **Geburtsname**<br/> Schueler.Geburtsname| `Bewerber > Daten 1 > Geburtsname`| Nein
15.| **Geschlecht**<br/> Schueler.Geschlecht| `Bewerber > Daten 1 > Geschlecht`| Ja
16.| **Nationalitaet**<br/> Schueler.Staatsangehörigkeit1| `Bewerber > Daten 2 > Staatsangeh. 1`| Ja
17.| **Nationalitaet2**<br/> Schueler.Staatsangehörigkeit2| `Bewerber > Daten 2 > Staatsangeh. 2`| Ja
18.| **Konfession**<br/> Schueler.Konfession| `Bewerber > Daten 1 > Konfession`| Nein
19.| **Einschulung**<br/> Schueler.Grundschuleintritt| `Bewerber > Daten 2 > Grundschuleintritt`| Nein
20.| **Migration**<br/> Migration| | Nein
21.| **ZuzugsJahr**<br/> Schueler.InDeutschlandSeit| `Bewerber > Daten 2 > In Deutschland seit`| Nein
22.| **Geburtsland**<br/> Schueler.Geburtsland| `Bewerber > Daten 1 > Geburtsland`| Ja
23.| **GeburtslandVater**<br/> Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!|     -| -
24.| **GeburtslandMutter**<br/>Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!|   -|-
25.| **Verkehrssprache**<br/> Schueler.Verkehrssprache| `Bewerber > Daten 2 > Verkehrsprache`| Ja
26.| **KeyExtern**<br/>Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!| -|- 
27.| **Ezb1_Anrede**<br/> Sorgeberechtigte.Anrede| `Sorgeberechtigte > Daten > Anrede`| Nein
28.| **Ezb1_Nachname**<br/> Sorgeberechtigte.Nachname| `Sorgeberechtigte > Daten > Name`| Nein
29.| **Ezb1_Vorname**<br/> Sorgeberechtigte.Vorname| `Sorgeberechtigte > Daten > Vorname`| Nein
30.| **Ezb1_Strasse**<br/> Sorgeberechtigte.Strasse| `Sorgeberechtigte > Daten > Straße`| Nein
31.| **Ezb1_Land**<br/> Sorgeberechtigte.Land| `Sorgeberechtigte > Daten > Land`| Nein
32.| **Ezb1_PLZ**<br/> Sorgeberechtigte.PLZ| `Sorgeberechtigte > Daten > Postleitzahl`| Nein
33.| **Ezb1_Wohnort**<br/> Sorgeberechtigte.Ort| `Sorgeberechtigte > Daten > Ort`| Nein
34.| **Ezb1_Telefon**<br/> Sorgeberechtigte.TelefonPrivat| `Sorgeberechtigte > Daten > Tel. (privat)`| Nein
35.| **Ezb1_Email**<br/> Sorgeberechtigte.Email| `Bewerber > Sorgeberechtigte > Email`| Nein
36.| **Ezb1_Art**<br/> SchuelerSorgebe.Verhaeltnis| `Bewerber > Sorgeberechtigte > Verhältnis`| Nein
37.| **Ezb2_Anrede**<br/> Sorgeberechtigte.Anrede|` Sorgeberechtigte > Daten > Anrede`| Nein
38.| **Ezb2_Nachname**<br/> Sorgeberechtigte.Nachname| `Sorgeberechtigte > Daten > Name`| Nein
39.| **Ezb2_Vorname**<br/> Sorgeberechtigte.Vorname| `Sorgeberechtigte > Daten > Vorname`| Nein
40.| **Ezb2_Strasse**<br/> Sorgeberechtigte.Strasse| `Sorgeberechtigte > Daten > Straße`| Nein
41.| **Ezb2_Land**<br/> Sorgeberechtigte.Land| `Sorgeberechtigte > Daten > Land`| Nein
42.| **Ezb2_PLZ**<br/> Sorgeberechtigte.PLZ| `Sorgeberechtigte > Daten > Postleitzahl`| Nein
43.| **Ezb2_Wohnort**<br/> Sorgeberechtigte.Ort| `Sorgeberechtigte > Daten > Ort`| Nein
44.| **Ezb2_Telefon**<br/> Sorgeberechtigte.TelefonPrivat| `Sorgeberechtigte > Daten > Tel. (privat)`| Nein
45.| **Ezb2_Email**<br/> Sorgeberechtigte.Email| `Bewerber > Sorgeberechtigte > Email`| Nein
46.| **Ezb2_Art**<br/> SchuelerSorgebe.Verhaeltnis| `Bewerber > Sorgeberechtigte > Verhältnis`| Nein
47.| **Schulnr**<br/> Schule.Schulnr| `Bewerber > Zugang > Bereits besuchte Schulen > Schule`| Nein
48.| **SchulBez**<br/> Schule.Name1| `Bewerber > Zugang > Bereits besuchte Schulen > Schule`| Ja
49.| **Schulform**<br/> SchuelerSchulen.Schulform| `Bewerber > Zugang > Bereits besuchte Schulen > Schulform`| Ja
50.| **Schulgliederung**<br/> SchuelerSchulen.Schulart| `Bewerber > Zugang > Bereits besuchte Schulen > Schulart`| Nein
51.| **AbschlussSchule**<br/> HoechsterAbschlussABS| `Bewerber > Daten 2 > HoechsterAbschlussABS<br/>Schüler > Daten 2 > HoechsterAbschlussABS`
52.| **AbschlussBeruf**<br/> HoechsterAbschlussBBS|`Bewerber > Daten 2 > HoechsterAbschlussBBS<br/>Schüler > Daten 2 > HoechsterAbschlussBBS`| Nein
53.| **Klasse**<br/> Schueler.Einschulmerkmal oder Schueler.Bewerbungsziel1| In Anhängigkeit von der Einstellung unter „1. Bildungsgang und Klasse“ evtl. unter `Bewerber > Daten 1 > Einschulmerkmal` oder `- Bewerbungsziel1`| Ja
54.| **Bildungsgang**<br/> SchuelerAusbildung.Bildungsgang<br/>Schueler.Einschulmerkmal<br/>Schueler.Bewerbungsziel1| `Bewerber > Ausbildung > Bildungsgang` <br/>In Anhängigkeit von der Einstellung unter „1. Bildungsgang und Klasse“ <br/>evtl. auch unter:<br/> `- Bewerber > Daten 1 > ` oder<br/> `- Einschulmerkmal 1 `oder<br/>` - Bewerber > Daten 1 > Bewerbungsziel 1`| Nein
55.| **Aufnahmestatus**<br/> Schueler.Bewerberstatus| Erklärung: Die verschiedenen Werte für den Aufnahmestatus werden in MAGELLAN wie folgt abgebildet:<br/><br/> - aufgenommen (Wert=1)<br/>Datensatz wird als Bewerber in MAGELLAN aufgenommen mit dem Bewerberstatus„Angenommen für Bewerbungsziel 1“<br/><br/> - Warteliste (Wert=2)<br/>Datensatz wird als Bewerber in MAGELLAN aufgenommen mit dem Bewerberstatus <br/><br/> -  abgelehnt (Wert=3)<br/> Datensatz wird als Bewerber in MAGELLAN aufgenommen mit dem Bewerberstatus „nicht angenommen“„Auf Warteliste“<br/><br/> - nicht erschienen (Wert=4)<br/> Datensatz wird als Bewerber in MAGELLAN aufgenommen mit dem Bewerberstatus „Nicht zum Gespräch/Test erschienen“<br/><br/> - abgemeldet (Wert=5)<br/> Datensatz wird als Bewerber in MAGELLAN aufgenommen mit dem Bewerberstatus „Abgemeldet“| Nein
56.| **Unterlagen**<br/> Unterlagen| `Schüler > Zugang/Abgang > bereits besuchte Schulen`| Ja
57.| **Beratung**<br/> | `Schüler > Merkmale > Bemerkung`| Nein
58.| **Notiz**<br/> Schueler.Bemerkung| `Bewerber > Merkmale > Bemerkung<br/>Bewerber > Daten 1 > Bewerbung am`| Nein
59.| **Anmeldedatum**<br/> Schueler.BewerbungAm| `Bewerber > Zugang/Abgang > Zugang am`| Nein
60.| **Aufnahmedatum**<br/> Schueler.ZugangAm| `Bewerber > Ausbildung > Ausbildung von`| Ja
61.| **Ausbildungbeginn**<br/> SchuelerAusbildung.| `Bewerber > Ausbildung > Ausbildung von`<br/>`Bewerber > Ausbildung > Ausbildung bis`| Nein
62.| **Ausbildungende**<br/> SchuelerAusbildung.| `Bewerber > Ausbildung > Ausbildung bis`| Nein
63.| **Klassenlehrer**<br/> | `Betriebe > Daten 1 > Name 1`| 
64.| **Betrieb**<br/> Betrieb.Name1<br/>Betrieb.Name2| `Betriebe > Daten 1 > Name 2`<br/>`Name 2`| Nein
65.| **BetriebStrasse**<br/> Betrieb.Strasse|`Betriebe > Daten 1 > Strasse` | Nein
66.| **BetriebLand**<br/> | `Betriebe > Daten 1 > Postleitzahl`| 
67.| **BetriebPLZ**<br/> Betrieb.PLZ| `Betriebe > Daten 1 > Ort`| Nein
68.| **BetriebOrt**<br/> Betrieb.Ort| `Betriebe > Daten 1 > Telefon`| Nein
69.| **BetriebTelefon**<br/> Betrieb.Telefon| `Betriebe > Daten 1 > Telefax`| Nein
70.| **BetriebFax**<br/> Betrieb.Fax| `Betriebe > Daten 1 > E-Mail`| Nein
71.| **BetriebEmail**<br/> Betrieb.Email| `Betriebe > Kontakte > Kontakt > Nachname`| Nein
72.| **BetriebKontakt**<br/> BetriebeKontakte.Nachname| `Betriebe > Kontakte > Kontakt > Nachname`| 
73.| **BetriebKammer**<br/> Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!| -| -
74.| **BetriebMitgliedsnummer**<br/>Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!| -| -
75.| **BetriebIdExtern**<br/>Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!| -| -
76.| **KrzBetriebeid**<br/>Keine Entsprechung in MAGELLAN,<br/>Spalte muss in der Datei aber enthalten sein!| -| -

## Wie sieht eine korrekte Kopfzeile aus

Wichtig ist, dass alle Spalten in der korrekten Reihenfolge in der Datei enthalten sind, nachstehend als Beispiel und auch zum Vergleich bei Importproblemen eine Kopfzeile:

`
"SchuelerID";"Nachname";Vorname";"Geburtsort";"Geburtsdatum";"Strasse";"Land";"Plz";"Wohnort";"Ortsteil";"Telefon";"Telefon2";"Email";"Geburtsname";"Geschlecht";"Nationalitaet";"Nationalitaet2";"Konfession";"Einschulung";"Migration";"ZuzugsJahr";"Geburtsland";"GeburtslandVater";"GeburtslandMutter";"Verkehrssprache";"KeyExtern";"Ezb1_Anrede";"Ezb1_Nachname";"Ezb1_Vorname";"Ezb1_Strasse";"Ezb1_Land";"Ezb1_PLZ";"Ezb1_Wohnort";"Ezb1_Telefon";"Ezb1_Email";"Ezb1_Art";"Ezb2_Anrede";"Ezb2_Nachname";"Ezb2_Vorname";"Ezb2_Strasse";"Ezb2_Land";"Ezb2_PLZ";"Ezb2_Wohnort";"Ezb2_Telefon";"Ezb2_Email";"Ezb2_Art";"Schulnr";"SchulBez";"Schulform";"Schulgliederung";"AbschlussSchule";"AbschlussBeruf";"Klasse";"Bildungsgang";"Aufnahmestatus";"Unterlagen";"Beratung";"Notiz";"Anmeldedatum";"Aufnahmedatum";"Ausbildungbeginn";"Ausbildungende";"Klassenlehrer";"Betrieb";"BetriebStrasse";"BetriebLand";"BetriebPLZ";"BetriebOrt";"BetriebTelefon";"BetriebFax";"BetriebEmail";"BetriebKontakt";"BetriebKammer";"BetriebMitgliedsnummer";"BetriebIdExtern";"KrzBetriebeid"

`
