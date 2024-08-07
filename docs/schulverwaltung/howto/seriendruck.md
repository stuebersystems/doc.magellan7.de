# Seriendruck, Serienemail

In diesem Kapitel erfahren Sie, wie Sie die Seriendruckfunktionalität von Microsoft Word  oder LibreOffice mit Magellan-Daten nutzen können. Zusätzlich wird die komfortable Dokumentenverwaltung vorgestellt und die Exportmöglichkeit der Schlüsselverzeichnisse und Auswahllisten nach Microsoft Excel.

## Seriendruck

Aus Magellan heraus können Sie mit Hilfe des Word oder LibreOffice Seriendrucks ein Anschreiben an beliebig viele Personen erstellen. Über eine Schnittstelle zu Microsoft Word/LibreOffice können Sie auf Basis der Auswahllisten für Bewerber, Schüler, Lehrer, Klassen, Sorgeberechtigte, Betriebe, Personen, Adressen, Mandanten und Schulen Seriendrucke erzeugen. Microsoft Word/LibreOffice wird dabei von Magellan aus ferngesteuert, d.h. Sie müssen nicht Magellan verlassen und Microsoft Word/LibreOffice zuvor starten, um die Seriendruckfunktionalität nutzen zu können.

!!! info "Hinweis"

    Eine Übersicht der für den Seriendruck übergebenen Felder aus Magellan finden Sie im [Abschnitt "Seriendruckfelder" unter dem Überpunkt "Referenz"](https://doc.magellan.stueber.de/schulverwaltung/reference/seriendruckfelder/).

### LibreOffice oder Word

Bevor Sie beginnen müssen Sie bitte je Arbeitsplatz wählen, ob die Seriendruckdaten an Magellan oder an LibreOffice übergeben werden sollen. Rufen Sie dazu den Punkt `Datenbank > Optionen > Dokumente > Seriendruck` auf und stellen auf der Karte `Seriendruck` das gewünschte Zielprogramm ein. Diese Einstellung wird für diesen Arbeitsplatz gespeichert. 

![Wählen Sie das Zielprogramm](/assets/images/seriendruck/24.png)

### Seriendruck starten

Um einen Seriendruck durchzuführen, markieren Sie z.B. die gewünschten Datensätze in der Auswahlliste (Bewerber, Schüler, Lehrer, Betriebe, Sorgeberechtigte usw) und wählen klicken anschließend unter Start auf die Schaltfläche oder nutzen den Shortcut (beides siehe Tabelle):

Schaltfläche unter Start | Shortcut
:--|:--
<img src="/assets/images/seriendruck/26.png">|STRG+S
<img src="/assets/images/seriendruck/25.png">|STRG+S

Es startet der Seriendruckassistent mit der folgenden Auswahl:

<img src="/assets/images/seriendruck/27.png">

!!! danger "Achtung"

    Mit dieser Auswahl legen Sie fest welche Datenmenge übernommen wird. Diese Auswahl muss zur Vorlage passen, die Sie im nächsten Schritt wählen. 
    Beispiel: 
    Wenn Sie die Sorgeberechtigten des Schülers anschreiben möchten, muss der Serienbrief in der Datenquelle auch die entsprechenden Daten finden, ansonsten entsteht ein Konflikt. In der nachstehenden Tabelle zeigen wir grob welche Datenmenge hinter welcher Auswahl liegt.

Datenquelle|Bedeutung|Datenmenge
-|- | -
An alle markierten Schüler|ein Brief pro markiertem Schüler|Schülerdaten<br/>Klassendaten
An alle Sorgeberechtigten der markierten aktiven Schüler|ein Brief pro Sorgeberechtigten, der unter `Schüler > Sorgeberechtigter > Benachrichtigung` auf "Immer" gesetzt wurde|Schülerdaten<br/>Klassendaten<br/>Sorgeberechtigtendaten
An den aktuellen Betrieb der markierten Schüler|ein Brief pro markiertem Schüler, an den Betrieb, der unter `Schüler > Ausbildung` als aktuellen Ausbildungsbetrieb markiert wurde|Schülerdaten<br/>Klassendaten<br/>Betriebedaten<br/>Ausbilderdaten

3. Hier wählen Sie aus, ob der Brief an die Schüler selbst, an die Sorgeberechtigten oder an die Betriebe adressiert werden soll. Klicken Sie auf `Weiter`.
 
![Seriendruck-Assistent „Vorlage auswählen“](/assets/images/seriendruck/seriendruck3.png)

Wählen Sie, ob Sie die Daten mit einer leeren Magellan-Vorlage verknüpfen wollen und das gefüllte Dokumente in der Dokumentenverwaltung speichern wollen, ob Sie die Daten mit einer leeren Magellan-Vorlage verknüpfen wollen oder ob Sie auf ein bereits erstelltes Dokument zurückgreifen möchten.

Klicken Sie auf `Weiter` und dann auf `Fertigstellen`. In beiden Fällen wird Word gestartet. Alle Dokumente, die in dem Ordner `Magellan > Vorlagen > Schüler` abgespeichert wurden, können Sie bei einem Seriendruck an die Schüler unter Vorlage aufrufen.

!!! info "Hinweis"

    Um die Option `Daten mit einer Vorlage` verknüpfen und vor dem Start von Word/LibreOffice das gefüllte Dokument pro Schüler in der Dokumentenverwaltung speichern nutzen zu können, müssen Sie in den Optionen von Magellan die entsprechenden Einstellungen gewählt haben.
    Aus Word kann je Schüler (alternativ Bewerber, Lehrer, Klasse, Sorgeberechtigte je nach Startmenüpunkt) in den Unterordnern als Worddokument gespeichert werden. Verwenden Sie LibreOffice speichert Magellan die Daten in einer PDF-Datei.

Sie können alle erstellten Vorlagen bequem von Magellan aus verwalten. Klicken Sie dazu auf die Schaltfläche `Organisieren`. Es öffnet sich das Fenster `Vorlagen organisieren`.

![Fenster „Vorlagen organisieren“](/assets/images/seriendruck/seriendruck4.png)

Das Fenster `„Vorlagen organisieren“` besteht aus einer Schnellstartleiste auf der linken Seite. Diese bestehen aus Ordnern, die den jeweiligen Kategorien hinterlegt sind. Klicken Sie auf den Ordner Schüler und alle Vorlagen, die Sie für Schüler erstellt und in dem Ordner „Schüler“ abgespeichert haben, erscheinen hier.

### Eigene Serienbriefvorlagen in Magellan einfügen

Um eigene Vorlagen einzufügen, gehen Sie bitte folgendermaßen vor:

1. Sie starten den Seriendruck und wählen die Option „Daten mit einem vorhandenen Dokument verknüpfen“. Verweisen Sie dabei auf die Datei, die den vorbereiteten Text enthält, aber noch keine Seriendruckfelder.

2. Word/LibreOffice startet, Sie sehen Ihren Text und können nun Ihre Seriendruckfelder an den gewünschten Stellen platzieren.

3. Wählen Sie `Datei > Speichern unter` und passen bitten den `Dateityp` auf `*.dotx oder *.ott` an. Speichern Sie das Dokument an einer beliebigen Stelle.

4. Wechseln Sie an die Stelle und kopieren Ihre Vorlage in die Zwischenablage, öffnen Magellan und wählen `Extras > Vorlagen organisieren > Schüler/Bewerber...` und fügen über `Rechtsklick > Einfügen` Ihre Datei mit der Endung `*.ott` oder `*.dotx` ein.

Beim nächsten Aufruf des Seriendrucks finden Sie unter den Beispielvorlagen im Punkt `„Daten mit einer Vorlage verknüpfen“` Ihre Vorlage mit zu Auswahl.

### An den aktuellen Betrieb oder den Ausbilder des Schülers

Wählen Sie in der Auswahlliste die Schüler, starten den Seriendruck und wählen als Adressaten "An den aktuellen Betrieb der markierten Schüler" aus.

![Wählen Sie bitte "An den aktuellen Betrieb der markierten Schüler" aus.](/assets/images/seriendruck/seriendruck.betrieb01.png)

Da in Magellan einem Schüler mehrere Ausbildungen zugewiesen können, um zum Beispiel eine Wechsel des Ausbildungsbetriebes oder des Ausbildungsberufes darzustellen, muss gekennzeichnet werden, welche Ausbildung die aktuelle Ausbildung des Schüler ist. Diese Eingabe nehmen Sie bitte unter `Schüler > Ausbildung` am unteren Fensterrand vor.

![Wählen Sie bitte die aktuelle Ausbildung aus!](/assets/images/seriendruck/seriendruck.betrieb00.png)

Nach Word/LibreOffice werden pro Schüler Daten über den aktuellen Betrieb, die Ausbildung und den Ausbilder übergeben.

![Wählen Sie bitte "An den aktuellen Betrieb der markierten Schüler" aus.](/assets/images/seriendruck/seriendruck.betrieb03.png)

### Den Ausbilder per Mail anschreiben?

 Wenn Sie die Nachricht nicht postalisch sondern per Mail versenden möchten, können Sie den fertigen Serienbrief auch aus Word/LibreOffice heraus per Mail versenden. Beide Programme lassen den Versand der Seriendruckdaten per Mail zu.

### An die Sorgeberechtigten des Schülers

!!! info "Hinweis"

    In Magellan können Sie einem Schüler oder einem Bewerber eine beliebige Anzahl von Sorgeberechtigten zuordnen. Welcher oder welche der Sorgeberechtigten im Seriendruck an Sorgeberechtigte angeschrieben werden sollen, steuern Sie über das Feld `Benachrichtigung` unter `Schüler > Sorgeberechtigter > Editieren > Benachrichtigung`.

 Wie Sie Sorgeberechtigte in Magellan erfassen können, beschreiben wir auch im Abschnitt ["Unterkarte "Familie"" unter der Überschrift "Sorgeberechtigte für den Seriendruck korrekt erfassen"](https://doc.magellan.stueber.de/schulverwaltung/howto/schueler/#registerkarte-„familie).

!!! info "Hinweis"

    Im Seriendruck wird pro Sorgeberechtigte ein Dokument erzeugt, der unter `Schüler > Sorgeberechtigter > Benachrichtigung` mit dem Wert „immer“ markiert wurde.

![Die Benachrichtigung "immer" erzeugt einen Serienbriefdatensatz](/assets/images/seriendruck/seriendruck5.png)

Unter `Schüler > Sorgeberechtigter` werden beim Zuweisen des Sorgeberechtigten zum Schüler zwei Felder vorbesetzt: 

* das Feld Briefempfänger
* das Feld Briefanrede.

* **Der Briefempfänger** wird für Ihre Schreiben für das Adressfeld vorbefüllt, als mit der Anrede und dem Nachnamen des Sorgeberechtigten. Ist es eine männliche Anrede wird aus „Herr“ automatisch „Herrn“.

* **Die Briefanrede** wird aus „Sehr geehrte“ oder „Sehr geehrter“, der Anrede und dem Nachnamen gebildet. Um Eltern mit unterschiedlichen Nachnamen korrekt im Seriendruck ansprechen zu können, ändern Sie bitte die vorbesetzten Felder entsprechend der nachfolgenden Abbildung ab, lassen aber bitte dennoch nur bei einem der Sorgeberechtigten die Benachrichtigung auf „immer“ stehen.

![Über die Felder Briefanrede und Briefempfänger können die Sorgeberechtigten im Seriendruck korrekt angesprochen werden](/assets/images/seriendruck/seriendruck6.png)

!!! info "Hinweis"

    In der Auswahlliste der Schüler gibt es das Feld „Volljährig“, das tagesaktuell die Volljährigkeit der Schüler anhand des Geburtsdatums und des Systemdatums Ihres Rechners errechnet. 
    Nutzen Sie diese Angabe um im Seriendruck den korrekten Adressaten (der Schüler selbst oder die Sorgeberechtigten) auszuwählen.

## Etikettendruck

Magellan bietet aufgrund der äußerst zahlreichen möglichen Etikettenformate keinen Bericht bzw. keine Vorlage für Adressetiketten-Aufkleber an. Sie können aber die Serienbrieffunktion in Magellan nutzen, um sich selbst solche Etikettenformate einzurichten. 

!!! info "Hinweis"

    Im Folgenden beschreiben wir die Vorgehensweise für Microsoft Office Word 2003. Sollten Sie eine ältere oder neuere Word-Version  oder LibreOffice einsetzen, wird die Vorgehensweise variieren. 

1. Klicken Sie im Menü `Extras `auf `Umschläge und Etiketten`.
 
![Das Menü „Extras“](/assets/images/seriendruck/seriendruck7.png)

2. Klicken Sie auf in der Registerkarte Etiketten auf Optionen.
 
![Dialog „Etitektten einrichten“](/assets/images/seriendruck/seriendruck8.png)


3. Wählen Sie im Feld Bestellnummer einen Etikettentyp aus, dessen Größe weitgehend mit den von Ihnen verwendeten Etiketten übereinstimmt. Wenn Sie den gewünschten Etikettentyp im Feld Bestellnummer nicht sehen, können Sie eventuell eine andere der aufgeführten Etiketten verwenden, oder Sie können eigene Etiketten erstellen.

4. Klicken Sie auf Details und vergleichen Sie dann die Etikettengröße und die Anzahl der Etiketten pro Blatt (bei Etiketten für Laser- und Tintenstrahldrucker) oder die Anzahl der Spalten des Etikettenformulars (bei Etiketten für Nadeldrucker).
 
![Dialog zum Einrichten des Etiketts](/assets/images/seriendruck/seriendruck9.png)

5. Führen Sie eine der folgenden Aktionen aus: Verwenden Sie das ausgewählte Etikett, wenn es eine ähnliche Größe und ein vergleichbares Layout wie die von Ihnen verwendeten Etiketten aufweist. Wenn Größe und Layout zu stark abweichen, klicken Sie auf Abbrechen, und fahren Sie mit Schritt 7 fort. Fahren Sie andernfalls bitte mit Schritt 9 fort.

6. Aktivieren Sie im Dialogfeld Etiketten einrichten das Kontrollkästchen für den zu verwendenden Druckertyp (entweder Nadeldrucker oder Laser und Ink Jet), und klicken Sie dann auf Neues Etikett. 

7. Geben Sie in das Feld Etikettenname den Namen des zu erstellenden Etiketts ein, wählen Sie die Höhe, Breite, Ränder und sonstigen Optionen für das Etikett aus, und klicken Sie dann auf OK. Das neue Etikett wird im Feld Bestellnummer als Etikettenname- Benutzerdefiniert angezeigt. Das Etikett wird auch in der Kategorie Andere/Standard gespeichert, so dass Sie bei der nächsten Verwendung Ihrer benutzerdefinierten Etiketten im Feld Etikettenmarke die Option Andere/Standard auswählen müssen.

8. Wählen Sie im Fenster „Umschläge und Etiketten“ die Schaltfläche Neues Dokument. In die Vorlage können nun die Seriendruckfelder über Magellan eingefügt werden. Hierzu speichern und schließen sie die Vorlage und greifen dann von Magellan aus darauf zu. Wählen Sie als Speicherort …\Stueber Software\Magellan 6\Vorlagen.  Hier finden Sie die Ordner der einzelnen Magellanmenüs. Möchten Sie nun Etiketten z.B. aus dem Schülermenü starten, dann speichern Sie das Dokument unter „Schueler“. Schließen Sie danach das Dokument.

!!! info "Hinweis"

    Messen Sie die Etiketten sorgfältig ab. Die tatsächliche Größe weicht möglicherweise geringfügig von der vom Etikettenhersteller angegebenen Größe ab. Es kann z.B. vorkommen, dass ein 4 x 8 cm großes Etikett in Wirklichkeit nur 3,9 cm hoch und 7,8 cm breit ist.
    Wenn Sie dann in Magellan im Menü Schüler mehrere Schüler markieren und über Bearbeiten|Seriendruck nach Word den Seriendruckassistenten aufrufen, dann können Sie die Daten mit dieser Word-Vorlage verknüpfen. Im Folgenden ein Beispiel, wie diese Vorlage aussehen könnte:
 
![Seriendruckvorlage](/assets/images/seriendruck/seriendruck10.png)

!!! info "Hinweis"

    Beachten Sie bitte, dass ab dem 2. Etikett zunächst das Bedingungsfeld <<Nächster Daten-satz>> eingefügt werden muss, bevor Sie die Seriendruckfelder auswählen. Wenn Sie dies nicht tun, erhalten Sie auf jedem Etikett der Seite nur die Angaben eines Schülers und nicht für jeden Schüler ein Etikett.
    Wenn Sie sich die Seriendruck-Vorschau anzeigen lassen, erfolgt die Druckvorschau für die Etiketten gefüllt mit den markierten Schülerdaten:
 
![Gefüllte Seriendruckvorlage](/assets/images/seriendruck/seriendruck11.png)

!!! info "Hinweis"

    Es kann sein, dass die Seriendruck-Vorschau von dem eigentlichen Ausdruck auf dem Drucker variiert. Gelegentlich ist dies der Fall, wenn man einen Etikettentyp benutzt, der auf einer Seite 2 Etikettenreihen nebeneinander hat. Man hat in der Vorschau den Eindruck, dass sich die 2. Spalte beim Durchblättern durch die Datensätze stets auf der Folgeseite wiederholt. Der Ausdruck auf dem Drucker aber erfolgt korrekt.

Sie können die Etiketten entweder sogleich über die Funktion Seriendruck an Drucker auf Ihrem Drucker ausgeben oder Sie entscheiden sich sicherheitshalber für die Funktion Seriendruck in Doku-ment. Damit wird ein Dokument erstellt, das Sie zum einen als Druckvorschau nutzen können, um den Ausdruck im Vorfeld zu überprüfen. Zum anderen können Sie dieses Dokument abspeichern und haben so Ihren Serienbrief jederzeit später noch einmal im Zugriff. So wie sich in diesem Dokument der Etikettendruck darstellt, so erfolgt er dann später auch beim Ausdruck auf Ihrem Drucker, während wie gesagt die Seriendruck-Vorschau von der tatsächlichen Druckausgabe abweichen kann.

