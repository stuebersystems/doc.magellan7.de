# Abschluss der Fachoberschule berechnen

Im Rahmen der Abschlussprüfung an Fachoberschulen kann ein Schüler die Fachhochschulreife erwerben. Grundlage für die Abschlussprüfungen bilden spezielle bundeslandspezifische Verordnungen.

Die jeweiligen Verordnungen spiegeln sich über die Landesanpassung von MAGELLAN in der Fachoberschulberechnung wider. 
Damit die Berechnungen korrekt durchgeführt werden können und Sie auch die Fachhochschulzeugnisse der Fachoberschule richtig ausgedruckt bekommen, müssen Sie allerdings einige wenige aber wichtige Details beachten. Diese Details werden in diesem Kapitel erklärt. Lesen Sie es bitte sorgfältig.

Die Abschlussberechnungen an Fachoberschulen basieren auf MAGELLAN-Skripten, die Sie mit Hilfe des MAGELLAN-Skripteditors bearbeiten können. Weitere Informationen zu diesen Skripten finden Sie in der Dokumentation [MAGELLAN  Scripting](https://doc.magellan-scripting.stueber.de/).

## Allgemein

Zur Organisation der Abschlussprüfung an Fachoberschulen gehören folgende Aufgaben:

1.	Oberstufenjahrgänge und andere Stammdaten einrichten
2.	Schüler-Fächer und Punkte eingeben
3.	Fachhochschulreife berechnen
4.	Zeugnisbemerkungen eingeben und Zeugnisse drucken

Um die Oberstufendaten des jeweiligen Schülers in MAGELLAN anzuzeigen, klicken Sie in MAGELLAN auf „Abitur“ in der Symbolleiste links.

In den folgenden Abschnitten werden die einzelnen Schritte für die Abschlussberechnung der Fachhochschulreife in der Fachoberschule mit MAGELLAN erläutert.
Bevor wir mit der Vorbereitung der Abschlussprüfung beginnen, müssen wir zunächst einige wichtige Bemerkungen zu Jahrgängen und besonderen Fächern machen.

## Skripte

Die gesamte Abschlussberechnung wird durch MAGELLAN-Skripte durchgeführt oder anders gesagt, jedes Abschlussberechnungsskript repräsentiert eine Fachoberschulprüfungsordnung (APO-FOS). Es wird im Folgenden jeweils das Veröffentlichungsjahr der entsprechenden Verordnung angeben.

> #### warning::Wichtig!
>
> Alle zur Verfügung stehenden Skripte finden Sie im [Skriptüberblick](https://doc.magellan6.stueber.de/bundeslaender/berlin/skriptuebersicht.html). Sämtliche notwendigen Einstellungen pro Skript beschreiben wir in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/). Für die Skriptdateien [BER-APO-FOS-2006/2013](https://doc.magellan6.stueber.de/bundeslaender/berlin/fos/ber-apo-fos-20062013.html) folgt die Beschreibung im nächsten Kapitel.

Die Skripte befinden sich im MAGELLAN-Verzeichnis im Ordner „Skripte“. Die MAGELLAN-Skripte berechnen die Fachhochschulreife für die Fachoberschule.

##	Jahrgänge einrichten

Für die Fachoberschule müssen die Jahrgänge 11 (einjährige Fachoberschule) bzw. die Jahrgänge 11 und 12 (zweijährige Fachoberschule) eingerichtet werden.

In MAGELLAN werden die Schüler einer Klassen bzw. einem Jahrgang zugeordnet, indem sie eingeschult werden. Für jeden Schüler werden in MAGELLAN die entsprechenden Fächer bzw. Kurse mit Punkten erfasst. 
In MAGELLAN werden die Daten halbjahresbezogen abgelegt. Sie definieren also die Klassen 11 (einjährige Fachoberschule) oder die Klassen 11 und 12 (zweijährige Fachoberschule) mit je zwei Zeiträumen bzw. Halbjahren. 
Folgende Angaben sind bei der Eingabe der Oberstufenjahrgänge neben den Halbjahren wichtig:

Eingabefeld|	Eingabe
--|--
Klassenart|	Oberstufenjahrgang (nur Kurse)
Jahrgang	|11 oder 12 (pro Zeitraum der Klasse notwendig)
Beurteilungsart	|Benotung durch Punkte

> #### warning::Wichtig!
>
> Um die pro Schüler in den Halbjahren erzielten Ergebnisse in die jeweils korrekte Spalte unter `Abitur  >  Qualifikation` zu synchronisieren, werden im Verzeichnis Verordnungen in der Spalte Typ die Werte „FOS2J“ oder „FOS1J“ erwartet. Für einjährige Klassen werden die Ergebnisse der 11 damit in die Spalten Q3 und Q4 gespielt, für zweijährige die Ergebnisse der 11-12 in die Spalten Q1-Q4.



## Abschlussberechnung vorbereiten


Für die Abschlussberechnung müssen Sie folgende Daten definieren und je Schüler eingeben:


1. Abschlussjahrgang definieren
2. Prüfungsordnung definieren
3. Je Schüler Abschlussjahrgang und Prüfungsordnung angeben
4. Je Schüler die Kurse synchronisieren oder manuell eingeben
5. Je Schüler die Punkte eingeben


In den nachfolgenden Abschnitten erfahren Sie mehr zu den einzelnen Punkten.


## Fachoberschuljahrgang definieren

![Fachoberschuljahrgang definieren](/images/berlin/fos/fos1.png)


Sie können in MAGELLAN unter `Verzeichnisse > Abschlussjahrgänge` Abschlussjahrgänge definieren. In unserem Fall ist dies ein Fachoberschuljahrgang. Damit können Sie jedem Schüler in der Rubrik „Abitur“ den entsprechenden Abiturjahrgang (=Fachoberschuljahrgang) zuordnen. Dieser Vermerk hat keinen Einfluss auf Abschlussberechnungen, sondern dient dazu, später alle Schüler eines bestimmten Fachoberschuljahrgangs z.B. für Ausdrucke herausfiltern zu können. 


> #### warning::Wichtig!
>
> Geben Sie bei der Definition des Fachoberschuljahrgangs im Fenster Verzeichnisse der Abschlussjahrgänge unter „Kategorie“ unbedingt „Abitur“ an.


## Prüfungsordnung definieren


![ Prüfungsordnung definieren](/images/berlin/fos/fos2.png)


Sie müssen für jeden Schüler die Fachoberschulverordnung angeben, die für ihn relevant ist. Dazu müssen Sie im Schlüsselverzeichnis Verordnungen die jeweilige Fachoberschulverordnung definieren. Klicken Sie dazu auf `Verzeichnisse > Verordnungen` und geben Sie dort Verordnung wie folgt an:


Spalte |Bedeutung
--|--
Kürzel| 8-stellige Kurzbezeichnung der Verordnung
Bezeichnung |Bezeichnung der Verordnung
Kategorie |Wenn Sie hier „Abitur“ eingeben, wird es bei den Schülerabiturdaten angezeigt
Typ |Tragen Sie hier „FOS2J“ oder „FOS1J“ ein
Gültig von |Gültigkeitsdatum von, ohne Bedeutung für die Berechnung
Gültig bis| Gültigkeitsdatum bis, ohne Bedeutung für die Berechnung
Skript |Geben Sie hier den Namen des Skripts für diese Fachoberschulverordnung ein. Alle verfügbaren Skripte befinden sich im MAGELLAN-Verzeichnis SKRIPTE.


## Fachoberschulhalbjahresdaten synchronisieren

![Fachoberschulhalbjahresdaten synchronisieren](/images/berlin/fos/fos3.png)


Bevor Sie den Fachoberschulabschluss überprüfen können, müssen Sie die Daten der Schüler synchronisieren, indem Sie in MAGELLAN auf „Abitur“ klicken und dann auf die Schaltfläche` Schüler Synchronisieren...` oben im MAGELLAN-Fenster klicken.


Beim Synchronisieren geschieht Folgendes:


MAGELLAN extrahiert für die markierten Schüler die Fachdaten der Halbjahre 11/1 bis 12/2. Dies ist die Voraussetzung dafür, dass die Qualifikations- und Abschlussberechnungen der Oberstufe durchgeführt werden können. Auch wenn Sie zuvor keine Fächer bzw. Punkte in den Oberstufenhalbjahren angegeben haben, müssen Sie diese Synchronisation einmal ausführen.


Damit die Schüler mit allen Fächern und Noten aus den einzelnen Jahrgängen korrekt übernommen werden können, sind folgende Angaben in MAGELLAN notwendig.


Eingabe|Bedeutung
--|--
Zeiträume|Im Verzeichnis der Zeiträume muss das Feld „Art“ mit dem Wert „1. Halbjahr“ bzw. “2. Halbjahr“ gefüllt sein.
Jahrgang| Bei jeder Klasse/Jahrgang muss auf der Registerkarte „Zeiträume“ für jeden Zeitraum das Feld „Jahrgang“ mit dem Wert „11“ oder „12“ angegeben werden.


Ohne diese Angaben werden nur die Schüler ohne Fächer und Noten übernommen.


> #### primary::Hinweis
>
> Beim Synchronisieren werden die Noten aus der Spalte „Endnote“ in das Menü „Abitur“ übernommen.


Beim Synchronisieren sollten Sie für die markierten Schüler die Fachoberschulverordnung und den Fachoberschuljahrgang eingeben.
Klicken Sie nach dem Synchronisieren auf die Schaltfläche „Abitur“ in der Symbolleiste links im MAGELLAN-Fenster. Es werden alle synchronisierten Schüler auf der Registerkarte „Auswahl“ angezeigt.
Per Doppelklick auf den gewünschten Schüler oder über einen Klick auf die Registerkarte wechseln Sie zur Fachhochschulzulassung. Auf dieser Registerkarte finden Sie die Fächer und Notenwerte der Oberstufenhalbjahre, falls Sie diese Angaben bereits in MAGELLAN unter der Rubrik „Schüler“ gemacht haben sollten. Andernfalls können Sie Fächer und Notenwerte für die Oberstufenhalbjahre auch hier eingeben.


## Fächer und Punkte eingeben


Sollten Sie die Fächer nicht schon im Schüler-Formular (Registerkarte „Zeugnis“) eingegeben haben, so dass sie beim Synchronisieren übernommen wurden, können Sie das auch direkt auf der Registerkarte „Abiturqualifikation“ machen. Mit der Einfg-Taste oder durch Klick auf das Einfügen-Symbol rechts oben erzeugen Sie eine neue Zeile. Geben Sie das Fach, die Unterrichtsart, den Fachstatus und die Punkte ein.


Die Kurse und Noten können Sie ausdrucken, indem Sie die entsprechenden Berichte für Punktekreditkarten verwenden.


## Die Spalte „Position“


Die Position kann als Merkmal für die Reihenfolge der Fächer auf der Registerkarte „Qualifikation“ und auf dem Fachhochschulzeugnis verwendet werden. Die in MAGELLAN mitgelieferten Skripte und Zeugnisformulare verwenden diese Positionsangaben. Beim Einfügen einer neuen Zeile wird automatisch die Position um Eins erhöht, um Ihnen die Eingabe zu ersparen.


Klicken Sie auf den Titel „Position“, um die Fächerliste entsprechend zu sortieren.


## Unterrichtsart, Fachstatus und Merkmal eingeben


In Abhängigkeit vom verwendeten Skript müssen bestimmte Einträge in den Spalten „Unterrichtsart“, „Fachstatus“ und „Merkmal“ berücksichtigt werden.

## Unterrichtsart, Fachstatus und Merkmal eingeben


In Abhängigkeit vom verwendeten Skript müssen bestimmte Einträge in den Spalten „Unterrichtsart“, „Fachstatus“ und „Merkmal“ berücksichtigt werden.


## Vornoten auf der Registerkarte „Qualifikation“

![ Vornoten auf der Registerkarte „Qualifikation“](/images/berlin/fos/fos4.png)

   
Auf  der Registerkarte „Qualifikation“ können Sie die Fächer und Punkte für die einzelnen Halbjahre des Schülers eingeben.  Sie dienen als Grundlage für die Berechnung der Vornote.  
Für die einjährige Fachoberschule werden die Punkte in die Spalten 11/1 und 11/2 eingetragen. Für die zweijährige Fachoberschule werden die Punkte in die Spalten 11/1 bis 12/2 eingetragen.
Haben Sie die einzelnen Punkte der Fächer bereits in den jeweiligen Zeiträumen der Laufbahn des Schülers eingetragen, werden diese im Rahmen der Synchronisation automatisch mit übernommen.

### Spalten ausblenden bzw. umbenennen

Im Dialogfenster „Layout anpassen“ können Sie auf der Registerkarte „Qualifikation“ die Spaltenüberschriften selbst bestimmen und Spalten auf Wunsch ausblenden.
 
![ Spalten ausblenden bzw. umbenennen](/images/berlin/fos/fos5.png)



> #### primary::Hinweis
>
> Sie können einzelne Spalten ausblenden bzw. die Spaltenüberschrift jeder einzelnen Spalte modifizieren. Klicken Sie dazu auf die Schaltfläche    „Layout anpassen“. Für das Skript BER-APO-FOS-2006 oder BER-APO-FOS-2013 muss statt der Spalte „Summe“ die Spalte „Summe2“ eingeblendet werden.

### Berechnung der Vornoten

Zur Berechnung der Vornoten aufgrund der eingetragenen Punkte der Halbjahre gehen Sie wie folgt vor:

* Klicken Sie dann auf „Neu berechnen“, um die Zulassung automatisch durch das Skript berechnen zu lassen. Im Meldungsfenster werden evtl. Fehler ausgegeben. 
Die errechnete Vornote wird in der Spalte „Summe“ auf der Registerkarte „Qualifikation“ eingetragen.

Außerdem werden automatisch Eingaben auf der Registerkarte „Prüfung“ durchgeführt:
* Die Fächer mit dem Fachstatus „1PF“ bis „4PF“ auf der Registerkarte „Qualifikation“ werden automatisch als 1. bis 4. Prüfungsfach auf der Registerkarte „Prüfung“ eingetragen

### Änderung der berechneten Vornote

Ist im Rahmen der jeweiligen Fachoberschulverordnung ein pädagogischer Freiraum zur Festlegung der Vornote gegeben, so kann die manuelle Vorschlagsnote in die Spalte 13/1 auf der Registerkarte „Qualifikation“ eingetragen werden. 
Für die weitere Berechnung wird dann diese Vorschlagsnote anstelle der automatisch berechneten Vorschlagsnote in Spalte  „Summe“ verwendet.

## Die Abschlussprüfung
 
 ![Die Abschlussprüfung](/images/berlin/fos/fos7.png)

 
Die Berechnung der Abschlussnoten aufgrund der Prüfungen und der Durchschnittsnote wird auf der Registerkarte „Prüfung“ durchgeführt. Die Abschlussnoten ergeben sich, indem zusätzlich zu den schon feststehenden Vornoten aus der Qualifikation im Prüfungsbereich noch  Noten in schriftlichen und mündlichen Prüfungen festgestellt werden

### Layout anpassen

Sie können die Anzahl der angezeigten Prüfungsfächer auf bis zu 11 Prüfungsfächer festlegen, indem Sie auf die Schaltfläche` „Layout anpassen“` klicken und im entsprechenden Dialogfenster die Einstellungen machen.

![Layout anpassen](/images/berlin/fos/fos8.png)

 
### Prüfungsdaten eingeben

Machen Sie  auf der Registerkarte „Prüfung“ folgende Angaben:

1. Geben Sie für die Prüfungsfächer unter „1. PF“ bis „11. PF“ das Fach und die Vornote ein. Die Werte sind teilweise durch die Berechnung der Vornote schon vorbesetzt.
2. Geben Sie die schriftlichen Noten ein.
3. Geben Sie die mündlichen Noten ein.

### Abschlussnoten der Prüfungen berechnen

Klicken Sie auf der Registerkarte “Prüfung“ auf die Schaltfläche  `Neu berechnen`, um die Abschlussnoten automatisch durch das entsprechende Skript berechnen zu lassen. 
Im Meldungsfenster wird das Erreichen bzw. das Nichterreichen der Fachhochschulreife ausgewiesen sowie entsprechende Hinweise und die Durchschnittsnote angezeigt.
 
![Abschlussnoten der Prüfungen berechnen](/images/berlin/fos/fos9.png)


> #### primary::Hinweis
>
>  Die Hinweise bzw. Fehlermeldungen im Meldungsfenster sind abhängig vom verwendeten Skript. Fehler führen dazu, dass die Zulassung nicht erreicht ist.

Solange keine Note für das mündliche Prüfungsfach eingetragen wurde, wird angezeigt, welche Mindestpunktzahl in der mündlichen Prüfung erreicht werden muss, damit das Abitur bestanden ist. Wenn als Mindestpunktzahl Null angezeigt wird, ist das Abitur bereits unabhängig von der mündlichen Note bestanden.

Außerdem werden automatisch folgende Zuordnungen durchgeführt:

* Der Status wird auf der Registerkarte auf „Fachhochschulreife erreicht“ oder „Fachhochschulreife nicht erreicht“ umgesetzt.
* Die Abschlussnoten (=Endnoten) für die Prüfungsfächer werden berechnet und auf der Registerkarte unter „Summe“ eingetragen. 
* Die Durchschnittsnote wird auf der Registerkarte eingetragen.

### Abschlussdaten manuell eingeben

Wenn Sie die Abschlussberechnung nicht skriptgesteuert eingeben möchten, können Sie die durch das Skript gemachten Eingaben auch selbst vornehmen:

1. Setzen Sie den Status auf „Fachhochschulreife erreicht“ oder „Fachhochschulreife nicht erreicht“.
2. Geben Sie die Abschlussnoten unter „Summen“ ein.
3. Geben Sie die Durchschnittsnote ein.

### 	Zeugnisbemerkungen eingeben

Geben Sie auf der Registerkarte „Zeugnis“ evtl. Zeugnisbemerkungen ein, die auf dem Fachhochschulzeugnis gedruckt werden sollen.

### 	Fachhochschulzeugnisse drucken

Klicken Sie bei den Abiturdaten des Schülers auf die Registerkarte „Zeugnis“, um die Zeugnisbemerkungen anzugeben. Zusammen mit den Angaben auf den Registerkarten „Qualifikation“ und „Prüfung“ verfügen Sie dann über alle Daten um das Abiturzeugnis auszudrucken.

### So drucken Sie Fachhochschulzeugnisse:

1. Markieren Sie in der Liste der Schüler der Oberstufe per Mausklick oder mit Umschalt+Mausklick oder Strg+Mausklick die entsprechenden Schüler.
2. Klicken Sie auf `Bearbeiten `und `Drucken `und wählen Sie das Zeugnisformular und klicken Sie auf `Drucken`.

