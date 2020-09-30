## Vorbereitungen

Bevor Sie mit dem Übungsteil beginnen können, müssen drei Startbedingungen erfüllt sein:

1. Die Verbindung zur mitgelieferten Beispieldatenbank ist angelegt.
2. An Ihrem Arbeitsrechner ist ein Barcodescanner installiert.
3. Das Programm ist gestartet.

Die dargestellten Übungen basieren auf Beispieldaten, die in der von uns mitgelieferten Datenbankdatei  `Magellan7.fdb` enthalten sind. Diese Demo-Datenbank wird bei der Installation von MAGELLAN standardmäßig unter folgenden Dateipfaden abgelegt.

| Betriebssystem | Pfad                                                                                          |
| -------------- | --------------------------------------------------------------------------------------------- |
| Windows Vista  | C:\Users\Public\Documents\Stüber Systems\Magellan 6\Datenbank                                 |
| Windows XP     | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\Magellan 6\Datenbank |
| Windows 2000   | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\Magellan 6\Datenbank       |

Wenn Sie MAGELLAN-BIBLIOTHEK nach der Installation das erste Mal starten, greifen Sie automatisch auf die dort hinterlegte Beispieldatenbank zurück.

Wenn Sie bereits MAGELLAN im Schulalltag einsetzen, dann haben Sie wahrscheinlich die in der vorinstallierten Datenbank enthaltenen Beispieldaten durch Ihre eigenen Daten ersetzt. In diesem Fall können Sie die Beispieldatenbank unter [https://support.stueber.de/](https://support.stueber.de/) anfordern und danach über den MAGELLAN-ADMINISTRATOR eine neue Datenbankverbindung registrieren. Wie Sie dazu im Einzelnen vorgehen müssen, erfahren Sie im Kapitel  `Datenbank verwalten` des MAGELLAN-Benutzerhandbuches.

## Barcodescanner anschließen

Damit Sie die hier dargestellten Übungen nachvollziehen können, muss an Ihrem Arbeitsplatzrechner ein Barcodescanner installiert sein.

Barcodes bzw. Strichcodes nehmen in MAGELLAN-BIBLIOTHEK eine zentrale Rolle bei der Erfassung und Verwaltung sowohl der Nutzer- als auch der Medien ein. Sie ermöglichen eine schnelle Abwicklung der Ausleihvorgänge ebenso wie eine zügige Erfassung neuer Medientitel, indem Medien- und Nutzerdaten nicht umständlich eingetippt, sondern über das Einscannen eines Strichcodes in Sekundenschnelle aufgerufen werden können. So wird in MAGELLAN-BIBLIOTHEK z.B. für jedes erfasste Medienexemplar und für jeden angemeldeten Benutzer ein eindeutiger Strichcode erzeugt, auf den später mittels eines Barcodescanner zugegriffen werden kann.

Bei einem Barcodescanner handelt es sich um ein Eingabegerät vergleichbar mit Maus oder Tastatur. Verbinden Sie einfach den USB-Stecker Ihres Barcodescanners mit einem freien USB-Port Ihres Rechners. Die heute handelsüblichen Geräte werden in der Regel von Ihrem Windows-Rechner automatisch erkannt, sobald eine Verbindung hergestellt wurde. Ein Betrieb von MAGELLAN-BIBLIOTHEK ohne ein entsprechendes Lesegerät ist aus Gründen der Arbeitseffizienz nicht zu empfehlen.

## MAGELLAN-BIBLIOTHEK starten

Um MAGELLAN-BIBLIOTHEK das erste Mal zu starten, gehen Sie bitte folgendermaßen vor:

1. Rufen Sie das Startmenü Ihres Windows-Betriebssystems auf und wählen Sie den Aufruf  `Programme` \(XP; 2000\) bzw.  `Alle Programme` \(Vista\).
2. Öffnen Sie den Programmordner  `STÜBER SYSTEMS`.
3. Klicken Sie dort mit der linken Maustaste auf die Programmzeile  `Magellan/Bibliothek`.

Es öffnet sich das Dialogfenster  `MAGELLAN-Anmeldung`, in das Sie einen Benutzernamen und ein Kennwort eintragen müssen. Tragen Sie hier bitte den Benutzernamen sysdba und das Kennwort masterkey \(gilt nur für neuinstallierte Testsysteme\) ein, die als Zugangsdaten bei jeder Installation standardmäßig hinterlegt werden. Außerdem müssen Sie in diesem Anmeldedialog den Namen der Datenbank, die Sie nutzen möchten, angeben. Beim ersten Programmstart steht Ihnen hier nur der Eintrag  `Magellan` zur Verfügung. Unter diesem Namen ist die mitgelieferte Demo-Datenbank für den Zugriff in Magellan registriert.

![Das Dialogfenster  `Magellan-Anmeldung` erscheint vor jedem Programmstart](/assets/images/bibliothek/anmeldung.png)

Sobald Sie Ihre Angaben mit  `OK` bestätigen, wird Magellan-Bibliothek mit dem  `Willkommensfenster` geöffnet.
 
![Das Willkommensfenster begrüßt Sie beim ersten Programmstart von MAGELLAN-BIBLIOTHEK und verweist Sie auf weiterführende Informationen und Services.](/assets/images/bibliothek/willkommen.png)

 Wenn Sie sich nicht als sysdba angemeldet hatten, sondern von Ihrem Schuladministrator persönliche Zugangsdaten erhalten hatten, können Sie nach dem Programmstart Ihr persönliches Anmeldekennwort festlegen. Gehen Sie dazu bitte folgendermaßen vor:

1. Führen Sie den Menüpunkt `Datenbank > Kennwort ändern` aus.

2. Geben Sie im Eingabefeld  `Neues Kennwort` Ihr gewünschtes Anmeldekennwort ein.

3. Wiederholen Sie im Eingabefeld  `Bestätigung` das gewählte Kennwort.

4. Bestätigen Sie bitte Ihre Angaben mit `OK`.

## Medien anlegen

In diesem Abschnitt erfahren Sie, wie Sie Ihre Medien, also Bücher, DVDs, Audio-CDs, CD-Roms etc. in MAGELLAN-BIBLIOTHEK erfassen können. Wenn Sie damit starten,MAGELLAN-BIBLIOTHEK im Schulalltag einzusetzen, ist das Erfassen Ihres kompletten Medienbestands sicherlich der aufwändigste Arbeitsschritt, den Sie erledigen müssen, bevor Sie den Leihbetrieb aufnehmen können.

Unsere Demo-Datenbank enthält bereits eine ganze Reihe von Medientiteln, so dass Sie für die Zwecke dieses Tutorials nur einige wenige Titel und Exemplare erfassen müssen, um sich mit den grundsätzlichen Arbeitstechniken vertraut zu machen.

Zur Liste der bereits eingegebenen Medien gelangen Sie, indem Sie über die blaue Navigationsleiste am linken Rand des Programmfensters die Ansicht  `Bücher/ Medien` aufrufen. Die Programmansicht  `Bücher/ Medien` enthält eine Reihe miteinander verknüpfter Registerkarten, die über das Anklicken des jeweiligen Reiters aufgerufen werden können. Die Registerkarte  `Auswahl` enthält die Liste der Bücher- und Medientitel.


![Die Registerkarte  `Auswahl` der Ansicht  `Bücher/ Medien` enthält die Liste der Bücher- und Medientitel](/assets/images/bibliothek/medien.png)

Damit Sie dieser Liste ein neues Medium hinzufügen können, müssen Sie die folgenden drei Arbeitsschritte ausführen:

1. Eingeben der Mediendaten

2. Erstellen einer Mediensignatur

3. Erfassen der Exemplardaten

Bei der Durchführung dieser Schritte unterstützt Sie der Eingabeassistent  `Neue Medien und Exemplare anlegen`, den Sie über die Programmansicht  `Bücher/Medien` erreichen. Diesen Assistenten rufen Sie auf, indem Sie z.B. den Befehl  `Bearbeiten > Neuer Datensatz` ausführen oder mit der linken Maustaste auf die Schaltfläche  `Neuer Datensatz` in der Symbolleiste des Programmfensters klicken.


![Über die erste Seite des Eingabeassistenten  `Neue Medien und Exemplare anlegen` wählen Sie den Weg, über den Sie die Mediendaten erfassen möchten](/assets/images/bibliothek/neue.medien.png)

### Mediendaten eingeben

Die erste Seite  `Mediendaten suchen oder auswählen` bietet Ihnen drei Optionen an, wie Sie die Grunddaten des zu erfassenden Mediums aufnehmen können:

1. Mediendaten manuell selbst erfassen

2. Automatisch nach dem Barcode suchen

3. Lokal nach einem Titel suchen

### Mediendaten manuell selbst erfassen

Diese Option bietet sich an, wenn Sie einen Titel anlegen wollen, der sich noch nicht in Ihrer Datenbank befindet. Zur manuellen Erfassung Ihrer Mediendaten steht Ihnen eine Eingabemaske für die wesentlichen bibliographischen Informationen zur Verfügung. Hier können Sie u.a Titel, Untertitel, Autor, Verlag , Verlagsort Erscheinungsjahr und Umfang des Mediums angeben.

Um Mediendaten von Hand einzugeben, gehen Sie bitte folgendermaßen vor:

1. Öffnen Sie über die Schaltfläche  `Neuer Datensatz` in der Symbolleiste des Programmfensters den Assistenten  `Neue Medien und Exemplare anlegen`.

2. Setzen Sie den Punkt im Kontrollkreis vor  `Manuell selbst erfassen (auf der nächsten Seite)`.

3. Bestätigen Sie bitte mit  `Weiter`.

4. Tragen Sie in der Eingabemaske der erscheinenden Assistentenseite `Mediendaten bearbeiten` die erforderlichen Mediendaten ein.

5. Bestätigen sie bitte abschließend mit  `Weiter`.

![Mediendaten bearbeiten](/assets/images/bibliothek/mediendaten_bearbeiten.png)

6. Sie gelangen nun zur nächsten Seite des Eingabeassistenten `Signatur aufbauen`, in dem Sie eine Signatur für das Medium erstellen können. Beachten sie bitte, dass Ihre Angaben erst in der Datenbank gespeichert werden, wenn Sie den Eingabeassistenten für  `Neue Medien und Exemplare anlegen` vollständig durchlaufen haben. Beendigen Sie den Assistenten vorher, so gehen alle bis dahin eingegebenen Informationen verloren.

![Signatur aufbauen](/assets/images/bibliothek/signatur_aufbauen.png)

7. Bestätigen sie bitte abschließend mit  `Weiter`.

8. Sie gelangen nun zur nächsten Seite des Eingabeassistenten `Exemplardaten neuer Exemplare`, in dem Sie die benötigten Exemplardaten eingeben können.
   
![Exemplardaten neuer Exemplare](/assets/images/bibliothek/Exemplardaten_neuer_Exemplare.png)

9. Bestätigen sie bitte abschließend mit  `Weiter`.



!!! info "Hinweis"

    Geben Sie bei der manuellen Erfassung im Feld  `Barcode` immer auch die Barcodenummer des Mediums ein. Dadurch erkennt der Eingabeassistent bei der späteren Erfassung eines neuen Exemplars mit Hilfe des Barcodescanners, ob das Medium bereits in der Datenbank gespeichert ist. Die Barcodenummer finden Sie direkt unter dem Strichcode des Medientitels.
