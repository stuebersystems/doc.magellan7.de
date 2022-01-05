
# Den Server oder einen Einzelplatz einrichten

In diesem Abschnitt wird beschrieben, wie ein Platz eingerichtet wird, auf dem lokal die Datenbank gespeichert wird, in der Regel sollte das der Schulserver sein oder ein Arbeitsplatz, von dem aus nicht auf den Server zugeriffen werden kann, beispielsweise ein Testrechner.

!!! danger "Achtung"

    Wenn Sie bereits MAGELLAN 8 einsetzen, lesen Sie bitte statt auch den Abschnitt [Umstieg von MAGELLAN 8 auf MAGELLAN 9](https://doc.magellan.stueber.de/schulverwaltung/update/umstieg-von-8-auf-9/)!

## Vorbereitung und Downloads

**MAGELLAN.lic**: 
Legen Sie sich bitte die Lizenzdatei so zurecht, dass Sie vom Server und von den Clients darauf zugreifen können. Die Datei wurde Ihnen als Test- oder Volllizenz von unserem Office-Team per Mail zugesandt. Sollte Ihnen die Lizenzdatei noch fehlen, können Sie sie per Mail an office@stueber.de neu anfragen. Für eine Volllizenz bitten wir um die Angabe der Kundennummer, herzlichen Dank!

**Downloads**: 
Für den Serverrechner benötigen Sie die Installationsdatei für Firebird und für MAGELLAN. Alle Installationspakete finden Sie hier:

* [Firebird](https://download.stueber.de/bin/de/firebird/Firebird-2.5.9.27139_0_Win32.exe) 
* MAGELLAN: Wählen Sie je nach Betriebssystem bitte das Installationspaket für [Windows 64-bit](https://download.stueber.de/bin/de/magellan/v9/magellan9.msi) oder [Windows 32-bit](https://download.stueber.de/bin/de/magellan/v9/magellan9_32.msi).

!!! danger "Hinweis"

    Die Unterscheidung zwischen dem MAGELLAN Installationspaket für Windows 32-bit und Windows 64-bit bezieht sich nicht auf MAGELLAN selbst, dass immer 32-bit angeboten wird, sondern gilt für die mit installierten Crystal Reports-Treiber. Kunden, die eine eigene Crystal Reports-Lizenz zum editieren von Berichten und Zeugnissen verwenden, greifen auf diese Treiber zu. Crystal Reports wird seit den letzten Veröffentlichungen nur noch als reine 64-bit-Software angeboten, kann also nur auf 64-bit Betriebssystemen verwendet werden und benötigt die 64-bit Treiber, die mit der MAGELLAN Installation hinterlegt werden.

## Installation von Firebird 2.5

!!! warning "Wichtig"

	Diese Installation wird einmalig im Netzwerk auf dem Rechner, auf dem später Ihre MAGELLAN-Datenbank liegen wird ausgeführt. 

Laden Sie bitte das Firebird-Installationspaket von unseren Webseiten oder unter [folgendem Link](https://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei `Firebird-2.5......Win32.exe`. Bitte übernehmen Sie im daraufhin startenden Installationsassistenten auf der Karte „Komponenten auswählen“ die voreingestellten Optionen.

![Komponenten auswählen](/assets/images/fb-components.png)

Auf der Karte „Zusätzliche Aufgaben auswählen“ übernehmen Sie bitte die Optionen und aktivieren zusätzlich das Häkchen „Die Firebird Client-Bibliothek ins Systemverzeichnis kopieren“.

![Zusätzliche Aufgaben auswählen](/assets/images/fb-tasks.png)

!!! warning "Wichtig"

	Firebird wird nur dem Rechner installiert werden, auf dem zukünftig die Datenbank gespeichert wird. Das kann Ihr Server sein oder auch ein netzwerkunabhängiger Rechner. 
	
	Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme \(Eingehende und Ausgehende Regel\) für diesen Port ein und versuchen es bitte erneut.

## MAGELLAN Installationstypen

!!! info "Hinweis"

    Die Installation des Datenbankservers \(Firebird\) wird für die Installationsarten Server und Einzelplatz vorausgesetzt. 
    Den Installationstyp `Server-/Einzelplatzinstallation` wählen Sie bitte aus, wenn Sie entweder eine netzwerkunabhängige MAGELLAN-Installation wünschen (zum Beispiel um MAGELLAN zu testen) oder wenn Sie Ihren Schulserver einrichten möchten.

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan9.msi`.

Der Setup Assistent von MAGELLAN wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/installation/9/setup_start.png)

![Installationart festlegen](/assets/images/installation/9/setup_type.png)

Wählen Sie die `Server-/Einzelplatzinstallation` aus! Es wird das Programm installiert, zusätzlich wird die Datenbank abgelegt und es werden die sogenannten Datenordner erzeugt. In den Datenordnern befinden sich alle Bestandteile auf die die Nutzer später gemeinsam zugreifen können, zum Beispiel Bericht, Seriendruckvorlagen, Skripte usw.

!!! info "Hinweis"

    Die Installation des Datenbankservers \(Firebird\) wird für die Installationsarten Server und Einzelplatz vorausgesetzt.

Jetzt ist der Setup Assistent bereit, die Installation der Dateien vorzunehmen. Die Installation selbst muss direkt auf dem Server oder dem Einzelplatz erfolgen.


Wählen Sie zunächst den Speicherort für die Programmdateien aus.

![Speicherort für die Programmdateien](/assets/images/installation/9/setup-folder.png)

Wählen Sie den Speicherort für die Datenbank und klicken Sie auf „Weiter“.

![Speicherort für die Datenbank](/assets/images/installation/9/setup-database.png)

Wählen Sie den Speicherort für die Datenordner \(Berichte-, Dokumente-, Importe-, Skripte- und Vorlagenordner\) und klicken Sie auf „Weiter“.

![Speicherort für die Datenordner](/assets/images/installation/9/setup-data-folder.png)

!!! info "Hinweis"

    Der Installationsassistent schlägt Ihnen hier Speicherpfade für die Datenordner vor. Diese Pfade können Sie im Assistenten anpassen. Bitte beachten Sie, dass diese Pfade später bei Updates verwendet werden. Sollten Sie hier angelegten Verzeichnisse auf Dateiebene verschieben, können trotz Update aktualisierte Daten fehlen. Sollten Sie sich später umentscheiden, deinstallieren Sie das Programm vom Serverrechner, installieren neu und geben den gewünschten Pfad an.

Klicken Sie nun auf „Installieren“, um mit der Installation zu beginnen.

![Bereit zur Installation](/assets/images/installation/9/setup-ready.png)

Die Installation selbst kann einige Minuten in Anspruch nehmen. Klicken Sie zum Abschließen der Installation auf „Fertigstellen“.

![Die Installation ist fertig](/assets/images/installation/9/setup-finished.png)

### Speicherorte der Dateien

Nach Abschluss der Installation befinden sich standardmäßig die Dateien in folgenden Ordnern auf dem Server:

Anwendungsdaten \(z.B. Magellan.exe\):

| Betriebssystem | Pfad |
| --- | --- |
| Windows 7 | C:\Programme\Stueber Systems\MAGELLAN 9 |
| Windows Server 2008 | C:\Program Files \(x86\)\Stueber Systems\MAGELLAN 9\ |
| Windows 8 | C:\Programme\Stueber Systems\MAGELLAN 9 |
| Windows 10 | C:\Program Files \(x86\)\Stueber Systems\MAGELLAN 9\ |

Allgemeine Einstellungs- und Lizenzdaten \(z.B. Magellan.evm, Magellan.lic, Magellan.SiteInfo, Magellan.UserInfo\):

| Betriebssystem | Pfad |
| --- | --- |
| Windows 7 | C:\ProgramData\Stueber Systems\MAGELLAN 9 |
| Windows Server 2008 | C:\ProgramData\Stueber Systems\MAGELLAN 9 |
| Windows 8 | C:\ProgramData\Stueber Systems\MAGELLAN 9 |
| Windows 10 | C:\ProgramData\Stueber Systems\MAGELLAN 9|

Datenordner \(Vorlagen, Skripte, Importe, Dokumente, Berichte, Datenordner\):

Auf die Datenordner sollen die Nutzer von den Arbeitsplatzrechnern aus zugreifen können. Bitte stellen Sie sicher, dass den Nutzern auf Betriebssystemebene Schreib- und Leserechte für diese Verzeichnisse eingeräumt werden. Diese Rechte sind notwendig, um alle MAGELLAN-Funktionalitäten nutzen zu können (Beispiel: Berichte organisieren, Vorlagen organisieren, Ablegen von Schülerdokumenten u.a.).
Richten Sie bitte eine Freigabe für diese Verzeichnisse ein, die Sie anschließend für den Verweispfad der Arbeitsplatzrechner verwenden können.

| Betriebssystem | Pfad |
| --- | --- |
| Windows 7 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 9 |
| Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 9|
| Windows 8 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 9 |
| Windows 10 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 9 |

!!! info "Hinweis"

    Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren.

## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie MAGELLAN 9 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/installation/9/welcome.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["MAGELLAN - Erste Schritte"](https://doc.kb.stueber.de/magellan/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/installation/9/welcome-license-type.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/installation/9/welcome-enter-license.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/installation/9/welcome-region.png)

Bei einer Server-/Einzelplatzinstallation sind die Pfade für die Datenordner, die Datenbank und den Server schon korrekt vorbefüllt, bitte ändern Sie hier nichts.

![Wahl der Datenbank](/assets/images/installation/9/welcome-database.png)

![ Daten für entfernte Datenbank](/assets/images/installation/9/welcome-remote-database.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul MAGELLAN ADMINISTRATOR auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. Bitte geben Sie den Netzwerkpfad zu Ihrem Server aus Sicht Ihres Rechners ein!

!!! info "Hinweis"

    Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul MAGELLAN ADMINISTRATOR auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/9/welcome-remote-backup.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](/assets/images/installation/9/Welcome-erste-schritte.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort „masterkey“ ein. Die Einrichtung Ihres Servers oder Ihres Arbeitsplatzes ist fertig!

![Abschluss des Willkommens-Assistenten](/assets/images/installation/9/anmeldung.png)
