# Abiturskript BER-APO-2011.dws 


Voraussetzung für die Abiturqualifikationsberechnung und Fachwahlüberprüfung ist, dass Sie für jedes in der Oberstufe benutzte Fach die Kategorie und den Aufgabenbereich und bei den Fächern des Schülers die entsprechende Unterrichtsart und den entsprechenden Fachstatus eingegeben haben.

##Verzeichnis Verordnung
Bitte legen Sie unter ```Verzeichnisse > Verordnungen``` eine neue Zeile an und füllen Sie diese mit den nachstehenden Werten. Beim Synchronisieren der Schüler in das Abitur-Menü weisen Sie den Schülern die Verordnung zu.

|Spalte|Wert|
|--|--|
|Kürzel|beliebig|
|Bezeichnung|beliebig|
|Kategorie|Abitur|
|Typ|leer|
|Ab Jahrgang|bitte tragen Sie vor der Synchronisation der Schüler ins Abiturmodul [bei G8] eine 10, sonst [G9] eine 11 ein|
|Skript|```...\Ihre Region\Ihr_Skript.dws``` (Pfad zur Skriptdatei auf Ihrem Server)|
|Notenart 11|Noten oder Punkte|
|Notenart 12|Punkte|
|Notenart 13|Punkte|
|Notenart 13|Punkte|
|Notenart BBS|leer|
|Gültig von |leer|
|Gültig bis|leer|



![Beispiel für Eintragung im Verzeichnis Verordnungen für Abiturberechnung (G8 oder G9)](/images/berlin/abitur/ber.apo.2011.png)




## Aufgabenbereiche


Die Aufgabenbereiche sind in MAGELLAN und DAVINCI fest vorgegeben. Ihre Bedeutung ergibt sich unmittelbar aus der allgemeinen Abiturverordnung.


> #### warning::Wichtig!
>
> Bitte verwenden Sie die Aufgabenbereiche in MAGELLAN unter `Verzeichnisse > Fächer` in Spalte Aufgabenbereich. Diese Angaben müssen für jedes für die Oberstufe verwendete Fach gesetzt werden.


Abkürzung| Bedeutung
---|---
sprachl.-lit.-künstlerisch |sprachlich-literarisch-künstlerisches Aufgabenfeld
gesellschaftswiss. |gesellschaftswissenschaftliches Aufgabenfeld
mathem.-nat.-techn. |mathematisch-naturwissenschaftlich-technisches Aufgabenfeld
Religion |Religion
Sport |Sport



## Fachkategorien

Jedem Fach, dass Sie in der Oberstufe verwenden, müssen Sie eine Kategorie unter ```Verzeichnisse > Fächer > Kategorie``` zuweisen.
Folgende Fachkategorien werden durch das Abiturqualifikationsskript verwendet, bitte verwenden Sie nur die gekennzeichneten Fachkategorien.

|Fachkategorien|Wird vom Skript berücksichtigt|
|--|--|--|
|Fremdsprache|JA|
|Religion/Ethik|JA|
|Deutsch|JA|
|Mathematik|JA|
|Kunst|JA|
|Musik|JA|
|Sport|JA|
|Informatik|JA|
|Philosophie|JA|
|Geschichte|JA|
|Physik|JA|
|Chemie|JA|
|Biologie|JA|
|Erdkunde|JA|
|Sozialkunde|JA|
|Wirtschaft|JA|
|Politik|JA|
|Darstellendes Spiel|JA|
|Evangelische Religion||
|Katholische Religion||
|Technik||
|Pädagogik||
|Sporttheorie|JA|
|BWL/RW||
|BWL/VWL||
|VWL||
|Seminar|JA|
|Gesundheit||
|Psychologie|JA|
|Recht|||
|Literatur|||




## Spalte „Unterrichtsart“


Folgende Unterrichtsarten werden durch das Abiturqualifikations- bzw. Fachwahlskript verwendet:


Kürzel| Schlüssel| Bedeutung
---|---|---
LK| LK |Leistungskurs
GK |GK |Grundkurs
Z |Z |Zusatzkurs
ME |ME |Musik Ensemble


## Spalte „Fachstatus“


Folgende Fachstatus werden durch das Abiturqualifikations- bzw. Fachwahlskript verwendet:


Kürzel |Schlüssel| Bedeutung
---|---|---
1PF |1PF |1. Prüfungsfach
2PF |2PF |2. Prüfungsfach
3PF |3PF |3. Prüfungsfach
4PF |4PF |4. Prüfungsfach
1PFBLL |1PFBLL |1. Prüfungsfach und Besondere Lernleistung
2PFBLL| 2PFBLL |2. Prüfungsfach und Besondere Lernleistung
3PFBLL| 3PFBLL |3. Prüfungsfach und Besondere Lernleistung
4PFBLL| 4PFBLL| 4. Prüfungsfach und Besondere Lernleistung
BLL |BLL |5. Prüfungskomponente Besondere Lernleistung
PRS |PRS |5. Prüfungskomponente Präsentationsprüfung


> #### primary::Hinweis
>
> Für das mitgelieferte Skript müssen die entsprechenden Schlüssel vorhanden sein. Das Kürzel wird nur zur Anzeige verwendet und kann daher beliebig gewählt werden.


## Die 5. Prüfungskomponente


Bei der 5. Prüfungskomponente wird zwischen einer „Präsentationprüfung“ und der „Besonderen Lernleistung“ unterschieden. Gehen Sie in MAGELLAN jeweils wie folgt vor:


### Präsentationprüfung


Bei der "Präsentationsprüfung" weisen Sie dem entsprechenden Fach im Menü „Abitur“ Registerkarte „Qualifikation“ in der Spalte „Fachstatus“ den Wert „PRS“ zu und führen das entsprechende Skript aus.
Im Menü „Abitur“ wird auf der Registerkarte „Prüfung“ im Feld „5. PF“ das jeweilige Fach automatisch eingetragen. Sie müssen nun nur noch die Gesamtnote im Feld "mündliche Note" eintragen.


### Besondere Lernleistung


Die "besondere Lernleistung" kann auch eines der ersten 4 Prüfungsfächer sein. In diesem Fall müssen Sie den Fachstatus auf der Registerkarte „Qualifikation“ wie folgt modifizieren:


- statt "1PF" nutzen Sie "1PFBLL"
- statt „2PF" nutzen Sie "2PFBLL"
- statt "3PF" nutzen Sie "3PFBLL" oder
- statt "4PF" nutzen Sie "4PFBLL"


Falls die Besondere Lernleistung nicht eines der Prüfungsfächer 1.-4. ist, weisen Sie dem Fach den Fachstatus "BLL" zu und führen das entsprechende Skript aus. Im Menü „Abitur“ wird auf der Registerkarte „Prüfung“ im Feld „5. PF“ das jeweilige Fach automatisch eingetragen. Sie müssen nun nur noch die Gesamtnote im Feld "mündliche Note" eintragen. 
