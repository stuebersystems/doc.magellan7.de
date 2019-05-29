# Schlüsselpflege

Um die vom Ministerium auswertbaren Daten liefern zu können, müssen in der Datenbank vorgegebene Schlüsselwerte verwendet werden. 
Damit Ihre Datenbank diese Werte enthält, sind folgende Schritte nötig:

|Nr.|So geht's|
|--|--|
|1.|Statistikschlüssel importieren|
|2.|Kontrolle und ggfs. Anpassen der Schlüsselverzeichnisse|
                                                                                                                               
## Für welche Verzeichnisse können Kataloge importiert werden?


|Verzeichnisname|Anmerkung|
|--|--|
|00_Behinderungsarten.keys|relevant für SaxSVS|
|00_Fachstati.keys|relevant für MAGELLAN|
|00_Faecher.keys|relevant für MAGELLAN|
|00_FoerderSchwerpunkte.keys|relevant für SaxSVS|
|00_Foerderungen.keys|relevant für SaxSVS|
|00_Klassenstufen.keys|relevant für MAGELLAN|
|00_Konfessionen.keys|relevant für MAGELLAN|
|00_Noten.keys|relevant für MAGELLAN|
|00_Sprachreferenzen.keys|relevant für MAGELLAN|
|00_Staatsangehoerigkeiten.keys|relevant für SaxSVS|
|00_Unterrichtsarten.keys|relevant für MAGELLAN|
|AS_SchulformenHerkunft.keys|relevant für MAGELLAN|
|BS_Abgangsarten.keys|relevant für SaxSVS|
|BS_AbschluesseExtern.keys|relevant für SaxSVS|
|BS_AbschluesseIntern.keys|relevant für SaxSVS|
|BS_Abschlussarten.keys|relevant für SaxSVS|
|BS_Abwesenheitsgruende.keys|relevant für SaxSVS|
|BS_Bildungsgaenge.keys|relevant für SaxSVS|
|BS_Organisationen.keys|relevant für SaxSVS|
|BS_SchuelerMerkmale.keys|relevant für SaxSVS|
|BS_Schulformen.keys|relevant für SaxSVS|
|BS_SchulformenHerkunft.keys|relevant für SaxSVS|
|BS_SopaedFoerderungen.keys|relevant für SaxSVS|


## Statistikschlüssel einlesen

Das Statistikamt gibt jährlich aktualisierte Schlüssel für die Landesstatistik heraus. Bitte importieren Sie die Schlüssel nach anstehender Anleitung!

|Nr.|So geht's|
|--|--|
|1.| Stellen Sie sicher, dass Sie die aktuellste Ausgabe von MAGELLAN 7 einsetzen!|
|2.| Öffnen Sie das Modul MAGELLAN- Administrator und wählen die Ansicht `Datenaustausch > Kataloge (Schlüsselverzeichnisse)importieren`.|
|3.| Wählen Sie Sachsen, Ihrer Schulart und Ihren Mandanten aus und importieren einen ausgewählten oder alle mitgelieferten Kataloge.|

![Import der mitgelieferten MAGELLAN-Schlüssel](/assets/images/sachsen/schluesselimport.png)


Wenn Sie MAGELLAN im Alltag einsetzen haben Sie bereits Schlüssel in Ihrer Datenbank verwendet, für die Sie eigene oder keine Werte in der Spalte `Schlüssel` eingetragen haben. 
Durch diese eigenen Werte haben wir nicht die Möglichkeit beim Import der neuen Schlüssel diese mit Ihren Schlüsseln abzugleichen. 
Es muss mindestens beim ersten Statistikdurchlauf (ab dem nächsten Jahr können dann Schlüssel erkannt werden) ein manuelle Nacharbeit erfolgen. Bitte lesen Sie dazu den nächsten Abschnitt!

Erhalten Sie eine Fehlermeldung beim Einlesen des Verzeichnisses `Bildungsgaenge`, lesen Sie bitte weiter unten den Abschnitt "Probleme beim Schlüsselimport?"!


## Kontrolle und Anpassung der Schlüsselverzeichnisse

Beim Import der Schlüssel gibt es einen Ablauf, der gewähren soll, dass die Wahrscheinlichkeit einen inaktuellen oder verkehrten Schlüssel im Alltag zu verwenden, minimiert wird. 

### Einleseprozess

|Nr.|Was passiert beim Einlesen?|
|--|--|
|1.|Alle noch nie verwendeten Schlüsselzeilen werden gelöscht.<br/>Übrig bleiben nur die Zeilen, die Sie bereits einmal verwendet haben.<br/>Diese Zeilen können jetzt für die Statistik richtig oder auch verkehrt sein.
|2.|Alle übrigen Zeilen werden mit einer grauen Raute als inaktive Schlüssel gekennzeichnet.<br/><br/> Zur Erklärung: Jedes Verzeichnis hat die Spalten `von` und `bis`. In diesen Spalten kann man ein Datum eintragen, das wird bei der Anzeige mit dem ausgewählten Zeitraum in MAGELLAN verglichen und der Schlüssel wird demnach mit einer grauen oder einer blauen Raute in der Programmoberfläche gezeigt. Schlüssel mit einer grauen Raute werden zusätzlich ans Ende der Liste sortiert.
|3.|Als nächstes wird ein Schlüssel aus dem Importkatalog anhand seines Schlüsselwerts (Inhalt der Spalte `Schlüssel`) mit den im Verzeichnis noch enthaltenen Schlüsseln verglichen. Werden Zeilen erkannt (gleicher Schlüsselwert), wird der Schlüssel (oder werden die Schlüssel, es dürfen auch mehrere Zeilen existieren) wieder aktiviert, das heißt der oder die Schlüsselzeilen werden als aktive Schlüssel mit einer blauen Raute dargestellt.<br/>Ist keine Zeile mit dem verglichenen Schlüssel im Verzeichnis vorhanden, wird die Schlüsselzeile im Verzeichnis mit angelegt - ist aber bislang nirgendwo im Programm mit einem Datensatz verbunden.|


### Ihre Schlüsselwerte an Vorgaben des Ministeriums anpassen

Um Ihre verwendeten Schlüsseldatensätze auf die Vorgaben des Ministeriums anzupassen, ist noch manuelle Nachpflege erforderlich:

|Nr.|So geht's|
|--|--|
|1.|Nach dem Einlesen öffnen Sie bitte jedes SAXSVS-relevante Verzeichnis (Liste der SAXSVS-relevanten Schlüsselverzeichnisse im Abschnitt "Für welche Verzeichnisse können Kataloge importiert werden?").|
|2.|Sortieren die Schlüssel nach dem `Bis`-Datum, so das Zeilen mit einem `Bis`-Datum oben angeordnet sind. |
|3.|Sind Schlüssel mit einem Eintrag vorhanden? <br/>Dann müssen diese Datensätze jetzt noch editiert werden. <br/>Es handelt sich vermutlich um Werte, die Sie in der Datenbank bereits verwendet haben, die aber nicht den korrekten Schlüsselwert haben. <br/><br/>**Bitte löschen Sie nicht diese Schlüssel!**|
|4.|Wenn Ihr Schlüssel nicht erkannt wurde und daher als inaktiv erkannt wurde, dann hat der Einleseprozess in der Liste, die Sie gerade geöffnet haben, auch den korrekten Schlüssel ergänzt. <br/>Bitte schauen Sie nach, kopieren den Wert aus dem Feld `Schlüssel` und geben Sie diesen Wert für Ihren Schlüssel im Feld `Schlüssel` ein.|
|5.| Entfernen Sie anschließend das `Bis`-Datum für diese Zeile und gehen für die weiteren Zeilen genauso vor.|
|6.|Wenn Sie die SAXSVS-relevanten Verzeichnisse geprüft und entsprechend angepasst haben, lesen Sie bitte die Schlüssel erneut ein! <br/><br/> Überzählige Schlüsseldatensätze werden dann wieder entfernt und Sie erhalten bei eventuell übersehenden Zeilen erneut ein `Bis`-Datum als Zeichen, das hier noch etwas korrigiert werden müsste.<br/> Ist nach dem Einlesen keine `Bis`-Datum mehr gefüllt, sind Ihre Schlüsselwerte korrekt und auch Ihren Schülern zugeordnet. <br/>Mit dieser Schlüsselbasis können dann auch im nächsten Jahr die Schlüssel einfach nur importiert werden, die manuelle Nacharbeit entfällt. 


### Probleme beim Schlüsselimport?

Die Kürzel aus den Verzeichnissen `Schulformen`, `Klassenstufen` und `Organisationen` werden auch indirekt, also als Verweis, im Verzeichnis `Bildungsgänge` benötigt, da einzelnen Bildungsgängen schon weitere Verweise auf andere Verzeichnisse zugeordnet wurden. 

Beispiel: Bildungsgänge in Vollzeit haben in der Spalte `Organisation` ein "v", Teilzeitbildungsgänge ein "t" zu stehen. 

![Verzeichnis `Bildungsgänge`](/assets/images/sachsen/bildungsgaenge.png)

Beim Import kann es zu Fehlermeldungen kommen. Hintergrund ist, wir prüfen die Schlüsselwerte beim Einlesen, ändern nie ein Kürzel. Kürzel sind generell dafür da, dass Schulen Ihre Daten nach eigenen Vorstellungen per Kürzel kennzeichnen. Ist der Schlüssel in Ihrer Datenbank vorhanden, Sie verwenden aber ein anderes Kürzel für den Wert, gelingt der Verweis zwischen Verzeichnissen nicht.

Erscheint eine Meldung zu den Organisationen, den Schulformen oder den Klassenstufen beim Einlesen der Bildungsgänge, schauen Sie bitte in Ihre Datenbank im entsprechenden Verzeichnis nach. 
Sie haben sicher schon Werte eingetragen und verwendet, dabei auch schon durchaus korrekt den Schlüsselwert gefüllt. Aber vielleicht das Kürzel anders gewählt, als es für den Verweis auf das Bildungsgangverzeichnis benötigt wird.
Die Meldung gibt den "Problemwert" aus. Bitte passen Sie das Kürzel in Ihren Verzeichnissen auf die nachstehenden Vorgaben an.

#### Organisationen

|Kuerzel|Schluessel|Bezeichnung|
|--|--|--|
|v|1|Vollzeit|
|t|2|Teilzeit|

#### Schulformen

Kuerzel|Schluessel|Bezeichnung
--|--|--
BS/BS|110|Berufsschule
BS/BGJ|111|Berufsgrundbildungsjahr
BS/BVJ|115|Berufsvorbereitungsjahr
BS/BvB|04|BvB
BS/EQ|05|Einstiegsqualifizierung
BS/VKl|06|Vorbereitungsklasse
BS/gBVJ|07|gestr. BVJ
FOS/FOS|140|Fachoberschule (zweijährig)
FOS12L (v)|14|Fachoberschule 12L Vollzeit
FOS12L (t)|15|Fachoberschule 12L Teilzeit
BFS (v)|120|Berufsfachschule
BFS (t)|20|Berufsfachschule TZ
FS/FS (v)|150|Fachschule
FS/FS (t)|24|Fachschule TZ
BGY|130|Berufliches Gymnasium
BS-F/BS|119|Berufsschule (berufsbildende Förderschule)
BS-F/BGJ|181|Berufsgrundbildungsjahr (berufsbildende Förderschule)
BS-F/BVJ|185|Berufsvorbereitungsjahr (berufsbildende Förderschule)
BS-F/BvB|11|BvB-rehaspezifisch
BS-F/kBVJ|12|koop. BVJ (berufsbildende Förderschule)
BFS-F/BFS|129|Berufsfachschule (berufsbildende Förderschule)

#### Klassenstufen

Kuerzel|Schluessel|Bezeichnung
--|--|--
KL11|12|Klassenstufe 11
JG12|13|Jahrgangsstufe 12
JG13|14|Jahrgangsstufe 13
AJ1|510|Ausbildungsjahr 1
AJ2|520|Ausbildungsjahr 2
AJ3|530|Ausbildungsjahr 3
AJ4|540|Ausbildungsjahr 4