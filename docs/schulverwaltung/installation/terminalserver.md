# MAGELLAN-Installation als Terminalserver

Terminalserver stellen innerhalb Ihres Netzwerks Terminals bereit. Das sind Sitzungen, die der Nutzer per Remotezugriff auf dem Terminalserver öffnet.
Jeder Nutzer hat dabei seine eigene Sitzung und arbeitet unbeeinflusst von anderen Nutzern, die sich auch am Server anmelden. Es werden lediglich die Maus- und Tastaturbewegungen zum Endgerät des Nutzers übertragen und die eigentliche Sitzung findet direkt auf dem Terminalserver stattfindet.

## Installation

Es ist möglich Firebird und MAGELLAN als Server-/Einzelplatzinstallation auf einem Terminalserver zu installieren und die Nutzer per Terminal darauf zugreifen zulassen.

## Updates

Soll MAGELLAN aktualisiert werden, müsste das auf allen eingesetzten Rechnern, also auf dem Server und auf den MAGELLAN Clients geschehen. Setzen Sie Magellan in einer Terminalserverumgebung ein, müsste nur der Terminalserver aktualisiert werden.

!!! warning "Sehr wichtig!"

    Original bei der Installation angelegte Verzeichnisse werden bei Updates aktualisiert, eine nachträglich (nach der Installation) individuell angelegte Struktur kann später per Update nicht erreicht werden.

## MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm

Die Dateien MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm werden standardmäßig je MAGELLAN-Installation unter `C:\ProgramData\Stueber Systems\Magellan 8` gespeichert, existieren also eigentlich je MAGELLAN-Client. Es ist zusätzlich möglich diese Dateien auch von einer selbstvorgegebenen zentralen Stelle zu laden, die Information wird aus der `MAGELLAN.paths` ausgelesen.
Eine Anleitung zum Einsatz einer MAGELLAN.paths beschreiben wir [hier](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).
Arbeiten die Nutzer in einer Terminal-Server-Umgebung, muss beim Konfigurieren beachtet werden, dass diese Daten (MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm) oder die `MAGELLAN.paths` je Nutzer individuell geladen werden können.