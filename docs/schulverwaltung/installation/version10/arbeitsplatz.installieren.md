# Arbeitsplatzinstallation

Die Einrichtung eines Arbeitsplatzes unterscheidet sich von der Einrichtung des Serverrechners, da hier nur MAGELLAN und die Runtimeversion von Crystal Reports als Programme installiert werden, die gemeinschaftlich verwendeten Bestandteile wie die Datenbank oder Berichte, Skripte usw. sind bereits auf dem Server vorhanden, es wird in einem späteren Schritt dann darauf verwiesen.

## Vorbereitung

### Downloads

Für den Serverrechner benötigen Sie die Installationsdateien für:

* die Runtimeversion von Crystal Reports 32- oder 64-Bit
* für MAGELLAN 32- oder 64-Bit

!!! danger "Wichtig!"

    Für MAGELLAN 10 wird eine aktuellere Crystal Reports Runtime verwendet.

**Nutzen Sie ein 32-Bit oder 64-Bit-Betriebssystem?**

1. Wählen Sie `Start > Einstellungen > System > Info` aus.
2. Unter `Gerätespezifikationen > Systemtyp` sehen Sie, ob Sie eine 32-Bit-Version oder eine 64-Bit-Version von Windows verwenden.

!!! danger "Wichtig!"

    Alle Installationspakete finden Sie [in unserem Downloadbereich](https://magellan.stueber.de/download.php).<br/>**Für Windows 32-Bit und 64-Bit gibt es gesonderte Installationsdateien für MAGELLAN und für die Runtimeversion von Crystal Reports.**

### Lizenzdaten

Legen Sie sich bitte die Lizenzdatei (*.lic) so zurecht, dass Sie vom Server darauf zugreifen können. 
Die Datei wurde Ihnen als Test- oder Volllizenz von unserem Office-Team per Mail zugesandt. Sollte Ihnen die Lizenzdatei noch fehlen, können Sie sie per Mail an office@stueber.de neu anfragen. Für eine Volllizenz bitten wir um die Angabe der Kundennummer, herzlichen Dank!

## Installation der Crystal Reports Runtimeversion

Diese Installation muss stets parallel zur MAGELLAN Installation erfolgen, diese Bestandteile sind die Voraussetzung für die Druckfunktionalitäten in MAGELLAN.

Starten Sie die Installation per Doppelklick auf das msi-Paket. Klicken Sie bitte auf `Next` im Installationsassistenten.

![Willkommen](/assets/images/installation/10/cr/004.png)

Stimmen Sie bitte dem "License Agreement" zu, indem Sie den oberen Radiobutton wie in der Abbildung aktivieren und auf `Next` klicken

![License Agreement](/assets/images/installation/10/cr/005.png)

Starten Sie die Installation per Klick auf `Next`.

![Start](/assets/images/installation/10/cr/006.png)

Der Fortschritt der Installation wird per Laufbalken gezeigt.

![Installationsfortschritt](/assets/images/installation/10/cr/007.png)

Die Installation ist beendet, bitte klicken Sie auf `Finish`.

![Fertigstellen](/assets/images/installation/10/cr/008.png)

## Installation von MAGELLAN

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan9.msi`.

Der Setup Assistent von MAGELLAN 10 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/installation/10/001.png)

Wählen Sie die `Arbeitsplatzinstallation` aus!<br/>Es wird nur das Programm installiert, es werden keine Datenbank abgelegt oder Datenordner (für Berichte, Skripte usw.) erzeugt.

![Installationart festlegen](/assets/images/installation/10/001.1.png)

Der Assistent schlägt Ihnen einen Installationspfad vor, wir empfehlen diese Auswahl mit `Weiter` zu übernehmen. Der in der Abbildung gezeigte Pfad entspricht der Installation auf einem Gerät mit 64-Bit Betriebssystem, der Pfad für ein 32-Bit Betriebssystem weicht davon ab.

![Installationart festlegen](/assets/images/installation/10/001.2.png)

Wählen Sie den Speicherort für die Datenbank und klicken Sie auf „Weiter“.

![Speicherort für die Datenbank](/assets/images/installation/10/001.3.png)

Wählen Sie den Speicherort für die Datenordner (Berichte, Dokumente, Improte, Skripte und Vorlagen) und klicken Sie auf „Weiter“.

![Speicherort für die Datenordner](/assets/images/installation/10/001.4.png)

Die Voreinstellungen sind abgeschlossen, bitte starten Sie die Installation mit `Fertigstellen`!

![Vorbereitungen abgeschlossen](/assets/images/installation/10/002.png)

![Installation läuft](/assets/images/installation/10/003.png)

Die Installation ist abgeschlossen, klicken Sie bitte auf `Fertigstellen`!

![Fertig!](/assets/images/installation/10/003.png)

## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie MAGELLAN 10 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/installation/10/w/001.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["MAGELLAN - Erste Schritte"](https://doc.kb.stueber.de/magellan/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/installation/10/w/002.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/installation/10/w/003.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/installation/10/w/004.png)

Wählen Sie bitte `Entfernte Datenbank` aus.
![Lokale Datenbank](/assets/images/installation/10/w/005.4.png)

Bei einer Arbeitsplatzinstallation wird im Feld `Wie heißt der Datenbankserver?` die IP oder der Name des Datenbankservers erwartet. Tragen Sie diese Daten bitte ohne Backslashes ein. Für den Pfad zur Datenbank wird der lokale Pfad (kein Netzlaufwerk, kein Netzwerkpfad) auf Ihrem Serverrechner zur Datenbank erwartet.
Sind die Eingaben für den Datenbankserver und den Pfad zur Datenbank korrekt, wird der Pfad schwarz dargestellt, ist der Pfad inkorrekt, wird der Pfad rot (siehe Abbildung) dargestellt.

![Datenbankpfad](/assets/images/installation/10/w/006.1.png)

Bitte vergeben Sie hier den Pfad (Netzwerkpfade und Netzlaufwerke möglich) zu den Datenordnern. Den Wurzelpfad können Sie in oberste Zeile eingeben und per Klick auf das Dreieck in die weiteren Zeilen übertragen lassen, der Pfad wird jeweils um den Verzeichnisnamen ergänzt. Ist der Pfad korrekt, wird der schwarz dargestellt, kann der Pfad nicht erreicht werden, wird er rot dargestellt.

![Datenordnerpfad](/assets/images/installation/10/w/006.3.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul MAGELLAN ADMINISTRATOR auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. Standardmäßig wird als Speicherort `Datenbanken > Datensicherungen > Backup bzw. Restore` vorgegeben, wir empfehlen diese Auswahl zu übernehmen.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/10/w/007.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](/assets/images/installation/10/w/008.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. 
Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort Ihr Passwort ein, dass Sie während der Firebird-Installation gewählt haben. Die Einrichtung Ihres Servers oder Ihres Arbeitsplatzes ist fertig!

![Abschluss des Willkommens-Assistenten](/assets/images/installation/10/w/009.png)
