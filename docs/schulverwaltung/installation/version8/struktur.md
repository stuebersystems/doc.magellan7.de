# MAGELLAN-Server für mehrere Schulen

Situation: Mehrere Schulen sollen einen gemeinsamen MAGELLAN Server nutzen, somit soll der administrative Aufwand eingeschränkt und auch verlagert werden. 

Nachstehend beschreiben wir einige Punkte, die zu bedenken sind.

## Terminal-Server oder nicht?

Soll MAGELLAN aktualisiert werden, muss das auf allen eingesetzten Rechnern, also auf dem Server und auf den MAGELLAN Clients geschehen. Eine Ausnahme wäre hier der Einsatz eines Terminalservers, bei dem jeder Nutzer eine eigene Sitzung auf dem Server öffnet, die Sitzungen anderer Nutzer parallel laufen. In diesem Fall müsste nur der Terminalserver aktualisiert werden.

## Datenbanken, Firebird, Rechte

Sollen die Daten mehrer Schulen auf einem Server gespeichert werden, sollten die Datenbanken vor dem Übertrag auf dem gleichen Versionsstand sein, werden dann auf den neuen Server übertragen und können dort in einer parallelen Ordnerstruktur gespeichert werden.

Auf dem Serverrechner selbst wird  Firebird installiert. Mit der Installation wird eine Firebirddatenbank angelegt, die Teil der Benutzerverwaltung ist. In dieser Datenbank werden die Nutzer und deren verschlüsselte Passworte aller Nutzer gespeichert:

* Es gibt einen administrativen Account (sysdba), der Zugriffsrecht auf alle Schuldatenbanken hat
* weitere Unteradministratoren je Datenbank (dbadmin)
* Nutzerkonten, die jeweils je Datenbankmandant Zugriffsrechte zugewiesen bekommen

## Verzeichnisse

Mit der Server-/Einzelplatzinstallation von MAGELLAN werden Unterverzeichnisse (Berichte, Skripte, Dokumente, Vorlagen, Import, Datenbank) angelegt, auf die die Nutzer einer Schule zugreifen sollen. Auf dem Terminalserver existiert nach der Installation von MAGELLAN nur ein Satz dieser Unterverzeichnisse. Es ist sinnvoll diese Verzeichnisse je Schule zur Verfügung zu stellen, da auch aus der MAGELLAN-Oberfläche heraus dort individuelle Daten abgelegt werden können und schulspezifische Strukturen existieren können. 

## Updates

Original bei der Installation angelegte Verzeichnisse werden bei Updates aktualisiert, die je Schule aufgeteilte und individuelle gespeicherte Struktur kann später per Update nicht erreicht werden. Hier wäre nur zu bedenken, dass zusätzlich zu den Verzeichniskopien je Schule die ursprünglich installierte Struktur einmal bestehen bleibt um bei Updates die Inhalte zu aktualisieren. Diese Inhalte (neue Skripte, neu Berichte o.ä.) können dann mit einem beliebigen Synchronisationstool in die schulindividuelle Verzeichnisstruktur übertragen werden.

## MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm

Die Dateien MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm werden standardmäßig je MAGELLAN-Installation unter `C:\ProgramData\Stueber Systems\Magellan 7` gespeichert, existieren also eigentlich je MAGELLAN-Client. Es ist zusätzlich möglich diese Dateien auch von einer selbstvorgegebenen zentralen Stelle zu laden, die Information wird aus der `MAGELLAN.paths` ausgelesen. 
Eine Anleitung zum Einsatz einer MAGELLAN.paths beschreiben wir [hier](https://doc.magellan7.stueber.de/schulverwaltung/installation/die-pathsdatei/).
Arbeiten die Nutzer in einer Terminal-Server-Umgebung, muss beim Konfigurieren beachtet werden, dass diese Daten (MAGELLAN.opt, MAGELLAN.lic, MAGELLAN.evm) oder die `MAGELLAN.paths` je Nutzer individuell geladen werden können. 