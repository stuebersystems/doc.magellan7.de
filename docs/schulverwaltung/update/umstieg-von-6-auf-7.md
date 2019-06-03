# Umstieg von MAGELLAN 6 auf MAGELLAN 7



!!! warning "Wichtig"

    Es empfiehlt sich **MAGELLAN 6 und MAGELLAN 7 nicht auf einem Rechner** zu verwenden, da es Probleme bei der Anzeige von Berichten geben kann. Es werden für die neue Crystal Reports-Schnittstelle ein neuer Treiber und auch abweichende ODBC-Einstellungen vorausgesetzt. Ein paralleles Arbeiten ist nicht sinnvoll, da beide Programme jeweils eigene Datenbanken verwenden.


|Notwendige Schritte |
|-|
|[1. MAGELLAN 6 und Firebird aktualisieren](https://doc.magellan7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/#magellan-6-und-firebird-aktualisieren)|
|[2. MAGELLAN 7 installieren](https://doc.magellan7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/#magellan-7-installieren)|
|[3. Daten aus MAGELLAN 6 nach MAGELLAN 7 übernehmen](https://doc.magellan7.stueber.de/schulverwaltung/update/umstieg-von-6-auf-7/#daten-aus-magellan-6-nach-magellan-7-%C3%BCbernehmen)|

## MAGELLAN 6 und Firebird aktualisieren

Um die Daten Ihrer MAGELLAN 6-Datenbank in eine MAGELLAN 7-Datenbank übernehmen zu können, muss die aktuellste Ausgabe von MAGELLAN 6 und der dazugehörigen Firebird-Installation eingesetzt werden.

!!! info "Hinweis"

     Bitte vergleichen Sie die angezeigte Version unter `MAGELLAN > Hilfe > Info über` und `Systemsteuerung > Firebird Server Manager (32-Bit)` mit den angezeigten Version auf im [Downloadbereich](https://magellan.stueber.de/download.php) oder im Abschnitt [Was ist neu?](https://doc.magellan7.stueber.de/schulverwaltung/changelog/) der MAGELLAN 6-Dokumentation!
     Bitte beachten Sie unsere Anleitungen zum Aktualisieren von [MAGELLAN 6](https://doc.magellan7.stueber.de/schulverwaltung/installation/update.html) und [älteren Firebirdversionen](https://doc.magellan7.stueber.de/schulverwaltung/installation/firebird-aktualisieren.html), da für den Wechsel auf MAGELLAN 7 zuvor die aktuellste MAGELLAN 6-Ausgabe vorausgesetzt wird!  

## MAGELLAN 7 installieren

!!! info "Hinweis"

    Sollten Sie eine Datenübernahme wiederholen wollen, benötigen Sie eine "frische" leere MAGELLAN 7 Datenbank. 
    Diese könnten Sie [hier](ftp://ftp.stueber.de/pub/bin/de/magellan/v7/database/MAGELLAN7.FDB) herunterladen.

Führen Sie im zweiten Schritt bitte die Installation von MAGELLAN 7 aus, beide Version (6 + 7) können parallel auf einem Rechner laufen (haben aber getrennte Datenbanken). Eine ausführliche Installationsanleitung finden Sie im Abschnitt [Installation](https://doc.magellan7.stueber.de/schulverwaltung/installation/).


## Daten aus MAGELLAN 6 nach MAGELLAN 7 übernehmen

Im dritten Schritt werden in eine leere MAGELLAN 7-Datenbank, die Daten aus Ihrer MAGELLAN 6-Datenbank übergeben. 

Öffnen Sie bitte das Modul MAGELLAN 7 ADMINISTRATOR und wählen den Unterpunkt `Datenbankpflege > Mandanten kopieren` und stellen die Variante `MAGELLAN 6 nach MAGELLAN 7`ein. Klicken Sie auf `Weiter`!


![Magellan 6 nach MAGELLAN 7](/assets/images/magellan.administrator/mandanten.kopieren5.png)

Das Übertragen der MAGELLAN 6-Daten ist nur in eine leere aktuelle MAGELLAN 7-Datenbank möglich. Bei der Installation von MAGELLAN 7 wird Ihnen im Datenbankverzeichnis eine leere Datenbank mit dem Namen "Magellan7.fdb". 
![leere Datenbank im Format für MAGELLAN 7](/assets/images/magellan.administrator/mandanten.kopieren6.png)

Sollten Sie den Übertrag bereits einmal durchgeführt haben, können Sie jederzeit [eine "frische" leere Datenbank im MAGELLAN 7-Format herunterladen.](ftp://ftp.stueber.de/pub/bin/de/magellan/v7/database/Magellan7.fdb)

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
Benutzernamen<br/>Kennwort|Tragen Sie als Benutzer bitte den sysdba und das dazugehörige Passwort ein.

Starten Sie anschließend den Assistenten mit `Weiter` und `Fertigstellen`.

## Wortersetzungen

Bei der Übernahme der Daten aus Ihrer MAGELLAN 6-Datenbank in die MAGELLAN 7-Datenbank können Ihre geänderten Feldbezeichnungen aus technischen Gründen nicht übernommen werden. Bitte tragen Sie  unter `MAGELLAN 7 > Extras > Bezeichnungen anpassen > Spalte "durch"` Ihre gewünschten Bezeichnungen neu ein!

