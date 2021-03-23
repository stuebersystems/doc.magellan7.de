# Die Berufsschulmatrix

Für die Berufsschule existieren unterschiedliche Berechnungsvorschriften für die Noten auf Jahres-, Abgangs- und Abschlusszeugnissen. MAGELLAN stellt sehr ausgefeilte Funktionen für die gesamte Endnotenberechnung der Berufsschule zur Verfügung. Diese Notenberechnungen werden mit den grundlegenden Merkmalen in diesem Kapitel vorgestellt. 

!!! info "Hinweis"

	Eine ausführliche Beschreibung der zeitraumübergreifenden Berechnungen in der Berufsschule finden Sie im entsprechenden Kapitel in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/). Dort können Sie auch nachlesen, für welche Bundesländer entsprechende Berechnungsskripte vorliegen. In diesem Handbuch werden nur die wichtigsten Schritte erläutert.

## Grundlagen

In der Berufsschule sind verschiedene Arten von Zeugnissen zu unterscheiden. Verlässt der Schüler die Klasse vorzeitig, so erhält er ein Abgangszeugnis. Verlässt er die Klasse erfolgreich zum Abschluss seiner Ausbildung, so erhält er ein Abschlusszeugnis. 

Die Halbjahres-, Zwischen- und Jahreszeugnisse des Schülers zum Ende eines Halbjahres beziehen sich fast ausschließlich auf die Noten des aktuellen Zeitraums. In diesem Fall greift ein Zeugnisbericht immer auf die Noten des aktuellen Zeitraums zu. Die Noten der Schüler werden dann in MAGELLAN pro Schüler unter den Leistungen auf der Registerkarte `Zeugnis` eingetragen (siehe [Zeugnisdaten erfassen](https://doc.magellan7.stueber.de/schulverwaltung/howto/zeugnisdaten/)). 

Bei den meisten Abgangs- bzw. Abschlusszeugnissen werden die Noten auf der Basis der Noten der einzelnen Schuljahre festgelegt. Dies erfolgt durch ein vorgegebenes Berechnungsschema, bei dem Noten sowohl innerhalb eines Schuljahres als auch im Verhältnis der Schuljahre zueinander berechnet werden. Diese Berechnungen erfolgen aufgrund der MAGELLAN-Scripting-Technologie ( [MAGELLAN Scripting](https://doc.magellan7-toolbox.stueber.de/scripting/)). 

Für die Gegenüberstellungen der Noten und deren Abschlussberechnung gibt es in MAGELLAN den gesonderten Bereich `Berufsschule`, der eine entsprechende Berufsschulmatrix beinhaltet. Dieser Bereich ist zunächst leer und muss durch ein Synchronisieren mit Schülern des aktuellen Zeitraums gefüllt werden. Im Rahmen der Synchronisation werden alle Fächer und Noten der Schüler aus den vorangegangenen Schuljahren der Klasse mit übertragen, so dass in der Berufsschulmatrix nur noch die Berechnung durchgeführt werden muss. 

Alternativ können auch nur die Schüler übertragen werden und die Fächer und Noten werden direkt in der Berufsschulmatrix eingetragen. Dies macht z.B. dann Sinn, wenn Sie MAGELLAN erst ein Jahr einsetzen und die anderen Noten von Jahren zuvor nachtragen wollen. Auf Basis der berechneten Endnoten können Sie dann die eigentlichen Zeugnisse ausdrucken. Dabei kann jede berechnete Endnote auch noch manuell aufgrund des pädagogischen Freiraums abgeändert werden. Die zeitraumübergreifenden Endnotenberechnungen basieren auf MAGELLAN-Skripten, die Sie mit Hilfe des MAGELLAN-Skripteditors bearbeiten können (siehe [MAGELLAN-Skripteditor](https://doc.magellan7-toolbox.stueber.de/scripting/skripteditor/))

## Vorbereitungen

Zur zeitraumübergreifenden Endnotenberechnung der Berufsschule und dem anschließenden Zeugnisdruck gehören folgende Aufgaben:

1. Berufsschulklassen und andere Stammdaten einrichten
2. Fächer und Noten der Schüler pro Zeitraum einer Zeugnisausgabe eingeben
3. Endnoten für Abgangs- bzw. Abschlusszeugnisse berechnen
4. Zeugnisbemerkungen eingeben und Zeugnisse drucken

Alle Schritte werden in MAGELLAN ausgeführt. Die Aufgaben 1 und 2 sind schon allgemein in den vorangegangenen Kapiteln ausführlich erläutert werden. Es werden daher nur die Besonderheiten für die Aufgaben 3 und 4 vorgestellt. Für die Vorbereitung der Endnotenberechnung müssen Sie folgende Daten definieren.

1. Abschlussjahrgang definieren
2. Berechnungsverordnung definieren

### Abschlussjahrgang definieren
 
 ![Hier definieren Sie die Abschlussjahrgänge.](/assets/images/berufsschulmatrix/berufsschulmatrix1.png)

Sie können in MAGELLAN unter `Extras > Schlüsselverzeichnisse > Abschlussjahrgänge` Abschlussjahrgänge definieren. Damit können Sie jedem Schüler in der Rubrik `Berufsschule` den entsprechenden Abschlussjahrgang zuordnen. Dieser Vermerk hat keinen Einfluss auf Abschlussnotenberechnungen, sondern dient dazu, später alle Schüler eines bestimmten Abschlussgangs z.B. für Ausdrucke herausfiltern zu können und die Art der zu synchronisierenden Noten festzulegen. 

* Die Art der zu synchronisierenden Noten des Abschlussjahrganges legen Sie über die Kategorie fest

* Wählen Sie die Kategorie „Berufsschule (Jahresnoten)“ um später beim Synchronisieren der Schüler nur die Noten des jeweils 2. Halbjahres in die Ansicht `Berufsschule` zu übertragen.

* Wählen Sie die Kategorie „Berufsschule (Halbjahresnoten)“ um später beim Synchronisieren der Schüler die Noten des jeweils 1. und 2. Halbjahres in die Ansicht `Berufsschule` zu übertragen.

### Berechnungsverordnung definieren
 

![Dies ist das Verzeichnis der Verordnungen](/assets/images/berufsschulmatrix/berufsschulmatrix2.png)

Sie müssen für jeden Schüler die Berechnungsverordnung angeben, die für ihn relevant ist. Dazu müssen Sie im Schlüsselverzeichnis `Verordnungen` die jeweilige Berechnungsverordnung definieren. Klicken Sie dazu auf `Extras > Schlüsselverzeichnisse > Verordnungen` und geben Sie dort die Verordnung wie folgt an:

Spalte      | Bedeutung
----------- | ---------
Kürzel      | Kurzbezeichnung der Verordnung (max. 8stellig)
Bezeichnung | Bezeichnung der Verordnung
Kategorie   | Wenn Sie hier `Berufsschule` eingeben, wird die Verordnung bei den Schüler-Berufsschuldaten angezeigt
Gültig von  | Gültigkeitsdatum von, ohne Bedeutung für die Berechnungen
Gültig bis  | Gültigkeitsdatum bis, ohne Bedeutung für die Berechnungen
Skript      | Geben Sie hier den Namen des Skripts für diese Berechungsverordnung ein. Alle verfügbaren Skripte befinden sich im MAGELLAN-Verzeichnis SKRIPTE.

!!! info "Hinweis"

	Die erwarteten Einstellungen pro Berechnungsskript beschreiben wir in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/).

## Schüler synchronisieren

Nach den Vorbereitungen müssen alle Schüler, deren Abschluss- bzw. Abgangsnoten berechnet werden sollen, synchronisiert werden. Klicken Sie dazu auf Ansicht `Berufsschule`. Danach müssen Sie auf die Schaltfläche `Schüler synchronisieren` oben im MAGELLAN-Fenster klicken.
 
![Dialog Schüler synchronisieren](/assets/images/berufsschulmatrix/berufsschulmatrix3.png)

Beim Synchronisieren geschieht Folgendes: 
MAGELLAN extrahiert für die markierten Schüler die Fachdaten der Noten der Grundstufe, Fachstufe 1, Fachstufe 2 bzw. Fachstufe 3. Besitzt der ausgewählt Abschlussjahrgang die Kategorie „Berufsschule (Jahresnoten)“, werden nur die Noten der jeweiligen 2. Halbjahre (=Jahresnoten) extrahiert. Besitzt der ausgewählt Abschlussjahrgang die Kategorie „Berufsschule (Halbjahresnoten)“, werden die Noten des 1. und 2. Halbjahres extrahiert. 

Dies ist die Voraussetzung dafür, dass die Abschlussberechnungen der Berufsschule durchgeführt werden können. Auch wenn Sie zuvor keine Fächer bzw. Noten in den Halbjahren des Schülers angegeben haben, müssen Sie diese Synchronisation einmal ausführen. Damit die Schüler mit allen Fächern, Noten und Faktoren aus den einzelnen Halbjahren korrekt übernommen werden können, sind folgende Angaben in MAGELLAN notwendig:

* **Zeiträume:** Im Verzeichnis der Zeiträume muss das Feld „Art“ mit dem Wert „1. Halbjahr“ bzw. „2. Halbjahr“ gefüllt sein.

* **Jahrgang:** Bei jeder Klasse der Berufsschule muss auf der Registerkarte „Zeiträume“ für jeden Zeitraum  das Feld Jahrgang mit dem Wert „1“ (=Grundstufe), „2“ (=Fachstufe 1), „3“ (=Fachstufe 2) oder „4“ (=Fachstufe 3) angegeben werden.

Ohne diese Angaben werden nur die Schüler ohne Fächer und Noten übernommen. Beim Synchronisieren sollten Sie für die markierten Schüler die Berechnungsverordnung und den Abschlussjahrgang eingeben. Klicken Sie nach dem Synchronisieren auf die Schaltfläche `Berufsschule` in der Symbolleiste links im MAGELLAN-Fenster. Es werden alle synchronisierten Schüler auf der Registerkarte `Auswahl` angezeigt. Per Doppelklick auf den gewünschten Schüler oder über einen Klick auf die Registerkarte `Matrix` wechseln Sie zur Notenmatrix der Berufsschule. Auf dieser Registerkarte finden Sie die Fächer, Unterrichtsarten, Fachstatus inkl. Notenwerte und Faktoren der Schuljahre, falls Sie diese Angaben bereits in MAGELLAN bei den Zeugnisdaten der Schüler gemacht haben sollten. Andernfalls können Sie diese Angaben für die einzelnen Schulhalbjahre 1, 2, 3 bzw. 4 auch hier eingeben. Zur Anpassung des Layouts der Notenmatrix müssen Sie links oben auf der Registerkarte `Matrix` auf die Schaltfläche ![](/assets/images/berufsschulmatrix/berufsschulmatrix4.png) klicken.

## Sammelzuweisung in der Matrix

Auf der Karte Matrix haben Sie die Möglichkeit Fachdaten eines Schülers auch auf andere Schüler zu kopieren. 

|So geht's|
|--|
|1. Wählen Sie den Schüler aus dessen Fächer Sie kopieren möchten und gehen Sie dann auf die Karte `Matrix`.|
|2. Starten Sie den Assistenten mit dem Punkt `Sammelzuweisung`.|
|3. Markieren Sie die  Schüler, denen die kopierten Angaben zugewiesen werden sollen.|
|4. Wählen Sie auf der folgenden Karte aus welche Daten übernommen werden sollen und ob bereits vorhandene Daten überschrieben werden sollen.|
 

![Dialogfenster zur Sammelzuweisung von Matrixdaten](/assets/images/berufsschulmatrix/berufsschulmatrix5.png)

## Prüfungsnoten eingeben und prüfen

Die Prüfungsnoten der Schüler können Sie über ein gesondertes Fenster pro Klasse pro Fach eingeben. 



|So geht's|
|--|
|1. Bitte öffnen Sie aus dem Menü `Berufsschule > Matrix` heraus den Punkt `Bearbeiten > Prüfungsnoten eingeben`. |
|2. Wählen Sie die Klasse und das Fach aus. Es werden im Fenster alle Schüler der Klasse aufgelistet, für die das gewählte Fach auf der Karte `Berufsschule > Matrix` erfasst oder synchronisiert wurde. |
|3. Erfassen Sie in der Spalte `Prüfungsnote `oder `Prüfungsnote (Kontrolle)` die Noten. Die Sichtbarkeit dieser beiden Spalten kann pro Benutzer geregelt werden. |

!!! info "Hinweis"

	Ein Kollege gibt die Noten in die Spalte `Prüfungsnote` ein, ein zweiter Kollege gibt in die Spalte `Prüfungsnoten (Kontrolle)` ein. Die zweite Spalte ist währen der Eingabe jeweils ausgeblendet und kann später zur Kontrolle eingeblendet werden. Bitte beachten Sie hierzu den Abschnitt [„Allgemeine Rechte“](https://doc.magellan7.stueber.de/schulverwaltung/admin/users/#allgemeine-rechte).
 
![Geben Sie pro Fach pro Klasse die Prüfungsnoten ein.](/assets/images/berufsschulmatrix/berufsschulmatrix6.png)

## Abschlussnoten berechnen

Die Eingabe der Endnoten für Abschlusszeugnisse kann in zwei Schritte auf der Registerkarte `Matrix` unterteilt werden:

1. Automatische Berechnung der Endnoten.
2. Eventuelle manuelle Eingabe/Korrektur der Endnoten.

Die folgenden Abschnitte sagen Ihnen, wie Sie genau vorgehen müssen.
 
![Hier sehen Sie die Notenmatrix einer Schülerin in der Ansicht `Berufsschule`](/assets/images/berufsschulmatrix/berufsschulmatrix7.png)

### Automatische Berechnung

Unter `Verordnung` muss die korrekte Endnotenverordnung eingestellt sein bzw. wählen Sie die entsprechende aus. Klicken Sie auf `Neu berechnen`, um die Endnoten automatisch durch das entsprechende Skript berechnen zu lassen. Durch die Berechnungen werden automatisch die Noten in die Spalte `Endnote` eingetragen. Je nach Skriptinhalt werden auch auf der rechten Seite die Felder BU-Note (=Gesamtnote für den Berufsbezogener Unterricht) bzw. „Gesamtnote“ (=Gesamtnote des Abschluss) berechnet. Im automatisch erzeugten Meldungsfenster werden zusätzliche Statusinformationen zur Berechnung angezeigt. Insbesondere wird hier eine Aussage über die erfolgreiche Durchführung der Berechnung und eventuell notwendige Zwischensummen angezeigt. Die nachfolgende Abbildung zeigt ein Berechnungsbeispiel für den Berufsschulabschluss in Rheinland-Pfalz.

![Hier sehen Sie die Meldung zur Notenberechnung einer Schülerin in der Ansicht `Berufsschule`](/assets/images/berufsschulmatrix/berufsschulmatrix8.png)

### Manuelle Eingabe/Korrektur der Endnoten

Alle Noten der Berufsschulnotenmatrix können neben der automatischen Berechnung auch manuell eingegeben werden. Sie können so die Berufschulmatrix nur zur Eingabe von bereits festgelegten Endnoten nutzen. Insbesondere können Sie die manuelle Eingabe aber im Sinne der Korrektur einer zuvor automatisch durchgeführten Berechnung der Endnoten nutzen. Hat beispielsweise die automatische Berechnung ergeben, dass der Schüler genau zwischen zwei Noten steht, so können aufgrund des pädagogischen Ermessens in solchen Fällen z.B. die Faktoren geändert werden. Nach der Änderung kann dann die automatische Berechnung nochmals durchgeführt werden.

## Zeugnisse drucken

Klicken Sie bei den Berufsschuldaten des Schülers auf die Registerkarte `Zeugnis`, um die Zeugnisbemerkungen anzugeben. Es steht Ihnen auch eine Sammelzuweisung für Zeugnisbemerkungen zur Verfügung. Zusammen mit den Angaben auf der Registerkarte Noten und den allgemeinen Daten zum Schüler verfügen Sie dann über alle Daten, um das zeitraumübergreifende Abschluss- bzw. Abgangszeugnis auszudrucken.


|So geht's|
|--|
|1. Markieren Sie in der Liste der Schüler der Berufsschule per Mausklick oder mit Umschalt+Mausklick oder Strg+Mausklick die entsprechenden Schüler.| 
|2. Klicken Sie auf `Bearbeiten `und `Drucken `und wählen Sie das Zeugnisformular und klicken Sie auf `Drucken`.|


### Zeugnisformulare aus dem Berufsschulmenü drucken

Um die beim Schüler hinterlegten [Zeugnisformulare](https://doc.magellan7.stueber.de/schulverwaltung/howto/zeugnisdaten/#zeugnisformulare) (`Schüler > Zeugnis > Zeugnisformulare`) automatisiert zu drucken, müssen Sie den bzw. die entsprechenden Schüler in der Auswahlliste `Berufsschule` markieren und dann mit der rechten Maustaste den Befehl `Drucken > Zeugnisformulare drucken` wählen. 

