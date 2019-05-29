# Seriendruck, Serienemail, Dokumentenverwaltung und Exportieren

In diesem Kapitel erfahren Sie, wie Sie die Seriendruckfunktionalität von Microsoft Word mit MAGELLAN-Daten nutzen können. Zusätzlich wird die komfortable Dokumentenverwaltung vorgestellt und die Exportmöglichkeit der Schlüsselverzeichnisse und Auswahllisten nach Microsoft Excel.



## Seriendruck

Aus MAGELLAN heraus können Sie mit Hilfe des Word Seriendrucks ein Anschreiben an beliebig viele Personen erstellen. Über eine Schnittstelle zu Microsoft Word können Sie auf Basis der Auswahllisten für Bewerber, Schüler, Lehrer, Klassen, Sorgeberechtigte, Betriebe, Personen, Adressen, Mandanten und Schulen Seriendrucke erzeugen. Microsoft Word wird dabei von MAGELLAN aus ferngesteuert, d.h. Sie müssen nicht MAGELLAN verlassen und Microsoft Word zuvor starten, um die Seriendruckfunktionalität nutzen zu können. 


!!! info "Hinweis"

  Eine Übersicht der für den Seriendruck nach Word übergebenen Felder aus MAGELLAN finden Sie im [Abschnitt "Seriendruckfelder" unter dem Überpunkt "Referenz"](https://doc.magellan7.stueber.de/schulverwaltung/reference/seriendruckfelder.html).




Um einen Seriendruck durchzuführen, markieren Sie z.B. die gewünschten Schüler in der Auswahlliste der Schüler.:

1. Klicken Sie in der Menüleiste auf das Schaltbild ![ ](/assets/images/seriendruck/seriendruck1.png) oder wählen Sie `Bearbeiten > Seriendruck nach Word` (STRG+W). Der „Serienbriefassistent“ öffnet sich.

2. Verfassen Sie ggf. den Serienbrief und fügen Sie die entsprechenden Seriendruckfelder ein. Um ein Worddokument als Vorlage für den MAGELLAN-Seriendruck verfügbar zu machen, speichern Sie dieses Dokument ab unter: 


![ Bitte schauen Sie die nachstehende Tabelle zur Bedeutung der Auswahl an!](/assets/images/seriendruck/seriendruck2.png)



Datenquelle|Bedeutung|Datenmenge
---|---
An alle markierten Schüler|ein Brief pro markiertem Schüler|Schülerdaten<br/>Klassendaten
An alle Sorgeberechtigten der markierten aktiven Schüler|ein Brief pro Sorgeberechtigten, der unter `Schüler > Sorgeberechtigter > Benachrichtigung` auf "Immer" gesetzt wurde|Schülerdaten<br/>Klassendaten<br/>Sorgeberechtigtendaten
An den aktuellen Betrieb der markierten Schüler|ein Brief pro markiertem Schüler, an den Betrieb, der unter `Schüler > Ausbildung` als aktuellen Ausbildungsbetrieb markiert wurde|Schülerdaten<br/>Klassendaten<br/>Betriebedaten<br/>Ausbilderdaten

!!! info "Hinweis"

  Bitte wählen Sie je nach Seriendruckvorlage im Assistenten den korrekten Adressaten aus, da damit eine unterschiedliche Menge an Seriendruckinformationen nach Word übergeben werden. Beispiel: Wenn eine vorbereitete Seriendruckvorlage Felder für die Sorgeberechtigten des Schülers enthält, müssen Sie bitte auch „An alle Sorgeberechtigten der markierten aktiven Schüler“ oder eine eigene Vorlage, die keine anderen Seriendruckfelder erwartet, wählen.


3. Hier wählen Sie aus, ob der Brief an die Schüler selbst, an die Sorgeberechtigten oder an die Betriebe adressiert werden soll. Klicken Sie auf `Weiter`.
 
![Seriendruck-Assistent „Vorlage auswählen“](/assets/images/seriendruck/seriendruck3.png)


4. Wählen Sie, ob Sie die Daten mit einer leeren MAGELLAN-Vorlage verknüpfen wollen und das gefüllte Dokumente in der Dokumentenverwaltung speichern wollen, ob Sie die Daten mit einer leeren MAGELLAN-Vorlage verknüpfen wollen oder ob Sie auf ein bereits erstelltes Dokument zurückgreifen möchten. 

5. Klicken Sie auf `Weiter` und dann auf `Fertigstellen`. In beiden Fällen wird Word gestartet. Alle Dokumente, die in dem Ordner `MAGELLAN > Vorlagen > Schüler` abgespeichert wurden, können Sie bei einem Seriendruck an die Schüler unter Vorlage aufrufen.

!!! info "Hinweis"

  Um die Option Daten mit einer Word-Vorlage verknüpfen und vor dem Start von Word das gefüllte Dokument pro Schüler in der Dokumentenverwaltung speichern nutzen zu können, müssen Sie in den Optionen von MAGELLAN die entsprechenden Einstellungen gewählt haben (siehe „Einstellung für Word-Seriendruck“).

Sie können alle erstellten Vorlagen bequem von MAGELLAN aus verwalten. Klicken Sie dazu auf die Schaltfläche `Organisieren`. Es öffnet sich das Fenster `Vorlagen organisieren`.
 
![Fenster „Vorlagen organisieren“](/assets/images/seriendruck/seriendruck4.png)


Das Fenster `„Vorlagen organisieren“` besteht aus einer Schnellstartleiste auf der linken Seite. Diese bestehen aus Ordnern, die den jeweiligen Kategorien hinterlegt sind. Klicken Sie auf den Ordner Schüler und alle Vorlagen, die Sie für Schüler erstellt und in dem Ordner „Schüler“ abgespeichert haben, erscheinen hier.

### Eigene Serienbriefvorlagen in MAGELLAN einfügen

Um eigene Vorlagen einzufügen, gehen Sie bitte folgendermaßen vor:

1. Sie starten den Seriendruck und wählen die Option „Daten mit einem vorhandenen Worddokument verknüpfen“. Verweisen Sie dabei auf die Worddatei, die den vorbereiteten Text enthält, aber noch keine Seriendruckfelder. 

2. Word startet, Sie sehen Ihren Text und können nun über die Wordfunktion „Seriendruckfeld einfügen“ an den gewünschten Stellen die Seriendruckfelder platzieren.

3. Wählen Sie `Datei > Speichern unter` und passen bitten den `Dateityp `auf `Wordvorlage` an. Speichern Sie das Dokument an einer beliebigen Stelle.

4. Wechseln Sie an die Stelle und kopieren Ihre Wordvorlage in die Zwischenablage, öffnen MAGELLAN und wählen `Extras > Vorlagen organisieren > Schüler/Bewerber...` und fügen über `Rechtsklick > Einfügen` Ihre Datei mit der Endung *.dot oder *.dotx ein.

Beim nächsten Aufruf des Seriendrucks finden Sie unter den Beispielvorlagen im Punkt `„Daten mit einer Wordvorlage verknüpfen“` Ihre Vorlage mit zu Auswahl.

### An den aktuellen Betrieb oder den Ausbilder des Schülers

Wählen Sie in der Auswahlliste die Schüler, starten den Seriendruck (STRG+W oder über das Wordsymbol in der Menüleiste) und wählen als Adressaten "An den aktuellen Betrieb der markierten Schüler" aus.


![Wählen Sie bitte "An den aktuellen Betrieb der markierten Schüler" aus.](/assets/images/seriendruck/seriendruck.betrieb01.png)

Da in MAGELLAN einem Schüler mehrere Ausbildungen zugewiesen können, um zum Beispiel eine Wechsel des Ausbildungsbetriebes oder des Ausbildungsberufes darzustellen, muss gekennzeichnet werden, welche Ausbildung die aktuelle Ausbildung des Schüler ist. Diese Eingabe nehmen Sie bitte unter `Schüler > Ausbildung` am unteren Fensterrand vor.

![Wählen Sie bitte die aktuelle Ausbildung aus!](/assets/images/seriendruck/seriendruck.betrieb00.png)

Nach Word werden pro Schüler Daten über den aktuellen Betrieb, die Ausbildung und den Ausbilder übergeben.

![Wählen Sie bitte "An den aktuellen Betrieb der markierten Schüler" aus.](/assets/images/seriendruck/seriendruck.betrieb03.png)

### Den Ausbilder per Mail anschreiben?

 Wenn Sie die Nachricht nicht postalisch sondern per Mail versenden möchten, können Sie den fertigen Serienbrief auch aus Word heraus per Mail versenden.
 
 Wählen Sie bitte unter "Fertigstellen und zusammenführen" den Unterpunkt "Email-Nachrichten senden..." aus.
 
![Unter "Fertigstellen und zusammenführen" den Unterpunkt "Email-Nachrichten senden..." wählen.](/assets/images/seriendruck/seriendruck.betrieb04.png)

Anschließend können Sie im Feld "Zu:" das Feld "Ausbilder_Email" wählen, diese Liste enthält die Mailadressen der den Schüler zugewiesenen Ausbildern der aktuellen Ausbildung.

![Wählen Sie bitte "An den aktuellen Betrieb der markierten Schüler" aus.](/assets/images/seriendruck/seriendruck.betrieb05.png)



### An die Sorgeberechtigten des Schülers

!!! info "Hinweis"

  In MAGELLAN können Sie einem Schüler oder einem Bewerber eine beliebige Anzahl von Sorgeberechtigten zuordnen. Welcher oder welche der Sorgeberechtigten im Seriendruck an Sorgeberechtigte angeschrieben werden sollen, steuern Sie über das Feld `Benachrichtigung` unter `Schüler > Sorgeberechtigter > Editieren > Benachrichtigung`. 


 Wie Sie Sorgeberechtigte in MAGELLAN erfassen können, beschreiben wir auch im Abschnitt ["Unterkarte "Familie"" unter der Überschrift "Sorgeberechtigte für den Seriendruck korrekt erfassen"](https://doc.magellan7.stueber.de/schulverwaltung/howto/schueler/#registerkarte-„familie).

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

MAGELLAN bietet aufgrund der äußerst zahlreichen möglichen Etikettenformate keinen Bericht bzw. keine Vorlage für Adressetiketten-Aufkleber an. Sie können aber die Serienbrieffunktion in MAGELLAN nutzen, um sich selbst solche Etikettenformate einzurichten. 

!!! info "Hinweis"

  Im Folgenden beschreiben wir die Vorgehensweise für Microsoft Office Word 2003. Sollten Sie eine ältere oder neuere Word-Version einsetzen, kann die Vorgehensweise variieren. Informationen erhalten Sie in der Microsoft Office Word Hilfe.

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

8. Wählen Sie im Fenster „Umschläge und Etiketten“ die Schaltfläche Neues Dokument. In die Vorlage können nun die Seriendruckfelder über MAGELLAN eingefügt werden. Hierzu speichern und schließen sie die Vorlage und greifen dann von MAGELLAN aus darauf zu. Wählen Sie als Speicherort …\Stueber Software\Magellan 6\Vorlagen.  Hier finden Sie die Ordner der einzelnen Magellanmenüs. Möchten Sie nun Etiketten z.B. aus dem Schülermenü starten, dann speichern Sie das Dokument unter „Schueler“. Schließen Sie danach das Dokument.

!!! info "Hinweis"

   Messen Sie die Etiketten sorgfältig ab. Die tatsächliche Größe weicht möglicherweise geringfügig von der vom Etikettenhersteller angegebenen Größe ab. Es kann z.B. vorkommen, dass ein 4 x 8 cm großes Etikett in Wirklichkeit nur 3,9 cm hoch und 7,8 cm breit ist.
   Wenn Sie dann in MAGELLAN im Menü Schüler mehrere Schüler markieren und über Bearbeiten|Seriendruck nach Word den Seriendruckassistenten aufrufen, dann können Sie die Daten mit dieser Word-Vorlage verknüpfen. Im Folgenden ein Beispiel, wie diese Vorlage aussehen könnte:
 
![Seriendruckvorlage](/assets/images/seriendruck/seriendruck10.png)

!!! info "Hinweis"

  Beachten Sie bitte, dass ab dem 2. Etikett zunächst das Bedingungsfeld <<Nächster Daten-satz>> eingefügt werden muss, bevor Sie die Seriendruckfelder auswählen. Wenn Sie dies nicht tun, erhalten Sie auf jedem Etikett der Seite nur die Angaben eines Schülers und nicht für jeden Schüler ein Etikett.
Wenn Sie sich die Seriendruck-Vorschau anzeigen lassen, erfolgt die Druckvorschau für die Etiketten gefüllt mit den markierten Schülerdaten:
 
![Gefüllte Seriendruckvorlage](/assets/images/seriendruck/seriendruck11.png)

!!! info "Hinweis"

  Es kann sein, dass die Seriendruck-Vorschau von dem eigentlichen Ausdruck auf dem Drucker variiert. Gelegentlich ist dies der Fall, wenn man einen Etikettentyp benutzt, der auf einer Seite 2 Etikettenreihen nebeneinander hat. Man hat in der Vorschau den Eindruck, dass sich die 2. Spalte beim Durchblättern durch die Datensätze stets auf der Folgeseite wiederholt. Der Ausdruck auf dem Drucker aber erfolgt korrekt.

Sie können die Etiketten entweder sogleich über die Funktion Seriendruck an Drucker auf Ihrem Drucker ausgeben oder Sie entscheiden sich sicherheitshalber für die Funktion Seriendruck in Doku-ment. Damit wird ein Dokument erstellt, das Sie zum einen als Druckvorschau nutzen können, um den Ausdruck im Vorfeld zu überprüfen. Zum anderen können Sie dieses Dokument abspeichern und haben so Ihren Serienbrief jederzeit später noch einmal im Zugriff. So wie sich in diesem Dokument der Etikettendruck darstellt, so erfolgt er dann später auch beim Ausdruck auf Ihrem Drucker, während wie gesagt die Seriendruck-Vorschau von der tatsächlichen Druckausgabe abweichen kann.

## Serienemail

Sie können aus MAGELLAN heraus Serienemails an Schüler/Bewerber, Betriebe der Schüler/Bewerber oder an deren Sorgeberechtigte versenden. Die Serienmailfunktion greift auf die unter Schü-ler/Bewerber, Betriebe oder Sorgeberechtigten jeweils unter Daten im Feld Email hinterlegten Emailadresse zurück. Markieren Sie die entsprechenden Schüler/Bewerber im Schüler-/Bewerbermenü und öffnen dann über Rechtsklick|Serienmail oder drücken der Tastenkombination STRG+M den Serienemailassistenten.  Im nächsten Schritt wählen Sie bitte eine der drei Optionen aus: An alle markierten Schüler/Bewerber, An alle Sorgeberechtigten der markierten aktiven Schüler/Bewerber oder An den aktuellen Betrieb der markierten Schüler/Bewerber. 
 
![Serienmailassistent](/assets/images/seriendruck/seriendruck12.png)


Im unteren Auswahlfeld desselben Fensters können Sie wählen, ob die Nachricht direkt an den Empfän-ger gesandt werden soll An, CC oder BCC.

!!! info "Hinweis"

  „Cc“ ist die Abkürzung für "Carbon copy". Es wird eine Kopie der Nachricht an diesen Empfänger gesendet, wobei der Name des Empfängers für andere Empfänger der Nachricht sichtbar ist. „Bcc“ ist die Abkürzung für "Blind carbon copy".  Es wird eine Kopie der Nachricht an diesen Empfänger gesendet, der Name des Empfängers ist jedoch für andere Empfänger der Nachricht nicht sichtbar.

Im Anschluss öffnet sich ein Emailfenster Ihres als Standard definierten Emailprogrammes. Im Adressfeld der Email sind die in MAGELLAN hinterlegten Emailadressen bereits eingefügt. 

