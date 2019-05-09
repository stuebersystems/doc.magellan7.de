# Datenstrukturanpassung findet keine Skripte oder der Pfad ist verkehrt

vier Möglichkeiten können hinter diesem Problem stecken: 

1.	dem Server fehlt das Update und damit auch die Strukturanpassungsskripte
2.	der Server hat das Update erhalten, aber das Update konnte die Anpassungsskripte nicht ablegen
3.	die Pfade zum Skripteverzeichnis auf dem Server fehlen
4.	die Pfade zum Skripteverzeichnis auf dem Server sind verkehrt

Zu 1.: Bitte immer als erstes den Serverrechner aktualisieren, da dieser Rechner der einzige im Netzwerk ist, der die gemeinsam genutzten Programmkomponenten, wie zum Beispiel die Skripte hat und für die Clientinstallationen zur Verfügung stellt.

Zu 2.: Sollten nach dem Update die Skripte u.a. dennoch nicht aktuell sein, kann es damit zusammenhängen, dass nach der ursprünglichen Serverinstallation die Pfade nachträglich verschoben wurden. Der bei der Installation und bei den Updates verwendete Windows Installer „möchte“ die Dateien am ursprünglichen Speicherort aktualisieren. Sollte dieser nicht mehr bestehen, müsste erneut installiert werden und gleich auf die gewünschten Pfade verwiesen werden.

Zu 3. und 4.: Eventuell wurde bei der Installation kein oder nicht der korrekte Pfad zu dem Skripteordner erfasst. Bitte rufen Sie das Anmeldefenster des Administrators auf und wählen die folgende Einstellung:

![](../assets/images/admin_ohne_anmeldung.jpg)
   
Anschließend rufen Sie im Administrator den Punkt Server-Verwaltung|Verbindungen verwalten|Starten|Verbindung markieren|Bearbeiten|Unterkarte "Datenordner" auf. Steht dort der Pfad zum Ordner Skripte? Wenn nicht tragen Sie ihn bitte nach.
  
Die Datenordner liegen je nach Betriebssystem bei unverändert übernommenen Installationspfaden an den nachfolgenden Stellen:
(Pfad bitte jeweils um den Namen des Verzeichnisses ergänzen: Berichte, Skripte, Vorlagen, Importe, Dokumente, Datenbank) finden Sie unter:

| Betriebssystem    |Standardpfad|
| --                | --         |
|  Vista            | C:\Users\Public\Documents\Magellan 6  |
|XP                 |C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber S...\Magellan 6|
|Windows 2000       |C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber S...\Magellan 6 |
|Windows 7          |C:\Users\Public\Documents\Stueber S...\Magellan 6 |
|Windows Server 2008|C:\Users\Public\Documents\Stueber S...\Magellan 6\ |


