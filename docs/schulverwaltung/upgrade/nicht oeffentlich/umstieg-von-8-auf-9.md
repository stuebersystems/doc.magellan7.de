# Umstieg von Magellan 8 auf Magellan 9

Folgende Punkte müssen erledigt werden um Ihre Magellan 8 Version auf Magellan 9 zu aktualisieren.

Nr.|Was ist zu tun
--|--
1.| Prüfen Sie, ob auf Ihrem Serverrechner Magellan 8 und Firebird aktuell sind und aktualisieren ggfs.
2.| Installieren Sie Magellan 9 auf dem Server und den Clientrechnern und lizenzieren es.
3.| Kopieren Sie die 8er Datenbank in den 9er Datenbankordner.
4.| Starten Sie Magellan um die Datenbank anzupassen, synchronisieren Sie die Zugriffsrechte.
5.| Übernehmen Sie eigene Berichte, Vorlagen oder Dokumente.
6.| Clientrechner installieren, lizenzieren, konfigurieren
7.| Fertig!

## Auf dem Server

### Ausgangssituation prüfen und aktualisieren

Auf Ihrem **Serverrechner** stellen Sie bitte sicher, dass jeweils die aktuellste Ausgabe von `Magellan 8` und `Firebird 2.5.9` einsetzt wird. Die Versionen auf den Clientrechner müssen nicht aktualisiert werden.

Programm|Version auslesen
--|--
Magellan-Version|Die bei Ihnen eingesetzte Ausgabe von Magellan wird im Programm unter `Hilfe > Info über` gezeigt, die aktuell verfügbare Version können Sie in der [Changelog-Datei](https://doc.magellan.stueber.de/changelog/changelog/) sehen.
Firebird| Auf Ihrem Serverrechner unter `Systemsteuerung > Firebird Server Manager (32 Bit)` wird die Version gezeigt. Sie sollte mit der Version unter [https://magellan.stueber.de/download.php](https://magellan.stueber.de/download.php) gezeigten Version (aktuell 2.5.9) übereinstimmen.

Wenn es hier Abweichungen gibt, aktualisieren Sie bitte im ersten Schritt Magellan und ggfs. Firebird auf Ihrem Serverrechner, Anleitungen finden Sie unter:

* [Magellan-Updateanleitung](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/)
* [Firebird-Updateanleitung](https://doc.magellan.stueber.de/schulverwaltung/update/firebird-aktualisieren/)

### Magellan 9 installieren und lizenzieren

Installieren Sie Magellan 9 auf Ihrem Serverrechner und auf den Clientrechnern.

!!! warning "Wichtig"

    Magellan 8 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unserer Anleitung für die Einrichtung und Lizenzierung des [Servers](https://doc.magellan.stueber.de/schulverwaltung/installation/version9/server.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von Magellan 9, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

### 8er Datenbank übernehmen

Auf Ihrem Magellan-Serverrechner soll im nächsten Schritt die 8er Datenbank übernommen und für Magellan 9 angepasst werden. Führen Sie hierfür bitte die folgenden Schritte aus:

1. Öffnen Sie auf dem Serverrechner bitte `Systemsteuerung > Verwaltung > Dienste` und stoppen dort den Firebird-Dienst.<br/>
![Firebird-Dienst stoppen](/assets/images/update/8zu9/01.png)
2. Kopieren Sie aus dem Datenbankverzeichnis von Magellan 8 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 8\Datenbank`) Ihre Datenbank (Standardbenennung: `Magellan8.FDB`) und legen die Datei im Datenbankverzeichnis von Magellan 9 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 9\Datenbank`) ab.
3. Sollte dort bereits eine Datei mit dem Namen `Magellan9.FDB` existieren, benennen Sie diese um oder verschieben sie, so dass Sie anschließend für Ihre `Magellan8.FDB` den Namen `Magellan9.FDB` verwenden können.
4. Öffnen Sie erneut den Punkt `Systemsteuerung > Verwaltung > Dienste` und starten dort den Firebird-Dienst wieder.<br/>
![Firebird-Dienst starten](/assets/images/update/8zu9/02.png)
5. Starten Sie Magellan 9 (Schulverwaltungsmodul, nicht den Administrator) als `sysdba` und führen Sie als erstes die Datensicherung durch. Der voreingestellte Sicherungspfad resultiert aus Ihren Angaben im Willkommensassistenten und kann im Magellan Administrator in den Verbindungseinstellungen auf der Unterkarte `Datensicherung` angepasst werden.<br/>
![Datenbanksicherung erstellen](/assets/images/update/8zu9/05.png)
6. Im Anschluss an die Datensicherung, klicken Sie bitte auf "Weiter", Magellan passt die Datenbank auf die neue Datenstruktur an.<br/>
![Datenbankstruktur anpassen](/assets/images/update/8zu9/06.png)
7. Öffnen Sie anschließend den Magellan 9 Administrator und synchronisieren die Zugriffsrechte im Punkt `Benutzerverwaltung` über den Aufruf  `Zugriffsrechte synchronsieren` in der Menüleiste. Damit werden für Ihre bereits angelegten Benutzer die Zugriffsrechte auf die geänderte Datenbankteile geklärt.<br/>
![Zugriffsrechte synchronisieren](/assets/images/update/8zu9/04.png)

### Eigene Daten übernehmen

Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese bitte und legen Sie in der neuen Verzeichnisstruktur von Magellan 9 ab.

!!! warning "Wichtig"

    Bitte legen Sie **nur Ihre zusätzlichen Dateien** in der neuen Verzeichnisstruktur ab und ersetzen Sie bitte nicht die Verzeichnisse! 

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil Magellan 9 hier beispielsweise einen anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Ja| Bitte je Unterverzeichnis nur Ihre selbsterstellten oder angepassten Berichte übernehmen, bitte nicht den gesamten Ordnerinhalt oder ganze Ordner übertragen, Sie überschreiben sich ansonsten ggfs. aktuellere Varianten.
Datenbank|Ja| Die Magellan 7 oder Magellan 8 Datenbank bitte mit neuer Bezeichnung (MAGELLAN9.FDB) in den Datenbankordern der Version 9 ablegen, dabei die dort vorhandene gleichnamige Datenbank ersetzen oder vorab umbenennen. 
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 9 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von Magellan 9 und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Sollten Sie eigene angepasste oder selbsterstellte Skripte einsezten, können Sie diese Dateien in der neuen Struktur ablegen.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 9 ab.

## Auf den Clientrechnern

### Magellan 9 installieren und lizenzieren

!!! warning "Wichtig"

    Magellan 8 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unserer Anleitungen für die Einrichtung und Lizenzierung der [Clients](https://doc.magellan.stueber.de/schulverwaltung/installation/version9/arbeitsplatz.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von Magellan 9, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

### Empfehlung

Wir empfehlen Ihnen Magellan auf einem Clientrechner zu installieren, zu lizenzieren und zu konfigurieren. Die Lizenzdaten und die Konfigurationsdaten können anschließend zentral abgelegt werden. Somit wäre ab dem zweiten Clientrechner nur die Installation notwendig und Sie legen zusätzlich eine Datei ab, die die Pfade enthält, von denen Magellan die Lizenz- und Konfigurationdaten lesen soll.

Nach der Installation auf dem ersten Clientrechner starten Sie bitte Magellan 9 um den Willkommens-Assistenten zu durchlaufen. Im Willkommensassistenten gibt man die Lizenzdaten, die Pfade aus Sicht des Clientrechners zur Datenbank und zu den Datenordnern ein, wählt eine Option für die Region. Diese Eingaben werden in Dateiform gespeichert und können auch für weitere Clients genutzt werden.

Testen Sie anschließend auf dem ersten Clientrechner, ob die Angaben korrekt waren.<br/>
**Test 1 (Datenbankpfad):** Dafür starten Sie Magellan auf dem Rechner, gelingt der Start des Moduls, ist der Pfad zur Datenbank ok.<br/>
**Test 2 (Datenordnerpfade):** In Magellan wechseln Sie in das Menü Schüler, markieren einen Schüler und drücken bitte STRG+P. Werden Schülerberichte zur Auswahl gezeigt, sind die Pfade zu den Datenordnern ok.

Die durch den Willkommens-Assistenten erzeugten Dateien, aus den die Lizenz, die Optionen und die Pfade ausgelesen werden, finden Sie unter `C:\ProgramData\Stueber Systems\Magellan 9`. Diese Dateien können Sie zentral ablegen und von allen Clientrechnern aus nutzen. Damit beim Programmstart von Magellan nicht die lokalen Daten ausgelesen werden, sondern die zentral abgelegten Dateien gelesen werden, muss eine Textdatei mit den Pfaden und einem bestimmten Namen angelegt und an einer bestimmten Stelle abgelegt werden. Bitte folgen Sie hierfür unserer Anleitung unter: [Die Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).

Die erzeugte Datei legen Sie auf allen anderen Clientrechnern (nicht auf dem Server!) nach der Installation bitte unter `C:\Program Files (x86)\Stueber Systems\Magellan 9` ab. Damit entfallen weitere Schritte zur Lizenzierung und Konfiguration.
