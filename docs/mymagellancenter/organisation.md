
# Organisation des zeitlichen Ablaufs

Vor dem Einsatz des MyMAGELLAN CENTERs bzw. von MyMAGELLAN sollten Sie sich ein entsprechendes Ablaufszenario erarbeiten. Dieses könnte beispielsweise wie folgt aussehen:

1. Bekanntgabe des Datums der Erzeugung der MyMAGELLAN-Dateien und der Frist zur Rückgabe der bearbeiteten MyMAGELLAN-Dateien pro Teilnehmer.

2. Bekanntgabe der Frist zur Kopie der MyMAGELLAN-Dateien auf die Datenträger.

3. Nach Ablauf der Rückgabefrist Überprüfung ob alle MyMAGELLAN-Dateien wieder eingespielt worden sind.

4. Einsammeln der MyMAGELLAN-Dateien.

## Mögliche Konflikte

### Konflikte bei Noten aufgrund Klassenlehrer/Tutor/Fachlehrer

Eine Verteilung der MyMAGELLAN-Dateien kann aufgrund der Benutzerrechte evtl. zu Konflikten führen.

Beim Erzeugen der Daten kann beispielsweise ein Schüler A sowohl in der MyMAGELLAN-Datei des Lehrers 1 existieren, weil dieser Klassenleiter 1 der aktuellen Klasse ist, als auch beim Fachlehrer der Klasse, weil dieser den Schüler A z.B. in Deutsch in der gleiche Klassen unterrichtet.

Es ist also organisatorisch festzulegen, wer überhaupt die Noten eingeben soll, um ein Überschreiben der Daten beim späteren Einsammeln zu vermeiden.

Beispielsweise könnten nur die Klassenleiter 1 der Klassen Teilnehmer von MyMAGELLAN sein, so dass nur die Klassenleiter die Noten mit MyMAGELLAN eingeben. Sie sollten daher beim Erzeugen der MyMAGELLAN-Dateien unter Filter genau festlegen, welche Daten in die MyMAGELLAN-Datei pro MyMAGELLAN-Teilnehmer übertragen werden sollen.

### Nicht eingegebene Noten in MyMAGELLAN

Nicht eingegebene Noten in MyMAGELLAN werden beim Einsammeln über das MyMAGELLAN CENTER besonders behandelt.

!!! info "Hinweis"

	Nicht eingegebene Noten in MyMAGELLAN werden beim Import nach MAGELLAN nicht berücksichtigt. Bestehende Noten in MAGELLAN werden so durch den Import einer MyMAGELLAN-Datei nicht gelöscht.

Hierbei gilt die Regel:
Ist einem Schüler in MyMAGELLAN für ein Fach keine Note eingetragen worden, so wird diese Note beim Import nach MAGELLAN nicht berücksichtigt. Wird z.B. in MyMAGELLAN für einen Schüler in einem Fach unter „Endnote 1“ keine Note eingetragen und in MAGELLAN ist für denselben Schüler unter „Endnote 1“ eine Note eingetragen, so wird diese durch dem Import nach MAGELLAN nicht überschrieben. 
Dieses Vorgehen ermöglicht die kombinierte Eingabe von Noten.
Unterrichtet beispielsweise der Lehrer L1 die Klasse 8a als Fachlehrer im Fach Deutsch und der Lehrer L2 ist Klassenleiter 1 der Klasse 8a , so ist folgende Konstellation möglich: Lehrer L2 gibt alle Noten bis auf das Fach Deutsch in MyMAGELLAN ein, Lehrer L1 gibt nur die Noten der 8a für das Fach Deutsch in MyMAGELLAN ein. Durch das Einspielen der MyMAGELLAN nach MAGELLAN werden beiden Dateien gemischt, so dass die Noten der Klasse 8a in MAGELLAN vollständig sind.

Dazu müssen Sie wie folgt vorgehen:

1. Lehrer L2 erhält über das Filter „Klassenleiter 1“ seine MyMAGELLAN-Datei. Er trägt in Absprache mit Lehrer L1 alle Noten der Klasse 8a mit Ausnahme des Fachs Deutsch über MyMAGELLAN ein und bringt die veränderte MyMAGELLAN-Datei wieder in die Schule.

2. Lehrer L1 erhält über das Filter „Fachlehrer“ seine MyMAGELLAN-Datei. Er trägt die Noten der Klasse 8a für das Fach Deutsch über MyMAGELLAN ein und bringt die veränderte MyMAGELLAN-Datei wieder in die Schule.

3. Die MyMAGELLAN-Dateien von L1 und L2 werden, unabhängig in welcher Reihenfolge, wieder nach MAGELLAN importiert. Alle Noten der 8a sind nun in MAGELLAN vollständig.

### Konflikt Klassenlehrer/Tutor/Fachlehrer bei „Weiteren Details“

Analog zu den Konflikten bei den Noten können auch Konflikte bei den weiteren Daten auftauchen:

* Unterrichtstage
* Versäumnisse
* Fehltage
* Davon unentschuldigt Fehltage
* Fehlstunden
* davon unentschuldigte Fehlstunden

Zur Konfliktlösung ist Folgendes zu berücksichtigen:

Kann der Lehrer eines Schülers die Registerkarte „Weiteren Daten“ in MyMAGELLAN editieren, so überschreiben in der Standardeinstellung seine Eingaben mit dem Einsammeln seiner MyMAGELLAN-Datei nach MAGELLAN unter grundsätzlich die bestehenden Eintragungen in MAGELLAN für diesen Schüler.

!!! info "Hinweis"

	Ausnahme: Wenn er keine Eintragungen in diesen Feldern in MyMAGELLAN vorgenommen hat, werden die Werte in MAGELLAN durch die >Eintragungen in MyMAGELLAN nicht überschrieben, wenn die Option beim Verteilen der MyMagelan-Dateien so gewählt wurde. 

Das gilt für folgende Werte:

* Unterrichtstage
* Versäumnisse
* Fehltage
* Davon unentschuldigt Fehltage
* Fehlstunden
* davon unentschuldigte Fehlstunden

Beispiel:
Der Lehrer L1 hat beim Schüler S1 in seiner MyMAGELLAN-Datei die Eintragung 2 bei den Fehlstunden gemacht. Der Lehrer L2 hat beim gleichen Schüler S1 in seiner MyMAGELLAN-Datei keine Eintragung (Standardwert=0) gemacht. Wird nun zuerst die MyMAGELLAN-Datei von Lehrer L1 eingelesen, so erhält der Schüler S1 in MAGELLAN den Wert 2 bei Fehlstunden. Wird anschließend die MyMAGELLAN-Datei des Lehrers L2 eingelesen, so bleibt die 2 bestehenen, wird nicht durch die 0 überschrieben. Sollte L2 die Null erfasst haben um einen Eintrag in MAGELLAN zu korrigieren, bleibt der vorherige Wert (> 0) bestehen. Erfasst Lehrer L2 einen anderen Wert, zum Beispiel 3 Fehlstunden, überschreibt die 3 die 2 (entscheidend ist die Reihenfolge des Einlesens).

Zur Konfliktlösung stehen Ihnen vier Möglichkeiten zur Verfügung.

* **Gewünschte Einstellungen bei Fehlstunden/-tage wählen:** Bei der Erstellung der MyMAGELLAN-Dateien über das MyMAGELLAN CENTER geben Sie an, ob die Fehlstunden/-tage beim späteren importieren überschrieben (nicht durch Null oder keinen Eintrag), addiert oder unverändert in MAGELLAN belassen werden. Ein Addieren macht beispielsweise dann Sinn, wenn jeder Fachlehrer nur seine Fehlstunden/-tage des Schüler einträgt.

* **Zeugnisbemerkungen: **Zeugnisbemerkungen werden generell nur aus Klassenleiter- oder Tutorendateien nach MAGELLAN eingelesen, nicht aus Fachlehrerdateien.
Nur Klassenleiter nutzen MyMAGELLAN: Bei der Erstellung der MyMAGELLAN-Dateien über das MyMAGELLAN CENTER werden nur Klassenleiter berücksichtigt (Exportfilter „Teilnehmer ist Klassenleiter 1 des Schülers“ aktiviert). Da ein Schüler nur einen „Klassenleiter 1“ zu einem Zeitraum in MAGELLAN besitzen kann, können die „Weiteren Daten“ eines Schülers nicht von einem anderen Lehrer beim Einlesen der MyMAGELLAN-Dateien überschrieben werden.

* **„Weitere Details“ exklusiv für Klassenleiter:** Bei der Erstellung der MyMAGELLAN-Dateien über das MyMAGELLAN CENTER werden Klassenleiter und Fachlehrer berücksichtigt, wobei die „Weiteren Daten“ nur für den Klassenleiter sichtbar sind (Exportfilter „Teilnehmer ist Klassenleiter 1 des Schülers“ und „Teilnehmer ist Fachlehrer des Schülers“ aktiviert, Editierbarkeit „Register „Weitere Daten“ ist für Fachlehrer sichtbar“ deaktiviert). In diesem Fall kann nur der Klassenleiter das Register “Weitere Daten“ in MyMAGELLAN nur bei den Schülern sehen, bei denen er Klassenleiter ist. Ist er nur Fachlehrer des Schülers, sieht es das Register „Weitere Daten“ in MyMAGELLAN nicht.

* **Unterscheidung von Fall zu Fall: **Bei der Erstellung der MyMAGELLAN-Dateien über das MyMAGELLAN CENTER werden Klassenleiter und Fachlehrer berücksichtigt, wobei die „Weiteren Daten“ für alle Lehrer sichtbar sind (Exportfilter „Teilnehmer ist Klassenleiter 1 des Schülers“ und „Teilnehmer ist Fachlehrer des Schülers“ aktiviert, Editierbarkeit „Register „Weitere Daten“ ist für Fachlehrer sichtbar“ aktiviert). In diesem Fall besteht die potentielle Gefahr, dass die Daten der Lehrer sich in Abhängigkeit von der Reihenfolge des Einlesens in MAGELLAN gegenseitig überschreiben. Man kann jedoch in MyMAGELLAN auf dem Register „Weitere Daten über“ das Optionsfeld „Nur Verhalten und Mitarbeit“ erreichen, dass nur die Felder „Verhalten“ und „Mitarbeit“ von den „Weiteren Daten“ beim Einlesen nach MAGELLAN berücksichtigt werden. Die Berücksichtigung dieser Möglichkeit setzt jedoch eine genaue Absprache zwischen den beteiligten Lehrern und sollte daher nur in Sonderfällen genutzt werden.

## Konflikt zwischen Tutoren und Klassenleitern beim Import von Zeugnisbemerkungen

 Wichtig bei den Bemerkungen, wie eigentlich auch bei allen anderen Zeugnisinformationen ist: Sind die MyMAGELLAN-Dateien beim Lehrer darf nichts in MAGELLAN verändert werden!
 
Beim Erstellen der MyMAGELLAN-Dateien werden bereits in MAGELLAN existierende Zeugnisbemerkungen in die Lehrer-/Tutorendateien mit ausgegeben. Um beim Import keine Dopplungen von Bemerkungen zu erzielen werden beim Einlesen der Klassenleiterdatei und der Tutorendatei jeweils zuvor die Schülerzeugnisbemerkungen gelöscht. Sollten einem Schüler ein Klassenleiter und ein Tutor zugeordnet worden sein, können damit je nach Einlesereihenfolge Zeugnisbemerkungen überschrieben werden.

Beispiel: Schüler S1 wurden Lehrer L1 und Tutor T1 zugeordnet. Beim Erstellen der MyMAGELLAN-Dateien haken Sie versehentlich beide Rollen an, also Klassenleiter und Tutorendatei erstellen. Eventuell in MAGELLAN bereits existente Zeugnisbemerkungen werden für S1 ausgespielt. L1 vergibt eine neue Zeugnisbemerkung, T1 vergibt keine neue Zeugnisbemerkung. Die Dateien von L1 und T1 werden wieder importiert. Import der Datei von L1: Zeugnisbemerkungen werden für S1 gelöscht, neue und alte Zeugnisbemerkung werden aus der Datei von L1 importiert. Als nächstes wird die Datei für T1 importiert: die Zeugnisbemerkungen von S1 werden gelöscht (neue und alte reimportierte Zeugnisbemerkungen), nur die alten Zeugnisbemerkungen werden eingelesen. Im Ergebnis fehlen die neuen Zeugnisbemerkungen von L1. Sie können den Konflikt nur lösen, indem Sie entweder:

> * entweder Schülern nicht einen Klassenleiter UND einen Tutor zuweisen
> * oder falls beide Felder für Schüler vergeben sind, beim Erstellen der Dateien nicht Tutor- und Klassenleiterdateien gemeinsam erstellen, sondern erst die Dateien für die zweite Rolle nach dem Einsammeln der Daten der ersten Rolle verteilen.  

!!! info "Hinweis"

	Zum Schluss eine Vorgehenstipp für die Schulen in Rheinland-Pfalz, an denen es eine MSS gibt: In der Mainzer Studienstufe wird das Fach „Gemeinschaftskunde“ als Grundkurs von zwei Lehrkräften je zweistündig unterrichtet. Dadurch sind in beiden Lehrerdateien die Schüler beinhaltet. Es sollte zuvor vereinbart werden, wer die Noten erfassen soll. Vorschlag: Es trägt diejenige Lehrkraft die Noten ein, in deren Fach die Kursarbeit geschrieben wurde.