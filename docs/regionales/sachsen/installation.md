## Installation und Lizenzierung von MAGELLAN 7


|Notwendige Schritte |
|-|
|[1. MAGELLAN 6 und Firebird aktualisieren](https://doc.magellan7.stueber.de/installation/umstieg-von-6-auf-7.html#magellan-6-und-firebird-aktualisieren)|
|[2. MAGELLAN 7 installieren](https://doc.magellan7.stueber.de/installation/umstieg-von-6-auf-7.html#magellan-7-installieren)|



## MAGELLAN 6 und Firebird aktualisieren

Um die Daten Ihrer MAGELLAN 6-Datenbank in eine MAGELLAN 7-Datenbank übernehmen zu können, muss die aktuellste Ausgabe von MAGELLAN 6 und der dazugehörigen Firebird-Installation eingesetzt werden.

> #### warning::Wichtig!
>
> Bitte vergleichen Sie die angezeigte Version unter `MAGELLAN > Hilfe > Info über` und `Systemsteuerung > Firebird Server Manager (32-Bit)` mit den angezeigten Version auf im [Downloadbereich](https://magellan.stueber.de/download.php) oder im Abschnitt [Was ist neu?](https://doc.magellan6.stueber.de/changelog.html) der MAGELLAN 6-Dokumentation!
> 
>Bitte beachten Sie unsere Anleitungen zum Aktualisieren von [MAGELLAN 6](https://doc.magellan6.stueber.de/installation/update.html) und [älteren Firebirdversionen](https://doc.magellan6.stueber.de/installation/firebird-aktualisieren.html), da für den Wechsel auf MAGELLAN 7 zuvor die aktuelleste MAGELLAN 6-Ausgabe vorausgesetzt wird!  

## MAGELLAN 7 installieren

Führen Sie als nächstes bitte die Installation von MAGELLAN 7 aus, beide Version (6 + 7) können parallel auf einem Rechner laufen (haben aber getrennte Datenbanken). Eine ausführliche Installationsanleitung finden Sie nachstehend.



> ####### warning::Wichtig!
>
>  Benötigen Sie eine "frische" leere Datenbank im MAGELLAN 7-Format können Sie diese [hier](ftp://ftp.stueber.de/pub/bin/de/magellan/v7/database/MAGELLAN7.FDB) herunterladen.



> #### primary::Hinweis
>
>  Da Sie MAGELLAN 7 aktuell nur einrichten um die Schnittstelle SAXSVS zu bedienen, genügt eine Server-/Einzelplatzinstallation auf Ihrem Serverrechner  oder auf einem Arbeitsplatzrechner. Sollten Sie sich für Ihren Serverrechner entscheiden, kann die dort laufende Firebirdversion 2.5.8 parallel von beiden Anwendungen genutzt werden, auf einem Arbeitsplatzrechner müsste Firebird zusätzlich installiert werden.

Bitte beachten Sie die [Systemvoraussetzungen](https://doc.magellan7.stueber.de/installation/systemvoraussetzungen.html).



## Netzwerk, Einzelarbeitsplatz oder einen Arbeitsplatz einrichten?

Kurz vorab, je nachdem was Sie einrichten möchten sind unterschiedliche Installationen oder Installationstypen notwendig.

Was ist grob zu tun?

Art|Was ist zu tun
---|---
**Netzwerk:** |Server: auf dem Serverrechner muss eine Firebird-Installation und MAGELLAN als Server/Einzelplatz-Installation durchgeführt werden. <br/><br/>Arbeitsplätze: Auf den Arbeitsplatzrechnern wird nur MAGELLAN mit dem Installationstyp "Arbeitsplatzinstallation" ausgeführt und die Verbindung zu dem auf dem Rechner abgelegten gemeinsam verwendeten Daten (Datenbank, Datenordner mit Skripten, Berichten usw.) eingerichtet. <br/><br/>Alle Rechner: Die Lizenz und die Verbindungsdaten werden pro Installation eingetragen. Alternativ können auch mehrere MAGELLAN-Installationen auf eine gemeinsame Lizenzdatei  und/oder Verbindungsdatei zugreifen. Was Sie dafür einrichten müssen beschreiben wir im Abschnitt [Die Pathsdatei](https://doc.magellan7.stueber.de/installation/die-pathsdatei.html).
**Einzelarbeitsplatz:**|Ein Einzelarbeitsplatz wird genau wie ein Serverrechner eingerichtet:<br/><br/> - Installieren Sie Firebird.<br/> - MAGELLAN wird als Server/Einzelplatz-Installation eingerichtet.. <br/> - Lizenzieren Sie die Installation.
**Arbeitsplatz:**|Sie haben ein Netzwerk bestehend aus einem MAGELLAN-Server und Arbeitsplatzrechnern und möchten nur einen weiteren Arbeitsplatzrechner einrichten? <br/><br/> - Führen Sie auf dem Rechner die MAGELLAN-Installation mit dem Installationstyp "Arbeitsplatzinstallation" aus. <br/> -  Lizenzieren Sie den Arbeitsplatz. <br/> - Richten die Verbindung zu den Daten auf dem Server ein. <br/><br/>Auch hier ist es möglich statt lokaler Verbindungsdaten und Lizenz per [Pathsdatei](https://doc.magellan7.stueber.de/installation/die-pathsdatei.html) auf gemeinsame Daten zu verweisen.




## Welche Firebirdversion? 

Wenn Sie MAGELLAN 7 nicht auf Ihrem Schulverwaltungserver einrichten möchten, sondern zum Beispiel nur auf einem Arbeitsplatz, dann muss dieser Rechner wie ein MAGELLAN 7-Server eingerichtet werden. Dazu gehört die Installation von Firebird 2.5.8 und eine Server-/Einzelplatzinstallation von MAGELLAN 7.
Wenn Sie Ihren Schulverwaltungsserver nutzen möchten, dann stellen Sie bitte sicher, dass dort auch die für das aktuelle MAGELLAN 6 genutzte Firebird 2.5.8 verwendet wird.

|Wenn nicht, gehen Sie wie folgt vor|
|--|
|Informieren Sie Ihre Kollegen darüber, dass MAGELLAN 6 kurzzeitig nicht genutzt werden kann und die Module geschlossen werden sollen|
|Stoppen Sie unter `Systemsteuerung > Verwaltung > Dienste` Ihren Firebird-Server-Manager. <br/><br/>![Firebirddienst stoppen](../assets/images/sachsen/fb.stoppen.png) |
| Laden Sie das aktuelle Installationspaket von Firebird herunter: [Firebird-Download](ftp://ftp.stueber.de/pub/bin/de/magellan/v6/Firebird-2.5.8.27089_0_Win32.exe) | 
| Starten Sie anschließend die Firebird-Installation durch einen Doppelklick auf die Datei `Firebird-2.5.8......Win32.exe`. <br/>Bitte übernehmen Sie im daraufhin startenden Installationsassistenten auf der Karte „Komponenten auswählen“ die voreingestellten Optionen.<br/><br/>![Komponenten auswählen](../assets/images/fb-components.png)|
| Auf der Karte „Zusätzliche Aufgaben auswählen“ übernehmen Sie bitte die Optionen und aktivieren zusätzlich das Häkchen „Die Firebird Client-Bibliothek ins Systemverzeichnis kopieren“. <br/><br/>![Zusätzliche Aufgaben auswählen](../assets/images/fb-tasks.png) |

> #### danger::Wichtig
>
> Firebird wird nur dem Rechner installiert werden, auf dem zukünftig die Datenbank gespeichert wird. Das kann Ihr Server sein oder auch ein netzwerkunabhängiger Rechner. 
> Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme \(Eingehende und Ausgehende Regel\) für diesen Port ein und versuchen es bitte erneut.

## Download und Installationstypen

Laden Sie bitte das MAGELLAN-Installationspaket unter [folgendem Link](ftp://ftp.stueber.de/pub/bin/de/magellan/v7/beta/magellan7.msi). Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan7.msi`.

Der Setup Assistent von MAGELLAN 7 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](../assets/images/sachsen/setup-start.png)

![Installationart festlegen](../assets/images/sachsen/setup-type.png)

Wählen Sie die gewünschte Installationsart aus:

Installationstyp|Anmerkung
---|---
Server|Der Datenbank-Server \(Firebird\) und alle weiteren Module werden auf einem Server installiert. Auf diesen befindet sich im Regelfall die MAGELLAN 7 Datenbank. Die einzelnen Arbeitsstationen, welche auf den Server zugreifen, werden mit der Art „Arbeitsplatz“ installiert.
Einzelplatz|Der Datenbank-Server und alle weiteren Module werden auf einem Rechner installiert. Sie entspricht der Serverinstallation im Netz und wird daher über die gleiche Option ausgewählt.
Arbeitsplatz|Es wird ein Arbeitsplatz in Netzwerk installiert. Dazu werden nur die Anwendungsdaten und der Datenbank-Client installiert, jedoch nicht Datenbank, Berichte oder Skripte. Eine Arbeitsplatzinstallation setzt eine Serverinstallation voraus. Firebird darf auf diesem Arbeitsplatz nicht installiert sein.

Die weiteren Beschreibungen finden Sie in den nachfolgenden Abschnitten „Serverinstallation“, „Arbeitsplatzinstallation“ und „Einzelplatzinstallation.

> #### danger::Wichtig
>
> Die Installation des Datenbankservers \(Firebird\) wird für die Installationsarten Server und Einzelplatz vorausgesetzt.

## Serverinstallation und Einzelplatzinstallation

Nachdem Sie die Installationsart „Server bzw. Einzelplatz“ gewählt haben, ist der Setup Assistent bereit, die Installation der Dateien vorzunehmen. Die Installation selbst muss direkt auf dem Server oder dem Einzelplatz erfolgen.


Wählen Sie zunächst den Speicherort für die Programmdateien aus.

![Speicherort für die Programmdateien](../assets/images/sachsen/setup-folder.png)

Wählen Sie den Speicherort für die Datenbank und klicken Sie auf „Weiter“.

![Speicherort für die Datenbank](../assets/images/sachsen/setup-database.png)

Wählen Sie den Speicherort für die Datenordner \(Berichte-, Dokumente-, Importe-, Skripte- und Vorlagenordner\) und klicken Sie auf „Weiter“.

![Speicherort für die Datenordner](../assets/images/sachsen/setup-data-folder.png)

> #### danger::Achtung!
>
> Der Installationsassistent schlägt Ihnen hier Speicherpfade für die Datenordner vor. Diese Pfade können Sie im Assistenten anpassen. Bitte beachten Sie, dass diese Pfade später bei Updates verwendet werden. Sollten Sie hier angelegten Verzeichnisse auf Dateiebene verschieben, können trotz Update aktualisierte Daten fehlen. Sollten Sie sich später umentscheiden, deinstallieren Sie das Programm vom Serverrechner, installieren neu und geben den gewünschten Pfad an.

Klicken Sie nun auf „Installieren“, um mit der Installation zu beginnen.

![Bereit zur Installation](../assets/images/sachsen/setup-ready.png)

Die Installation selbst kann einige Minuten in Anspruch nehmen. Klicken Sie zum Abschließen der Installation auf „Fertigstellen“.

![Die Installation ist fertig](../assets/images/sachsen/setup-finished.png)

### Speicherorte der Dateien

Nach Abschluss der Installation befinden sich standardmäßig die Dateien in folgenden Ordnern auf dem Server:

#### Anwendungsdaten \(z.B. Magellan.exe\):

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\Program Files\Stueber Systems\MAGELLAN 7 |
| Windows XP | C:\Programme\Stueber Systems\MAGELLAN 7 |
| Windows 2000 | C:\Programme\Stueber Systems\MAGELLAN 7 |
| Windows 7 | C:\Programme\Stueber Systems\MAGELLAN 7 |
| Windows Server 2008 | C:\Program Files \(x86\)\Stueber Systems\MAGELLAN 7\ |
| Windows 8 | C:\Programme\Stueber Systems\MAGELLAN 7 |
| Windows 10 | C:\Program Files \(x86\)\Stueber Systems\MAGELLAN 7\ |

#### Allgemeine Einstellungs- und Lizenzdaten \(z.B. Magellan.evm, Magellan.lic, Magellan.SiteInfo, Magellan.UserInfo\):

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\MAGELLAN 7 |
| Windows 2000 | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\MAGELLAN 7 |
| Windows 7 | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows Server 2008 | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows 8 | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows 10 | C:\ProgramData\Stueber Systems\MAGELLAN 7 |

#### Datenordner \(Vorlagen, Skripte, Importe, Dokumente, Berichte, Datenordner\):

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7 |
| Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\MAGELLAN 7 |
| Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\MAGELLAN 7 |
| Windows 7 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7 |
| Windows Server 2008 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7 |
| Windows 8 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7 |
| Windows 10 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7 |

> #### primary::Hinweis
>
> Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren.

## Arbeitsplatzinstallation

Starten Sie die Installation per Doppelklick auf das Installationspaket, wählen Sie im Assitenten bitte den Installationstyp "Arbeitsplatz" aus.
Im Unterschied zur Serverinstallation werden bei der Arbeitsplatzinstallation nur die Anwendungsdaten installiert. Die dafür verwendeten standardmäßigen Ordner entsprechen jenen bei der Serverinstallation.

![Bitte wählen Sie den Installationstyp Arbeitsplatz aus!](../assets/images/sachsen/setup-type.png)


## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie MAGELLAN 7 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](../assets/images/sachsen/welcome.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.


![Wahl zwischen Vollversion und Testlizenz](../assets/images/sachsen/welcome-license-type.png)


Wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](../assets/images/sachsen/welcome-enter-license.png)

** Wählen Sie hier als Region "Sachsen" aus und klicken dann auf „Weiter“.** Wenn hier eine andere Auswahl getroffen wird, steht später in der Oberfläche nicht der Export für SAXSVS zur Verfügung!

![Wahl der Region](../assets/images/sachsen/welcome-region.png)

Sie müssen entscheiden, ob Sie mit einer entfernten oder einer lokalen Datenbank arbeiten möchten. Bei einer Server-/Einzelplatzinstallation stellen Sie „Lokale Datenbank“ ein. Bei einer Arbeitsplatzinstallation wählen Sie „Entfernte Datenbank“.

![Wahl der Datenbank](../assets/images/sachsen/welcome-database.png)

### Entfernte Datenbank

Bei der Auswahl „Entfernte Datenbank“ werden Sie zur Eingabe des Servernamens und des Datenbank-Pfads aufgefordert.

![ Daten für entfernte Datenbank](../assets/images/sachsen/welcome-remote-database.png)

Geben Sie unter „Server“ den **Servernamen bzw. die IP-Adresse Ihres Servers** ein, auf dem sich die MAGELLAN 7 Datenbank befindet. Im unteren Feld geben Sie den lokalen Serverpfad \(aus Sicht des Servers\) zur MAGELLAN 7 Datenbank an.

Der standardmäßige Pfad zur MAGELLAN 7 Datenbank lautet:

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\Users\Public\Documents\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems \MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 7 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2003 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2008 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7 Datenbank\Magellan7.fdb |

Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der oben gezeigten Datenbankpfade zu.

Im folgenden Bild werden die Verzeichnisse der Datenordner abgefragt. Die Datenordner (Berichte, Skripte, Vorlagen usw.) werden bei der Installation des Serverrechners oder der Einzelplatzinstallation angelegt. Sie verweisen in diesem Fenster auf den Speicherort der Verzeichnisse, die alle gemeinsam an einer Stelle abgelegt wurden. Um sich Tipparbeit zu sparen, können Sie in der oberen Zeile den Wurzelpfad eingeben und auf das Startdreieck klicken, die nachfolgenden Zeilen werden dann entsprechend mit diesem Pfad und dem Standardnamen des Verzeichnisses befüllt.

![Daten für entfernte Datenordner](../assets/images/sachsen/welcome-remote-datafolder.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul MAGELLAN ADMINISTRATOR auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. Bitte geben Sie den Netzwerkpfad zu Ihrem Server aus Sicht Ihres Rechners ein!

> #### primary::Hinweis
>
> Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul MAGELLAN ADMINISTRATOR auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](../assets/images/sachsen/welcome-remote-backup.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](../assets/images/sachsen/Welcome-erste-schritte.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort „masterkey“ ein.

![Abschluss des Willkommens-Assistenten](../assets/images/sachsen/anmeldung.png)


### Lokale Datenbank

Direkt auf dem Server oder einem Einzelplatz entscheiden Sie sich bitte für „Lokale Datenbank“. Sie werden dann zur Eingabe des Datenbankpfads aufgefordert.

Im Anschluss:

![Daten für lokale Datenbank](../assets/images/sachsen/welcome-local-database.png)

Der standardmäßige Pfad zur MAGELLAN 7 Datenbank lautet:

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\Users\Public\Documents\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems \MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 7 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2003 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2008 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7 Datenbank\Magellan7.fdb |

> #### primary::Hinweis
>
> Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der beiden oben gezeigten Beispielpfade zu. Bei der Installation werden zwei Datenbanken abgelegt. Einmal die noch leere MAGELLAN7.fdb, in die dann Ihre Daten übertragen werden sollen und eine Beispieldatenbank mit der Bezeichnung "MAGELLAN7_Beispiel.FDB".

Im folgenden Bild werden die Verzeichnisse der Datenordner abgefragt. In der Regel sind die Vorgaben richtig. Hat man die Skripte, Berichte, Dokumente etc. aber an anderer Stelle \(z.B. auf dem Server\) gespeichert, kann man dies hier angeben.

![Daten für lokale Datenordner](../assets/images/sachsen/welcome-local-datafolder.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Die vorgeschlagenen Verzeichnisse werden bei der Installation mit angelegt. Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul MAGELLAN ADMINISTRATOR auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](../assets/images/sachsen/welcome-local-backup.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](../assets/images/sachsen/Welcome-erste-schritte.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort „masterkey“ ein.

![Abschluss des Willkommens-Assistenten](../assets/images/sachsen/anmeldung.png)




