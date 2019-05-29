
# Arbeitsplatzinstallation


Diesen Installationstyp wählen Sie bitte aus, wenn Sie einen Arbeitsplatzrechner einrichten möchten. Das bedeutet, MAGELLAN als Programm wird auf diesem Rechner installiert, auf alle gemeinsam verwendeten Dateien (zb. Berichte, Vorlagen, Skripte usw.) wird über das Netzwerk zugriffen.

Es werden während der Installation nur Programmdateien abgelegt, im Anschluss wird der Willkommensassistent gestartet, Sie geben die Pfade zu den gemeinsam genutzten Verzeichnissen in Ihrem Netzwerk ein.

!!! info "Hinweis"

  Vermutlich werden Sie mehr als einen Arbeitsplatz einrichten? Ab dem zweiten Arbeitplatz müsste nur noch die Installation ausgeführt werden, einige Dateien können mit den enthaltenen Einstellungen entweder lokal ([Einstellungen vom Arbeitsplatz kopieren](https://doc.magellan7.stueber.de/schulverwaltung/installation/arbeitsplatz.installlieren/#einstellungen-vom-arbeitsplatz-kopieren)) auf den weiteren Arbeitsplätze abgelegt werden oder für eine gemeinsame Nutzung zentral (["Die Pathsdatei"](https://doc.magellan7.stueber.de/schulverwaltung/installation/die-pathsdatei.html)) abgelegt werden.



## Download und Installationstypen

Laden Sie bitte das MAGELLAN-Installationspaket von unseren Webseiten oder unter [folgendem Link](ftp://ftp.stueber.de/pub/bin/de/magellan/v7/beta/magellan7.msi). Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan7.msi`.

Der Setup Assistent von MAGELLAN 7 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/setup-start.png)

![Installationart festlegen](/assets/images/setup-type.png)

Wählen Sie die `Arbeitsplatzinstallation` aus! Es wird nur das Programm installiert, es werden keine Datenbank abgelegt oder sogenannten Datenordner erzeugt.


![Bitte wählen Sie den Installationstyp Arbeitsplatz aus!](/assets/images/setup-type.png)

## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie MAGELLAN 7 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/welcome.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["MAGELLAN 7 - Erste Schritte"](https://doc.magellan7-kb.stueber.de/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/welcome-license-type.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/welcome-enter-license.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/welcome-region.png)

Wählen Sie „Entfernte Datenbank“.

![Wahl der Datenbank](/assets/images/welcome-database.png)

Sie werden zur Eingabe des Servernamens und des Datenbank-Pfads aufgefordert.
Geben Sie unter `Server` den **Servernamen bzw. die IP-Adresse Ihres Servers** ein, auf dem sich die MAGELLAN 7 Datenbank befindet. Im unteren Feld geben Sie den lokalen Serverpfad \(aus Sicht des Servers\) zur MAGELLAN 7 Datenbank an.

!!! info "Hinweis"

	Der einzutragende Pfad unterscheidet sich zwischen dem Serverrechner und dem Arbeitsplatzrechner nicht, der Unterschied besteht lediglich beim Eintrag im Feld `Server`.

![ Daten für entfernte Datenbank](/assets/images/welcome-remote-database.png)

Der standardmäßige Pfad zur MAGELLAN 7 Datenbank lautet:

| Betriebssystem | Pfad |
| --- | --- |
| Windows Vista | C:\Users\Public\Documents\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows XP | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems \MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2000 | C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 7 | C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2003 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7\Datenbank\Magellan7.fdb |
| Windows 2008 | C:\ProgramData\Documents\Stueber Systems\MAGELLAN 7 Datenbank\Magellan7.fdb |

!!! warning "Wichtig"

	Nach einer Neuinstallation einer Server-/Einzelplatzinstallation liegen im Verzeichnis Datenbank eine leere Datenbank (MAGELLAN7.fdb) und eine Beispieldatenbank (MAGELLAN7_Beispiel.fdb). Wenn Sie MAGELLAN gern testen möchten, verweisen Sie bitte auf die Beispieldatenbank. Wenn Sie Ihre Daten gern importieren möchten oder aus Ihrer MAGELLAN6.fdb übernehmen möchten, verweisen Sie bitte auf die MAGELLAN7.fdb. Eine Anleitung zur Datenübernahme von MAGELLAN 6 nach MAGELLAN 7 finden Sie im Abschnitt ["Daten aus MAGELLAN 6 nach MAGELLAN 7 übernehmen"](https://doc.magellan7.stueber.de/schulverwaltung/installation/umstieg-von-6-auf-7/#daten-aus-magellan-6-nach-magellan-7-%C3%BCbernehmen).

Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der oben gezeigten Datenbankpfade zu.

Im folgenden Bild werden die Verzeichnisse der Datenordner abgefragt. Die Datenordner (Berichte, Skripte, Vorlagen usw.) werden bei der Installation des Serverrechners oder der Einzelplatzinstallation angelegt. Sie verweisen in diesem Fenster auf den Speicherort der Verzeichnisse, die alle gemeinsam an einer Stelle abgelegt wurden. Um sich Tipparbeit zu sparen, können Sie in der oberen Zeile den Wurzelpfad eingeben und auf das Startdreieck klicken, die nachfolgenden Zeilen werden dann entsprechend mit diesem Pfad und dem Standardnamen des Verzeichnisses befüllt.

![Daten für entfernte Datenordner](/assets/images/welcome-remote-datafolder.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul MAGELLAN ADMINISTRATOR auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. Bitte geben Sie den Netzwerkpfad zu Ihrem Server aus Sicht Ihres Rechners ein!

!!! info "Hinweis"

	Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul MAGELLAN ADMINISTRATOR auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/welcome-remote-backup.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](/assets/images/Welcome-erste-schritte.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort „masterkey“ ein.

![Abschluss des Willkommens-Assistenten](/assets/images/anmeldung.png)

## Einstellungen vom Arbeitsplatz kopieren

Die im Willkommensassistenten eingegebenen Daten werden als Dateien auf dem Arbeitsplatz gespeichert. 

Bevor Sie diese Dateien für einen weiteren Rechner kopieren und weiterverwenden, sollten Sie kurz testen, ob Ihre Eingaben korrekt waren. 

!!! info "Hinweis"

	Die zu kopierenden Dateien unterscheiden sich hinsichtlich der Pfadangaben zwischen einer Server-/Einzelplatzinstallation und einem Arbeitsplatzrechner. Sie können also nur die Dateien des Arbeitsplatzrechners für einen weiteren Arbeitsplatzrechner verwenden.

Melden Sie sich bitte an MAGELLAN an, wenn Sie MAGELLAN erstmalig einsetzen sollten der Benutzer "sysdba" und das Standardpasswort "masterkey" funktionieren. 
Öffnet sich MAGELLAN? Dann stimmt der Pfad zur Datenbank.
Um zu schauen, ob auch die Pfade zu den Datenordner korrekt waren, testen Sie bitte am Beispiel des Berichte-Ordners.
Wechseln Sie bitte ins Menü `Schüler`, wählen eine Schüler, klicken auf `Drucken > Berichte`. Wird eine Liste von Dateien mit der Endung *.rpt gezeigt? Dann können wir davon ausgehen, dass auch die Pfade zu den Verzeichnissen stimmen.  

Öffnen Sie bitte auf dem Rechner den Pfad `C:\ProgramData\Stueber Systems\Magellan 7`. Sollten Sie das Verzeichnis `ProgramData` nicht sehen, kopieren Sie den oben genannten Pfad, fügen ihn in die Adressleiste eines beliebigen Ordnerfensters ein und drücken Enter.
Sie sollten im korrekten Verzeichnis landen: 

![`C:\ProgramData\Stueber Systems\Magellan 7`](/assets/images/installation/programdata.png)

Kopieren Sie bitte die Dateien (MAGELLAN.evm, MAGELLAN.lic, MAGELLAN.opt) auf ein Netzwerkverzeichnis, einen Stick o.ä. und wechseln auf den einzurichtenden Rechner.
Installieren Sie auf dem anderen Rechner bitte MAGELLAN als Arbeitsplatzinstallation und fügen anschließend an der identischen Stelle (die Verzeichnisstruktur wird durch die Installation angelegt) die drei Dateien wieder ein, fertig!