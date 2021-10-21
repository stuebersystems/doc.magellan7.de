# MAGELLAN-Installation als Terminalserver

Terminalserver stellen innerhalb Ihres Netzwerks sogenannte Terminals bereit. Das sind Sitzungen, die der Nutzer per Remotezugriff auf dem Terminalserver öffnet.
Jeder Nutzer hat dabei seine eigene Sitzung und arbeitet unbeeinflusst von anderen Nutzern, die sich auch am Server anmelden. Das System hat Vorteile (bspw. Updates müssen nur auf dem Terminalserver eingespielt werden) und Nachteile (bspw. Bildschirminhalte und Eingaben die per Internet übertragen werden, sind immer durch eine gewisse Latenz gekennzeichnet), die von den Schulen abgewägt werden müssen.

## Installation

Es ist möglich Firebird und MAGELLAN als Server-/Einzelplatzinstallation auf einem Terminalserver zu installieren und die Nutzer per Terminal darauf zugreifen zulassen.

## Updates

Soll MAGELLAN aktualisiert werden, müsste das auf allen eingesetzten Rechnern, also auf dem Server und auf den MAGELLAN Clients geschehen. Setzen Sie Magellan in einer Terminalserverumgebung ein, müsste nur der Terminalserver aktualisiert werden.

!!! warning "Sehr wichtig!"

    Original bei der Installation angelegte Verzeichnisse werden bei Updates aktualisiert, eine nachträglich (nach der Installation) individuell angelegte Struktur kann später per Update nicht erreicht werden.

## benutzerindividuelle Daten

Die Dateien MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm werden standardmäßig je MAGELLAN-Installation unter `C:\ProgramData\Stueber Systems\Magellan 8` gespeichert, existieren also eigentlich je MAGELLAN-Client. Arbeiten die Nutzer in einer Terminal-Server-Umgebung, muss beim Konfigurieren beachtet werden, dass diese Daten (MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm) oder die `MAGELLAN.paths` je Nutzer individuell geladen werden können.

!!! tipp "Hinweis!"

    Es ist zusätzlich möglich diese Dateien auch von einer selbstvorgegebenen zentralen Stelle zu laden, die Information wird aus der `MAGELLAN.paths` ausgelesen. Eine Anleitung zum Einsatz einer MAGELLAN.paths beschreiben wir [hier](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).
