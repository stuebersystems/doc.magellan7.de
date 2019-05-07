
# BER-APO-2017



## Allgemein


In diesem Skript werden für die korrekte Berechnung unter `Abitur > Qualifikation` drei als Leistungskurse markierte Fachzeilen erwartet, die nicht als 1. oder 2.Prüfungsfach erfasst wurden (Unterrichtsart LK und nicht Fachstatus 1PF oder 2PF). Der 3. Leistungskurs wird in der Berechnung wie ein Grundkurs behandelt.


## Verzeichnis Verordnung


Bitte legen Sie unter ```Verzeichnisse > Verordnungen``` eine neue Zeile an und füllen Sie diese mit den nachstehenden Werten. Beim Synchronisieren der Schüler in das Abitur-Menü weisen Sie den Schülern die Verordnung zu.


|Spalte|Wert|
|--|--|
|Kürzel|beliebig|
|Bezeichnung|beliebig|
|Kategorie|Abitur|
|Typ|bitte leer lassen|
|Ab Jahrgang|bitte tragen Sie vor der Synchronisation der Schüler ins Abiturmodul bei G8 eine 10, sonst eine 11 ein|
|Skript|```...\Ihre Region\Ihr_Skript.dws``` (Pfad zur Skriptdatei auf Ihrem Server)|
|Notenart 11|Noten oder Punkte|
|Notenart 12|Punkte|
|Notenart 13|Punkte|
|Notenart 13|Punkte|
|Notenart BBS|leer|
|Gültig von |leer|
|Gültig bis|leer|




![Eintragung im Verzeichnis Verordnungen für Abiturberechnung und Fachwahl](/images/berlin/ber-apo-2017.00.png)




## Fachkategorien


Jedem Fach, dass Sie in der Oberstufe verwenden, müssen Sie eine Kategorie unter ```Verzeichnisse > Fächer > Kategorie``` zuweisen.
Folgende Fachkategorien werden durch das Abiturqualifikationsskript verwendet, bitte verwenden Sie nur die gekennzeichneten Fachkategorien.


|Fachkategorien|Wird vom Skript berücksichtigt|
|--|--|
|Fremdsprache|x|
|Religion/Ethik|x|
|Deutsch|x|
|Mathematik|x|
|Kunst|x|
|Musik|x|
|Sport|x|
|Informatik|x|
|Philosophie|x|
|Geschichte|x|
|Physik|x|
|Chemie|x|
|Biologie|x|
|Erdkunde|x|
|Sozialkunde|x|
|Wirtschaft|x|
|Politik|x|
|Darstellendes Spiel|x|
|Evangelische Religion||
|Katholische Religion||
|Technik||
|Pädagogik||
|Sporttheorie|x|
|BWL/RW||
|BWL/VWL||
|VWL||
|Seminar|x|
|Gesundheit||
|Psychologie|x|
|Recht|||
|Literatur|||


## Aufgabenbereiche


Folgende Aufgabenbereiche stehen zur Verfügung und müssen unter ```Verzeichnisse > Fächer > Spalte Aufgabenbereich``` verwendet werden:


|Aufgabenbereich|
|--|
|sprachl.-lit.-künstlerisch|
|gesellschaftswiss.|
|mathem.-nat.-technisch|
|Religion|
|Sport|


## Unterrichtsart


Die Unterrichtsart muss unter ```Abitur > Qualifikation > Unterrichtsart``` zugeordnet sein. Sie kann aber auch beim Synchronisieren der Schülerfachdaten bereits aus ```Schüler > Zeugnis > Fächer > Unterrichtsart``` übernommen werden.
Prüfen Sie bitte unter ```Verzeichnisse > weitere Schlüsselverzeichnisse > Unterrichtsarten```, dass in Ihrem Verzeichnis alle erwarteten Werte vorhanden sind oder legen Sie ggfs. an.


|Kürzel| Schlüssel |Bedeutung|
|--|--|--|
|LK|LK|Leistungskurs|
|GK|GK|Grundkurs|
|Z|Z|Zusatzkurs|
|ME|ME|Musik Ensemble|




## Fachstatus


Der Fachstatus muss unter ```Abitur > Qualifikation > Fachstatus``` zugeordnet sein. Er kann aber auch beim Synchronisieren der Schülerfachdaten bereits aus ```Schüler > Zeugnis > Fächer > Fachstatus``` übernommen werden.
Prüfen Sie bitte unter ```Verzeichnisse > weitere Schlüsselverzeichnisse > Fachstatus```, dass in Ihrem Verzeichnis alle erwarteten Werte vorhanden sind oder legen Sie ggfs. an.


|Kürzel |Schlüssel |Bedeutung|
|--|--|--|
|1PF|1PF|1. Prüfungsfach|
|2PF|2PF|2. Prüfungsfach|
|3PF|3PF|3. Prüfungsfach|
|4PF|4PF|4. Prüfungsfach|
|1PFBLL|1PFBLL|1. Prüfungsfach und besondere Lernleistung|
|2PFBLL|2PFBLL|2. Prüfungsfach und besondere Lernleistung|
|3PFBLL|3PFBLL|3. Prüfungsfach und besondere Lernleistung|
|4PFBLL|4PFBLL|4. Prüfungsfach und besondere Lernleistung|
|BLL|Bll|5. Prüfungskomponente besondere Lernleistung|
|PRS|PRS|5. Prüfungskomponente Präsentationsprüfung|


### 5. Prüfungskomponente

Bei der 5. Prüfungskomponente wird zwischen einer **Präsentationprüfung** und der **Besonderen Lernleistung** unterschieden. Gehen Sie jeweils wie folgt vor:

#### Präsentationprüfung

Bei der **Präsentationsprüfung** weisen Sie dem entsprechenden Fach im Menü ``Abitur > Qualifikation > Fachstatus`` den Wert „PRS“ zu und führen das entsprechende Skript aus. 
Im Menü ``Abitur`` wird auf der Registerkarte ``Prüfung`` im Feld ``5. PF`` das jeweilige Fach automatisch eingetragen. Die Noten für die schriftl. Ausarbeitung, Präsentation und das Prüfungsgespräch der Präsenationsprüfung tragen Sie bitte unter ```Abitur > Prüfung`` wie folgt ein:

|Feld | Note|
|--|--|
|schriftliche Note|Note der **schriftliche Ausarbeitung**|
|mündliche Note|Note der **Präsentation**|
|2. mündl. Note| Note des **Prüfungsgespräches**|

![Noteneingabe Präsentationsprüfung](/assets/BER-APO-2017_praesentationspruefung1.png)

#### Besondere Lernleistung

Die **besondere Lernleistung** kann auch eines der ersten 4 Prüfungsfächer sein. In diesem Fall müssen Sie den Fachstatus auf der Registerkarte ``Qualifikation`` wie folgt modifizieren: 
- statt "1PF" nutzen Sie "1PFBLL"
- statt „2PF" nutzen Sie "2PFBLL"
- statt "3PF" nutzen Sie "3PFBLL" oder
- statt "4PF" nutzen Sie "4PFBLL"

Falls die Besondere Lernleistung nicht eines der Prüfungsfächer 1.-4. ist, weisen Sie dem Fach den Fachstatus "BLL" zu und führen das entsprechende Skript aus. Im Menü ```Abitur >  Prüfung`` wird im Feld „5. PF“ das jeweilige Fach automatisch eingetragen. Sie müssen nun nur noch die Gesamtnote im Feld "mündliche Note" eintragen.




