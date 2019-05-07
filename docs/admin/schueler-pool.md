# Der SCHÜLERPOOL

Dieses Kapitel erläutert die Nutzung des so genannten SCHÜLERPOOLs innerhalb von MAGELLAN. Der SCHÜLERPOOL ist eine Datenbank mit Schülerstammdaten. Er dient als zentrale Datenbasis und Informationsquelle für die Aufnahme von möglichen Bewerbern an Ihrer Schule. Sie können innerhalb dem SCHÜLERPOOL nach möglichen Bewerber suchen, deren Poolstatus abfragen und Schüler aus dem SCHÜLERPOOL als Pool-Bewerber an Ihrer Schule aufnehmen.

> #### primary::Hinweis
>
> Die Nutzung der hier beschriebenen Funktionalitäten setzt den Erwerb des Moduls „MAGELLAN-SCHÜLERPOOL“ voraus.

## Pool-Bewerber

### Pool-Bewerber versus Bewerber

In Abschnitt „Bewerber eingeben“ wird die Eingabe der Bewerber beschrieben. Dabei müssen Sie alle Stammdaten des Bewerbers in die entsprechenden Felder eingeben. Mit der Nutzung des MAGELLAN-SCHÜLERPOOLs wird eine Datenbank mit potentiellen Bewerbern für Ihre Schule zur Verfügung gestellt. Die darin enthaltenen Schüler sind schon mit Ihren Stammdaten eingetragen und können in Abhängigkeit von Ihrem Poolstatus als so genannte „Pool-Bewerber“ per Knopfdruck in die Liste der Bewerber übernommen werden. Grundsätzlich haben Sie somit zwei Möglichkeiten Bewerber an Ihrer Schule aufzunehmen:

* Aufnahme als Bewerber: Der Bewerber wird durch Eingabe seiner Stammdaten in die Felder von MAGELLAN erfasst.

* Aufnahme als Pool-Bewerber: Der Bewerber wir nach einer Suche aus dem SCHÜLERPOOL als so genannter Pool-Bewerber mit seinen Stammdaten nach MAGELLAN übernommen. Pool-Bewerber werden in der Liste der Bewerber zur Unterscheidung mit einer gelben Raute mit einem Ausrufezeichen gekennzeichnet.


![Pool-Bewerber werden durch das Symbol in der Liste der Bewerber gekennzeichnet](/images/sp_1.symbol.png)



### Poolstatus

Die SCHÜLERPOOL-Datenbank wird vom Administrator mit einem gesonderten Programm verwaltet, um diese mit Stammdaten potentieller Bewerbern für Ihre Schule zu füllen. Diese SCHÜLERPOOL-Datenbank kann mehreren Schulen für den zeitgleichen Zugriff zur Verfügung gestellt werden. Für jeden Schüler in der SCHÜLERPOOL-Datenbank (=Pool-Schüler) wird ein so genannter „Poolstatus“ festgehalten. Folgende Poolstati werden dabei unterschieden:

* Pool-Schüler ist frei: Der Pool-Schüler ist von keiner Schule als Pool-Bewerber aufgenommen worden.

* Pool-Schüler hat sich beworben: Der Pool-Schüler ist von mindestens einer Schule als Pool-Bewerber übernommen worden.

* Pool-Schüler ist Schüler: Der Pool-Schüler ist an mindestens einer Schule vom Pool-Bewerber in einen Schüler umgewandelt worden.

Von MAGELLAN aus können Sie auf die SCHÜLERPOOL-Datenbank über die SCHÜLERPOOL-Suche zugreifen. Die nachfolgenden Abschnitte werden die SCHÜLERPOOL-Suche wie auch alle anderen Funktionalitäten im Rahmen der Nutzung des SCHÜLERPOOLs erläutern.

![Hier sehen Sie die Bewerberauswahlliste mit einem Pool-Bewerber](/images/sp_2.Liste der Bewerber.png)

## SCHÜLERPOOL-Funktionen

### Bewerber im SCHÜLERPOOL suchen

Im Rahmen der Aufnahme von Bewerbern an Ihrer Schule können Sie die Suchfunktion im SCHÜLERPOOL nutzen. Durch Eingabe von Vorname, Nachname und Geburtsdatum können Sie suchen, ob der aktuelle Interessent an Ihrer Schule im SCHÜLERPOOL verzeichnet ist. Dazu gehen Sie wie folgt vor:

1. Klicken Sie in der Startleiste auf der linken Bildschirmseite auf `Bewerber` oder wählen Sie `Ansicht > Bewerber`.

2. Klicken Sie auf `SCHÜLERPOOL-Suche`.

3. Geben Sie im Dialogfenster `SCHÜLERPOOL-Suche` unter Suchfilter Vornamen, Nachnamen und Geburtsdatum des Bewerbers an und klicken Sie dann auf Schüler suchen.

![Wählen Sie hieraus, welchen Bewerber Sie im SCHÜLERPOOL suchen.](/images/sp_3.Suche.png)


Es wird eine Verbindung von MAGELLAN zur SCHÜLERPOOL-Datenbank aufgebaut und das Suchergebnis wird unter Ergebnis im Dialogfenster angezeigt.

Folgende Ergebnisse sind dabei möglich:

Ergebnis|Bemerkung
--|--
Kein Eintrag gefunden|Es wurde kein passender Eintrag mit den angegebenen Daten im SCHÜLERPOOL gefunden. Der Bewerber ist nicht im SCHÜLERPOOL verzeichnet.
Bewerber ist frei| Es wurde ein passender Eintrag mit den angegebenen Daten im SCHÜLERPOOL gefunden. Der Bewerber ist im SCHÜLERPOOL verzeichnet. Er ist weder Pool-Bewerber noch eingeschulter Schüler an einer anderen Schule.
Bewerber hat sich beworben|Es wurde ein passender Eintrag mit den angegebenen Daten im SCHÜLERPOOL gefunden. Der Bewerber ist Pool-Bewerber an mindestens einer Schule und ist an noch keiner Schule eingeschult.
Bewerber ist Schüler|Es wurde ein passender Eintrag mit den angegebenen Daten im SCHÜLERPOOL gefunden. Der Bewerber ist an mindestens einer Schule als Schüler erfasst.

![Der Bewerber hat sich bereits an einer Schule beworben](/images/sp_4.Suche.png)

Jedes dieser Suchergebnisse beinhaltet spezifische Informationen:

Ergebnis|Bemerkung
--|--
Kein Eintrag gefunden|Der Bewerber kann nicht als Pool-Bewerber aufgenommen werden. Seine Stammdaten müssen direkt in MAGELLAN eingegeben werden.
Bewerber ist frei|Der Bewerber hat sich bisher an keiner Schule beworben. Sie können nun entscheiden, ob der Bewerber als Pool-Bewerber in MAGELLAN aufgenommen werden soll. Um den Bewerber als Pool-Bewerber zu übernehmen, müssen Sie auf Als Pool-Bewerber übernehmen klicken.
Bewerber hat sich beworben|Der Bewerber gibt seine Bewerbung an mehreren Schulen ab. Welche Schulen dies sind, wird Ihnen in der Ergebnisanzeige dargestellt. Sie können nun entscheiden, ob der Bewerber als Pool-Bewerber auch an Ihrer Schule in MAGELLAN aufgenommen werden soll. Um den Bewerber als Pool-Bewerber zu übernehmen, müssen Sie auf Als Pool-Bewerber übernehmen klicken.
Bewerber ist Schüler|Der Bewerber ist bereits an einer Schule als Schüler geführt. Falls notwendig kann der Schüler zusätzlich an Ihrer Schule als Bewerber aufgenommen werden. Welche Schule dies ist, wird Ihnen in der Ergebnisanzeige dargestellt.

> #### primary::Hinweis
>
> Mit der Übernahme des Bewerbers als Pool-Bewerber an Ihre Schule wird im SCHÜLERPOOL der Poolstatus des Schülers entsprechend aktualisiert. Die Anzeige der unterschiedlichen Poolstatus erleichtert die Aufnahme von Bewerbern an der Schule erheblich. Sie können direkt erkennen, ob der Schüler sich eventuell schon an einer anderen Schule beworben bzw. dort eventuell sogar schon eingeschult ist.

### Pool-Bewerber löschen

Das Löschen eines Pool-Bewerbers erfolgt analog zum Löschen eines Bewerbers. Um einen Pool-Bewerber zu löschen, markieren Sie den gewünschten Pool-Bewerber in der Auswahlliste der Bewerber. Wählen Sie dann `Bearbeiten > Datensatz löschen` und bestätigen Sie die Sicherheitsabfrage mit `Ja`. Mit dem Löschen des Pool-Bewerbers aus MAGELLAN wird im SCHÜLERPOOL der Poolstatus des Schülers entsprechend aktualisiert.

### Pool-Bewerber in Schüler umwandeln

Die Umwandlung eines Pool-Bewerbers in einen Schüler erfolgt analog zur Umwandlung eines Bewerbers in einen Schüler. Dazu gehen Sie wie folgt vor:

1. Klicken Sie in der Startleiste auf der linken Bildschirmseite auf Bewerber oder wählen Sie `Ansicht > Bewerber`.

2. Markieren Sie alle Bewerber bzw. Pool-Bewerber in der Bewerberliste, die den Bewerbungsstatus `Angenommen `besitzen. Die Sortier- oder Gruppierfunktion anhand des Spaltenkopfes `Bewerbungsstatus` vereinfacht an dieser Stelle die Markierung der Datensätze, da Sie sich hierdurch das Suchen aller Bewerber mit dem Bewerbungsstatus `Angenommen `in der Auswahlliste ersparen.

3. Wählen Sie dann Bearbeiten > Bewerberverfahren, um den Assistenten für das Bewerberverfahren aufzurufen.

4. Wählen Sie die Option `Übernahme als Schüler `und klicken Sie auf `Weiter`.

5. Bestätigen Sie über `Fertigstellen`.

Die zuvor markierten Bewerber bzw. Pool-Bewerber werden jetzt aus der Bewerberliste gelöscht und in die Liste der Schüler eingefügt. Gleichzeitig wird für alle umgewandelten Pool-Bewerber im SCHÜLERPOOL der Poolstatus entsprechend aktualisiert.