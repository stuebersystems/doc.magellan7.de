
# Schülergruppen für Rheinland-Pfalz

Dieses Kapitel erläutert die Nutzung der Schülergruppen für das Bundesland Rheinland-Pfalz. Schülergruppen dienen der Erfassung von schülerbezogene Unterrichtseinheiten, die auch als Lerngruppen bezeichnet werden.

## Voraussetzung

Voraussetzung für die Nutzung der Schülergruppen ist eine entsprechende Installation von MAGELLAN für das Bundesland Rheinland-Pfalz. Dazu müssen Sie im Rahmen der Installation im Willkommen-Assistenten das Bundesland Rheinland-Pfalz auswählen.

> #### success::Tipp
>
> Sollten Sie im Willkommens-Assistenten irrtümlich das falsche Bundesland eingestellt haben, so können Sie dieses nachträglich im MAGELLAN-Administrator korrigieren. Zusätzlich müssen Sie im Dialogfenster Optionen auf der Registerkarte Ein-/Ausblenden die Option `Schülergruppe ausblenden` deaktivieren.

# Änderungen im Verzeichnis „Fachtafeln“

Durch die Verwendung von Schülergruppen muss im Verzeichnis der Fachtafeln von MAGELLAN zwischen den bisherigen Fachtafeln für Noten- bzw. Zeugniserfassung und den Stundentafeln für den Klassenunterricht unterschieden werden. Dies erfolgt durch die neue Spalte Stundentafel auf der Registerkarte Fachtafeln des Dialogfensters Verzeichnis der Fachtafeln. Ist diese markiert, gilt die Fachtafel als Stundentafel. 

![Im Verzeichnis der Fachtafeln können Stundentafel für den Unterricht der Klasse über den Eintrag unter „Stundentafel“ definiert werden.](/bundeslaender/rlp/images/rlp01.png)



## Klassen, Fächer, Lehrer


### Erfassen des Klassenunterrichts


Für die Verwendung von Schülergruppen wird die Ansicht Klassen um die Registerkarte Unterricht erweitert. Diese unterteilt sich in die Registerkarten Fächer und Lehrer.

![In der Ansicht „Klassen“ kann der Klassenunterricht auf der Registerkarte „Unterricht“ definiert werden.](/bundeslaender/rlp/images/rlp02.png)

### Registerkarte „Fächer“

Auf der Registerkarte Fächer werden gemäß Stundenvorgabe des Kultusministeriums die zu unterrichtenden Fächer der Klasse mit deren Sollstunden erfasst. Die von diesem Sollstunden an der Schule eventuell abweichenden Stunden werden in der Spalte Angleichungsstunden festgehalten.
Das Erfassen der einzelnen Angaben kann manuell oder durch Zuweisen einer zuvor definierten Stundentafel im Verzeichnis der Fachtafeln erfolgen. Die Zuweisung einer Stundentafel kann über die Schaltfläche Stundentafel zuweisen durchgeführt werden.

> #### primary::Hinweis
>
>  Die Registerkarte „Fächer“ ist im Stundenplanprogramm DAVINCI mit der Zuordnung einer Stundentafel zu einer Klasse vergleichbar.


Für jede Eintragszeile auf der Registerkarte Fächer kann durch Anwahl der Schaltfläche Details anzeigen oder durch Anwahl der Registerkarte Lehrer festgelegt werden, welche Lehrer das entsprechende Fach unterrichten.

### Registerkarte „Lehrer“

Auf der Registerkarte Lehrer können Sie für das aktuell ausgewählte Fach auf der Registerkarte Fächer festlegen, welche Lehrer mit welcher Iststundenzahl das Fach unterrichten. Findet der Unterricht nicht im Klassenverband statt, so handelt es sich um eine schülerbezogenen Unterrichtseinheit. In diesem Fall ist das Feld Gruppenunterricht zu markieren.

> #### primary::Hinweis
>
> Die Markierung in der Spalte „Gruppenunterricht“ kennzeichnet eine schülerbezogene Unterrichtseinheit. Dies ist die Voraussetzung für die Definition der zugehörigen Schülergruppe in der Ansicht „Schülergruppen“.

## Erstellen der Schülergruppen

Um eine Schülergruppe zu erstellen, müssen Sie in die Ansicht Schülergruppen wechseln. Gehen Sie dazu wie folgt vor:
Klicken Sie in der Startleiste auf der linken Bildschirmseite auf ```Schülergruppen``` oder wählen Sie ```Ansicht Schülergruppen```.
Das Anlegen von Schülergruppen können Sie manuell oder mit Hilfe eines Assistenten automatisch vornehmen.

### Schülergruppe manuell erfassen

Um eine Schülergruppe in der Ansicht Schülergruppen zu erfassen, gehen Sie wie folgt vor:
*	Wählen Sie im Menü Bearbeiten den Menüpunkt ```Neuer Datensatz```.
*	Wählen Sie im Dialogfenster ```Neue Schülergruppe``` unter Klasse eine Klasse aus.

![Dies ist das Dialogfenster zur Definition einer neuen Schülergruppe.](/bundeslaender/rlp/images/rlp03.png)



*	Wählen Sie unter Unterricht eine der zur Auswahl angebotenen schülerbezogenen Unterrichtseinheiten aus, die Sie vor bei der Klasse definiert haben. Mit der Auswahl wird das Kürzel der Schülergruppe im Feld Kürzel automatisch vorbesetzt.
*	Unter Name 1 bzw. Name 2 können Sie eine aussagekräftige Benennung der Schülergruppe optional vornehmen.
*	Klicken Sie auf ```OK```, um die Eingabe zu speichern und auf die Registerkarte ```Daten``` zu wechseln.

![Auf der Registerkarte „Daten“ können Sie die der Schülergruppe zugeordneten Schüler sehen.](/bundeslaender/rlp/images/rlp04.png)


*	Über die Schaltfläche ```Schüler zuweisen ```gelangen Sie in das Dialogfenster ```Schülergruppen Schüler zuweisen``` zur Zuordnung der Schüler zur Schülergruppe.

![Im Dialogfenster „Schülergruppe Schüler zuordnen“ legen Sie fest, welcher Schüler der jeweiligen Schülergruppe angehört.](/bundeslaender/rlp/images/rlp05.png)


*	In der linken Spalte markieren Sie die zu bearbeitende Schülergruppe. In der rechten Spalte `Auswahl der Schüler` wählen Sie unter Klassen eine bestimmte Klasse mit den zugehörigen Schülern aus.
*	Wählen Sie in der rechten unteren Spalte die gewünschten Schüler durch Mehrfachmarkierung aus.
*	Übernehmen Sie diese Schüler per Drag and Drop mit der Maus oder durch Drücken der Schaltfläche `Hinzufügen `in die Spalte `Zugeordnete Schüler`.
*	Um weitere Schüler anderer Klassen derselben Schülergruppe zuzuordnen, müssen Sie eine andere Klasse auswählen, die entsprechenden Schüler markieren und analog in die Spalte `Zugeordnete Schüler` übernehmen.
*	Drücken Sie `Schließen`, um das Dialogfenster zu schließen.

### Schülergruppen über Assistenten erstellen lassen

Neben dem manuellen Erstellen der einzelnen Schülergruppen, können Sie auch alle Schülergruppen über einen Assistenten automatisch erzeugen lassen.
*	Wählen Sie im der Ansicht Schülergruppen die Registerkarte Auswahl.
*	Drücken Sie die Schaltfläche Alle Schülergruppen erzeugen.

![Dies ist der Assistent zur automatischen Erstellung alle Schülergruppen](/bundeslaender/rlp/images/rlp06.png)


*	Klicken Sie auf ```Weiter```.
*	Legen Sie hier die Optionen für die Erstellung der Schülergruppen fest. Wenn Sie die Einstellung Schüler automatisch zuweisen markieren, werden auch gleichzeitig die Schüler der Schülergruppe zugewiesen. Klicken Sie dann auf ```Weiter```.
*	Klicken Sie auf ```Starten```, um die Erstellung der Schülergruppen auszuführen.
*	Wählen Sie ```Schließen```, um den Assistenten wieder zu verlassen.

Wenn Sie jetzt weitere Angaben zu den definierten Schülergruppen vornehmen wollen, wie z.B. Schüler nachträglich den Schülergruppen zuordnen, können Sie dies analog zum vorherigen Abschnitt „Schülergruppe manuell erfassen“ vornehmen.