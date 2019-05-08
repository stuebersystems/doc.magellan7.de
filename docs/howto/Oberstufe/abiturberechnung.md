# Die Abiturberechnung

In diesem Abschnitt beschreiben wir Ihnen die Funktionalitäten der Unterkarten `Qualifikation`, `Prüfung` und `Zeugnis`.

Folgende Aktionen werden auf diesen Karten abgebildet:

1. Zulassung zur 12 überprüfen (nur in einigen Bundesländern)
2. Abiturzulassung überprüfen
3. Gesamtqualifikation für schriftlichen Prüfungsbereich (Abiturnote) berechnen
4. Fachhochschulreife berechnen
5. Zeugnisbemerkungen eingeben und Zeugnisse drucken

##  Schüler ins Menü Abitur synchronisieren

![Dialogfenster zum Synchronisieren der Daten für das Abitur](../assets/images/gym_oberstufe/gym_oberstufe03.png)

Bevor Sie die Abiturqualifikationen überprüfen können, müssen Sie die Daten der Schüler synchronisieren, indem Sie in MAGELLAN auf `Abitur` klicken und dann auf die Schaltfläche `Schüler synchronisieren` im MAGELLAN-Fenster klicken.

|Beim Synchronisieren prüft MAGELLAN die `Klassenart` unter `Klasse > Daten`|
|--|
|** Oberstufenjahrgang (Leistungs- und Grundkurse)** <br/> **Oberstufenjahrgang (nur Kurse)**<br/><br/>MAGELLAN synchronisiert die Schülerdaten, Schülerfachdaten und in den Halbjahren erfassten Leistungen.|
|** Standard mit Oberstufensynchronisation**<br/><br/>MAGELLAN synchronisiert die Schülerdaten als Voraussetzung für die Fachwahl, keine Fächer oder Leistungen. In der Regel trägt man diese Klassenart für den Jahrgang 10 ein, da die Schüler sich in der Jahrgangsstufe 10 für die Fachwahl in der Oberstufe entscheiden.



!!! info "Hinweis"

	 MAGELLAN extrahiert für die markierten Schüler die Fachdaten der Halbjahre 11/1 bis 13/2 (bei G9) bzw. 10/1 bis 12/2 (bei G8) und ordnet die Daten in den Spalten E1 bis Q4 auf der Qualifikationskarte im Menü Abitur an. 
      Ob die Schülerdaten passend nach dem G8- oder G9-System angeordnet werden, legen Sie im Verzeichnis `Verordnungen` in der Spalte `Jahrgang` an. Was genau Sie dort eintragen, beschreiben wir pro Berechnungsskript in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/).


![Klassenart für die Oberstufenberechnungen](../assets/images/gym_oberstufe/oberstufe02.png)


## Die Abiturzulassungsüberprüfung

Die Überprüfung der Abiturzulassung gliedert sich in zwei aufeinander folgende Schritte:

1. Die Überprüfung der Leistungsfachqualifikation. Dieser Punkt entfällt ggf. je nach Bundesland.
2. Die Überprüfung der Abiturzulassung

Diese Schritte werden in den nachfolgenden Abschnitten erläutert.

![Registerkarte `Qualifikation` in der Ansicht „Abitur“](../assets/images/gym_oberstufe/gym_oberstufe14.png)

!!! info "Hinweis"

	Überprüfen Sie, ob für den Schüler unter „Prüfungsordnung“ die korrekte Prüfungsordnung eingestellt ist bzw. wählen Sie die entsprechende aus.

Sie können auf der Registerkarte `Qualifikation` einzelne Spalten ausblenden bzw. die Spaltenüberschrift jeder einzelnen Spalte modifizieren. Klicken Sie dazu auf die Schaltfläche `Layout anpassen…`.

### Was soll berechnet werden?

Stellen Sie den `Status` auf `LK-Qualifikation berechnen` oder `Gesamtqualifikation berechnen`. Beide Berechnungen unterscheiden sich nur darin, dass bei der Berechnung der LK-Qualifikation der GK-Bereich nicht beachtet wird. Markieren Sie anschließend die eingebrachten Kurse. Eingebrachte Kurse werden gelb markiert angezeigt. Sie können die eingebrachten Kurse manuell oder per Automatik (Schaltfläche `Vorschlag`) markieren.

### Eingebrachte Kurse manuell markieren

Klicken Sie auf `Initialisieren`. Entsprechend des Skripts geschieht beim Initialisieren Folgendes:

Es werden für jeden Kurs automatisch die Halbjahre grau markiert, die für die Abiturzulassung nicht relevant sind. Diese Funktion ist abhängig vom jeweiligen Skript.
Alle anderen Halbjahre des jeweiligen Kurses werden zur Eingabeerleichterung gelb, d.h. „eingebracht“ markiert. Sie brauchen dann nur noch auf `Manuelles Markieren` zu klicken und diejenigen Kurse zu demarkieren, die nicht eingebracht werden sollen.

Markieren Sie die eingebrachten Kurse des Schülers, d.h. markieren Sie `Manuelles Markieren`, wählen Sie die Option `Kurse einbringen` und klicken Sie die entsprechenden Kurse an. Die eingebrachten Kurse werden gelb markiert.


### Die Vorschlagsautomatik

Wenn Sie auf `Vorschlag `klicken, dann werden von der Vorschlagsautomatik entsprechend der Abiturverordnung die Kurse automatisch gelb markiert, die die maximale Qualifikationspunktzahl in den ersten beiden Qualifikationsbereichen erbringen.

!!! info "Hinweis"

	Voraussetzung für die Vorschlagsautomatik ist, dass Sie über die Angaben in der Spalte „Fachstatus“ die vier - bzw. in einigen Bundesländern fünf - Prüfungsfächer bestimmt haben.
     Die Vorschlagsautomatik des jeweiligen Skriptes generiert einen Vorschlag für die maximale Qualifikationssumme des Schülers. 
     STÜBER SYSTEMS hat die Vorschlagsautomatik sorgfältig an die offiziellen Bestimmungen angepasst und arbeitet ggf. Novellierungen der Bestimmungen in die Skripte ein. 
     STÜBER SYSTEMS übernimmt allerdings keine Garantie für die Richtigkeit des Vorschlags.

### Zulassung berechnen

Klicken Sie auf `Neu berechnen`, um die Zulassung automatisch durch das entsprechende Skript berechnen zu lassen. Im Meldungsfenster werden die Qualifikationspunktzahl für den LK- und den GK-Bereich (letzteres nur bei `Gesamtqualifikation berechnen`) sowie evtl. Fehler angezeigt. Wenn Sie auf `Vorschlag `geklickt haben, ist das Meldungsfenster bereits geöffnet und die Qualifikation berechnet worden. Liegt die Summe beider Bereiche über der Mindestpunktzahl und sind keine weiteren Fehler ausgewiesen, dann ist die Abiturzulassung erreicht.

![Meldungsfenster mit Fehlermeldungen zur Abiturzulassung](../assets/images/gym_oberstufe/gym_oberstufe15.png)

Die Hinweise bzw. Fehlermeldungen im Meldungsfenster sind abhängig vom verwendeten Skript. Fehler führen dazu, dass die Zulassung nicht erreicht ist.

!!! info "Hinweis"

	 Klicken Sie auf die Schaltfläche `Meldungen anzeigen`, wenn Sie das Meldungsfenster anzeigen wollen, ohne auf `Vorschlag` oder auf `Neu berechnen` klicken zu müssen.

Außerdem werden automatisch folgende Berechnungen bzw. Eingaben auf der Registerkarte `Prüfung` durchgeführt:

* Der „Status“ wird auf „Leistungsfachqualifikation erreicht“ oder „Leistungsfachqualifikation nicht erreicht“ bzw. „Gesamtqualifikation erreicht“ oder „Gesamtqualifikation nicht erreicht“ umgesetzt.

* Die Summen der Punkte der einzelnen Halbjahre auf der Registerkarte `Qualifikation` werden berechnet und in der Spalte „Summe“ angezeigt.

* Die Prüfungsfächer 1 bis 4 (bzw. 5) werden auf der Registerkarte `Prüfung` eingetragen.

* Die Noten aus 13 werden auf der Registerkarte `Prüfung` eingetragen.

### Zulassungsdaten manuell eingeben

Wenn Sie die Zulassungsdaten nicht skriptgesteuert eingeben möchten, können Sie die durch das Skript gemachten Eingaben auch selbst vornehmen:

1. Setzen Sie den „Status“ auf „Qualifikation erreicht“ oder „Qualifikation nicht erreicht“.

2. Tragen Sie die Summen je Fach in der Spalte „Summe“ auf der Registerkarte `Qualifikation` ein.

3. Tragen sie die Prüfungsfächer 1 bis 4 (bzw. 5) auf der Registerkarte `Prüfung` ein.

4. Tragen Sie die Noten aus 13 auf der Registerkarte `Prüfung` ein.

### Kurse nicht auf dem Zeugnisausdruck drucken

Kurse des Schülers, die nicht auf dem Abiturzeugnis erscheinen sollen, müssen Sie entsprechend markieren. Markieren Sie dazu `Manuelles Markieren`, wählen Sie die Option `Nicht auf Zeugnis drucken` und klicken Sie die entsprechenden Kurse an. Die ausgenommenen Kurse werden standardmäßig grau markiert.

> #### primary::Hinweis
>
> Die Farben in der Oberstufe im Menü „Abitur“ sind individuell einstellbar. Unter `Abitur > Farben…` legen Sie fest, welche Hintergrundfarben in der Ansicht verwendet werden sollen.

## Simulationsmodus

Wenn Sie z.B. für einen Schüler die eingebrachten Kurse verändern möchten, um eine neue Einbringungsvariante durchzuspielen, können Sie dazu den Simulationsmodus in MAGELLAN verwenden. Klicken Sie auf `Abitur > Simulation` oder die entsprechende Schaltfläche oben in der Symbolleiste, um das Simulationsfenster zu öffnen. Das Simulationsfenster umfasst die Registerkarten `Qualifikation` und `Prüfung`. Wenn Sie die Simulation beenden möchten, klicken Sie auf die Schaltfläche `Simulation beenden`. Sie werden dabei in einem Dialogfenster gefragt, ob Sie die Änderungen dauerhaft übernehmen möchten.

## Die Gesamtqualifikation

Die Berechnung der Gesamtqualifikation bzw. der Abiturnote wird auf der Registerkarte `Prüfung` durchgeführt.

![Registerkarte `Prüfung` in der Ansicht „Abitur“](../assets/images/gym_oberstufe/gym_oberstufe16.png)

Die Gesamtqualifikation ergibt sich, indem zusätzlich zu der schon feststehenden Qualifikation im Leistungs- und Grundfachbereich die Qualifikation im Prüfungsbereich durch die Noten im schriftlichen und mündlichen Abitur festgestellt wird. Sie erfolgt in zwei Schritten:

1. Eingabe der schriftlichen Abiturnoten und Qualifikationsüberprüfung für das schriftliche Abitur
2. Eingabe der mündlichen Abiturnoten und Abiturnotenberechnung

!!! info "Hinweis"

	Einige Bundesländer haben fünf Prüfungsfächer. Standardmäßig werden 4 Prüfungsfächer angezeigt. Sie können die Anzeige auf fünf Prüfungsfächer erweitern, indem Sie auf die Schaltfläche `Layout anpassen` klicken.

### Layout anpassen

Sie können die Anzahl der angezeigten Prüfungsfächer auf fünf und die Anzahl der angezeigten Teilnoten für die besondere Lernleistung auf vier erweitern, indem Sie das Fenster `Abiturprüfung anpassen`  über die Schaltfläche `Layout anpassen` aufrufen und im entsprechenden Dialogfenster die Einstellungen machen.

### Schriftliche Prüfungsdaten pro Schüler oder pro Fach und Lehrer eingeben

Für die Eingabe der schriftlichen Prüfungsnoten stehen Ihnen zwei Varianten zur Auswahl: Sie tragen die Noten pro Schüler unter `Abitur > Prüfungen` ein oder Sie nutzen den Assistenten `Schriftliche Prüfungsnoten...`.

Für die Eingabe pro Schüler machen Sie auf der Registerkarte `Prüfung` folgende Angaben:

1. Geben Sie ggf. die Noten aus 13 ein. Wenn Sie auf der Registerkarte `Qualifikation` auf Neu berechnen klicken, werden automatisch die angegebenen Prüfungsfächer und die Noten aus 13 auf diese Registerkarte übertragen.

2. Geben Sie die schriftlichen Noten ein.

3. Geben Sie ggf. das Thema und die Punktzahl der besonderen Lernleistung ein.

4. Geben Sie ggf. das Fach der Fachpraxisprüfung und die entsprechende Note ein.

5. Markieren Sie die Sprachkenntnisse.

6. Kontrollieren Sie, ob der „Status“ auf „Gesamtqualifikation erreicht“ steht. Stellen Sie ihn andernfalls manuell ein. Dieser Status wird in der Regel durch Neu berechnen durch das Skript eingestellt.



Für die Eingabe mit Hilfe des Assistenten `Schriftliche Prüfungsnoten...` gehen Sie bitte wie folgt vor:

1. Lösen Sie bitte unter `Abitur > Qualifikation` den Punkt `Neu Berechnen` aus, damit die Prüfungsfächer vorbelegt sind

2. Starten Sie den Assistenten unter `Abitur > Prüfung > Schriftliche Prüfungsnoten`

3. Wählen Sie ein Prüfungsfach aus, die Fächer werden nach den unterrichtenden Lehrern getrennt aufgelistet.

![Auswahl des Faches](../assets/images/gym_oberstufe/gym_oberstufe17.png)

Ihnen werden alle Schüler gezeigt, die dieses Fach als Prüfungsfach beim gleichen Lehrer haben. Für die Eingabe kann nach der Unterrichtsart und dem Fachstatus gefiltert werden.

![Eingabeliste für die schriftlichen Prüfungsnoten](../assets/images/gym_oberstufe/gym_oberstufe18.png)

Spalte|Bedeutung
--|--
Spalte Note|Wenn für Schüler bereits schriftliche Prüfungsnoten für dieses Fach erfasst wurden, werden diese in der Spalte Note gezeigt. Ändern Sie diese Note, wird sie nach dem Beenden des Assistenten auf der Karte Prüfung als schriftliche Note gezeigt.
Spalten Prüfer1 und Prüfer2| Nutzen Sie diese beiden Spalten um eine höhere Genauigkeit für die Notenerfassung zu erzielen. Lassen Sie dazu Ihre Prüfer die Noten jeweils in die Spalten Prüfer1 und Prüfer2 eintragen – die Spalte Note wird nur gefüllt, wenn beide Noten identisch sind. Beide Spalten lassen sich jeweils Layout anpassen ein- oder ausblenden.

### Die besondere Lernleistung

Geben Sie auf der Registerkarte `Prüfung` das Fach (nur bestimmte Bundesländer), Thema und Punktzahl der besonderen Lernleistung ein, falls eine vorliegt. Die Anzahl der Bewertungen können Sie ggf. (je nach Bundesland) auf maximal vier Punktzahlen erweitern (siehe „Layout anpassen“). Markieren Sie „Lernleistung einbringen“, falls die Lernleistung eingebracht werden soll. Wenn Sie auf „Neu berechnen“ klicken, um die Prüfungsqualifikation zu berechnen, prüft das Skript automatisch, ob eine besondere Lernleistung vorliegt und ob es besser wäre, die Lernleistung einzubringen oder nicht. Ggf. wird ein Hinweis im Meldungsfenster ausgegeben, der Sie darauf hinweist, die Lernleistung besser einzubringen bzw. nicht einzubringen.

### Fachpraxisprüfung

Geben Sie auf der Registerkarte `Prüfung` das Fach und die Note der Fachpraxisprüfung ein, falls eine vorliegt (z.B. in Rheinland-Pfalz).

### Prüfungsqualifikation für das schriftliche Abitur automatisch berechnen

Klicken Sie auf `Neu berechnen`, um die Qualifikation im Prüfungsbereich automatisch durch das entsprechende Skript berechnen zu lassen. Im Meldungsfenster unten werden die Qualifikationspunktzahl in den drei Bereichen, die Gesamtpunktzahl und die Durchschnittsnote angezeigt. Solange keine Note für das mündliche Prüfungsfach eingetragen wurde, wird angezeigt, welche Mindestpunktzahl in der mündlichen Prüfung erreicht werden muss, damit das Abitur bestanden ist. Wenn als Mindestpunktzahl Null angezeigt wird, ist das Abitur bereits unabhängig von der mündlichen Note bestanden. Außerdem werden automatisch folgende Berechnungen bzw. Zuordnungen durchgeführt:

* Der „Status“ wird auf der Registerkarte auf „Abitur bestanden“ oder „Abitur nicht bestanden“ umgesetzt.

* Die Summen für die Prüfungsfächer 1 bis 4 werden berechnet und auf der Registerkarte eingetragen.

* Die Gesamtpunktzahl wird auf der Registerkarte eingetragen.

* Die Durchschnittsnote wird auf der Registerkarte eingetragen.

### Abiturnote berechnen

Nach dem mündlichen Abitur tragen Sie die mündlichen Prüfungsnoten auf der Registerkarte `Prüfung` ein. Klicken Sie danach wieder auf `Neu berechnen`, um die Abiturnote zu berechnen.

!!! info "Hinweis"

	Über die Schaltfläche „Sammelzuweisung“ können Sie mehreren Abiturienten das gleiche Konferenz- bzw. Zeugnisdatum zuweisen.

### Prüfungsqualifikationsdaten manuell eingeben

Wenn Sie die Gesamtqualifikation nicht skriptgesteuert eingeben möchten, können Sie die durch das Skript gemachten Eingaben auch selbst vornehmen:

1. Setzen Sie den „Status“ auf Abitur bestanden oder Abitur nicht bestanden um.
2. Geben Sie die Summen für die Prüfungsfächer 1 bis 4 ein.
3. Geben Sie die Gesamtpunktzahl ein.
4. Geben Sie die Durchschnittsnote ein.

### Zeugnisbemerkungen eingeben

Geben Sie auf der Registerkarte „Zeugnis“ evtl. Zeugnisbemerkungen ein, die auf dem Abiturzeugnis gedruckt werden sollen. Sie können die Zeugnisbemerkung eintippen, auf das Verzeichnis Zeugnisbemerkungen zugreifen und die Rechtschreibprüfung nutzen. Bitte lesen Sie dazu auch den Abschnitt [Zeugnisbemerkungen](https://doc.magellan6.stueber.de/howto/zeugnisdaten.html#zeugnisbemerkungen).

## Oberstufenzeugnisse

Bei der Ausgabe der Zeugnisse in der Oberstufe muss man zwischen zwei Arten von Zeugnissen unterscheiden:
Zeugnisse des aktuellen Zeitraums: Hierbei handelt es sich um Halbjahres- oder Jahreszeugnisse wie z.B. das Zeugnis der Jahrgangsstufe 12/1 oder der Jahrgangsstufe 12/2. Sie beziehen sich immer auf den aktuell eingestellten Zeitraum in MAGELLAN.

Zeugnisse über mehrere Zeiträume: Diese Zeugnisse beziehen sich auf Daten aus mehreren Zeiträumen. Im Fall der Oberstufe werden diese Daten im Bereich „Abitur“ in MAGELLAN eingetragen. Beispiele für zeitraumübergreifende Zeugnisse sind das Fachhochschul-, das Abiturzeugnis oder die Punktekreditkarte.

### Zeugnisse des aktuellen Zeitraums

Die Ausgabe der Zeugnisse des aktuellen Zeitraums erfolgt analog zum Drucken von Standardzeugnissen in MAGELLAN. Die Eingabe der für den Zeugnisausdruck relevanten Daten des Schülers entspricht dem Vorgehen aus Kapitel [Zeugnisdaten erfassen](https://doc.magellan6.stueber.de/howto/zeugnisdaten.html#zeugnisdaten-erfassen).

### Zeugnisse über mehrere Zeiträume

Klicken Sie bei den Abiturdaten des Schülers auf die Registerkarte `Zeugnis`, um die Zeugnisbemerkungen anzugeben. Zusammen mit den Angaben auf den Registerkarten `Qualifikation` und `Prüfung` verfügen Sie dann über alle Daten, um zeitraumübergreifende Zeugnisse wie das Abiturzeugnis auszudrucken. So drucken Sie Abitur-, Fachhochschulzeugnisse, Punktekreditkarten:

1. Markieren Sie in der Liste der Schüler der Oberstufe per Mausklick oder mit Umschalt+Mausklick oder Strg+Mausklick die entsprechenden Schüler.

2. Klicken Sie auf `Bearbeiten` und `Drucken `und wählen Sie das Zeugnisformular und klicken Sie auf `Drucken`.