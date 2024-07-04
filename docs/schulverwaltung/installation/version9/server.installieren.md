
# Den Server oder einen Einzelplatz einrichten

In diesem Abschnitt wird beschrieben, wie ein Platz eingerichtet wird, auf dem lokal die Datenbank gespeichert wird. 
In der Regel sollte das der Schulserver sein oder ein Arbeitsplatz, von dem aus nicht auf den Server zugeriffen werden kann, beispielsweise ein Testrechner.

!!! danger "Achtung"

    Wenn Sie bereits Magellan 8 einsetzen, lesen Sie bitte statt auch den Abschnitt [Umstieg von Magellan 8 auf Magellan 9](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-8-auf-9/)!

## Vorbereitung

### Downloads

Für den Serverrechner benötigen Sie die Installationsdateien für:

* Firebird
* die Runtimeversion von Crystal Reports 32- oder 64-Bit
* für Magellan 32- oder 64-Bit

**Nutzen Sie ein 32-Bit oder 64-Bit-Betriebssystem?**

1. Wählen Sie `Start > Einstellungen > System > Info` aus.
2. Unter `Gerätespezifikationen > Systemtyp` sehen Sie, ob Sie eine 32-Bit-Version oder eine 64-Bit-Version von Windows verwenden.

!!! danger "Wichtig!"    

    Alle Installationspakete finden Sie [in unserem Downloadbereich](https://magellan.stueber.de/download.php).<br/>**Für Windows 32-Bit und 64-Bit gibt es gesonderte Installationsdateien für Magellan und für die Runtimeversion von Crystal Reports.**<br/>**Das Installationspaket für Firebird ist für beide Ausgaben gleich.**

### Lizenzdaten

Legen Sie sich bitte die Lizenzdatei (*.lic) so zurecht, dass Sie vom Server darauf zugreifen können. 
Die Datei wurde Ihnen als Test- oder Volllizenz von unserem Office-Team per Mail zugesandt. Sollte Ihnen die Lizenzdatei noch fehlen, können Sie sie per Mail an office@stueber.de neu anfragen. Für eine Volllizenz bitten wir um die Angabe der Kundennummer, herzlichen Dank!

## Installation von Firebird 2.5

!!! warning "Wichtig"

	Diese Installation wird einmalig im Netzwerk auf dem Rechner, auf dem später Ihre Magellan-Datenbank liegen wird ausgeführt. 

Laden Sie bitte das Firebird-Installationspaket von unseren Webseiten oder unter [folgendem Link](https://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei `Firebird-2.5......Win32.exe`. Bitte übernehmen Sie im daraufhin startenden Installationsassistenten auf der Karte „Komponenten auswählen“ die voreingestellten Optionen.

![Komponenten auswählen](/assets/images/fb-components.png)

Auf der Karte „Zusätzliche Aufgaben auswählen“ übernehmen Sie bitte die Optionen und aktivieren zusätzlich das Häkchen „Die Firebird Client-Bibliothek ins Systemverzeichnis kopieren“.

![Zusätzliche Aufgaben auswählen](/assets/images/fb-tasks.png)

!!! warning "Wichtig"

	Firebird wird nur dem Rechner installiert werden, auf dem zukünftig die Datenbank gespeichert wird. Das kann Ihr Server sein oder auch ein netzwerkunabhängiger Rechner. 
	
	Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme \(Eingehende und Ausgehende Regel\) für diesen Port ein und versuchen es bitte erneut.

## Installation der Crystal Reports Runtimeversion

Diese Installation muss stets parallel zur Magellan Installation erfolgen, diese Bestandteile sind die Voraussetzung für die Druckfunktionalitäten in Magellan.

Starten Sie die Installation per Doppelklick auf das msi-Paket. Klicken Sie bitte auf `Next` im Installationsassistenten.

![Willkommen](/assets/images/installation/9/004.png)

Stimmen Sie bitte dem "License Agreement" zu, indem Sie den oberen Radiobutton wie in der Abbildung aktivieren und auf `Next` klicken

![License Agreement](/assets/images/installation/9/005.png)

Starten Sie die Installation per Klick auf `Next`.

![Start](/assets/images/installation/9/006.png)

Der Fortschritt der Installation wird per Laufbalken gezeigt.

![Installationsfortschritt](/assets/images/installation/9/007.png)

Die Installation ist beendet, bitte klicken Sie auf `Finish`.

![Fertigstellen](/assets/images/installation/9/008.png)

## Magellan Installationstypen

!!! info "Hinweis"

    Den Installationstyp `Server-/Einzelplatzinstallation` wählen Sie bitte aus, wenn Sie entweder eine netzwerkunabhängige Magellan-Installation wünschen oder wenn Sie Ihren Schulserver einrichten möchten. In beiden Fällen installieren Sie bitte auch `Firebird`.

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan9.msi`.

Der Setup Assistent von Magellan 9 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/installation/9/009.png)

Wählen Sie die `Server-/Einzelplatzinstallation` aus! <br/>Es wird das Programm installiert, zusätzlich wird die Datenbank abgelegt und es werden die Datenordner (Skripte, Berichte usw.) erzeugt. In den Datenordnern befinden sich alle Bestandteile auf die die Nutzer später gemeinsam zugreifen können, zum Beispiel Bericht, Seriendruckvorlagen, Skripte usw.

!!! info "Hinweis"

    Die Installation des Datenbankservers `Firebird` wird für die Installationsart `Server-/Einzelplatzinstallation` vorausgesetzt.

![Installationart festlegen](/assets/images/installation/9/010.png)

Der Assistent schlägt Ihnen einen Installationspfad vor, wir empfehlen diese Auswahl mit `Weiter` zu übernehmen.

![Installationspfad Programmdateien](/assets/images/installation/9/011.png)

Wählen Sie den Speicherort für die Datenbank und klicken Sie auf „Weiter“.

![Installationspfad Datenbank](/assets/images/installation/9/012.png)

Wählen Sie den Speicherort für die Datenordner `Berichte-, Dokumente-, Importe-, Skripte- und Vorlagenordner` und klicken Sie auf „Weiter“.

![Installationspfad Datenordner](/assets/images/installation/9/013.png)

Die Vorbereitungen sind abgeschlossen, klicken Sie auf `Weiter` um die Installation auszuführen.

![Vorbereitung abgeschlossen](/assets/images/installation/9/014.png)

![Fortschrittsbalken](/assets/images/installation/9/015.png)

Die Installation ist abgeschlossen, bitte klicken Sie auf `Fertigstellen`!

![Die Installation ist abgeschlossen.](/assets/images/installation/9/016.png)

### Speicherorte der Dateien

Nach Abschluss der Installation befinden sich standardmäßig die Dateien in folgenden Ordnern auf dem Server:

Anwendungsdaten (z.B. Magellan.exe):

| Betriebssystem | Pfad |
| --- | --- |
| Windows Server 2008 | C:\Program Files\Stueber Systems\Magellan 9\ |
| Windows 8 | C:\Programme\Stueber Systems\Magellan 9 |
| Windows 10 |C:\Program Files\Stueber Systems\Magellan 9 |
| Windows 11 |C:\Program Files\Stueber Systems\Magellan 9 |

Allgemeine Einstellungs- und Lizenzdaten (z.B. Magellan.evm, Magellan.lic, Magellan.SiteInfo, Magellan.UserInfo):

| Betriebssystem | Pfad |
| --- | --- |
| Windows Server 2008 | C:\ProgramData\Stueber Systems\Magellan 9 |
| Windows 8 | C:\ProgramData\Stueber Systems\Magellan 9 |
| Windows 10 | C:\ProgramData\Stueber Systems\Magellan 9|
| Windows 11 | C:\ProgramData\Stueber Systems\Magellan 9|

Datenordner (Vorlagen, Skripte, Importe, Dokumente, Berichte, Datenordner):

Auf die Datenordner sollen die Nutzer von den Arbeitsplatzrechnern aus zugreifen können. Bitte stellen Sie sicher, dass den Nutzern auf Betriebssystemebene Schreib- und Leserechte für diese Verzeichnisse eingeräumt werden. Diese Rechte sind notwendig, um alle Magellan-Funktionalitäten nutzen zu können (Beispiel: Berichte organisieren, Vorlagen organisieren, Ablegen von Schülerdokumenten u.a.).
Richten Sie bitte eine Freigabe für diese Verzeichnisse ein, die Sie anschließend für den Verweispfad der Arbeitsplatzrechner verwenden können.

| Betriebssystem | Pfad |
| --- | --- |
| Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\Magellan 9|
| Windows 8 | C:\Users\Public\Documents\Stueber Systems\Magellan 9 |
| Windows 10 | C:\Users\Public\Documents\Stueber Systems\Magellan 9 |
| Windows 11 | C:\Users\Public\Documents\Stueber Systems\Magellan 9 |

!!! info "Hinweis"

    Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren.

## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie Magellan 9 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/installation/9/welcome.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["Magellan - Erste Schritte"](https://doc.kb.stueber.de/magellan/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/installation/9/welcome-license-type.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/installation/9/welcome-enter-license.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/installation/9/welcome-region.png)

Bei einer Server-/Einzelplatzinstallation sind die Pfade für die Datenordner, die Datenbank und den Server schon korrekt vorbefüllt, bitte ändern Sie hier nichts.

![Wahl der Datenbank](/assets/images/installation/9/welcome-database.png)

![ Daten für entfernte Datenbank](/assets/images/installation/9/welcome-remote-database.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul Magellan Administrator auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. Bitte geben Sie den Netzwerkpfad zu Ihrem Server aus Sicht Ihres Rechners ein!

!!! info "Hinweis"

    Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul Magellan Administrator auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/9/welcome-remote-backup.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in Magellan](/assets/images/installation/9/Welcome-erste-schritte.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von Magellan. Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort „masterkey“ ein. Die Einrichtung Ihres Servers oder Ihres Arbeitsplatzes ist fertig!

![Abschluss des Willkommens-Assistenten](/assets/images/installation/9/anmeldung.png)
