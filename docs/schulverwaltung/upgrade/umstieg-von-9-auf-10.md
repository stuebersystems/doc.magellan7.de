# Umstieg von MAGELLAN 9 auf MAGELLAN 10

**Dieses Kapitel wird gerade angepasst!!!**

Folgende Punkte müssen erledigt werden um Ihre MAGELLAN 9 Version auf MAGELLAN 10 zu aktualisieren. 

!!! tipp "Benötigen Sie unsere Unterstützung?"
        Bitte melden Sie sich unter [office@stueber.de](office@stueber.de) und nennen Ihre Ausgangsversion, wir erstellen Ihnen eine Umstiegsangebot und vereinbaren für die Umstellung per Fernwartung einen Termin mit Ihnen. Wir stellen Ihren Serverrechner um, richten einen Client ein und konfigurieren und testen die Verbindung. Für weitere Clients geben wir Ihnen eine kurze Handlungsanweisung.

Nr.|Was ist zu tun
--|--
 1.|Downloads, Lizenzdatei zurechtlegen
 2.|Ist MAGELLAN 9 aktuell? [Wenn nicht, dann bitte aktualisieren.](https://doc.magellan.stueber.de/schulverwaltung/update/vorbereitung/)
 3.|ggfs. Lehrer-E-Mailadressen unter `MAGELLAN > Lehrer > Daten 1 > E-Mail` nachpflegen
 4.|Sicherung der Datenbank unter MAGELLAN 9/Firebird 2.5.9
 5.|Installation von Firebird 4.0.2, MAGELLAN 10, CR Runtimeversion
 6.|Willkommensassistent starten (Pfade und Lizenz)
 7.|Wiederherstellung der MAGELLAN9.fbk mit dem MAGELLAN 10/ Firebird 4.0.2
 8.|Einfügen der wiederhergestellten MAGELLAN10.fdb ins Datenbankverzeichnis
 9.|Start von MAGELLAN 10 und Anpassung der Datenstruktur
10.|Admin Emails nachtragen lassen
11.|Kennworte neu erzeugen lassen, ggfs. per Mail verteilen
12.|Zugriffsrechte synchronisieren
13.|Arbeitsplatzrechner aktualisieren (MAGELLAN 10, CR Runtimeversion)

## Downloads, Lizenzdatei zurechtlegen

## Emailadressen nachpflegen

Beim Umstieg von Firebird 2.5.9 auf Firebird 4.0.2 können nicht die bisher für die MAGELLAN-Anmeldung verwendeten Passworte übertragen werden. Hintergrund sind unterschiedliche Verschlüsselungstechnik der Passwortdatenbanken (security2.fdb und security4.fdb) der beiden Versionen. Die Benutzer selbst und Ihre zugewiesenen Rechte werden in der MAGELLAN-Datenbank gespeichert und stellen damit kein Problem dar.
Für MAGELLAN 10 müssen für alle Benutzer neue Passworte gesetzt werden, wir stellen dafür eine Funktion zur Verfügung, die zufällige Passworte für alle in der Benutzerverwaltung markierten Benutzer generiert. In dem Moment des Erzeugens können wir diese Passworte zusammen mit der Benutzerkennung und - falls vorhanden- einer Emailadresse (beispielsweise als Vorlage für eine Serienmail) in eine CSV-Datei ausgeben.
Die Emailadressen können mit einer neuen Funktion aus `MAGELLAN > Lehrer > Daten 1 > E-Mail` übernommen werden. Für Benutzer, die nicht mit einem Lehrer aus MAGELLAN verbunden sind, kann direkt im MAGELLAN Administrator eine E-Mailadresse hinterlegt werden.
Wenn Sie die neu zu erzeugenden Passworte per Mail verteilen möchten, kontrollieren Sie bitte in MAGELLAN (auch schon vorab in Version 9 möglich) ob die Adressen entsprechend gefüllt sind. Für einen schnellen Überblick können Sie die Spalte `E-Mail` in der Auswahlliste `Lehrer` nutzen.





## Auf dem Server

### Ausgangssituation prüfen und aktualisieren

Auf Ihrem **Serverrechner** stellen Sie bitte sicher, dass jeweils die aktuellste Ausgabe von `MAGELLAN 8` und `Firebird 2.5.9` einsetzt wird. Die Versionen auf den Arbeitsplatz müssen nicht aktualisiert werden.

Programm|Version auslesen
--|--
MAGELLAN-Version|Die bei Ihnen eingesetzte Ausgabe von MAGELLAN wird im Programm unter `Hilfe > Info über` gezeigt, die aktuell verfügbare Version können Sie in der [Changelog-Datei](https://doc.magellan.stueber.de/changelog/changelog/) sehen.
Firebird| Auf Ihrem Serverrechner unter `Systemsteuerung > Firebird Server Manager (32 Bit)` wird die Version gezeigt. Sie sollte mit der Version unter [https://magellan.stueber.de/download.php](https://magellan.stueber.de/download.php) gezeigten Version (aktuell 2.5.9) übereinstimmen.

Wenn es hier Abweichungen gibt, aktualisieren Sie bitte im ersten Schritt MAGELLAN und ggfs. Firebird auf Ihrem Serverrechner, Anleitungen finden Sie unter:

* [MAGELLAN-Updateanleitung](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/)
* [Firebird-Updateanleitung](https://doc.magellan.stueber.de/schulverwaltung/update/firebird-aktualisieren/)

### MAGELLAN 9 installieren und lizenzieren

Installieren Sie MAGELLAN 9 auf Ihrem Serverrechner und auf den Arbeitsplätzen.

!!! warning "Wichtig"

    MAGELLAN 8 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unserer Anleitung für die Einrichtung und Lizenzierung des [Servers](https://doc.magellan.stueber.de/schulverwaltung/installation/version9/server.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von MAGELLAN 9, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

### 8er Datenbank übernehmen

Auf Ihrem MAGELLAN-Serverrechner soll im nächsten Schritt die 8er Datenbank übernommen und für MAGELLAN 9 angepasst werden. Führen Sie hierfür bitte die folgenden Schritte aus:

1. Öffnen Sie auf dem Serverrechner bitte `Systemsteuerung > Verwaltung > Dienste` und stoppen dort den Firebird-Dienst.<br/>
![Firebird-Dienst stoppen](/assets/images/update/8zu9/01.png)
2. Kopieren Sie aus dem Datenbankverzeichnis von MAGELLAN 8 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 8\Datenbank`) Ihre Datenbank (Standardbenennung: `Magellan8.fdb`) und legen die Datei im Datenbankverzeichnis von MAGELLAN 9 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 9\Datenbank`) ab.
3. Sollte dort bereits eine Datei mit dem Namen `Magellan9.fdb` existieren, benennen Sie diese um oder verschieben sie, so dass Sie anschließend für Ihre `Magellan8.fdb` den Namen `Magellan9.fdb` verwenden können.
4. Öffnen Sie erneut den Punkt `Systemsteuerung > Verwaltung > Dienste` und starten dort den Firebird-Dienst wieder.<br/>
![Firebird-Dienst starten](/assets/images/update/8zu9/02.png)
5. Starten Sie MAGELLAN 9 (Schulverwaltungsmodul, nicht den Administrator) als `sysdba` und führen Sie als erstes die Datensicherung durch. Der voreingestellte Sicherungspfad resultiert aus Ihren Angaben im Willkommensassistenten und kann im MAGELLAN Administrator in den Verbindungseinstellungen auf der Unterkarte `Datensicherung` angepasst werden.<br/>
![Datenbanksicherung erstellen](/assets/images/update/8zu9/05.png)
6. Im Anschluss an die Datensicherung, klicken Sie bitte auf "Weiter", MAGELLAN passt die Datenbank auf die neue Datenstruktur an.<br/>
![Datenbankstruktur anpassen](/assets/images/update/8zu9/06.png)
7. Öffnen Sie anschließend den MAGELLAN 9 ADMINISTRATOR und synchronisieren die Zugriffsrechte im Punkt `Benutzerverwaltung` über den Aufruf  `Zugriffsrechte synchronsieren` in der Menüleiste. Damit werden für Ihre bereits angelegten Benutzer die Zugriffsrechte auf die geänderte Datenbankteile geklärt.<br/>
![Zugriffsrechte synchronisieren](/assets/images/update/8zu9/04.png)

### Eigene Daten übernehmen

Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese bitte und legen Sie in der neuen Verzeichnisstruktur von MAGELLAN 9 ab.

!!! warning "Wichtig"

    Bitte legen Sie **nur Ihre zusätzlichen Dateien** in der neuen Verzeichnisstruktur ab und ersetzen Sie bitte nicht die Verzeichnisse! 

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil MAGELLAN 9 hier beispielsweise einen anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Ja| Bitte je Unterverzeichnis nur Ihre selbsterstellten oder angepassten Berichte übernehmen, bitte nicht den gesamten Ordnerinhalt oder ganze Ordner übertragen, Sie überschreiben sich ansonsten ggfs. aktuellere Varianten.
Datenbank|Ja| Die MAGELLAN 7 oder MAGELLAN 8 Datenbank bitte mit neuer Bezeichnung (MAGELLAN9.fdb) in den Datenbankordern der Version 9 ablegen, dabei die dort vorhandene gleichnamige Datenbank ersetzen oder vorab umbenennen. 
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für MAGELLAN 9 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von MAGELLAN 9 und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Sollten Sie eigene angepasste oder selbsterstellte Skripte einsezten, können Sie diese Dateien in der neuen Struktur ablegen.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für MAGELLAN 9 ab.

## Auf den Arbeitsplätzen

### MAGELLAN 9 installieren und lizenzieren

!!! warning "Wichtig"

    MAGELLAN 8 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unserer Anleitungen für die Einrichtung und Lizenzierung der [Arbeitsplätzen](https://doc.magellan.stueber.de/schulverwaltung/installation/version9/arbeitsplatz.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von MAGELLAN 10, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

### Empfehlung

Wir empfehlen Ihnen MAGELLAN auf einem Arbeitsplatz zu installieren, zu lizenzieren und zu konfigurieren. Die Lizenzdaten und die Konfigurationsdaten können anschließend zentral abgelegt werden. Somit wäre ab dem zweiten Arbeitsplatz nur die Installation notwendig und Sie legen zusätzlich eine Datei ab, die die Pfade enthält, von denen MAGELLAN die Lizenz- und Konfigurationdaten lesen soll.

Nach der Installation auf dem ersten Arbeitsplatz starten Sie bitte MAGELLAN 9 um den Willkommens-Assistenten zu durchlaufen. Im Willkommensassistenten gibt man die Lizenzdaten, die Pfade aus Sicht des Arbeitsplatzs zur Datenbank und zu den Datenordnern ein, wählt eine Option für die Region. Diese Eingaben werden in Dateiform gespeichert und können auch für weitere Clients genutzt werden.

Testen Sie anschließend auf dem ersten Arbeitsplatz, ob die Angaben korrekt waren.<br/>
**Test 1 (Datenbankpfad):** Dafür starten Sie MAGELLAN auf dem Rechner, gelingt der Start des Moduls, ist der Pfad zur Datenbank ok.<br/>
**Test 2 (Datenordnerpfade):** In MAGELLAN wechseln Sie in das Menü Schüler, markieren einen Schüler und drücken bitte STRG+P. Werden Schülerberichte zur Auswahl gezeigt, sind die Pfade zu den Datenordnern ok.

Die durch den Willkommens-Assistenten erzeugten Dateien, aus den die Lizenz, die Optionen und die Pfade ausgelesen werden, finden Sie unter `C:\ProgramData\Stueber Systems\Magellan 10`. Diese Dateien können Sie zentral ablegen und von allen Arbeitsplätzen aus nutzen. Damit beim Programmstart von MAGELLAN nicht die lokalen Daten ausgelesen werden, sondern die zentral abgelegten Dateien gelesen werden, muss eine Textdatei mit den Pfaden und einem bestimmten Namen angelegt und an einer bestimmten Stelle abgelegt werden. Bitte folgen Sie hierfür unserer Anleitung unter: [Die Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).

Die erzeugte Datei legen Sie auf allen anderen Arbeitsplätzen (nicht auf dem Server!) nach der Installation bitte unter `C:\Program Files (x86)\Stueber Systems\Magellan 10` ab. Damit entfallen weitere Schritte zur Lizenzierung und Konfiguration.
