# MAGELLAN und Linux

MAGELLAN selbst wird nicht auf dem Linuxsystem betrieben, sondern ist ausschließlich auf Windows Betriebssysteme abgestimmt. 
Aber: Der Firebird-Datenbankserver und die Datenbank können unter Linux eingesetzt werden. 

Der Betrieb mit einem unter Linux laufenden Firebird-Datenbankserver unterscheidet sich in der praktischen Handhabung durch den Nutzer kaum vom Betrieb mit einem unter Windows laufenden Firebird-Server.  

> ####### warning::Wichtig!
>
> Allerdings besteht der Unterschied, dass der von unserer Seite übliche umfassende Einzel-Anwendersupport nur für die Windows-Version von Firebird besteht. Wo MAGELLAN mit einem unter Linux laufenden Datenbankserver genutzt wird, wie dies z. B. in Bremen der Fall ist, wird die Server-Umgebung den Schulen in Regel vorkonfiguriert zur Verfügung gestellt. 


Abgesehen von diesen grundsätzlichen Vorgaben unterstützen wir Sie in einem weniger umfassenden Rahmen natürlich trotzdem gern, wenn Sie an Ihrer Schule eigenverantwortlich MAGELLAN mit einer Linux-Version von Firebird einsetzen wollen. Die Einrichtung von MAGELLAN mit einem unter Linux laufenden Firebird unterscheidet sich nur wenig von der Einrichtung unter Windows. 

Sie können für die Einrichtung des MAGELLAN-Clients hierzu gern auf unsere [Installationsanleitung](https://doc.magellan7.stueber.de/schulverwaltung/installation/) zurückgreifen.


Bei der Einrichtung der neuen Serververbindung zu Ihrem Linux-Server im MAGELLAN Administrator sollten Sie abweichend von der obigen Anleitung darauf achten, dass der Dateipfad auf dem Server entsprechend der auf dem Linux-System geltenden Vorgaben für Verzeichnispfade eingetragen werden muss. Den genauen Dateipfad können Sie der Konfiguration von Firebird entnehmen.
 
Unter Windows würde der Pfad im MAGELLAN-Administrator zum Beispiel so aussehen(Server-Verwaltung > Verbindungen verwalten > Starten > Verbindung markieren > Bearbeiten > Karte Datenbank):



```
 C:\ProgramData\Documents\Stueber Software\MAGELLAN 7\Datenbank\MAGELLAN7.fdb
```



 So z.B. an der gleichen Stelle für Linux: 


```
/var/lib/firebird/2.5/data/mag6-linux.fdb
```



Daneben sind bei der Verwendung einer existierenden MAGELLAN-Datenbank, die zuvor mit einer Windows-Version von Firebird betrieben wurde, sowie unserer Beispieldatenbank bei der Übertragung auf ein Linux-System noch zwei weitere Besonderheiten zu berücksichtigen: Erstens unterscheidet sich die Zuweisung von entsprechenden Benutzer- und Zugriffsrechten auf die Datenbank-Datei vom Konzept zwischen Windows und Linux. Unter Linux läuft der Firebird-Server in der Regel im Kontext eines eigenen Benutzers, so dass diesem Zugriffsrechte auf die Datenbank-Datei eingeräumt werden müssen, z. B. (je nach System-Konfiguration) firebird:
firebird, rw-, rw-, --- 

Zweitens kann sich die sog. „on-disk strukture“ der Datenbank-Datei zwischen verschiedenen Versionen des Firebird-Servers unterscheiden. In diesem Fall kann beim Kopieren einen Anpassung durch Sichern der Ursprungsdatei und Wiederherstellen auf dem Linux-System mit Hilfe des Firebird zugehörigen Backup-Programms „gbak“ notwendig sein. Zum Übertragen einer Windows-MAGELLAN-Datenbank können also folgende zusätzliche Schritte nötig sein: Übertragen einer Datenbank 

1. Sichern der MAGELLAN-Beispieldatenbank in einer anderen lauffähigen MAGELLAN-Installation über den MAGELLAN-Administrator
2. Wiederherstellen des so erstellten Beispieldatenbank-Backups um die On-Disk-Structure an Linux anzupassen. (#gbak -c Dateinamebackup.fbk Dateinamedatenbank.fdb -USER 'sysdba' -PAS 'masterkey') 
3. Ggf. Kopieren der wiederhergestellten Datenbank in das Standardverzeichnis von Firebird (/var/lib/firebird/2.5/data) und überprüfen der Gruppenzugehörigkeit und Benutzerrechte (z. B. firebird:firebird, rw-, rw-, ---) 
