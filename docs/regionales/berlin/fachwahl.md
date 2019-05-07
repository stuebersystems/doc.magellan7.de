# Schüler-Fachwahlen eingeben und prüfen

> #### warning::Wichtig!
>
> Die Schüler-Fachwahlen können anstatt in MAGELLAN auch in DAVINCI KURSPLAN erfasst werden. Die Fachwahlüberprüfung in MAGELLAN und DAVINCI erfolgt mit dem gleichen Fachwahlskript.  In DAVINCI können im Gegensatz zu MAGELLAN noch zusätzlich die Stundenzahlen je Halbjahr erfasst werden.

##	Voraussetzung für die Fachwahlen
Um Fachwahlen für Schüler in MAGELLAN zu erfassen, muss der jeweilige Schüler:

*	in MAGELLAN angelegt und einer Klasse zugeordnet und
*	in die Ansicht „Abitur“ synchronisiert worden sein.

Das Anlegen eines Schülers und dessen Einschulung in eine Klasse können Sie der Dokumentation [MAGELLAN 6](https://doc.magellan6.stueber.de/) entnehmen. Der Klasse selbst muss  unter Ansicht ` „Klassen“  >  Daten` im Feld Klassenart einer der Werte:

*	Standard mit Oberstufensynchronisation
*	Oberstufenjahrgang (Nur Kurse)
*	Oberstufenjahrgang (Leistungs- und Grundkurse) 

zugewiesen sein, um Schüler dieser Klasse in die Ansicht „Abitur“ zu synchronisieren. Um Schüler in die Ansicht „Abitur“ zu synchronisieren, müssen Sie den:

* den Abiturjahrgang definieren
* die Fachwahlverordnung definieren

###	Abiturjahrgang definieren
Sie können in MAGELLAN unter `Verzeichnisse > Abschlussjahrgänge` Abschlussjahrgänge definieren. In unserem Fall ist dies ein Abiturjahrgang. Damit können Sie jedem Schüler in der Rubrik „Abitur“ den entsprechenden Abiturjahrgang zuordnen. Dieser Vermerk hat keinen Einfluss auf Abschluss- oder Qualifikationsberechnungen, sondern dient dazu, später alle Schüler eines bestimmten Abiturjahrgangs herausfiltern zu können.
 
![Hier definieren Sie den Abiturjahrgang mit der Kategorie „Abitur“](/images/berlin/fachwahl/fachwahl1.png)

> #### warning::Wichtig!
>
> Geben Sie bei der Definition des Abiturjahrgangs im Fenster „Verzeichnisse der Abschlussjahrgänge“ unter „Kategorie“ unbedingt den Wert „Abitur“ an.

###	Fachwahlverordnung definieren

Spalte|	Bedeutung
--|--
Kürzel	|Kurzbezeichnung der Fachwahlverordnung (max. 10-stellig)
Bezeichnung|	Bezeichnung der Fachwahlverordnung (frei wählbar)
Kategorie	|Wenn Sie hier „Fachwahl“ eingeben, können Sie diese Verordnung für die Fachwahlüberprüfung auf der Registerkarte Ansicht „Abitur“ > Fachwahl verwendet.
Typ	|Geben Sie hier den Wert „G8“ an, wenn es ein G8-Abitur ist (2-jährige Form). Bei keiner Angabe wird von der dreijährigen Form (G9) ausgegangen.
Ab Jahrgang	|Geben Sie hier den Jahrgang an, ab der die Oberstufenverordnung gilt, mögliche Eingaben sind Jahrgang 10(G8) oder 11(G9). Nach dieser Eingabe werden die Daten in unterschiedliche Spalten im Abiturmodul synchronisiert.
Notenart 11-13|Geben Sie hier an, ob Sie in der Oberstufe Punkt- oder Notenwerte vergeben möchten.
Gültig von|	ohne Bedeutung für die Berechnungen
Gültig bis	|ohne Bedeutung für die Berechnungen
Skript	|Verweisen Sie hier bitte auf die Skriptdatei. Das Skript enthält auch die Berechnung der Fachhochschulreife. Alle verfügbaren Skripte befinden sich im MAGELLAN-Verzeichnis SKRIPTE in Ihrem Bundeslandunterordner.

 
![Verzeichnis der Verordnungen](/images/berlin/fachwahl/fachwahl2.png)

Sie müssen für jeden Schüler die Abiturordnung angeben, die für ihn relevant ist. Dazu müssen Sie im Schlüsselverzeichnis „Verordnungen“ die jeweilige Fachwahlverordnung und/oder Abiturprüfungsordnung definieren. Klicken Sie dazu auf `Verzeichnisse > Verordnungen` und geben Sie dort die Verordnung wie folgt an:

###	Schülerdaten in die Ansicht „Abitur“ synchronisieren 

Bevor Sie die Fachwahlen bzw. Abiturqualifikationen überprüfen können, müssen Sie die Daten der Schüler in die Ansicht „Abitur“ synchronisieren.

Voraussetzung|	Anmerkung
---|---
Zeitraumart	|Im Verzeichnis der Zeiträume muss das Feld „Art“ mit dem Wert „1. Halbjahr“ bzw. “2. Halbjahr“ gefüllt sein.
Klassenart	|Unter Klasse  >  Daten muss im Feld „Klassenart“ die Auswahl „Oberstufenjahr-gang (Leistungs- und Grundkurse)“ oder „Oberstufenjahrgang (nur Kurse)“ getroffen sein. Für den Übertrag der Schüler für die Fachwahl kann auch „Standard mit Oberstufensynchronisation“ gewählt werden. In diesem Fall werden keine Fachdaten synchronisiert, sondern nur die Schüler.
Jahrgang	|Bei jeder Klasse/Jahrgang muss auf der Registerkarte „Zeiträume“ für jeden Zeitraum das Feld „Jahrgang“ mit dem Wert „11“, „12“ oder „13“ angegeben werden. Das gilt nicht für Klassen mit der Klassenart „Standard mit Oberstufensynchronisation“.
Abschlussjahrgänge|	Bitte legen Sie unter Verzeichnisse  >  Verordnungen die Abschlussjahrgänge an. Es genügt dabei die Angabe des Kürzels, der Bezeichnung und der Kategorie (Abitur).
Verordnungen|	Richten Sie bitte unter `Verzeichnisse  >  Verordnungen` pro verwendeter Abiturverordnung oder Fachwahl eine Zeile entsprechend der Anleitung im Abschnitt „Fachwahlverordnung definieren“ ein.

Beim Synchronisieren extrahiert MAGELLAN für die markierten Schüler die Fachdaten der Halbjahre E1, E2, Q1, Q2, Q3 und Q4 in die Ansicht „Abitur“. Dies ist die Voraussetzung für die Fachwahl-, Qualifikations- und Abschlussberechnungen der Oberstufe. Liegen noch keine Fachdaten in den Halbjahren vor, werden nur die Grunddaten des Schülers in die Ansicht „Abitur“ übernommen. Vor der Eingabe der Fachwahlen auf der Registerkarte Ansicht Abitur > Fachwahl sind beispielsweise noch keine Fächer beim Schüler auf der Registerkarte Ansicht `Schüler > Zeugnis > Fächer` eingetragen. 

> #### warning::Wichtig!
>
> Für das Erfassen der Fachwahlen der Schüler, müssen vor dem Synchronisieren keine Fächer auf der Registerkarte Ansicht `Schüler > Zeugnis > Fächer` eingetragen werden. Sind dort aber bereits Fächer erfasst gewesen, können Sie die Fächer beim Synchronisieren auch zusätzlich mit in die Fachwahlen übertragen lassen. Wählen Sie dafür vor der Synchronisation die Option `Extras  >  Optionen > Einstellungen > Abgleich Qualifikationen/Fachwahl im Abitur`.
Indem Sie in MAGELLAN auf die Ansicht „Abitur“ und dann auf die Schaltfläche `Schüler synchronisieren...` auf der oberen Symbolleiste klicken, öffnen Sie das Dialogfenster Daten für Abitur synchronisieren.
 
![Schaltfläche „Schüler synchronisieren“ in der oberen Symbolleiste der Ansicht „Abitur“](/images/berlin/fachwahl/fachwahl3.png)

Im Dialogfenster Daten für Abitur synchronisieren müssen Sie nun wie folgt vorgehen:
1.	Markieren Sie alle die Schüler, die Sie in die Ansicht „Abitur“ synchronisieren wollen. Klicken Sie dann auf `Weiter`.
 
![ Auswahl der Schüler im Dialogfenster zum Synchronisieren der Daten in die Ansicht „Abitur“](/images/berlin/fachwahl/fachwahl4.png)

2.	Wählen Sie bei den weiteren Angaben die zugehörige Abturjahrgang und die entsprechende Prüfungsverordnung für das Abitur aus, die für die zuvor markierten Schüler gelten soll. Klicken Sie dann auf `Weiter`.
 
![Weitere Angaben im Dialogfenster zum Synchronisieren der Daten in die Ansicht „Abitur“](/images/berlin/fachwahl/fachwahl5.png)

3.	Klicken Sie abschließend auf `Fertigstellen`.

Die Schüler werden jetzt in die Ansicht „Abitur“ synchronisiert.
In der Ansicht „Abitur“ finden Sie alle bereits synchronisierten Schüler in der Auswahlliste. Wenn Sie dort einen Schüler markieren und auf die Registerkarte Fachwahl gehen, sehen Sie dort dessen die Fachwahlinformationen.
 
 ![Die Fachwahlinformationen für den Schüler „Thomas Müller“ auf der Registerkarte „Fachwahl“ in der Ansicht „Abitur“](/images/berlin/fachwahl/fachwahl6.png)

##	Fachwahl Layout einstellen
In der Ansicht „Abitur“ können Sie auf der Registerkarte Fachwahl das Layout der dargestellten Spalten verändern, indem Sie auf die Schaltfläche Layout anpassen klicken. 
 
![ Hier kann das Layout der Spalten auf der Registerkarte „Fachwahl“ in der Ansicht „Abitur“ eingestellt werden](/images/berlin/fachwahl/fachwahl7.png)

Im Dialogfenster Layout anpassen können Sie für jede Spalte bestimmen, ob diese sichtbar ist oder nicht. Spaltenüberschriften können Sie ändern, wenn Sie auf den jeweiligen Text unter „Spaltenüberschrift“ klicken.
Wenn die Einführungsphase keinen Einfluss auf die Fachwahlprüfung hat, sollte man z.B. die Spalten „E1“ und „E2“ ausblenden.

## Schüler-Fachwahl eintragen

In der Ansicht „Abitur“ können Sie der Registerkarte Fachwahl grundsätzliche folgende Funktionen ausführen:

1.	die Fachwahl des Schülers eingetragen (siehe diesen Abschnitt „Schüler-Fachwahl eintragen“),
2.	die Fachwahl auf Basis einer Fachwahlverordnung auf Gültigkeit überprüft (siehe nachfolgender Abschnitt „Fachwahl prüfen“.
3.	die gültige Fachwahl abschließend zu den Fächern des Schülers übernommen (siehe nachfolgenden Abschnitt „Schüler-Fachwahl als Fächer des Schülers übernehmen“) und
4.	die Fachwahl an Untis übergeben (siehe nachfolgendes Kapitel „Schüler-Fachwahlen nach Untis übertragen“).
Das Eintragen der Fächer für die Fachwahl kann sowohl rein manuell pro Fach erfolgen oder wesentlich komfortabler per Zuordnung von Fachwahltafeln.

## Fachwahltafeln verwenden

Mit der Verwendung von Fachwahltafeln können Sie sich die Eingabe erleichtern, indem Sie eine Fachwahltafel einem oder mehreren Schüler gleichzeitig zuweisen.

So definieren Sie eine Fachwahltafel:

1. 	Wählen über `Verzeichnisse > Fachtafeln` das Verzeichnis der Fachtafeln aus.
2.	Legen Sie auf der Registerkarte Fachtafeln über Neue Zeile eine neue Fachwahltafel an. Achten Sie dabei auf den Eintrag Fachwahltafel in der Spalte Art.
3.	Tragen Sie für die Fachwahltafel auf der Registerkarte Fachwahltafel – Fächer die Fächer der Fachwahltafel mit deren Eigenschaften ein.
  
## Empfehlung zum Anlegen einer Fachwahltafel

Die nachstehenden Hinweise eine Empfehlung, damit Sie möglichst wenig nach dem Zuweisen noch pro Schüler anpassen müssen. Zusätzlich sind für Berechnungsskripte und Zeugnisberichte bestimmte Eintragungen Voraussetzung für korrektes Funktionieren, einige Angaben können Sie hiermit bereits sicherstellen.

Eintrag|Hinweis
---|---
**Fach**|Legen Sie in der Fachwahltafel jedes in der Oberstufe wählbare Fach als nur eine Zeile an. Es gibt nur eine Zeile für Deu,  nicht Deu als GK und Deu als LK usw. <br/>Das ist besonders wichtig, wenn Sie im Anschluss zum Beispiel einen Kurswahlbogen nutzen möchten, Berichte sind für eine Höchstzahl von Zeilen ausgelegt (oder erwarten genau eine Zeile für ein bestimmtes Fach), anderenfalls gelingt die korrekte Darstellung eventuell nicht mehr.  
**Unterrichtsart**|Weisen Sie jedem Fach die am ehesten zutreffende Unterrichtsart zu, zum Beispiel alle Fächer erhalten die Unterrichtsart GK.
**Fachstatus**|Tragen Sie hier nur etwas ein, wenn es eine definitive Zuordung zwischen Fach und Fachstatus gibt.
**Markieren**|Legen Sie hier das häufigste Belegungsmuster fest.
**Position**|Zeugnisberichte benötigen Informationen um Fächer an der korrekten Stelle zeigen zu können. Bitte schauen Sie im Modul MAGELLAN Berichte nach, ob für die von Ihnen eingesetzen Zeugnisberichte Vorgaben für Position pro Fach existieren und tragen Sie diese hier bitte bereits ein. 
**Q1Sprache-Q4Sprache**|Einige Zeugnisberichte geben Hinweise zu bilingualem Unterricht aus, bitte schauen vorab im Modul MAGELLAN Berichte nach, ob das für Ihre Zeugnisse zutrifft und geben ggfs. die Information bereits hier ein. 


![Beispiel für den Inhalt einer Fachwahltafel](/images/gym_oberstufe/fachwahltafel.png)



> #### primary::Hinweis
>
> Wenn Sie in einer Fachzeile auf die Schaltfläche `Markieren `klicken, markieren Sie alle Halbjahre 6 Halbjahre auf einmal. Ein erneutes Anwählen der Schaltfläche `Markieren `führt zur Demarkierung aller 6 Halbjahre.


> #### primary::Hinweis
>
> Das Schlüsselverzeichnis „Kurssprachen“ unter Verzeichnisse > Weitere Schlüsselverzeichnisse > Kurssprachen muss mit entsprechenden Fremdsprachen gefüllt sein, damit Sie in den Spalten Q1 Sprache, Q2 Sprache, Q3 Sprache und Q4 Sprache einen Wert für die Unterrichtssprache auswählen können.

So weisen Sie eine Fachwahltafel Schülern in der Ansicht „Abitur“ zu:

1.	Wechseln Sie in der Ansicht „Abitur“ auf die Registerkarte Fachwahl.
2.	Klicken Sie im oberen Bereich auf die Schaltfläche` Fachwahltafel zuweisen`.
  
 ![Hier markieren Sie die Schüler, denen Sie eine Fachwahltafel zuweisen wollen.](/images/berlin/fachwahl/fachwahl9.png)
 
3.	Markieren Sie die Schüler, denen Sie eine Fachwahltafel zuweisen wollen und klicken Sie dann auf `Weiter`. 
4.	Markieren Sie die gewünschte Fachwahltafel und ordnen Sie optional im unteren Bereich den Halbjahren die entsprechende Zeiträume zu. Sollen bei der Zuweisung der Fachwahltafeln die eventuell bereits bestehenden Fachwahlen der markierten Schüler nicht zuvor gelöscht werden, so müssen Sie das Kontrollkästchen `Vorhandene Fachwahlen der Schüler nicht löschen` markieren. Klicken Sie auf `Weiter`.
 
![ Wählen Sie hier die Fahlwahltafel für die markierten Schüler aus.](/images/berlin/fachwahl/fachwahl10.png)

5.	Geben Sie optional den zuzuordnenden Abiturjahrgang und die Fachwahlverordnung an und klicken Sie dann auf `Weiter`.
 
 ![Ordnen Sie den markierten Schülern optional einen Abiturjahrgang und eine Fachwahlverordnung zu.](/images/berlin/fachwahl/fachwahl11.png)
 
6.	Klicken Sie auf `Fertigstellen`, um die Fachwahltafel den markierten Schülern zuzuordnen.
 
![Darstellung auf der Registerkarte „Fachwahl“ in der Ansicht „Abitur“ nach der Zuweisung einer Fachwahltafel für den Schüler „Thomas Müller“](/images/berlin/fachwahl/fachwahl12.png)

## Schüler-Fachwahl manuell eingeben

Die Fächer der Fachwahl können auch ohne die Kopiervorlage der Fachwahltafeln dem Schüler zugeordnet werden. Dazu gehen Sie pro Fach wie folgt vor:

1.	Wechseln Sie in der Ansicht „Abitur“ auf die Registerkarte Fachwahl.
2.	Klicken Sie im oberen Bereich auf das Symbol ![  ](/images/berlin/fachwahl/fachwahl13.png)für eine neue Zeile.
3.	Tragen Sie jetzt das Fach und optional die Unterrichtsart und den Fachstatus ein.

> #### warning::Wichtig!
>
> Wird ein Fach manuell zugeordnet, sind in der dadurch erzeugten neuen Zeile die sichtbaren Spalten „E1“ bis „Q4“ automatisch markiert.

Wenn Sie die Fachwahl manuell pro Fach auf diese Weise zuordnen, müssen Sie im Unterschied zur Zuweisung per Fachwahltafel auch 

*	pro Fach die Pflichtkursanzahl optional eintragen,
*	pro Fach die Unterrichtsart und optional den Fachstatus eintragen,
*	pro Fach festlegen, in welchen Halbjahren das Fach belegt wird sowie
*	die Fachwahlverordnung festlegen 
*	und Zuordnung der Halbjahre zu den die Zeiträume pro Schüler manuell vornehmen.

##	Fachwahl prüfen

> #### primary::Hinweis
>
> Die Fachwahlüberprüfung richtet sich nach der beim Schüler unter „Fachwahlverordnung“ eingestellten Verordnung. Die Verordnung wird durch das Fachwahlskript geprüft. Der Name des verwendeten Fachwahlskripts wird beim Schüler immer unten links ausgegeben, z.B.  „BER-FW-APO-BBS-2011.js“
Sobald Sie dem Schüler eine Fachwahlverordnung zugeordnet haben, wird die Schaltfläche `Neu prüfen` zur Überprüfung der Fachwahl aktiv. 
 
 ![Aktive Schaltfläche „Neu prüfen“ auf der Registerkarte „Fachwahl“ in der Ansicht „Abitur“ nach der Zuweisung der Fachwahlverordnung für den Schüler „Thomas Müller“.](/images/berlin/fachwahl/fachwahl14.png)
 
Das Prüfen der Fachwahl basiert auf Eintragungen:
*	der Spalte Fach,
*	der Spalte Unterrichtsart,
*	der Spalte Fachstatus und 
*	den Markierungen der Spalten Q1, Q2, Q3, Q4.

Auf Basis der eingetragenen Fachwahl können Sie durch Wahl der Schaltfläche `Neu prüfen` diese prüfen. Das Ergebnis der Prüfung wird im oberen Bereich der Registerkarte Fachwahl angezeigt. Ist die Anzeige rot unterlegt, handelt es sich um eine (noch) nicht gültige Fachwahl. 
 
 ![Diese Fachwahl ist noch fehlerhaft](/images/berlin/fachwahl/fachwahl15.png)
 
Bei einer gültigen Fachwahl ist der obere Hinweistext grün hinterlegt mit dem Hinweis „Fachwahl ist gültig“.
 
 ![Diese Fachwahl ist gültig und weist die gültige Fachwahlkombinationsnummer 1 aus.](/images/berlin/fachwahl/fachwahl16.png)
 
Mit Wahl der Schaltfläche `Neu prüfen` wird oberhalb dieser Schaltfläche der Status Fachwahl geprüft angezeigt. Verändert man die Fachwahl des Schülers, wechselt der Status automatisch auf `Fachwahl nicht geprüft`.
    
![Dies ist die Anzeige des Prüfstatus „Fachwahl nicht geprüft“](/images/berlin/fachwahl/fachwahl17.png) 
![bzw. „Fachwahl geprüft“](/images/berlin/fachwahl/fachwahl18.png)


> #### warning::Wichtig!
>
> Ist für ein eingetragenes Fach keine der Spalten „E1“ bis „Q4“ markiert, wird dieses Fach bei der Fachwahlprüfung als nicht gewählt betrachtet.
> Die Zuordnung der Zeiträume zu den Halbjahren 1 bis 6 auf der rechten Seite haben keinen Einfluss auf die Fachwahlprüfung. Sie dienen nur der späteren Zuweisung der Fahlwahlen eines Halbjahres zu den Fächern des Schülers (siehe nachfolgender Abschnitt)
> Das Skript prüft die Stundenbelegung. Dabei werden Leistungskurse 5-stündig, Grundkurse 3-stündig gezählt. Eine Ausnahme bildet Sport-Praxis, dieses Fach wird als 2-stündig gezählt, erkannt wird das Fach anhand des Fachschlüssels 129.
 
Für eine G8-Fachwahl werden mindestens 32 Grundkurse (GK+LK=40) mit 132 Stunden erwartet. Für eine G9-Fachwahl werden mindestens 24 Grundkurse (GK+LK=32) in 112 Stunden erwartet. 

##	Fachwahl verändern
Wenn Sie eine Fachwahl nachträglich ändern wollen, so gelten hier die gleichen Funktionalitäten wie bei der Eintragen und Prüfung der Fachwahl. Bei einer umfangreichen Änderung der Fachwahl können Sie auch eine andere Fachwahltafel neu zuzuweisen.

##	Schüler-Fachwahl als Fächer des Schülers übernehmen
Die unter Ansicht „Abitur“ > Fachwahl erstellten Fachwahlen der Schüler haben keine Verbindung zu den Fächern der Schüler auf der Registerkarte Ansicht` „Schüler“ > Zeugnis > Fächer`. Die unter Ansicht `„Abitur“ > Fachwahl` erstellten Fachwahlen der Schüler können nun zu Fächern der Schüler auf der Registerkarte Ansicht `„Schüler“ > Zeugnis > Fächer `übernommen werden. Diese Zuweisung erfolgt immer zum aktuell eingestellten Zeitraum in MAGELLAN.

Bei der Übernahme der Fachwahl eines Schülers werden nur die Fächer übernommen, die

*	in einem der sechs Halbjahre auf der rechten Seite den aktuellen Zeitraum von MAGELLAN zugewiesen haben und
*	die in diesem Halbjahr das Kontrollkästchen markiert haben.

**Beispiel: **
In MAGELLAN ist der aktuelle Zeitraum das „1. Halbjahr 2013/2014“. Der Schüler hat die nachfolgende Fachwahl:
  
 ![Ein Beispiel für die Fachwahl eines Schülers](/images/berlin/fachwahl/fachwahl19.png)

Die Spalte Q3 entspricht dem Zeitraum „1. Halbjahr 2013/2014“. Übernimmt man nun die Fachwahl im aktuellen Zeitraum, so werden alle Fächer der Fachwahl übernommen bis auf das Fach „IN“, da dieses in der Spalte Q3 nicht markiert ist.
Auf Basis dieser Zuordnung kann nun die Zuweisung der Fachwahlen zu den Fächern der Schüler wie folgt durchgeführt werden:

1.	Wechseln Sie in der Ansicht „Abitur“ auf die Registerkarte Fachwahl.
2.	Klicken Sie im oberen Bereich auf die Schaltfläche Fachwahl übernehmen.
3.	Markieren Sie die Schüler, deren Fachwahl Sie übernehmen wollen. Standardmäßig werden Fachwahlen für einen Schüler übernommen, wenn der Schüler keine Fächer unter Ansicht `„Schüler“ > Zeugnis > Fächer` im aktuellen Zeitraum besitzt. Soll eine Übernahme der Fachwahlen erfolgen, auch in den Fällen, in welchen der Schüler Fächer unter Ansicht `„Schüler“ > Zeugnis > Fächer` im aktuellen Zeitraum besitzt, so müssen Sie die Option `Vorhandene Fächer in der Ansicht „Schüler > Zeugnis > Fächer“ aktualisieren ` auswählen. Sollen bei der Übernahme die eventuell bereits bestehenden Fächer der markierten Schüler nicht zuvor gelöscht werden, so müssen Sie das `Kontrollkästchen Vorhandene Fächer der Schüler nicht löschen` markieren. Klicken Sie dann auf `Weiter`. 

 ![Der Assistent zur Übernahme der Fachwahlen](/images/berlin/fachwahl/fachwahl20.png)
 
4.	Klicken Sie auf `Fertigstellen`, um die Fachwahlübernahme zu starten.

Die übernommen Fächer finden Sie nun auf der Registerkarte Ansicht `„Schüler“ > Zeugnis > Fächer`.

 ![Nach der Übernahme der Fachwahlen sind die Fächer in der Ansicht „Schüler“ > Zeugnis > Fächer](/images/berlin/fachwahl/fachwahl21.png)
  
> #### warning::Wichtig!
>
> 	Nach der Übernahme der Fächer des Schülers aus der Fachwahl in die Ansicht `„Schüler“ > Zeugnis > Fächer` sind noch keine Kurse zugeordnet. Dies erfolgt erst durch die Kursbildung bzw. Kursblockung in Untis. Die dort jedem Schüler zugeordneten Kurse können dann nach MAGELLAN übertragen (siehe Kapitel „Schüler-Kurswahlen von Untis “)


##	Abgleich der Fächer in der Ansicht „Abitur“
Unter `Extras > Optionen > Einstellungen` kann die Option `Abgleich Qualifikation/Fachwahl im Abitur` gewählt werden. 

> #### warning::Wichtig!
>
> Diese Option ist für keinen Schritt in der Oberstufe Voraussetzung: die Fächer- und Notendaten der Schüler werden später beim Synchronisieren der Schülerdaten ins Abiturmodul auf die Qualifikationskarte übertragen!

Der gewöhnliche Ablauf bestehend aus den Schritten:

1. Fachwahl im Abiturbereich
2. Übergabe auf die Schülerzeugniskarte
3. Noteneingabe auf der Schülerzeugniskarte
4. Synchronisieren der Fächer und Noten in den Abiturbereich)
 
![Die Einstellung der Option „Automatischer Abgleich Qualifikation/Fachwahl“ im Dialogfenster „Optionen“](/images/berlin/fachwahl/fachwahl22.png)

Durch die Aktivierung dieser Optionen werden Veränderungen an den Fächern auf den Registerkarten Ansicht „Abitur“ > Qualifikation und Ansicht „Abitur“ > Fachwahl automatisch mit der jeweils anderen Registerkarte abgeglichen.

* Synchronisieren von Schülern in die Ansicht „Abitur“: Gibt es für die synchronisierten Schüler bereits Fachdaten in der Ansicht „Schüler“ > Zeugnis > Fächer, werden diese auf die Registerkarte Ansicht „Abitur“ > Qualifikation und Ansicht „Abitur“ > Fachwahl übernommen.
*	Ein Fach wird ergänzt: Wird ein Fach auf der Registerkarte Ansicht „Abitur“ > Qualifikation oder auf der Registerkarte Ansicht „Abitur“ > Fachwahl neu angelegt, wird das Fach automatisch auf der anderen Registerkarte ergänzt. Das gilt auch durch das Ergänzen per Fachwahltafel auf der Registerkarte Ansicht „Abitur“ > Fachwahl oder durch erneutes Synchronisieren der Schüler in die Ansicht „Abitur“. 
*	Ein Fach wird gelöscht: Wird ein Fach auf der Registerkarte Ansicht „Abitur“ > Qualifikation oder auf der Registerkarte Ansicht „Abitur“ > Fachwahl gelöscht, wird das Fach auch automatisch auf jeweils anderen Registerkarte entfernt.
*	Unterrichtsart, Fachstatus o.ä. wird verändert: Ist ein Fach durch den Abgleich auf beiden Karten angelegt worden und es wird eine der zusätzlich zur Verfügung stehenden Eigenschaften geändert, wird die Änderung auch auf der anderen Karte mit abgebildet. 

> #### warning::Wichtig!
>
> Bereits bestehende Fächer auf den Registerkarten Fachwahl und Qualifikation werden durch das Setzen der Option `Abgleich Qualifikation/Fachwahl im Abitur` nicht automatisch abgeglichen. Die Option wirkt sich nur auf neu angelegte oder neu synchronisierte Fächer aus.


