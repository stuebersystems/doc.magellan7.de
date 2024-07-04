# Installation

Dieses Kapitel beschreibt im Detail, wie Sie Magellan installieren.

Dieser Abschnitt beschreibt die Installation von Magellan mit den einzelnen Installationsschritten und Installationsarten. Bitte beachten Sie die [Systemvoraussetzungen](https://doc.magellan.stueber.de/schulverwaltung/installation/systemvoraussetzungen/).

* Installation von Firebird und Server-/Einzelplatzinstallation
* Arbeitsplatzinstallation
* Magellan starten nach Neuinstallation

Setzen Sie bereits Magellan ein? Dann finden Sie nachstehend in der Tabelle die Links zu den jeweiligen Umstiegsanleitungen.

Eingesetzte Version|Anleitung fürs Upgrade
--|--
Version 8|[https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-8-auf-9/](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-8-auf-9/)
Version 7|[https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-7-auf-8/](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-7-auf-8/)
Version 6|[https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-6-auf-8/](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-6-auf-8/)

## Magellan zum ersten Mal einrichten

Kurz vorab, je nachdem was Sie einrichten möchten sind unterschiedliche Installationen oder Installationstypen notwendig.

Was ist grob zu tun?

| Art                     | Was ist zu tun                           |
|-------------------------|------------------------------------------|
| **Netzwerk:**           | Server: auf dem Serverrechner muss eine Firebird-Installation und Magellan als Server/Einzelplatz-Installation durchgeführt werden. <br/><br/>Arbeitsplätze: Auf den Arbeitsplatzrechnern wird nur Magellan mit dem Installationstyp "Arbeitsplatzinstallation" ausgeführt und die Verbindung zu dem auf dem Rechner abgelegten gemeinsam verwendeten Daten (Datenbank, Datenordner mit Skripten, Berichten usw.) eingerichtet. <br/><br/>Alle Rechner: Die Lizenz und die Verbindungsdaten werden pro Installation eingetragen. Alternativ können auch mehrere Magellan-Installationen auf eine gemeinsame Lizenzdatei  und/oder Verbindungsdatei zugreifen. Was Sie dafür einrichten müssen beschreiben wir im Abschnitt [Die Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/). |
| **Einzelarbeitsplatz:** | Ein Einzelarbeitsplatz wird genau wie ein Serverrechner eingerichtet:<br/><br/> - Installieren Sie Firebird.<br/> - Magellan wird als Server/Einzelplatz-Installation eingerichtet.. <br/> - Lizenzieren Sie die Installation. |
| **Arbeitsplatz:**       | Sie haben ein Netzwerk bestehend aus einem Magellan-Server und Arbeitsplatzrechnern und möchten nur einen weiteren Arbeitsplatzrechner einrichten? <br/><br/> - Führen Sie auf dem Rechner die Magellan-Installation mit dem Installationstyp "Arbeitsplatzinstallation" aus. <br/> -  Lizenzieren Sie den Arbeitsplatz. <br/> - Richten die Verbindung zu den Daten auf dem Server ein. <br/><br/>Auch hier ist es möglich statt lokaler Verbindungsdaten und Lizenz per [Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/) auf gemeinsame Daten zu verweisen. |
