
# Die Fachwahl

Die Fachwahlkarte speichert die geplante Fachwahl des Schülers für die Oberstufe. Die Fachwahl wird meist in Klassenstufe 10 gefüllt und dann halbjahresweise in den für den Zeugnisdruck relevanten Bereich `Schüler > Zeugnis` übertragen, damit die Leistungen erfasst werden können. Für die Abiturberechnung werden die Eintragungen in den Halbjahren der Oberstufe unter `Schüler > Zeugnis` in das Menü `Abitur > Qualifikation` synchronisiert.

Auf der Fachwahlkarte wird:

1. die Fachwahl des Schülers eingetragen 
2. die Fachwahl auf Basis einer Fachwahlverordnung auf Gültigkeit überprüft 
3. die gültige Fachwahl halbjahresweise zu den Fächern des Schülers übernommen 

!!! info "Hinweis"

	Die Fachwahleingabe kann auch in DaVinci Kursplan erfolgen. Dort ist die Fachwahleingabe etwas ausführlicher und komfortabler: Es können zusätzlich die Stundenzahlen der einzelnen Halbjahre eingegeben werden. Das zugrundeliegende Skript, d.h. das Regelwerk, ist in beiden Fällen das gleiche: Magellan verwendet für die Fachwahlüberprüfung das DaVinci Fachwahl-Skript. Alternativ kann aber auch die Fachwahl des aktuellen Jahres oder die Fachwahl über die gesamte Oberstufe nach DaVinci übergeben werden.


## Abgleich der Karte Qualifikation und Karte Fachwahl

Unter `Datenbank > Optionen > Einstellungen` kann die Option `Abgleich Qualifikation/Fachwahl` im Abitur gewählt werden. Damit würden Einträge, die auf der Karte `Fachwahl` getätigt werden, auch auf der Karte `Qualifikation` gezeigt werden. Das ist aber mitunter missverständlich, da die Qualifikationskarte per Synchronisation aus dem Bereich `Schüler > Zeugnis > Fächer und Leistungen` befüllt wird.

!!! info "Hinweis"

	**Wir empfehlen diese Option NICHT zu wählen!** Die Qualifikationskarte wird später aus den Daten der Halbjahre mit den belegten Fächern und den dazugehörigen Noten befüllt. Die Fachwahl kann durchaus Fächer beinhalten, die später nicht belegt werden.
  

## Ablauf 

Auf der Karte `Fachwahl` wird die Fachwahl des Schülers für die kommenden Oberstufenhalbjahre festgehalten. 
Sollte sich mit der Zeit etwas an der Fachwahl des Schülers ändern, weil er zum Beispiel umwählt oder ein Kurs nicht zustande kommt, wird die Änderungen auf dieser Karte vermerkt. 
Zu Beginn jedes Halbjahres werden von der Fachwahlkarte aus die Fachwahlen für das jeweilige Halbjahr in den Bereich `Schüler > Zeugnis > Fächer` übernommen um dort die Grundlage für die Erfassung der Halbjahres- oder Jahresnoten und damit für den Zeugnisdruck zu bilden. 
Nach dem Durchlauf der Oberstufe werden die über die Halbjahre gesammelten Ergebnisse und Fächer dann gesammelt auf die Karte `Abitur > Qualifikation` synchronisiert um die Grundlage für die Abiturberechnung zu bilden.

![Ablauf](/assets/images/gym_oberstufe/fw.05.png)

## Vorbereitung

### Fachwahltafel

 Unter `Verzeichnisse > Fachtafeln` legen Sie eine Fachwahltafel an. Diese Fachwahltafel enthält alle Fächer die in der Oberstufe vorkommen einmal und es wird die meist zutreffende Unterrichtsart zugeordnet. 
 Wenn Sie Zeugnisse verwenden, die Positionsnummern erwarten, dann tragen Sie diese auch hier schon ein.

Eintrag|Hinweis
---|---
**Fach**|Legen Sie in der Fachwahltafel jedes in der Oberstufe wählbare Fach als eine Zeile an, nicht Deu als GK und Deu als LK usw. <br/>Das ist besonders wichtig, wenn Sie im Anschluss einen Kurswahlbogen nutzen möchten, Berichte sind für eine Höchstzahl von Zeilen ausgelegt, anderenfalls gelingt die korrekte Darstellung eventuell nicht mehr.  
**Unterrichtsart**|Weisen Sie jedem Fach die am ehesten zutreffende Unterrichtsart zu, zum Beispiel alle Fächer erhalten die Unterrichtsart GK.
**Fachstatus**|Tragen Sie hier nur etwas ein, wenn es eine definitive Zuordung zwischen Fach und Fachstatus gibt.
**Markieren**|Legen Sie hier das häufigste Belegungsmuster fest.
**Position**|Zeugnisberichte benötigen Informationen um Fächer an der korrekten Stelle zeigen zu können. Bitte schauen Sie im Modul Magellan Berichte nach, ob für die von Ihnen eingesetzen Zeugnisberichte Vorgaben für Position pro Fach existieren und tragen Sie diese hier bitte bereits ein. 
**Q1Sprache-Q4Sprache**|Einige Zeugnisberichte geben Hinweise zu bilingualem Unterricht aus, bitte schauen vorab im Modul Magellan Berichte nach, ob das für Ihre Zeugnisse zutrifft und geben ggfs. die Information bereits hier ein. Grundlage ist das Verzeichnis `Kurssprache` unter `Extras > Schlüsselverzeichnisse`.

![vorbereitete Fachwahltafel](/assets/images/gym_oberstufe/fw.00.png)

### Abschlussjahrgang

Prüfen Sie, ob unter `Extras > Schlüsselverzeichnisse > Abschlussjahrgang` Abschlussjahrgang eingerichtet wurde, zu dem die Schüler voraussichtlich ihr Abitur ablegen werden. Diese Angabe ist verpflichtend im Assistenten zur Synchronisation der Schüler, dient aber eigentlich Ihrer Übersicht unter `Abitur > Auswahl`.

### Abiturverordnung

Prüfen Sie, ob unter `Extras > Schlüsselverzeichnisse > Verordnungen` die Verordnung eingerichtet wurde, nach der die Schüler voraussichtlich ihr Abitur ablegen werden. 

!!! info "Hinweis"

	Bitte lesen Sie dazu auch den Abschnitt ["Vorbereitung"](https://doc.magellan.stueber.de/schulverwaltung/howto/Oberstufe/vorbereitung/)!

### Zeiträume

Um die Fachwahlen für die Oberstufe erfassen zu können, müssen zusätzlich zukünftige Zeiträume angelegt werden. Bitte legen Sie die Zeiträume soweit an, dass die Schuljahre bis zum Abitur für die aktuelle Klasse 10 existieren.

Beispiel:
Aktuelles Schuljahr 2018/2019: Um für Schüler der aktuellen Klasse 10 (die ihr Abitur voraussichtlich in der Klassenstufe 12 absolvieren) die Oberstufenfachwahl zu erfassen, müssen auch das Schuljahr 2019/2020 (Jahrgang 11) und das Schuljahr 2020/2021 (Jahrgang 12) angelegt werden.

### Klassenjahrgang und Klassenart

Prüfen Sie, ob die Klassen die korrekte `Klassenart` und den korrekten `Klassenjahrgang` haben.

![Klasseneinstellungen](/assets/images/gym_oberstufe/fw.01.png)

## Schüler für Fachwahlen synchronisieren

Als erstes müssten die Schüler, für die die künftige Fachwahl erfasst werden soll, in den Punkt `Abitur` synchronisiert werden.  In der Regel müssen nur die Schüler (also ohne Fachdaten oder Noten) ins Menü `Abitur` übernommen werden. Dieser Unterschied wird mit der Klassenart vorgenommen, stellen Sie bei den Klassen bitte "Standard mit Oberstufensynchronisation" ein.

![Klassenart für die Fachwahl](/assets/images/gym_oberstufe/oberstufe01.png)

|So geht's|
|--|
|1.  Wechseln Sie im gewünschten Zeitraum ins Menü `Abitur` und starten den Punkt `Schüler > Schüler synchronisieren`!|
|2.  Markieren Sie die gewünschten Schüler, dabei können Sie per Gruppieren, Filtern, Sortieren und Filtern Ihre Auswahl zusammenstellen.|
|3.  Wählen Sie den Abschlussjahrgang und die Verordnung aus, nach der die Schüler später Ihr Abitur ablegen werden.|

Die Schüler werden jetzt im Menü `Abitur` in der Auswahlliste gezeigt.

## Fachwahlen zuordnen

### Zuordnen per Assistent

|So geht's|
|--|
|1. Wechseln Sie in der Ansicht `Abitur` auf die Registerkarte `Fachwahl`.|
|2. Klicken Sie im oberen Bereich auf die Schaltfläche `Fachwahltafel zuweisen`.<br/><img src="/assets/images/gym_oberstufe/gym_oberstufe07.png">|
|3. Markieren Sie die Schüler, denen Sie eine Fachwahltafel zuweisen wollen und klicken Sie dann auf `Weiter`.|
|4. Markieren Sie die gewünschte Fachwahltafel und ordnen Sie optional im unteren Bereich den Halbjahren die entsprechende Zeiträume zu. Sollen bei der Zuweisung der Fachwahltafeln die eventuell bereits bestehenden Fachwahlen der markierten Schüler nicht zuvor gelöscht werden, so müssen Sie das Kontrollkästchen Vorhandene Fachwahlen der Schüler nicht löschen markieren. Klicken Sie auf `Weiter`.|
|5. Geben Sie optional den zuzuordnenden `Abiturjahrgang `und die `Fachwahlverordnung `an und klicken Sie dann auf `Weiter`.|
|6. Klicken Sie auf `Fertigstellen`, um die Fachwahltafel den markierten Schülern zuzuordnen.|

### Fächer manuell zuordnen

Die Fächer der Fachwahl können auch ohne die Kopiervorlage der Fachwahltafeln dem Schüler zugeordnet werden. 

|So geht's|
|--|
|1. Wechseln Sie in der Ansicht `Abitur` auf die Registerkarte Fachwahl.|
|2. Klicken Sie im oberen Bereich auf das rote Plus für eine neue Zeile.|
|3. Tragen Sie jetzt das Fach und optional die Unterrichtsart und den Fachstatus ein.|

## Schülerfachwahlen individuell anpassen

* Passen Sie die Fachwahlkarte pro Schüler an, je nach individueller Fachwahl des Schülers, tragen Sie die Prüfungsfächer und Leistungskurse ein.

!!! info "Hinweis"

	Je nach Kursbildung werden eventuelle Änderungen ( ein Lateinkurs kommt doch nicht zu Stande o.ä.) auf der Fachwahlkarte eingetragen!

## Fachwahl prüfen

Sobald Sie dem Schüler eine Fachwahlverordnung zugeordnet haben, wird die Schaltfläche `Neu prüfen` zur Überprüfung der Fachwahl aktiv. Auf Basis der eingetragenen Fachwahl können Sie durch Wahl der Schaltfläche `Neu prüfen` diese prüfen. Das Ergebnis der Prüfung wird im oberen Bereich der Registerkarte Fachwahl angezeigt. Ist die Anzeige rot unterlegt, handelt es sich um eine (noch) nicht gültige Fachwahl.

 ![Diese Fachwahl ist noch fehlerhaft](/assets/images/gym_oberstufe/gym_oberstufe09.png)

Bei einer gültigen Fachwahl ist der obere Hinweistext grün hinterlegt mit dem Hinweis „Fachwahl ist gültig“.

![Diese Fachwahl ist gültig](/assets/images/gym_oberstufe/gym_oberstufe10.png)

Mit Wahl der Schaltfläche `Neu prüfen` wird oberhalb dieser Schaltfläche der Status `Fachwahl geprüft ` angezeigt. Verändert man die Fachwahl des Schülers, wechselt der Status automatisch auf Fachwahl nicht geprüft.

![Dies ist die Anzeige des Prüfstatus „Fachwahl nicht geprüft“ ](/assets/images/gym_oberstufe/gym_oberstufe11.png)

![Dies ist die Anzeige des Prüfstatus „Fachwahl geprüft“](/assets/images/gym_oberstufe/gym_oberstufe12.png)

!!! info "Hinweis"

Ist für ein eingetragenes Fach keine der Spalten „1. HJ“ bis „6. HJ“ markiert, wird dieses Fach bei der Fachwahlprüfungals nicht gewählt betrachtet.
Die Zuordnung der Zeiträume zu den Halbjahren 1 bis 6 auf der rechten Seite haben keinen Einfluss auf die Fachwahlprüfung. Sie dienen nur der späteren Zuweisung der Fahlwahlen eines Halbjahres zu den Fächern des Schülers.

## Fachwahl pro Halbjahr nach `Schüler > Zeugnis` übernehmen

Die unter Ansicht `Abitur > Fachwahl` erstellten Fachwahlen der Schüler können nun zu Fächern der Schüler auf der Registerkarte Ansicht `Schüler > Zeugnis > Fächer` übernommen werden. Diese Übernahme erfolgt immer zum aktuell eingestellten Zeitraum.

Bei der Übernahme der Fachwahl eines Schülers werden nur die Fächer übernommen, die

* in einem der sechs Halbjahre auf der rechten Seite den aktuellen Zeitraum von Magellan zugewiesen haben und
* die in diesem Halbjahr das Kontrollkästchen markiert haben.

Beispiel:

In Magellan ist der aktuelle Zeitraum das „1. Halbjahr 2011/2012“. Der Schüler hat die nachfolgende Fachwahl:

 ![Beispiel für die Fachwahl eines Schülers](/assets/images/gym_oberstufe/gym_oberstufe13.png)

Die Spalte 1. HJ entspricht dem Zeitraum „1. Halbjahr 2011/2012“. Übernimmt man nun die Fachwahl im aktuellen Zeitraum, so werden alle Fächer der Fachwahl übernommen bis auf das Fach „Fr“, da dieses in der Spalte 1. HJ nicht markiert ist.

Auf Basis dieser Zuordnung kann nun die Zuweisung der Fachwahlen zu den Fächern der Schüler wie folgt durchgeführt werden.

|So geht's|
|--|
|1. Wechseln Sie in der Ansicht ``Abitur`` auf die Registerkarte `Fachwahl`.|
|2. Klicken Sie im oberen Bereich auf die Schaltfläche `Fachwahl übernehmen`.|
|3. Markieren Sie die Schüler, deren Fachwahl Sie übernehmen wollen. Sollen bei der Übernahme die eventuell bereits bestehenden Fächer der markierten Schüler nicht zuvor gelöscht werden, so müssen Sie das Kontrollkästchen `Vorhandene Fächer der Schüler nicht löschen` markieren. Klicken Sie dann auf `Weiter`.|
|4. Klicken Sie auf `Fertigstellen`, um die Fachwahlübernahme zu starten.|

Die übernommen Fächer finden Sie nun auf der Registerkarte Ansicht `Schüler > Zeugnis > Fächer`.

|Option im Assistenten|Bedeutung|
|--|--|
| <img src="/assets/images/gym_oberstufe/fw.06.png">|Es wird geprüft, ob bereits für den Schüler Fächer unter `Schüler > Zeugnis > Fächer` existieren, wenn ja wird die Fachwahl nicht übernommen. Hat der Schüler keine Fächer, werden die Fächer übergeben.|
|<img src="/assets/images/gym_oberstufe/fw.07.png"> |Es werden unter `Schüler > Zeugnis > Fächer` existierende Fächer gelöscht (damit auch ev. bereits erfasste Noten) und die Fächer aus der Fachwahl eingetragen.|
|<img src="/assets/images/gym_oberstufe/fw.08.png"> |Bestehende Fächer auf der Zeugniskarte bleiben erhalten, die Fächer der Fachwahl werden ergänzt. |
|<img src="/assets/images/gym_oberstufe/fw.09.png"> |Bestehende Fächer auf der Zeugniskarte bleiben erhalten, die Fächer der Fachwahl werden ergänzt, der Fachstatus bleibt erhalten.|

!!! info "Hinweis"

	Eventuelle Umwahlen werden für die Schüler vor der halbjährlichen Übernahme der Fächer unter `Abitur > Fachwahl` eintragen.

![Fachwahl schülerindividuell von der Fachwahlkarte in den Schülerzeugnisbereich übertragen](/assets/images/gym_oberstufe/fw.04.png)

### Nutzung der Fachwahlen in Stundenplanprogrammen

Nachdem die Fachwahlen den Fächern der Schüler zugewiesen worden sind, können diese Daten im Stundenplanprogramm DaVinci oder anderen Stundenplanprogrammen zur weiteren Stundenplanung verwendet werden. Nähere Informationen zum Datenabgleich finden Sie im Kapitel [„Stundenplandaten“](https://doc.magellan.stueber.de/schulverwaltung/howto/stundenplaene/).

## Wie geht es weiter?

* Wenn die Oberstufe durchlaufen wurde, werden die Fächer und die Leistungen der Oberstufenhalbjahre aus `Schüler > Zeugnis` nach `Abitur > Qualifikation` synchronisiert. Dafür führen Sie den Assistenten unter `Abitur > Qualifikation > Schüler synchronisieren` aus.

!!! info "Hinweis"

	Das Synchronisieren der Fächer und Leistungen auf die Karte `Qualifikation` ändert keine Einträge auf der Karte `Fachwahl`.
