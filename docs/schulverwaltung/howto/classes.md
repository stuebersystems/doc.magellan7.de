# Klassen

In diesem Kapitel wird Ihnen gezeigt, wie Sie Klassen in MAGELLAN aufnehmen und verwalten.

Klassendaten besitzen immer einen Zeitraumbezug. Sie stellen das Bindeglied zwischen Zeiträumen und Schülern dar. Jeder Klasse ist mindestens ein Zeitraum zugeordnet. Klassen sind mit ihren Schülern und den zugehörigen Fächern in jedem Zeitraum einzigartig.
Klassen existieren in MAGELLAN genausolange, wie in der Realität an Ihrer Schule.

Schultyp|Beispiel
--|--
ABS|Eine Klasse 5a existiert genau eine Schuljahr lang, also zwei Halbjahre. Im Jahr darauf wird es eine neue Klasse 5a geben, um die Schüler der 4a zu versetzen oder beispielsweise auch einen Schüler der alten 5a wiederholen zu lassen. MAGELLAN verwaltet alle Datensätze, also auch Ihre Klassen anhand einer eindeutigen ID, hier kann nichts durcheinander geraten.
BBS|An Berufsbildenden Schulen können Klassen länger existieren, so kann beispielsweie eine Berufsschulklasse für Bürokaufleute (BüKo2018) aktuell starten und insgesamt 3 Jahre, also 6 Halbjahre lang laufen. Dennoch startet in jedem Jahr eine neue Klasse mit Bürokaufleuten (BüKo2019), die dann ein Jahr länger existiert, als ihre Vorgängerklasse.

## Neue Klasse anlegen

Um eine neue Klasse anzulegen, klicken Sie in der Startleiste auf der linken Bildschirmseite auf `Klassen` oder wählen Sie `Ansicht > Klassen`. Wählen Sie dann das Plus in der oberen Symbolleiste oder die Tastenkombination `STRG+N`. Es öffnet sich das Dialogfenster `Neue Klasse`.

![Hier geben Sie eine neue Klasse ein.](/assets/images/klassen/lehrer.klassen_08neu.klasse.png)

Geben Sie mindestens das Kürzel der neuen Klasse ein und klicken Sie auf `OK`. Die Klasse ist nun neu aufgenommen und Sie befinden sich automatisch auf der Registerkarte „Daten“ dieser Klasse, um deren weitere Daten zu erfassen. Optional können Sie im Dialogfenster `Neue Klasse` auch direkt einen Langnamen in den Feldern „Langname 1“ und „Langname 2“ bzw. eventuell das für die Statistik verwendete Statistikkürzel der Klasse eintragen. Diese Angaben können Sie aber auch zu einem späteren Zeitpunkt auf der Registerkarte „Daten“ der Klasse angeben.

!!! danger "Achtung"

	Wenn Sie beginnen mit MAGELLAN zu arbeiten sollten Sie wie vorstehend beschrieben neue Klassen anlegen. Wenn Sie allerdings bereits Klassendaten eingepflegt haben, können Sie diese Klassen als neue Klassen kopieren lassen. Damit sparen Sie Zeit und es können auch keine beispielsweise statistikrelevanten Eintragungen übersehen werden. Bitte lesen hierfür den Abschnitt [Assistent Klassen übernehmen](https://doc.magellan.stueber.de/schulverwaltung/howto/classes/#assistent-klassen-ubernehmen)!

## Registerkarte „Daten“

Auf der Registerkarte „Daten“ sind insbesondere die Einstellungen bei „Klassenart“ und „Beurteilungsart“ wichtig.

![Ansicht Klassen > Daten](/assets/images/klassen/lehrer.klassen_09daten.png)

Bei der `Klassenart `müssen Sie die Art der Klasse festlegen. Diese Einstellungen haben insbesondere Auswirkungen auf den Bereich „Abitur“ und „Berufsschule“ in MAGELLAN.

Durch die `Beurteilungsart `legen Sie fest, wie die Beurteilungen der Leistungen der einzelnen Schüler in der Klasse erfolgen sollen. Im Standardfall erfolgt die Beurteilung durch Noten. Bei Grundschulklassen können beispielsweise reine Beurteilungstexte genutzt werden. In der Oberstufe ist die Beurteilung durch Punkte möglich.

Die Felder `Beruf`, `Bildungsgang `und `Berufsfeld `sind nur für Berufsbildende Schulen von Interesse. Die bei diesen drei Feldern vorgenommenen Einstellungen sind Standardvorgaben für alle Schüler der Klasse, die im Bedarfsfall auch pro Schüler abgeändert werden.

## Registerkarte „Zeiträume“

Auf dieser Registerkarte sind alle Zeiträume der Klasse in einer Liste eingetragen. Pro Zeitraum werden die Schüler der Klasse angezeigt werden. Pro Zeitraum können auf der rechten Seite auf der Registerkarte Zeitraum bestimmte Angaben vorgenommen werden.

![Übersicht der Klassenzeiträume](/assets/images/klassen/lehrer.klassen_10zeitraeume.png)

!!! info "Hinweis"

	Klassen in Allgemeinbildenden Schulen besitzen im Regelfall zwei Zeiträume (1. und 2. Halbjahr des Schuljahres).
Klassen in Berufsbildenden Schulen besitzen im Regelfall zwei (einjährige Klasse), vier (zweijährige Klasse) oder sechs (dreijährige Klasse) Zeiträume.

Unter `Klassenleiter 1` und `Klassenleiter 2` können Sie den Klassenleiter und seinen Vertreter eintragen. Diese Eintragung ist wichtig für die Benutzerverwaltung: anhand dieser Zuordnung wird die Eintragung der Leistungen (für Schüler dieser Klasse) für den erfassten Kollegen ermöglicht.

Das Feld `Fachtafel` kann eine zuvor definierte Fachtafel besitzen, welche Sie später bei der Eingabe der Zeugnisdaten der Schüler nutzen können.

Je nach Inhalt des hinterlegten Verzeichnisses wird im Feld `Organisation`zum Beispiel zwischen Vollzeit und Teilzeit unterschieden. Das Schlüsselverzeichnis finden Sie unter `Verzeichnisse > weitere Schlüsselverzeichnisse|Organisationen`.

Im Feld `Jahrgang` tragen Sie den Klassenjahrgang ein, dass ist vor allem für Oberstufenklassen eine Voraussetzung zum späteren Synchronisieren der Schüler in das Menü Abitur. Sollten in der Klasse Schüler aus verschiedenen Jahren gemeinsam unterrichtet werden, gibt es alternativ auch einen Jahrgang pro Schüler unter `Schüler > Zeugnis > Details`, dieser Jahrgang kann auch automatisch beim Fortschreiben oder Versetzen der Schüler erhöht werden.

Erfassen Sie in diesem Feld zum Beispiel für Berufsschulklassen die Anzahl der `Unterrichtstage`.

Die Felder `Elternsprecher/Schülersprecher/Wahlvertreter` können erst gewählt werden, wenn Schüler in die Klasse eingeschult wurde, denen (für die Zuordnung des Elternsprechers/Wahlvertreters) Sorgeberechtigte zugewiesen wurden.

Im Feld `Fachtafel` kann für die Klasse pro Klassenzeitraum eine Fachtafel vorgemerkt werden. Die in der Fachtafel enthaltenen Felder können später den Schülern der Klasse über Sammelzuweisung zugewiesen werden.

!!! info "Hinweis"

	Der Inhalt dieses Feldes beinhaltet noch keine Zuweisung der Fächer zu den einzelnen Schülern der Klasse!

![Auf der untergeordneten Registerkarte Schüler sehen Sie zum aktuell markierten Zeitraum alle Schüler der Klasse inkl. deren Aufsummierung im Fuß der Registerkarte.](/assets/images/klassen/lehrer.klassen_11zeitraeume2.png)

## Assistent "Klassen übernehmen"

Neue Klassen können Sie aus dem Menü `Klassen` per `STRG+N` oder über die Plusschaltfläche erzeugen.

Wenn Sie aber bereits mit MAGELLAN arbeiten, dann haben Sie bereits Klassen angelegt und mit den für Sie und Ihre Region wichtigen Einstellungen versehen. Auf der Basis Ihrer bestehenden Klassen erzeugt der Assistent `Klassen übernehmen` neue Klassen für Sie. Kurz gesagt: Sie wählen bestehende Klassen und ein Assistent erzeugt neue Klassen mit neuer ID, aber mit fast allen bisher verwendeten Einstellungen.
Nicht mit übernommen werden die Eintragungen, die aufgrund der Schüler in der Klasse getroffen wurden, also es wird beispielsweise kein Elternvertreter oder Klassensprecher übernommen.

Es gibt noch einen Unterschied zwischen ABS- und BBS-Klassen:

### Allgemeinbildende Schulen

Sie benötigen je nach Schulart jedes Schuljahr neue Klassen von der 1. Klasse bis zur 13. Klasse um neue Schüler einschulen zu können und um Ihre bestehenden Schüler in die nächsthöhere Klasse (Wiederholer dann beispielsweise von der alten Klasse 5 in dei neue Klasse 5) versetzen zu können. Am Kürzel ändern Sie im nachstehend erklärten Assistenten nichts, aus der alten 5a wird einfach eine neue 5a erzeugt - die in der alten Klasse gewählten Einstellungen (Jahrgang, Fachtafel usw) passen dann und werden übernommen.

### Berufsbildende Schulen

Sie benötigen in der Regel nicht für Schüler eine neue Klasse, da die meisten Schüler solange ein Bildungsgang dauert in derselben Klasse bleiben. Sie benötigen aber neue Klasse für neue Bildungsgänge. Sollten Sie ein berufliches Gymnasium sein, kann es auch hier, dass Sie die Schüler nicht durchgehend fortschreiben, sondern wie im allgemeinbildenden Bereich im Wechsel Fortschreiben und Versetzen (Beispiel: Noten in der 11, Punkte ab der 12, in diesem Fall würden die Schüler versetzt werden müssen, um die geänderte Benotung darstellen zu können).
Wenn Sie Ihre Klassenkürzel wie folgt aufbauen, kann der Assistent auch die Jahreszahlen im Klassenkürzel/Statistikkürzel anpassen:

Maler_2019 oder Maler_19

Tragen Sie den Teil des Kürzels, der später als Alpha erkannt werden soll im gleichnamigen Feld unter `Klassen > Daten > Alpha` ein.

![Alpha vorbelegen bei den Klassen](/assets/images/schuljahreswechsel/klassen_uebernehmen01.png)

Diese Vorbelegung kann man später im Assistenten einfach austauschen lassen.

|Aktion|
|:--|
|1. Wechseln Sie ins neue Schulhalbjahr und rufen das Menü ``Laufbahnprozesse > Klassenübernehmen`` auf!|
|2. Der Assistent zeigt Ihnen die Klassen des letzten Halbjahres an. <br/>**Berufsbildende Schulen:**<br/>Wenn Sie das Klassenalpha anpassen möchten, müssen Sie vor der Übernahme der Klassen auf der rechten Seite ins Feld `Alpha` bitte Ihr neues `Alpha` (Beispiel: 2020 oder 20) eintragen!|
|3. Markieren Sie die Klassen, die Sie fürs dieses Schuljahr benötigen und klicken auf das Plus oben links, um Ihre Auswahl in die rechte Fensterhälfte zu übernehmen.|
|**Abbildung:** <img src=/assets/images/schuljahreswechsel/klassen_uebernehmen02.png>|
|**Abbildung:** <img src=/assets/images/schuljahreswechsel/klassen_uebernehmen03.png>|
|4. Auf der rechten Seite haben Sie die Möglichkeit die Klassenkürzel oder Bezeichnungen anzupassen. Sollten Sie versehentlich zu viele Klassen übernommen haben, können Sie die Klassen auch auf der rechten Seite markieren und über das Minus links oben wieder entfernen. Wenn die Auswahl stimmt klicken Sie bitte auf `Fertigstellen`, die neuen Klassen werden angelegt.|

!!! info "Hinweis"

  Wir empfehlen zum Anlegen von Klassen fürs neue Schuljahr diesen Assistenten zu verwenden, Sie können so gut sicherstellen, dass immer alle relevanten Einstellungen (zum Beispiel die Klassenfachtafel, die Klassenart, der Jahrgang usw.) für die Klassen vergeben wurden.