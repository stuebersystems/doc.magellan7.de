# Datenbankpflege

## Generatoren synchronisieren

Setzt die Generatoren zur Erstellung der automatisch hochgezählten Ids auf den nächstmöglichen Wert. Diese Funktion sollte zum Beispiel nach dem Leeren der Datenbank ausgeführt werden.

![Klicken Sie auf `Ausführen`oder doppelt auf `Generatoren synchronisieren`](/assets/images/magellan.administrator/generatoren.sync.png)

## Gemeinden synchronisieren

Setzt für Schüler, Betriebe, Lehrer, Schulen und Sorgeberechtigte (Sorgeberechtigte neu ab 7.0.12) die Gemeindekennziffern anhand der PLZ und des Ortes, wenn damit nicht mehrere Gemeinden gekennzeichnet sind.
Es werden nur nicht vorhandene Gemeinden gesetzt.

![Klicken Sie auf `Ausführen`oder doppelt auf `Gemeinden synchronisieren`](/assets/images/magellan.administrator/gemeinden.sync.png)

## Korrektur Mandanten kopieren (702)

MAGELLAN 7 erlaubt es den Schüler in Stamm- und Nebenschüler zur trennen, um parallel laufende Laufbahnen abzubilden. Die Stammdaten werden jeweils nur beim Stammschüler gespeichert, aber bei Stammschüler oder Nebenschüler eingegeben und gezeigt.
Beim Kopieren der Daten aus MAGELLAN 6 nach MAGELLAN 7.0.2 sind die Ausbildungen und Herkünfte der Nebenschüler nicht zum Stammschüler umgeboten worden, weshalb diese nicht in MAGELLAN 7 gezeigt werden. Diese Funktion korrigiert diesen Umstand.

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/korrektur.mandant.png)


## Aktuelle Bewerber-Ausbildung setzen

Diese Funktion setzt für alle Bewerber, die nur eine Ausbildung unter `Bewerber > Ausbildung` haben, diese Ausbildung auf "aktuelle Ausbildung". Der Eintrag als "aktuelle Ausbildung" ist Voraussetzung für den Seriendruck und -mail an den Bewerberbetrieb und für einige Berichte.

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/akt.bewerber.png)

## Code 128 generieren

Legt für Schüler, Lehrer und Personen fehlende Barcodes (Code 128) an. Für direkt in MAGELLAN angelegte Schüler, Lehrer oder Personen wird dieser Barcode automatisch erzeugt. Für alte Datenbestände oder importierte Datensätze kann dieser Barcode für Schülerausweise auf diesem Weg nachträglich erzeugt werden.
Der für die Bibliothek für die Medienausleiher(Schüler, Lehrer, Personen) erzeugte Barcode hat hiermit nichts zu tun. Dieser gesonderte Barcode wird erzeugt, wenn ein Schüler/Lehrer/Person als Medienausleiher in die MAGELLAN Bibliothek übernommen wird.

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/code128.png)

## Mandanten kopieren

Kopiert MAGELLAN-Daten in eine andere MAGELLAN-Datenbank. Zum Beispiel zur

* Datenübernahme einer MAGELLAN 6 Datenbank
* Datenrettung bei erfolglosem Versuch einer Datenbankreparatur (Datapump)
* Zusammenführen von Daten zweier Datenbanken in eine Datenbank mit zwei Mandanten

![Klicken Sie auf `Ausführen`oder doppelt auf `Mandanten kopieren`](/assets/images/magellan.administrator/mandanten.kopieren.png)

![Varianten des `Mandanten kopieren`](/assets/images/magellan.administrator/mandanten.kopieren1.png)

### Variante 1: Mandantenunabhängig (vollständig)

Das nicht mandantenbezogene Kopieren der MAGELLAN-Daten überträgt alle Daten aller Tabellen in eine neue leere Datenbank. Diese Variante ist besonders bei eventuell korrupten Datenbanken geeignet.

> #### warning::Wichtig!
>
> Übertragen werden können Daten aus einer MAGELLAN 7 Datenbank in eine leere MAGELLAN 7 Datenbank.

![Mandantenunabhängig (vollständig)](/assets/images/magellan.administrator/mandanten.kopieren2.png)

![Eintragungen](/assets/images/magellan.administrator/mandanten.kopieren3.png)

Feld|Anmerkung
--|--
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Quelldatenbank|Tragen Sie bitte den lokalen Pfad zur Quelldatenbank und deren Dateinamen ein.
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Zieldatenbank|Tragen Sie bitte den lokalen Pfad zur Zieldatenbank und deren Dateinamen ein. **Bitte beachten Sie, dass eine leere Zieldatenbank erwartet wird. Über das Symbol am Ende der Zeile können Sie eine leere MAGELLAN 7 Datenbank herunterladen.**
Benutzernamen<br/>Kennwort|Tragen Sie als Benutzer bitte den sysdba und das dazugehörige Passwort ein.

### Variante 2: Mandantenabhängig

!!! warning "Wichtig"

    Dieser Abschnitt der Dokumentation ist aktuell nicht gültig und steht in Kürze überarbeitet zur Verfügung!

Das mandantenbezogene Kopieren der MAGELLAN Daten überträgt lediglich Tabellen und Dateien, die sich auf einen ausgewählten Mandanten beziehen.

![Mandantenabhängig](/assets/images/magellan.administrator/mandanten.kopieren4.png)

![Eintragungen](/assets/images/magellan.administrator/mandanten.kopieren3.png)

Feld|Anmerkung
--|--
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Quelldatenbank|Tragen Sie bitte den lokalen Pfad zur Quelldatenbank und deren Dateinamen ein.
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Zieldatenbank|Tragen Sie bitte den lokalen Pfad zur Zieldatenbank und deren Dateinamen ein. 
Benutzernamen<br/>Kennwort|Tragen Sie als Benutzer bitte den sysdba und das dazugehörige Passwort ein.

Um alle mandantenbezogenen Daten eines Mandanten aus einer MAGELLAN-Datenbank A (=Ausgangsdatenbank) in eine MAGELLAN-Datenbank B (=Zieldatenbank) zu kopieren, gehen Sie wie folgt vor:

Vor dem Kopieren der mandantenbezogen Daten in eine andere MAGELLAN-Datenbank müssen folgenden Voraussetzungen erfüllt sein:

* Ausgangs- und Zieldatenbank müssen die gleichen Zeiträume besitzen.
* Der zu kopierenden Mandant darf noch nicht in der Zieldatenbank existieren.
* Das Kürzel des zu kopierenden Mandanten darf noch nicht als Kürzel für einen Mandanten der Zieldatenbank verwendet worden sein.

!!! info "Hinweis"

     Über die Funktion „Mandanten kopieren“ können Sie die Inhalte zweier Mandanten aus verschieden MAGELLAN-Datenbanken zu einer einzigen MAGELLAN-Datenbank mit zwei Mandanten zusammenführen. Auf diese Weise können beispielweise zwei Schulen mit bisher getrennt arbeitenden MAGELLAN-Datenbanken auf einer einzigen MAGELLAN-Datenbank arbeiten und die Vorteile einer SchoolCentral-Lösung nutzen.

### Variante 3: Magellan 6 nach MAGELLAN 7

Bitte lesen Sie dazu den Abschnitt [Umstieg von 6 auf 7](https://doc.magellan7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/)!

## Anrede setzen

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/anreden.setzen.png)

Setzt für Schüler, Bewerber, Lehrer und Personen, denen noch keine Anrede hinterlegt wurde, eine Anrede anhand des erfassten Geschlechts.
Dabei wird aus dem Geschlecht weiblich die Anrede Frau und aus dem Geschlecht männlich die Anrede Herr befüllt.

## Schüler-Passfotos löschen

![Klicken Sie auf `Ausführen`](/assets/images/magellan.administrator/passfoto.loeschen.png)

Löscht alle Passfotos inaktiver Schüler aus der Datenbank heraus.
Die Größe der Datenbank reduziert sich, wenn Sie anschließend die Datenbank sichern und wiederherstellen.

## Verwaiste Stammschüler-Verweise entfernen

Diese Funktionalität entfernt Einträge im Feld `IDIntern` bei Nebenschülern, die auf einen nicht mehr existenten Stammschüler verweisen. Diese Situation kann durch Fehleinträge in MAGELLAN 6 entstanden sein und ist in MAGELLAN 7 nicht mehr möglich.

![Verwaiste Stammschüler-Verweise entfernen](/assets/images/magellan.administrator/verwaiste.eintraege.png)