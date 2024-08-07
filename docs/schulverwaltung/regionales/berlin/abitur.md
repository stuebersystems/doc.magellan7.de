# Das Abitur

[1]:/assets/images/berlin/abitur/abitur1.png
[2]:/assets/images/berlin/abitur/abitur2.png
[3]:/assets/images/berlin/abitur/abitur3.png
[4]:/assets/images/berlin/abitur/abitur4.png
[5]:/assets/images/berlin/abitur/abitur5.png
[6]:/assets/images/berlin/abitur/abitur6.png

[16]:/assets/images/berlin/abitur/abitur16.png
[17]:/assets/images/berlin/abitur/abitur17.png


## Die Abiturzulassungsüberprüfung

Die Überprüfung der Abiturzulassung gliedert sich in zwei aufeinander folgende Schritte:

1. Die Überprüfung der Leistungsfachqualifikation. Dieser Punkt entfällt ggf. je nach Bundesland.
2. Die Überprüfung der Abiturzulassung

Diese Schritte werden in den nachfolgenden Abschnitten erläutert.

[![Bereich `Abitur > Qualifikation`][1]][1]

!!! info "Hinweis"

    Überprüfen Sie, ob für den Schüler unter „Prüfungsordnung“ die korrekte Prüfungsordnung eingestellt ist bzw. wählen Sie die entsprechende aus.
    Sie können im Bereich `Abitur > Qualifikation` einzelne Spalten ausblenden bzw. die Spaltenüberschrift jeder einzelnen Spalte modifizieren. Klicken Sie dazu auf die Schaltfläche `Layout anpassen…`.

### Was soll berechnet werden?

Stellen Sie im Auswahlfeld "Status" auf `Leistungsfachqualifikation berechnen` oder `Gesamtqualifikation berechnen`. Beide Berechnungen unterscheiden sich nur darin, dass bei der Berechnung der Leistungsfachqualifikation der GK-Bereich nicht beachtet wird.

Markieren Sie anschließend die eingebrachten Kurse. Eingebrachte Kurse werden gelb markiert angezeigt. Sie können die eingebrachten Kurse manuell oder per Automatik markieren.

### Eingebrachte Kurse manuell markieren

Über die Schaltfläche `Initialisieren` wird folgendes skriptgesteuert umgesetzt:

* Es werden zunächst alle dKurse zur Eingabeerleichterung gelb, d.h. als „eingebracht“ markiert. Sie brauchen dann nur noch auf `Manuelles Markieren` zu klicken und diejenigen Kurse zu demarkieren, die nicht eingebracht werden sollen.

Markieren Sie die eingebrachten Kurse des Schülers, d.h. markieren Sie `Manuelles Markieren`, wählen Sie die Option `Kurse einbringen` und klicken Sie die entsprechenden Kurse an. Die eingebrachten Kurse werden gelb markiert.

[![Bereich `Abitur > Qualifikation`, Aufruf "Initilisieren"][16]][16]

### Die Vorschlagsautomatik

Wenn Sie auf die Schaltfläche `Vorschlag` klicken, dann werden von der Vorschlagsautomatik entsprechend der Abiturverordnung die Kurse automatisch gelb markiert, die die maximale Qualifikationspunktzahl in den ersten beiden Qualifikationsbereichen erbringen.

!!! info "Hinweis"

    Voraussetzung für die Vorschlagsautomatik ist, dass Sie über die Angaben in der Spalte „Fachstatus“ die vier Prüfungsfächer bzw. 5. Prüfungskomponente bestimmt haben.
     Die Vorschlagsautomatik des jeweiligen Skriptes generiert einen Vorschlag für die maximale Qualifikationssumme des Schülers. STÜBER SYSTEMS hat die Vorschlagsautomatik sorgfältig an die offiziellen Bestimmungen angepasst und arbeitet ggf. Novellierungen der Bestimmungen in die Skripte ein. STÜBER SYSTEMS übernimmt allerdings keine Garantie für die Richtigkeit des Vorschlags.

[![Meldungsfenster mit Information nach Ausführung der Vorschlagsautomatik][2]][2]

### Zulassung berechnen

Klicken Sie auf die Schaltfläche  `Berechnen`, um die Zulassung automatisch durch das entsprechende Skript berechnen zu lassen. Im Meldungsfenster werden die Qualifikationspunktzahl für den LK- und den GK-Bereich (letzteres nur bei „Gesamtqualifikation berechnen“) sowie evtl. Fehler angezeigt. Wenn Sie auf die Schaltfläche `Vorschlag` geklickt haben, ist das Meldungsfenster bereits geöffnet und die Qualifikation berechnet worden. Liegt die Summe beider Bereiche über der Mindestpunktzahl und sind keine weiteren Fehler ausgewiesen, dann ist die Abiturzulassung erreicht.

[![Meldungsfenster mit Fehlermeldungen zur Abiturzulassung][3]][3]


!!! info "Hinweis"

     Die Hinweise bzw. Fehlermeldungen im Meldungsfenster sind abhängig vom verwendeten Skript. Fehler führen dazu, dass die Zulassung nicht erreicht ist.
     Klicken Sie auf die Schaltfläche `Meldungen anzeigen`, wenn Sie das Meldungsfenster anzeigen wollen, ohne auf `Vorschlag` oder auf `Neu berechnen` klicken zu müssen.

[![Meldungsfenster aufrufen][17]][17]

Außerdem werden automatisch folgende Berechnungen bzw. Eingaben auf der Registerkarte „Prüfung“ durchgeführt:

* Der „Status“ wird auf „Leistungsfachqualifikation erreicht“ oder „Leistungsfachqualifikation nicht erreicht“ bzw. „Gesamtqualifikation erreicht“ oder „Gesamtqualifikation nicht erreicht“ umgesetzt.
* Die Summen der Punkte der einzelnen Halbjahre wird unter `Abitur > Qualifikaion` berechnet und in der Spalte „Summe“ angezeigt.
* Die Prüfungsfächer 1 bis 4 (bzw. 5) werden auf der unter `Abitur > Prüfung` eingetragen.
* Die Noten aus Q4 werden unter `Abitur > Prüfung` eingetragen.

### Zulassungsdaten manuell eingeben

Wenn Sie die Zulassungsdaten nicht skriptgesteuert eingeben möchten, können Sie die durch das Skript gemachten Eingaben auch selbst vornehmen:

1. Setzen Sie den „Status“ auf „Qualifikation erreicht“ oder „Qualifikation nicht erreicht“.
2. Tragen Sie die Summen je Fach in der Spalte „Summe“ auf der Registerkarte „Qualifikation“ ein.
3. Tragen Sie die Prüfungsfächer 1 bis 4 (bzw. 5) auf der Registerkarte „Prüfung“ ein.
4. Tragen Sie die Noten aus dem letzten Qualifikationshalbjahr auf der Registerkarte „Prüfung“ in der Spalte „Noten aus letztem HJ“ ein.

### Kurse nicht auf dem Zeugnisausdruck drucken

Kurse des Schülers, die nicht auf dem Abiturzeugnis erscheinen sollen, müssen Sie entsprechend markieren. Markieren Sie dazu unter `Abitur > Qualifikation` das Feld "Manuelles Markieren", wählen Sie die Option `Nicht auf Zeugnis drucken` und klicken Sie die entsprechenden Kurse an. Die ausgenommenen Kurse werden standardmäßig grau markiert.

### Bilingualer Unterrricht

Sollten Sie in der Qualifikationsphase Q1 bis Q4 auch bilingualen Unterricht haben, so können Sie die Sprache des Unterrichts gesondert eintragen. Dies kann:

* bereits bei der Fachwahl unter `Abitur > Fachwahl` erfolgen
* pro Qualifikationshalbjahr (pro Zeitraum) in der Ansicht `Schüler > Zeugnis > Fächer` in der Spalte Sprache.
* in der Qualifikationsmatrix in der Ansicht `Abitur > Qualifikation` in den Spalte Q1 Sprache, Q2 Sprache, Q3 Sprache und Q4 Sprache.
 
[![`Abitur > Qualifikation` mit eingeblendeten Spalten für bilingualen Unterricht][4]][4]

!!! info "Hinweis"

    Sollten die Spalten Q1 Sprache, Q2 Sprache, Q3 Sprache und Q4 Sprache in der Ansicht `Abitur > Qualifikation` nicht sichtbar sein, so können Sie diese Spalten über die Schaltfläche Layout anpassen anzeigen lassen.
     Kurssprachen der entsprechenden Fremdsprachen erfassen Sie über `Extras > Schlüsselverzeichnisse > Kurssprachen`, erst danach stehen Ihnen diese in den SpaltenQ1 Sprache, Q2 Sprache, Q3 Sprache und Q4 Sprache zur Auswahl.

## Der Simulationsmodus

Wenn Sie z.B. für einen Schüler die eingebrachten Kurse verändern möchten, um eine neue Einbringungsvariante durchzuspielen, können Sie dazu den Simulationsmodus in Magellan verwenden. Klicken Sie auf den Reiter `Abitur` und wählen Sie die Schaltfläche `Simulation`. Darüber öffnen Sie das Simulationsfenster. Es umfasst die Registerkarten `Qualifikation` und `Prüfung` aus dem Menü `Abitur`. Wenn Sie die Simulation beenden möchten, klicken Sie auf die Schaltfläche `Simulation beenden`. Sie werden dabei in einem Dialogfenster gefragt, ob Sie die Änderungen dauerhaft übernehmen möchten.

[![Das Dialogfenster mit dem Simulationsmodus][5]][5]

## Die Gesamtqualifikation

Die Berechnung der Gesamtqualifikation bzw. der Abiturnote wird auf der Registerkarte „Prüfung“ durchgeführt.

[![Registerkarte „Prüfung“ in der Ansicht „Abitur“][6]][6]

Die Gesamtqualifikation ergibt sich, indem zusätzlich zu der schon feststehenden Qualifikation im Leistungs- und Grundfachbereich die Qualifikation im Prüfungsbereich durch die Noten im schriftlichen und mündlichen Abitur festgestellt wird. 

Sie erfolgt in zwei Schritten:

1. Eingabe der schriftlichen Abiturnoten und Qualifikationsüberprüfung für das schriftliche Abitur
2. Eingabe der mündlichen Abiturnoten und Abiturnotenberechnung

!!! info "Hinweis"

    Einige Bundesländer haben fünf Prüfungsfächer. Standardmäßig werden 4 Prüfungsfächer angezeigt. Sie können die Anzeige auf fünf Prüfungsfächer erweitern, indem Sie auf die Schaltfläche `Layout anpassen` klicken.

### Layout anpassen

Sie können die Anzahl der angezeigten Prüfungsfächer auf fünf und die Anzahl der angezeigten Teilnoten für die besondere Lernleistung auf vier erweitern, indem Sie auf die Schaltfläche `Abiturprüfung anpassen` klicken und im entsprechenden Dialogfenster die Einstellungen machen.

### Schriftliche Prüfungsdaten eingeben

Machen Sie  auf der Registerkarte „Prüfung“ folgende Angaben:

1. Geben Sie ggf. die Noten aus dem letzten Halbjahr in die Spalte Note aus letztem Halbjahr ein. Wenn Sie auf der Registerkarte „Qualifikation“ auf `Neu berechnen` klicken, werden automatisch die angegebenen Prüfungsfächer und die Noten aus den letzten Qualifikationshalbjahr auf diese Registerkarte übertragen.
2. Geben Sie die schriftlichen Noten ein.
3. Geben Sie ggf. das Thema und die Punktzahl der besonderen Lernleistung ein.
4. Geben Sie ggf. das Fach der Fachpraxisprüfung und die entsprechende Note ein.
5. Markieren Sie die Sprachkenntnisse.
6. Kontrollieren Sie, ob der „Status“ auf „Gesamtqualifikation erreicht“ steht. Stellen Sie ihn andernfalls manuell ein. Dieser Status wird in der Regel durch `Neu berechnen` durch das Skript eingestellt.

### Prüfungsqualifikation für das schriftliche Abitur automatisch berechnen

Klicken Sie auf `Neu berechnen`, um die Qualifikation im Prüfungsbereich automatisch durch das entsprechende Skript berechnen zu lassen. Im Meldungsfenster unten werden die Qualifikationspunktzahl in den drei Bereichen, die Gesamtpunktzahl und die Durchschnittsnote angezeigt. Solange keine Note für das mündliche Prüfungsfach eingetragen wurde, wird angezeigt, welche Mindestpunktzahl in der mündlichen Prüfung erreicht werden muss, damit das Abitur bestanden ist. Wenn als Mindestpunktzahl Null angezeigt wird, ist das Abitur bereits unabhängig von der mündlichen Note bestanden. 

Außerdem werden automatisch folgende Berechnungen bzw. Zuordnungen durchgeführt:

* Der „Status“ wird auf der Registerkarte auf „Abitur bestanden“ oder „Abitur nicht bestanden“ umgesetzt.
* Die Summen für die Prüfungsfächer 1 bis 4 bzw. die 5. Prüfungskomponente werden berechnet und auf der Registerkarte eingetragen. 
* Die Gesamtpunktzahl wird auf der Registerkarte eingetragen.
* Die Durchschnittsnote wird auf der Registerkarte eingetragen.

### Abiturnote berechnen

Nach dem mündlichen Abitur tragen Sie die mündlichen Prüfungsnoten auf der Registerkarte „Prüfung“ ein. Klicken Sie danach wieder auf `Neu berechnen`, um die Abiturnote zu berechnen.

!!! info "Hinweis"

    Über die Schaltfläche „Sammelzuweisung“ können Sie mehreren Abiturienten das gleiche Konferenz- bzw. Zeugnisdatum zuweisen.

### Prüfungsqualifikationsdaten manuell eingeben

Wenn Sie die Gesamtqualifikation nicht skriptgesteuert eingeben möchten, können Sie die durch das Skript gemachten Eingaben auch selbst vornehmen:

1. Setzen Sie den „Status“ auf `Abitur bestanden` oder `Abitur nicht bestanden` um.
2. Geben Sie die Summen für die Prüfungsfächer 1 bis 4 bzw. die 5. Prüfungskomponente ein.
3. Geben Sie die Gesamtpunktzahl ein.
4. Geben Sie die Durchschnittsnote ein.

### Zeugnisbemerkungen eingeben

Geben Sie unter `Abitur > Zeugnisbemerkungen` evtl. Zeugnisbemerkungen ein, die auf dem Abiturzeugnis gedruckt werden sollen. Sie können die Zeugnisbemerkung eintippen, auf das Verzeichnis Zeugnisbemerkungen zugreifen und die Rechtschreibprüfung nutzen.

## Informationen über Zeugnisse

Wir beschreiben die notwendigen Eingaben für unsere Zeugnisse und Berichte im Abschnitt [Berichte](https://doc.la.stueber.de/berichte/01_uebersicht/) der Magellan Landesanpassungen.

## Oberstufenzeugnisse

Bei der Ausgabe der Zeugnisse in der Oberstufe muss man zwischen zwei Arten von Zeugnissen unterscheiden:

* **Zeugnisse des aktuellen Zeitraums:** Hierbei handelt es sich um Halbjahres- oder Jahreszeugnisse wie z.B. das Zeugnis der Qualifikationsphase Q1 oder der Qualifikationsphase 2. Sie beziehen sich immer auf den aktuell eingestellten Zeitraum in Magellan. 
* **Zeugnisse über mehrere Zeiträume:** Diese Zeugnisse beziehen sich auf Daten aus mehreren Zeiträumen. Im Fall der Oberstufe werden diese Daten im Bereich „Abitur“ in Magellan eingetragen. Beispiele für zeitraumübergreifende Zeugnisse sind das Fachhochschul- oder das Abiturzeugnis.

### Zeugnisse des aktuellen Zeitraums

Die Ausgabe der Zeugnisse des aktuellen Zeitraums erfolgt analog zum Drucken von Standardzeugnissen in Magellan.

### Zeugnisse über mehrere Zeiträume

Klicken Sie bei den Abiturdaten des Schülers auf die Registerkarte `„Abiturzeugnis“`, um die Zeugnisbemerkungen anzugeben. Zusammen mit den Angaben auf den Registerkarten `Abiturzulassung` und `Abiturprüfung` verfügen Sie dann über alle Daten, um zeitraumübergreifende Zeugnisse wie das Abiturzeugnis auszudrucken. 

So drucken Sie Abitur-, Fachhochschulzeugnisse, Punktekreditkarten:

1. Markieren Sie in der Liste der Schüler der Oberstufe per Mausklick oder mit Umschalt+Mausklick oder Strg+Mausklick die entsprechenden Schüler. 
2. Klicken Sie auf `Bearbeiten` und `Drucken` und wählen Sie das Zeugnisformular und klicken Sie auf `Drucken`.
Optional können Sie auch über das Schüler-Formular drucken, indem Sie wie bei den Zeugnissen des aktuellen Zeitraums den Schüler in der Auswahlliste markieren.

## Beispiele für Berichte der Oberstufe

In den nachfolgenden Abbildungen finden Sie Beispiele für Crystal Reports Berichte in der Oberstufe.

### 1. Seite des Crystal Reports Berichts für den  Berechnungsbogen mit 5. Prüfungskomponente gem. VO-GO

![1. Seite des Crystal Reports Berichts für den  Berechnungsbogen mit 5. Prüfungskomponente gem. VO-GO](/assets/images/berlin/abitur/abitur7.png)

### 2. Seite des Crystal Reports Berichts für den  Berechnungsbogen mit 5. Prüfungskomponente gem. VO-GO

![2. Seite des Crystal Reports Berichts für den  Berechnungsbogen mit 5. Prüfungskomponente gem. VO-GO](/assets/images/berlin/abitur/abitur8.png)

### 1. Seite eines Crystal Reports Berichts für eine Kursliste

![1. Seite eines Crystal Reports Berichts für eine Kursliste ](/assets/images/berlin/abitur/abitur9.png)

### 1. Seite des Crystal Reports Berichts für den Übersichtsplan über die Schullaufbahn ab 2010 – 12jähriger Bildungsgang (VO-GO)

![ 1. Seite des Crystal Reports Berichts für den Übersichtsplan über die Schullaufbahn ab 2010 – 12jähriger Bildungsgang (VO-GO)](/assets/images/berlin/abitur/abitur10.png)

### 2. Seite des Crystal Reports Berichts für den Übersichtsplan über die Schullaufbahn ab 2010 – 12jähriger Bildungsgang (VO-GO)

![2. Seite des Crystal Reports Berichts für den Übersichtsplan über die Schullaufbahn ab 2010 – 12jähriger Bildungsgang (VO-GO)](/assets/images/berlin/abitur/abitur11.png)

### Crystal Reports Berichts für das Zeugnis des 1. Kurshalbjahr der gymnasialen Oberstufe]

![ Crystal Reports Berichts für das Zeugnis des 1. Kurshalbjahr der gymnasialen Oberstufe](/assets/images/berlin/fachwahl/fachwahl12.png)

### 1. Seite eines Crystal Reports Berichts für ein Abiturzeugnis

![1. Seite eines Crystal Reports Berichts für ein Abiturzeugnis](/assets/images/berlin/abitur/abitur13.png)

### 2. Seite eines Crystal Reports Berichts für ein Abiturzeugnis

![2. Seite eines Crystal Reports Berichts für ein Abiturzeugnis](/assets/images/berlin/abitur/abitur14.png)

### 3. Seite eines Crystal Reports Berichts für ein Abiturzeugnis

![3. Seite eines Crystal Reports Berichts für ein Abiturzeugnis](/assets/images/berlin/abitur/abitur15.png)