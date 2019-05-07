# Update von Firebird 2.5.1/2.5.2 auf 2.5.5

1. Bitte gehen Sie wie folgt vor:
Laden Sie die aktuelle Version von Firebird herunter: [Download Firebird 2.5.5](ftp://ftp.stueber.de/pub/bin/de/magellan/v6/Firebird-2.5.5.26952_0_Win32.exe)
2. Stoppen Sie den laufenden Firebirdserver unter `Start > Systemsteuerung > Verwaltung > Dienste > Firebird-Server > Rechtsklick > Beenden`.

![Firebird-Server-Dienst stoppen](/assets/images/firebird_stop.jpg)
 3. Starten Sie die Installation per Doppelklick auf das Installationspaket. Folgen Sie dem Installationsassistenten.
 4. Starten Sie den Firebirdserver unter `Start > Systemsteuerung > Verwaltung > Dienste > Firebird-Server > Rechtsklick > Neu starten`.
 5. Melden Sie sich als sysdba am Magellan-Administrator an und erstellen unter `Datenbanksicherung > Sicherungskopie erstellen` eine Sicherung der Datenbank. Der Speicherort der Sicherung muss sich auf dem Rechner befinden, auf dem sich Ihre Magellan-Datenbank befindet. Wir empfehlen die Sicherung im Verzeichnis Datenbank > Backup zu erstellen und als Dateinamen das Tagesdatum zu verwenden.

![Datenbank sichern](/assets/images/db_sichern.jpg)

6. Stellen Sie anschließend aus der Sicherung eine neue Datenbank wiederher, verwenden Sie dafür den Punkt `Datenbanksicherung > Sicherungskopie wiederherstellen`. Sie können mit der neuen Datenbank nicht Ihre aktuelle Datenbank überschreiben, verwenden Sie bitte einen neuen Datennamen.

![](/assets/images/db_neu.jpg)

7. Als letzten Schritt tauschen Sie bitte die aktuelle Datenbank gegen die mit der aktuellen Firebirdversion wiederhergestellte Datenbank aus. Stoppen Sie den laufenden Firebirdserver unter `Start > Systemsteuerung > Verwaltung > Dienste > Firebird-Server > Rechtsklick > Beenden`. Benennen Sie die aktuelle Datenbank um (z.B. in alt_Magellan6.fdb) und geben der wiederhergestellten Datenbank den bisherigen Datenbanknamen.Starten Sie den Firebirdserver unter `Start > Systemsteuerung > Verwaltung > Dienste > Firebird-Server > Rechtsklick > Neu starten`. Anschließend starten Sie Magellan und folgen bitte dem Assistenten zur Datenstrukturanpassung.  
