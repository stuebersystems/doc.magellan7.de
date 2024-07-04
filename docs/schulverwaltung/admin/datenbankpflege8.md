# Datenbankpflege

[1]:/assets/images/magellan.administrator/03.png
[2]:/assets/images/magellan.administrator/04.png
[3]:/assets/images/magellan.administrator/05.png
[4]:/assets/images/magellan.administrator/06.png
[5]:/assets/images/magellan.administrator/07.png
[6]:/assets/images/neues/908.png

## Generatoren synchronisieren

Setzt die Generatoren zur Erstellung der automatisch hochgezählten Ids auf den nächstmöglichen Wert. Diese Funktion sollte zum Beispiel nach dem Leeren der Datenbank ausgeführt werden.

![Klicken Sie auf `Ausführen`oder doppelt auf `Generatoren synchronisieren`](/assets/images/magellan.administrator/generatoren.sync.png)

## Gemeinden synchronisieren

Setzt für Schüler, Betriebe, Lehrer, Schulen und Sorgeberechtigte (Sorgeberechtigte neu ab 7.0.12) die Gemeindekennziffern anhand der PLZ und des Ortes, wenn damit nicht mehrere Gemeinden gekennzeichnet sind.
Es werden nur nicht vorhandene Gemeinden gesetzt.

![Klicken Sie auf `Ausführen`oder doppelt auf `Gemeinden synchronisieren`](/assets/images/magellan.administrator/gemeinden.sync.png)

## Aktuelle Bewerber-Ausbildung setzen

Diese Funktion setzt für alle Bewerber, die nur eine Ausbildung unter `Bewerber > Ausbildung` haben, diese Ausbildung auf "aktuelle Ausbildung". Der Eintrag als "aktuelle Ausbildung" ist Voraussetzung für den Seriendruck und -mail an den Bewerberbetrieb und für einige Berichte.

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/akt.bewerber.png)

## Code 128 generieren

Legt für Schüler, Lehrer und Personen fehlende Barcodes (Code 128) an. Für direkt in Magellan angelegte Schüler, Lehrer oder Personen wird dieser Barcode automatisch erzeugt. Für alte Datenbestände oder importierte Datensätze kann dieser Barcode für Schülerausweise auf diesem Weg nachträglich erzeugt werden.
Der für die Bibliothek für die Medienausleiher(Schüler, Lehrer, Personen) erzeugte Barcode hat hiermit nichts zu tun. Dieser gesonderte Barcode wird erzeugt, wenn ein Schüler/Lehrer/Person als Medienausleiher in die Magellan Bibliothek übernommen wird.

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/code128.png)

## Mandanten kopieren

Kopiert Magellan-Daten in eine andere Magellan-Datenbank zur Datenübernahme einer Magellan 6 Datenbank

* Datenrettung bei erfolglosem Versuch einer Datenbankreparatur (Datapump)
* Zusammenführen von Daten zweier Datenbanken in eine Datenbank mit zwei Mandanten

![Klicken Sie auf `Ausführen`oder doppelt auf `Mandanten kopieren`](/assets/images/magellan.administrator/mandanten.kopieren.png)

!!! info "Hinweis"

    Bitte lesen Sie dazu den Abschnitt [Umstieg von 6 auf 8](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-6-auf-8/)!

## Anrede setzen

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/anreden.setzen.png)

Setzt für Schüler, Bewerber, Lehrer und Personen, denen noch keine Anrede hinterlegt wurde, eine Anrede anhand des erfassten Geschlechts.
Dabei wird aus dem Geschlecht weiblich die Anrede Frau und aus dem Geschlecht männlich die Anrede Herr befüllt.

## Organisiertes Löschen

Starten Sie den Assistenten unter Datenbankpflege per Doppelklick auf den nachstehend gelb markierten Bereich.


[![Klicken Sie auf `Ausführen`][6]][6]

Es erscheint das Fenster des Assistenten.

[![Assistentenfenster][2]][2]

Der Assistent unterstützt Sie beim Löschen von wahlweise:

*  Schülerdatensätzen
*  Fachdaten von Schülern (`Schüler > Zeugnis > Fächer/Leistungen`)
*  Passbildern von Schülern
*  
[![Optionen][1]][1]

Sie geben Ihren Mandanten und als Zeitpunkt eine Monatsanzahl ein, die ausgehend vom aktuellen Tagesdatum die Löschungen für Schüler durchführt, die zu diesem Zeitpunkt nicht mehr Schüler Ihrer Schule waren.
Im Beispiel wurden 12 Monate eingegeben, ausgehend vom Tagesdatum werden zwei Zeiträume identifiziert und in der Liste unterhalb dargestellt.  

[![Assistentenfenster][3]][3]

Wechseln Sie mit `Weiter` auf die nächste Karte, die Prüfung durchsucht die Zeiträume und stellt Schüler dar, die ausgeschult sind und in den auf der vorhergehenden Karte gezeigten Zeiträumen zuletzt Schüler diese Schule waren.

!!! warning "Wichtig!"

    Die Prüfung kontrolliert: <br/>
     * den Status des Schülers (inaktiv) <br/>
     * der Schüler darf keinen späteren Zeitraum an der Schule besucht haben <br/>
     * es darf keine mit ihm verbundenen Schülerkopien in späteren Zeiträumen geben 

Für unser Beispiel sieht man in der nachstehenden Abbildung auf der linken Seite die Schüler der Klasse 12, nur drei der Schüler sind ausgeschult, nur diese werden vom Assistenten gezeigt. 

[![Vergleich Magellan und Prüfung des Assistenten][4]][4]

Wechseln Sie mit `Weiter` auf die nächste Karte und klicken Sie auf `Sichern`. Bevor Ihre Aktion ausgeführt wird, muss eine Sicherung der Datenbank auf dem Stand vor Ihrer Änderung erstellt werden. Der Assistent liest Ihre Einstellungen zur Datensicherung aus den Verbindungseinstellungen aus, erstellt die Sicherung und speichert sie.
Es wird parallel zur Datenbanksicherung auch eine Excelliste mit den Schülerdatensätzen zur Nachkontrolle erzeugt. Die Ablagestelle für die Sicherung der Datenbank und die Protokolllisten ergeben sich aus Ihren Eintragungen in der Verbindung zur Datenbank.


[![Sicherung erstellen][5]][5]

Wechseln Sie mit `Weiter` auf die nächste Karte und klicken auf `Fertigstellen`, Ihre gewählte Option löscht die Passbilder, Fachdaten oder die Schülerdatensätze aus Ihrer Datenbank.
