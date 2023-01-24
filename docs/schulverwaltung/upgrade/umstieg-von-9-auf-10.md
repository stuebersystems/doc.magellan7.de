# Umstieg von MAGELLAN 9 auf MAGELLAN 10

**Dieses Kapitel wird gerade angepasst!!!**

Folgende Punkte müssen erledigt werden um Ihre MAGELLAN 9 Version auf MAGELLAN 10 zu aktualisieren. 

!!! tipp "Benötigen Sie unsere Unterstützung?"
        Bitte melden Sie sich unter [office@stueber.de](office@stueber.de) und nennen Ihre Ausgangsversion, wir erstellen Ihnen eine Umstiegsangebot und vereinbaren für die Umstellung per Fernwartung einen Termin mit Ihnen. Wir stellen Ihren Serverrechner um, richten einen Client ein und konfigurieren und testen die Verbindung. Für weitere Clients geben wir Ihnen eine kurze Handlungsanweisung.

Nr.|Was ist zu tun
--|--
 1.|[Downloads, Lizenzdatei zurechtlegen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#downloads-lizenzdatei-zurechtlegen)
 2.|E-Mail-Adressen nachpflegen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#2-e-mail-adressen-nachpflegen)
 3.|[Sicherung der Datenbank unter MAGELLAN 9/Firebird 2.5.9](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#3-sicherung-der-datenbank-unter-firebird-259)
 4.|[Deinstallation von Firebird 2.5.9 und `MAGELMAG 9`]()
 5.|[Installation von Firebird 4.0.2, `MAGELLAN 10`, CR Runtimeversion]()
 6.|[Willkommensassistent starten (Pfade und Lizenz)](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#6-willkommensassistent-starten-pfade-und-lizenz)
 7.|[Wiederherstellung der MAGELLAN9.fbk](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#7-wiederherstellung-der-magellan9fbk)
 8.|[Einfügen der wiederhergestellten MAGELLAN10.fdb](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#8-einfugen-der-wiederhergestellten-magellan10fdb)
 9.|[Start von MAGELLAN 10 und Anpassung der Datenstruktur](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#9-start-von-magellan-10-und-anpassung-der-datenstruktur)
10.|[E-Mail-Adressen übernehmen]()
11.|[Kennworte neu erzeugen lassen](E-Mail-Adressen übernehmen)
12.|[Zugriffsrechte synchronisieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#12-zugriffsrechte-synchronisieren)
13.|[Eigene Daten übernehmen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#13-eigene-daten-ubernehmen)
14.|[Arbeitsplatzrechner](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-9-auf-10/#14-arbeitsplatzrechner)

## 1. Downloads, Lizenzdatei zurechtlegen

Bitte stellen Sie sicher, dass Ihnen die neue Lizenzdatei vorliegt, ggfs. können Sie die Datei auch unter office@stueber.de erneut anfordern.

Für die folgenden Schritte benötigen Sie die Installationspakete für:

* Firebird 4.0.2 (32 Bit)
* MAGELLAN 10 (32 oder 64 Bit)
* CR Runtimeversion (32 oder 64 Bit)

Alle Installationsdateien stellen wir Ihnen in unserem Downloadbereich unter [https://magellan.stueber.de/download.php](https://magellan.stueber.de/download.php).

## 2. E-Mail-Adressen nachpflegen

Beim Umstieg von Firebird 2.5.9 auf Firebird 4.0.2 können nicht die bisher für die MAGELLAN-Anmeldung verwendeten Passworte übertragen werden. Hintergrund sind unterschiedliche Verschlüsselungstechnik der Passwortdatenbanken (security2.fdb und security4.fdb) der beiden Versionen. Die Benutzer selbst und Ihre zugewiesenen Rechte werden in der MAGELLAN-Datenbank gespeichert und stellen damit kein Problem dar.
Für MAGELLAN 10 müssen für alle Benutzer neue Passworte gesetzt werden, wir stellen dafür eine Funktion zur Verfügung, die zufällige Passworte für alle in der Benutzerverwaltung markierten Benutzer generiert. In dem Moment des Erzeugens können wir diese Passworte zusammen mit der Benutzerkennung und - falls vorhanden- einer Emailadresse (beispielsweise als Vorlage für eine Serienmail) in eine CSV-Datei ausgeben.
Die Emailadressen können mit einer neuen Funktion aus `MAGELLAN > Lehrer > Daten 1 > E-Mail` übernommen werden. Für Benutzer, die nicht mit einem Lehrer aus MAGELLAN verbunden sind, kann direkt im MAGELLAN Administrator eine E-Mailadresse hinterlegt werden.
Wenn Sie die neu zu erzeugenden Passworte per Mail verteilen möchten, kontrollieren Sie bitte in MAGELLAN (auch schon vorab in Version 9 möglich) ob die Adressen entsprechend gefüllt sind. Für einen schnellen Überblick können Sie die Spalte `E-Mail` in der Auswahlliste `Lehrer` nutzen.

## 3. Sicherung der Datenbank unter Firebird 2.5.9

Bevor die neue Firebirdversion installiert wird, erstellen Sie bitte eine Sicherung der MAGELLAN-Datenbank mit dem MAGELLAN 9 Administrator. Aus dieser Datenbank wird später mit Firebird 4.0.2 und dem MAGELLAN 10 Administrator die neue Datenbank wieder hergestellt.
Eine Anleitung zum Sichern der Datenbank finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/admin/sicherung/).

## 4. Deinstallation von Firebird 2.5.9 und MAGELMAG 9

Öffnen Sie auf Ihrem Serverrechner den Punkt `Systemsteuerung > Programme und Features` und deinstallieren bitte Firebird 2.5.9 und `MAGELLAN 9`vollständig.

## 5. Installationen

### 5.1. Firebird 4.0.2

!!! warning "Wichtig"

	Diese Installation wird einmalig im Netzwerk auf dem Rechner, auf dem später Ihre MAGELLAN-Datenbank liegen wird ausgeführt. 

Laden Sie bitte das Firebird-Installationspaket von unseren Webseiten oder unter [folgendem Link](https://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei `Firebird-4.0.2.....-Win32`.

Die Installationsschritte im Einzelnen:

Wählen Sie bitte "English" und klicken auf `OK`!

[00]:/assets/images/installation/10/fb/00.png "Text"
![][00]

Stimmen Sie der Lizenzvereinbarung bitte zu (I accept the agreement) und klicken auf "Next"!

![](/assets/images/installation/10/fb/01.png)

Klicken Sie bitte auf "Next"!

![](/assets/images/installation/10/fb/03.png)

Bitte übernehmen Sie den voreingestellten Installationspfad!

[04]:/assets/images/installation/10/fb/04.png "Text"
![][04]

Bitte übernehmen Sie den voreingestellten Optionen!

[05]:/assets/images/installation/10/fb/05.png "Text"
![][05]

Bitte übernehmen Sie den voreingestellten Menüordner und klicken auf `Next`!

[06]:/assets/images/installation/10/fb/06.png "Text"
![][06]

Bitte übernehmen Sie die dargestellten Optionen und klicken auf `Next`!

[07]:/assets/images/installation/10/fb/07.png "Text"
![][07]

!!! warning "Wichtig!"

    Vergeben Sie ein 8-stelliges Passwort für den Benutzer `sysdba`. **Bitte stellen Sie sicher, dass dieses Passwort gesichert wird, beispielsweise in einem Passwortmanager.**
    Dieser Benutzer hat die höchsten administrativen Rechte und kann für die Erstanmeldung an MAGELLAN verwendet werden, bevor personalisierte Benutzerzugänge verwendet werden.

[08]:/assets/images/installation/10/fb/08.png "Text"
![][08]

Starten Sie die Installation über die Schaltfläche `Install`!

[09]:/assets/images/installation/10/fb/09.png "Text"
![][09]

[10]:/assets/images/installation/10/fb/10.png "Text"
![][10]

Die Installation ist abschlossen, bitte klicken Sie auf `Next`!

[11]:/assets/images/installation/10/fb/11.png "Text"
![][11]

Bitte lassen Sie mindestens das Häkchen vor `Start Firebird Service now?` aktiviert um den Firebird-Dienst zu starten!

[12]:/assets/images/installation/10/fb/12.png "Text"
![][12]

### 5.2. Crystal Reports Runtimeversion

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

### 5.3. MAGELLAN 10

Starten Sie anschließend die Installation per Doppelklick auf die Datei `Magellan10.msi`.

Der Setup Assistent von MAGELLAN 10 wird gestartet und die Installationsdateien werden entpackt.

![Startdialog der Installation](/assets/images/installation/10/001.png)

Wählen Sie die `Server-/Einzelplatzinstallation` aus! <br/>Es wird das Programm installiert, zusätzlich wird die Datenbank abgelegt und es werden die Datenordner (Skripte, Berichte usw.) erzeugt. In den Datenordnern befinden sich alle Bestandteile auf die die Nutzer später gemeinsam zugreifen können, zum Beispiel Bericht, Seriendruckvorlagen, Skripte usw.

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

## 6. Willkommensassistent starten (Pfade und Lizenz)

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

Bei einer Server-/Einzelplatzinstallation sind die Pfade für die Datenordner, die Datenbank und den Server schon korrekt durch Ihre Angaben während der MAGELLAN-Installation vorbefüllt, bitte ändern Sie hier nichts. 

![Lokale Datenbank](/assets/images/installation/10/w/005.1.png)

Es wird standardmäßig auf eine Beispieldatenbank verwiesen, in der für erste Tests bereits Daten vorbereitet sind. Wenn Sie mit einer leeren Datenbank beginnen möchten, ändern Sie lediglich die Bezeichnung der Datenbank. Beide Datenbankvarianten wurden bei der Installation von MAGELLAN abgelegt.
<br/> Leere Datenbank: `Magellan10.fdb`
<br/> Beispieldatenbank: `Magellan10_Beispiel.fdb`

![Datenbankpfad](/assets/images/installation/10/w/005.2.png)

Für die Verbindungsinformationen geben Sie jetzt bitte noch einen Standardablageort für zukünftige Sicherungen an. Eine Sicherung Ihrer Datenbank kann über das Modul MAGELLAN ADMINISTRATOR auch von einer Arbeitsplatzinstallation aus ausgelöst werden, allerdings wird die Sicherung immer auf dem Rechner erstellt werden, auf die Datenbank sich befindet - das sollte Ihr Serverrechner sein. 

!!! info "Hinweis"

    Sollten Sie andere Speicherorte wünschen, stellen Sie bitte sicher, dass die Zielverzeichnisse auch existieren. Die Sicherung der Datenbank oder auch das Wiederherstellen einer neuen Datenbank aus einer Sicherungskopie können Sie über das Modul MAGELLAN ADMINISTRATOR auslösen.

![Einstellungen für Backup und Restore Ihrer Datenbank](/assets/images/installation/10/w/007.png)

Bestätigen Sie mit "Weiter", es erscheint eine Informationsseite, die Ihnen kurz die Schritte aufzeigt, die von der Datenbank mit Beispieldaten zu einer Datenbank mit Realdaten führen.

![Erste Schritte in MAGELLAN](/assets/images/installation/10/w/008.png)

Bestätigen Sie mit „Weiter“, es erscheint das Anmeldefenster von MAGELLAN. 
Geben Sie im Anmeldedialog bei Benutzer „sysdba“ und als Kennwort Ihr Passwort ein, dass Sie während der Firebird-Installation gewählt haben. Die Einrichtung Ihres Servers oder Ihres Arbeitsplatzes ist fertig!

![Abschluss des Willkommens-Assistenten](/assets/images/installation/10/w/009.png)

## 7. Wiederherstellung der MAGELLAN9.fbk

Starten Sie den `MAGELLAN 10 Administrator` und stellen die zuvor gesicherte Datenbank wieder her, eine Anleitung für das Wiederherstellen finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/admin/sicherung/#sicherungskopie-wiederherstellen).

## 8. Einfügen der wiederhergestellten MAGELLAN10.fdb

Die wiederhergestellte Datenbank legen Sie bitte im Datenbankverzeichnis von `MAGELLAN 10` ab. An welcher Stelle die Datenbank erwartet wird und welcher Dateiname für die Datenbank erwartet wird, ist in den Verbindungseinstellungen festgelegt worden, die Sie in der Installation und/oder im Willkommensassistenten festgelegt haben. 
Die Daten sind änder- und einsehbar. Bitte starten Sie den `MAGELLAN 10 Administrator`  ohne Anmeldung (im Anmeldefenster unter `Datenbank` auswählbar) und klicken doppelt auf die Zeile Ihrer Verbindung, die Sie unter dem Punkt `Datenbankverbindungen` finden. Im folgenden Fenster ist der Pfad zur Datenbank und der erwartete Name der Datenbankdatei unter dem Punkt `Datenbank` sichtbar.

## 9. Start von MAGELLAN 10 und Anpassung der Datenstruktur

Starten Sie `MAGELLAN 10` und melden sich mit dem Benutzer `sysdba` und dem von Ihnen vergebenen Passwort an. Der Assistent fordert Sie auf eine Sicherung der Datenbank zu erstellen, im Anschluss wird die Strukturanpassung der Datenbank auf die aktuelle Version vorgenommen. 

## 10. E-Mail-Adressen übernehmen

E-Mailadressen, die Sie für `Lehrer` unter `Daten 1 > E-Mail` verfasst haben, können Sie in den `MAGELLAN 10 Administrator` übernehmen. Diese Adressen werden beim gesammelten Erstellen von Passworten gemeinsam mit den Passworten und den Benutzerkennungen in eine CSV-Datei gespielt werden und dann ggfs. zum Versenden verwendet werden.
Rufen Sie die Funktion unter `Benutzerverwaltung > Extras > E-Mail übernehmen` auf. Der Assistent übernimmt die Adressen. Sie finden die übernommenen Adressen in der Liste der Benutzerverwaltung. 

![Emails übernehmen](/assets/images/upgrade/10/001.png)

![Emails in der Benutzerliste](/assets/images/upgrade/10/002.png)

Für Benutzer, die nicht auf einen Lehrerdatensatz aus MAGELLAN basieren, können Sie die Adresse per Doppelklick auf den Datensatz erfassen.

![Emails für weitere Nutzer erfassen](/assets/images/upgrade/10/003.png)

## 11. Kennworte neu erzeugen lassen

Bedingt durch den Wechsel der Firebird-Versionen müssen allen Nutzern neue Kennworte zugewiesen werden. Dazu markieren Sie bitte alle Benutzer in der `Benutzerverwaltung` und führen den Assistenten aus, den Sie unter `Benutzerverwaltung > Extras > Kennwörter erzeugen` aufrufen können. Als Ergebnis wird eine CSV-Datei erzeugt, die die Kennungen, die Passworte und, falls gefüllt, die Emailadressen der Benutzer enthalten.

![Emails für weitere Nutzer erfassen](/assets/images/upgrade/10/004.png)

## 12. Zugriffsrechte synchronisieren

Um die Rechte der existierenden Benutzer auf für die neuen Datenbankstrukturteile anzupassen, führen Sie bitte den Punkt `Benutzerverwaltung > Start > Zugriffsrechte synchronisieren` aus.

![Emails für weitere Nutzer erfassen](/assets/images/upgrade/10/005.png)

## 13. Eigene Daten übernehmen

Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese bitte und legen Sie in der neuen Verzeichnisstruktur von MAGELLAN 10 ab.

!!! warning "Wichtig"

    Bitte legen Sie **nur Ihre zusätzlichen Dateien** in der neuen Verzeichnisstruktur ab und ersetzen Sie bitte nicht die Verzeichnisse! 

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil MAGELLAN 10 hier beispielsweise einen anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Ja| Bitte je Unterverzeichnis nur Ihre selbsterstellten oder angepassten Berichte übernehmen, bitte nicht den gesamten Ordnerinhalt oder ganze Ordner übertragen, Sie überschreiben sich ansonsten ggfs. aktuellere Varianten.
Datenbank|Ja| Bitte beachten Sie hier die Anleitung zum Sichern der Datenbank mit `MAGELLAN 9` und Firebird 2.5. und zum Wiederherstellen mit `MAGELLAN 10` und Firebird 4.0.2.
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für MAGELLAN 10 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von `MAGELLAN 10` und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Sollten Sie eigene angepasste oder selbsterstellte Skripte einsezten, können Sie diese Dateien in der neuen Struktur ablegen.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für `MAGELLAN 10` ab.

## 14. Arbeitsplatzrechner 

!!! warning "Wichtig"

    Bitte deinstallieren Sie `MAGELLAN 9` auf den Arbeitsplätzen.

Zur Installation und Konfiguration von `MAGELLAN 10` und der Crystal Reports Runtimeversion folgen Sie bitte unserer Anleitung für [Arbeitsplätze](https://doc.magellan.stueber.de/schulverwaltung/installation/version10/arbeitsplatz.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von `MAGELLAN 10`, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

### Empfehlung für weitere Arbeitspltze

Wir empfehlen Ihnen MAGELLAN auf einem Arbeitsplatz zu installieren, zu lizenzieren und zu konfigurieren. Die Lizenzdaten und die Konfigurationsdaten können anschließend zentral abgelegt werden. Somit wäre ab dem zweiten Arbeitsplatz nur die Installation notwendig und Sie legen zusätzlich eine Datei ab, die die Pfade enthält, von denen MAGELLAN die Lizenz- und Konfigurationdaten lesen soll.

Nach der Installation auf dem ersten Arbeitsplatz starten Sie bitte MAGELLAN 10 um den Willkommens-Assistenten zu durchlaufen. Im Willkommensassistenten gibt man die Lizenzdaten, die Pfade aus Sicht des Arbeitsplatzs zur Datenbank und zu den Datenordnern ein, wählt eine Option für die Region. Diese Eingaben werden in Dateiform gespeichert und können auch für weitere Clients genutzt werden.

Testen Sie anschließend auf dem ersten Arbeitsplatz, ob die Angaben korrekt waren.<br/>
**Test 1 (Datenbankpfad):** Dafür starten Sie MAGELLAN auf dem Rechner, gelingt der Start des Moduls, ist der Pfad zur Datenbank ok.<br/>
**Test 2 (Datenordnerpfade):** In MAGELLAN wechseln Sie in das Menü Schüler, markieren einen Schüler und drücken bitte STRG+P. Werden Schülerberichte zur Auswahl gezeigt, sind die Pfade zu den Datenordnern ok.

Die durch den Willkommens-Assistenten erzeugten Dateien, aus den die Lizenz, die Optionen und die Pfade ausgelesen werden, finden Sie unter `C:\ProgramData\Stueber Systems\Magellan 10`. Diese Dateien können Sie zentral ablegen und von allen Arbeitsplätzen aus nutzen. Damit beim Programmstart von MAGELLAN nicht die lokalen Daten ausgelesen werden, sondern die zentral abgelegten Dateien gelesen werden, muss eine Textdatei mit den Pfaden und einem bestimmten Namen angelegt und an einer bestimmten Stelle abgelegt werden. Bitte folgen Sie hierfür unserer Anleitung unter: [Die Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).

Die erzeugte Datei legen Sie auf allen anderen Arbeitsplätzen (nicht auf dem Server!) nach der Installation bitte unter `C:\Program Files (x86)\Stueber Systems\Magellan 10` ab. Damit entfallen weitere Schritte zur Lizenzierung und Konfiguration.
