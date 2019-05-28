# ODBC-Anbindung unter 64 bit Betriebssystemen

1. Deinstallieren Sie auf diesem Rechner bitte Ihre Firebird-Version und auch Magellan.
2. Löschen Sie anschließend den Verzeichnissen System, System32 und auch SysWOW64  die eventuell noch vorhandenen Dateien: -  ODBCJDBC.dll  und- ODBCJDBCinst.dll
3. Installieren Sie anschließend den von uns zur Verfügung gestellten Firebirdtreiber  mit den Standardvorgaben plus dem Häkchen, wie im nachstehenden Screenshot:


 ![Wählen Sie bitte diese Option mit aus!](images/import3.png)

4. Installieren Sie [MAGELLAN](http://magellan.stueber.de/download.php) erneut.
5. Prüfen Sie anschließend im Verzeichnis SysWOW64, ob die Dateien ODBCJDBC.dll und ODBCJDBCinst.dll vorhanden sind. Falls nicht, kopieren Sie sie aus dem Verzeichnis System32 dorthin. 
6. Öffnen Sie nun das das Verzeichnis SysWOW64 und starten die Anwendung ODBCAD32.exe. Bitte richten Sie hier die ODBC-Anbindung analog dem nachstehenden Screenshot ein(der Datenbankpfad wird sicher abweichen):

 ![Einstellungen für das Firebird ODBC Setup](images/import4.png)
