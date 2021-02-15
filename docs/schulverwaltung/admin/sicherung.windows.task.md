# Sicherung per Windows Task

!!! danger "Achtung"

	Die nachstehenden Hinweise beschreiben keine unserer MAGELLAN-Funktionalitäten, sondern zusätzliche Möglichkeiten, die direkt auf ein Firebird-Tool aufsetzen.

Sie können die Aktion "Datenbanksicherungskopie erstellen" mit in den Taskplaner des Serverrechners einbinden. Damit könnten Sie sicherstellen, dass diese Aktion automatisch einmal täglich ausgeführt wird. Gehen Sie dafür bitte folgendermaßen vor:

Erstellen Sie mit dem Texteditor eine neue Datei und kopieren den nachfolgenden Text hinein.

!!! info "Hinweis"

	Bitte beachten Sie, dass die Pfade bei Ihrer Installation abweichen können!

```
@echo off

:: Parameters to be entered by the user

:: Path to gbak.exe
set gbakcmd="C:\Firebird\bin\gbak.exe"

:: Path to log file (includes date)
set log="C:\Users\Benutzer.STUEBER\Documents\Stueber Systems\Magellan 7\Datenbank\MAGELLAN_%date:~0%.log" 

:: Path to source database file (FDB)
set source="C:\Users\Benutzer.STUEBER\Documents\Stueber Systems\Magellan 7\Datenbank\MAGELLAN7.FDB"

:: Path to destination backup file (FBK)
set dest="C:\Users\Benutzer.STUEBER\Documents\Stueber Systems\Magellan 7\Datenbank\Magellan.fbk" 

:: User credentials to Authenticate/authorize (masterkey is the default, please change to your password)
set username="SYSDBA"
set password="masterkey"

:: DO NOT CHANGE THESE LINES
echo %gbakcmd% -v -t -user %username% -password %password% -y %log% %source% %dest%
%gbakcmd% -v -t -user sysdba -password masterkey -y %log% %source% %dest%

pause

@echo on
```

Speichern Sie diesen Text und passen die drei Pfade den Gegebenheiten auf Ihrem Serverrechner an. Wir beschreiben nachstehend die Bedeutung der einzelnen Punkte:

Hinweis    | Bedeutung
---------- | -------------
Pfad zur gbak.exe | Der erste Pfad führt zur gbak.exe, die die Datensicherung Ihrer Magellan6.fdb erstellt. Der von uns angebebene Pfad entspricht dem Standardinstallationspfad, könnte bei Ihnen aber abweichen.
 -user und -password | Anschließend ist die Administratorenanmeldung an Ihrer Datenbank in der Datei enthalten, wenn Sie ein anderes Passwort verwenden, tragen Sie dieses anstelle von „masterkey“ein. 
 -y und Pfad|Dieser optionale Pfad legt Ihnen pro Sicherung eine Logdatei mit dem Tagesdatum mit den Meldungen an. 
 Pfad und Dateiname der *.fdb |Der nachfolgende Pfad verweist auf Ihre Datenbank. Liegt Ihre Datenbank an anderer Stelle, passen Sie diesen Pfad bitte an.  
Ablagepfad der Sicherungskopie|Als letzte Information wird der Ablagepfad für die Sicherungskopie mit angegeben. Sie könnten sich einen gesonderten Unterordner "Backup" erstellen, müssten auf diesen dann im Pfad verweisen.
Pfad und Dateiname der *.fbk | Der Dateiname wird automatisch mit Magellan6_aktuelles Datum.fbk angegeben. Durch das Datum im Namen wird sichergestellt, dass die Sicherungskopie des Vortages nicht täglich überschrieben wird.
pause | Programmfenster im Vordergrund oder unsichtbar: Wenn Sie "pause" weglassen, dann läuft die Sicherung im Hintergrund ab, mit pause können Sie den Fortschritt im Vordergrund verfolgen. Wenn Sie eine Logdatei erstellen lassen, können Sie auf diesen Parameter verzichten.

Wenn alle Angaben angepasst sind, speichern Sie die Datei und benennen sie anschließend in "MagellanBackup.bat"um. Legen Sie diese Datei bitte auf Ihrem Server im Datenbankordner ab.

!!! info "Hinweis"

	Führen Sie die Datei zum Test bitte per `Doppelklick` oder `Rechtsklick > Ausführen` aus.

Hat es funktioniert? Dann richten Sie im Taskplaner bitte einen neuen Task ein, der täglich zu einer bestimmten Zeit diese Datei ausführt. Gehen Sie dazu auf dem Server unter `Start > Programme > Zubehör > Systemprogramme > Geplante Tasks`.
