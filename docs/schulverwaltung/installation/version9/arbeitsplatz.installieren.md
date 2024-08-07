﻿
# Arbeitsplatzinstallation

Die Einrichtung eines Arbeitsplatzes unterscheidet sich von der Einrichtung des Serverrechners, da hier nur Magellan und die Runtimeversion von Crystal Reports als Programme installiert werden, die gemeinschaftlich verwendeten Bestandteile wie die Datenbank oder Berichte, Skripte usw. sind bereits auf dem Server vorhanden, es wird in einem späteren Schritt dann darauf verwiesen.

## Vorbereitung

### Downloads

Für den Serverrechner benötigen Sie die Installationsdateien für:

* die Runtimeversion von Crystal Reports 32- oder 64-Bit
* für Magellan 32- oder 64-Bit

**Nutzen Sie ein 32-Bit oder 64-Bit-Betriebssystem?**

1. Wählen Sie `Start > Einstellungen > System > Info` aus.
2. Unter `Gerätespezifikationen > Systemtyp` sehen Sie, ob Sie eine 32-Bit-Version oder eine 64-Bit-Version von Windows verwenden.

!!! danger "Wichtig!"

    Alle Installationspakete finden Sie [in unserem Downloadbereich](https://magellan.stueber.de/download.php).<br/>**Für Windows 32-Bit und 64-Bit gibt es gesonderte Installationsdateien für Magellan und für die Runtimeversion von Crystal Reports.**

### Lizenzdaten

Legen Sie sich bitte die Lizenzdatei (*.lic) so zurecht, dass Sie vom Server darauf zugreifen können. 
Die Datei wurde Ihnen als Test- oder Volllizenz von unserem Office-Team per Mail zugesandt. Sollte Ihnen die Lizenzdatei noch fehlen, können Sie sie per Mail an office@stueber.de neu anfragen. Für eine Volllizenz bitten wir um die Angabe der Kundennummer, herzlichen Dank!

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

## Installation von Magellan

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan9.msi`.

Der Setup Assistent von Magellan 9 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/installation/9/009.png)

Wählen Sie die `Arbeitsplatzinstallation` aus!<br/>Es wird nur das Programm installiert, es werden keine Datenbank abgelegt oder Datenordner (für Berichte, Skripte usw.) erzeugt.

![Installationart festlegen](/assets/images/installation/9/010.png)

Der Assistent schlägt Ihnen einen Installationspfad vor, wir empfehlen diese Auswahl mit `Weiter` zu übernehmen.

![Installationspfad](/assets/images/installation/9/011.png)

Die Vorbereitungen sind abgeschlossen, klicken Sie auf `Weiter` um die Installation auszuführen.

![Vorbereitung abgeschlossen](/assets/images/installation/9/014.png)

![Fortschrittsbalken](/assets/images/installation/9/015.png)

Die Installation ist abgeschlossen, bitte klicken Sie auf `Fertigstellen`!

![Die Installation ist abgeschlossen.](/assets/images/installation/9/016.png)

## Der Willkommensassistent

Nach Beenden des Setup Assistenten müssen Sie Magellan 9 starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/installation/9/welcome.png)

Klicken Sie auf „Weiter“. Um Magellan starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["Magellan 9 - Erste Schritte"](https://doc.kb.stueber.de/magellan/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/installation/9/welcome-license-type.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/installation/9/welcome-enter-license.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/installation/9/welcome-region.png)

Wählen Sie „Entfernte Datenbank“.

![Wahl der Datenbank](/assets/images/installation/9/welcome-database.png)

Sie werden zur Eingabe des Servernamens und des Datenbank-Pfads aufgefordert.
Geben Sie unter `Server` den **Servernamen bzw. die IP-Adresse Ihres Servers** ein, auf dem sich die Magellan 9 Datenbank befindet. Im unteren Feld geben Sie den lokalen Serverpfad (aus Sicht des Servers) zur Magellan 9 Datenbank an.

!!! info "Hinweis"

	Der einzutragende Pfad unterscheidet sich zwischen dem Serverrechner und dem Arbeitsplatzrechner nicht, der Unterschied besteht lediglich beim Eintrag im Feld `Server`.

![Daten für entfernte Datenbank](/assets/images/installation/9/welcome-remote-database.png)

Der standardmäßige Pfad zur Magellan 9 Datenbank lautet:

| Betriebssystem | Pfad |
| --- | --- |
| Windows 8/10/11 | C:\Users\Public\Documents\Stueber Systems\Magellan 9\Datenbank\Magellan9.FDB |

!!! warning "Wichtig"

	Nach einer Neuinstallation einer Server-/Einzelplatzinstallation liegen im Verzeichnis Datenbank eine leere Datenbank (Magellan9.FDB) und eine Beispieldatenbank (Magellan9_Beispiel.FDB). Wenn Sie Magellan gern testen möchten, verweisen Sie bitte auf die Beispieldatenbank. Wenn Sie Ihre Daten gern importieren möchten oder aus Ihrer MAGELLAN6.FDB übernehmen möchten, verweisen Sie bitte auf die Magellan9.FDB. Eine Anleitung zur Datenübernahme von Magellan 7 nach Magellan 9 finden Sie im Abschnitt ["Daten aus Magellan 6 nach Magellan 7 übernehmen"](https://doc.Magellan7.stueber.de/schulverwaltung/update/umstieg-von-8-auf-9/).

Die Pfade sind exemplarisch für die deutschen Versionen der Betriebssysteme und können je nach Sprache und Ausgabe des Betriebssystems variieren. Wenn Sie die Originaleinstellungen während der Installation beibehalten haben, trifft einer der oben gezeigten Datenbankpfade zu.

Im folgenden Bild werden die Verzeichnisse der Datenordner abgefragt. Die Datenordner (Berichte, Skripte, Vorlagen usw.) werden bei der Installation des Serverrechners oder der Einzelplatzinstallation angelegt. Sie verweisen in diesem Fenster auf den Speicherort der Verzeichnisse, die alle gemeinsam an einer Stelle abgelegt wurden. 
Um sich Tipparbeit zu sparen, können Sie in der oberen Zeile den Wurzelpfad eingeben und auf das Startdreieck klicken, die nachfolgenden Zeilen werden dann entsprechend mit diesem Pfad und dem Standardnamen des Verzeichnisses befüllt.

![Daten für entfernte Datenordner](/assets/images/installation/9/welcome-remote-datafolder.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul Magellan Administrator auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. Bitte geben Sie den Netzwerkpfad zu Ihrem Server aus Sicht Ihres Rechners ein!

!!! info "Hinweis"

	Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul Magellan Administrator auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/9/welcome-remote-backup.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in Magellan](/assets/images/installation/9/welcome-erste-schritte.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von Magellan. Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort „masterkey“ ein.

![Abschluss des Willkommens-Assistenten](/assets/images/installation/9/anmeldung.png)

## Einstellungen vom Arbeitsplatz kopieren

Die im Willkommensassistenten eingegebenen Daten werden als Dateien auf dem Arbeitsplatz gespeichert.

Bevor Sie diese Dateien für einen weiteren Rechner kopieren und weiterverwenden, sollten Sie kurz testen, ob Ihre Eingaben korrekt waren.

!!! info "Hinweis"

	Die zu kopierenden Dateien unterscheiden sich hinsichtlich der Pfadangaben zwischen einer Server-/Einzelplatzinstallation und einem Arbeitsplatzrechner. Sie können also nur die Dateien des Arbeitsplatzrechners für einen weiteren Arbeitsplatzrechner verwenden.

Melden Sie sich bitte an Magellan an, wenn Sie Magellan erstmalig einsetzen sollten der Benutzer "sysdba" und das Standardpasswort "masterkey" funktionieren.
Öffnet sich Magellan? Dann stimmt der Pfad zur Datenbank.
Um zu schauen, ob auch die Pfade zu den Datenordner korrekt waren, testen Sie bitte am Beispiel des Berichte-Ordners.
Wechseln Sie bitte ins Menü `Schüler`, wählen eine Schüler, klicken auf `Drucken > Berichte`. Wird eine Liste von Dateien mit der Endung *.rpt gezeigt? Dann können wir davon ausgehen, dass auch die Pfade zu den Verzeichnissen stimmen.  

Öffnen Sie bitte auf dem Rechner den Pfad `C:\ProgramData\Stueber Systems\Magellan 9`. Sollten Sie das Verzeichnis `ProgramData` nicht sehen, kopieren Sie den oben genannten Pfad, fügen ihn in die Adressleiste eines beliebigen Ordnerfensters ein und drücken Enter.
Sie sollten im korrekten Verzeichnis landen:

![`C:\ProgramData\Stueber Systems\Magellan 9`](/assets/images/installation/9/programdata.png)

Kopieren Sie bitte die Dateien (Magellan.evm, Magellan.lic, Magellan.opt) auf ein Netzwerkverzeichnis, einen Stick o.ä. und wechseln auf den einzurichtenden Rechner.
Installieren Sie auf dem anderen Rechner bitte Magellan als Arbeitsplatzinstallation und fügen anschließend an der identischen Stelle (die Verzeichnisstruktur wird durch die Installation angelegt) die drei Dateien wieder ein, fertig!
