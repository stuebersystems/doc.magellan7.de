# Schülerexport für Berlin

Für das Bundesland Berlin können die in den Masken für Berlin erfassten Schüler- bzw. Bewerberdaten in CSV-Dateien exportiert werden. Hier erfahren Sie, wie Sie diese Dateien aus der Ansicht „Schüler“ bzw. der Ansicht „Bewerber“ erstellen können.

## Exportieren

Um Schülerdaten zu exportieren, gehen Sie wie folgt vor.

1. Wählen Sie die Ansicht `Schüler` und wechseln anschließend auf `Extras >  Exporte  >  Export > Schüler (Berlin)`.
2. Geben Sie im Export-Assistenten den Exportordner an und wählen `Schüler` oder `Bewerber` aus. Wählen Sie zusätzlich, ob bei Schlüsselfeldern das Kürzel oder der Schlüssel ausgegeben werden soll.
3. Starten Sie mit `Fertigstellen` den Export.

![Exportfenster](/assets/images/berlin/export01.png)

Der Export der Bewerberdaten erfolgt analog.

## Exportformat

Je nachdem, ob Schüler- oder Bewerberdaten exportiert werden, sind die Exportdateien benannt. In beiden Fällen kommen vom Format die gleichen Dateien heraus, lediglich der Dateiname ändert sich. 

Export Bewerber|Export Schüler
---|---
bewerber.export.csv|schueler.export.csv
bewerber_sorgebe.export.csv|schueler_sorgebe.export.csv
bewerber_herkunft.export.csv|schueler_herkunft.export.csv
bewerber_ausbildung.export.csv|schueler_ausbildung.export.csv

## Datei (bewerber  >  schueler).export.csv

Feld| Bemerkung
--|--
SchulNr |Schulnummer
Mandant |ID des Mandanten
Typ |Folgende Werte sind möglich:<br/><br/>Wert / Bedeutung<br/>K / Schlüsselfelder werden als Kürzel exportiert<br/> S / Schlüsselfelder werden als Schlüssel exportiert
ID |ID des Schülers
GUID| GUID des Schülers
Nachname|-  
Namenszusatz |-  
Vorname |-  
Vorname2|-  
Geschlecht | Folgende Werte sind möglich:<br/><br/> Wert / Bedeutung<br/>M / Männlich<br/> W / Weiblich
Anrede | Folgende Werte sind möglich:<br/><br/> Wert / Bedeutung<br/>Wert / Bedeutung<br/>F / Frau<br/>H / Herr<br/>FD / Frau Dr.<br/>HD / Herr Dr.<br/>FP / Frau Prof.<br/>HP / Herr Prof.<br/>FPD / Frau Prof. Dr.<br/>HPD / Herr Prof. Dr.<br/>MS / Ms.<br/>MRS / Mrs.<br/> MR / Mr.
Geburtsdatum|- 
Geburtsort |- 
Geburtsname|- 
Geburtsland|- 
Strasse |-
Adresszusatz |-
Land |-
PLZ |-
Ort |-
Ortsteil |- 
Gemeinde |- 
Stadtbezirk|-  
Telefon  |-
Mobil  |-
Email  |-
Staatsangeh1| 1. Staatsangehörigkeit des Schülers
Staatsangeh2| 2. Staatsangehörigkeit des Schülers
InDeutschlandSeit  |-
AufenthalterlaubnisBis |- 
Verkehrssprache |-
NichtDeutscherHerkunft |- 
Aussiedler  |-
Foerderschwerpunkt  |-
Beeintraechtigung |-
Schularzt  |-
Krankenkasse |-
Konfession |-
Berlinpass |-
BerlinpassBis  |-
BAFoeG  |-
BAFoeGBis |- 
LernmittelBefreit|- 
LernmittelBefreitBis |- 
TeilnahmeMittagessen |- 
Bemerkung|- 
MerkmalA1|- 
MerkmalA2 |- 
MerkmalA3 |- 
MerkmalB1 |- 
MerkmalB2 |- 
 MerkmalB3  |-
 VonABSSchuleSchulNr  |-
 VonABSSchuleKuerzel  |-
 VonABSSchuleName1  |-
 VonABSSchuleName2  |-
 VonABSSchuleStrasse  |-
 VonABSSchuleLand  |-
 VonABSSchulePLZ  |-
 VonABSSchuleOrt  |-
 VonABSAbschluss  |-
 VonABSAbschlussErreichtAm |-
 VonBBSSchuleSchulNr  |-
 VonBBSSchuleKuerzel  |-
 VonBBSSchuleName1  |-
 VonBBSSchuleName2  |-
 VonBBSSchuleStrasse  |-
 VonBBSSchuleLand  |-
 VonBBSSchulePLZ  |-
 VonBBSSchuleOrt  |-
 VonBBSAbschluss  |-
 VonBBSAbschlussErreichtAm |-
 VonBBSAustritt  |-
 VonBBSBeruf  |-
 VonBBSBerufsjahre |-
 VonBBSNotendurchschnitt  |-
 Einschulmerkmal  |-
 GanztagbetriebGebunden  |-
 GanztagbetriebOffen  |-
 RelTeilnahme  |-
 Schulbeginn  |-
 Schulbeginn  |-
 Einschulungsantrag |-
 VonGrundschuleSchulNr  |-
 VonGrundschuleKuerzel  |-
 VonGrundschuleName1  |-
 VonGrundschuleName2  |-
 VonGrundschuleStrasse  |-
 VonGrundschuleLand  |-
 VonGrundschulePLZ  |-
 VonGrundschuleOrt  |-
 KlasseKuerzel  |-
 KlasseAlpha  |-
 KlasseStufe  |Entspricht auch Jg/ Saph / Jül
 KlasseKlassenart  |Folgende Werte sind möglich:<br/><br/>Wert/Bedeutung<br/>ST/Standard<br/> GT/Ganztagsklasse<br/>OK/Oberstufe (Nur Kurse)<br/> OL/Oberstufe (Leistungs- und Grundkurse)<br/> AK/Abschlussklasse<br/>KK/Kombinationsklasse<br/>SK/Schulkindergarten
KlasseSchulart |-
 KlasseIntegration |-
 KlasseAbteilung  |-
 KlasseBildungsgang |-
 KlasseLeiter1Nachname  |-
 KlasseLeiter1Vorname  |-
 KlasseBemerkung  |-
 Wiederholer  |-
 Wiederholungsart  |-
 Ausbildung  |-
 Wahlfach1 | Entspricht auch Kurs1
 Wahlfach2 | Entspricht auch Kurs2
 Wahlfach3  |-
 Wahlfach4  |-
 Wahlfach5  |-
 Wahlfach6  |-
 Fremdsprache1  |-
 Fremdsprache1Von  |-
 Fremdsprache1Bis  |-
 Fremdsprache1Note  |-
 Fremdsprache1Abgewaehlt  |-
 Fremdsprache2  |-
 Fremdsprache2Von  |-
 Fremdsprache2Bis  |-
 Fremdsprache2Note |-
 Fremdsprache2Abgewaehlt  |-
 Fremdsprache3  |-
 Fremdsprache3Von  |-
 Fremdsprache3Bis  |-
 Fremdsprache3Note  |-
 Fremdsprache3Abgewaehlt  |-
 Fremdsprache4  |-
 Fremdsprache4Von  |-
 Fremdsprache4Bis  |-
 Fremdsprache4Note  |-
 Fremdsprache4Abgewaehlt  |-
 Latinum  |-
 Graecum  |-
 TutorVorname  |-
 TutorNachname  |-
 SchulwechselAnSchuleSchulNr  |-
 SchulwechselAnSchuleKuerzel  |-
 SchulwechselAnSchuleName1  |-
 SchulwechselAnSchuleName2  |-
 SchulwechselAnSchuleStrasse  |-
 SchulwechselAnSchuleLand  |-
 SchulwechselAnSchulePLZ  |-
 SchulwechselAnSchuleOrt  |-
 SchulwechselUebergangAm  |-
 SchulwechselInJahrgang  |-
 SchulwechselUnterlagenUebersandt  |-
 SchulwechselZeugnisAusgeben  |-
 SchulwechselFoerderbogenUebersandt  |-
 SchuelerZuletztBearbeitet  |-
 SchuelerZuletztBearbeitetVon  |-
 BewerbungStatus | Folgende Werte Sind möglich:<br/><br/> Wert/Bedeutung<br/>0/Auf Warteliste<br/> 1/für Bildungsziel 1<br/>2/Angenommen für Bildungsziel 2<br/> 3/Angenommen für Bildungsziel 3<br/>4/Nicht angenommen<br/>5/Angenommen für Bildungsziel 4<br/>6/Beratungstest<br/>7/Beratungsgespräch<br/>8/Nicht zum Gespräch/Test erschienen<br/>9/Aufnahmebescheid<br/>10/Zusage nicht zurück 
 BewerbungStatusGeaendertAm  |-
 BewerbungAm  |-
 BewerbungPunkte  |-
 BewerbungHauptfachnote  |-
 BewerbungGesamtnote  |-
 BewerbungGesamtdurchschnitt  |-
 BewerbungZiel1  |-
 BewerbungZiel2  |-
 BewerbungZiel3  |-
 BewerbungZiel4  |-
 BewerbungAnStufe  |-
 BewerbungEmpfehlung  |-
 BewerbungHaertefall  |-
 BewerbungSchulwunsch2SchulNr  |-
 BewerbungSchulwunsch2Kuerzel  |-
 BewerbungSchulwunsch2Name1  |-
 BewerbungSchulwunsch2Name2  |-
 BewerbungSchulwunsch2Strasse  |-
 BewerbungSchulwunsch2Land  |-
 BewerbungSchulwunsch2PLZ  |-
 BewerbungSchulwunsch2Ort  |-
 BewerbungSchulwunsch3SchulNr  |-
 BewerbungSchulwunsch3Kuerzel  |-
 BewerbungSchulwunsch3Name1  |-
 BewerbungSchulwunsch3Name2  |-
 BewerbungSchulwunsch3Strasse  |-
 BewerbungSchulwunsch3Land  |-
 BewerbungSchulwunsch3PLZ  |-
 BewerbungSchulwunsch3Ort  |-
 BewerbungProfilfach1Fach  |-
 BewerbungProfilfach1Gewicht  |-
 BewerbungProfilfach1Note1  |-
 BewerbungProfilfach1Note2  |-
 BewerbungProfilfach2Fach  |-
 BewerbungProfilfach2Gewicht  |-
 BewerbungProfilfach2Note1  |-
 BewerbungProfilfach2Note2  |-
 BewerbungProfilfach3Fach  |-
 BewerbungProfilfach3Gewicht  |-
 BewerbungProfilfach3Note1  |-
 BewerbungProfilfach3Note2  |-
 BewerbungProfilfach4Fach  |-
 BewerbungProfilfach4Gewicht  |-
 BewerbungProfilfach4Note1  |-
 BewerbungProfilfach4Note2  |-
 BewerbungProfilfach5Fach  |-
 BewerbungProfilfach5Gewicht  |-
BewerbungProfilfach6Fach  |-
BewerbungProfilfach6Gewicht  |-
BewerbungProfilfachSumme  |-
BewerbungGesamtdurchschnittPunkte  |-
BewerbungTestpunkte  |-
BewerbungProfilPunkte  |-
BewerbungKompetenzPunkte  |-
BewerbungPunkteRanking  |-
SchuelerJahrgang  |-

## Datei (bewerber > schueler)_sorgebe.export.csv

Feld| Bemerkung
---|---
Mandant |ID des Mandanten
ID |ID des Sorgeberechtigten
SchuelerID |ID des zugehörigen Schülers
Vorname|-
Namenszusatz|-
 Nachname|-
 Anrede |Folgende Werte sind möglich:<br/><br/>Wert /Bedeutung<br/>F /Frau<br/>H/ Herr<br/>FD/ Frau Dr.<br/>HD/ Herr Dr.<br/>FP/ Frau Prof.<br/>HP /Herr Prof.<br/>FPD/Frau Prof. Dr.<br/>HPD/ Herr Prof. Dr.<br/>FA /Familie<br/>HF /Herr und Frau<br/>MS/ Ms.<br/>MRS/ Mrs.<br/>MR /Mr.<br/>MRMS /Mr. and Ms.<br/>MRMRS /Mr. and Mrs.<br/>EH/Eheleute
 Geschlecht|-
Strasse|-
PLZ|-
Ort|-
TelefonBeruf|-
TelefonPrivat|-
Mobil|-
Email|-
Beruf|-
Typ |Folgende Werte sind möglich: <br/><br/>Wert /Bedeutung <br/>E /Erreichbar<br/>N /Nicht erreichbar<br/>V /Verstorben
Verhaeltnis |Folgende Werte sind möglich:<br/>Wert/ Bedeutung<br/>MU/ Mutter<br/>VA /Vater<br/>EL /Eltern<br/>ER /Erziehungsberechtigte(r)<br/>SO /Sorgeberechtigte(r)<br/>AN /Ansprechpartner(in)<br/>VO/ Vormund<br/>GM/ Großmutter<br/>GV/ Großvater<br/>PF/ Pflegeeltern<br/>EH/ Eheleute
Nachricht| Folgende Werte sind möglich:  <br/><br/>Wert /Bedeutung  <br/>P/ Immer benachrichtigenN /Nur im Notfall<br/>K /Keine Benachrichtigung (Nie)
SeriendruckName1|-
 SeriendruckName2|-
Position |Gibt die Sortierreihenfolge der Sorgeberechtigten an.
TelefonPrioritaet| Folgende Werte sind möglich: <br/><br/> Wert /Bedeutung<br/>P /Telefon Privat<br/>B /Telefon Beruf<br/>M /Mobil
Bemerkung|-

## Datei (bewerber  >  schueler)_herkunft.export.csv

Nr. Feld  | Bemerkung
---|---
Mandant| ID des Mandanten
SchuelerID| ID des zugehörigen Schülers
SchuleID |ID der zugehörigen Schule
SchulNr |     -
Kuerzel  |     -
Name1    |      -
Name2    |       -
Strasse   |       -
Land    |         -
PLZ     |           -
Ort      |           -
Schullaufbahn     |   -
Schulform        |     -
Schulart        |      -
SchulbesuchVon   |     -
SchulbesuchBis   |      -
LetzteKlasse      |      -
LetzteKlassenstufe|        -
Klassenleiter     |         -
Abschluss         |          -
Herkunftsart     |           -
Unterlagen       |            -

## Datei (bewerber  >  schueler)_ausbildung.export.csv

Feld| Bemerkung
--|--
Mandant |-
ID |-
SchuelerID |-
AusbildungKuerzel  |-
AusbildungName1  |-
AusbildungName2  |-
AusbildungStrasse  |-
AusbildungLand  |-
AusbildungPLZ  |-
AusbildungOrt  |-
AusbildungBeruf  |-
AusbildungBildungsgang  |-
AusbildungVon |-
AusbildungBis  |-
AusbildungDauer |-
AusbildungKontaktNachname |-
AusbildungKontaktVorname |-
AusbildungKontaktGeschlecht |-
AusbildungKontaktTelefon |-
AusbildungKontaktEmail |-
AusbildungKontaktBemerkung |-
PraxisbetriebKuerzel  |-
PraxisbetriebName1  |-
PraxisbetriebName2  |-
PraxisbetriebStrasse  |-
PraxisbetriebLand  |-
PraxisbetriebPLZ  |-
PraxisbetriebOrt  |-
PraxisbetriebVon  |-
PraxisbetriebBis  |-
PraxisbetriebDauer |-
PraxisKontaktNachname |-
PraxisKontaktVorname |-
PraxisKontaktGeschlecht |-
PraxisKontaktTelefon |-
PraxisKontaktEmail |-
PraxisKontaktBemerkung |-
AusbildungVertrag  |-
AusbildungVertragsart  |-
AusbildungVertragVorgelegtAm  |-
AusbildungVertragsnummer  |-
AusbildungBemerkung |-
