# Installation

Dieses Kapitel beschreibt im Detail, wie Sie MAGELLAN 7 installieren.

Dieser Abschnitt beschreibt die Installation von MAGELLAN 7 mit den einzelnen Installationsschritten und Installationsarten. Bitte beachten Sie die Systemvoraussetzungen.

* Installation von Firebird
* Server-/Einzelplatzinstallation
* Arbeitsplatzinstallation
* MAGELLAN 7 starten nach Neuinstallation

!!! danger "Achtung"

    Wenn Sie bereits MAGELLAN einsetzen, lesen Sie bitte stattdessen den Abschnitt [Umstieg von MAGELLAN 6 auf MAGELLAN 7](https://doc.magellan7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/) und, falls Sie eigene Berichte verwenden, auch den Abschnitt [Berichte für MAGELLAN 7 anpassen](https://doc.magellan7.stueber.de/schulverwaltung/update/Berichte_anpassen/)!

## Netzwerk, Einzelarbeitsplatz oder einen Arbeitsplatz einrichten

Kurz vorab, je nachdem was Sie einrichten möchten sind unterschiedliche Installationen oder Installationstypen notwendig.

Was ist grob zu tun?

| Art                     | Was ist zu tun                           |
|-------------------------|------------------------------------------|
| **Netzwerk:**           | Server: auf dem Serverrechner muss eine Firebird-Installation und MAGELLAN als Server/Einzelplatz-Installation durchgeführt werden. <br/><br/>Arbeitsplätze: Auf den Arbeitsplatzrechnern wird nur MAGELLAN mit dem Installationstyp "Arbeitsplatzinstallation" ausgeführt und die Verbindung zu dem auf dem Rechner abgelegten gemeinsam verwendeten Daten (Datenbank, Datenordner mit Skripten, Berichten usw.) eingerichtet. <br/><br/>Alle Rechner: Die Lizenz und die Verbindungsdaten werden pro Installation eingetragen. Alternativ können auch mehrere MAGELLAN-Installationen auf eine gemeinsame Lizenzdatei  und/oder Verbindungsdatei zugreifen. Was Sie dafür einrichten müssen beschreiben wir im Abschnitt [Die Pathsdatei](https://doc.magellan7.stueber.de/schulverwaltung/installation/die-pathsdatei/). |
| **Einzelarbeitsplatz:** | Ein Einzelarbeitsplatz wird genau wie ein Serverrechner eingerichtet:<br/><br/> - Installieren Sie Firebird.<br/> - MAGELLAN wird als Server/Einzelplatz-Installation eingerichtet.. <br/> - Lizenzieren Sie die Installation. |
| **Arbeitsplatz:**       | Sie haben ein Netzwerk bestehend aus einem MAGELLAN-Server und Arbeitsplatzrechnern und möchten nur einen weiteren Arbeitsplatzrechner einrichten? <br/><br/> - Führen Sie auf dem Rechner die MAGELLAN-Installation mit dem Installationstyp "Arbeitsplatzinstallation" aus. <br/> -  Lizenzieren Sie den Arbeitsplatz. <br/> - Richten die Verbindung zu den Daten auf dem Server ein. <br/><br/>Auch hier ist es möglich statt lokaler Verbindungsdaten und Lizenz per [Pathsdatei](https://doc.magellan7.stueber.de/schulverwaltung/installation/die-pathsdatei/) auf gemeinsame Daten zu verweisen. |
