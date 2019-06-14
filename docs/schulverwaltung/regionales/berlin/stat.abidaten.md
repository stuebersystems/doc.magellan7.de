# Abiturdatenexport

Dieser Abschnitt beschreibt für Schulen in Berlin den Datenexport der Abiturdatenerfassung im Jahr 2018 für die Senatsverwaltung für Bildung, Jugend und Wissenschaft (SenBJW) im Rahmen des Projekts eGovernment@School. Voraussetzung hierfür ist eine Lizenz von MAGELLAN.

## Einführung

Der Export kann jederzeit für das aktuelle Halbjahr auf Basis der Daten in MAGELLAN in elektronischer Form vorgenommen werden. Die zu exportierende Statistikdatei wird wie gefordert im Dateiformat CSV aus MAGELLAN erzeugt. Für Sie als Schule bedeutet dies: Sie müssen die je nach Schulart die folgende CSV-Datei je nach Schulart erzeugen und dann nach Anleitung des SenBJW weiterverarbeiten:

Schule|Dateiname
--|--
Für Allgemeinbildende Schulen| Abiturerfassung_ABS_2018_xxxxx.csv
Für Berufsbildende Schulen| Abiturerfassung_BBS_2018_xxxxx.csv

Hierbei steht xxxxx für Ihre Schulnummer. Die erzeugte Statistikdatei können Sie dann in die Abiturdaten-Prüfsoftware ASDPW einlesen.

## Notwendige Schritte

Folgende Schritte sind notwendig, um die Statistikdatei erfolgreich erstellen zu können.

1. Schritt: Statistikschlüssel aktualisieren 
2. Schritt: Statistisch relevante Daten in MAGELLAN eingeben
4. Schritt: Statistikdaten erstellen
5. Schritt: Sie können sich den Inhalt der Dateien mit Hilfe von einem Texteditor oder Excel anzeigen lassen.

Diese Schritte werden nachfolgend ausführlich erklärt.

## Wann wird eine Exportdatei erzeugt?

Voraussetzung für das Exportieren der Abiturerfassungsdaten sind folgende Angaben:

### Angaben bei der Klasse


 Feld|Anmerkung
 --|--
**Feldname** | **Statistikkürzel**
 Ansicht/Maske|Klassen > Daten 1 >  **Statistikkürzel**
 Bedingung|Das Feld muss gefüllt sein.
 **Feldname** | **Klassenart**
Ansicht/Maske|Klassen > Daten 1 > **Klassenart**
Bedingung|Muss einen der folgenden Werte enthalten:<br/><br/>Oberstufenjahrgang (nur Kurse) <br/>Oberstufenjahrgang (Leistungs- und Grundkurse)
**Feldname**|**Jahrgang**
Ansicht/Maske|Klassen > Zeiträume > **Jahrgang**
Bedingung|Im aktuellen Zeitraum 2. Halbjahr 2017/2018 muss das Feld den Wert 12 für G8-Abitur oder 13 für G9-Abitur haben

### Abiturjahrgang

!!! info "Hinweis"

     Es werden nur die Schüler in der Ansicht „Abitur“ exportiert, die einen Abiturjahrgang zugeordnet haben. Dieser Abiturjahrgang muss im Verzeichnis der Abschlussjahrgänge mit einem „Bis-Datum“ definiert sein, welches in 2018 liegt.

Feld|Bedingung
--|--
**Feldname**|**Abiturjahrgang**
Ansicht / Maske|Abitur > Auswahl >  Abiturjahrgang <br/> Abitur > Qualifikation >  Abiturjahrgang<br/>Abitur > Prüfung >  Abiturjahrgang <br/>Abitur > Fachwahl >  Abiturjahrgang
Bedingung|Das Feld muss mit einem Wert gefüllt sein, der im Schlüsselverzeichnis `Abschlussjahrgänge `definiert worden ist. Dieser Abschlussjahrgang muss wie nachfolgend unter dem `Feld Bis` beschrieben definiert sein.
**Feldname**|**Bis**
Ansicht / Maske|Extras > Abschlussjahrgänge > Bis
Bedingung|Das Feld muss mit einem Datum gefüllt sein, dessen Jahr = 2018 ist, z.B. 31.07.2018

### Statistikkürzel

Voraussetzung für das Ausspielen der Daten in das Statistikformat ist die Angabe des Feldes `Klassen > Daten 1 > Statistikkürzel`. Das Feld kann beliebig eingetragen werden und sollte eindeutig benannt sein. Üblicherweise wird hier einfach das Klassenkürzel wiederholt.
Das Statistikkürzel der Klasse muss eindeutig gefüllt sein, tragen Sie am besten das Klassenkürzel hier erneut ein.
Schüler, für deren Klasse kein Statistikkürzel eingetragen ist, werden statistisch nicht berücksichtigt.

## Statistikschlüssel aktualisieren

Um die aktuellen Schlüsselverzeichnisse für Berlin nach MAGELLAN zu importieren, gehen Sie wie folgt vor:

1. Starten Sie den MAGELLAN-ADMINISTRATOR.
2. Wechseln Sie in die Ansicht `Datenimporte`.
3. Klicken Sie auf `Starten` im Punkt `Schlüsselverzeichnisse importieren`.
4. Im Dialogfenster geben Sie Ihr Bundesland Berlin, Ihre Schulart und den Mandanten (Ihre Schule) an. Unter `Importiere folgenden Katalog` wählen Sie entweder den Wert `Alle Kataloge` oder einen bestimmten Katalog. Bestätigen Sie dann mit `OK`.

## Statistisch relevante Daten eingeben

Bei einem Großteil der statistisch relevanten Daten handelt es sich um Stammdaten, die bei der alltäglichen Arbeit bereits erfasst wurden. Einige Daten werden Sie nachtragen müssen. Alle für die Statistik erforderlichen Daten finden Sie nachfolgend im in einer tabellarischen Übersicht „Statistikfelder mit Beschreibung“.

## Statistikdaten erstellen

Zum Erstellen der Statistikdaten gehen Sie bitte wie folgt vor:

1. Starten Sie MAGELLAN.
2. Klicken Sie im Menü `Extras` auf `Statistik`.
3. Wählen Sie als Bundesland Berlin und als Schulart Allgemeinbildende Schule (ABS) oder Berufsbildende Schulen (BBS). Klicken Sie dann auf `Weiter`.

![ ](/assets/images/berlin/abidaten/abidaten1.png)

4. Wählen Sie als Art der Erstellung `Nur Statistikdateien` erstellen. Markieren Sie die gewünschte Statistikdatei. Unter Statistikzeiträume auswählen stellen Sie den aktuellen Zeitraum ein. Klicken Sie dann auf `Weiter`.

 ![ ](/assets/images/berlin/abidaten/abidaten2.png)
 
5. Geben Sie das Erstellungsdatum an und wählen Sie den Ordner für den späteren Export der Statistikdateien aus. Klicken Sie auf `Weiter`.

![ ](/assets/images/berlin/abidaten/abidaten3.png)

6. Klicken Sie auf `Start`, um die Erstellung der Statistikdatei zu starten.

## Statistikfelder mit Beschreibung

### Legende

In der nachfolgend aufgelisteten Tabelle zur Statistik erhalten Sie eine Übersicht der geforderten Daten und Ihrer Zuordnung in MAGELLAN, mit entsprechenden Beschreibungen.

**Statistikfeld in der Statistikdatei: **In der erzeugten CSV-Statistikdatei sind die Daten in einer bestimmten Struktur abgelegt. Den Inhalt der CSV-Datei können Sie mit Microsoft Excel ansehen. Über den hier angegeben Pfad zum entsprechenden Statistikfeld, können Sie eine abgespeicherte Statistikinformation gezielt in der CSV-Datei finden.


!!! info "Hinweis"

     Sie wollen überprüfen, ob in der CSV-Datei die Schulnummer korrekt enthalten ist? In der Spalte Statistikfeld finden Sie dazu den Wert 01 – Schul-Nr. Beim Öffnen der CSV-Datei finden Sie die Information dann aufgrund der Listenbeschreibung, als erstes Feld.

Feld|Bedeutung
---|---
Überschrift der Statistikdatei |Ein zusätzliches „*“ in der in der Überschrift der Statistikdatei, zeigt Ihnen an, ob in diesem Jahr eine Änderung für diese Statistikdatei stattgefunden hat.
Bedeutung |Kurzform der Bedeutung des Feldes in der Datenbeschreibung
Datenfeld in MAGELLAN |Hier finden Sie die Angabe, wo Sie das entsprechend zu füllende Datenfeld in MAGELLAN finden. Bei Feldern die sich auf allen Berlinern Sondermasken befinden wird die Ansicht als Masken betitelt, um die Masken nicht einzeln aufzuzählen.
Beschreibung |Diese Spalte enthält eine allgemeine Beschreibung bzw. Hinweis zum auszufüllenden Datenfeld in MAGELLAN.
Typ| In der Spalte „Typ“ können folgende Werte stehen:<br/><br/>P: Gibt an, dass es sich bei diesem Feld um ein Pflichtfeld handelt.<br/>B: Gibt an, dass es sich bei diesem Feld um ein bedingtes Pflichtfeld handelt. Bedingte Pflichtfelder sind Felder, die je nach schulischer Situation für Sie Pflicht sein können.

## Statistikdaten

Feld |Information
--|--
**Statistikfeld**|**Schul-Nr.**
Position|1 
MAGELLAN-Feld|Mandant > Daten1 >  Schulnummer
Beschreibung|Bitte tragen Sie hier die Schulnummer Ihrer Schule ein.
Typ|P
**Statistikfeld**|**Schuljahr Anfang**
Position|2 
MAGELLAN-Feld|-
Beschreibung|Fester vierstelliger Wert (zb. 2017)
Typ|-
**Statistikfeld**|**Schuljahr Ende**
Position|3 
MAGELLAN-Feld|-
Beschreibung|Fester vierstelliger Wert (zb. 2018)
Typ|-
**Statistikfeld**|**Identifikator** 
Position|4
MAGELLAN-Feld|Identifikator 
Beschreibung|Schulinterne Nummer des Schülers. Es wird die ID des Schülers in MAGELLAN exportiert.
Typ|P
**Statistikfeld**|**Name**
Position|5
MAGELLAN-Feld|Schüler > Daten1 > Nachname <br/>Masken > Nachname
Beschreibung|Geben Sie hier den Nachnamen des Schülers ein.
Typ|P
**Statistikfeld**|**Vorname**
Position|6
MAGELLAN-Feld|Schüler > Daten 1 > Vorname<br/>Masken > Nachname
Beschreibung|Geben Sie hier den Vornamen des Schülers ein.
Typ|P
**Statistikfeld**|**Geschlecht**
Position|7
MAGELLAN-Feld|Schüler > Daten 1 > Geschlecht<br/>Masken > Geschlecht
Beschreibung|Wählen Sie hier das Geschlecht des Schülers aus.
Typ|P
**Statistikfeld**| **Geburtsdatum**
Position|8
MAGELLAN-Feld| Schüler > Daten 1 > Geburtsdatum <br/>Masken > Geburtsdatum
Beschreibung| Geben Sie hier das Geburtsdatum des Schülers ein.
Typ| P
**Statistikfeld**| **Geburtsort**
Position|9
MAGELLAN-Feld| Schüler > Daten 1 > Geburtsort<br/>Masken > Geburtsort
Beschreibung| Geben Sie hier den Geburtsort des Schülers ein.
Typ| P
**Statistikfeld**| **Geburtsland**
Position|10
MAGELLAN-Feld| Schüler > Daten 1 > Geburtsland<br/>Masken > Geburtsland
Beschreibung| Geben Sie hier das Geburtsland des Schülers ein.
Typ| P
**Statistikfeld**| **Staatsangehörigkeit**
Position|11
MAGELLAN-Feld| Schüler > Daten 2 > Staatsangeh. 1<br/>Masken > Staatsangeh. 1
Beschreibung| Geben Sie hier die Staatsangehörigkeit des Schülers ein.
Typ| P
**Statistikfeld**| **Herkunftssprache**
Position|12
MAGELLAN-Feld| Schüler > Daten 2 > Muttersprache
Beschreibung| Geben Sie hier die Herkunftssprache Schülers ein.
Typ| B
**Statistikfeld**| **Familiensprache**
Position|13
MAGELLAN-Feld| Schüler > Daten 2 > Verkehrssprache<br/>Masken > Verkehrssprache 
Beschreibung| Geben Sie hier die Verkehrssprache des Schülers ein.
Typ| B
**Statistikfeld**|**Lernmittelbefreiung**
Position|14  
MAGELLAN-Feld| Masken > Lernmittel befreit  
Beschreibung| Geben Sie hier an, ob der Schüler von der Lernmittelabgabe befreit ist  <br/>Wenn Sie nichts eingeben, dann trifft es für den Schüler nicht zu
Typ| P 
**Statistikfeld**|**Bildungsgang**
Position|15
MAGELLAN-Feld| Klassen > Zeiträume > Jahrgang  
Beschreibung| Im aktuellen Zeitraum 2  Halbjahr 20167/2018 muss das Feld den Wert „12“ für G8-Abitur oder „13“ für G9-Abitur haben 
Typ| P 
**Statistikfeld**|**Ersteinschulung**
Position|16  
MAGELLAN-Feld| Schüler > Daten 2 >  Grundschuleintritt  
Beschreibung| Geben Sie hier das Jahr der Ersteinschulung ein  
Typ| B 
**Statistikfeld**|**Eintritt E-Phase**  
Position|17  
MAGELLAN-Feld| Schüler > Laufbahn > Allgemein > Zugang  
Beschreibung| Nur für G9-Abitur: <br/>Geben Sie im Jahrgang 11 der Abiturklasse den Schuljahresanfang für den Eintritt in die E-Phase ein 
Typ| B 
**Statistikfeld**|**Eintritt Q-Phase**  
Position|18  
MAGELLAN-Feld| Schüler > Laufbahn > Allgemein > Zugang  
Beschreibung| Geben Sie im Jahrgang 12 der Abiturklasse den Schuljahresanfang für den Eintritt in die Q-Phase ein  
Typ| P 
**Statistikfeld**|**Anzahl Kurshalbjahre**
Position|19   
MAGELLAN-Feld| Klassen > Zeiträume > Zeitraum > Jahrgang  
Beschreibung| Die Anzahl der Kurshalbjahre errechnet sich durch die korrekte Eingabe der Jahrgänge über alle Halbjahre der Klassen 11-13 hinweg  
Typ| P 
**Statistikfeld**| **Anzahl Wdh in der Oberstufe**
Position|20   
MAGELLAN-Feld| Klassen > Zeiträume > Zeitraum > Jahrgang<br/>Schüler > Laufbahn > Allge-mein > Wiederholer<br/>Schüler > Laufbahn > Allgemein > Versetzt  
Beschreibung| Die Anzahl der Wiederholungen in der Oberstufe errechnet sich durch die Eingabe der Jahrgänge aller Halbjahre der Klassen 11-13  <br/>Wiederholungen müssen entweder mit Wiederholer oder Schüler wurde NICHT versetzt gekennzeichnet werden
Typ| P 
**Statistikfeld**|**Abiturzulassung**
Position|21  
MAGELLAN-Feld| Abitur > Prüfung > Status<br/>Abitur > Qualifikation > Status  
Beschreibung| Der Schüler hat die Abiturzulassung erreicht, wenn im Feld Status der Wert Abiturprüfung bestanden bzw  Abiturprüfung nicht bestanden steht
Typ| P 
**Statistikfeld**|**Nach Zulassungsbescheid zurückgetreten**  
Position|22  
MAGELLAN-Feld| Abitur > Qualifikation > Rücktritt nach Zulassung 
Beschreibung| Geben Sie an, ob der Schüler nach Zulassungsbescheid zurückgetreten ist  
Typ| P 
**Statistikfeld**|**Abiturprüfung Wdh** 
Position|23  
MAGELLAN-Feld| Schüler > Statistik > Merkmal S2  
Beschreibung| Geben Sie hier an, ob der Schüler die Abiturprüfung wiederholt hat<br/>Wenn Sie nichts eingeben, dann trifft es für den Schüler nicht zu
Typ| P 
**Statistikfeld**|**1 LF Kürzel <br/>2 LF Kürzel<br/>3 PF Kürzel<br/>4 PF Kürzel<br/>5 PK Kürzel** 
Position|24,29,34,39,43      
MAGELLAN-Feld| Abitur > Prüfung > Fach      
Beschreibung| Ergibt sich durch die Eingaben im Abiturmodul  <br/>Es wird das eingetragene Fach exportiert     
Typ| P     
**Statistikfeld**|**1 LF Gesamtpunktzahl<br/>2 LF Gesamtpunktzahl<br/>3 PF Gesamtpunktzahl<br/>4 PF Gesamtpunktzahl<br/>5 PK Punktzahl** 
Position|25,30,39,44      
MAGELLAN-Feld| Abitur > Prüfung > 1 PF-5 PF   
Beschreibung| Ergibt sich durch die Eingaben im Abiturmodul und Berechnung der Endnoten      
Typ| -     
**Statistikfeld**|**1 LF Punkte schriftlich<br/>2 LF Punkte schriftlich<br/>3 PF Punkte schriftlich**   
Position|26,31,36      
MAGELLAN-Feld| Abitur > Prüfung > 1 PF-3 PF > Schriftliche Note    
Beschreibung| Geben Sie im Abiturmodul für das entsprechende Prüfungsfach die schriftliche Note ein      
Typ| B     
**Statistikfeld**|**1 LF Punkte mündlich<br/>2 LF Punkte mündlich<br/>3 PF Punkte mündlich**  
Position|27,32,37      
MAGELLAN-Feld| Abitur > Prüfung > 1 PF-3 PF > Mündliche Note    
Beschreibung| Geben Sie im Abiturmodul für das entsprechende Prüfungsfach die mündliche Note ein      
Typ| B     
**Statistikfeld**|**1 LF bilingual <br/>2 LF bilingual<br/>3 PF bilingual<br/>4 PF bilingual** 
Position|28,33,38,41      
MAGELLAN-Feld| Abitur > Qualifikation > Q1 Sprache - Q4 Sprache      
Beschreibung| Geben Sie für ein bilingual gehaltenes Fach die Fremdsprache unter Q1 Sprache – Q4 Sprache an      
Typ| B     
**Statistikfeld**|**5 PK Art**     
Position|42      
MAGELLAN-Feld| Für Gymnasien und Sekundarschulen:<br/> Abitur > Qualifikation > Fachstatus<br/><br/>Für Kollegschulen: Abitur > Prüfung > Lernleistung <br/>Häkchen aktiv- > BLL<br/>Häkchen inaktiv- > Präsentation      
Beschreibung| Für Gymnasien und Sekundarschulen: Ist dort der Wert BLL eingetragen, ist eine besondere Lernleistung  Andernfalls ist eine Präsentationsprüfung  <br/><br/>Für Kollegschulen: es entscheidet das Häkchen für das Einbringen der besonderen Lernleistung    
Typ| P     
**Statistikfeld**|**Theoretische Prüfung Sport**    
Position|45       
MAGELLAN-Feld| Abitur > Prüfung > Fachpraxis > Fach <br/>Abitur > Prüfung > Fachpraxis > Note 1      
Beschreibung| Zum Erfassen der Theoretischen Prüfung in Sport tragen Sie unter Fachpraxis das Fach Sport und in Note 1 das Ergebnis der theoretischen Prüfung ein      
Typ| B     
**Statistikfeld**|**Praktische Prüfung**     
Position|46      
MAGELLAN-Feld| Sport Abitur > Prüfung > Fachpraxis > Fach<br/>Abitur > Prüfung > Fachpraxis > Note 2      
Beschreibung| Zum Erfassen der Praktischen Prüfung in Sport tragen Sie unter Fachpraxis das Fach Sport und in Note 2 das Ergebnis der theoretischen Prüfung ein      
Typ| B     
**Statistikfeld**|**Ausschluss mündl Prüfung**     
Position|47      
MAGELLAN-Feld| Abitur > Prüfung > Eigenschaften > Ausschluss Mündliche Prüfung      
Beschreibung| Markieren Sie das Feld, wenn der Schüler von der Mündlichen Prüfung ausgeschlossen ist     
Typ| B     
**Statistikfeld**|**Abiturprüfung bestanden**      
Position|48      
MAGELLAN-Feld| Abitur > Prüfung > Status <br/>Abitur > Qualifikation > Status<br/>Abitur > Qualifikation > Rücktritt folgenlos      
Beschreibung| Der Schüler hat die Abiturprüfung bestanden, wenn im Feld Status der Wert Abiturprüfung bestanden steht  <br/>Möchte zurücktreten, so muss das Feld Rücktritt folgenlos angewählt sein     
Typ| P     
**Statistikfeld**|**Gesamtpunktzahl**
Position|49      
MAGELLAN-Feld| Abitur > Prüfung > Gesamtpunktzahl      
Beschreibung| Ergibt sich durch die Eingaben und Berechnungen im Feld Gesamtpunktzahl      
Typ| P     
**Statistikfeld**|**1 Fremdsprache<br/>2 Fremdsprache<br/>3 Fremdsprache<br/>4 Fremdsprache**  
Position|50,54,58,61      
MAGELLAN-Feld| Schüler > Daten 3 > Fremdsprachenfolge > 1 -4  Fremdsprache    
Beschreibung| Geben Sie die 1  bis 4  Fremdsprache ein    
Typ| -     
**Statistikfeld**|**1 FS andere anerkannt** <br/>**2 FS andere anerkannt**
Position|51,55      
MAGELLAN-Feld| -     
Beschreibung| -     
Typ|B     
**Statistikfeld**|**1 FS Klasse von<br/>2 FS Klasse von<br/>3 FS Klasse von<br/>4 FS Klasse von**  
Position|52,56,59,62      
MAGELLAN-Feld| Schüler > Daten 3 > Fremdsprachenfolge > 1 -4  Fremdsprache > von    
Beschreibung| Geben Sie die Klassenstufe von für die 1  bis 4  Fremdsprache ein    
Typ|B     
**Statistikfeld**|**1 FS Klasse bis<br/>2 FS Klasse bis<br/>3 FS Klasse bis<br/>4 FS Klasse bis**  
Position|53,57,60,63      
MAGELLAN-Feld| Schüler > Daten 3 > Fremdsprachenfolge > 1-4 Fremdsprache > bis    
Beschreibung| Geben Sie die Klassenstufe bis für die 1 bis 4 Fremdsprache ein    
Typ|B     
**Statistikfeld**|**Latinum**
Position|64      
MAGELLAN-Feld| Abitur > Prüfung > Latinum      
Beschreibung| Geben Sie an, ob der Schüler das Latinum erreicht hat      
Typ|P     
**Statistikfeld**|**Graecum**      
Position|65      
MAGELLAN-Feld| Abitur > Prüfung > Graecum      
Beschreibung| Geben Sie an, ob der Schüler das Graecum erreicht hat      
Typ|P     
**Statistikfeld**|**Hebraicum**      
Position|66      
MAGELLAN-Feld| Abitur > Prüfung > Hebraicum      
Beschreibung| Geben Sie an, ob der Schüler das Hebraicum erreicht hat      
Typ| P     
**Statistikfeld**|**Fach**      
Position|67      
MAGELLAN-Feld| Abitur > Qualifikation > Fach      
Beschreibung| Hier sind jeweils Fächer eingegeben, die für die Oberstufe verwendet werden      
Typ|P     
**Statistikfeld**|**Zusatzfach**     
Position|68      
MAGELLAN-Feld| -     
Beschreibung| Wird aktuell nicht berücksichtigt und daher als leer ausgegeben     
Typ|-     
**Statistikfeld**|**Punkte 1 KHJ**    
Position|69      
MAGELLAN-Feld| Abitur > Qualifikation > Q1      
Beschreibung| Geben Sie hier die Punkte in Q1 ein      
Typ|B     
**Statistikfeld**|**Punkte 1 KHJ (eingebracht)**     
Position|70      
MAGELLAN-Feld| Abitur > Qualifikation > Q1 (markiert)      
Beschreibung| Wenn die Punkte in Q1 eingebracht werden, müssen diese farblich markiert sein (Standardfarbe ist gelb)      
Typ|B     
**Statistikfeld**|**Punkte 2 KHJ**    
Position|71      
MAGELLAN-Feld| Abitur > Qualifikation > Q2      
Beschreibung| Geben Sie hier die Punkte in Q2 ein      
Typ|B     
**Statistikfeld**|**Punkte 2 KHJ (eingebracht)**     
Position|72      
MAGELLAN-Feld| Abitur > Qualifikation > Q2 (markiert)      
Beschreibung| Wenn die Punkte in der Q2 eingebracht werden, müssen diese farblich markiert sein (Standardfarbe ist gelb)      
Typ|B     
**Statistikfeld**|**Punkte 3 KHJ**     
Position|73      
MAGELLAN-Feld| Abitur > Qualifikation > Q3      
Beschreibung| Geben Sie hier die Punkte in Q3 ein      
Typ|B     
**Statistikfeld**|**Punkte 3 KHJ (eingebracht)**     
Position|74      
MAGELLAN-Feld| Abitur > Qualifikation > Q3 (markiert)      
Beschreibung| Wenn die Punkte in Q3 eingebracht werden, müssen diese farblich markiert sein (Standardfarbe ist gelb)      
Typ|B     
**Statistikfeld**|**Punkte 4 KHJ**
Position|75      
MAGELLAN-Feld| Abitur > Qualifikation > Q4      
Beschreibung| Geben Sie hier die Punkte in Q4 ein      
Typ|B     
**Statistikfeld**|**Punkte 4 KHJ (eingebracht)**     
Position|76      
MAGELLAN-Feld| Abitur > Qualifikation > Q4 (markiert)      
Beschreibung| Wenn die Punkte in Q4 eingebracht werden, müssen diese farblich markiert sein (Standardfarbe ist gelb)      
Typ|B 