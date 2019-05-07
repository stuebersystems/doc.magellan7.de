# Statistik Schülerdaten

Dieser Abschnitt beschreibt für Schulen in Berlin die Schülerdatenerfassung 2009/2010 aus MAGELLAN in die Dateien für den Datenaustausch des eGovernment Projekts des Senates im Schuljahr. Voraussetzung hierfür ist eine Lizenz von MAGELLAN.


Der Export kann jederzeit für das aktuelle Halbjahr auf Basis der Daten in MAGELLAN in elektronischer Form vorgenommen werden. Die Statistikdaten werden wie gefordert im Dateiformat CSV aus MAGELLAN erzeugt. Für Sie als Schule bedeutet dies: Sie müssen die folgenden CSV-Dateien je nach Schulart an den Senat übermitteln:

Art |Schulform |Dateiname
----|----------|--------
Schülerdaten|Für Allgemeinbildende Schulen|SchuelerABS_2010_xxxxx.csv
-|Für Berufsbildende Schulen|SchuelerBBS_2010_xxxxx.csv
Abiturerfassung<br/>[Anleitung](https://doc.magellan6.stueber.de/bundeslaender/berlin/abidaten.html)|Für Allgemeinbildende Schulen|Abiturerfassung_ABS_2015_xxxxx.csv
-|Für Berufsbildende Schulen|Abiturerfassung_BBS_2015_xxxxx.csv

Hierbei steht xxxxx für Ihre Schulnummer.


> #### warning::Wichtig!
>
> Die Anleitung zum Export der Abiturdaten finden Sie in der MAGELLAN-Dokumentation unter [Bundesländer > Berlin > Abiturdatenexport](https://doc.magellan6.stueber.de/bundeslaender/berlin/abidaten.html).



## Notwendige Schritte

1.	Schritt: [Statistikschlüssel aktualisieren](../magellan/schluessel-importieren.md) 
2.	Schritt: Dateneingabe
3.	Schritt: [Datenprüfung](../datenpruefung.md)
4.	Schritt: Statistikdateien erstellen

Diese Schritte werden nachfolgend ausführlich erklärt.

## Statistikschlüssel aktualisieren

Statistikämter setzen für einige Felder Wertelisten voraus, die STÜBER SYSTEMS in Form von Schlüsselverzeichnissen zur Verfügung stellt. Bitte lesen Sie dazu den Abschnitt [Schlüsselverzeichnisse importieren](schlusselverzeichnisse_importieren.md).

## Statistisch relevante Daten eingeben

Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im Anhang in einer tabellarischen Übersicht.

## Datenprüfung


Vor dem Erstellen der eigentlichen Statistikdateien sollten Sie eine Prüfung der Daten in MAGELLAN vornehmen. Diese Prüfung ist eine Plausibilitätsprüfung, dessen Regelwerk uns größtenteils vom Senat zur Prüfung Ihrer Daten zur Verfügung gestellt wird.

### Datenprüfung für Allgemeinbildende oder Berufsbildende Schulen starten

Zur Datenprüfung gehen Sie bitte wie folgt vor:
1.	Starten Sie MAGELLAN.
2.	Klicken Sie im Menü ```Extras``` auf ```Statistik```.
3.	Wählen Sie als Bundesland Berlin und als Schulart Allgemeinbildende Schule (ABS) oder Berufsbildende Schulen (BBS). Klicken Sie dann auf ```Weiter```.
4.	Wählen Sie als Art der Erstellung ```Nur Datenprüfung```. Markieren Sie die Dateien, welche Sie prüfen wollen. Unter Statistikzeiträume müssen Sie den Erhebungszeitpunkt, den aktuellen Zeitraum (1. Halbjahr 2013/2014) und die Zeiträume des Vorjahres (2. Halbjahr 2012/2013 und 1. Halbjahr 2012/2013) einstellen. Klicken Sie dann auf ```Weiter```. 
5.	Geben Sie das Erstellungsdatum an und wählen Sie den Ordner für den späteren Export der Statistikdateien aus. Klicken Sie auf ```Weiter```.
6.	Klicken Sie auf ```Start```, um die Datenprüfung zu starten.

### Datenprüfung auswerten

Die Ergebnisse der Datenprüfung werden unter Hinweise aufgelistet. Sind dort keine Hinweise enthalten, sind die Daten für die Abgabe korrekt eingegeben. Die Hinweise werden unterschieden nach Art der Datei, dem betroffenen Daten-satz, Kontroll-Nr. der Plausibilität und dem eigentlichen Meldungstext. Sie können die Hinweise gruppieren und/oder Filtern und über die Schaltfläche „Export nach Excel“ nach Excel exportieren.
Sie müssen nun die Meldungen in MAGELLAN bearbeiten und dann erneut eine Datenprüfung durchführen.

>Viele in der Prüfung abgefragte Werte werden nicht in den Statistikdateien ausgegeben, dienen aber als Voraussetzung für die Plausibilitätsprüfungen. Beispiel: Zur Prüfung von korrekten Fremdsprachen muss die Schulart angegeben sein. Wurde diese nicht oder fehlerhaft angegeben, gibt die Prüfung eine Fehlermeldung aufgrund dieser Bedingung aus.

## Statistikdaten erstellen

Zum Erstellen der Statistikdaten gehen Sie bitte wie folgt vor:
1.	Starten Sie MAGELLAN.
2.	Klicken Sie im Menü ```Extras``` auf ```Statistik```.
3.	Wählen Sie als Bundesland Berlin und als Schulart Allgemeinbildende Schule (ABS) oder Berufsbildende Schulen (BBS). Klicken Sie dann auf ```Weiter```.
4.	Wählen Sie als Art der Erstellung ```Nur Statistikdateien``` erstellen. Markieren Sie die gewünschte Statistikdatei. Unter Statistikzeiträume auswählen stellen Sie den aktuellen Zeitraum ein. Klicken Sie dann auf ```Weiter```. 
5.	Geben Sie das Erstellungsdatum an und wählen Sie den Ordner für den späteren Export der Statistikdateien aus. Klicken Sie auf ```Weiter```.
6.	Klicken Sie auf ```Start```, um die Erstellung der Statistikdatei zu starten.


## Statistikfelder mit Beschreibung


### Besonderheiten


Die Datei für Berufsbildende Schulen ist unterteilt in Teil I und Teil II. Die Zuordnung der Felder zum entsprechenden Teil finden sich in der Tabelle wieder.

Der Teil II wird nur gefüllt für 
* „Berufsschulen mit sonderpäd. Aufgaben“ – Schlüssel 30 der Klasse.Schulform ODER
* „Berufsschulen“ – Schlüssel 32 der Klasse.Schulform
* UND „Auszubildenden“ – Schlüssel 01 der Klasse.Bildungsgang


Anderenfalls werden Leerfelder in der Datei ausgegeben. Diese sehen sie in Excel als leere Felder, in einem Texteditor als Semikolon.

Feld|Wert
---|---
**Statistikfeld**|	BSN						
MAGELLAN-Feld|	Mandant > Daten1 >Schulnummer						
Anmerkung|	Bitte tragen Sie hier die Schulnummer Ihrer Schule ein	 (Für ABS und BBS)					
Typ|	P						
Teil|	Teil I						
**Statistikfeld**|	S_Nummer						
MAGELLAN-Feld|	Wird beim Export berechnet						
Anmerkung|	Schulinterne Nummer des Schülers<br/> Wird von MAGELLAN automatisch erzeugt	 <br/>Achtung: <br/>Es handelt sich aufgrund der Restriktion, dass es sich um eine max 5-stellige Zahl handeln darf hierbei nicht um die Schüler	ID aus MAGELLAN		
Typ|	P						
Teil|	Teil I						
**Statistikfeld**|	S_Name 						
MAGELLAN-Feld|	Schüler > Daten1 > Nachname						
Anmerkung|	Geben Sie hier den Vornamen des Schülers ein						
Typ|	P						
Teil|	Teil I						
**Statistikfeld**|	S_Vorname						
MAGELLAN-Feld|	Schüler > Daten1 > Vorname						
Anmerkung|	Wählen Sie hier das Geschlecht des Schülers aus						
Typ|	P						
Teil|	Teil I						
**Statistikfeld**|	S_Geschlecht						
MAGELLAN-Feld|	Schüler > Daten 1 > Geschlecht						
Anmerkung|	Geben Sie hier das Geburtsdatum des Schülers ein						
Typ|	P						
Teil|	Teil I						
**Statistikfeld**|	S_Geburtsdatum						
MAGELLAN-Feld|	Schüler > Daten 1 > Geburtsdatum						
Anmerkung|	Geben Sie hier das Geburtsdatum des Schülers ein						
Typ|	 -						
Teil|	Teil I						
**Statistikfeld**|	S_StrasseHNr						
MAGELLAN-Feld|	Schüler > Daten1 > Straße						
Anmerkung|	Geben Sie hier die Straße und Hausnummer des Schülers ein						
Typ|	-						
Teil|	Teil I						
**Statistikfeld**|	S_PLZ						
MAGELLAN-Feld|	Schüler > Daten1 > PLZ						
Anmerkung|	Geben Sie hier die Postleitzahl des Schülers ein						
Typ|	 -						
Teil|	Teil I						
**Statistikfeld**|	S_Ort						
MAGELLAN-Feld|	Schüler > Daten 1 > Ort						
Anmerkung|	Geben Sie hier den Wohnort des Schülers ein						
Typ|	 -						
Teil|	Teil I						
**Statistikfeld**|	S_NDH						
MAGELLAN-Feld|	Schüler > Daten 4 > Förderbedarf						
Anmerkung|	Geben Sie hier das Merkmal Schüler nichtdeutscher Herkunftssprache an						
Typ|	-						
Teil|	Teil I						
**Statistikfeld**|	S_Lernmittelbefreiung						
MAGELLAN-Feld|	Schüler > Statistik > Merkmal S0						
Anmerkung|	Geben Sie hier an, ob der Schüler von der Lernmittelabgabe befreit ist<br/> Wenn Sie nichts eingeben, dann trifft es für den Schüler nicht zu					
Typ|	 -						
Teil|	-						
**Statistikfeld**|	S_SaphJuel_JahrgStufe						
MAGELLAN-Feld|	Klasse > Zeitraum > Klassenstufe<br/>  Schueler > Statistik > Merkmal S2<br/>Klasse > Schulart<br/>Klasse > Zeitraum > Klassenstufe						
Anmerkung|	Für SAPH Klassen geben Sie in der Klassenstufe der Klasse die 60 an und die eigentliche Klassenstufe des Schülers im Feld Merkmal S2 der Statistikmerkmale ein	 <br/>SAPH Klassen sind Regelklassen (Klassenart)	 <br/>Für JUEL Klassen geben Sie in der Schulart die 34 an, in der Klassenstufe der Klasse jeweils die höchste Klassenstufe (3 oder 6) <br/>und die eigentliche Klassenstufe des Schülers im Feld Merkmal S2 der Statistikmerkmale ein	<br/> Nur für Grundschulen Pflicht!|			
Typ|	 -						
Teil|	 -						
**Statistikfeld**|	K_JahrgStufe						
MAGELLAN-Feld|	Klasse > Zeitraum > Klassenstufe						
Anmerkung|	Geben Sie bitte hier die Klassenstufe der Klasse ein	 Bei Jahrgangsübergreifenden Klasse hier die höchste Klassenstufe eintragen	 (nur ABS)				
Typ|	-						
Teil|	-						
**Statistikfeld**|	K_Alpha						
MAGELLAN-Feld|	Klassen > Daten > Statistikkürzel						
Anmerkung|	Tragen Sie das Statistikkürzel ein, wenn Sie eine Klasse und Schüler für die Statistik erfassen möchten	<br/>Üblicherweise trägt man hier das Kürzel der Klasse erneut ein	<br/>Wenn Sie mit Parallelklassen arbeiten, müssen Sie hier mit Buchstaben von A-Z angeben, um welche Parallelklasse es sich handelt	<br/>Beispiel: 7A, 7B, 7C, 7D etc	<br/>Aus dem Statistikkürzel wird der letzte Buchstabe ausgelesen	 Handelt es sich nicht um einen Buchstaben zwischen A-Z wird automatisch A ausgegeben	 (nur ABS)|
Typ|	-						
Teil|	Teil I						
**Statistikfeld**|	K_Schulzweig						
MAGELLAN-Feld|	Klassen > Daten > Schulform						
Anmerkung|	Geben Sie bitte hier die Schulform der Klasse ein						
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	K_Klassenart						
MAGELLAN-Feld|	Klassen > Daten > Schulart						
Anmerkung|	Die Klassenart wird aufgrund der erweiterbaren Werteliste im Feld Schulart der Klasse eingetragen						
Typ|	-						
Teil|	-						
**Statistikfeld**|	K_Integrationsmerkmal						
MAGELLAN-Feld|	Klassen > Merkmale > Merkmal S1						
Anmerkung|	Geben Sie hier Integrationsmerkmal der Klasse ein	 (nur ABS)					
Typ|	-						
Teil|	-						
**Statistikfeld**|	K_Foerderschwerpunkt						
MAGELLAN-Feld|	Klassen > Merkmale > Merkmal S2						
Anmerkung|	Geben Sie hier den Förder-schwerpunkt der Klasse ein	 (nur ABS)					
Typ|	-						
Teil|	Teil I						
**Statistikfeld**|	K_Schuelergruppe						
MAGELLAN-Feld|	Klassen > Daten > Bildungsgang						
Anmerkung|	Geben Sie hier die Zugehörigkeit des Schülers zu einer Schülergruppe ein	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Wohnsitz						
MAGELLAN-Feld|	Schüler > Daten 1 > Gemeinde						
Anmerkung|	Geben Sie im Feld „Gemeinde“, die Wohngemeinde des Schülers ein	 Diese wird auch automatisch eingetragen, wenn Sie die Felder PLZ und Wohnort eintragen	<br/>Der Statistikwert wird automatisch aus der Gemeindekennziffer berechnet	 (nur BBS)			
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Staat						
MAGELLAN-Feld|	Schüler > Daten 2 > Staatsangehörigkeiten > Staatsangeh	1					
Anmerkung|	Geben Sie hier die Staatsangehörigkeit des Schülers ein	(nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Behinderung						
MAGELLAN-Feld|	Schüler > Daten 4 > Sonstige Daten > Behinderung						
Anmerkung|	Geben Sie hier an, ob der Schüler unter einer Behinderung leidet	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Berufsklasse						
MAGELLAN-Feld|	Schüler > Ausbildung >Ausbildungsbetrieb > Beruf  <br/><br/>Schüler > Daten 1 > Ausbildungsberuf						
Anmerkung|	Geben Sie auf der Registerkarte Ausbildung einen Ausbildungsbetrieb mit dem Ausbildungsberuf ein	<br/><br/>Wählen Sie diesen Ausbildungsbetrieb unter Daten 1 als aktuellen Ausbildungsplatz aus	 (nur BBS)				
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Neuer_Beruf						
MAGELLAN-Feld|	Schüler > Ausbildung > Ausbildungsbetrieb > Beruf <br/>Schüler > Statistik > Merkmal T1						
Anmerkung|	Handelt es sich beim Ausbildungsberuf des Schülers um einen neuen Beruf, der nicht in den Schlüsseln vorhanden ist, wählen Sie bitte den Schlüssel „Neuer Beruf“ als Ausbildungsberuf und tragen den Klartext des neuen Berufes bitte im Statistikmerkmal T1 ein	 Andernfalls müssen Sie hierfür keinen Eintrag machen	 (nur BBS)				
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_AusbildungsJahr						
MAGELLAN-Feld|	Schüler > Zeugnis > Details > Ausbildungsjahr						
Anmerkung|	Geben Sie hier das aktuelle Ausbildungsjahr des Schülers ein	 Beim Fortschreiben können Sie dies jährlich automatisch erhöhen lassen, dann muss der Wert nicht mehr manuell eingetragen werden	 (nur BBS)				
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_AusbildungsOrt						
MAGELLAN-Feld|	Schüler > Ausbildung >Ausbildungsbetrieb > Betrieb  <br/>Betriebe > Daten 1 > Gemeinde						
Anmerkung|	Wählen, oder geben Sie einen neuen Betrieb beim Anlegen des Ausbildungsbetriebes eines Schülers ein	 Beim Ausbildungsbetrieb geben Sie im Feld „Gemeinde“, die Gemeinde des Ausbildungsstandortes ein	 Der Statistikwert wird automatisch daraus errechnet	 (nur BBS)			
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Schulische_Vorbildung						
MAGELLAN-Feld|	Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss						
Anmerkung|	Geben Sie hier den höchsten erreichten Schulabschluss des Schülers ein	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_AusbildungsOrt						
MAGELLAN-Feld|	Schüler > Ausbildung > Ausbildungsbetrieb > Betrieb <br/>Betriebe > Daten 1 > Gemeinde						
Anmerkung|	Wählen, oder Geben Sie einen neuen Betrieb beim Anlegen des Ausbildungsbetriebes eines Schülers ein	 Beim Ausbildungsbetrieb geben Sie im Feld „Gemeinde“, die Gemeinde des Ausbildungsstandortes ein	 Der Statistikwert wird automatisch daraus errechnet	 (nur BBS)			
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Schulische_Vorbildung						
MAGELLAN-Feld|	Schüler > Daten 2 > Höchster Abschluss ABS > Abschluss						
Anmerkung|	Geben Sie hier den höchsten erreichten Schulabschluss des Schülers ein	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Beruflische_Vorbildung						
MAGELLAN-Feld|	Schüler > Daten 2 > Höchster Abschluss BBS > Abschluss						
Anmerkung|	Geben Sie hier den höchsten erreichten beruflichen Abschluss des Schülers ein	 (nur BBS)					
Typ|	-						
Teil|	-						
**Statistikfeld**|	S_SchulAbSchlussjahr						
MAGELLAN-Feld|	Schüler > Daten 2 > Höchster Abschluss BBS > Erreicht am						
Anmerkung|	Geben Sie hier an, wann der höchste schulische Abschluss erreicht wurde	 Relevant ist ein Datum im korrekten Schuljahr	 (nur BBS) Beispiel: <br/>14	5	2009 = Schuljahr 08/09 <br/>02	8	2009 = Schuljahr 09/10
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	S_Unterrichtsstunden						
MAGELLAN-Feld|	Klassen > Merkmale > Merkmal B1						
Anmerkung|	Geben Sie hier die Anzahl der wöchentlichen Unterrichststunden der Auszubildenden ein, wenn es sich nicht um Blockunterricht handelt	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	K_Klassenbezeichnung						
MAGELLAN-Feld|	Wert wird berechnet						
Anmerkung|	Durchzählung derAusbildungsklassen im Format 001-300	 Wird beim Export automatisch von MAGELLAN berechnet	 (nur BBS)				
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	K_Blockunterricht						
MAGELLAN-Feld|	Klassen > Daten > Organisation						
Anmerkung|	Geben Sie hier die Klassenorganisation ein	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	U_Fremdsprache_Pflicht						
MAGELLAN-Feld|	Schüler > Daten 3 > Fremdsprachenfolge > 1	Fremdsprache<br/>Schüler > Daten 3 > Fremdsprachenfolge > 1	Fremdsprache > Zusatz				
Anmerkung|	Geben Sie die erste Fremdsprache ein und tragen diese unter Zusatz als „Pflichtfach“ ein	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	U_Fremdsprache_Wahlpflicht						
MAGELLAN-Feld|	Schüler > Daten 3 > Fremdsprachenfolge > 2	Fremdsprache <br/>Schüler > Daten 3 > Fremdsprachenfolge > 2	Fremdsprache > Zusatz				
Anmerkung|	Geben Sie die zweite Fremdsprache ein und tragen diese unter Zusatz als „Wahlpflichtfach“ ein	 (nur BBS)					
Typ|	-						
Teil|	Teil II						
**Statistikfeld**|	U_Fremdsprache_Fakultativ						
MAGELLAN-Feld|	Schüler > Daten 3 > Fremdsprachenfolge > 3	Fremdsprache<br/>Schüler > Daten 3 > Fremdsprachenfolge > 3	Fremdsprache > Zusatz				
Anmerkung|	Geben Sie die dritte Fremdsprache ein und tragen diese unter Zusatz als „Wahlfach (fakultative FS)“ ein	 (nur BBS)					
Typ|	-						
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
							
