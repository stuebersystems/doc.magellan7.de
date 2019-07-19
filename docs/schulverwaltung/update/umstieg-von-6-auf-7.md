# Umstieg von MAGELLAN 6 auf MAGELLAN 7

!!! warning "Wichtig"

    Es empfiehlt sich **MAGELLAN 6 und MAGELLAN 7 nicht auf einem Rechner** zu verwenden, da es Probleme bei der Anzeige von Berichten geben kann. Es werden für die neue Crystal Reports-Schnittstelle ein neuer Treiber und auch abweichende ODBC-Einstellungen vorausgesetzt. Ein paralleles Arbeiten ist nicht sinnvoll, da beide Programme jeweils eigene Datenbanken verwenden.

## Schüler und Schülerkopien

   In MAGELLAN 7 werden Schüler, die mehrfach vorhanden sind und durch Kopieren von Schülern erzeugt wurden (Beim Kopieren erfolgt ein Übertrag der Originalschüler-ID ins Feld IDIntern der Schülerkopie), anders behandelt. Alle Kopien sind mit dem Original verbunden, eine Änderung von Stammdaten an einem der Schüler wird für alle anderen Übertragen. Das gilt nicht für alle Daten, beispielsweise die Zeugnisdaten existieren pro Datensatz, Ausbildungsdaten werden als Liste gezeigt. Einzelheiten beschreiben wir im Abschnitt ["Rückkehrer, parallele Laufbahn, parallele Bewerbung"](https://doc.MAGELLAN7.stueber.de/schulverwaltung/howto/sonderfaelle/#ruckkehrer-parallele-laufbahn-parallele-bewerbung)

Dieser neue Umgang muss bei der Übernahme der Daten aus Ihrer MAGELLAN6.fdb in die neue MAGELLAN7.fdb berücksichtigt werden. Dieses "Merken" der ID als IDIntern in MAGELLAN 6 war dafür gedacht, dass beim Einschulen der Kopien die Auswahl "Zusammenführen" gewählt werden konnte und dann von einem der beiden Datensätze die Stammdaten übernommen wurden, die Laufbahn wurde zusammengeführt. Ob die Daten aus dem Bewerbermenü übernommen werden sollen, oder die Daten des Originals aus dem Schülermenü, konnte in den Optionen gewählt werden.

In MAGELLAN 7 gibt es diese Option nicht mehr, da es unerheblich ist an welchem Datensatz man einen Werte der Stammdaten ändert, die Änderung wird für alle zusammenhängenden Datensätze durchgeführt. Es gibt aus das "Zusammenführen" beim Einschulen so nicht mehr, der Assistent prüft selbstständig, ob eine Zusammenführen hier möglich ist oder nicht und führt die notwendigen Schritte aus.

### nicht zusammengeführte Schüler

Wenn Sie das Zusammenführen in der Version 6 nicht durchgeführt haben, dann gibt es Schülerkopien, die unabhaängig von einander in Version 6 geführt wurden. Um diesen Umstand beizubehalten, leeren wir bei der Datenübernahme das Feld `IDIntern` für alle aktiven und inaktiven Schüler, damit bleiben diese Datensätze wie in MAGELLAN 6 voneinander unabhängig.

### Bewerber mit einer IDIntern

Bewerber, die zum Zeitpunkt der Datenübernahme mit einer `IDIntern` gekennzeichnet im Menü `Bewerber` sind, bleibt diese IDIntern erhalten. Durch diese Verknüpfung werden in MAGELLAN 7 automatisch die Stammdaten des Originalschülers gezeigt. Änderungen, die Sie an dem Bewerber in Magellan 6 vorgenommen haben, sind nicht sichtbar. Dieses Vorgehen ist für den Mehrwert der gleichen Datenlage umungänglich.

Was könnten Sie tun?

- Erfassen Sie die Abweichungen in MAGELLAN 7 erneut, egal ob beim Schüler oder beim Bewerber.
- Oder: Schulen Sie die Bewerber vorab in MAGELLAN ein, wählen Sie beim Einschulen, ob zusammengeführt werden soll oder nicht
- Erfassen Sie die Änderungen in MAGELLAN 6 direkt beim Originalschüler

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
MAGELLAN | Bitte vergleichen Sie die angezeigte Version (am besten der Serverrechner-Installation) unter `MAGELLAN > Hilfe > Info über`  mit den angezeigten Version auf im [Downloadbereich](https://MAGELLAN.stueber.de/download.php) oder im Abschnitt ["Was ist neu?"](https://doc.MAGELLAN7.stueber.de/schulverwaltung/changelog/) der MAGELLAN 6-Dokumentation!<br/> Bitte beachten Sie unsere Anleitungen zum Aktualisieren von [MAGELLAN 6](https://doc.MAGELLAN6.stueber.de/installation/update.html)
FIREBIRD | Die Firebird-Versionsnummer sehen Sie unter `Serverrechner > Systemsteuerung > Firebird Server Manager (32-Bit)`. <br/> Ist es die 2.5.8? Dann ist es die korrekte Ausgabe. <br/> Ist es eine ältere Ausgabe finden Sie im Abschnitt ["älteren Firebirdversionen"](https://doc.MAGELLAN6.stueber.de/installation/firebird-aktualisieren.html) der MAGELLAN 6-Dokumentation eine Anleitung für das Aktualisieren.

## MAGELLAN 7 installieren

!!! info "Hinweis"

    Sollten Sie eine Datenübernahme wiederholen wollen, benötigen Sie eine "frische" leere MAGELLAN 7 Datenbank. 
    Diese könnten Sie [hier](ftp://ftp.stueber.de/pub/bin/de/MAGELLAN/v7/database/MAGELLAN7.FDB) herunterladen.

Führen Sie im zweiten Schritt bitte die Installation von MAGELLAN 7 aus, beide Version (6 + 7) können parallel auf einem Rechner laufen (haben aber getrennte Datenbanken). Eine ausführliche Installationsanleitung finden Sie im Abschnitt [Installation](https://doc.MAGELLAN7.stueber.de/schulverwaltung/installation/).

## Daten aus MAGELLAN 6 nach MAGELLAN 7 übernehmen

Im dritten Schritt werden in eine leere MAGELLAN 7-Datenbank, die Daten aus Ihrer MAGELLAN 6-Datenbank übergeben.

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

Während der Datenübernahme können Ihnen Meldungen ausgegeben werden, die Ihnen Datensätze melden, die nicht übernommen werden können. Ursache dafür können Inkonsistenzen in Ihrer Datenbank sein. Diese Meldungen können Sie nutzen um anschließend die Punkte in MAGELLAN 7 nachzupflegen.

## Pflege

!!! warning "Wichtig"

    Nachdem Sie Ihre Datenbank übernommen haben, führen Sie bitte im MAGELLAN ADMINISTRATOR unter `Datenpflege` noch die Punkte `Aktuelle Bewerber-Ausbildung setzen` und `Verwaiste Stammschüler-Verweise entfernen` aus!

![Bitte diese beiden Punkte abschließend ausführen!](/assets/images/magellan.administrator/01.png)

## Wortersetzungen

Bei der Übernahme der Daten aus Ihrer MAGELLAN 6-Datenbank in die MAGELLAN 7-Datenbank können Ihre geänderten Feldbezeichnungen aus technischen Gründen nicht übernommen werden. Bitte tragen Sie  unter `MAGELLAN 7 > Extras > Bezeichnungen anpassen > Spalte "durch"` Ihre gewünschten Bezeichnungen neu ein!
