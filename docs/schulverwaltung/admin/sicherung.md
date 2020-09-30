# Datensicherung

Über den Punkt `Datenbankverbindungen` kommen Sie zu den Datensicherungsmöglichkeiten in MAGELLAN. In dieser Funktion wird das Sicherungstool der Firebird-Datenbank ausgeführt. Sie können mit diesem Tool Sicherungskopien der Schulverwaltungsdatenbank (MAGELLAN.fdb) erstellen und aus Sicherungsdateien (*.fbk) eine neue Datenbank wiederherstellen.

!!! info "Hinweis"

	Eine Sicherung/Wiederherstellung der Datenbank kann ausschließlich auf dem Rechner angelegt werden, auf dem auch die Datenbank selbst gespeichert ist und der Firebird-Server läuft. Sie können zwar die Aktionen zum Sichern oder Wiederherstellen (Sie müssen den Dateinamen der Sicherung und den Speicherort kennen) selbst von einem Clientrechner starten, die Sicherung/Wiederherstellung kann aber nur auf dem Rechner angelegt werden, auf dem auch die Datenbank selbst gespeichert ist und der Firebird-Server läuft, wenn Sie Zugriff auf diesen Ornder haben ansonsten werden diese auf Ihrem Serverrechner abgelegt.

![Schaltflächen zum Erstellen eines Backups oder dem Wiederherstellen einer Sicherung](/assets/images/magellan.administrator/datensicherung.png)

!!! warning "Wichtig"

	Wir empfehlen eine tägliche Sicherung Ihrer Datenbank! Bitte verwenden Sie dazu den entsprechenden Punkt im MAGELLAN-ADMINISTRATOR oder den unten beschriebenen Weg per Windows Taskplaner. Diese von Firebird mit angebotene Funktion kann auch erfolgen, während der Firebird-Dienst läuft und MAGELLAN verwendet wird. Es werden die Daten Ihrer MAGELLAN.fdb in eine neue Datei mit der Endung *.fbk geschrieben, hieraus kann eine neue Datenbank aufgebaut werden. Anders als bei einer Sicherung per Kopie der Datenbank (die nie bei laufendem Firebird-Dienst erfolgen darf!) erhalten Sie Rückmeldungen zur Qualität der gesicherten Daten.
	Sie sollten in Abständen, zum Beispiel vierteljährlich, mit einer wiederhergestellten Datenbank weiterarbeiten. Dazu stoppen Sie den Firebird-Server-Manager in der Systemsteuerung Ihres Serverrechners, tauschen die Datenbanken (z.B. C:\Users\Public\Documents\Stueber Software\MAGELLAN 7\Datenbank) aus und starten den Firebird-Server-Manager erneut.
	
	Das Herstellen einer Sicherungskopie und anschließende Wiederherstellen dieser Sicherungskopie hat eine reparierende und zugleich komprimierende Funktion. Die wiederhergestellte Sicherungskopie ist meist kleiner als die Ausgangsdatenbank, da "Lücken" in der Datenbank beseitigt werden und so die Datenmenge „abgespeckt“ wird.

## Sicherungskopie erstellen

Der nachstehend beschriebene Assistent kann eine Sicherung Ihrer Datenbank erstellen.

![Sicherung einer Datenbank](/assets/images/magellan.administrator/backup.png)

Wir beschreiben in der nachstehenden Tabelle die Eingabeoptionen:

Gruppe|Feld|Bedeutung
---|---|---
Verbindung|Welche Verbindung soll gesichert werden?|Es wird Ihnen eine Liste Ihrer unter Server-Verwaltung angelegten Datenbankanbindungen gezeigt. Mit der Auswahl der Verbindung, wählen Sie auch die der Verbindung zugeordnete Datenbank aus, die Felder unter dem Punkt "Datenbank" werden automatisch aus den Verbindungsinformationen gefüllt.
Datenbank|Protokoll|wird aus den Einstellungen der unter Server-Verwaltung angelegten und im Schritt zuvor ausgewählten Verbindung befüllt
Datenbank|Server|wird aus den Einstellungen der unter Server-Verwaltung angelegten und im Schritt zuvor ausgewählten Verbindung befüllt
Datenbank|Datei|wird aus den Einstellungen der unter Server-Verwaltung angelegten und im Schritt zuvor ausgewählten Verbindung befüllt
Sicherung|Sicherung|Hier wird der in der Verbindung unter der Unterkarte `Sicherung` erfasst Pfad vorbelegt. <br/>Sollten Sie die Verbindungsdaten nicht entsprechend befüllt haben:<br/>Tragen Sie hier bitte einen lokalen Pfad auf Ihrem MAGELLAN-Server ein, damit dort die Sicherungskopie erzeugt werden kann. Wir empfehlen die Sicherung in das Backupverzeichnis im Datenbankordner abzulegen. <br/>Der Pfad könnte dafür wie folgt aussehen:<br/>`C:\Users\Public\Documents\Stueber Systems\Magellan 6\Datenbank\Datensicherung\Backup`<br/><br/>Der Name der Sicherung wird vom Programm ergänzt und beinhaltet: <br/>`[Datum, Uhrzeit]Verbindungsname - Benutzer.fbk` oder <br/> Beispiel: <br/>[2019-07-25, 10-32-21] Magellan - sysdba.fbk<br/><br/>Wenn Sie das Modul MAGELLAN ADMINISTRATOR auf dem MAGELLAN-Server aufrufen, steht Ihnen die Schaltfläche zur Auswahl per Datenexplorer zur Verfügung.
Sicherung|Wiederherstellung|Hier wird der in der Verbindung unter der Unterkarte `Sicherung` erfasst Pfad vorbelegt. <br/>Sollten Sie die Verbindungsdaten nicht entsprechend befüllt haben:<br/>Tragen Sie hier bitte einen lokalen Pfad auf Ihrem MAGELLAN-Server ein, damit dort die Sicherungskopie erzeugt werden kann. Wir empfehlen die Sicherung in das Backupverzeichnis im Datenbankordner abzulegen. <br/>Der Pfad könnte dafür wie folgt aussehen:<br/>`C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank\Datensicherung\Restore`<br/><br/>Der Name der Sicherung wird vom Programm ergänzt und beinhaltet: <br/>` [Datum, Uhrzeit]Verbindungsname - Benutzer.fdb` oder <br/> Beispiel: <br/>[2019-07-25, 10-32-21] Magellan - sysdba.fdb<br/><br/>Wenn Sie das Modul MAGELLAN ADMINISTRATOR auf dem MAGELLAN-Server aufrufen, steht Ihnen die Schaltfläche zur Auswahl per Datenexplorer zur Verfügung.
Anmeldung|Benutzer|Tragen Sie bitte die sysdba-Kennung ein!
Anmeldung|Kennwort|Tragen Sie bitte Ihr sysdba-Passwort ein!
Ergebnis|Ergebnis|In diesem Feld erhalten Sie eine Rückmeldung über gewählte Aktion!

## Sicherungskopie wiederherstellen

Der nachstehend beschriebene Assistent kann aus einer Sicherung Ihrer Datenbank eine neue Datenbankdatei aufbauen.

![Sicherung einer Datenbank](/assets/images/magellan.administrator/restore.png)

Wir beschreiben in der nachstehenden Tabelle die Eingabeoptionen:

Gruppe|Feld|Bedeutung
---|---|---
Verbindung|Verbindung|Um eine Sicherung wiederherstellen zu können, muss eine Firebird-Server zur Verfügung stehen. Diesen wählen Sie indirekt mit der Verbindung aus. Welche Sicherung wirklich wiederhergestellt werden soll, legen Sie im Bereich Sicherung fest.<br/> Mit der Auswahl der Verbindung, wählen Sie auch die der Verbindung zugeordnete Datenbank aus, die folgenden Felder werden automatisch aus den Verbindungsinformationen gefüllt.
Datenbank|Protokoll|wird aus den Einstellungen der unter Server-Verwaltung angelegten und im Schritt zuvor ausgewählten Verbindung befüllt
Datenbank|Server|wird aus den Einstellungen der unter Server-Verwaltung angelegten und im Schritt zuvor ausgewählten Verbindung befüllt
Datenbank|Datei|wird aus den Einstellungen der unter Server-Verwaltung angelegten und im Schritt zuvor ausgewählten Verbindung befüllt
Sicherung|Sicherung|Der Pfad zum Backupverzeichnis wird auch Ihren Eintragungen für die Verbindung gelesen. <br/><br/>**Auf dem Serverrechner:**<br/>Klicken Sie bitte auf die Schaltfläche am Ende der Zeile und verweisen auf die konkrete Sicherungsdatei!<br/>Beispiel: `C:\Users\Public\Documents\Stueber Systems\Magellan 6\Datenbank\Datensicherung\Backup\[2019-07-25, 10-32-21] Magellan - sysdba.fbk`<br/><br/>**Vom Client aus:**<br/>Ergänzen Sie den Pfad zum Backup-Verzeichnis um den Dateinamen der Sicherung.
Sicherung|Wiederherstellung|Der Pfad zum Restore-Ordner wird aus den Einstellungen der Verbindung gelesen, der neue Datenbankname wird aus dem Namen der Sicherung vom Programm selbst generiert.
Anmeldung|Benutzer|Tragen Sie bitte die sysdba-Kennung ein!
Anmeldung|Kennwort|Tragen Sie bitte Ihr sysdba-Passwort ein!
Ergebnis|Ergebnis|In diesem Feld erhalten Sie eine Rückmeldung über gewählte Aktion!

!!! info "Hinweis"

	Wenn Sie von einem Client aus die Sicherung der Datenbank auf dem Server durchführen, haben Sie nicht die Möglichkeit (Schaltfläche mit den drei Punkten am Ende der Zeile) den Pfad auszusuchen. Sie können lediglich manuell den entsprechenden Pfad eintragen. Erwartet wird immer lokaler Pfad auf dem Rechner, auf dem auch der Firebirdserver läuft. Sie können keine Sicherung auf einen anderen Rechner in Ihrem Netzwerk erstellen lassen.Eine Sicherungskopie kann im laufenden Betrieb von MAGELLAN durchgeführt werden. Von der Sicherungskopie sind alle Dokumente, Word-Vorlagen und Berichte ausgenommen.

!!! danger "Achtung"

	Achten Sie bitte darauf, dass die Verzeichnisse, die in den Pfaden angegebnen werden auch existieren. Legen Sie ggfs. bitte `Datenbank > **Datensicherung** > **Backup**` und `Datenbank > **Datensicherung** > **Restore**` an.

## Einbinden der Sicherung in den Windows Taskplaner

Sie können eine Datensicherung auch außerhalb des MAGELLAN-ADMINISTRATORs nur mit den Möglichkeiten von Firebird erstellen. mit in den Taskplaner des Serverrechners einbinden. Damit Sie sicherstellen können, dass diese Aktion automatisch einmal täglich ausgeführt wird, können Sie die Aktion in den Windows Taskplaner einbinden. Der nachfolgende Abschnitt basiert auf der Firebird-Dokumentation.

Erstellen Sie mit dem Texteditor eine neue Datei und kopieren den nachfolgenden Text hinein.

!!! info "Hinweis"

	Bitte beachten Sie, dass die Pfade bei Ihrer Installation abweichen können!

`"C:\Program Files (x86)\Firebird\Firebird_2_5\bin\gbak.exe" -v -t -user SYSDBA -password masterkey -y "C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank\Backup\MAGELLAN6_%date:~0%.log" "C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank\MAGELLAN6.FDB" "C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank\Backup\MAGELLAN6_%date:~0%.FBK" pause`

Speichern Sie diesen Text und passen die drei Pfade den Gegebenheiten auf Ihrem Serverrechner an. Wir beschreiben nachstehend die Bedeutung der einzelnen Punkte:

Hinweis | Bedeutung
---------- | -------------
Pfad zur gbak.exe | Der erste Pfad führt zur gbak.exe, die die Datensicherung Ihrer Magellan7.fdb erstellt. Der von uns angebebene Pfad entspricht dem Standardinstallationspfad, könnte bei Ihnen aber abweichen.
-user und -password | Anschließend ist die Administratorenanmeldung an Ihrer Datenbank in der Datei enthalten, wenn Sie ein anderes Passwort verwenden, tragen Sie dieses anstelle von „masterkey“ein.
-y und Pfad|Dieser optionale Pfad legt Ihnen pro Sicherung eine Logdatei mit dem Tagesdatum mit den Meldungen an.
Pfad und Dateiname der *.fdb |Der nachfolgende Pfad verweist auf Ihre Datenbank. Liegt Ihre Datenbank an anderer Stelle, passen Sie diesen Pfad bitte an.
Ablagepfad der Sicherungskopie|Als letzte Information wird der Ablagepfad für die Sicherungskopie mit angegeben. Sie könnten sich einen gesonderten Unterordner "Backup" erstellen, müssten auf diesen dann im Pfad verweisen.
Pfad und Dateiname der *.fbk | Der Dateiname wird automatisch mit Magellan7_aktuelles Datum.fbk angegeben. Durch das Datum im Namen wird sichergestellt, dass die Sicherungskopie des Vortages nicht täglich überschrieben wird.
pause | Programmfenster im Vordergrund oder unsichtbar: Wenn Sie "pause" weglassen, dann läuft die Sicherung im Hintergrund ab, mit pause können Sie den Fortschritt im Vordergrund verfolgen. Wenn Sie eine Logdatei erstellen lassen, können Sie auf diesen Parameter verzichten.

Wenn alle Angaben angepasst sind, speichern Sie die Datei und benennen sie anschließend in "MagellanBackup.bat"um. Legen Sie diese Datei bitte auf Ihrem Server im Datenbankordner ab.

!!! info "Hinweis"

	Führen Sie die Datei zum Test bitte per `Doppelklick` oder `Rechtsklick > Ausführen` aus.

Hat es funktioniert? Dann richten Sie im Taskplaner bitte einen neuen Task ein, der täglich zu einer bestimmten Zeit diese Datei ausführt. Gehen Sie dazu auf dem Server unter `Start > Programme > Zubehör > Systemprogramme > Geplante Tasks`.