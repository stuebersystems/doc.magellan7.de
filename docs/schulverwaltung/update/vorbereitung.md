# Update-Planung

Wenn ein Update ansteht, sollte der erste Schritt sein, zu prüfen, was genau in Ihrem System aktualisiert werden muss. 

Folgende Varianten wären möglich:

Variante 1| Variante 2
--|--
MAGELLAN Update (Server und Clients)| MAGELLAN Update (Server und Clients)<br/>+ Datenstrukturanpassung<br/>+ Zugriffsrechte synchronisieren

|Eventuell zusätzlich nötig|Anleitung|
|-|-|
|Firebird-Update|[Firebird aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/update/firebird-aktualisieren/)|
|Update der Crystal Reports Runtimeversion|[CR Runtime aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/update/cr-aktualisieren/)|

!!! warning "Wichtig!"    

     Muss `Firebird` aktualisiert werden oder veröffentlichen wir eine neue `Crystal Reports Runtimeversion` weisen wir unter ["Was ist neu?"](https://doc.magellan.stueber.de/changelog/changelog/) darauf hin.

Um die Ausgangsbasis zu bestimmen starten Sie bitte eine MAGELLAN-Instanz und prüfen bitte die Versionsnummer unter `Hilfe > Version und Lizenz`. 
Vergleichen Sie die letzten drei Stellen mit der im Newsletter oder im Abschnitt [Was ist neu?](https://doc.magellan.stueber.de/changelog/changelog/) angegebenen Version.

Beispiel:

**Version 9.0.1 900**

Versionsnummer für die Software|Versionsnummer der Datenbank
---|---
9.0.1|900

Ist die Datenbankversionsnummer dort höher angegeben, wäre das Variante 2, lesen Sie bitte den Abschnitt ["Updates mit Datenstrukturerweiterung"](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)! <br/>Ist die Datenbankversionsnummer gleich (Variante 1), lesen Sie bitte den nachfolgenden Abschnitt ["Updates ohne Datenstrukturerweiterung"](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-ohne-datenstrukturerweiterung).

### Updates ohne Datenstrukturerweiterung

Bitte aktualisieren Sie immer als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Sie können das aktuelle msi-Paket aus dem [Downloadbereich](https://magellan.stueber.de/download.php) unserer Webseite herunterladen und direkt per Doppelklick starten oder dazu ein Tool zur Softwareverteilung nutzen.

### Updates mit Datenstrukturerweiterung

Bitte aktualisieren Sie auch hier immer als erstes Ihren Serverrechner, führen die nachfolgend beschriebenen Schritte aus und aktualisieren anschließend alle Arbeitsplatzrechner!

Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Sie müssen dazu wie folgt vorgehen:

1. Melden Sie sich als sysdba in MAGELLAN an.
2. Alle anderen Benutzer müssen MAGELLAN verlassen haben!
3. Der Assistent zur Konvertierung erscheint, führen Sie zuerst die Sicherung Ihrer Datenbank und anschließend die die Konvertierung aus. Sollten Sie mehrere Strukturanpassungs-Updates übersprungen haben, werden diese der Reihe nach vom Assistenten durchgeführt. Schließen Sie MAGELLAN.
4. Rufen Sie den MAGELLAN-Administrator auf. Synchronisieren Sie die Zugriffsrechte der Benutzer (`Benutzerverwaltung > Zugriffsrechte synchronisieren`).

![`Benutzerverwaltung > Zugriffsrechte synchronisieren`](/assets/images/zugriffsrechte.sync.png)

!!! info "Hinweis"

    Falls es Probleme gibt, lesen Sie bitte im Abschnitt ["Probleme beim Update"](https://doc.magellan.stueber.de/schulverwaltung/update/probleme-beim-update/) weiter!

