# Datenbankpflege

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

Legt für Schüler, Lehrer und Personen fehlende Barcodes (Code 128) an. Für direkt in MAGELLAN angelegte Schüler, Lehrer oder Personen wird dieser Barcode automatisch erzeugt. Für alte Datenbestände oder importierte Datensätze kann dieser Barcode für Schülerausweise auf diesem Weg nachträglich erzeugt werden.
Der für die Bibliothek für die Medienausleiher(Schüler, Lehrer, Personen) erzeugte Barcode hat hiermit nichts zu tun. Dieser gesonderte Barcode wird erzeugt, wenn ein Schüler/Lehrer/Person als Medienausleiher in die MAGELLAN Bibliothek übernommen wird.

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/code128.png)

## Mandanten kopieren

Kopiert MAGELLAN-Daten in eine andere MAGELLAN-Datenbank zur Datenübernahme einer MAGELLAN 6 Datenbank
* Datenrettung bei erfolglosem Versuch einer Datenbankreparatur (Datapump)
* Zusammenführen von Daten zweier Datenbanken in eine Datenbank mit zwei Mandanten

![Klicken Sie auf `Ausführen`oder doppelt auf `Mandanten kopieren`](/assets/images/magellan.administrator/mandanten.kopieren.png)

!!! info "Hinweis"

    Bitte lesen Sie dazu den Abschnitt [Umstieg von 6 auf 8](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-6-auf-8/)!

## Anrede setzen

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/anreden.setzen.png)

Setzt für Schüler, Bewerber, Lehrer und Personen, denen noch keine Anrede hinterlegt wurde, eine Anrede anhand des erfassten Geschlechts.
Dabei wird aus dem Geschlecht weiblich die Anrede Frau und aus dem Geschlecht männlich die Anrede Herr befüllt.

## Organisisertes Löschen

**Dieser Abschnitt wird aktuell überarbeitet.**

![Klicken Sie auf `Ausführen`](/assets/images/neues/908.png)

Der Assistent unterstützt Sie beim Löschen von wahlweise:

*  Schülerdatensätzen
*  Fachdaten von Schülern
*  Passbildern von Schülern

Sie geben als Zeitpunkt dafür eine Monatsanzahl ein, die ausgehend vom aktuellen Tagesdatum die Löschungen für Schüler durchführt, die zu diesem Zeitpunkt nicht mehr Schüler Ihrer Schule waren.  
