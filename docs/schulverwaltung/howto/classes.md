# Klassen

In diesem Kapitel wird Ihnen gezeigt, wie Sie Klassen in MAGELLAN aufnehmen und verwalten.

## Klassen eingeben

Klassendaten besitzen immer einen Zeitraumbezug. Sie stellen das Bindeglied zwischen Zeiträumen und Schülern dar. Jeder Klasse ist mindestens ein Zeitraum zugeordnet. Klassen sind mit ihren Schülern und den zugehörigen Fächern in jedem Zeitraum einzigartig.
Klassen existieren in MAGELLAN genausolange, wie in der Realität an Ihrer Schule. 

Schultyp|Beispiel
--|--
ABS|Eine Klasse 5a existiert genau eine Schuljahr lang, also zwei Halbjahre. Im Jahr darauf wird es eine neue Klasse 5a geben, um die Schüler der 4a zu versetzen oder beispielsweise auch einen Schüler der alten 5a wiederholen zu lassen. MAGELLAN verwaltet alle Datensätze, also auch Ihre Klassen anhand einer eindeutigen ID, hier kann nichts durcheinander geraten. 
BBS|An Berufsbildenden Schulen können Klassen länger existieren, so kann beispielsweie eine Berufsschulklasse für Bürokaufleute (BüKo2018) aktuell starten und insgesamt 3 Jahre, also 6 Halbjahre lang laufen. Dennoch startet in jedem Jahr eine neue Klasse mit Bürokaufleuten (BüKo2019), die dann ein Jahr länger existiert, als ihre Vorgängerklasse.

### Neue Klasse aufnehmen

Um eine neue Klasse anzulegen, klicken Sie in der Startleiste auf der linken Bildschirmseite auf `Klassen `oder wählen Sie `Ansicht > Klassen`. Wählen Sie dann das Plus in der oberen Symbolleiste oder die Tastenkombination `STRG+N`. Es öffnet sich das Dialogfenster `Neue Klasse`.

![Hier geben Sie eine neue Klasse ein.](/assets/images/lehrer.klassen_08neu.klasse.png)


Geben Sie mindestens das Kürzel der neuen Klasse ein und klicken Sie auf `OK`. Die Klasse ist nun neu aufgenommen und Sie befinden sich automatisch auf der Registerkarte „Daten“ dieser Klasse, um deren weitere Daten zu erfassen. Optional können Sie im Dialogfenster `Neue Klasse` auch direkt einen Langnamen in den Feldern „Langname 1“ und „Langname 2“ bzw. eventuell das für die Statistik verwendete Statistikkürzel der Klasse eintragen. Diese Angaben können Sie aber auch zu einem späteren Zeitpunkt auf der Registerkarte „Daten“ der Klasse angeben.

### Registerkarte „Daten“

Auf der Registerkarte „Daten“ sind insbesondere die Einstellungen bei „Klassenart“ und „Beurteilungsart“ wichtig.

![Ansicht "Klassen > Daten"](/assets/images/lehrer.klassen_09daten.png)


Bei der `Klassenart `müssen Sie die Art der Klasse festlegen. Diese Einstellungen haben insbesondere Auswirkungen auf den Bereich „Abitur“ und „Berufsschule“ in MAGELLAN. 

Durch die `Beurteilungsart `legen Sie fest, wie die Beurteilungen der Leistungen der einzelnen Schüler in der Klasse erfolgen sollen. Im Standardfall erfolgt die Beurteilung durch Noten. Bei Grundschulklassen können beispielsweise reine Beurteilungstexte genutzt werden. In der Oberstufe ist die Beurteilung durch Punkte möglich. 

Die Felder `Beruf`, `Bildungsgang `und `Berufsfeld `sind nur für Berufsbildende Schulen von Interesse. Die bei diesen drei Feldern vorgenommenen Einstellungen sind Standardvorgaben für alle Schüler der Klasse, die im Bedarfsfall auch pro Schüler abgeändert werden.

### Registerkarte „Zeiträume“

Auf dieser Registerkarte sind alle Zeiträume der Klasse in einer Liste eingetragen. Pro Zeitraum werden die Schüler der Klasse angezeigt werden. Pro Zeitraum können auf der rechten Seite auf der Registerkarte Zeitraum bestimmte Angaben vorgenommen werden.

![Übersicht der Klassenzeiträume](/assets/images/lehrer.klassen_10zeitraeume.png)


!!! info "Hinweis"

	Klassen in Allgemeinbildenden Schulen besitzen im Regelfall zwei Zeiträume (1. und 2. Halbjahr des Schuljahres).
Klassen in Berufsbildenden Schulen besitzen im Regelfall zwei (einjährige Klasse), vier (zweijährige Klasse) oder sechs (dreijährige Klasse) Zeiträume.

Unter `Klassenleiter 1` und `Klassenleiter 2` können Sie den Klassenleiter und seinen Vertreter eintragen. Diese Eintragung ist wichtig für die Benutzerverwaltung: anhand dieser Zuordnung wird die Eintragung der Leistungen (für Schüler dieser Klasse) für den erfassten Kollegen ermöglicht.

Das Feld `Fachtafel `kann eine zuvor definierte Fachtafel besitzen, welche Sie später bei der Eingabe der Zeugnisdaten der Schüler nutzen können.

Je nach Inhalt des hinterlegten Verzeichnisses wird im Feld `Organisation`zum Beispiel zwischen Vollzeit und Teilzeit unterschieden. Das Schlüsselverzeichnis finden Sie unter `Verzeichnisse > weitere Schlüsselverzeichnisse|Organisationen`.

Im Feld `Jahrgang `tragen Sie den Klassenjahrgang ein, dass ist vor allem für Oberstufenklassen eine Voraussetzung zum späteren Synchronisieren der Schüler in das Menü Abitur. Sollten in der Klasse Schüler aus verschiedenen Jahren gemeinsam unterrichtet werden, gibt es alternativ auch einen Jahrgang pro Schüler unter `Schüler > Zeugnis > Details`, dieser Jahrgang kann auch automatisch beim Fortschreiben oder Versetzen der Schüler erhöht werden.

Erfassen Sie in diesem Feld zum Beispiel für Berufsschulklassen die Anzahl der `Unterrichtstage`.

Die Felder `Elternsprecher/Schülersprecher/Wahlvertreter` können erst gewählt werden, wenn Schüler in die Klasse eingeschult wurde, denen (für die Zuordnung des Elternsprechers/Wahlvertreters) Sorgeberechtigte zugewiesen wurden.


Im Feld `Fachtafel` kann für die Klasse pro Klassenzeitraum eine Fachtafel vorgemerkt werden. Die in der Fachtafel enthaltenen Felder können später den Schülern der Klasse über Sammelzuweisung zugewiesen werden.

!!! info "Hinweis"

	Der Inhalt dieses Feldes beinhaltet noch keine Zuweisung der Fächer zu den einzelnen Schülern der Klasse!


![Auf der untergeordneten Registerkarte Schüler sehen Sie zum aktuell markierten Zeitraum alle Schüler der Klasse inkl. deren Aufsummierung im Fuß der Registerkarte.](/assets/images/lehrer.klassen_11zeitraeume2.png)


## Assistent für den Schuljahreswechsel

Für den Schuljahreswechsel steht Ihnen ein Assistent zur Verfügung, der Ihnen Kopien ausgewählter oder aller Klassen des aktuellen Zeitraums für den nachfolgenden Zeitraum erzeugt. Dabei werden neue Klassen, mit neuer ID erzeugt, die die bereits voreingestellten Angaben der „alten“ Klassen übernehmen. 

> #### warning::Wichtig!
>
> **allgemeinbildender Bereich**: Sie verwenden den Assistenten um auf der Basis der bereits existierenden Klassen sich neue Klassen anlegen zu lassen. Beispiel: alle Klassen von der 1a bis zur 10b existieren auch im Folgejahr, daher erzeugen Sie mit dem Assistenten Kopien der bestehenden Klassen um dort neue Schüler einzuschulen und Bestandsschüler zu versetzen. Ein Abändern der Kürzel erfolgt nicht, da die Einstellungen der alten Klassen auch für die neuen Klassen gelten.
>**berufsbildender Bereich:** Für alle im neuen Schuljahr neu startenden Bildungsgänge werden Klassen benötigt. Markieren Sie im Assistenten die Klassen der alten entsprechenden Klassen, vergeben dann die neuen Klassenkürzel/Statistikkürzel (Beispiel: aus BüKo2016 wird Büko2017) und lassen die Klassen neu erzeugen. Bitte passen Sie dann für die neuen Klassen noch die Klassenjahrgänge/-stufen unter `Klassen > Zeiträume` an.

Öffnen Sie in dem Zeitraum, in dem die zu kopierenden Klassen vorhanden sind, den Punkt `Klassen > Auswahlliste > Rechtsklick > Schuljahreswechselassistent`.

![Aufruf des Schuljahreswechselassistenten](/assets/images/lehrer.klassen_12schuljahreswechsel1.png)



![Auswählen der Klassen im Schuljahreswechselassistent](/assets/images/lehrer.klassen_12schuljahreswechsel.png)


Wählen Sie die zu kopierenden Klassen aus.

![Anpassen der Kürzel für die neuen Klassen](/assets/images/lehrer.klassen_13schuljahreswechsel2.png)


Sie können auf dieser Karte die Kürzel und die Statistikkürzel der neuen Klassen (nur für den berufsbildenden Bereich) festlegen. Diese Eingaben könnten Sie aber auch später unter `Klassen > Daten` vornehmen.