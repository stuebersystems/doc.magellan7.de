
# Importlogik

Nachstehend wird beschrieben was genau beim Import passiert, falls Daten in Magellan und/oder in in MyMagellan vorhanden sind.

!!! warning "Wichtig"

	Bitte ändern Sie in Magellan keine Verzeichniswerte oder Daten auf der Unterkarte `Schüler > Zeugnis` solange MyMagellan-Dateien für die Kollegen verteilt wurden.


!!! warning "Wichtig"

	Zeugnisbemerkungen werden nur von Klassenleitern und Tutoren nach Magellan übernommen.

In der nachstehenden Tabelle zeigen wir welche Felder nicht editierbar sind. Sie können beim Erzeugen der Dateien jedes der Felder gezielt ausblenden, für ausgeblendete Daten wird kein Wert in die MyMagellan-Datei gespielt und auch nichts wieder importiert.

Feld | wahlweise<br/> editierbar | wahlweise<br/>ausblendbar | Importverhalten
-- | -- | -- |--
Fach | NEIN |NEIN | siehe Abschnitt [Informationsfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#informationsfelder)
Kurs<br/>kombinierte Ansicht von Fach und Kursnummer | NEIN |NEIN | siehe Abschnitt [Informationsfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#informationsfelder)
Schriftl. Note 1 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Schriftl. Note 2 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Schriftl. Note 3 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Schriftl. Note 4 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Mündl. Note | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Endnote | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Endnote(Gesamt) | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Position | JA |JA | siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Faktor | JA |JA | siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Merkmal | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Schwerpunkt | NEIN |JA | siehe Abschnitt [Informationsfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#informationsfelder)
Fachstatus | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Unterrichtsart | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Tutor | NEIN |JA | siehe Abschnitt [Informationsfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#informationsfelder)
Fachlehrer | NEIN |JA | siehe Abschnitt [Informationsfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#informationsfelder)
Niveau | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Mahnung | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Zusatznote 1 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 2 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 3 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 4 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 5 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 6 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 7 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 8 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Zusatznote 9 | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Beurteilung | JA | JA |siehe Abschnitt [Beurteilungen](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#beurteilungen)
Vornote | JA | JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Vergessene Hausaufgaben | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Vergessene Arbeitsmaterialien | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Personalnummer | NEIN |JA| siehe Abschnitt [Informationsfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#informationsfelder)
Leistungsart| JA |JA| siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Bestanden| JA |JA| siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschluss 1 | JA |JA|siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschlussart 1 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Vergessene Hausaufgaben | JA |JA| siehe Abschnitt [Weitere Listenfelder](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#weitere-listenfelder)
Abschlussdatum 1 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschlussnote 1 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschluss 2 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschlussart 2 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschlussdatum 2 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Abschlussnote 2 | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Versetzt | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Versetzungsart | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Zeugniskonferenz | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Zeugnisdatum | JA |JA |siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)
Verhalten | JA |JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Mitarbeit | JA |JA | siehe Abschnitt [Noten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#noten)
Unterrichtstage | JA |JA | siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Versäumnisse | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Fehltage | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Versäumnisse | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Fehltage (unentschuldigt) | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Fehlstunden | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Fehlstunden (unentschuldigt) | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Fehltage Praktikum | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Fehltage Praktikum (unentschuldigt) | JA |JA| siehe Abschnitt [Fehlzeiten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#fehlzeiten)
Leistungsanforderung | JA |JA | siehe Abschnitt [Zeugnisdaten](https://doc.magellan.stueber.de/mymagellancenter/importlogik/#zeugnisdaten)

## Informationsfelder

Die Inhalte dieser Felder werden nur zur Information und für eine einfachere Sortierung nach MyMagellan übertragen, es ist keine Änderung dieser Inhalte über MyMagellan möglich.

## Noten

Stand in Magellan/MyMagellan |Was passiert beim Import?
---|---
Note ist in Magellan /keine Note in MyMagellan| Note in Magellan bleibt bestehen
Note ist nicht in Magellan, Note ist in MyMagellan| Note aus der MyMagellan-Datei wird eingelesen
Noten sind in beiden Programmen|Note aus MyMagellan wird eingelesen

!!! info "Hinweis"

	Das bedeutet, wenn in Magellan eine Note besteht, die Sie in der MyMagellan-Datei entfernen, dann bleibt die Note weiterhin nach dem Einlesen in Magellan bestehen.

## weitere Listenfelder

Stand in Magellan/MyMagellan |Was passiert beim Import?
---|---
Wert ist in Magellan /kein Wert in MyMagellan | Wert in Magellan bleibt bestehen
Wert ist nicht in Magellan, Wert ist in MyMagellan | Wert aus der MyMagellan-Datei wird eingelesen
Wert ist in beiden Programmen | Wert aus MyMagellan wird eingelesen

!!! info "Hinweis"

	Das bedeutet, wenn in Magellan ein Wert besteht, die Sie in der MyMagellan-Datei entfernen, dann bleibt der Wert weiterhin nach dem Einlesen in Magellan bestehen.

## Beurteilungen

Gemeint sind die Beurteilungen unter `Schüler > Zeugnis > Leistungen` im Feld `Beurteilungen`. Hier können zusätzlich zur Benotung (per Punkt- oder Notenwert) schriftliche Beurteilungen pro Fach erfolgen.

Stand in Magellan/MyMagellan |Ergebnis
---|---
Beurteilung ist in Magellan /keine Beurteilung in MyMagellan| Beurteilung in Magellan bleibt bestehen
Beurteilung ist nicht in Magellan, Beurteilung ist in MyMagellan| Beurteilung aus der MyMagellan-Datei wird eingelesen
Beurteilung sind in beiden Programmen|Beurteilung aus MyMagellan wird eingelesen

!!! info "Hinweis"

	Beispiel: Sie verteilen die Daten für Fachlehrer und Klassenleiter gleichzeitig, es ist beispielsweise die Fachzeile für Mathematik eines Schülers in der Fachlehrerdatei und in der Klassenleiterdatei. **Die Eintragungen beider Rollen werden beim Import gleichwertig behandelt.** 
	Trägt nur einer der beiden in seine Datei eine Leistungsbeurteilung für Mathe ein, wird dessen Eintragung nach Magellan importiert. 
	Tragen beide Kollegen (also der Fachlehrer und der Klassenlehrer tragen etwas für die Mathezeile ein) ein oder wurde bereits eine Eintragung in die MyMagellan-Dateien exportiert, werden die Eingaben nacheinander importiert, die zuletzt importierte Information bleibt in Magellan bestehen.   

## Zeugnisbemerkungen

!!! warning "Wichtig"

	Zeugnisbemerkungen können nur für Schüler editiert und importiert werden, für die der Kollege entweder als Klassenleiter in Magellan hinterlegt wurde, oder als Tutor. 

Stand in Magellan/MyMagellan |Ergebnis
-|-
Bemerkung in Magellan existiert, MyMagellan-Datei wird erzeugt|Bemerkung wird mit in die MyMagellan-Datei übergeben
Bemerkung wird in MyMagellan aktualisiert<br/>Bemerkung wird in Magellan neu angelegt|Bemerkungen werden beim Import in Magellan gelöscht und durch aktualisierte oder neue Bemerkungen aus MyMagellan ersetzt
Neue Bemerkung wird in Magellan erfasst,<br/>während die MyMagellan-Dateien ausgeteilt sind|Bemerkungen wird beim Import in Magellan gelöscht und durch aktualisierte oder neue Bemerkungen ersetzt. Sind keine neuen Bemerkungen in MyMagellan erfasst worden, können als Ergebnis auch KEINE Bemerkungen übrig bleiben.

!!! warning "Wichtig"

	Beim Erstellen der MyMagellan-Dateien werden bereits in Magellan existierende Zeugnisbemerkungen in die Lehrer-/Tutorendateien mit ausgegeben. 
	Um beim Import keine Dopplungen von Bemerkungen zu erzielen, werden beim Einlesen der Klassenleiterdatei und der Tutorendatei jeweils zuvor die Schülerzeugnisbemerkungen gelöscht. 
	Sollten einem Schüler ein Klassenleiter und ein Tutor zugeordnet worden sein, können damit je nach Einlesereihenfolge Zeugnisbemerkungen überschrieben werden.

Beispiel:

Schüler S1 wurden Lehrer L1 und Tutor T1 zugeordnet. Beim Erstellen der MyMagellan-Dateien haken Sie versehentlich beide Rollen an, also Klassenleiter- und >Tutorendatei erstellen.
Eventuell in Magellan bereits existente Zeugnisbemerkungen werden für S1 ausgespielt.
L1 vergibt eine neue Zeugnisbemerkung, T1 vergibt keine neue Zeugnisbemerkung. Die Dateien von L1 und T1 werden wieder importiert.

Import der Datei von L1: Zeugnisbemerkungen werden für S1 gelöscht, neue und alte Zeugnisbemerkung werden aus der Datei von L1 importiert.

Als nächstes wird die Datei für T1 importiert: die Zeugnisbemerkungen von S1 werden gelöscht (neue und alte reimportierte Zeugnisbemerkungen), nur die alten Zeugnisbemerkungen werden eingelesen. Im Ergebnis fehlen die neuen Zeugnisbemerkungen von L1.
Sie können den Konflikt nur lösen, indem Sie entweder:

* entweder Schülern nicht einen Klassenleiter UND einen Tutor zuweisen
* oder falls beide Felder für Schüler vergeben sind, beim Erstellen der Dateien nicht Tutor- und Klassenleiterdateien gemeinsam erstellen, sondern nacheinander, also erst die Dateien für die zweite Rolle **nach** dem Einsammeln der Daten der ersten Rolle verteilen.

## Fehlzeiten

Folgende Felder sind gemeint:

|Felder|Anmerkung|
|--|--|
|**Fehltage**|Je nach Auswahl beim Erstellen der Datei: kein Aktualisieren, Addieren oder Ersetzen. <br/>Wird die Option "Fehlstunden/-tage in Magellan beim Einsammeln überschreiben" gewählt, wird beim Einsammeln ein Unterschied zwischen `kein Eintrag` (leer) und einer 0 gemacht. <br/>Die 0 wird berücksichtigt, überschreibt also gegebenenfalls einen vorher importierten Eintrag, ist das Feld leer, wird nichts beim Einlesen geändert.|
|**davon unentschuldigt**|analog der Beschreibung für `Fehltage`|
|**Fehlstunden**|analog der Beschreibung für `Fehltage`|
|**davon unentschuldigt**|analog der Beschreibung für `Fehltage`|
|**Fehltage Praktikum**|analog der Beschreibung für `Fehltage`|
|**davon unentschuldigt**|analog der Beschreibung für `Fehltage`|
|**Unterrichtstage**|Kein Addieren, der Wert wird übertragen. <br/>Kein Eintrag aus MyMagellan wird nicht nach Magellan übergeben, überschreibt also keinen Magellan-Wert.
|**Versäumnisse**|Kein Addieren, der Wert wird übertragen. <br/>Kein Eintrag aus MyMagellan wird nicht nach Magellan übergeben, überschreibt also keinen Magellan-Wert.|

![Bei Fehlzeiten richtet es sich danach, welche Option Sie beim Erzeugen der MyMagellan-Datei gewählt haben.](/assets/images/mymagellan/mym_13.fehlzeitoptionen.png)

Die Option "Fehlstunden/-tage in Magellan beim Einsammeln addieren" ist ungeeignet fürs erneute Einlesen, da die Werte dann wieder aufsummiert werden, also die doppelte Anzahl von Fehlzeiten das Ergebnis wäre.

Gut geeignet ist die Option "Fehlstunden/-tage in Magellan beim Einsammeln überschreiben".

Option|Ergebnis
-|-
Fehlstunden/-tage in Magellan beim Einsammeln überschreiben|Der Eintrag aus der MyMagellan, auch eine gezielt eingetragene 0, überschreibt den Eintrag in Magellan. <br/> **Ausnahme: Es erfolgt kein Eintrag in MyMagellan, also das Feld bleibt leer, in diesem Fall bleiben der Magellan-Eintrag und ggfs. vorab eingelesene Daten erhalten.**
Fehlstunden/-tage in Magellan beim Einsammeln addieren|Fehlstunden/-tage aus allen MyMagellan-Dateien werden aufaddiert. <br/>**Bitte beachten Sie, dass das erneute Einlesen einer Datei bei dieser Option auch erneut die Werte addiert.**
Fehlstunden/-tage in Magellan beim Einsammeln nicht aktualisieren|Es erfolgt keine Änderung in Magellan.

## Zeugnisdaten

Feld|Aktion beim Übertrag nach Magellan
--|--
Abschluss 1|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschluss 2|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschlussart 1|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschlussart 2|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Versetzungsart|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Versetzt|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Leistungsanforderung|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Zeugniskonferenz<br/>(Datum)|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Zeugnisdatum<br/>(Datum)|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschlussdatum 1<br/>(Datum)|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschlussdatum 2<br/>(Datum)|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschlussnote 1|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Abschlussnote 2|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Verhalten|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.
Mitarbeit|Wert aus MyMagellan überschreibt den Wert in Magellan.<br/>Es sein denn, in MyMagellan ist das Feld leer, dann bleibt der Magellan-Wert bestehen.