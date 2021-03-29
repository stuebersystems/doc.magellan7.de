# Umstieg von MAGELLAN 7 auf MAGELLAN 8

Folgende Punkte müssen erledigt werden um Ihre MAGELLAN 7 Version auf MAGELLAN 8 zu aktualisieren.

Nr.|Was ist zu tun
--|--
1.| Prüfen Sie, ob auf Ihrem Serverrechner MAGELLAN und Firebird aktuell sind und aktualisieren ggfs.
2.| Installieren Sie MAGELLAN 8 auf dem Server und den Clientrechnern und lizenzieren es.
3.| Kopieren Sie die 7er Datenbank in den 8er Datenbankordner.
4.| Starten Sie MAGELLAN um die Datenbank anzupassen, synchronisieren Sie die Zugriffsrechte.
5.| Übernehmen Sie eigene Berichte, Vorlagen oder Dokumente.
6.| Fertig!

## Ausgangssituation prüfen und aktualisieren

Auf Ihrem **Serverrechner** stellen Sie bitte sicher, dass jeweils die aktuellste Ausgabe von `MAGELLAN 7` und `Firebird 2.5.9` einsetzt wird. Die Versionen auf den Clientrechner müssen nicht aktualisiert werden.

Programm|Version auslesen
--|--
MAGELLAN-Version|Die bei Ihnen eingesetzte Ausgabe von MAGELLAN wird im Programm unter `Hilfe > Info über` gezeigt, die aktuell verfügbare Version können Sie in der [Changelog-Datei](https://doc.magellan7.stueber.de/changelog/changelog/) sehen.
Firebird| Auf Ihrem Serverrechner unter `Systemsteuerung > Firebird Server Manager (323 Bit)` wird die Version gezeigt. Sie sollte mit der Version unter [https://magellan.stueber.de/download.php](https://magellan.stueber.de/download.php) gezeigten Version (aktuell 2.5.9) übereinstimmen.

Wenn es hier Abweichungen gibt, aktualisieren Sie bitte im ersten Schritt MAGELLAN und ggfs. Firebird auf Ihrem Serverrechner, Anleitungen finden Sie unter:

* [MAGELLAN-Updateanleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/)
* [Firebird-Updateanleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/firebird-aktualisieren/)

## MAGELLAN 8 installieren und lizenzieren

Installieren Sie MAGELLAN 8 auf Ihrem Serverrechner und auf den Clientrechnern.

!!! warning "Wichtig"

    MAGELLAN 7 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unseren Anleitungen für die Einrichtung und Lizenzierung des [Servers](https://doc.magellan7.stueber.de/schulverwaltung/installation/version8/server.installieren/) und der [Clients](https://doc.magellan7.stueber.de/schulverwaltung/installation/version8/arbeitsplatz.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von MAGELLAN 8, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

## 7er Datenbank übernehmen

Auf Ihrem MAGELLAN-Serverrechner soll im nächsten Schritt die 7er Datenbank übernommen und für MAGELLAN 8 angepasst werden. Führen Sie hierfür bitte die folgenden Schritte aus:

1. Öffnen Sie auf dem Serverrechner bitte `Systemsteuerung > Verwaltung > Dienste` und stoppen dort den Firebird-Dienst.

![Firebird-Dienst stoppen](/assets/images/update/7zu8/01.png)

2. Kopieren Sie aus dem Datenbankverzeichnis von MAGELLAN 7 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 7\Datenbank`) Ihre Datenbank (Standardbenennung: `Magellan7.fdb`) und legen die Datei im Datenbankverzeichnis von MAGELLAN 8 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 8\Datenbank`) ab.
3. Sollte dort bereits eine Datei mit dem Namen `Magellan8.fdb` existieren, benennen Sie diese um oder verschieben sie, so dass Sie anschließend für Ihre `Magellan7.fdb` den Namen `Magellan8.fdb` verwenden können.
4. Öffnen Sie erneut den Punkt `Systemsteuerung > Verwaltung > Dienste` und starten dort den Firebird-Dienst wieder.

![Firebird-Dienst starten](/assets/images/update/7zu8/02.png)

5. Starten Sie MAGELLAN 8 als `sysdba` und führen Sie als erstes die Datensicherung durch. Der voreingestellte Sicherungspfad resultiert aus Ihren Angaben im Willkommensassistenten. Sollten die Angaben nicht stimmen, weil zum Beispiel der Pfad nicht stimmt, können Sie einen alternativen Pfad für die Sicherung angeben.
Der Pfad selbst kann im MAGELLAN ADMINISTRATOR unter `Datenbankverbindungen > Doppelklick auf Ihre Verbindung > Unterkarte "Datensicherung"` angepasst werden.
Im Anschluss an die Datensicherung, klicken Sie bitte auf "Weiter", MAGELLAN passt die Datenbank auf die neue Datenstruktur an.
6. Öffnen Sie anschließend den MAGELLAN 8 ADMINISTRATOR und synchronisieren die Zugriffsrechte im Punkt `Benutzerverwaltung` über den Aufruf  `Zugriffsrechte synchronsieren` in der Menüleiste. Damit werden für Ihre bereits angelegten Benutzer die Zugriffsrechte auf die geänderte Datenbankteile geklärt.

![Zugriffsrechte](/assets/images/update/7zu8/03.png)

## Eigene Daten übernehmen

Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese bitte und legen Sie in der neuen Verzeichnisstruktur von MAGELLAN 8 ab.

!!! warning "Wichtig"

    Bitte legen Sie nur Ihre zusätzlichen Dateien in der neuen Verzeichnisstruktur ab und ersetzen Sie bitte nicht die Verzeichnisse! 
