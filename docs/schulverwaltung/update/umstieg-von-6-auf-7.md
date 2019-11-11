# Umstieg von MAGELLAN 6 auf MAGELLAN 7

!!! warning "Wichtig"

    Es empfiehlt sich **MAGELLAN 6 und MAGELLAN 7 nicht auf einem Rechner** zu verwenden, solange MAGELLAN 6 noch verwendet wird. Es kann ansonsten Probleme bei der Anzeige von Berichten geben. Es werden für die neue Crystal Reports-Schnittstelle ein neuer Treiber und auch abweichende ODBC-Einstellungen vorausgesetzt. 

    Für den Umstieg von MAGELLAN 6 auf MAGELLAN 7 hingegen, spricht natürlich nichts dagegen, dieser Hinweis bezieht sich lediglich auf einen parallelen Einsatz der beiden Versionen.

## Was ist vorab zu beachten

### Übernahme nicht übers Netzwerk

Es kann zu einem zeitlich immensen Unterschied kommen, wenn Sie während der Übernahme der Daten durch Ihr Netzwerk auf eine der beiden Datenbanken zugreifen. 
Bitte legen Sie beide Datenbanken, also die leere MAGELLAN7.fdb und Ihre gefüllte MAGELLAN6.fdb auf dem gleichen Rechner ab.

!!! danger "Achtung"

    Bevor Sie die MAGELLAN6.fdb kopieren stoppen Sie bitte den Firebirddienst unter `Start > Systemsteuerung > Verwaltung > Dienste`.

### Datenübernahme testen

Es empfiehlt sich mindestens einmal vorab die Datenübernahme zu testen, um sicherzustellen das beim Umstieg dann alles reibungslos läuft.

### Eigene Berichte

MAGELLAN beinhaltet eine aktualisierte Schnittstelle zu Crystal Reports, damit können Sie neue Funktionen in Ihren MAGELLAN-Berichten verwenden.
Aufgrund dieser technischen Veränderungen müssen Ihre selbsterstellte Berichte für die Verwendung in MAGELLAN  7 angepasst werden.

Bitte folgen Sie hierzu der [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/Berichte_anpassen/)!

### Sächsische Schulen

In MAGELLAN 7 werden Schüler und Ihre Ausbildungen mittels einer GUID eindeutig gekennzeichnet, damit Sie später wiederkehrend Daten nach SAXSVS übergeben können und die Schüler anhand dieses Merkmals eindeutig identifiziert werden können. Wenn Sie die Datenübernahme aber nur für den Export nach SAXSVS durchführen, dann in MAGELLAN 6 weiterarbeiten und später erst auf MAGELLAN 7 umsteigen, dann wird beim späteren Umstieg auch die GUID neu erzeugt. Diese weicht dann natürlich von der in SAXSVS erwarteten GUID ab, eine Identifikation ist so nicht möglich. Ab dem Zeitpunkt, ab dem Sie Daten aus MAGELLAN 7 nach SAXSVS übergeben, muss auch im Alltag auf MAGELLAN 7 umgestiegen werden.

### Schüler und Schülerkopien

In MAGELLAN 7 werden Schüler, die mehrfach vorhanden sind und durch Kopieren von Schülern erzeugt wurden (Beim Kopieren erfolgt ein Übertrag der Originalschüler-ID ins Feld IDIntern der Schülerkopie), anders behandelt. Alle Kopien sind mit dem Original verbunden, eine Änderung von Stammdaten an einem der Schüler wird für alle anderen Übertragen. Das gilt nicht für alle Daten, beispielsweise die Zeugnisdaten existieren pro Datensatz, Ausbildungsdaten werden als Liste gezeigt. Einzelheiten beschreiben wir im Abschnitt ["Rückkehrer, parallele Laufbahn, parallele Bewerbung"](https://doc.MAGELLAN7.stueber.de/schulverwaltung/howto/sonderfaelle/#ruckkehrer-parallele-laufbahn-parallele-bewerbung)

Dieser neue Umgang muss bei der Übernahme der Daten aus Ihrer MAGELLAN6.fdb in die neue MAGELLAN7.fdb berücksichtigt werden. Dieses "Merken" der ID als IDIntern in MAGELLAN 6 war dafür gedacht, dass beim Einschulen der Kopien die Auswahl "Zusammenführen" gewählt werden konnte und dann von einem der beiden Datensätze die Stammdaten übernommen wurden, die Laufbahn wurde zusammengeführt. Ob die Daten aus dem Bewerbermenü übernommen werden sollen, oder die Daten des Originals aus dem Schülermenü, konnte in den Optionen gewählt werden.

In MAGELLAN 7 gibt es diese Option nicht mehr, da es unerheblich ist an welchem Datensatz man einen Werte der Stammdaten ändert, die Änderung wird für alle zusammenhängenden Datensätze durchgeführt. Es gibt aus das "Zusammenführen" beim Einschulen so nicht mehr, der Assistent prüft selbstständig, ob eine Zusammenführen hier möglich ist oder nicht und führt die notwendigen Schritte aus.

#### Nicht zusammengeführte Schüler

Wenn Sie das Zusammenführen in der Version 6 nicht durchgeführt haben, dann gibt es Schülerkopien, die unabhaängig von einander in Version 6 geführt wurden. Um diesen Umstand beizubehalten, leeren wir bei der Datenübernahme das Feld `IDIntern` für alle aktiven und inaktiven Schüler, damit bleiben diese Datensätze wie in MAGELLAN 6 voneinander unabhängig.

#### Bewerber mit einer IDIntern

Bewerber, die zum Zeitpunkt der Datenübernahme mit einer `IDIntern` gekennzeichnet im Menü `Bewerber` sind, bleibt diese IDIntern erhalten. Durch diese Verknüpfung werden in MAGELLAN 7 automatisch die Stammdaten des Originalschülers gezeigt. Änderungen, die Sie an dem Bewerber in Magellan 6 vorgenommen haben, sind nicht sichtbar. Dieses Vorgehen ist für den Mehrwert der gleichen Datenlage umungänglich.

Was könnten Sie tun?

- Erfassen Sie die Abweichungen in MAGELLAN 7 erneut, egal ob beim Schüler oder beim Bewerber.
- Oder: Schulen Sie die Bewerber vorab in MAGELLAN ein, wählen Sie beim Einschulen, ob zusammengeführt werden soll oder nicht
- Erfassen Sie die Änderungen in MAGELLAN 6 direkt beim Originalschüler

## Wortersetzungen

Bei der Übernahme der Daten aus Ihrer MAGELLAN 6-Datenbank in die MAGELLAN 7-Datenbank können Ihre geänderten Feldbezeichnungen aus technischen Gründen nicht übernommen werden. Bitte tragen Sie  unter `MAGELLAN 7 > Extras > Bezeichnungen anpassen > Spalte "durch"` Ihre gewünschten Bezeichnungen neu ein!

## Notwendige Schritte

|Notwendige Schritte |
|-|
|[1. ggfs. MAGELLAN 6 und ggfs. Firebird aktualisieren](https://doc.MAGELLAN7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/#MAGELLAN-6-und-firebird-aktualisieren)|
|[2. MAGELLAN 7 installieren](https://doc.MAGELLAN7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/#MAGELLAN-7-installieren)|
|[3. Daten aus MAGELLAN 6 nach MAGELLAN 7 übernehmen](https://doc.MAGELLAN7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/#daten-aus-MAGELLAN-6-nach-MAGELLAN-7-%C3%BCbernehmen)|

## MAGELLAN 6 und Firebird aktualisieren

Um die Daten Ihrer MAGELLAN 6-Datenbank in eine MAGELLAN 7-Datenbank übernehmen zu können, muss die aktuellste Ausgabe von MAGELLAN 6 und die dazugehörige Firebird-Ausgabe eingesetzt werden.

!!! info "Hinweis"

     Wenn Sie die letzte Ausgabe von MAGELLAN 6 eingespielt haben und die empfohlene Ausgabe von Firebird (2.5.8) verwenden, ist hier nichts weiter zu tun.

Programm| Wo kann ich die Version überprüfen?
--|--
MAGELLAN | Bitte vergleichen Sie die angezeigte Version (am besten der Serverrechner-Installation) unter `MAGELLAN > Hilfe > Info über`  mit den angezeigten Version auf im [Downloadbereich](https://MAGELLAN.stueber.de/download.php) oder im Abschnitt ["Was ist neu?"](https://doc.MAGELLAN7.stueber.de/changelog/) der MAGELLAN 6-Dokumentation!<br/> Bitte beachten Sie unsere Anleitungen zum Aktualisieren von [MAGELLAN 6](https://doc.MAGELLAN6.stueber.de/installation/update.html)
FIREBIRD | Die Firebird-Versionsnummer sehen Sie unter `Serverrechner > Systemsteuerung > Firebird Server Manager (32-Bit)`. <br/> Ist es die -Ausgabe, die wir im [Downloadbereich](https://magellan.stueber.de/download.php) anbieten? Dann ist es die korrekte Ausgabe. <br/> Ist es eine ältere Ausgabe finden Sie im Abschnitt ["älteren Firebirdversionen"](https://doc.MAGELLAN6.stueber.de/installation/firebird-aktualisieren.html) der MAGELLAN 6-Dokumentation eine Anleitung für das Aktualisieren.

## MAGELLAN 7 installieren

!!! info "Hinweis"

    Sollten Sie eine Datenübernahme wiederholen wollen, benötigen Sie eine "frische" leere MAGELLAN 7 Datenbank. 
    Diese könnten Sie [hier](ftp://ftp.stueber.de/pub/bin/de/MAGELLAN/v7/database/MAGELLAN7.FDB) herunterladen.

Führen Sie im zweiten Schritt bitte die Installation von MAGELLAN 7 aus, beide Version (6 + 7) können parallel auf einem Rechner laufen (haben aber getrennte Datenbanken). Eine ausführliche Installationsanleitung finden Sie im Abschnitt [Installation](https://doc.MAGELLAN7.stueber.de/schulverwaltung/installation/).

## Daten aus MAGELLAN 6 nach MAGELLAN 7 übernehmen

Im dritten Schritt werden in eine leere MAGELLAN 7-Datenbank, die Daten aus Ihrer MAGELLAN 6-Datenbank übergeben.

!!! warning "Wichtig"

    Bitte verwenden Sie einen leistungsstarken Rechner und legen beiden Datenbanken (die leere MAGELLAN7- und die gefüllte MAGELLAN6-Datenbank) auf diesem Rechner ab. Die Übertragung der Daten aus einer großen Datenbank kann viel Zeit in Anspruch nehmen, wenn die Daten dabei noch über Ihr Netzwerk übertragen werden, beeinflussen Sie diesen Prozess ungünstig.

Öffnen Sie bitte das Modul MAGELLAN 7 ADMINISTRATOR und wählen den Unterpunkt `Datenbankpflege > Mandanten kopieren` und stellen die Variante `MAGELLAN 6 nach MAGELLAN 7` ein. Klicken Sie auf `Weiter`!

![MAGELLAN 6 nach MAGELLAN 7](/assets/images/magellan.administrator/mandanten.kopieren5.png)

Das Übertragen der MAGELLAN 6-Daten ist nur in eine leere aktuelle MAGELLAN 7-Datenbank möglich. Bei der Installation von MAGELLAN 7 wird Ihnen im Datenbankverzeichnis eine leere Datenbank mit dem Namen "MAGELLAN7.fdb".
![leere Datenbank im Format für MAGELLAN 7](/assets/images/magellan.administrator/mandanten.kopieren6.png)

Sollten Sie den Übertrag bereits einmal durchgeführt haben, können Sie jederzeit [eine "frische" leere Datenbank im MAGELLAN 7-Format herunterladen.](ftp://ftp.stueber.de/pub/bin/de/MAGELLAN/v7/database/MAGELLAN7.fdb)

![Laden Sie ggfs. eine leere Datenbank herunter!](/assets/images/magellan.administrator/mandanten.kopieren7.png)

Füllen Sie bitte die Felder (siehe untere Tabelle) des Assistenten aus, im oberen Teil verweisen Sie auf die Quelldatenbank (MAGELLAN 6), im unteren Bereich auf die Zieldatenbank (MAGELLAN 7).

![Eintragungen für die Quell- und Zieldatenbank](/assets/images/magellan.administrator/mandanten.kopieren8.png)

Feld|Anmerkung
--|--
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Quelldatenbank|Tragen Sie bitte den lokalen Pfad zur Quelldatenbank und deren Dateinamen ein.
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Zieldatenbank|Tragen Sie bitte den lokalen Pfad zur Zieldatenbank und deren Dateinamen ein. **Bitte beachten Sie, dass eine leere Zieldatenbank erwartet wird. Über das Symbol am Ende der Zeile können Sie eine leere MAGELLAN 7 Datenbank herunterladen.**
Benutzernamen <br/> Kennwort|Tragen Sie als Benutzer bitte den sysdba und das dazugehörige Passwort ein.

Starten Sie anschließend den Assistenten mit `Weiter` und `Fertigstellen`.

!!! info "Hinweis"

     Die Datenübernahme aus Ihrer MAGELLAN 6-Datenbank in die neue MAGELLAN 7-Datenbank kann je nach Datenvolumen auch mehrere Stunden dauern. Bitte stellen Sie sicher, dass der verwendete Rechner auch aktiviert bleibt.

## Meldungen

Während der Datenübernahme können Ihnen Meldungen ausgegeben werden, die Ihnen Datensätze melden, die nicht übernommen werden können. Ursache dafür können Inkonsistenzen in Ihrer Datenbank sein. Es kann sein, dass die Meldungen dazudienen, Ihnen Datensätze zu zeigen, die Sie in Version 7 nachpflegen müssen.

Es könnten aber auch Fehlermeldungen sein, die anzeigen, dass an einer Stelle in Ihrer Datenbank die Daten nicht wie erwartet vorliegen.
Mit diesem Meldungen sollten Sie sich an unser [Supportteam](https://support.stueber.de/) wenden, damit gegebenenfalls noch Korrekturen vorab vorgenommen werden können!

!!! info "Hinweis"

    Sollten Sie die Datenstruktur der MAGELLAN 6 Datenbank verändert haben, müssen Sie diese Änderungen zurücksetzen um die Datenübernahme erfolgreich abschließen zu können.

## Pflege

!!! warning "Wichtig"

    Nachdem Sie Ihre Datenbank übernommen haben, führen Sie bitte im MAGELLAN ADMINISTRATOR unter `Datenpflege` noch die Punkte `Aktuelle Bewerber-Ausbildung setzen` und `Verwaiste Stammschüler-Verweise entfernen` aus!

![Bitte diese beiden Punkte abschließend ausführen!](/assets/images/magellan.administrator/01.png)

## Benutzeranmeldung

Wenn die Version 7 auf einem anderen Serverrechner als die Version 6 läuft, dann muss die Passwortdatenbank (security2.fdb) von Firebird noch mit übernommen werden, also auf dem neuen Rechner an gleicher Stelle abgelegt werden.
Sie finden die `security2.fdb`  bei einer Standardfirebirdinstallation unter `C:\Program Files (x86)\Firebird\Firebird_2_5\`.

!!! danger "Achtung"

    Bitte beachten Sie, dass durch die veränderte Datenstruktur das `Zugriffsrechte synchronisieren` im Modul `Administrator` ausgeführt werden muss!

![MAGELLAN ADMINISTRATOR > Benutzerverwaltung > Zugriffsrechte synchronisieren](/assets/images/update/01.png)

## Datenordner

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil MAGELLAN 7 hier beispielsweise eine anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Nein| Unsere originalen Berichte sind für die Nutzung in MAGELLAN 7 angepasst, [eigene Berichte müssen entsprechend angepasst werden](https://doc.magellan7.stueber.de/schulverwaltung/update/Berichte_anpassen/).
Datenbank|Nein| Die Daten aus Ihrer Datenbank werden in die neue Datenbank übertragen.
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für MAGELLAN 7 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von MAGELLAN 7 und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Aufgrund der geänderten Datenstruktur können Skripte aus MAGELLAN 6 nicht unter MAGELLAN 7 funktionieren, eine Übernahme würde hier schaden.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für MAGELLAN 7 ab.
