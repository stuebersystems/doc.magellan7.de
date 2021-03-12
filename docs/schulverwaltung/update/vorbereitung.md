# Update-Planung: Wird die Datenstruktur angepasst oder nicht?

Das ist der erste Punkt, der vor der Planung der Updates geprüft werden sollte. Wird nach dem Update die Datenstruktur um neue Felder oder Tabellen erweitert, müssen vorübergehend alle MAGELLAN-Nutzer von der Datenbank abgemeldet werden.

Die Versionsnummer besteht aus einem Teil, der die Ausgabe der Software kennzeichnet und einem Teil, der die Ausgabe der Datenbankversion kennzeichnet. Die Versionsnummer finden Sie im Programm unter `Hilfe > Version und Lizenz`.

Beispiel:
**Version 7.0.0 700**

Versionsnummer für die Software|Versionsnummer der Datenbank
---|---
7.0.0|700


Vergleichen Sie die letzten drei Stellen mit der im Newsletter oder im Abschnitt [Was ist neu?](http://doc.MAGELLAN7.stueber.de/changelog/) angegebenen Version. Ist die Datenbankversionsnummer dort höher angegeben, lesen Sie bitte den Abschnitt ["Updates mit Datenstrukturerweiterung"](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

!!! info "Hinweis"

     Wir informieren über neue Ausgaben über unseren [Newsletter](http://www.stueber.de/newsletter.php). 

## Updates ohne Datenstrukturerweiterung

Bitte aktualisieren Sie immer als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Sie können das aktuelle [msi-Paket](https://download.stueber.de/bin/de/MAGELLAN/v7/MAGELLAN7.msi) von unserer Webseite herunterladen und direkt per Doppelklick starten oder dazu ein Tool zur Softwareverteilung nutzen.

## Updates mit Datenstrukturerweiterung

Bitte aktualisieren Sie auch hier immer als erstes Ihren Serverrechner, führen die nachfolgend beschriebenen Schritte aus und aktualisieren anschließend alle Arbeitsplatzrechner!

Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Sie müssen dazu wie folgt vorgehen:

1. Melden Sie sich als sysdba in MAGELLAN an. 
2.  Alle anderen Benutzer müssen MAGELLAN verlassen haben!        
3.  Der Assistent zur Konvertierung erscheint, führen Sie zuerst die Sicherung Ihrer Datenbank und anschließend die die Konvertierung aus. Sollten Sie mehrere Strukturanpassungs-Updates übersprungen haben, werden diese der Reihe nach vom Assistenten durchgeführt. Schließen Sie MAGELLAN.
4. Rufen Sie den MAGELLAN-Administrator auf. Synchronisieren Sie die Zugriffsrechte der Benutzer (`Benutzerverwaltung > Zugriffsrechte synchronisieren`).

![`Benutzerverwaltung > Zugriffsrechte synchronisieren`](/assets/images/zugriffsrechte.sync.png)

!!! info "Hinweis"

    Falls es Probleme gibt, lesen Sie bitte im Abschnitt ["Probleme beim Update"](https://doc.magellan7.stueber.de/schulverwaltung/update/probleme-beim-update.html) weiter!

