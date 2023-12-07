# Umstieg von MAGELLAN 10 auf MAGELLAN 11

**Die Anleitung ist aktuell in Vorbereitung. <br/>MAGELLAN 11 erscheint voraussichtlich im 1. Quartal 2024**

Folgende Punkte müssen erledigt werden um Ihre MAGELLAN 10 Version auf MAGELLAN 11 zu aktualisieren.

!!! tipp "Benötigen Sie unsere Unterstützung?"
        Bitte melden Sie sich unter [office@stueber.de](office@stueber.de) und nennen Ihre Ausgangsversion, wir erstellen Ihnen eine Umstiegsangebot und vereinbaren für die Umstellung per Fernwartung einen Termin mit Ihnen. Wir stellen Ihren Serverrechner um, richten einen Client ein und konfigurieren und testen die Verbindung. Für weitere Clients geben wir Ihnen eine kurze Handlungsanweisung.

Nr.|Was ist zu tun
--|--
 1.|[Downloads, Lizenzdatei zurechtlegen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#1-downloads-lizenzdatei-zurechtlegen)
 2.|Installation von [`MAGELLAN 11`](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#22-magellan-11) und der [CR Runtimeversion](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#21-crystal-reports-runtimeversion)
 3.|[Willkommensassistent starten (Pfade und Lizenz)](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#3-willkommensassistent-starten-pfade-und-lizenz)
 4.|[Übernahme der MAGELLAN10.fdb](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#4-ubernahme-der-magellan10fdb)
 5.|[Anpassen auf die neue Datenstruktur](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#5-anpassen-auf-die-neue-datenstruktur)
 6.|[Zugriffsrechte synchronisieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#6-zugriffsrechte-synchronisieren)
 7.|[Eigene Daten übernehmen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#7-eigene-daten-ubernehmen)
 8.|[Arbeitsplatzrechner einrichten](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#14-arbeitsplatzrechner-einrichten)

## 1. Downloads, Lizenzdatei zurechtlegen

Bitte stellen Sie sicher, dass Ihnen die neue Lizenzdatei vorliegt, ggfs. können Sie die Datei auch unter [office@stueber.de](office@stueber.de) erneut anfordern.

Für die folgenden Schritte benötigen Sie die Installationspakete für:

* MAGELLAN 11 (32 oder 64 Bit)
* CR Runtimeversion (32 oder 64 Bit)

Alle Installationsdateien stellen wir Ihnen in unserem Downloadbereich unter [https://magellan.stueber.de/download.php](https://magellan.stueber.de/download.php).

## 2. Installationen

### 2.1 Crystal Reports Runtimeversion

Nr.|Was ist zu tun
--|--
 1.|[Downloads, Lizenzdatei zurechtlegen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#1-downloads-lizenzdatei-zurechtlegen)
 2.|Installation von [`MAGELLAN 11`](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#22-magellan-11) und der [CR Runtimeversion](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#21-crystal-reports-runtimeversion)
 3.|[Willkommensassistent starten (Pfade und Lizenz)](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#3-willkommensassistent-starten-pfade-und-lizenz)
 4.|[Übernahme der MAGELLAN10.fdb](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#4-ubernahme-der-magellan10fdb)
 5.|[Anpassen auf die neue Datenstruktur](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#5-anpassen-auf-die-neue-datenstruktur)
 6.|[Zugriffsrechte synchronisieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#6-zugriffsrechte-synchronisieren)
 7.|[Eigene Daten übernehmen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#7-eigene-daten-ubernehmen)
 8.|[Arbeitsplatzrechner einrichten](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#14-arbeitsplatzrechner-einrichten)


Diese Installation muss stets parallel zur MAGELLAN Installation erfolgen, diese Bestandteile sind die Voraussetzung für die Druckfunktionalitäten in MAGELLAN.

Starten Sie die Installation per Doppelklick auf das msi-Paket. Klicken Sie bitte auf `Next` im Installationsassistenten.

![Willkommen](/assets/images/installation/11/cr/004.png)

Stimmen Sie bitte dem "License Agreement" zu, indem Sie den oberen Radiobutton wie in der Abbildung aktivieren und auf `Next` klicken

![License Agreement](/assets/images/installation/11/cr/005.png)

Starten Sie die Installation per Klick auf `Next`.

![Start](/assets/images/installation/11/cr/006.png)

Der Fortschritt der Installation wird per Laufbalken gezeigt.

![Installationsfortschritt](/assets/images/installation/11/cr/007.png)

Die Installation ist beendet, bitte klicken Sie auf `Finish`.

![Fertigstellen](/assets/images/installation/11/cr/008.png)

### 2.2. MAGELLAN 11

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan11.msi`.

Der Setup Assistent von `MAGELLAN 11` wird gestartet und die Installationsdateien werden entpackt.

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

## 3. Willkommensassistent starten (Pfade und Lizenz)

Nach Beenden des Setup Assistenten müssen Sie `MAGELLAN 11` starten. Es erscheint zunächst der Willkommen-Assistent.

![Willkommen](/assets/images/installation/11/w/001.png)

Klicken Sie auf „Weiter“. Um MAGELLAN starten zu können, müssen Sie Ihre Lizenzdaten für eine Vollversion oder eine Testlizenz eingeben.
Unten links im Fenster können Sie über den Link ["MAGELLAN - Erste Schritte"](https://doc.kb.stueber.de/magellan/erste-schritte-in-magellan.html) ein Infoblatt aufrufen, dass Ihnen die ersten Schritte von einer Beispieldatenbank zu einer Datenbank mit Ihren Realdaten beschreibt.

![Wahl zwischen Vollversion und Testlizenz](/assets/images/installation/11/w/002.png)

Wählen Sie „Eine Testlizenz anfordern“ und klicken Sie dann auf „Weiter“, wenn Sie noch keine Lizenzdaten besitzen. Die Lizenzdaten können Sie dann mit Hilfe des Assistenten per E-Mail direkt anfordern oder als Textdatei speichern, falls Sie keinen E-Mailzugang besitzen.

Wenn Sie Ihre Lizenzdaten erhalten haben, wählen Sie „Meine Lizenzdaten eingeben“ und klicken Sie dann auf „Weiter“. Tragen Sie nun Ihre Lizenzierung ein. Sollten Sie mit Ihren Lizenzdaten auch eine Lizenzdatei erhalten haben, so können Sie diese alternativ über „Lizenz importieren“ einlesen. Klicken Sie dann auf „Weiter“.

![Eingabe der Lizenzdaten](/assets/images/installation/11/w/003.png)

Wählen Sie hier Ihre Region (Bundesländer, Auslandsschulen, Schweiz oder Deutschland möglich) aus und klicken dann auf „Weiter“.

![Wahl der Region](/assets/images/installation/11/w/004.png)

Bei einer Server-/Einzelplatzinstallation sind die Pfade für die Datenordner, die Datenbank und den Server schon korrekt durch Ihre Angaben während der MAGELLAN-Installation vorbefüllt, bitte ändern Sie hier nichts. 

![Lokale Datenbank](/assets/images/installation/11/w/005.1.png)

Es wird standardmäßig auf eine Beispieldatenbank verwiesen, wir erläutern in nachfolgenden Schritten die Übernahme Ihrer bisherigen `MAGELLAN10.fdb` als `MAGELLAN11.fdb`, bitte wählen Sie daher in diesem Schritt für Ihre Verbindung den Wert `MAGELLAN11.fdb` aus.

![Datenbankpfad](/assets/images/installation/11/w/005.2.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an.   
Eine Sicherung Ihrer Datenbank kann über das Modul MAGELLAN ADMINISTRATOR auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. 

!!! danger "Warnung"

      Sollten Sie andere Speicherorte also vorgeschlagen wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren.<br/>
      Die Sicherung kann später von jedem Rechner aus über das Modul MAGELLAN ADMINISTRATOR gestartet werden, wird aber stets auf dem Rechner erzeugt, auf dem die Datenbank liegt.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/11/w/007.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](/assets/images/installation/11/w/008.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. 
Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort Ihr Passwort ein, dass Sie bereits für MAGELLAN 10 verwendet haben. Es öffnet sich eine leere Magellan-Datenbank, die im nächsten Schritt gegen Ihre Realdatenbank ausgetauscht wird. Bitte schließen Sie MAGELLAN dafür wieder!

![Abschluss des Willkommens-Assistenten](/assets/images/installation/11/w/009.png)

## 4. Übernahme der MAGELLAN10.fdb

1. Stoppen Sie während des Austauschs den Firebird-Dienst unter `Systemsteuerung > Verwaltung > Dienste`! ![Datenbank wiederherstellen](/assets/images/upgrade/10/007.png). 

2. Wechseln Sie in das Verzeichnis `C:\Users\Public\Documents\Stueber Systems\Magellan 11\Datenbank`. In diesem Verzeichnis befindet sich eine leere Datenbank mit der Bezeichung `MAGELLAN11.fdb`, benennen Sie diese in "leere_MAGELLAN11.fdb" um.

3. Kopieren Sie anschließend Ihre `MAGELLAN10.fdb` aus dem bisherigen Datenbankverzeichnis und fügen Sie unter `C:\Users\Public\Documents\Stueber Systems\Magellan 11\Datenbank` als `MAGELLAN11.fdb` wieder ein.

4. Starten Sie bitte den Firebird-Dienst erneut!

## 5. Anpassen auf die neue Datenstruktur

Starten Sie `MAGELLAN 11` und melden sich mit dem Benutzer `sysdba` und dem von Ihnen vergebenen Passwort an. Der Assistent fordert Sie auf eine Sicherung der Datenbank zu erstellen, im Anschluss wird die Strukturanpassung der Datenbank auf die aktuelle Version vorgenommen.

## 6. Zugriffsrechte synchronisieren

Um die Rechte der existierenden Benutzer für die neuen Datenbankstrukturteile anzupassen, führen Sie bitte im MAGELLAN ADMINISTRATOR den Punkt `Benutzerverwaltung > Start > Zugriffsrechte synchronisieren` aus.

![Emails für weitere Nutzer erfassen](/assets/images/upgrade/10/005.png)

## 7. Eigene Daten übernehmen

Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese bitte und legen Sie in der neuen Verzeichnisstruktur von `MAGELLAN 11` ab.

!!! danger "Achtung!"

    Bitte legen Sie **nur Ihre zusätzlichen Dateien** in der neuen Verzeichnisstruktur ab und ersetzen nicht generell Verzeichnisse! 
    Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten **nicht** übernommen werden.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Ja| Bitte je Unterverzeichnis nur Ihre selbsterstellten oder angepassten Berichte übernehmen, bitte nicht den gesamten Ordnerinhalt oder ganze Ordner übertragen, Sie überschreiben sich ansonsten ggfs. aktuellere Varianten.
Datenbank|Ja| Bitte folgen Sie hierfür dem Abschnitt [Übernahme der MAGELLAN10.fdb](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-10-auf-11/#4-ubernahme-der-magellan10fdb).
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für `MAGELLAN 11` ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von `MAGELLAN 11` und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Sollten Sie eigene angepasste oder selbsterstellte Skripte einsetzen, können Sie diese Dateien zusätzlich in der neuen Struktur ablegen.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für `MAGELLAN 11` ab.

## 8. Arbeitsplatzrechner einrichten 

!!! warning "Wichtig"

    Bitte deinstallieren Sie `MAGELLAN 10` auf den Arbeitsplätzen.

Zur Installation und Konfiguration von `MAGELLAN 11` und der Crystal Reports Runtimeversion folgen Sie bitte unserer Anleitung für [Arbeitsplätze](https://doc.magellan.stueber.de/schulverwaltung/installation/version11/arbeitsplatz.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von `MAGELLAN 11`, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

### Einrichten weiterer Arbeitsplätze

Wir empfehlen Ihnen MAGELLAN auf einem Arbeitsplatz zu installieren, zu lizenzieren, zu konfigurieren und einen Funktionstest durchzuführen. Die Lizenzdaten und die Konfigurationsdaten können anschließend zentral abgelegt werden. Somit wäre ab dem zweiten Arbeitsplatz nur die Installation notwendig und Sie legen zusätzlich eine Datei ab, die die Pfade enthält, von denen MAGELLAN die Lizenz- und Konfigurationdaten lesen soll.

Nach der Installation auf dem ersten Arbeitsplatz starten Sie bitte `MAGELLAN 11` um den Willkommens-Assistenten zu durchlaufen. Im Willkommensassistenten gibt man die Lizenzdaten, die Pfade aus Sicht des Arbeitsplatzs zur Datenbank und zu den Datenordnern ein, wählt eine Option für die Region. Diese Eingaben werden in Dateiform gespeichert und können auch für weitere Clients genutzt werden.

#### Test

Testen Sie anschließend auf dem ersten Arbeitsplatz, ob die Angaben korrekt waren.<br/>
**Test 1 (Datenbankpfad):** Dafür starten Sie MAGELLAN auf dem Rechner, gelingt der Start des Moduls, ist der Pfad zur Datenbank ok.<br/>
**Test 2 (Datenordnerpfade):** In MAGELLAN wechseln Sie in das Menü `Schüler`, markieren einen Schüler und drücken bitte STRG+P. Werden Schülerberichte zur Auswahl gezeigt, sind die Pfade zu den Datenordnern ok.

#### Konfigurationsdateien

Die durch den Willkommens-Assistenten erzeugten Dateien, aus den die Lizenz, die Optionen und die Pfade ausgelesen werden, finden Sie unter `C:\ProgramData\Stueber Systems\Magellan 11`. Diese Dateien können Sie zentral ablegen und von allen Arbeitsplätzen aus nutzen. Damit beim Programmstart von MAGELLAN nicht die lokalen Daten ausgelesen werden, sondern die zentral abgelegten Dateien gelesen werden, muss eine Textdatei mit den Pfaden und einem bestimmten Namen angelegt und an einer bestimmten Stelle abgelegt werden. Bitte folgen Sie hierfür unserer Anleitung unter: [Die Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).

Die erzeugte Datei legen Sie auf allen anderen Arbeitsplätzen (nicht auf dem Server!) nach der Installation bitte unter `C:\Program Files (x86)\Stueber Systems\Magellan 11` ab. Damit entfallen weitere Schritte zur Lizenzierung und Konfiguration.
