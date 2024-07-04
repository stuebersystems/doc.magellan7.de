# Schüler-Fachwahlen eingeben und prüfen

[2]:/assets/images/berlin/fachwahl/fachwahl2.png
[6]:/assets/images/berlin/fachwahl/fachwahl6.png
[7]:/assets/images/berlin/fachwahl/fachwahl7.png
[9]:/assets/images/berlin/fachwahl/fachwahl9.png
[10]:/assets/images/berlin/fachwahl/fachwahl10.png
[11]:/assets/images/berlin/fachwahl/fachwahl11.png
[12]:/assets/images/berlin/fachwahl/fachwahl12.png
[14]:/assets/images/berlin/fachwahl/fachwahl14.png
[15]:/assets/images/berlin/fachwahl/fachwahl15.png
[16]:/assets/images/berlin/fachwahl/fachwahl16.png
[19]:/assets/images/berlin/fachwahl/fachwahl19.png
[20]:/assets/images/berlin/fachwahl/fachwahl20.png
[21]:/assets/images/berlin/fachwahl/fachwahl21.png
[22]:/assets/images/berlin/fachwahl/fachwahl22.png
[23]:/assets/images/berlin/fachwahl/fachwahl23.png

!!! info "Hinweis"

    Die Schüler-Fachwahlen können anstatt in Magellan auch in DaVinci Kursplan erfasst werden. Die Fachwahlüberprüfung in Magellan und DaVinci erfolgt mit dem gleichen Fachwahlskript. In DaVinci können im Gegensatz zu Magellan noch zusätzlich die Stundenzahlen je Halbjahr erfasst werden.

## Voraussetzung für die Fachwahlen

Um Fachwahlen für Schüler in Magellan zu erfassen, muss der jeweilige Schüler:

* in Magellan angelegt und einer Klasse zugeordnet und
* in die AnsichtAbitursynchronisiert worden sein.

Das Anlegen eines Schülers und dessen Einschulung in eine Klasse können Sie der Dokumentation [Magellan](https://doc.magellan.stueber.de/schulverwaltung/howto/schueler/) entnehmen. Der Klasse selbst muss unter Ansicht `Klassen > Daten` im Feld "Klassenart" einer der Werte:

* Standard mit Oberstufensynchronisation
* Oberstufenjahrgang (Nur Kurse)
* Oberstufenjahrgang (Leistungs- und Grundkurse)

zugewiesen sein, um Schüler dieser Klasse in die Ansicht `Abitur` zu synchronisieren. Um Schüler in die Ansicht `Abitur` zu synchronisieren, müssen Sie den:

* den Abiturjahrgang definieren
* die Fachwahlverordnung definieren

### Abiturjahrgang definieren

Sie können in Magellan unter `Extras > Schlüsselverzeichnisse > Abschlussjahrgänge` Abschlussjahrgänge definieren. In unserem Fall ist dies ein Abiturjahrgang. Damit können Sie jedem Schüler in der Rubrik `Abitur` den entsprechenden Abiturjahrgang zuordnen. Dieser Vermerk hat keinen Einfluss auf Abschluss- oder Qualifikationsberechnungen, sondern dient dazu, später alle Schüler eines bestimmten Abiturjahrgangs herausfiltern zu können.
 
![Abiturjahrgang mit der Kategorie "Abitur“ definieren](/assets/images/berlin/fachwahl/fachwahl1.png)

!!! info "Hinweis"

    Geben Sie bei der Definition des Abiturjahrgangs im FensterVerzeichnisse der AbschlussjahrgängeunterKategorieunbedingt den WertAbituran.

### Fachwahlverordnung definieren

Spalte| Bedeutung
--|--
Kürzel |Kurzbezeichnung der Fachwahlverordnung (max. 10-stellig)
Bezeichnung| Bezeichnung der Fachwahlverordnung (frei wählbar)
Kategorie |Wenn Sie hier Fachwahl eingeben, können Sie diese Verordnung für die Fachwahlüberprüfung unter `Abitur> Fachwahl` verwendet.
Typ |Geben Sie hier den Wert "G8" an, wenn es ein G8-Abitur ist (2-jährige Form). Bei keiner Angabe wird von der dreijährigen Form (G9) ausgegangen.
Ab Jahrgang |Geben Sie hier den Jahrgang an, ab der die Oberstufenverordnung gilt, mögliche Eingaben sind Jahrgang 10(G8) oder 11(G9). Nach dieser Eingabe werden die Daten in unterschiedliche Spalten im Abiturmodul synchronisiert.
Notenart 11-13|Geben Sie hier an, ob Sie in der Oberstufe Punkt- oder Notenwerte vergeben möchten.
Gültig von| ohne Bedeutung für die Berechnungen
Gültig bis |ohne Bedeutung für die Berechnungen
Skript |Verweisen Sie hier bitte auf die Skriptdatei. Das Skript enthält auch die Berechnung der Fachhochschulreife. Alle verfügbaren Skripte befinden sich im Magellan-Verzeichnis unter dem Ordner "Skripte" in Ihrem Bundeslandunterordner.

[![Verzeichnis der Verordnungen][2]][2]

Sie müssen für jeden Schüler die Abiturordnung angeben, die für ihn relevant ist. Dazu müssen Sie im `Schlüsselverzeichnis > Verordnungen` die jeweilige Fachwahlverordnung und/oder Abiturprüfungsordnung definieren. Gehen Sie hier zu `Extras > Schlüsselverzeichnisse > Verordnungen` und geben Sie dort die Verordnung wie folgt an:

### Schülerdaten in die Ansicht `Abitur` synchronisieren 

Bevor Sie die Fachwahlen bzw. Abiturqualifikationen überprüfen können, müssen Sie die Daten der Schüler in die Ansicht `Abitur` synchronisieren.

Voraussetzung| Anmerkung
---|---
Zeitraumart |Im Verzeichnis der Zeiträume muss das FeldArtmit dem Wert1. Halbjahrbzw. “2. Halbjahrgefüllt sein.
Klassenart |Unter `Klasse > Daten` muss im Feld "Klassenart" die Auswahl "Oberstufenjahrgang (Leistungs- und Grundkurse)" oder "Oberstufenjahrgang (nur Kurse)"getroffen sein. Für den Übertrag der Schüler für die Fachwahl kann auch "Standard mit Oberstufensynchronisation" gewählt werden. In diesem Fall werden keine Fachdaten synchronisiert, sondern nur die Schüler.
Jahrgang |Bei jeder Klasse/Jahrgang muss unter `Klasse > Zeiträume` für jeden Zeitraum das Feld "Jahrgang" mit dem Wert "11“, "12" oder "13 " angegeben werden. Das gilt nicht für Klassen mit der Klassenart "Standard mit Oberstufensynchronisation“.
Abschlussjahrgänge| Bitte legen Sie unter `Extras > Schlüsselverzeichnisse > Verordnungen` die Abschlussjahrgänge an. Es genügt dabei die Angabe des Kürzels, der Bezeichnung und der Kategorie (Abitur).
Verordnungen| Richten Sie bitte unter `Extras > Schlüsselverzeichnisse > Verordnungen` pro verwendeter Abiturverordnung oder Fachwahl eine Zeile entsprechend der Anleitung unter "Fachwahlverordnung" definieren ein.

Beim Synchronisieren extrahiert Magellan für die markierten Schüler die Fachdaten der Halbjahre E1, E2, Q1, Q2, Q3 und Q4 in das Menü `Abitur`. Dies ist die Voraussetzung für die Fachwahl-, Qualifikations- und Abschlussberechnungen der Oberstufe. Liegen noch keine Fachdaten in den Halbjahren vor, werden nur die Grunddaten des Schülers in die Ansicht `Abitur` übernommen. Vor der Eingabe der Fachwahlen in der Ansicht `Abitur > Fachwahl` sind beispielsweise noch keine Fächer beim Schüler in der Ansicht `Schüler > Zeugnis > Fächer` eingetragen.

Über die Ansicht `Abitur` unter `Start > Schüler synchronisieren...` öffnen Sie das Dialogfenster zum Synchronisieren Ihrer Daten in die Ansicht `Abitur`.
 
![Schaltfläche "Schüler synchronisieren" in der oberen Symbolleiste der Ansicht `Abitur`](/assets/images/berlin/fachwahl/fachwahl3.png)

Im Dialogfenster `Daten für Abitur synchronisieren` müssen Sie nun wie folgt vorgehen:

1. Markieren Sie alle die Schüler, die Sie in die Ansicht `Abitur` synchronisieren wollen. Klicken Sie dann auf `Weiter`.
 
![Auswahl der Schüler im Dialogfenster zum Synchronisieren der Daten in die Ansicht `Abitur`](/assets/images/berlin/fachwahl/fachwahl4.png)

2. Wählen Sie bei den weiteren Angaben die zugehörige Abturjahrgang und die entsprechende Prüfungsverordnung für das Abitur aus, die für die zuvor markierten Schüler gelten soll. Klicken Sie dann auf `Weiter`.

![Weitere Angaben im Dialogfenster zum Synchronisieren der Daten in die Ansicht `Abitur`](/assets/images/berlin/fachwahl/fachwahl5.png)

3. Klicken Sie abschließend auf `Fertigstellen`.

Die Schüler werden jetzt in die Ansicht `Abitur` synchronisiert. In der Ansicht `Abitur` finden Sie alle bereits synchronisierten Schüler in der Auswahlliste. Wenn Sie dort einen Schüler markieren und auf die Registerkarte `Fachwahl` gehen, sehen Sie dort dessen die Fachwahlinformationen.

[![Die Fachwahlinformationen für den gewählten Schüler unter `Abitur > Fachwahl`][6]][6]

## Fachwahl Layout einstellen

In der Ansicht `Abitur > Fachwahl` können Sie das Layout der dargestellten Spalten verändern, indem Sie auf die Schaltfläche `Layout anpassen` klicken.

[![Hier kann das Layout der Spalten unter `Abitur > Fachwahl` eingestellt werden][7]][7]

Im Dialogfenster `Layout anpassen` können Sie für jede Spalte bestimmen, ob diese sichtbar ist oder nicht. Spaltenüberschriften können Sie ändern, wenn Sie auf den jeweiligen Text unter Spaltenüberschrift klicken.
Wenn die Einführungsphase keinen Einfluss auf die Fachwahlprüfung hat, sollte man z.B. die Spalten "E1" und "E2" ausblenden.

## Schüler-Fachwahl eintragen

In der Ansicht `Abitur > Fachwahl` können Sie der grundsätzliche folgende Funktionen ausführen:

1. die Fachwahl des Schülers eingetragen,
2. die Fachwahl auf Basis einer Fachwahlverordnung auf Gültigkeit überprüft,
3. die gültige Fachwahl abschließend zu den Fächern des Schülers übernommen und
4. die Fachwahl an Untis übergeben.
   
Das Eintragen der Fächer für die Fachwahl kann sowohl rein manuell pro Fach erfolgen oder wesentlich komfortabler per Zuordnung von Fachwahltafeln.

## Fachwahltafeln verwenden

Mit der Verwendung von Fachwahltafeln können Sie sich die Eingabe erleichtern, indem Sie eine Fachwahltafel einem oder mehreren Schüler gleichzeitig zuweisen.

So definieren Sie eine Fachwahltafel:

1. Wählen über `Extras > Schlüsselverzeichnisse > Fachtafeln` das Verzeichnis der Fachtafeln aus.
2. Legen Sie auf der Registerkarte `Fachtafeln` über Neue Zeile eine neue Fachwahltafel an. Achten Sie dabei auf den Eintrag Fachwahltafel in der Spalte "Art".
3. Tragen Sie für die Fachwahltafel auf der Registerkarte "Fachwahltafel – Fächer" die Fächer der Fachwahltafel mit deren Eigenschaften ein.

## Empfehlung zum Anlegen einer Fachwahltafel

Die nachstehenden Hinweise eine Empfehlung, damit Sie möglichst wenig nach dem Zuweisen noch pro Schüler anpassen müssen. Zusätzlich sind für Berechnungsskripte und Zeugnisberichte bestimmte Eintragungen Voraussetzung für korrektes Funktionieren, einige Angaben können Sie hiermit bereits sicherstellen.

Eintrag|Hinweis
---|---
**Fach**|Legen Sie in der Fachwahltafel jedes in der Oberstufe wählbare Fach als nur eine Zeile an. Es gibt nur eine Zeile für Deu, nicht Deu als GK und Deu als LK usw. <br/> Das ist besonders wichtig, wenn Sie im Anschluss zum Beispiel einen Kurswahlbogen nutzen möchten, Berichte sind für eine Höchstzahl von Zeilen ausgelegt (oder erwarten genau eine Zeile für ein bestimmtes Fach), anderenfalls gelingt die korrekte Darstellung eventuell nicht mehr.
**Unterrichtsart**|Weisen Sie jedem Fach die am ehesten zutreffende Unterrichtsart zu, zum Beispiel alle Fächer erhalten die Unterrichtsart GK.
**Fachstatus**|Tragen Sie hier nur etwas ein, wenn es eine definitive Zuordung zwischen Fach und Fachstatus gibt.
**Markieren**|Legen Sie hier das häufigste Belegungsmuster fest.
**Position**|Zeugnisberichte benötigen Informationen um Fächer an der korrekten Stelle zeigen zu können. Bitte schauen Sie im Modul Magellan Berichte nach, ob für die von Ihnen eingesetzen Zeugnisberichte Vorgaben für Position pro Fach existieren und tragen Sie diese hier bitte bereits ein. 
**Q1Sprache-Q4Sprache**|Einige Zeugnisberichte geben Hinweise zu bilingualem Unterricht aus, bitte schauen vorab im Modul Magellan Berichte nach, ob das für Ihre Zeugnisse zutrifft und geben ggfs. die Information bereits hier ein. 

![Beispiel für den Inhalt einer Fachwahltafel](/assets/images/berlin/fachwahl/fachwahltafel.png)

!!! info "Hinweis"

    Wenn Sie in einer Fachzeile auf die Schaltfläche `Markieren` klicken, markieren Sie alle Halbjahre 6 Halbjahre auf einmal. Ein erneutes Anwählen der Schaltfläche `Markieren`führt zur Demarkierung aller 6 Halbjahre.

!!! info "Hinweis"

    Das Schlüsselverzeichnis `Kurssprachen` unter `Extras > Schlüsselverzeichnisse > Kurssprachen` muss mit entsprechenden Fremdsprachen gefüllt sein, damit Sie in den Spalten "Q1 Sprache", "Q2 Sprache", "Q3 Sprache" und "Q4 Sprache" einen Wert für die Unterrichtssprache auswählen können.

So weisen Sie eine Fachwahltafel Schülern in der Ansicht `Abitur` zu:

1. Wechseln Sie in die Ansicht `Abitur > Fachwahl`
2. Klicken Sie im oberen Bereich auf die Schaltfläche `Fachwahltafel zuweisen`.

[![Hier markieren Sie die Schüler, denen Sie eine Fachwahltafel zuweisen wollen.][9]][9]
 
3. Markieren Sie die Schüler, denen Sie eine Fachwahltafel zuweisen wollen und klicken Sie dann auf `Weiter`. 
4. Markieren Sie die gewünschte Fachwahltafel und ordnen Sie optional im unteren Bereich den Halbjahren die entsprechende Zeiträume zu. Sollen bei der Zuweisung der Fachwahltafeln die eventuell bereits bestehenden Fachwahlen der markierten Schüler nicht zuvor gelöscht werden, so müssen Sie das Kontrollkästchen `Vorhandene Fachwahlen der Schüler nicht löschen` markieren. Klicken Sie auf `Weiter`.

[![Wählen Sie hier die Fahlwahltafel für die markierten Schüler aus.][10]][10]

5. Geben Sie optional den zuzuordnenden Abiturjahrgang und die Fachwahlverordnung an und klicken Sie dann auf `Weiter`.

[![Ordnen Sie den markierten Schülern optional einen Abiturjahrgang und eine Fachwahlverordnung zu.][11]][11]
 
6. Klicken Sie auf `Fertigstellen`, um die Fachwahltafel den markierten Schülern zuzuordnen.

[![Darstellung unter `Abitur > Fachwahl` in der nach der Zuweisung einer Fachwahltafel für einen Schüler][12]][12]

## Schüler-Fachwahl manuell eingeben

Die Fächer der Fachwahl können auch ohne die Kopiervorlage der Fachwahltafeln dem Schüler zugeordnet werden. Dazu gehen Sie pro Fach wie folgt vor:

1. Wechseln Sie in die Ansicht `Abitur> Fachwahl`.
2. Klicken Sie im oberen Bereich auf das "+" Symbol für eine neue Zeile.

![](/assets/images/berlin/fachwahl/fachwahl13.png) 

3. Tragen Sie jetzt das Fach und optional die "Unterrichtsart" und den "Fachstatus" ein.

!!! info "Hinweis"

    Wird ein Fach manuell zugeordnet, sind in der dadurch erzeugten neuen Zeile die sichtbaren Spalten "E1" bis" Q4" automatisch markiert.

Wenn Sie die Fachwahl manuell pro Fach auf diese Weise zuordnen, müssen Sie im Unterschied zur Zuweisung per Fachwahltafel auch 

* pro Fach die Pflichtkursanzahl optional eintragen,
* pro Fach die Unterrichtsart und optional den Fachstatus eintragen,
* pro Fach festlegen, in welchen Halbjahren das Fach belegt wird sowie
* die Fachwahlverordnung festlegen 
* und Zuordnung der Halbjahre zu den die Zeiträume pro Schüler manuell vornehmen.

## Fachwahl prüfen

!!! info "Hinweis"

    Die Fachwahlüberprüfung richtet sich nach der beim Schüler unter `Fachwahl > Verordnung` eingestellten Verordnung. Die Verordnung wird durch das Fachwahlskript geprüft. Der Name des verwendeten Fachwahlskripts wird beim Schüler immer unten links ausgegeben.

Sobald Sie dem Schüler eine Fachwahlverordnung zugeordnet haben, können Sie über die Schaltfläche `Neu prüfen` die Überprüfung der Fachwahl ausführen. 

[!["Neu Prüfen" nach der Zuweisung der Fachwahlverordnung für den Schüler][14]][14]
 
Das Prüfen der Fachwahl basiert auf Eintragungen:

* der Spalte "Fach",
* der Spalte "Unterrichtsart",
* der Spalte "Fachstatus" und 
* den Markierungen der Spalten "Q1", "Q2", "Q3", "Q4".

Auf Basis der eingetragenen Fachwahl können Sie durch Wahl der Schaltfläche `Neu prüfen` diese prüfen. Das Ergebnis der Prüfung wird im oberen Bereich der Registerkarte Fachwahl angezeigt. Ist die Anzeige rot unterlegt, handelt es sich um eine (noch) nicht gültige Fachwahl. 

[![Diese Fachwahl ist noch fehlerhaft][15]][15]
 
Bei einer gültigen Fachwahl ist der obere Hinweistext grün hinterlegt mit dem HinweisFachwahl ist gültig“.

[![Diese Fachwahl istDiese Fachwahl ist gültig und weist die gültige Fachwahlkombinationsnummer 54 aus.][16]][16]
 
Mit Wahl der Schaltfläche `Neu prüfen` wird rechts `Fachwahl geprüft` angezeigt. Verändert man die Fachwahl des Schülers, wechselt der Status automatisch auf `Fachwahl nicht geprüft`.

![Dies ist die Anzeige des Prüfstatus "Fachwahl geprüft"](/assets/images/berlin/fachwahl/fachwahl17.png) 

![bzw. "Fachwahl nicht geprüft“](/assets/images/berlin/fachwahl/fachwahl18.png)

!!! info "Hinweis"

    Ist für ein eingetragenes Fach keine der Spalten "E1" bis"Q4" markiert, wird dieses Fach bei der Fachwahlprüfung als nicht gewählt betrachtet. Die Zuordnung der Zeiträume zu den Halbjahren 1 bis 6 auf der rechten Seite haben keinen Einfluss auf die Fachwahlprüfung. Sie dienen nur der späteren Zuweisung der Fahlwahlen eines Halbjahres zu den Fächern des Schülers. Das Skript prüft die Stundenbelegung. Dabei werden Leistungskurse 5-stündig, Grundkurse 3-stündig gezählt. 

## Fachwahl verändern

Wenn Sie eine Fachwahl nachträglich ändern wollen, so gelten hier die gleichen Funktionalitäten wie bei der Eintragen und Prüfung der Fachwahl. Bei einer umfangreichen Änderung der Fachwahl können Sie auch eine andere Fachwahltafel neu zuzuweisen.

## Schüler-Fachwahl als Fächer des Schülers übernehmen

Die unter Ansicht `Abitur> Fachwahl` erstellten Fachwahlen der Schüler haben keine Verbindung zu den Fächern der Schüler unter `Schüler> Zeugnis > Fächer`. Die unter `Abitur > Fachwahl` erstellten Fachwahlen der Schüler können nun zu Fächern der Schüler unter `Schüler > Zeugnis > Fächer` übernommen werden. Diese Zuweisung erfolgt immer zum aktuell eingestellten Zeitraum in Magellan.

Bei der Übernahme der Fachwahl eines Schülers werden nur die Fächer übernommen, die

* in einem der sechs Halbjahre auf der rechten Seite den aktuellen Zeitraum von Magellan zugewiesen haben und
* die in diesem Halbjahr das Kontrollkästchen markiert haben.

**Beispiel:**

In Magellan ist der aktuelle Zeitraum das 1. Halbjahr 2021/2022. Der Schüler hat die nachfolgende Fachwahl:

[![Ein Beispiel für die Fachwahl eines Schülers][19]][19]

Die Spalte "Q1" entspricht dem Zeitraum "1. Halbjahr 2021/2022“. Übernimmt man nun die Fachwahl im aktuellen Zeitraum, so werden alle Fächer der Fachwahl übernommen bis auf das Fach "PW“, da dieses in der Spalte Q1 nicht markiert ist. Auf Basis dieser Zuordnung kann nun die Zuweisung der Fachwahlen zu den Fächern der Schüler wie folgt durchgeführt werden:

1. Wechseln Sie in der Ansicht `Abitur > Fachwahl`
2. Klicken Sie im oberen Bereich auf die Schaltfläche `Fachwahl übernehmen`.

[![`Fachwahl übernehmen` aufrufen][23]][23]

3. Markieren Sie die Schüler, deren Fachwahl Sie übernehmen wollen. Standardmäßig werden Fachwahlen für einen Schüler übernommen, wenn der Schüler keine Fächer unter Ansicht `Schüler > Zeugnis > Fächer` im aktuellen Zeitraum besitzt. Soll eine Übernahme der Fachwahlen erfolgen, auch in den Fällen, in welchen der Schüler Fächer unter Ansicht `Schüler> Zeugnis > Fächer` im aktuellen Zeitraum besitzt, so müssen Sie die Option `Vorhandene Fächer in der Ansicht Schüler > Zeugnis > Fächer aktualisieren` auswählen. Sollen bei der Übernahme die eventuell bereits bestehenden Fächer der markierten Schüler nicht zuvor gelöscht werden, so müssen Sie das `Kontrollkästchen Vorhandene Fächer der Schüler nicht löschen` markieren. Klicken Sie dann auf `Weiter`.

[![Der Assistent zur Übernahme der Fachwahlen][20]][20]

4. Klicken Sie auf `Fertigstellen`, um die Fachwahlübernahme zu starten.

Die übernommen Fächer finden Sie nun auf der Registerkarte Ansicht `Schüler> Zeugnis > Fächer`.

[![Nach der Übernahme der Fachwahlen sind die Fächer in der Ansicht `Schüler > Zeugnis > Fächer`][21]][21]

!!! info "Hinweis"

    Nach der Übernahme der Fächer des Schülers aus der Fachwahl in die Ansicht `Schüler > Zeugnis > Fächer` sind noch keine Kurse zugeordnet. Dies erfolgt erst durch die Kursbildung bzw. Kursblockung in Untis. Die dort jedem Schüler zugeordneten Kurse können dann nach Magellan übertragen

## Abgleich der Fächer in der Ansicht `Abitur`

Gehen Sie bitte wie folgt vor:

1. Fachwahl im Bereich `Abitur > Fachwahl` eingeben 
2. Übergabe dieser in den Bereich `Schüler > Zeugnis > Fächer`
3. Noteneingabe im Bereich `Schüler > Zeugnis > Leistungen`
4. Synchronisieren der Fächer und Noten in den Bereich  `Abitur` durch `Schüler synchronisieren`.