# Probleme bei Installation oder Update

Beim ersten Einrichten oder beim späteren Update von MAGELLAN gibt es umgebungsspezifische Ursachen für Probleme, die wir gesammelt haben und nachstehend jeweils den Lösungsansatz beschreiben.

## Installation

### Die Erstanmeldung klappt nicht

Folgende Ursachen könnten der Grund sein: MAGELLAN startet auf dem Serverrechner nicht? Ist Firebird auf dem Serverrechner installiert und gestartet? In der Systemsteuerung Ihres Serverrechners finden Sie unter `Verwaltung > Dienste` einen Aufruf für den Firebird-Datenbank-Manager. Die Einstellungen sollten wie folgt sein:

![Firebird Server Einstellungen](/assets/images/fb-control.png)

### Datenbank und Firebird sind auf unterschiedlichen Partitionen installiert

Firebird nutzt für den Datenverkehr den **Port 3050**, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme (Eingehende und Ausgehende Regel) für diesen Port ein und versuchen es bitte erneut.

### Der Pfad zur Datenbank ist verkehrt

Starten Sie den Magellan-Administrator ohne Anmeldung:

`Starten > Verbindung markieren > Bearbeiten > Unterkarte „Datenbank“`. Bitte prüfen Sie, dass Pfad zur Datenbank korrekt ist (Achtung: nachstehende Abbildung enthält lediglich einen Beispielpfad!) und mit dem Dateinamen der Datenbank endet, wie in der folgenden Abbildung:

!["Datenbank registrieren"](/assets/images/admin-connection-dialog.png )

### MAGELLAN startet auf dem Arbeitsplatzrechner nicht

Eventuell ist auch hier der Pfad zur Datenbank verkehrt. Starten Sie bitte den MAGELLAN-Administrator ohne Anmeldung:

![Magellan Administrator starten ohne Anmeldung](/assets/images/admin-ohne-anmeldung.png)

Prüfen Sie bitte, dass für die Arbeitsplatzinstallation der Pfad zur Datenbank 1:1 wie auf dem Serverrechner eingetragen wurde. Der Unterschied in der Verbindung liegt nur in den Feldern „Protokoll“ und „Server“.

Im Feld Protokoll sollte TCP/IP gewählt werden, im Feld Server tragen Sie bitte nur den Namen des Serverrechners oder die IP-Adresse des Serverechners ein.

### Port 3050 freigeben

Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme (Eingehende und Ausgehende Regel) für diesen Port ein und versuchen es bitte erneut.

## Updates

In den nachfolgenden Punkte beschreiben wir die Lösungen zu Problemen, die bei Updates auftreten können. 

### Datenbanksicherung kann nicht erstellt werden

Die Sicherung der Datenbank kann nur auf dem selben Rechner erstellt werden, auf dem auch die Datenbank selbst gespeichert ist. Versuchen Sie die Sicherung auf einem anderen Rechner oder über ein Netzlaufwerk erstellen zu lassen, stoppt der Assistent mit nachfolgender Meldung.  
Bitte wählen Sie einen lokales Verzeichnis, wir empfehlen das Verzeichnis "Backup" in Ihrem Datenbankverzeichnis und einen Dateinamen, der das Tagesdatum enthält.

Beispiel die Benennung: 2016-04-23.fbk

![Fehlermeldung wenn die Sicherung nicht lokal gespeichert wird](/assets/images/sicherungnichtlokalspeichern.jpg)

### Die Magellan-Datenbank-ODS-Version ist nicht aktuell

Der Assistent prüft die ODS-Version (On-Disc-Structure) der Datenbank, um das Strukturupdate korrekt ausführen zu können. Ihre Datenbank sollte für die Anpassung bestimmte Befehle "kennen". Durch das Sichern und anschließende Wiederherstellen erhöht sich die ODS-Version , d.h. die Datenbank "lernt" neue Befehle. 
Folgende Schritte sind nötig:

1.	Firebird aktualisieren
2.	Sichern und Wiederherstellen der Datenbank im MAGELLAN ADMINISTRATOR > Datensicherung
3.	Firebird stoppen
4.	wiederhergestellte Datenbank gegen Realdatenbank tauschen
5.	Firebird starten
6.	MAGELLAN starten Datenstruktur anpassen
7.	MAGELLAN ADMINISTRATOR starten und Datenbankpflege > Zugriffsrechte synchronisieren ausführen.

Prüfen Sie bitte auf Ihrem Serverrechner in der Systemsteuerung im "Firebird-Server-Manager" oder unter dem Punkt "Programme und Funktionen|Firebird" welche Version von Firebird Sie einsetzen. Die aktuell empfohlene Ausgabe finden Sie auf unserer Webseite im [Downloadbereich](https://magellan.stueber.de/download.php). 

Wenn Sie diese Meldung erhalten, laden Sie über den Link unten links im Meldungsfenster die aktuelle Firebird-Version herunter. Stoppen Sie dann die aktuelle Firebird-Installation auf dem Serverrechner unter ```Systemsteuerung > Klassische Ansicht > Firebird-Server-Manager``` und schließen das Firebird-Fenster wieder. 

Falls Sie den Aufruf in der Systemsteuerung nicht finden können, rufen Sie stattdessen den Punkt ```Systemsteuerung > Verwaltung > Dienste > Firebird-Server ```per Doppelklick auf stoppen den Dienst hier.

Starten Sie anschließend die Installation von Firebird per Doppelklick auf das Installationspaket und folgen dem Assistenten. Starten Sie anschließend den Firebird-Dienst wieder in der Systemsteuerung. Wenn Sie diese Version bereits einsetzen, dann fehlen noch die folgenden Schritte:

1.	Melden Sie sich auf dem Serverrechner als sysdba am Magellan-Administrator an. Es wird erkannt, dass die Datenbank nicht in der aktuellen Version vorliegt, daher wird der Administrator nur mit dem Punkt Datenbanksicherung geöffnet.
2.	Wählen Sie den Punkt ```Datensicherung > Sicherungskopie```, geben einen Pfad und einen Datennamen an. Beispiel: ```C|...|Stüber Systems|Magellan 6|Datenbank|Backup|2016-03-24.fbk``` Starten Sie die Sicherung! 
1.	Im Anschluss stellen Sie die Datensicherung wieder her, die "Echtdatenbank" kann dabei nicht überschrieben werden.
 
1.	Stoppen den Firebird-Dienst (Systemsteuerung|Firebird Server Manager).
2.	Tauschen die Echtdatenbank gegen die wiederhergestellte Datenbank aus und starten den Firebird-Dienst wieder. 
	
>Den Pfad zur Echtdatenbank auf Ihrem Serverrechner finden Sie unter ```MAGELLAN ADMINISTRATOR > Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Unterkarte Datenordner```.

3.	Starten Sie Magellan erneut als sysdba und führen Sie die Datenstrukturerweiterung aus.

### Andere Benutzer sind noch angemeldet

Für die Datenstrukturanpassung darf kein Nutzer außer dem sysdba, der die Anpassung durchführt, angemeldet sein. Wenn Sie nicht wissen, wer in Ihrem Netzwerk noch ein Magellan-Modul(Schulverwaltung, Bibliothek, Haushalt&Inventar u.a) gestartet hat, können Sie den Firebird-Dienst stoppen und erneut starten. Öffnen Sie dazu auf Ihrem Server-Rechner in der Systemsteuerung den Punkt Firebird-Server-Manager, stoppen den Dienst und starten ihn erneut. 

![Firebird-Dienst über das Firebird-Control in der Systemsteuerung stoppen](/assets/images/fb_control_stoppen.png)

Alternativ können Sie den Firebird-Server auch unter `Start > Systemsteuerung > Verwaltung > Dienste` anhalten.


![Firebird-Dienst stoppen](/assets/images/firebird_stop.jpg)

Fehlt Ihnen der Aufruf in der Systemsteuerung? Sie können den Dienst auch unter Systemsteuerung|Verwaltung|Dienste|Firebird-Server finden.

### MAGELLAN findet den Skripteordner nicht

Sie starten nach dem Update MAGELLAN und erhalten folgende Meldung?

![Fehlermeldung beim Start von MAGELLAN](/assets/images/strukturanpassenfehler2.png)

Nr|Ursache
--|--
1.|	die Pfade zum Skripteverzeichnis auf dem Server fehlen
2.|	die Pfade zum Skripteverzeichnis auf dem Server sind verkehrt

Eventuell wurde bei der Installation kein oder nicht der korrekte Pfad zu dem Skripteordner erfasst. Bitte rufen Sie das Anmeldefenster des Administrators auf und wählen die folgende Einstellung:

![Magellan Administrator starten ohne Anmeldung](/assets/images/admin-ohne-anmeldung.png)
   
Anschließend rufen Sie im Administrator den Punkt Server-Verwaltung|Verbindungen verwalten|Starten|Verbindung markieren|Bearbeiten|Unterkarte "Datenordner" auf. Steht dort der Pfad zum Ordner Skripte? Wenn nicht tragen Sie ihn bitte nach.
  
Die Datenordner liegen je nach Betriebssystem bei unverändert übernommenen Installationspfaden an den nachfolgenden Stellen:
(Pfad bitte jeweils um den Namen des Verzeichnisses ergänzen: Berichte, Skripte, Vorlagen, Importe, Dokumente, Datenbank) finden Sie unter:

| Betriebssystem    |Standardpfad|
| --                | --         |
|  Vista            | C:\Users\Public\Documents\Magellan 7  |
|XP                 |C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber S...\Magellan 7|
|Windows 2000       |C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber S...\Magellan 7 |
|Windows 7          |C:\Users\Public\Documents\Stueber S...\Magellan 7 |
|Windows Server 2008|C:\Users\Public\Documents\Stueber S...\Magellan 7\ |

### Trotz Update fehlen Skripte oder andere aktuelle Daten

Sie spielen das Update ein und dennoch fehlen Skripte für die Strukturanpassung oder zum Beispiel das in der LiesMich-Datei angekündigte neue Zeugnis?

![Fehlermeldung beim Start von MAGELLAN](/assets/images/strukturanpassenfehler1.png)

Drei Möglichkeiten können hinter diesem Problem stecken: 

Nr|Ursache
--|--
1.|dem Server fehlt das Update und damit auch zum Beispiel die  Strukturanpassungsskripte
2.|der Server hat das Update erhalten, aber das Update konnte die Anpassungsskripte nicht ablegen
3.|Sie haben eine Einzelplatzinstallation und haben Ihr Betriebssystem auf Windows 10 aktualisiert

**Zu 1.:**

Bitte immer als erstes den Serverrechner aktualisieren, da dieser Rechner der einzige im Netzwerk ist, der die gemeinsam genutzten Programmkomponenten, wie zum Beispiel die Skripte hat und für die Clientinstallationen zur Verfügung stellt.

**Zu 2.:**

Sollten nach dem Update die Skripte u.a. dennoch nicht aktuell sein, kann es damit zusammenhängen, dass nach der ursprünglichen Serverinstallation die Pfade nachträglich verschoben wurden. Der bei der Installation und bei den Updates verwendete Windows Installer „möchte“ die Dateien am ursprünglichen Speicherort aktualisieren. Sollte dieser nicht mehr bestehen, müsste erneut installiert werden und gleich auf die gewünschten Pfade verwiesen werden.

**zu 3.:**  
Wenn Sie Ihren Rechner mit einer bestehenden MAGELLAN-Installationauf Windows 10 aktualisieren, kann es passieren, dass beim Folgeupdate von Magellan die Datenordner vom Windows Installer nicht gefunden werden und keine neuen Bestandteile wie Skripte, Berichte usw abgelegt werden.
Das betrifft keine Clientinstallationen die auf Datenordner auf dem Serverrechner nutzen, sondern nur Server-/Einzelplatzinstallationen. Bitte deinstallieren Sie Magellan und installieren Sie es neu!

### Meldung "no permission for read/select Access to TABLE..."?

Wenn bei einem Update die Datenstruktur um eine neue Tabelle erweitert wurde, dann muss für die bereits eingerichteten Benutzer geklärt werden, ob sie darauf zugreifen können. Daher ist der letzte Schritt im Updateprozess das Ausführen des Punktes "Zugriffsrechte synchronisieren" im Modul MAGELLAN Administrator.

Bitte rufen Sie den MAGELLAN Administrator auf und führen den Punkt `Datenbankpflege > Datenbank überprüfen > Zugriffsrechte synchronisieren` durch, im Anschluss können die Kollegen sich wieder mit der gewohnten Kennung anmelden.

![Führen Sie diesen Punkt aus, um für neue Bestandteile der Datenbank die Zugriffsrechte für Ihre Benutzer zu vergeben](/assets/images/update.zugriffsrechte.synch.png)

### Meldung "Runtime error ..."

Vermutlich ist eine der Dateien, die beim Start von MAGELLAN geladen werden sollen, beschädigt. Die möglichen Dateien pro Arbeitsplatz wären (außer Sie verwenden eine MAGELLAN.paths um die Dateien gemeinsam zu verwenden):

  *  MAGELLAN.opt (Optionen)
  *  MAGELLAN.evm (Pfade zur Datenbank und zu den gemeinsam verwendeten Datenordnern)
  *  MAGELLAN.lic (Lizenz)

Bitte schauen Sie an dem Rechner je nach Betriebssystem unter folgendem Pfad nach:

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\ProgramData\Stueber Software\Magellan 6 |
| Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6 |
| Windows 2000 | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Software\Magellan 6 |
| Windows 7 | C:\ProgramData\Stueber Software\Magellan 6 |
| Windows Server 2008 | C:\ProgramData\Stueber Software\Magellan 6 |
| Windows 8 | C:\ProgramData\Stueber Software\Magellan 6 |
| Windows 10 | C:\ProgramData\Stueber Software\Magellan 6 |

Bitte benennen Sie der Reihe nach immer eine der Dateien um und starten MAGELLAN, um zu sehen, welche der Dateien das Problem verursacht.
Wenn Sie eine Dateien ausmachen konnten, gehen Sie je nach Datei wie folgt vor:

Datei|nächster Schritt
--|--
MAGELLAN.opt?|Bitte einfach löschen, die Datei wird beim nächsten Schließen von MAGELLAN neu angelegt, anschließend bitte die Optionen unter `Extras > Einstellungen` neu auswählen.
MAGELLAN.evm?|Bitte von einem anderen Clientrechner kopieren und hier einfügen.
MAGELLAN.lic?|Bitte von einem anderen Clientrechner kopieren und hier einfügen.

#### ODBC Meldungen

Wenn bei Ihnen eine der nachstehenden Meldungen bei der Berichtsvorschau gezeigt werden, laden Sie das jeweilige Paket über den Link bei der Meldung herunter, installieren es und führen die Installation/das Update von MAGELLAN bitte erneut aus. 

Bezeichnung|Inhalt
--|--
**Problem**| Die Druckvorschau zeigt die Meldung **"Fehler beim Anlegen der ODBC-Verbindung. ODBC-Fehler(0): Komponente wurde in der Registrierung nicht gefunden"** <br/><br/><img src=/assets/images/update/Fehler04.png>
**Lösung**|[https://download.stueber.de/bin/de/common/fb_driver/Firebird_ODBC_2.0.5.156_Win32.exe](https://download.stueber.de/bin/de/common/fb_driver/Firebird_ODBC_2.0.5.156_Win32.exe)

### Crystal Reports Meldungen

Wir setzen in MAGELLAN für die Druckvorschau und den Druck eine Runtimeversion von Crystal Reports ein. Dieser Teil setzt Programmbibliotheken voraus, die in der Regel beispielsweise mit dem Officepaket schon installiert wurden. Sollte es dennoch hier zu Problemen kommen, kann man gezielt die Voraussetzungen nachinstallieren.
Es kann auch zu Problemen kommen wenn Teile der Runtimeversion nicht korrekt beim Update oder bei der Installation vorn MAGELLAN registriert werden konnten.

Nachstehend zeigen wir eine Reihe von möglichen Meldungen, dazu jeweils einen Link über den Sie Software zur Lösung laden können.

!!! warning "Sehr wichtig!"

    Wenn bei Ihnen eine der nachstehenden Meldungen bei der Installation, beim Update von MAGELLAN oder ggfs. auch in der Berichtsvorschau gezeigt werden, laden Sie das jeweilige Paket über den Link bei der Meldung herunter, installieren es und führen anschließend bitte eine **Reparaturinstallation** von MAGELLAN aus.

Bezeichnung|Inhalt
--|--
**Problem**|**Fehler beim Schreiben in Datei. CrystalDecisions.CrystalReports.Engine.dll**<br/><br/> <img src="/assets/images/installation/03.png"> 
**Lösung**|[https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net462-web-installer](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net462-web-installer)
**Problem**|**Fehler beim Registrieren von Modul ... crtslv.dll**<br/><br/><img src="/assets/images/installation/fehler_cr.png"> 
**Lösung**|[https://download.stueber.de/bin/de/common/vc_redist_2015/vc_redist.x86.exe](https://download.stueber.de/bin/de/common/vc_redist_2015/vc_redist.x86.exe)
**Problem**|**Typeninitialisierer für Crystal.Decisions**<br/><br/><img src="/assets/images/installation/02.png">
**Lösung**|[https://download.stueber.de/bin/de/common/cr_runtime/CR13SP30MSI32_0-10010309.MSI](https://download.stueber.de/bin/de/common/cr_runtime/CR13SP30MSI32_0-10010309.MSI)
**Problem**|**Fehler beim Registrieren von Modul C:\Program Files (x86)\SAP BusinessObjects\MapWinGIS\win32_x86\MapWinGIS.ocx. HRESULT -2147024770. Wenden Sie sich an den Support.** <br/><br/><img src=/assets/images/update/Fehler03.png>
**Lösung**|[https://download.stueber.de/bin/de/common/cr_runtime/CR13SP30MSI32_0-10010309.MSI](https://download.stueber.de/bin/de/common/cr_runtime/CR13SP30MSI32_0-10010309.MSI)
**Problem**| Die Druckvorschau zeigt die Meldung **"Fehler beim Anlegen der ODBC-Verbindung. ODBC-Fehler(0): Komponente wurde in der Registrierung nicht gefunden"** <br/><br/><img src=/assets/images/update/Fehler04.png>
**Lösung**|[https://download.stueber.de/bin/de/common/fb_driver/Firebird_ODBC_2.0.5.156_Win32.exe](https://download.stueber.de/bin/de/common/fb_driver/Firebird_ODBC_2.0.5.156_Win32.exe)
