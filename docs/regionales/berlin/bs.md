#	Berufsschulnoten

## 	Allgemeines

Zur zeitraumübergreifenden Endnotenberechnung der Berufsschule und dem anschließenden Zeugnisdruck gehören folgende Aufgaben:

1.	Berufsschulklassen und andere Stammdaten einrichten
2.	Fächer und Noten der Schüler pro Zeitraum einer Zeugnisausgabe eingeben
3.	Endnoten für Abgangs- bzw. Abschlusszeugnisse berechnen
4.	Zeugnisbemerkungen eingeben und Zeugnisse drucken

Alle Schritte werden in MAGELLAN ausgeführt.  

Um die Noten der Berufsschule des jeweiligen Schülers in MAGELLAN anzuzeigen, klicken Sie in MAGELLAN auf `Berufsschule` in der Symbolleiste links.
MAGELLAN verfügt über sehr kompakte Funktionen für die gesamte Endnotenberechnung und macht Ihnen so die Arbeit so leicht wie möglich. Es liegt leider in der Natur der Sache, dass zusätzlich von Ihrer Seite aus sehr gute Kenntnisse in der jeweiligen Verordnung erforderlich sind.

In den folgenden Abschnitten werden die einzelnen Schritte in der Endnotenberechnung mit MAGELLAN erläutert.
Bevor wir mit der eigentlichen Berechnung beginnen, müssen wir zunächst einige wichtige Bemerkungen zu Berufsschulklassen, Unterrichtsarten, Fachstatus, Stundenfaktoren und früher abgeschlossene Fächern machen.

##	Landesspezifische Skripte für Berlin

Die gesamte Notenberechnung bei zeitraumübergreifenden Abschluss- bzw. Abgangszeugnissen wird durch MAGELLAN-Skripte durchgeführt oder anders gesagt, jedes Berufsschulskript repräsentiert eine spezielle Berechnungsvorschrift für die Noten auf dem Abschluss- bzw. Abgangszeugnis der Berufsschule. 

> #### warning::Wichtig!
>
> Alle zur Verfügung stehenden Skripte werden in der Übersicht [Alle Skripte im Überblick](https://doc.la.stueber.de/alle_skripte_im_uberblick.html#berlin) gezeigt. Sämtliche notwendigen Einstellungen pro Skript beschreiben wir in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/).

Die Skripte befinden sich im MAGELLAN-Verzeichnis im Ordner „Skripte“ und dort im jeweiligen Landesordner (z.B. „Skripte\Berlin“ für das Bundesland Berlin). 

##	Berufsschulklassen einrichten
Eine Klasse in der Berufsschule besteht aus den Jahrgängen 1 (=Grundstufe), 2 (Fachstufe 1), 3 (Fachstufe 2) bzw. 4 (Fachstufe 3). 

In MAGELLAN werden die Daten halbjahresbezogen abgelegt. Sie definieren also eine Klasse mit je zwei Zeiträumen bzw. Halbjahren für die Grundstufe, Fachstufe 1 und evtl. Fachstufe 2 bzw. Fachstufe 3. 
Eine zweijährige Klasse besteht demnach aus 4 Halbjahren mit dem Jahrgang 1 für die ersten beiden Halbjahr und dem Jahrgang 2 für die letzten beiden Halbjahre.

Folgende Angaben sind bei der Eingabe der Berufsschulklasse neben den Halbjahren wichtig:

Eingabefeld	|Eingabe
---|---
Klassenart|	Standard
Jahrgang	|1, 2, 3 oder 4 (pro Zeitraum der Klasse notwendig)
Beurteilungsart|	Benotung durch Noten

## Unterrichtsarten, Fachstatus und Faktoren

Voraussetzung für die Abgangs- bzw. Abschlussnotenberechnung ist, dass Sie bei den Fächern des Schülers die entsprechende Unterrichtsart und den entsprechenden Fachstatus eingegeben haben. Zusätzlich müssen Sie evtl. auch den Stundenfaktor des Fachs angeben.

Generell verwenden Sie die gleichen Unterrichtsarten, Fachstatus und Faktoren, die Sie auch in den sonstigen Zeugnissen (z.B. Jahreszeugnis) nutzen.

Bei den einzelnen Berechnungsskripten werden bestimmten Unterscheidungen in den Unterrichtsarten bzw. Fachstatus vorausgesetzt d.h. die entsprechenden Schlüssel müssen vorhanden sein (die Kürzel werden nur zur Anzeige verwendet). Teilweise müssen Sie auch Angaben zum Stundenfaktor des Fachs machen. Diese Informationen werden nachfolgend aufgelistet.

##	Das Skript BER-BBS-Matrix-2007

### Fächer
Bei dem Skript „BER-BBS-Matrix-2007“ für das Bundesland Berlin sind die folgenden Angaben für das Fach Sport/Gesundheitsförderung und fakultative Fächer Voraussetzung.

#### Sport/Gesundheitsförderung
Ob ein dem Schüler zugeordnetes Fach das Fach Sport/Gesundheitsförderung ist, richtet sich nach der Definition des Fachs im Verzeichnis der Fächer. 

Kürzel	|Schlüssel	|Bedeutung
---|---|---
Spo|	beliebig    	|Sport

Kürzel (im abgebildeten Fall „Spo“ für Sport) und Schlüssel können dabei beliebig gewählt werden, entscheidend ist die Zuordnung des Fachs zur Kategorie „Sport“ im Verzeichnis der Fächer.

#### Religion
Ob ein dem Schüler zugeordnetes Fach das Fach „Religion“ bzw. „Ethik“ ist, richtet sich nach der Definition des Fachs im Verzeichnis der Fächer.

Kürzel	|Schlüssel	|Bedeutung
---|---|---
Rel	|beliebig   | 	Religion/Ethik
Eth	|beliebig   |	Religion/Ethik

Kürzel (im abgebildeten Fall „Rel“ für Religion bzw. „Eth“ für Ethik) und Schlüssel können dabei beliebig gewählt werden, entscheidend ist die Zuordnung des Fachs zur Kategorie „Religion/Ethik“ im Verzeichnis der Fächer.

#### Fakultative Fächer
Fakultative Fächer werden bei der Zuordnung der Fächer zum Schüler durch den Fachstatus „Wahlb“ gekennzeichnet, wie z.B.:

Fach|	Fachstatus
---|---
Fra	|Wahlb

Besitzt ein Fach die Kategorie „Religion/Ethik“ wird es automatisch als fakultatives Fach betrachtet. 
Das Fach Sport/Gesundheitsförderung und fakultative Fächer werden bei der Berechnung des Gesamtnotendurchschnitts in der Berufsschulmatrix nicht berücksichtigt.

### Wiederholer

Ob ein Schüler im jeweils letzten Zeitraum seiner Laufbahn die Klasse wiederholt, richtet sich nach dem Eintrag unter Ansicht `„Schüler“ > Laufbahn > Allgemein“` im Feld „Wiederholer“. Ist dieses markiert, wiederholt der Schüler die Klasse.
Für das Skript bedeutet dies, dass er kein Zeugnis zugewiesen bekommt. 

### Kammerprüfung
Ob ein Schüler bei Berufsschulabschluss die Kammerprüfung bestanden hat, richtet sich nach dem Eintrag unter Ansicht `„Schüler“ > Laufbahn > Allgemein“ im Feld „Entscheidung“. Da dies ein Schlüsselfeld ist, müssen Sie unter `„Verzeichnisse > Entscheidungen“` folgenden Eintrag definieren:

Kürzel	|Schlüssel	|Bedeutung
--|--|--
J	|beliebig | 	Kammerprüfung bestanden

Bei keinem Eintrag im Feld „Entscheidung“ hat der Schüler die Kammerprüfung nicht bestanden.

### Höchster bisheriger Abschluss 

Für die Berechnung des zusätzlichen Abschlusses im obigen Abschnitt, muss für den Schüler festgehalten werden, ob er den Hauptschulabschluss besitzt. Dieser Abschluss wird pro Schüler unter der Ansicht `Schüler > Daten 2` im Feld `„Höchster Abschluss ABS/Abschluss“` bzw. `„Höchster Abschluss BBS/Abschluss“ ` eingetragen. Für diese Felder muss unter `„Verzeichnisse > Abschlüsse (Extern)“` folgende Einträge definiert werden:

Kürzel	|Schlüssel|	Bedeutung
--|--|--
HS	|HS|	Hauptschulabschluss
EHS	|EHS|	Erweiterter Hauptschulabschluss
MSA	|MSA|	Mittlerer Schulabschluss
BOS	|BOS|	Abschuss der Berufsoberschule
FH	|FH|	Abschluss Fachhochschulreife
ABI	|ABI|	Abschluss Abitur

### Ausreichende Fremdsprachenkenntnisse

Ob ein Schüler bei Berufsschulabschluss ausreichende Fremdsprachenkenntnisse besitzt, richtet sich nach dem Eintrag unter Ansicht `„Schüler > Laufbahn > Allgemein“` im Feld `„Empfehlung“`. Da dies ein Schlüsselfeld ist, müssen Sie unter `Verzeichnisse > Empfehlungen` folgenden Eintrag definieren:

Kürzel	|Schlüssel	|Bedeutung
--|--|--
J	|beliebig  |Ausreichende Fremdsprachenkenntnisse

Bei keinem Eintrag im Feld „Empfehlung“ hat der Schüler nicht ausreichende Fremdsprachenkenntnisse.

### Regelstundenzeit des Bildungsgangs 

Ob ein Schüler bei Berufsschulabschluss die ausreichende Regelstundenzeit in seinem Bildungsgang besitzt, richtet sich nach den unter dem Bildungsgang des Schülers eingetragenen Regelstunden. Die Regelstunden eines Bildungsgangs definieren Sie unter `Verzeichnisse > Bildungsgänge` im Feld `„Statistik-ID“`.

Kürzel|	Schlüssel	|Bedeutung|	Statistik-ID
--|--|--|--
beliebig |beliebig|beliebig|Anzahl der Regelstunden  

Einen Bildungsgang können Sie demnach beispielweise wie folgt definieren.

Kürzel|	Schlüssel	|Bedeutung|	Statistik-ID
--|--|--|--
KFZ	|KFZ	|Feinmechatroniker|	480

Hat der Schüler weniger als 480 Stunden als Regelstundenzeit in seinem Bildungsgang, so muss er für das Erreichen des Mittleren Schulabschlusses den zusätzlichen allgemeinbildenden Unterricht mit Erfolg besucht haben. 
Ob ein Schüler den zusätzlichen  allgemeinbildenden Unterricht mit Erfolg besucht hat,  richtet sich nach dem Eintrag unter Ansicht ` Schüler > Merkmale` im Feld `„Merkmal A6“`.

Kürzel	|Schlüssel	|Bedeutung
--|--|--
J|beliebig|Zusätzlicher Unterricht MSA erfolgreich besucht

## Zeugnisformulare für Abschluss- und Abgangszeugnis

Da das Skript automatisch die jeweiligen Zeugnisformulare den Schülern zuordnet, müsse die Zeugnisformulare zuvor unter „Verzeichnisse/Zeugnisformulare“ definiert werden. 

Bezeichnung|	Typ	|Datei
--|--|--
BER-BS-AS	|beliebig  |beliebig    
BER-BS-MSA	|beliebig  |beliebig   
BER-BS-AZ	|beliebig  |beliebig    

> #### warning::Wichtig!
>
> Die Bezeichnungen BER-BS-AS für das Abschlusszeugnis, BER-BS-MSA für das Zusatzzeugnis Mittlerer Schulabschluss und BER-BS-AZ für das Abgangszeugnis sind fest vorgegeben.


##	Endnotenberechnung vorbereiten

 ![Berufsschulmatrix](/images/berlin/bs/bs1.png) 
 
Für die Endnotenberechnung müssen Sie folgende Daten definieren und je Schüler eingeben:

1.	Abschlussjahrgang definieren
2.	Berechnungsverordnung definieren
3.	Je Schüler Abschlussjahrgang und Berechnungsverordnung angeben
4.	Je Schüler die Fächer, Noten bzw. Faktoren synchronisieren oder manuell eingeben

In den nachfolgenden Abschnitten erfahren Sie mehr zu den einzelnen Punkten.

###	Abschlussjahrgang definieren

![Abschlussjahrgang definieren](/images/berlin/bs/bs2.png) 
   
Sie können in MAGELLAN unter `Verzeichnisse > Abschlussjahrgänge` Abschlussjahrgänge definieren. Damit können Sie jedem Schüler in der Rubrik „Berufsschule“ den entsprechenden Abschlussjahrgang zuordnen. Dieser Vermerk hat keinen Einfluss auf Abschlussnotenberechnungen, sondern dient dazu, später alle Schüler eines bestimmten Abschlussgangs z.B. für Ausdrucke herausfiltern zu können und die Art der zu synchronisierenden Noten festzulegen.
 
Die Art der zu synchronisierenden Noten des Abschlussjahrsganges legen Sie über die Kategorie fest:

* Wählen Sie die Kategorie „Berufsschule (Jahresnoten)“ um später beim Synchronisieren der Schüler nur die Noten des jeweils 2. Halbjahres in die Ansicht „Berufschule“ zu übertragen.

 * Wählen Sie die Kategorie „Berufsschule (Halbjahresnoten)“ um später beim Synchronisieren der Schüler die Noten des jeweils 1. und 2. Halbjahres in die Ansicht „Berufschule“ zu übertragen.
 
 
## Skript BER-BBS-Matrix-2007

Bei der Definition eines Abschlussjahrgangs für das Skript „BER-BBS-Matrix-2007“ müssen Sie als Kategorie „Berufsschule (Halbjahresnoten)“ wählen. Es werden dann bei der Synchronisation der Berufsschuldaten bis zu 9 Halbjahre eines Schülers in die Berufsschulmatrix übertragen.

###	Berechnungsverordnung definieren

![Berechnungsverordnung definieren](/images/berlin/bs/bs3.png)

   
Sie müssen für jeden Schüler die Berechnungsverordnung angeben, die für ihn relevant ist. Dazu müssen Sie im Schlüsselverzeichnis „Verordnungen“ die jeweilige Berechnungsverordnung definieren. Klicken Sie dazu auf `„Verzeichnisse > Verordnungen“ `und geben dort die Verordnung wie folgt an:

Spalte|	Bedeutung
--|--
Kürzel	|8-stellige Kurzbezeichnung der Verordnung
Bezeichnung|	Bezeichnung der Verordnung
Kategorie	|Wenn Sie hier „Berufsschule“ eingeben, wird die Verordnung bei den Schüler-Berufsschuldaten angezeigt
Typ|	Bei einigen Verordnungen muss hier eine spezielles Kürzel angegeben werden.
Gültig von|	Gültigkeitsdatum von, ohne Bedeutung für die Berechnungen
Gültig bis|	Gültigkeitsdatum bis, ohne Bedeutung für die Berechnungen
Skript|	Geben Sie hier den Namen des Skripts für diese Berechnungsverordnung ein. Alle verfügbaren Skripte befinden sich im MAGELLAN-Verzeichnis SKRIPTE.

## Skript BER-BBS-Matrix-2007

Bei der Definition der Verordnung für das Skript „BER-BBS-Matrix-2007“ müssen Sie unter Typ „BER-BS“ angeben. 

## Berufsschuldaten synchronisieren
 
![Berufsschuldaten synchronisieren](/images/berlin/bs/bs4.png)


Bevor Sie die Endnotenberechnung durchführen können, müssen Sie die Daten der Schüler synchronisieren, indem Sie in MAGELLAN auf `„Berufsschule“` klicken und dann auf die Schaltfläche `„Synchronisieren“` oben im MAGELLAN-Fenster klicken. 

Beim Synchronisieren geschieht Folgendes: 

MAGELLAN extrahiert für die markierten Schüler die Fachdaten der Noten der Grundstufe, Fachstufe 1, Fachstufe 2 bzw. Fachstufe 3. Besitzt der ausgewählt Abschlussjahrgang die Kategorie „Berufschule (Jahresnoten)“, werden nur die Noten der jeweiligen 2. Halbjahre  (=Jahresnoten) extrahiert. Besitzt der ausgewählt Abschlussjahrgang die Kategorie „Berufschule (Halbjahresnoten)“, werden die Noten des 1. und 2. Halbjahres extrahiert. 

Dies ist die Voraussetzung dafür, dass die Abschlussberechnungen der Berufschule durchgeführt werden können. Auch wenn Sie zuvor keine Fächer bzw. Noten in den Halbjahren des Schülers angegeben haben, müssen Sie diese Synchronisation einmal ausführen.

Damit die Schüler mit allen Fächern, Noten und Faktoren aus den einzelnen Halbjahren korrekt übernommen werden können, sind folgende Angaben in MAGELLAN notwendig.

Eintrag|Bedeutung
--|--
Zeiträume| Im Verzeichnis der Zeiträume muss das Feld „Art“ mit dem Wert „1. Halbjahr“ bzw. „2. Halbjahr“ gefüllt sein.
Jahrgang| Bei jeder Klasse der Berufschule muss auf der Registerkarte „Zeiträume“ für jeden Zeitraum  das Feld „Jahrgang“ mit dem Wert „1“ (=Grundstufe), „2“ (=Fachstufe 1), „3“ (=Fachstufe 2) oder „4“ (=Fachstufe 3) angegeben werden.

> #### warning::Wichtig!
>
> Ohne vorstehenden Angaben werden nur die Schüler ohne Fächer und Noten übernommen.

Beim Synchronisieren sollten Sie für die markierten Schüler die Berechnungsverordnung und den Abschlussjahrgang eingeben.
Klicken Sie nach dem Synchronisieren auf die Schaltfläche „Berufsschule“ in der Symbolleiste links im MAGELLAN-Fenster. Es werden alle synchronisierten Schüler auf der Registerkarte „Auswahl“ angezeigt.

Per Doppelklick auf den gewünschten Schüler oder über einen Klick auf die Registerkarte wechseln Sie zur Notenmatrix der Berufsschule. Auf dieser Registerkarte finden Sie die Fächer, Unterrichtsarten, Fachstatus inkl. Notenwerte und Faktoren der Schuljahre, falls Sie diese Angaben bereits in MAGELLAN bei den Zeugnisdaten der Schüler gemacht haben sollten. Andernfalls können Sie diese Angaben für die einzelnen Schulhalbjahre 1, 2, 3 bzw. 4 auch hier eingeben.

## Spalte „Faktor“ auf der Registerkarte „Matrix“

Auf der Registerkarte „Matrix“ hat die Spalte „Faktor“ für einige Skripte eine besondere Bedeutung. Sie gibt im Rahmen der Berechnung der Gesamtnote (auch teilweise „Gesamtnotendurchschnitt“ genannt) an, mit welchen Faktoren die Endnoten untereinander verrechnet werden.

Allen Berufschulverordnungen gemeinsam ist die Tatsache, dass die Fächer für Sport, Religion/Ethik und fakultative Fächer nicht bei der Gesamtnote berücksichtigt werden. Entsprechend wird die Spalte „Faktor“ im Rahmen der Synchronisation mit dem Faktor „0“ vorbesetzt.

Wie evtl. die Fächer für Sport, Religion/Ethik und fakultative Fächer speziell zu kennzeichnen sind, ist bei den jeweiligen landesspezifischen Skripten.

## Fächer und Punkte eingeben

Sollten Sie die Fächer nicht schon unter Ansicht `Schüler > Zeugnis > Leistungen` eingegeben haben, so dass sie beim Synchronisieren übernommen wurden, können Sie das auch direkt auf der Registerkarte „Matrix“ machen. Mit der Einfg-Taste oder durch Klick auf das Einfügen-Symbol rechts oben erzeugen Sie eine neue Zeile. Geben Sie das Fach, Unterrichtsart, Fachstatus und die Noten mit dem jeweiligen Faktor für die einzelnen Schuljahre ein.


## Sammelzuweisung für Fächer, Faktoren, Positionen, Merkmale, Konferenz- und Zeugnisdaten

Auf der Karte Matrix haben Sie die Möglichkeit Fachdaten eines Schülers auch auf andere Schüler zu kopieren. Sie gehen dazu wie folgt vor:

1.	Wählen Sie den Schüler aus dessen Fächer Sie kopieren möchten und gehen Sie dann auf die Karte „Matrix“.
2.	Starten Sie den Assistenten mit dem  Punkt „Sammelzuweisung“.
3.	Markieren Sie die  Schüler, denen die kopierten Angaben zugewiesen werden sollen.
4.	Wählen Sie auf der folgenden Karte aus welche Daten übernommen werden sollen und ob bereits vorhandene Daten überschrieben werden sollen.
 
 ![Sammelzuweisung für Fächer, Faktoren, Positionen, Merkmale, Konferenz- und Zeugnisdaten](/images/berlin/bs/bs5.png)

 
## Die Spalte „Position“

Die Position kann als Merkmal für die Reihenfolge der Fächer auf der Registerkarte „Notenmatrix“ und auf den Abschluss-/Abgangszeugnis verwendet werden, welche die Berufsschulmatrix nutzen. Die in MAGELLAN mitgelieferten Skripte und Zeugnisformulare für die Berufsschulmatrix verwenden diese Positionsangaben. 
Klicken Sie auf den Titel „Position“, um die Fächerliste entsprechend zu sortieren.

## Unterrichtsarten eingeben

Geben Sie in der Spalte „Unterrichtsart“ für  jedes Fach die Unterrichtsart ein. Sie ist vom verwendeten Skript abhängig.

##	Fachstatus eingeben

Geben Sie in der Spalte „Fachstatus“ für  jedes Fach den Fachstatus ein. Er ist vom verwendeten Skript abhängig . 

## Endnotenberechnung durchführen

Die Endnoten  für Abschlusszeugnisse kann in zwei Schritte unterteilt werden:

1.	Automatische Berechnung der Endnoten.
2.	Eventuelle manuelle Eingabe/Korrektur der Endnoten.

Die folgenden Abschnitte sagen Ihnen, wie Sie genau vorgehen müssen:

### 	Automatische Berechnung
Überprüfen Sie, ob für den Schüler die notwendigen Fächer inkl. der Faktoren für die einzelnen Jahresnoten auf der Registerkarte Notenmatrix eingetragen sind. Zudem muss unter Verordnung die korrekte Endnotenverordnung eingestellt ist bzw. wählen Sie die entsprechende aus.

Klicken Sie auf die Schaltfläche `Neu berechnen`, um die Endnoten automatisch durch das entsprechende Skript berechnen zu lassen. Durch die Berechnungen werden automatisch die Noten in die Spalte Endnote eingetragen. Je nach Skriptinhalt werden auch auf der rechten Seite die Felder BU-Note (=Gesamtnote für den Berufsbezogener Unterricht) bzw. Gesamtnote (=Gesamtnote des Abschluss) berechnet.

Im automatisch erzeugten Meldungsfenster werden zusätzliche Statusinformationen zur Berechnung angezeigt. Insbesondere wird hier eine Aussage über die erfolgreiche Durchführung der Berechnung und eventuell notwendige Zwischensummen angezeigt. Die nachfolgende Abbildung zeigt ein Berechnungsbeispiel für den Berufsschulabschluss in Rheinland-Pfalz.

![ Berechnungsbeispiel für den Berufsschulabschluss in Rheinland-Pfalz](/images/berlin/bs/bs6.png)
   
## Skript BER-BBS-Matrix-2007

Bei diesem Skript gelten einige zusätzliche Eigenschaften bei der automatischen Berechnung

### Endnote

Das Feld „Endnote“ eines Fachs wird nur dann neu berechnet, wenn das jeweilige Endnotenfeld des Fachs leer ist. Andernfalls wird davon ausgegangen, dass die Endnote absichtlich manuell eingeben worden ist.
Über die Schaltfläche Endnoten löschen können Sie alle Endnoten in der Spalte „Endnote“ des jeweiligen Schülers löschen.

#### Faktor der Endnote

Das Feld „Faktor“ der Endnote wird automatisch berechnet, sobald die Schaltfläche „Neu berechnen“ gewählt wird.

#### Zusätzlicher Abschluss

In Abhängigkeit vom erfolgreichen Berufsschulabschluss wird im Rahmen der automatischen Berechnung gemäß der nach der Verordnung zu erfüllenden Voraussetzungen der zusätzliche Abschluss berechnet und dem Schüler zugewiesen. Dieser Abschluss wird auf der Registerkarte „Abschluss“  im Feld „Abschluss 2“ eingetragen.

#### Zeugnis

In Abhängigkeit vom erfolgreichen Berufsschulabschluss wird im Rahmen der automatischen Berechnung gemäß der nach der Verordnung zu erfüllenden Voraussetzungen das Abschluss- bzw. Abgangszeugnis dem Schüler unter Ansicht `„Schüler“ > Zeugnis > Zeugnis` unter Zeugnisformulare automatisch zugewiesen. Der Ausdruck der Zeugnisse kann dann später über das automatisierte Drucken von Zeugnisformularen erfolgen.

##	Manuelle Eingabe/Korrektur der Endnoten

Alle Noten der Berufsschulnotenmatrix können neben der automatischen Berechnung auch manuell eingegeben werden. Sie können so die Berufsschulmatrix nur zur Eingabe von bereits  festgelegten Endnoten nutzen. 
Insbesondere können Sie die manuelle Eingabe aber im Sinne der Korrektur einer zuvor automatischen Berechnung der Endnoten nutzen. Hat beispielsweise die automatische Berechnung ergeben, dass der Schüler genau zwischen zwei Noten steht, so können aufgrund des pädagogischen Ermessens in solchen Fällen z.B. die Faktoren geändert werden. Nach der Änderung kann dann die automatische Berechnung nochmals durchgeführt werden.

## Wer hat Berufsschuldaten geändert?

Abschluss- bzw. Abgangsdaten der Berufsschule sind sensible Daten. Über die Benutzerverwaltung des MAGELLAN-ADMINISTRATORs wird festgelegt, wer Zugang zu welchen Daten hat. Wie aber können Sie feststellen, dass Daten unter „Berufsschule“ geändert worden sind und sei es versehentlich durch Sie selbst? 

Bei Änderungen auf den Berufsschule-Registerkarten vermerkt MAGELLAN automatisch das aktuelle Datum und die Kennung des aktuellen Benutzers.  Auf der Registerkarte „Auswahl“ werden für jeden Schüler das Datum und die Kennung desjenigen angezeigt, der diese Angaben bestätigt hat. So ist überprüfbar, wer wann Daten auf der Registerkarte „Berufsschule“ eines Schülers geändert hat.

## Zeitraumübergreifende Zeugnisse drucken

Im Kapitel 4 werden die verfügbaren Abgangszeugnisse und Abschlusszeugnisse der Berufsschule aufgelistet. Sollten für Ihr Bundesland keine zeitraumübergreifenden Zeugnisse verfügbar sein, können Sie diese selbst mit Crystal Reports erstellen, indem Sie das Zeugnis eines anderen Bundeslandes als Vorlage nehmen oder Sie geben STÜBER SYSTEMS den Auftrag, das Zeugnis für Sie zu erstellen.

Alle zeitraumübergreifenden Zeugnisse der Berufsschule basieren auf den Eintragungen unter Berufsschule.
Klicken Sie bei den Berufsschuldaten des Schülers auf die Registerkarte „Zeugnis“, um die Zeugnisbemerkungen anzugeben. Zusammen mit den Angaben auf der Registerkarte „Notenmatrix“ und den allgemeine Daten zum Schüler verfügen Sie dann über alle Daten, um das zeitraumübergreifende Abschluss- bzw. Abgangszeugnis auszudrucken.

So drucken Sie zeitraumübergreifende Abschluss- und Abgangszeugnisse der Berufsschule:

1.	Markieren Sie in der Liste der Schüler der Berufsschule per Mausklick oder mit Umschalt+Mausklick oder Strg+Mausklick die entsprechenden Schüler. 
2.	Klicken Sie auf `Bearbeiten` und `Drucken` und `„Zeugnisse drucken“` und wählen Sie das Zeugnisformular und klicken Sie auf `Drucken`.

Optional können Sie auch über das Schüler-Formular drucken.

## Zeugnisformulare aus dem Berufsschulmenü drucken

Um die beim Schüler unter Ansicht `Schüler > Zeugnis > Zeugnis > Zeugnisformulare` hinterlegten Zeugnisformulare automatisiert zu drucken, müssen Sie den bzw. die entsprechenden Schüler in der „Auswahlliste Berufsschule“ markieren und dann mit der rechten Maustaste den Befehl `Drucken > Zeugnisformulare drucken` wählen.

