# Durchschnitt/Abschluss berechnen

Für die Berechnung der Durchschnittsnote(n) und Abschlüsse innerhalb eines Zeitraums existieren unterschiedliche Berechnungsvorschriften. MAGELLAN stellt sehr ausgefeilte Funktionen für die gesamte Durchschnitts- bzw. Abschlussberechnung zur Verfügung. Diese Berechnungen werden mit den grundlegenden Merkmalen in diesem Kapitel vorgestellt. 

> #### warning::Wichtig!
>
> Für welche Bundesländer entsprechende Berechnungsskripte für die Versetzung vorliegen, finden Sie in dem entsprechenden Kapitel in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/).

## Grundlagen

Innerhalb eines Zeitraums können Noten eines Schülers über dessen Versetzung bzw. Durchschnittsnote entscheiden. Die dazu notwendigen Berechnungen basieren auf Verordnungen der jeweiligen Bundesländer. Diese Berechnungen erfolgen aufgrund der [MAGELLAN-Scripting-Technologie](https://doc.MAGELLAN-scripting.stueber.de/). Auf Basis der berechneten Noten einer Verordnung und der damit verbundenen Durchschnittsnote können Sie dann die eigentlichen Zeugnisse ausdrucken. Dabei kann jede berechnete Endnote bzw. Durchschnittsnote auch noch manuell aufgrund des pädagogischen Freiraums abgeändert werden. Die zeitraumbezogenen Versetzungs-/Durchschnittsberechnungen basieren auf MAGELLAN-Skripten, die Sie mit Hilfe des MAGELLAN-Skripteditors bearbeiten können.

## Vorbereitungen

Zur Berechnung der Durchschnittsnote(n) und Abschlüsse innerhalb eines Zeitraums gehören folgende Aufgaben:

1. Klassen und andere Stammdaten einrichten

2. Fächer der Schüler für den gewünschten Zeitraum einer Zeugnisausgabe eingeben.

3. Noten pro Fach der Schüler für den gewünschten Zeitraum einer Zeugnisausgabe eingeben.

4. Endnoten / Durchschnittsnoten berechnen


Alle Schritte werden in MAGELLAN ausgeführt. Die Aufgaben 1 und 2 sind schon allgemein in den vorangegangenen Kapiteln ausführlich erläutert werden. Es werden daher nur die Besonderheiten für die Aufgaben 3 und 4 vorgestellt. Für die Vorbereitung der Berechnung müssen Sie folgende Daten definieren.

1. Berechnungsverordnung definieren

2. Zusätzliche Noten definieren

### Berechnungsverordnung definieren
 
![Geben Sie hier die Berechnungsverordnung mit der Kategorie „Versetzung“ ein.](/images/durchschnitt/durchschnitt1.png)

Sie müssen für jeden Schüler die Berechnungsverordnung angeben, die für ihn relevant ist. Dazu müssen Sie im Schlüsselverzeichnis `Verordnungen` die jeweilige Berechnungsverordnung definieren. Klicken Sie dazu auf `Extras > Schlüsselverzeichnisse > Verordnungen` und geben Sie dort die Verordnung wie folgt an:

Spalte      | Bedeutung
----------- | ---------
Kürzel      | Kurzbezeichnung der Verordnung (max. 8stellig)
Bezeichnung | Bezeichnung der Verordnung
Kategorie   | Wenn Sie hier „Versetzung“ eingeben, wird die Verordnung bei den Schülern auf der Registerkarte `Zeugnis > Leistungen` angezeigt
Gültig von  | Gültigkeitsdatum von, ohne Bedeutung für die Berechnungen
Gültig bis  | Gültigkeitsdatum bis, ohne Bedeutung für die Berechnungen
Skript      | Geben Sie hier den Namen des Skripts für diese Berechungsverordnung ein. Alle verfügbaren Skripte befinden sich im MAGELLAN-Verzeichnis SKRIPTE.

### Zusätzliche Noten definieren

Beinhaltet Ihre Verordnung die Berechnung/Verwendung von Zwischendurchschnittsnoten, so sind diese möglichen Noten eventuell als zusätzliche Noten in Ihr Verzeichnis der Noten aufzunehmen.
 
![Die Noten „2,8“ oder „3,7“ in der Spalte "Schriftl. Note 2" können nur eingetragen werden, wenn dies auch im Verzeichnis der Noten „Verzeichnisse > Noten“ definiert sind.](/images/durchschnitt/durchschnitt2.png)

Welche Verordnung Zwischendurchschnittsnoten bzw. besondere Kommanoten verwenden, können Sie den Berechnungsskripten für die Versetzung in dem entsprechenden Kapitel im Dokument [Landesanpassungen](https://doc.la.stueber.de/) entnehmen.

## Noten zur Berechnung eingeben

Um die Berechnungen durchzuführen, müssen Sie zunächst die Noten der Schüler eintragen. Wie Sie schon im Kapitel „Noteneingabe“ erfahren haben, werden dazu die Noten der Schüler auf der Registerkarte `Zeugnisse > Leistungen` pro Schüler eingetragen. Im Unterschied zum Regelfall der Noteneingabe, wo die Noten in der Spalte `Endnote` eingegeben werden, können je nach Berechnungsskript für die jeweilige Verordnung die Noten in ein oder mehreren Spalten auf der Registerkarte `Leistungen` eingetragen werden. Welche Spalte die genau sind und welche Spalten sich evtl. automatisch berechnen, können Sie den Berechnungsskripten für die Versetzung in dem entsprechenden Kapitel der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/) entnehmen.

## Berechnung durchführen

Markieren Sie für den Schüler auf der Registerkarte `Zeugnisdaten > Leistungen` das Optionsfeld `Durchschnitt einblenden`. Auf der rechten Seite der Registerkarte erscheint nun eine zusätzliche Leiste.

### Automatische Berechnung

Geben Sie unter `Prüfungsordnung` die gewünschte Prüfungsordnung zur Versetzung an. Klicken Sie auf `Neu berechnen`, um die Daten automatisch durch das entsprechende Skript berechnen zu lassen. Durch die Berechnungen werden automatisch die Noten in die Spalte `Endnote` und/oder Durchschnitte 1-3 in Abhängigkeit vom Skriptinhalt eingetragen. Im automatisch erzeugten Meldungsfenster werden zusätzliche Statusinformationen zur Berechnung angezeigt. Insbesondere wird hier eine Aussage über die erfolgreiche Durchführung der Berechnung und eventuell notwendige Zwischensummen angezeigt. 

Die nachfolgende Abbildung zeigt ein Berechnungsbeispiel für die Berufsschule in Baden-Württemberg.

![Meldung nach der automatischen Berechnung der Durchschnittsnote.](/images/durchschnitt/durchschnitt3.png)

### Manuelle Eingabe/Korrektur der Ergebnisse

Alle Ergebnisse können neben der automatischen Berechnung auch manuell eingegeben werden. Sie können so auch die Eingabe von bereits festgelegten Endnoten nutzen. Insbesondere können Sie die manuelle Eingabe aber im Sinne der Korrektur einer zuvor automatisch durchgeführten Berechnung der Endnoten bzw. Durchschnitte nutzen. Hat beispielsweise die automatische Berechnung ergeben, dass der Schüler genau zwischen zwei Noten steht, so können Sie aufgrund des pädagogischen Ermessens in solchen Fällen z.B. die Durchschnittsnote manuell eintragen.
