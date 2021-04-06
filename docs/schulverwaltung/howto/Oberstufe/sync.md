# Schüler synchronisieren

Bevor Schülerdaten für die Fachwahl oder beispielsweise für die Abiturberechnung im Modul `Abitur` sichtbar werden, müssen die Daten synchronisiert werden. Bei der Synchronisation werden Daten, die Sie zuvor im Menü `Schüler`, im Menü `Klassen` und in einigen Schlüsselfeldern angelegt haben ausgewertet und je nach gefundenen Eintragungen im Menü `Abitur` dargestellt.

Wollen Sie Schülerdaten für die Karte `Fachwahl` des Schülers synchronisieren, werden nur die Schülerdaten und die Schülerklasse synchronisiert, Fachdaten oder Noten spielen hier noch keine Rolle und werden nicht übertragen.

Wollen Sie Schüler synchronisieren um im nächsten Schritt eine Abiturberechnung auszuführen, werden zusätzlich Fach- und Leistungsdaten der Oberstufenhalbjahre extrahiert und in das Menü `Abitur` synchronisiert.

## Voraussetzungen zum Synchronisieren

Für diese komplexe Aktion werden einige Eintragungen vorausgesetzt:

Eintrag|Bedeutung
--|--
Zeitraumart<br/>`Extras > Schlüsselverzeichnisse > Zeiträume > Art`| Das Feld „Art“ muss mit dem Wert „1. Halbjahr“ bzw. “2. Halbjahr“ gefüllt sein.
Klassenart<br/>`Klassen > Daten > Klassenart`|`Oberstufenjahrgang (Leistungs- und Grundkurse)` oder`Oberstufenjahrgang (nur Kurse)`:<br/>Synchronisation der Schüler-, Fach- und Leistungsdaten der Oberstufenhalbjahre. <br/><br/>`Standardklasse mit Oberstufensynchronisation`: Synchronisation ohne Fach- und Leistungsdaten (als Vorbereitung für die Fachwahl des Schülers).
Jahrgang<br/>`Klassen > Zeiträume > Jahrgang`|Bei jeder Klasse/Jahrgang muss auf der Registerkarte „Zeiträume“ für jeden Zeitraum das Feld „Jahrgang“ mit dem Wert "10",„11“, „12“ oder „13“ angegeben werden. | Bei jeder Klasse/Jahrgang muss auf der Registerkarte „Zeiträume“ für jeden Zeitraum das Feld „Jahrgang“ mit dem Wert "10",„11“, „12“ oder „13“ angegeben werden.
Abschlussjahrgänge<br/>`Extras > Schlüsselverzeichnisse > Zeiträume > Abschlussjahrgänge` |  Bitte legen Sie die Abschlussjahrgänge an. Es genügt dabei die Angabe des Kürzels, der Bezeichnung und der Kategorie (Abitur).
Verordnungen<br/>`Extras > Schlüsselverzeichnisse > Zeiträume > Verordnungen` | Richten Sie bitte pro verwendeter Abiturverordnung oder Fachwahl eine Zeile entsprechend der Anleitung [http://doc.la.stueber.de/](http://doc.la.stueber.de/) ein.

## Was passiert beim Synchronisieren

Als erstes ist zu unterscheiden welche Klassenart die Klassen haben, denen der Schüler zugewiesen ist. Ist es `Standard mit Oberstufensynchronisation` werden die Schüler mit dem Klassenkürzel ins Menü `Abitur` synchronisiert, Fach- oder Leistungdaten spielen hier keine Rolle.

Deutlich komplexer ist der Prozess, wenn die Klassenart `Oberstufenjahrgang (Grund- und Leistungskurse)` oder `Oberstufenjahrgang (nur Kurse)` zugewiesen wurde. Beide Klassenarten sind funktionell absolut gleichwertig, der Unterschied liegt tatsächlich nur in der Benennung.

Wenn  diese Auswahl getroffen wurde, werden für die Schüler alle Fach- und Leistungsdaten der Oberstufenjahrgänge extrahiert.

Folgender Ablauf:
Es wird geprüft, welche Halbjahresdaten für den Schüler ausgelesen werden sollten (Klassenart, Klassenjahrgang), dann ergibt sich eine Liste mit Daten, nachfolgende ein Beispiel für ein Fach für ein Halbjahr:

* Jahrgang im Verzeichnis `Verordnungen`: 11
* Fach: Deu
* Klassenjahrgang: 11
* Endnote: 15
* Zeitraumart: 1. Halbjahr
* Unterrichtsart: GK
* Fachstatus: leer
* Merkmal: leer
* Lehrer: Bru
* Bestanden: leer
* Leistungsart: Klausur

Anhand dieser Daten kann die Information in der Qualifikationsmatrix eingetragen werden, bei G9 ( Wert 11 Jahrgang im Verzeichnis `Verordnungen`) wäre die 11.1 die Spalte `E1`. Die Daten des Halbjahres werden der Reihe nach übertragen.

Wird im Anschluss beim Durchlauf des nächsten Halbjahres wieder eine Zeile mit dem Fach Deu gefunden, wird keine neue Zeile eröffnet, sondern nur der Notenwert 
aus der Spalte Endnote in das passende Kurshalbjahr eingetragen. Wäre die Unterrichtsart oder der Fachstatus abweichend, würde der zuerst erfasste Wert überschrieben, am Ende des Durchlaufs würde der letzte Wert erhalten bleiben (Ausnahmen im Abschnitt "Besondere Optionen").

### Wiederholer

Der vorangegangene Ablauf geht davor aus, dass jedes Oberstufenhalbjahr nur einmal existiert. Wiederholt ein Schüler können die Listen der Halbjahresdaten mehrfach erscheinen. Beispiel: der Schüler wiederholt die Klasse 11, dann hat er abschließend zweimal Fächer und Leistungen für die 11.1 und auch zweimal für die 11.2.
Eigentlich könnten wir jetzt einfach die Daten des ersten Durchgangs mit denen des zweiten Durchgangs überschreiben, sollte aber ein Umwahl von Fächern vorgenommen worden sein, ist das Ergebnis fehlerhaft.
Aus diesem Grund werden beim Übertragen sobald Daten einer Wiederholung gefunden werden, alle Noten des ersten Durchlaus, also in unserem Beispiel der ersten 11.1 und der ersten 11.2 überschrieben.

### Anzeige von Wiederholernoten im Abitur

Bei der Synchronisation der Oberstufenergebnisse auf die Qualifikationskarte werden für wiederholte Halbjahre nur die zuletzt erworbenen Leistungen überragen. Möchten Sie alle Leistungen sehen, die in der Oberstufe erworben wurden, können für Wiederholer die Daten angezeigt werden.

Folgenden Daten sind dafür Voraussetzung:

* `Klassen > Daten > Klassenart` = Oberstufenjahrgang
* `Klassen > Zeiträume > Jahrgang` = 11, 12 oder 13 (ein Eintrag je Klassenzeitraum)
* `Schüler > Laufbahn > Wiederholer` = Wiederholerhäkchen für das erste Halbjahr des Wiederholerjahrs soll gesetzt sein 

Beispiel:
Der Schüler hat die Klasse 11 wiederholt, in seiner Laufbahn ist für das erste Halbjahr in dem er wiederholt der "Wiederholer-Haken" aktiviert.

![Wiederholer-Häkchen für 11.1 im 1.HJ 21/22 gesetzt ](/assets/images/changelog/aenderungen8/12.png)

In der Abituransicht `Qualifikation` werden nach dem Aufruf über die Schaltfläche `Wiederholernoten` alle Fächer und Noten aus der Oberstufe für den Schüler (und alle anderen Wiederholer) gezeigt. Sie können die Daten filtern, gruppieren oder sortieren um die gewünschte Auswahl zu zeigen. sie können diese Daten als Vorlage nutzen um manuell Anpassungen der Leistungen auf der Karte `Qualifikation` vorzunehmen.

![Anzeige aller Oberstufenleistungen ](/assets/images/changelog/aenderungen8/13.png)

!!! danger "Achtung"

    Bitte beachten Sie, dass bei erneuter Synchronisation der Schülerleistungen die manuelle Anpassung zurückgesetzt wird.

## Die Synchronisation

Den Assistenten zum Synchronisieren der Schülerdaten rufen Sie im Menü `Abitur` über die Schaltfläche am oberen Fensterrand auf. 

![Synchronisation aufrufen](/assets/images/gym_oberstufe/01sync.png)

Es werden Ihnen nur Schüler angeboten, die in einer Klasse sind, die eine der oben genannten Klassenarten hinterlegt hat.

![Dialogfenster zum Synchronisieren der Daten für das Abitur](/assets/images/gym_oberstufe/gym_oberstufe03.png)


|Beim Synchronisieren prüft MAGELLAN die `Klassenart` unter `Klasse > Daten`|
|--|
|** Oberstufenjahrgang (Leistungs- und Grundkurse)** <br/> **Oberstufenjahrgang (nur Kurse)**<br/><br/>MAGELLAN synchronisiert die Schülerdaten, Schülerfachdaten und in den Halbjahren erfassten Leistungen.|
|** Standard mit Oberstufensynchronisation**<br/><br/>MAGELLAN synchronisiert die Schülerdaten als Voraussetzung für die Fachwahl, keine Fächer oder Leistungen. In der Regel trägt man diese Klassenart für den Jahrgang 10 ein, da die Schüler sich in der Jahrgangsstufe 10 für die Fachwahl in der Oberstufe entscheiden.

!!! info "Hinweis"

	 MAGELLAN extrahiert für die markierten Schüler die Fachdaten der Halbjahre 11/1 bis 13/2 (bei G9) bzw. 10/1 bis 12/2 (bei G8) und ordnet die Daten in den Spalten E1 bis Q4 auf der Qualifikationskarte im Menü Abitur an. 
     Ob die Schülerdaten passend nach dem G8- oder G9-System angeordnet werden, legen Sie im Verzeichnis `Verordnungen` in der Spalte `Jahrgang` an. Was genau Sie dort eintragen, beschreiben wir pro Berechnungsskript in der Dokumentation [Landesanpassungen](https://doc.la.stueber.de/).

![Klassenart für die Oberstufenberechnungen](/assets/images/gym_oberstufe/oberstufe02.png)

## Besondere Optionen

Im Assistenten gibt es folgende Optionen:

![Synchronisation aufrufen](/assets/images/gym_oberstufe/02sync.png)

Option|Auswirkung
--|--
getrennt nach Unterrichstart| Der Assistent würde für ein Fach, dass mehrfach mit verschiedenen Unterrichtsarten für den Schüler geführt wurde eigentlich nur eine Fachzeile anlegen. Wählen Sie dieses Häkchen wird das Fach mehrfach getrennt nach Unterrichtsart auf der Qualifikationskarte angelegt.
Fachstatus nicht überschreiben|Ohne diese Option würde der Fachstatus, der in den Halbjahresdaten des Schülers unter Schüler > Zeugnis > Fächer/Leistungen geführt wurde auf die Karte Qualifikation übergeben werden. Wenn Sie diese Eintragung direkt auf der Karte `Qualifikation` vorgenommen haben, setzen Sie das Häkchen um diese Eintragung trotz Synchronisation beizubehalten.

## "Bestanden" und "Leistungsart"

Für Nordrhein-Westfalen gibt es die Felder `Bestanden` und `Leistungsart`, die wahlweise bereits beim Schüler unter `Schüler > Zeugnis > Leistungen` je Halbjahr erfasst werden können. Diese Daten werden beim Synchronisieren mit auf die Karte `Qualifikation` übertragen und dort je Kurshalbjahr (E1-Q4) dargestellt.

!!! warning "Wichtig"

    Bitte entscheiden Sie sich für den Eintrag unter `Schüler > Zeugnis > Leistungen` ODER direkt im Abitur. Eine gemischte Erfassung ist nicht möglich, da rein logisch beim Synchronisieren der Daten keine Unterscheidung möglich ist. Daher würden die Daten auf der Qualifikationskarte stets durch die Daten aus `Schüler > Zeugnis > Leistungen` überschrieben.

![Schüler > Zeugnis > Leistungen](/assets/images/gym_oberstufe/03sync.png)
