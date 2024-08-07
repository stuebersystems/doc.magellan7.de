# Update-Planung

Wenn ein Update ansteht, sollte der erste Schritt sein, zu prüfen, was genau in Ihrem System aktualisiert werden muss. 

Folgende Varianten wären möglich:

Variante 1| Variante 2
--|--
Magellan Update (Server und Clients)| Magellan Update (Server und Clients)<br/>+ Datenstrukturanpassung<br/>+ Zugriffsrechte synchronisieren

!!! warning "Wichtig!"    

     Eventuell zusätzlich nötig kann es sein, [Firebird](https://doc.magellan.stueber.de/schulverwaltung/update/firebird-aktualisieren/) und/oder [CR Runtime](https://doc.magellan.stueber.de/schulverwaltung/update/cr-aktualisieren/) zu aktualisieren. Wir weisen auch darauf in der [Was ist neu?](https://doc.magellan.stueber.de/changelog/changelog/)  hin.

## Ausgangsbasis bestimmen

Um die Ausgangsbasis zu bestimmen starten Sie bitte eine Magellan-Instanz und prüfen bitte die Versionsnummer unter `Hilfe > Version und Lizenz`. 
Vergleichen Sie die letzten drei Stellen mit der im Newsletter oder im Abschnitt [Was ist neu?](https://doc.magellan.stueber.de/changelog/changelog/) angegebenen Version.

Beispiel: **Version 10.0.1 100**

Versionsnummer für die Software|Versionsnummer der Datenbank
---|---
10.0.1|100

Ist die Datenbankversionsnummer dort höher angegeben, wäre das Variante 2, lesen Sie bitte den Abschnitt ["Updates mit Datenstrukturerweiterung"](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)! <br/>Ist die Datenbankversionsnummer gleich (Variante 1), lesen Sie bitte den nachfolgenden Abschnitt ["Updates ohne Datenstrukturerweiterung"](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/#updates-ohne-datenstrukturerweiterung).

## 32 oder 64 Bit

Für ein Update benötigen Sie die Installationsdateien für:

* die Runtimeversion von Crystal Reports 32- oder 64-Bit
* für Magellan 32- oder 64-Bit

**Nutzen Sie ein 32-Bit oder 64-Bit-Betriebssystem?**

1. Wählen Sie `Start > Einstellungen > System > Info` aus.
2. Unter `Gerätespezifikationen > Systemtyp` sehen Sie, ob Sie eine 32-Bit-Version oder eine 64-Bit-Version von Windows verwenden.

!!! danger "Wichtig!"

    Alle Installationspakete finden Sie [in unserem Downloadbereich](https://magellan.stueber.de/download.php).<br/>**Für Windows 32-Bit und 64-Bit gibt es gesonderte Installationsdateien für Magellan und für die Runtimeversion von Crystal Reports.**

## Updates ohne Datenstrukturerweiterung

Bitte aktualisieren Sie immer als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Sie können das aktuelle msi-Paket aus dem [Downloadbereich](https://magellan.stueber.de/download.php) unserer Webseite herunterladen und direkt per Doppelklick starten oder dazu ein Tool zur Softwareverteilung nutzen.

## Updates mit Datenstrukturerweiterung

Bitte aktualisieren Sie auch hier immer als erstes Ihren Serverrechner, führen die nachfolgend beschriebenen Schritte aus und aktualisieren anschließend alle Arbeitsplatzrechner!

Beim ersten Start von Magellan erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Sie müssen dazu wie folgt vorgehen:

1. Melden Sie sich als sysdba in Magellan an.
2. Alle anderen Benutzer müssen Magellan verlassen haben!
3. Der Assistent zur Konvertierung erscheint, führen Sie zuerst die Sicherung Ihrer Datenbank und anschließend die die Konvertierung aus. Sollten Sie mehrere Strukturanpassungs-Updates übersprungen haben, werden diese der Reihe nach vom Assistenten durchgeführt. Schließen Sie Magellan.
4. Rufen Sie den Magellan-Administrator auf. Synchronisieren Sie die Zugriffsrechte der Benutzer (`Benutzerverwaltung > Zugriffsrechte synchronisieren`).

![`Benutzerverwaltung > Zugriffsrechte synchronisieren`](/assets/images/zugriffsrechte.sync.png)

!!! info "Hinweis"

    Falls es Probleme gibt, lesen Sie bitte im Abschnitt ["Probleme beim Update"](https://doc.magellan.stueber.de/schulverwaltung/update/probleme/) weiter!