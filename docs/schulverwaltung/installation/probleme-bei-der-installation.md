# Probleme bei der Installation

## Die Erstanmeldung klappt nicht

Folgende Ursachen könnten der Grund sein: MAGELLAN startet auf dem Serverrechner nicht? Ist Firebird auf dem Serverrechner installiert und gestartet? In der Systemsteuerung Ihres Serverrechners finden Sie unter `Verwaltung > Dienste` einen Aufruf für den Firebird-Datenbank-Manager. Die Einstellungen sollten wie folgt sein:

![Firebird Server Einstellungen](/assets/images/fb-control.png)

## Datenbank und Firebird sind auf unterschiedlichen Partitionen installiert

Firebird nutzt für den Datenverkehr den **Port 3050**, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme (Eingehende und Ausgehende Regel) für diesen Port ein und versuchen es bitte erneut.

## Der Pfad zur Datenbank ist verkehrt

Starten Sie den Magellan-Administrator ohne Anmeldung:

`Starten > Verbindung markieren > Bearbeiten > Unterkarte „Datenbank“`. Bitte prüfen Sie, dass Pfad zur Datenbank korrekt ist (Achtung: nachstehende Abbildung enthält lediglich einen Beispielpfad!) und mit dem Dateinamen der Datenbank endet, wie in der folgenden Abbildung:

!["Datenbank registrieren"](/assets/images/admin-connection-dialog.png )

## MAGELLAN startet auf dem Arbeitsplatzrechner nicht

Eventuell ist auch hier der Pfad zur Datenbank verkehrt. Starten Sie bitte den MAGELLAN-Administrator ohne Anmeldung:

![Magellan Administrator starten ohne Anmeldung](/assets/images/admin-ohne-anmeldung.png)

Prüfen Sie bitte, dass für die Arbeitsplatzinstallation der Pfad zur Datenbank 1:1 wie auf dem Serverrechner eingetragen wurde. Der Unterschied in der Verbindung liegt nur in den Feldern „Protokoll“ und „Server“.

Im Feld Protokoll sollte TCP/IP gewählt werden, im Feld Server tragen Sie bitte nur den Namen des Serverrechners oder die IP-Adresse des Serverechners ein.

## Port 3050 freigeben

Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme (Eingehende und Ausgehende Regel) für diesen Port ein und versuchen es bitte erneut.

## Fehler beim Schreiben in Datei. CrystalDecisions.CrystalReports.Engine.dll

![Fehlermeldung](/assets/images/installation/03.png)

Die vorstehende Meldung erscheint, wenn erwartete Programmbibliotheken nicht auf dem Rechner gefunden werden.

Das ist in den meisten Fällen unwahrscheinlich, da diese beispielsweise mit dem Officepaket installiert werden sollten. Sollten Sie diese Meldung erhalten, laden Sie über den untenstehenden Downloadlink bitte das Paket herunter.

Führen Sie die Installation per Doppelklick aus, im Anschluss installieren Sie bitte MAGELLAN erneut oder führen Sie eine Reparaturinstallation aus.

[https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net462-web-installer](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net462-web-installer)

## Fehler beim Registrieren von Modul ... crtslv.dll

![Fehlermeldung](/assets/images/installation/fehler_cr.png)

Die vorstehende Meldung erscheint, wenn erwartete Programmbibliotheken nicht auf dem Rechner gefunden werden.

Das ist in den meisten Fällen unwahrscheinlich, da diese beispielsweise mit dem Officepaket installiert werden sollten. Sollten Sie diese Meldung erhalten, laden Sie über den untenstehenden Downloadlink bitte das Paket herunter.

Führen Sie die Installation per Doppelklick aus, im Anschluss installieren Sie bitte MAGELLAN erneut oder führen Sie eine Reparaturinstallation aus.

[https://download.stueber.de/bin/de/common/vc_redist_2015/vc_redist.x86.exe](https://download.stueber.de/bin/de/common/vc_redist_2015/vc_redist.x86.exe)

## Typeninitialisierer für Crystal.Decisions

![Fehlermeldung](/assets/images/installation/02.png)

Die vorstehende Meldung erscheint, wenn erwartete Programmbibliotheken nicht auf dem Rechner gefunden werden.

Das ist in den meisten Fällen unwahrscheinlich, da diese beispielsweise mit dem Officepaket installiert werden sollten. Sollten Sie diese Meldung erhalten, laden Sie über den untenstehenden Downloadlink bitte das Paket herunter.

Führen Sie die Installation per Doppelklick aus, im Anschluss installieren Sie bitte MAGELLAN erneut oder führen Sie eine Reparaturinstallation aus.

[https://download.stueber.de/bin/de/common/vc_redist_2015/vc_redist.x86.exe](https://download.stueber.de/bin/de/common/vc_redist_2015/vc_redist.x86.exe)

## Der Typeninitialisiert für "CrystalDecisions.CrystalReports.Engine.CRPE"...

Meldung:
Der Typeninitialisiert für "CrystalDecisions.CrystalReports.Engine.CRPE" hat eine Ausnahme verursacht.

![Meldung](/assets/images/update/Fehler01.png)

Die vorstehende Meldung erscheint, wenn auf dem Betriebssystem Teile der Runtimeversion nicht korrekt beim Update oder bei der Installation vorn MAGELLAN registriert werden konnten. Bitte laden Sie in diesem Fall die nachstehende Datei herunter und führen sie aus, es wird die für den Druck und Druckvorschau von MAGELLAN notwendige Runtimeversion von MAGELLAN gesondert installiert.

[https://download.stueber.de/bin/de/common/cr_runtime/CR13SP30MSI32_0-10010309.MSI](https://download.stueber.de/bin/de/common/cr_runtime/CR13SP30MSI32_0-10010309.MSI)