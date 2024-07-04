# Den Server oder einen Einzelplatz einrichten

In diesem Abschnitt wird beschrieben, wie ein Platz eingerichtet wird, auf dem lokal die Datenbank gespeichert wird. 
In der Regel sollte das der Schulserver sein oder ein Arbeitsplatz, von dem aus nicht auf den Server zugeriffen werden kann, beispielsweise ein Testrechner.

!!! danger "Achtung"

    Wenn Sie bereits Magellan 10 einsetzen, lesen Sie bitte statt auch den Abschnitt [Umstieg von Magellan 10 auf Magellan 11](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/)!

## Vorbereitung

### Downloads

Für den Serverrechner benötigen Sie die Installationsdateien für:

* Firebird 4.0.2
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

## Installation von Firebird 4.0.2

!!! warning "Wichtig"

	Diese Installation wird einmalig im Netzwerk auf dem Rechner, auf dem später Ihre Magellan-Datenbank liegen wird ausgeführt. 

Laden Sie bitte das Firebird-Installationspaket von unseren Webseiten oder unter [folgendem Link](https://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei `Firebird-4.0.2.....-Win32`.

Die Installationsschritte im Einzelnen:

Wählen Sie bitte "English" und klicken auf `OK`!

[00]:/assets/images/installation/11/fb/00.png "Text"
![][00]

Stimmen Sie der Lizenzvereinbarung bitte zu (I accept the agreement) und klicken auf "Next"!

![](/assets/images/installation/11/fb/01.png)

Klicken Sie bitte auf "Next"!

![](/assets/images/installation/11/fb/03.png)

Bitte übernehmen Sie den voreingestellten Installationspfad!

[04]:/assets/images/installation/11/fb/04.png "Text"
![][04]

Bitte übernehmen Sie den voreingestellten Optionen!

[05]:/assets/images/installation/11/fb/05.png "Text"
![][05]

Bitte übernehmen Sie den voreingestellten Menüordner und klicken auf `Next`!

[06]:/assets/images/installation/11/fb/06.png "Text"
![][06]

Bitte übernehmen Sie die dargestellten Optionen und klicken auf `Next`!

[07]:/assets/images/installation/11/fb/07.png "Text"
![][07]

!!! warning "Wichtig!"

    Vergeben Sie ein 8-stelliges Passwort für den Benutzer `sysdba`. **Bitte stellen Sie sicher, dass dieses Passwort gesichert wird, beispielsweise in einem Passwortmanager.**
    Dieser Benutzer hat die höchsten administrativen Rechte und kann für die Erstanmeldung an Magellan verwendet werden, bevor personalisierte Benutzerzugänge verwendet werden.

[08]:/assets/images/installation/11/fb/08.png "Text"
![][08]

Starten Sie die Installation über die Schaltfläche `Install`!

[09]:/assets/images/installation/11/fb/09.png "Text"
![][09]

[10]:/assets/images/installation/11/fb/10.png "Text"
![][10]

Die Installation ist abschlossen, bitte klicken Sie auf `Next`!

[11]:/assets/images/installation/11/fb/11.png "Text"
![][11]

Bitte lassen Sie mindestens das Häkchen vor `Start Firebird Service now?` aktiviert um den Firebird-Dienst zu starten!

[12]:/assets/images/installation/11/fb/12.png "Text"
![][12]

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

## Magellan Installation

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan11.msi`.

Der Setup-Assistent von Magellan 11 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/installation/11/001.png)

Wählen Sie die `Server-/Einzelplatzinstallation` aus! <br/>Es wird das Programm installiert, zusätzlich wird die Datenbank abgelegt und es werden die Datenordner (Skripte, Berichte usw.) erzeugt. In den Datenordnern befinden sich alle Bestandteile auf die die Nutzer später gemeinsam zugreifen können, zum Beispiel Bericht, Seriendruckvorlagen, Skripte usw.

![Installationart festlegen](/assets/images/installation/11/001.1.png)

Der Assistent schlägt Ihnen einen Installationspfad vor, wir empfehlen diese Auswahl mit `Weiter` zu übernehmen. Der in der Abbildung gezeigte Pfad entspricht der Installation auf einem Gerät mit 64-Bit Betriebssystem, der Pfad für ein 32-Bit Betriebssystem weicht davon ab.

![Installationart festlegen](/assets/images/installation/11/001.2.png)

Wählen Sie den Speicherort für die Datenbank und klicken Sie auf „Weiter“.

![Speicherort für die Datenbank](/assets/images/installation/11/001.3.png)

Wählen Sie den Speicherort für die Datenordner (Berichte, Dokumente, Improte, Skripte und Vorlagen) und klicken Sie auf „Weiter“.

![Speicherort für die Datenordner](/assets/images/installation/11/001.4.png)

Die Voreinstellungen sind abgeschlossen, bitte starten Sie die Installation mit `Fertigstellen`!

![Vorbereitungen abgeschlossen](/assets/images/installation/11/002.png)

![Installation läuft](/assets/images/installation/11/003.png)

Die Installation ist abgeschlossen, klicken Sie bitte auf `Fertigstellen`!

![Fertig!](/assets/images/installation/11/003.png)

### Speicherorte der Dateien

Nach Abschluss der Installation befinden sich standardmäßig die Dateien in folgenden Ordnern auf dem Server:

#### Anwendungsdaten (z.B. Magellan.exe)

| Betriebssystem | Pfad |
| --- | --- |
| Windows Server 2008 | C:\Program Files\Stueber Systems\Magellan 11\ |
| Windows 64 Bit |C:\Program Files\Stueber Systems\Magellan 11 |
| Windows 32 Bit|C:\Program Files (x86)\Stueber Systems\Magellan 11|

#### Allgemeine Einstellungs- und Lizenzdaten 

(z.B. Magellan.evm, Magellan.lic, Magellan.SiteInfo, Magellan.UserInfo):

| Betriebssystem | Pfad |
| --- | --- |
| Windows Server 2008 | C:\ProgramData\Stueber Systems\Magellan 11 |
| Windows 8 | C:\ProgramData\Stueber Systems\Magellan 11 |
| Windows 10 | C:\ProgramData\Stueber Systems\Magellan 11|
| Windows 11 | C:\ProgramData\Stueber Systems\Magellan 11|

#### Datenordner

(Vorlagen, Skripte, Importe, Dokumente, Berichte, Datenordner):

!!! warning "Wichtig!"

    Auf die Datenordner sollen die Nutzer von den Arbeitsplatzrechnern aus zugreifen können. Bitte stellen Sie sicher, dass den Nutzern auf Betriebssystemebene Schreib- und Leserechte für diese Verzeichnisse eingeräumt werden. Diese Rechte sind notwendig, um alle Magellan-Funktionalitäten nutzen zu können (Beispiel: Berichte organisieren, Vorlagen organisieren, Ablegen von Schülerdokumenten u.a.).
    Richten Sie bitte eine Freigabe für diese Verzeichnisse ein, die Sie anschließend für den Verweispfad der Arbeitsplatzrechner verwenden können.

| Betriebssystem | Pfad |
| --- | --- |
| Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\Magellan 11|
| Windows 8 | C:\Users\Public\Documents\Stueber Systems\Magellan 11 |
| Windows 10 | C:\Users\Public\Documents\Stueber Systems\Magellan 11 |
| Windows 11 | C:\Users\Public\Documents\Stueber Systems\Magellan 11 |

!!! info "Hinweis"

    Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren.

## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie Magellan 11 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/installation/11/w/001.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["Magellan - Erste Schritte"](https://doc.kb.stueber.de/magellan/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/installation/11/w/002.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/installation/11/w/003.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/installation/11/w/004.png)

Bei einer Server-/Einzelplatzinstallation sind die Pfade für die Datenordner, die Datenbank und den Server schon korrekt durch Ihre Angaben während der Magellan-Installation vorbefüllt, bitte ändern Sie hier nichts. 

![Lokale Datenbank](/assets/images/installation/11/w/005.1.png)

Es wird standardmäßig auf eine Beispieldatenbank verwiesen, in der für erste Tests bereits Daten vorbereitet sind. Wenn Sie mit einer leeren Datenbank beginnen möchten, ändern Sie lediglich die Bezeichnung der Datenbank. Beide Datenbankvarianten wurden bei der Installation von Magellan abgelegt.
<br/> Leere Datenbank: `Magellan11.fdb`
<br/> Beispieldatenbank: `Magellan11_Beispiel.fdb`

![Datenbankpfad](/assets/images/installation/11/w/005.2.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an.   
Eine Sicherung Ihrer Datenbank kann über das Modul Magellan Administrator auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. 

!!! danger "Warnung"

      Sollten Sie andere Speicherorte also vorgeschlagen wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren.<br/>
      Die Sicherung kann später von jedem Rechner aus über das Modul Magellan Administrator gestartet werden, wird aber stets auf dem Rechner erzeugt, auf dem die Datenbank liegt.


![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/11/w/007.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in Magellan](/assets/images/installation/11/w/008.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von Magellan. 
Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort Ihr Passwort ein, dass Sie während der Firebird-Installation gewählt haben. Die Einrichtung Ihres Servers oder Ihres Arbeitsplatzes ist fertig!

![Abschluss des Willkommens-Assistenten](/assets/images/installation/11/w/009.png)
