# Schüler 

Dieses Kapitel beschreibt die Aufnahme von Schülern mit den zugehörigen Daten (Sorgeberechtigten, Ausbildungsbetriebe und Herkunftsschulen) und die Zuordnung zu ihrer Zielklasse. 

Die Aufnahme von neuen Schülern an der Schule erfolgt in zwei Schritten:

1. Erfassen der Stammdaten des Schülers.

2. Einschulen des Schülers in eine Klasse.

Das Erfassen der Stammdaten des Schülers kann über zwei Vorgehensweisen in MAGELLAN erfolgen:

| Art                   | Vorgehen                                                                                                                                                                                                                                                                               |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mit Bewerberaufnahme  | Der neue Schüler wird zunächst als Bewerberim Menü `Bewerber` aufgenommen. Im Rahmen eines Bewerberverfahrens wird der Bewerber dann als Schüler übernommen. Bitte lesen Sie dazu das gesonderte Kapitel [Bewerber](https://doc.magellan7.stueber.de/schulverwaltung/howto/bewerber/)! Der Schritt |
| Ohne Bewerberaufnahme | Wenn Sie einen neuen Schüler anlegen möchten, von dem Sie sicher wissen, dass er Schüler Ihrer Schule wird, legen Sie ihn bitte direkt im Menü `Schüler` an.                                                                                                                           |


## Neuen Schüler aufnehmen

Sollten Sie den Schüler nicht über das Bewerberverfahren neu erzeugt haben, können Sie auch direkt einen Schüler in MAGELLAN aufnehmen. Um einen neuen Schüler aufzunehmen, klicken Sie in der Startleiste auf der linken Bildschirmseite auf Schüler oder wählen Sie `Ansicht > Schüler`. Wählen Sie dann das Plus in der oberen Symbolleiste oder die Tastenkombination `STRG+N`. Es öffnet sich das Dialogfenster `Neuer Schüler`.
 
![Geben Sie Vor- und Nachname ein und bestätigen Sie mit OK](/assets/images/schueler/schueler_27neuer.schueler.png)


Nun wird der  neue Schüler erstellt. Sie befinden sich automatisch auf der Registerkarte `Daten 1` des Schülers. Geben Sie nun die erforderlichen Daten zum Schüler ein. 

!!! info "Hinweis"

   Der neu erzeugte Schüler ist noch keiner Klasse zugeordnet. Entsprechend ist diesem Schüler noch kein Status in der Statusspalte zugeordnet. Dies erfolgt erst mit dem Einschulen des. Erst dann können Sie auch dessen Zeugnisdaten wie Fächer, Noten, Abschlüsse usw. erfassen.

### Doublettenprüfung

Gibt es einen Schüler bereits als Abgänger, Bewerber oder aktiven Schüler, erscheint das nachfolgende Fenster. Sie können nun wählen, ob Sie den Schüler trotzdem anlegen möchten oder den bereits vorhandenen Datensatz ansehen möchten. 
 
![Fenster der Doublettenprüfung](/assets/images/schueler/schueler_28doublettenpruefung.png)

!!! info "Hinweis"

  Die Doublettenprüfung wird für neue Schüler, Bewerber, Lehrer, Klassen, Sorgeberechtigte und Personen durchgeführt.

## Registerkarte `Schüler > Daten 1`

Im Unterschied zur Registerkarte `Daten 1` des Bewerbers, findet man beim Schüler keine Bewerbungsdaten, sondern einige neue Eingabefelder. Die Felder `Klasse` und `Klassenleiter` werden für die Klasse eingetragen und dann automatisch hier eingeblendet.
 
![Schüler > Daten1](/assets/images/schueler/schueler_06schueler.daten1.png) 

## Registerkarte `Schüler > Daten 2`

Auf der Registerkarte `Daten 2` geben Sie die `Religion`, die `Staatsangehörigkeiten`, die `Muttersprache`, die `Sprachgruppen`, den `Grundschuleintritt` und die erworbenen `Abschlüsse` an. 
Die Zugangsdaten werden auch auf dieser Registerkarte festgehalten. Dazu können neben dem Zugangs- und voraussichtlichen Abgangsdatum zur Schule auch die gesamten bisherigen Schulbesuche des Bewerbers festgehalten werden. Ein zweites Zugangsdatum kann eingegeben werden, falls eine Schülerin z.B. die Schule für eine Babypause unterbricht.

![Registerkarte `Daten2`](/assets/images/schueler/daten2.png)

!!! info "Hinweis"

  Unter `Bewerber > Schüler > Sammelzuweisung` haben Sie die Möglichkeit für mehrere Bewerber in einem Arbeitsschritt Felder zu befüllen.

### Bereich `Zugang und Abgang`

An dieser Stelle wird der erste Zugang und der Abgang von Ihrer Schule erfasst. Den Zugang und Abgang bezogen auf die Schülerklasse können Sie auf der Laufbahnkarte sehen. Das Feld `Zugang am` kann manuell auf dieser Karte gefüllt werden, es kann durch den Assistenten beim Einschulen der Schüler befüllt werden oder Sie tragen das Datum per Sammelzuweisung ein.
Das Feld `Abgang am` kann manuell oder durch den Assistenten zum Ausschulen der Schüler befüllt werden.

![Bereich Zugang und Abgang](/assets/images/schueler/bereich.zugang.abgang.png)


### Bereich `bereits besuchte Schule`

Um eine besuchte Schule einzufügen, müssen Sie auf `Hinzufügen `klicken. Sie können dann eine bereits verzeichnete Schule auswählen. Die zuletzt besuchte Schule müssen Sie dann im Feld `Herkunftsschule` auf Basis der zuvor hinzugefügten besuchten Schulen auswählen.

Existiert die Herkunftsschule noch nicht, können Sie sie aber auch über das Pluszeichen im Assistent aus dieser Ansicht heraus ergänzen.
 
![Bereich `bereits besuchte Schulen` ](/assets/images/schueler/bereits.besuchte.schulen.png)

### Bereich `höchster Abschluss ABS und BBS`

Dieser Bereich ist gedacht um bereits erreichte Abschlüsse des Schülers zu erfassen. Unterteilt wird hier in einen allgemeinbildenden Abschluss und ggfs. einen berufsbildenden Abschluss. 

![Bereich `höchster Abschluss ABS/BBS` ](/assets/images/schueler/hoechster.abschluss.png)

Dem jeweiligen Feld `Abschluss`  (also ABS oder BBS) sind die Daten des Schlüsselverzeichnisses `Abschlüsse extern` zugeordnet. Sie können die Inhalte Ihres Verzeichnisses über das Verzeichnisfeld `Kategorie` filtern.

| Kategoriefeld | Anzeige                           |
| ------------- | --------------------------------- |
| ABS           | Anzeige nur für Abschluss ABS     |
| BBS           | Anzeige nur für Abschluss BBS     |
| ABS+BBS       | Anzeige für Abschluss ABS und BBS |
| kein Wert     | Anzeige für Abschluss ABS und BBS |

![Extras > Schlüsselverzeichnisse > Abschlüsse (Extern) > Kategorie ](/assets/images/schueler/abschluesse.extern.png)
 
## Registerkarte `Schüler > Daten 3`

Im Unterschied zum Bewerber können beim Schüler bis zu acht Funktionen zugewiesen werden. Jedem Schüler kann individuell der Auskunftsstatus `Geheim` zuwiesen werden. Dieser Status wird dann mit einem roten Symbol in jeder Registerkarte oben gekennzeichnet. Jeder MAGELLAN-Benutzer erkennt so auf Anhieb, dass sie über den entsprechenden Schüler keine Auskünfte herausgeben darf.
 
![Unterkarte Daten3](/assets/images/schueler/schueler_32daten3.png)

 Beim Setzen des Auskunftsstatus `Geheim` werden Sie gleichzeitig gefragt, ob auch die Sorgeberechtigten ebenfalls als `Geheim` markiert werden sollen.
 
![Bestätigungsdialog für Auskunftsstatus `Geheim`](/assets/images/schueler/schueler_33geheim.png)

## Registerkarten `Schüler > Merkmale` und `Statistik`

Die Funktionalität dieser beiden Karten wird im gesonderten Abschnitt [Merkmale](https://doc.magellan7.stueber.de/schulverwaltung/howto/merkmalsfelder/)beschrieben.

!!! info "Hinweis"

  Die Feldbezeichner der Felder der beiden Karten können für Ihre Datenbank angepasst werden, die Inhalte der Verzeichnisfelder kann in den Schlüsselverzeichnissen editiert werden. 
 Wichtig zu beachten ist, dass einige dieser Felder, speziell die Felder auf der Karte `Statistik` für statistische Eingaben reserviert sein können und nicht mit eigenen Angaben belegt werden können. Ob das für Ihr Bundesland und Ihre Schulform zutrifft wird im jeweiligen Statistikabschnitt im Dokument [Landesstatistiken](https://doc.ls.stueber.de/) beschrieben.

![Unterkarte Merkmale](/assets/images/schueler/merkmal01.png)
![Unterkarte Statistik](/assets/images/schueler/merkmal02.png)

## Sammelzuweisung für `Daten1`,`Daten 2`,`Daten3`, `Merkmale` und `Statistik`

Sie können für mehrere Schüler oder Bewerber gleichzeitig bestimmte Werte auf den Registerkarten `Daten 1`, `Daten 2`, `Daten 3`, `Merkmale` und `Statistik` zuweisen. 
Auf diese Weise können Sie beispielsweise allen Schülern einer Klasse mit einer Anweisung die gleiche Konfession, Staatsangehörigkeit oder Fremdsprachenfolge zuordnen. 
Einige der nachfolgenden Karten sind nicht generell eingeblendet, zum Beispiel die Felder für Ihre `Bewerber` sind nur beim Aufruf aus dem Menü zu sehen oder die Berufsschulfelder sind nur mit der Lizenz Berufsschule sichtbar.

1. Um den Assistenten für die Sammelzuweisung der Stammdaten zu starten, müssen Sie auf `Schüler > Sammelzuweisungen… `klicken. 
2. Klicken Sie jeweils auf `Weiter`, um zum nächsten Schritt des Assistenten zu kommen. 
3. Markieren Sie unter Schüler auswählen bzw. Bewerber auswählen die Schüler, die im Rahmen der Sammelzuweisung den bzw. die gleichen Einträge in den Stammdaten erhalten sollen. 
 
![Dialog Sammelzuweisung `Allgemeine Felder…`](/assets/images/schueler/sammelzuweisung01.png)

![Dialog Sammelzuweisung `Fremdsprachendaten…`](/assets/images/schueler/sammelzuweisung02.png)

![Dialog Sammelzuweisung `Ausbildungsdaten…`](/assets/images/schueler/sammelzuweisung03.png)

![Dialog Sammelzuweisung `allgemeine Merkmale…`](/assets/images/schueler/sammelzuweisung04.png)

![Dialog Sammelzuweisung `Statistik-Merkmale…`](/assets/images/schueler/sammelzuweisung05.png)

![Dialog Sammelzuweisung `Wahlfächer/Kurse und sonstige Daten`](/assets/images/schueler/sammelzuweisung06.png)

![Dialog Sammelzuweisung `Bewerbungsdaten...`](/assets/images/schueler/sammelzuweisung07.png)

!!! info "Hinweis"

  Sie können die Sammelzuweisung nutzen um Felder für mehrere Schüler in einem Arbeitsschritt zu füllen oder auch zu leeren. Wenn Sie ein Feld per Häkchen aktivieren, aber keinen Wert im Feld vergeben, wird der Eintrag für die ausgewählten Schüler gelöscht.


## Registerkarte `Schüler > Ausbildung`

Die Registerkarte `Ausbildung` wendet sich ausschließlich an Berufsbildende Schulen oder Schulen, deren Schüler ein Praktikum absolvieren.
 

![Schüler > Ausbildung](/assets/images/schueler/schueler_13ausbildung.png)

Klicken Sie auf `Hinzufügen`, um neue Ausbildungsdaten hinzuzufügen.
 
![neuer Ausbildungsdatensatz](/assets/images/schueler/schueler_14neu.ausbildung.png)

## Registerkarten `Schüler > Laufbahn` und `Zeugnis`

Die Registerkarten `Laufbahn` und `Zeugnis` enthalten zeitraumbezogene Daten. Die Registerkarte `Laufbahn` wird daher in den Abschnitten `Laufbahn und Zeugnis` und `Laufbahn` vorgestellt. Die andere Registerkarte wird im Kapitel `Zeugnisdaten erfassen` vorgestellt.

## Schüler einschulen

Nachdem Sie die Daten der neuen Schüler erfasst haben, müssen Sie diese einer Klasse zuweisen, das heißt, sie müssen unter MAGELLAN `eingeschult` werden. Mit der Zuordnung zu einer Klasse beginnt für den Schüler in MAGELLAN die zeitraumbezogene Dokumentation seines Werdegangs. Bitte beachten Sie, dass vor dem Einschulen die entsprechenden Klassen eingerichtet sein müssen (siehe `Klassen eingeben`). 

| Nr. | So geht's                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1.  | Klicken Sie auf `Laufbahnprozesse` und dann auf `Schüler einschulen`. Es erscheint der Assistent `Schüler einschulen`. Klicken Sie jeweils auf `Weiter`, um zum nächsten Schritt des Assistenten zu kommen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 2.  | Unter Schüler auswählen werden alle Schüler aufgelistet, die noch nicht eingeschult worden sind.<br/><br/>![Dialog `Schüler einschulen`](/assets/images/schueler/schueler_34einschulen.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 3.  | Schüler werden klassenweise eingeschult. Damit Sie die Schüler abhängig von bestimmten Eigenschaften, z.B. erster Fremdsprache oder Konfessionszugehörigkeit, einer Klasse zuweisen können, sind die entsprechenden Spalten hier ebenfalls angezeigt. Sie können die Spalten entsprechend denen der Gesamtliste bearbeiten ([Sortieren, Gruppieren, Filtern und Suchen](https://doc.magellan7.stueber.de/schulverwaltung/howto/sort-group-filter-search/)). Haben Sie z.B. ein Einschulungskriterium vergeben, können Sie danach gruppieren und alle Schüler, die Sie einer Klasse zuweisen möchten, auf einmal markieren und einschulen. Markieren Sie die Schüler, die Sie z.B. der Klasse 5a zuweisen möchten und klicken Sie auf `Weiter`. |
| 4.  | Unter `Klassen auswählen` werden die Klassen angezeigt, die Sie für das neue Schuljahr angelegt haben. <br/><br/>![Wählen Sie die Klasse aus, in die Sie die markierten Schüler einschulen möchten, indem Sie einmal auf die Klasse klicken.](/assets/images/schueler/schueler_35einschulen2.png)                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 5.  | Markieren Sie die gewünschte Klasse, in welche die zuvor markierten Schüler eingeschult werden sollen und klicken Sie dann auf `Weiter`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 6.  | Unter `Weitere Angaben` können Sie weitere Angaben per Sammelzuweisung allen ausgewählten Schülern zuordnen. Hierbei muss mindestens das `Zugangsdatum` angegeben werden. Klicken Sie jetzt auf `Weiter` und anschließend auf `Fertigstellen`, um die Einschulung der Schüler durchzuführen. Die eingeschulten Schüler werden jetzt in der Auswahlliste der Schüler mit einem blau gefüllten Kreis in der Statusspalte von den noch nicht eingeschulten Schülern unterschieden, die kein Symbol in der Spalte `Status` haben. Sie sehen noch nicht eingeschulte Schüler, wenn Sie den Filter der Auswahlliste auf `Vagabunden` umstellen.<br/><br/> ![Filter der Auswahlliste](/assets/images/schueler/vagabundenfilter.png)     |
| 7.  | Starten Sie erneut den Einschulungsassistenten um weitere Schüler klassenweise einzuschulen. In dieser Liste sind nun die Schüler, die Sie gerade eingeschult haben, nicht mehr enthalten. Dies verhindert, dass Schüler aus Versehen mehrfach eingeschult werden. Sie können jetzt im nächsten Schritt die Schüler, die noch nicht eingeschult wurden, einer anderen Klasse, beispielsweise der Klasse 5b, zuweisen.                                                                                                                                                                                                                                                                                                              |


## Registerkarte `Schüler > Laufbahn`

Nach dem Einschulen des Schülers, sieht man erste Einträge auf der Karte `Laufbahn`, zusätzlich sind für eingeschulte Schüler auf die Karten unter `Zeugnis` editierbar. Die Registerkarte `Zeugnis` wird im Kapitel `Zeugnisdaten erfassen` erläutert. Auf der Registerkarte `Laufbahn` können Sie die Laufbahn des Schülers an Ihrer Schule verfolgen. Diese Registerkarte füllt sich in einer Liste auf der linken Seite automatisch mit den Zeiträumen und den dazugehörigen Klassen, die der Schüler an der Schule besucht hat. Zu jedem markierten Zeitraumeintrag in der Liste werden rechts auf den beiden Registerkarten `Allgemein` und `Abschluss` die detaillierte Angaben angezeigt.

![Registerkarte `Laufbahn`](/assets/images/schueler/laufbahnkarte.png)

## Fehlzeiten erfassen

Sie können für jeden Schüler individuell Fehlzeiten mit Gründen und Status erfassen. Markieren Sie dazu zunächst den entsprechenden Schüler in der Auswahlliste und wählen dann `Rechtsklick > Fehlzeiten…` oder rufen Sie den Dialog per STRG+F auf. Die Fehlgründe erfassen Sie im Schlüsselverzeichnis `Fehlgründe (Schüler)` unter `Extras > Schlüsselverzeichnisse`.
Hier sehen Sie die Fehlzeiten eines Schülers, es wird als Standardfilter immer der Zeitraum vor dem aktuellen Datum gesetzt.
 
![Fehlzeitenfenster, aufrufbar in der Schülerauswahlliste mit STRG+F](/assets/images/schueler/schueler_36fehlzeiten.png)


## Unfallanzeigen erstellen und verwalten

Um eine Unfallanzeige in MAGELLAN zu erfassen, gehen Sie bitte wie folgt vor:
Legen Sie bitte die möglichen Empfänger der Unfallanzeige im Menü Adressen an. Unter `Adressen > Daten` können Sie eine oder mehrere Adressen als Unfallanzeigen markieren und auch die Trägernummern eintragen. 
 
![Setzen Sie das Häkchen und tragen die Trägernummer ein](/assets/images/schueler/schueler_37unfallanzeige.png)

Um einen Unfall aufzunehmen, markieren Sie den Schüler in der Schülerauswahlliste und wählen `Schüler > Unfallanzeigen...`.
 
![Fenster `Unfallanzeige`](/assets/images/schueler/schueler_38unfallanzeige2.png)

Legen Sie über `Neue Unfallanzeige` einen neuen Datensatz an. Sie können auch einen bereits erfassten Unfallbericht markieren und per Unfallanzeige bearbeiten erneut öffnen. 
 
![Tragen Sie hier den Hergang ein](/assets/images/schueler/schueler_39unfallanzeige3.png)

Anschließend können Sie die Daten drucken oder wahlweise auch parallel als PDF im Schülerunterordner ablegen lassen. 
Die erfassten Daten werden gespeichert, Sie können jederzeit auch ältere Vorgänge wieder pro Schüler einsehen.

!!! info "Hinweis"

  Die Daten der Unfallanzeige werden beim Druck mit Hilfe des Berichtes `Unfallanzeige.rpt` ausgegeben. Dieser Bericht liegt standardmäßig auf Ihrem Server unter `Berichte > Schueler`. Zusätzlich gibt es den Bericht `Unfallanzeige (mit Erläuterungen).rpt`, der eine zweite Seite mit Erläuterungen zu den Eingaben des Berichtes beinhaltet. Um diesen Bericht zu verwenden müssten Sie ihn in `Unfallanzeige.rpt` umbenennen.

