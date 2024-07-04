# Umstieg von Magellan 6 auf Magellan 8

!!! warning "Wichtig"

    Es empfiehlt sich **Magellan 6 und Magellan 8 nicht auf einem Rechner** zu verwenden, solange Magellan 6 noch verwendet wird. Es kann ansonsten Probleme bei der Anzeige von Berichten geben. Es werden für die neue Crystal Reports-Schnittstelle ein neuer Treiber und auch abweichende ODBC-Einstellungen vorausgesetzt. 

    Für den Umstieg von Magellan 6 auf Magellan 8 hingegen, spricht natürlich nichts dagegen, dieser Hinweis bezieht sich lediglich auf einen parallelen Einsatz der beiden Versionen.

## Was ist vorab zu beachten

### Datenübernahme testen

Es empfiehlt sich mindestens einmal vorab die Datenübernahme zu testen, um sicherzustellen das beim Umstieg dann alles reibungslos läuft.
Bei der Übernahme können Meldungen ausgegeben werden, die müssten bitte geprüft und die Ursache behoben werden, mehr dazu im Abschnitt [Meldungen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-7/#meldungen).
Bitte kontrollieren Sie die Daten im Anschluss stichpunktartig, schauen Sie beispielsweise ob `Schüler > Zeugnis > Fächer/Leistungen` gefüllt ist oder ob, wenn Sie Oberstufenschüler verwalten, ob die Karte `Abitur > Qualifikation` für einzelne Beispiele befüllt sind.

### Übernahme nicht übers Netzwerk

Es kann zu einem zeitlich immensen Unterschied kommen, wenn Sie während der Übernahme der Daten durch Ihr Netzwerk auf eine der beiden Datenbanken zugreifen.
Bitte legen Sie beide Datenbanken, also die leere MAGELLAN8.fdb und Ihre gefüllte MAGELLAN6.fdb auf dem gleichen Rechner ab.

!!! danger "Achtung"

    Bevor Sie die MAGELLAN6.fdb kopieren, stoppen Sie bitte den Firebirddienst unter `Start > Systemsteuerung > Verwaltung > Dienste`.

### Eigene Berichte

Magellan beinhaltet eine aktualisierte Schnittstelle zu Crystal Reports, damit können Sie neue Funktionen in Ihren Magellan-Berichten verwenden.
Aufgrund dieser technischen Veränderungen müssen Ihre selbsterstellte Berichte für die Verwendung in Magellan  8 angepasst werden.

Bitte folgen Sie hierzu der [Anleitung](https://doc.magellan.stueber.de/schulverwaltung/upgrade/berichte_anpassen/)!

### Sächsische Schulen

Ab Magellan 7 werden Schüler und Ihre Ausbildungen mittels einer GUID eindeutig gekennzeichnet, damit Sie später wiederkehrend Daten nach SAXSVS übergeben können und die Schüler anhand dieses Merkmals eindeutig identifiziert werden können. Wenn Sie die Datenübernahme aber nur für den Export nach SAXSVS durchführen, dann in Magellan 6 weiterarbeiten und später erst auf Magellan 7/8 umsteigen, dann wird beim späteren Umstieg auch die GUID neu erzeugt. Diese weicht dann natürlich von der in SAXSVS erwarteten GUID ab, eine Identifikation ist so nicht möglich. Ab dem Zeitpunkt, ab dem Sie Daten aus Magellan nach SAXSVS übergeben, muss auch im Alltag auf diese Magellan-Ausgabe umgestiegen werden.

### Schüler und Schülerkopien

Ab Magellan 7 werden Schüler, die mehrfach vorhanden sind und durch Kopieren von Schülern erzeugt wurden (Beim Kopieren erfolgt ein Übertrag der Originalschüler-ID ins Feld IDIntern der Schülerkopie), anders behandelt. Alle Kopien sind mit dem Original verbunden, eine Änderung von Stammdaten an einem der Schüler wird für alle anderen Übertragen. Das gilt nicht für alle Daten, beispielsweise die Zeugnisdaten existieren pro Datensatz, Ausbildungsdaten werden als Liste gezeigt. Einzelheiten beschreiben wir im Abschnitt ["Rückkehrer, parallele Laufbahn, parallele Bewerbung"](https://doc.Magellan.stueber.de/schulverwaltung/howto/sonderfaelle/#ruckkehrer-parallele-laufbahn-parallele-bewerbung)

Dieser neue Umgang muss bei der Übernahme der Daten aus Ihrer MAGELLAN6.fdb in die neue MAGELLAN8.fdb berücksichtigt werden. Dieses "Merken" der ID als IDIntern in Magellan 6 war dafür gedacht, dass beim Einschulen der Kopien die Auswahl "Zusammenführen" gewählt werden konnte und dann von einem der beiden Datensätze die Stammdaten übernommen wurden, die Laufbahn wurde zusammengeführt. Ob die Daten aus dem Bewerbermenü übernommen werden sollen, oder die Daten des Originals aus dem Schülermenü, konnte in den Optionen gewählt werden.

Im aktuellen Magellan gibt es diese Option nicht mehr, da es unerheblich ist an welchem Datensatz man einen Werte der Stammdaten ändert, die Änderung wird für alle zusammenhängenden Datensätze durchgeführt. Es gibt aus das "Zusammenführen" beim Einschulen so nicht mehr, der Assistent prüft selbstständig, ob eine Zusammenführen hier möglich ist oder nicht und führt die notwendigen Schritte aus.

#### Nicht zusammengeführte Schüler

Wenn Sie das Zusammenführen in der Version 6 nicht durchgeführt haben, dann gibt es Schülerkopien, die unabhängig von einander in Version 6 geführt wurden. Um diesen Umstand beizubehalten, leeren wir bei der Datenübernahme das Feld `IDIntern` für alle aktiven und inaktiven Schüler, damit bleiben diese Datensätze wie in Magellan 6 voneinander unabhängig.

#### Bewerber mit einer IDIntern

Bewerber, die zum Zeitpunkt der Datenübernahme mit einer `IDIntern` gekennzeichnet im Menü `Bewerber` sind, bleibt diese IDIntern erhalten. Durch diese Verknüpfung werden in Magellan jetzt automatisch die Stammdaten des Originalschülers gezeigt. Änderungen, die Sie an dem Bewerber in Magellan 6 vorgenommen haben, sind nicht sichtbar. Dieses Vorgehen ist für den Mehrwert der gleichen Datenlage umungänglich.

Was könnten Sie tun?

- Erfassen Sie die Abweichungen in Magellan erneut, egal ob beim Schüler oder beim Bewerber.
- Oder: Schulen Sie die Bewerber vorab in Magellan ein, wählen Sie beim Einschulen, ob zusammengeführt werden soll oder nicht.
- Erfassen Sie die Änderungen in Magellan 6 direkt beim Originalschüler.

## Wortersetzungen

Bei der Übernahme der Daten aus Ihrer Magellan 6-Datenbank in die Magellan 8-Datenbank können Ihre geänderten Feldbezeichnungen aus technischen Gründen nicht übernommen werden. Bitte tragen Sie  unter `Magellan 8 > Extras > Bezeichnungen anpassen > Spalte "durch"` Ihre gewünschten Bezeichnungen neu ein!

## Notwendige Schritte

|Notwendige Schritte |
|-|
|[1. ggfs. Magellan 6 und ggfs. Firebird aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#magellan-6-und-firebird-aktualisieren)|
|[2. 6er Datenbank vorbereiten](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#6er-datenbank-vorbereiten)|
|[3. Magellan 8 installieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#magellan-8-installieren)|
|[4. Daten aus Magellan 6 nach Magellan 8 übernehmen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#daten-aus-magellan-6-nach-magellan-8-ubernehmen)|

## Magellan 6 und Firebird aktualisieren

Um die Daten Ihrer Magellan 6-Datenbank in eine Magellan 8-Datenbank übernehmen zu können, muss die aktuellste Ausgabe von Magellan 6 und die dazugehörige Firebird-Ausgabe eingesetzt werden.

!!! info "Hinweis"

     Wenn Sie die letzte Ausgabe von Magellan 6 eingespielt haben und die empfohlene Ausgabe von Firebird (2.5.9) verwenden, ist hier nichts weiter zu tun.

Programm| Wo kann ich die Version überprüfen?
--|--
Magellan | Bitte vergleichen Sie die angezeigte Version (am besten der Serverrechner-Installation) unter `Magellan > Hilfe > Info über`  mit den angezeigten Version auf im [Downloadbereich](https://Magellan.stueber.de/download.php) oder im Abschnitt ["Was ist neu?"](https://doc.magellan6.stueber.de/changelog.html) der Magellan 6-Dokumentation!<br/> Bitte beachten Sie unsere Anleitungen zum Aktualisieren von [Magellan 6](https://doc.magellan6.stueber.de/installation/update.html)
FIREBIRD | Die Firebird-Versionsnummer sehen Sie unter `Serverrechner > Systemsteuerung > Firebird Server Manager (32-Bit)`. <br/> Ist es die -Ausgabe, die wir im [Downloadbereich](https://magellan.stueber.de/download.php) anbieten? Dann ist es die korrekte Ausgabe. <br/> Ist es eine ältere Ausgabe finden Sie im Abschnitt ["älteren Firebirdversionen"](https://doc.magellan6.stueber.de/installation/firebird-aktualisieren.html) der Magellan 6-Dokumentation eine Anleitung für das Aktualisieren.

## 6er Datenbank vorbereiten

Falls Sie es noch nicht mit Firebird 2.5.9 durchgeführt haben:
Bitte erstellen Sie eine [Sicherung](https://doc.magellan6.stueber.de/admin/db-connection.html#sicherungskopie-erstellen#sicherungskopie-erstellen) der MAGELLAN6.fdb und stellen aus der Datensicherung (*.fbk) [wieder eine neue Datenbank her](https://doc.magellan6.stueber.de/admin/db-connection.html#sicherungskopie-erstellen#sicherungskopie-wiederherstellen) und verwenden diese Datenbank für die Übernahme der Daten.

## Magellan 8 installieren

!!! info "Hinweis"

    Sollten Sie eine Datenübernahme wiederholen wollen, benötigen Sie eine "frische" leere Magellan 8 Datenbank. 
    Diese könnten Sie [hier](https://download.stueber.de/bin/de/assets/magellan/v8/database/MAGELLAN8.FDB) herunterladen.

Führen Sie im zweiten Schritt bitte die Installation von Magellan 8 aus, beide Version (6 + 8) können parallel auf einem Rechner laufen (haben aber getrennte Datenbanken). Eine ausführliche Installationsanleitung finden Sie im Abschnitt [Installation](https://doc.Magellan.stueber.de/schulverwaltung/installation/).

## Daten aus Magellan 6 nach Magellan 8 übernehmen

Im dritten Schritt werden in eine leere Magellan 8-Datenbank, die Daten aus Ihrer Magellan 6-Datenbank übergeben.

!!! warning "Wichtig"

    Bitte verwenden Sie einen leistungsstarken Rechner und legen beiden Datenbanken (die leere MAGELLAN8- und die gefüllte MAGELLAN6-Datenbank) auf diesem Rechner ab. Die Übertragung der Daten aus einer großen Datenbank kann viel Zeit in Anspruch nehmen, wenn die Daten dabei noch über Ihr Netzwerk übertragen werden, beeinflussen Sie diesen Prozess ungünstig.

1. Öffnen Sie bitte das Modul Magellan 8 Administrator und wählen den Unterpunkt `Datenbankpflege > Mandanten kopieren` und stellen die Variante `Magellan 6 nach Magellan 8` ein. Klicken Sie auf `Weiter`!

2. Das Übertragen der Magellan 6-Daten ist nur in eine leere aktuelle Magellan 8-Datenbank möglich. Bei der Installation von Magellan 8 wird Ihnen im Datenbankverzeichnis eine leere Datenbank mit dem Namen "MAGELLAN8.fdb".
![leere Datenbank im Format für Magellan 8](/assets/images/magellan.administrator/mandanten.kopieren6.1.png)

Sollten Sie den Übertrag bereits einmal durchgeführt haben, können Sie jederzeit [eine "frische" leere Datenbank im Magellan 8-Format herunterladen.](https://download.stueber.de/bin/de/assets/magellan/v8/database/MAGELLAN8.fdb)

Füllen Sie bitte die Felder (siehe untere Tabelle) des Assistenten aus, im oberen Teil verweisen Sie auf die Quelldatenbank (Magellan 6), im unteren Bereich auf die Zieldatenbank (Magellan 8).

![Eintragungen für die Quell- und Zieldatenbank](/assets/images/magellan.administrator/mandanten.kopieren8.1.png)

Feld|Anmerkung
--|--
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Quelldatenbank|Tragen Sie bitte den lokalen Pfad zur Quelldatenbank und deren Dateinamen ein.
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/Ip`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Zieldatenbank|Tragen Sie bitte den lokalen Pfad zur Zieldatenbank und deren Dateinamen ein. **Bitte beachten Sie, dass eine leere Zieldatenbank erwartet wird. Über das Symbol am Ende der Zeile können Sie eine leere Magellan 8 Datenbank herunterladen.**
Benutzernamen <br/> Kennwort|Tragen Sie als Benutzer bitte den sysdba und das dazugehörige Passwort ein.

Starten Sie anschließend den Assistenten mit `Weiter` und `Fertigstellen`.

!!! info "Hinweis"

     Die Datenübernahme aus Ihrer Magellan 6-Datenbank in die neue Magellan 8-Datenbank kann je nach Datenvolumen auch mehrere Stunden dauern. Bitte stellen Sie sicher, dass der verwendete Rechner auch aktiviert bleibt.

## Meldungen

Während der Datenübernahme können Ihnen Meldungen ausgegeben werden, die Ihnen Datensätze melden, die nicht übernommen werden können. Ursache dafür können Inkonsistenzen in Ihrer Datenbank sein. Es kann sein, dass die Meldungen dazudienen, Ihnen Datensätze zu zeigen, die Sie in Version 8 nachpflegen müssen.



Es könnten aber auch Fehlermeldungen sein, die anzeigen, dass an einer Stelle in Ihrer Datenbank die Daten nicht wie erwartet vorliegen. Diese Meldungen sollten nicht ignoriert werden, sondern gegebenenfalls sind Änderungen in Magellan 6 notwendig und ein erneuter Übertrag der Daten aus der korrigierten MAGELLAN6-Datenbank in eine neue leere Magellan8.fdb. 

Ein Beispiel für Meldungen:

```
[FireDAC][Phys][FB]validation error for column "Schularten"."Kuerzel", value "*** null ***"
Fehler beim Einfügen von Daten in die Tabelle "Schularten"
Kuerzel: 
EnbreaID: 
Schluessel: 
Bezeichnung: 
StatistikID: 
GueltigVon: NULL
GueltigBis: NULL
```

```
[FireDAC][Phys][FB]validation error for column "Sprachgruppen"."Kuerzel", value "*** null ***"
Fehler beim Einfügen von Daten in die Tabelle "Sprachgruppen"
Kuerzel: 
Schluessel: 
Bezeichnung: 
StatistikID: 
GueltigVon: NULL
GueltigBis: NULL
```

In diesem Fall ist die Ursache das in den genannten Verzeichnissen (Schularten, Sprachgruppen) Einträge ohne Kürzel enthalten sind oder Leerzeilen. Entfernen Sie diese Einträge oder pflegen Sie das Kürzel nach und starten einen neuen Übertrag.

Mit Meldungen, die Sie nicht selbst zuordnen können, sollten Sie sich an unser [Supportteam](https://support.stueber.de/) wenden, damit gegebenenfalls noch Korrekturen vorab vorgenommen werden können!

!!! info "Hinweis"

    Sollten Sie die Datenstruktur der Magellan 6 Datenbank verändert haben, müssen Sie diese Änderungen zurücksetzen um die Datenübernahme erfolgreich abschließen zu können.

## Pflege

!!! warning "Wichtig"

    Nachdem Sie Ihre Datenbank übernommen haben, führen Sie bitte im Magellan Administrator unter `Datenpflege` noch den Punkt `Aktuelle Bewerber-Ausbildung setzen` aus!

## Benutzeranmeldung

Wenn Version 8 auf einem anderen Serverrechner als die Version 6 läuft, dann muss die Passwortdatenbank (security2.fdb) von Firebird noch mit übernommen werden, also auf dem neuen Rechner an gleicher Stelle abgelegt werden.
Sie finden die `security2.fdb`  bei einer Standardfirebirdinstallation unter `C:\Program Files (x86)\Firebird\Firebird_2_5\`.

!!! danger "Achtung"

    Bitte beachten Sie, dass durch die veränderte Datenstruktur das `Zugriffsrechte synchronisieren` im Modul `Administrator` ausgeführt werden muss!

![Magellan Administrator > Benutzerverwaltung > Zugriffsrechte synchronisieren](/assets/images/update/01.png)

## Datenordner

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil Magellan 8 hier beispielsweise eine anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Nein| Unsere originalen Berichte sind für die Nutzung in Magellan 8 angepasst, [eigene Berichte müssen entsprechend angepasst werden](https://doc.magellan.stueber.de/schulverwaltung/upgrade/berichte_anpassen/).
Datenbank|Nein| Die Daten aus Ihrer Datenbank werden in die neue Datenbank übertragen.
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 8 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von Magellan 8 und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Aufgrund der geänderten Datenstruktur können Skripte aus Magellan 6 nicht unter Magellan 8 funktionieren, eine Übernahme würde hier schaden.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 8 ab.

## MyMagellan-Passworte

In Magellan 6 konnte im Magellan Administrator das Magellan-Passwort oder ein abweichendes Passwort angegeben werden, dass beim Erstellen der MYM-Dateien als Dateipasswort verwendet wird. Dieses Passwort wird in der Magellan6.fdb gespeichert und bei der Datenübernahme in die Magellan 8-Datenbank auch übergeben.

### Problem

Die Passwörter wurden chiffriert direkt in der Datenbank (Magellan6.fdb) gespeichert. Bei der Übernahme der Daten in die neue Magellan8.fdb wurden diese chiffrierten Werte in UTF-8 umgewandelt, womit sie nun nicht mehr mit den Klarpasswörtern übereinstimmen. Insofern können die bisherigen Passworte leider nicht ohne weitere Schritte interpretiert werden.

### Lösung

Die Passworte können über eine neue Importfunktion gesammelt für die MyMagellan-Teilnehmer vergeben und in der aktuellen Chiffrierung wieder eingelesen werden.

!!! tip "Tipp"

    Wenn Sie die bislang verwendeten Passworte nutzen möchten, können wir Ihnen auch im Rahmen des Magellan-Supportvertrages die alten Passworte aus der Magellan6.fdb auslesen und für die Nutzung in der csv-Datei zur Verfügung stellen. Bitte melden Sie sich hierfür über unser Ticketsystem.

!!! warning "Wichtig"

    Diese Schritte müssen **vor** dem Erstellen der MYM-Dateien ausgeführt werden.

Eine ausführlichere Anleitung finden Sie in der Anleitung für das Magellan Center im Abschnitt [Benutzereinstellungen exportieren und importieren](https://doc.magellan.stueber.de/mymagellancenter/verteilen/#benutzereinstellungen-exportieren-und-importieren). Nachstehend eine Kurzanleitung.

|So gehts:|
|--|
|1. Starten Sie bitte den Magellan-Administrator als sysdba oder als Benutzer mit dem Zusatzrecht `Mandantenadministrator` und rufen den Punkt `MyMagellan CENTER` auf. |
|Wählen Sie in der Menüleiste den Punkt `Benutzer exportiern` und erzeugen eine csv-Datei.|
|Öffnen Sie diese Datei, beispielsweise mit Excel, pflegen die Passworte ein und speichern das Ergebnis.|
|Wählen Sie in der Menüleiste den Punkt `Benutzer importieren` und verweisen auf die csv-Datei. Die Passworte werden in der Datenbank gespeichert und werden beim Erzeugen der MYM-Dateien verwendet.|

## MyMagellan-Dateiendungen

Unter MyMagellan 6 war die Dateiendung "mym", jetzt ist sie "mymx". Sie können die Endungen gesammelt ergänzen.

Exportieren Sie dazu in der `Benutzerverwaltung` die Benutzer in eine csv-Datei (Aufruf in der Menüleiste `Benutzer exportieren`), nutzen `Suchen und Ersetzen` Ihres Editors und ersetzen `.mym;` mit `.mymx;`. Importieren (Aufruf in der Menüleiste `Benutzer importieren`) Sie anschließend die Benutzer aus der Datei wieder.

## Eigene Berichte

Eigene Berichte müssen für die Nutzung unter Magellan 8  angepasst werden, eine Anleitung finden Sie im Punkt [Eigene Berichte anpassen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/berichte_anpassen/).