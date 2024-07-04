# Von Version 6 auf Version 9

!!! check "Benötigen Sie Hilfe beim Umstieg?"

    Bitte melden Sie sich unter [office@stueber.de](office@stueber.de) und nennen bitte Ihre Ausgangsversion, wir erstellen Ihnen eine Umstiegsangebot und vereinbaren für die Umstellung per Fernwartung einen Termin mit Ihnen. Wir stellen Ihren Serverrechner um, richten einen Client ein und konfigurieren und testen die Verbindung. Für weitere Clients geben wir Ihnen eine kurze Handlungsanweisung.
        Sollten Sie von Version 6 aus umsteigen möchten, können wir auch Ihre selbsterstellten oder angepassten Berichte für die aktuelle Version umstellen.

Um von Version 6 auf Version 9 umzusteigen, sind Zwischenschritte nötig, nachfolgend beschreiben wir die Schritte. Eine Installation der Version 8 oder Lizenz für Version 8 ist nicht notwendig.

Was|Wie
--|--
Alte SQL-Update-Skripte|Laden Sie das [Skriptpaket](https://my.hidrive.com/lnk/gtypCW3w) herunter, entpacken die enthaltenen Skripte nach der Installation der Version 9 auf dem Serverrechner in das Verzeichnis `C:\Users\Public\Documents\Stueber Systems\Magellan 9\Skripte\SQLUpdate`.
Leere `Magellan8.fdb`|In der nachfolgenden Anleitung ist beschrieben, dass Sie die leere `Magellan8.fdb` nutzen sollen. Diese Datenbank können Sie an folgender Stelle herunterladen: [Hier eine leere Datenbank im Magellan 8-Format herunterladen](https://download.stueber.de/bin/de/assets/magellan/v8/database/MAGELLAN8.fdb)
Anpassung von Version 6 auf 8|Im Magellan Administrator der Version 9 ist der Assistent zur Umstellung von Magellan 6 auf Magellan 8 enthalten. Installieren und lizenzieren Sie Magellan 9, verwenden den Assistenten wie im Abschnitt [Umstieg von 6 auf 8](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-9/#umstieg-von-magellan-6-auf-magellan-9) beschrieben.
Anpassung von Version 8 auf 9|Führen Sie anschließend die Anpassung der 8er Datenbank wie in der Anleitung unter [Umstieg von 8 auf 9](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-9/#umstieg-von-magellan-8-auf-magellan-9) durch. 
Eigene Berichte umstellen|Bitte denken Sie daran, dass die Berichte, die Sie in den Versionen vor Magellan 7 selbst erstellt oder angepasst haben, noch umgestellt werden müssen. Eine Anleitung finden Sie dafür hier: [Eigene Berichte anpassen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-9/#magellan-6-berichte-fur-7-oder-hoher-anpassen)

## Umstieg von Magellan 6 auf Magellan 9

!!! warning "Wichtig"

    Es empfiehlt sich **Magellan 6 und Magellan 9 nicht auf einem Rechner** zu verwenden, solange Magellan 6 noch verwendet wird. Es kann ansonsten Probleme bei der Anzeige von Berichten geben. Es werden für die neue Crystal Reports-Schnittstelle ein neuer Treiber und auch abweichende ODBC-Einstellungen vorausgesetzt. 

    Für den Umstieg von Magellan 6 auf Magellan 9 hingegen, spricht natürlich nichts dagegen, dieser Hinweis bezieht sich lediglich auf einen parallelen Einsatz der beiden Versionen.
  
### Was ist vorab zu beachten

#### Datenübernahme testen

Es empfiehlt sich mindestens einmal vorab die Datenübernahme zu testen, um sicherzustellen das beim Umstieg dann alles reibungslos läuft.
Bei der Übernahme können Meldungen ausgegeben werden, die müssten bitte geprüft und die Ursache behoben werden, mehr dazu im Abschnitt [Meldungen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-7/#meldungen).
Bitte kontrollieren Sie die Daten im Anschluss stichpunktartig, schauen Sie beispielsweise ob `Schüler > Zeugnis > Fächer/Leistungen` gefüllt ist oder ob, wenn Sie Oberstufenschüler verwalten, ob die Karte `Abitur > Qualifikation` für einzelne Beispiele befüllt sind.

#### Übernahme nicht übers Netzwerk

Es kann zu einem zeitlich immensen Unterschied kommen, wenn Sie während der Übernahme der Daten durch Ihr Netzwerk auf eine der beiden Datenbanken zugreifen.
Bitte legen Sie beide Datenbanken, also die leere MAGELLAN8.fdb und Ihre gefüllte MAGELLAN6.fdb auf dem gleichen Rechner ab.

!!! danger "Achtung"

    Bevor Sie die MAGELLAN6.fdb kopieren, stoppen Sie bitte den Firebirddienst unter `Start > Systemsteuerung > Verwaltung > Dienste`.

#### Sächsische Schulen

Ab Magellan 7 werden Schüler und Ihre Ausbildungen mittels einer GUID eindeutig gekennzeichnet, damit Sie später wiederkehrend Daten nach SAXSVS übergeben können und die Schüler anhand dieses Merkmals eindeutig identifiziert werden können. Wenn Sie die Datenübernahme aber nur für den Export nach SAXSVS durchführen, dann in Magellan 6 weiterarbeiten und später erst auf Magellan 7/8 umsteigen, dann wird beim späteren Umstieg auch die GUID neu erzeugt. Diese weicht dann natürlich von der in SAXSVS erwarteten GUID ab, eine Identifikation ist so nicht möglich. Ab dem Zeitpunkt, ab dem Sie Daten aus Magellan nach SAXSVS übergeben, muss auch im Alltag auf diese Magellan-Ausgabe umgestiegen werden.

##### Schüler und Schülerkopien

Ab Magellan 7 werden Schüler, die mehrfach vorhanden sind und durch Kopieren von Schülern erzeugt wurden (Beim Kopieren erfolgt ein Übertrag der Originalschüler-ID ins Feld IDIntern der Schülerkopie), anders behandelt. Alle Kopien sind mit dem Original verbunden, eine Änderung von Stammdaten an einem der Schüler wird für alle anderen Übertragen. Das gilt nicht für alle Daten, beispielsweise die Zeugnisdaten existieren pro Datensatz, Ausbildungsdaten werden als Liste gezeigt. Einzelheiten beschreiben wir im Abschnitt ["Rückkehrer, parallele Laufbahn, parallele Bewerbung"](https://doc.Magellan.stueber.de/schulverwaltung/howto/sonderfaelle/#ruckkehrer-parallele-laufbahn-parallele-bewerbung)

Dieser neue Umgang muss bei der Übernahme der Daten aus Ihrer MAGELLAN6.fdb in die neue MAGELLAN8.fdb berücksichtigt werden. Dieses "Merken" der ID als IDIntern in Magellan 6 war dafür gedacht, dass beim Einschulen der Kopien die Auswahl "Zusammenführen" gewählt werden konnte und dann von einem der beiden Datensätze die Stammdaten übernommen wurden, die Laufbahn wurde zusammengeführt. Ob die Daten aus dem Bewerbermenü übernommen werden sollen, oder die Daten des Originals aus dem Schülermenü, konnte in den Optionen gewählt werden.

Im aktuellen Magellan gibt es diese Option nicht mehr, da es unerheblich ist an welchem Datensatz man einen Werte der Stammdaten ändert, die Änderung wird für alle zusammenhängenden Datensätze durchgeführt. Es gibt aus das "Zusammenführen" beim Einschulen so nicht mehr, der Assistent prüft selbstständig, ob eine Zusammenführen hier möglich ist oder nicht und führt die notwendigen Schritte aus.

##### Nicht zusammengeführte Schüler

Wenn Sie das Zusammenführen in der Version 6 nicht durchgeführt haben, dann gibt es Schülerkopien, die unabhängig von einander in Version 6 geführt wurden. Um diesen Umstand beizubehalten, leeren wir bei der Datenübernahme das Feld `IDIntern` für alle aktiven und inaktiven Schüler, damit bleiben diese Datensätze wie in Magellan 6 voneinander unabhängig.

##### Bewerber mit einer IDIntern

Bewerber, die zum Zeitpunkt der Datenübernahme mit einer `IDIntern` gekennzeichnet im Menü `Bewerber` sind, bleibt diese IDIntern erhalten. Durch diese Verknüpfung werden in Magellan jetzt automatisch die Stammdaten des Originalschülers gezeigt. Änderungen, die Sie an dem Bewerber in Magellan 6 vorgenommen haben, sind nicht sichtbar. Dieses Vorgehen ist für den Mehrwert der gleichen Datenlage umungänglich.

Was könnten Sie tun?

- Erfassen Sie die Abweichungen in Magellan erneut, egal ob beim Schüler oder beim Bewerber.
- Oder: Schulen Sie die Bewerber vorab in Magellan ein, wählen Sie beim Einschulen, ob zusammengeführt werden soll oder nicht.
- Erfassen Sie die Änderungen in Magellan 6 direkt beim Originalschüler.

### Wortersetzungen

Bei der Übernahme der Daten aus Ihrer Magellan 6-Datenbank in die Magellan 8-Datenbank können Ihre geänderten Feldbezeichnungen aus technischen Gründen nicht übernommen werden. Bitte tragen Sie  unter `Magellan 8 > Extras > Bezeichnungen anpassen > Spalte "durch"` Ihre gewünschten Bezeichnungen neu ein!

### Notwendige Schritte

|Notwendige Schritte |
|-|
|[1. ggfs. Magellan 6 und ggfs. Firebird aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#magellan-6-und-firebird-aktualisieren)|
|[2. 6er Datenbank vorbereiten](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#6er-datenbank-vorbereiten)|
|[3. Magellan 8 installieren](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#magellan-8-installieren)|
|[4. Daten aus Magellan 6 nach Magellan 8 übernehmen](https://doc.magellan.stueber.de/schulverwaltung/upgrade/umstieg-von-6-auf-8/#daten-aus-magellan-6-nach-magellan-8-ubernehmen)|

#### Magellan 6 und Firebird aktualisieren

Um die Daten Ihrer Magellan 6-Datenbank in eine Magellan 8-Datenbank übernehmen zu können, muss die aktuellste Ausgabe von Magellan 6 und die dazugehörige Firebird-Ausgabe eingesetzt werden.

!!! info "Hinweis"

     Wenn Sie die letzte Ausgabe von Magellan 6 eingespielt haben und die empfohlene Ausgabe von Firebird (2.5.9) verwenden, ist hier nichts weiter zu tun.

Programm| Wo kann ich die Version überprüfen?
--|--
Magellan | Bitte vergleichen Sie die angezeigte Version (am besten der Serverrechner-Installation) unter `Magellan > Hilfe > Info über`  mit den angezeigten Version auf im [Downloadbereich](https://Magellan.stueber.de/download.php) oder im Abschnitt ["Was ist neu?"](https://doc.magellan6.stueber.de/changelog.html) der Magellan 6-Dokumentation!<br/> Bitte beachten Sie unsere Anleitungen zum Aktualisieren von [Magellan 6](https://doc.magellan6.stueber.de/installation/update.html)
FIREBIRD | Die Firebird-Versionsnummer sehen Sie unter `Serverrechner > Systemsteuerung > Firebird Server Manager (32-Bit)`. <br/> Ist es die -Ausgabe, die wir im [Downloadbereich](https://magellan.stueber.de/download.php) anbieten? Dann ist es die korrekte Ausgabe. <br/> Ist es eine ältere Ausgabe finden Sie im Abschnitt ["älteren Firebirdversionen"](https://doc.magellan6.stueber.de/installation/firebird-aktualisieren.html) der Magellan 6-Dokumentation eine Anleitung für das Aktualisieren.

#### 6er Datenbank vorbereiten

Falls Sie es noch nicht mit Firebird 2.5.9 durchgeführt haben:
Bitte erstellen Sie eine [Sicherung](https://doc.magellan6.stueber.de/admin/db-connection.html#sicherungskopie-erstellen#sicherungskopie-erstellen) der MAGELLAN6.fdb und stellen aus der Datensicherung (*.fbk) [wieder eine neue Datenbank her](https://doc.magellan6.stueber.de/admin/db-connection.html#sicherungskopie-erstellen#sicherungskopie-wiederherstellen) und verwenden diese Datenbank für die Übernahme der Daten.


### Daten aus Magellan 6 nach Magellan 9 übernehmen

Im dritten Schritt werden in eine leere Magellan 8-Datenbank, die Daten aus Ihrer Magellan 6-Datenbank übergeben.

!!! warning "Wichtig"

    Bitte verwenden Sie einen leistungsstarken Rechner und legen beiden Datenbanken (die leere MAGELLAN8- und die gefüllte MAGELLAN6-Datenbank) auf diesem Rechner ab. Die Übertragung der Daten aus einer großen Datenbank kann viel Zeit in Anspruch nehmen, wenn die Daten dabei noch über Ihr Netzwerk übertragen werden, beeinflussen Sie diesen Prozess ungünstig.

1. Öffnen Sie bitte das Modul Magellan 9 Administrator und wählen den Unterpunkt `Datenbankpflege > Mandanten kopieren` und stellen die Variante `Magellan 6 nach Magellan 9` ein. Klicken Sie auf `Weiter`!

2. Das Übertragen der Magellan 6-Daten ist nur in eine leere aktuelle Magellan 8-Datenbank möglich. [Eine "frische" leere Datenbank im Magellan 8-Format können Sie hier herunterladen.](https://download.stueber.de/bin/de/assets/magellan/v8/database/MAGELLAN8.fdb)

Füllen Sie bitte die Felder (siehe untere Tabelle) des Assistenten aus, im oberen Teil verweisen Sie auf die Quelldatenbank (Magellan 6), im unteren Bereich auf die Zieldatenbank (Magellan 8).

![Eintragungen für die Quell- und Zieldatenbank](/assets/images/magellan.administrator/mandanten.kopieren8.1.png)

Feld|Anmerkung
--|--
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/IP`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Quelldatenbank|Tragen Sie bitte den lokalen Pfad zur Quelldatenbank und deren Dateinamen ein.
Protokoll|Wählen Sie `lokal`für eine lokale gespeicherte Datenbank, wählen Sie `TCP/IP`für eine entfernt gespeicherte Datenbank.
Server|Falls Sie beim `Protokoll` den Wert `Server`gewählt haben, tragen Sie bitte den Namen des Serverrechners oder dessen IP-Adresse ein.
Zieldatenbank|Tragen Sie bitte den lokalen Pfad zur Zieldatenbank und deren Dateinamen ein. **Bitte beachten Sie, dass eine leere Zieldatenbank erwartet wird.**
Benutzernamen <br/> Kennwort|Tragen Sie als Benutzer bitte den sysdba und das dazugehörige Passwort ein.

Starten Sie anschließend den Assistenten mit `Weiter` und `Fertigstellen`.

!!! info "Hinweis"

     Die Datenübernahme aus Ihrer Magellan 6-Datenbank in die neue Magellan 8-Datenbank kann je nach Datenvolumen auch mehrere Stunden dauern. Bitte stellen Sie sicher, dass der verwendete Rechner auch aktiviert bleibt.

### Meldungen

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

### Pflege

!!! warning "Wichtig"

    Nachdem Sie Ihre Datenbank übernommen haben, führen Sie bitte im Magellan Administrator unter `Datenpflege` noch den Punkt `Aktuelle Bewerber-Ausbildung setzen` aus!

### Benutzeranmeldung

Wenn Version 8 auf einem anderen Serverrechner als die Version 6 läuft, dann muss die Passwortdatenbank (security2.fdb) von Firebird noch mit übernommen werden, also auf dem neuen Rechner an gleicher Stelle abgelegt werden.
Sie finden die `security2.fdb`  bei einer Standardfirebirdinstallation unter `C:\Program Files (x86)\Firebird\Firebird_2_5\`.

!!! danger "Achtung"

    Bitte beachten Sie, dass durch die veränderte Datenstruktur das `Zugriffsrechte synchronisieren` im Modul `Administrator` ausgeführt werden muss!

![Magellan Administrator > Benutzerverwaltung > Zugriffsrechte synchronisieren](/assets/images/update/01.png)

### Datenordner

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil Magellan 8 hier beispielsweise eine anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Nein| Unsere originalen Berichte sind für die Nutzung in Magellan 8 angepasst, [eigene Berichte müssen entsprechend angepasst werden](https://doc.magellan.stueber.de/schulverwaltung/upgrade/berichte_anpassen/).
Datenbank|Nein| Die Daten aus Ihrer Datenbank werden in die neue Datenbank übertragen.
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 8 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von Magellan 8 und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Aufgrund der geänderten Datenstruktur können Skripte aus Magellan 6 nicht unter Magellan 8 funktionieren, eine Übernahme würde hier schaden.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 8 ab.

### MyMagellan-Passworte

In Magellan 6 konnte im Magellan Administrator das Magellan-Passwort oder ein abweichendes Passwort angegeben werden, dass beim Erstellen der MYM-Dateien als Dateipasswort verwendet wird. Dieses Passwort wird in der Magellan6.fdb gespeichert und bei der Datenübernahme in die Magellan 8-Datenbank auch übergeben.

#### Problem

Die Passwörter wurden chiffriert direkt in der Datenbank (Magellan6.fdb) gespeichert. Bei der Übernahme der Daten in die neue Magellan8.fdb wurden diese chiffrierten Werte in UTF-8 umgewandelt, womit sie nun nicht mehr mit den Klarpasswörtern übereinstimmen. Insofern können die bisherigen Passworte leider nicht ohne weitere Schritte interpretiert werden.

#### Lösung

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

### MyMagellan-Dateiendungen

Unter MyMagellan 6 war die Dateiendung "mym", jetzt ist sie "mymx". Sie können die Endungen gesammelt ergänzen.

Exportieren Sie dazu in der `Benutzerverwaltung` die Benutzer in eine csv-Datei (Aufruf in der Menüleiste `Benutzer exportieren`), nutzen `Suchen und Ersetzen` Ihres Editors und ersetzen `.mym;` mit `.mymx;`. Importieren (Aufruf in der Menüleiste `Benutzer importieren`) Sie anschließend die Benutzer aus der Datei wieder.

## Umstieg von Magellan 8 auf Magellan 9

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

### Auf dem Server

#### Ausgangssituation prüfen und aktualisieren

Auf Ihrem **Serverrechner** stellen Sie bitte sicher, dass jeweils die aktuellste Ausgabe von `Magellan 8` und `Firebird 2.5.9` einsetzt wird. Die Versionen auf den Clientrechner müssen nicht aktualisiert werden.

Programm|Version auslesen
--|--
Magellan-Version|Die bei Ihnen eingesetzte Ausgabe von Magellan wird im Programm unter `Hilfe > Info über` gezeigt, die aktuell verfügbare Version können Sie in der [Changelog-Datei](https://doc.magellan.stueber.de/changelog/changelog/) sehen.
Firebird| Auf Ihrem Serverrechner unter `Systemsteuerung > Firebird Server Manager (32 Bit)` wird die Version gezeigt. Sie sollte mit der Version unter [https://magellan.stueber.de/download.php](https://magellan.stueber.de/download.php) gezeigten Version (aktuell 2.5.9) übereinstimmen.

Wenn es hier Abweichungen gibt, aktualisieren Sie bitte im ersten Schritt Magellan und ggfs. Firebird auf Ihrem Serverrechner, Anleitungen finden Sie unter:

* [Magellan-Updateanleitung](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/)
* [Firebird-Updateanleitung](https://doc.magellan.stueber.de/schulverwaltung/update/firebird-aktualisieren/)

#### Magellan 9 installieren und lizenzieren

Installieren Sie Magellan 9 auf Ihrem Serverrechner und auf den Clientrechnern.

!!! warning "Wichtig"

    Magellan 8 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unserer Anleitung für die Einrichtung und Lizenzierung des [Servers](https://doc.magellan.stueber.de/schulverwaltung/installation/version9/server.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von Magellan 9, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

#### 8er Datenbank übernehmen

Auf Ihrem Magellan-Serverrechner soll im nächsten Schritt die 8er Datenbank übernommen und für Magellan 9 angepasst werden. Führen Sie hierfür bitte die folgenden Schritte aus:

1. Öffnen Sie auf dem Serverrechner bitte `Systemsteuerung > Verwaltung > Dienste` und stoppen dort den Firebird-Dienst.<br/>
![Firebird-Dienst stoppen](/assets/images/update/8zu9/01.png)
2. Kopieren Sie aus dem Datenbankverzeichnis von Magellan 8 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 8\Datenbank`) Ihre Datenbank (Standardbenennung: `Magellan8.fdb`) und legen die Datei im Datenbankverzeichnis von Magellan 9 (Standardablageort: `C:\Users\Public\Documents\Stueber Systems\Magellan 9\Datenbank`) ab.
3. Sollte dort bereits eine Datei mit dem Namen `Magellan9.fdb` existieren, benennen Sie diese um oder verschieben sie, so dass Sie anschließend für Ihre `Magellan8.fdb` den Namen `Magellan9.fdb` verwenden können.
4. Öffnen Sie erneut den Punkt `Systemsteuerung > Verwaltung > Dienste` und starten dort den Firebird-Dienst wieder.<br/>
![Firebird-Dienst starten](/assets/images/update/8zu9/02.png)
5. Starten Sie Magellan 9 (Schulverwaltungsmodul, nicht den Administrator) als `sysdba` und führen Sie als erstes die Datensicherung durch. Der voreingestellte Sicherungspfad resultiert aus Ihren Angaben im Willkommensassistenten und kann im Magellan Administrator in den Verbindungseinstellungen auf der Unterkarte `Datensicherung` angepasst werden.<br/>
![Datenbanksicherung erstellen](/assets/images/update/8zu9/05.png)
6. Im Anschluss an die Datensicherung, klicken Sie bitte auf "Weiter", Magellan passt die Datenbank auf die neue Datenstruktur an.<br/>
![Datenbankstruktur anpassen](/assets/images/update/8zu9/06.png)
7. Öffnen Sie anschließend den Magellan 9 Administrator und synchronisieren die Zugriffsrechte im Punkt `Benutzerverwaltung` über den Aufruf  `Zugriffsrechte synchronsieren` in der Menüleiste. Damit werden für Ihre bereits angelegten Benutzer die Zugriffsrechte auf die geänderte Datenbankteile geklärt.<br/>
![Zugriffsrechte synchronisieren](/assets/images/update/8zu9/04.png)

#### Eigene Daten übernehmen

Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese bitte und legen Sie in der neuen Verzeichnisstruktur von Magellan 9 ab.

!!! warning "Wichtig"

    Bitte legen Sie **nur Ihre zusätzlichen Dateien** in der neuen Verzeichnisstruktur ab und ersetzen Sie bitte nicht die Verzeichnisse! 

Aus einigen Datenordnern sollten Daten übernommen werden, aus anderen Datenordnern dürfen Daten NICHT übernommen werden, weil Magellan 9 hier beispielsweise einen anderen Aufbau erwartet.

Datenordner | Übernahme | Hinweise
--|--|--
Berichte|Ja| Bitte je Unterverzeichnis nur Ihre selbsterstellten oder angepassten Berichte übernehmen, bitte nicht den gesamten Ordnerinhalt oder ganze Ordner übertragen, Sie überschreiben sich ansonsten ggfs. aktuellere Varianten.
Datenbank|Ja| Die Magellan 7 oder Magellan 8 Datenbank bitte mit neuer Bezeichnung (MAGELLAN9.fdb) in den Datenbankordern der Version 9 ablegen, dabei die dort vorhandene gleichnamige Datenbank ersetzen oder vorab umbenennen. 
Dokumente|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Dokumente` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 9 ab.
Importe|Nein| Die Dateien unterscheiden sich im Aufbau nicht, durch die Installation von Magellan 9 und spätere Updates haben Sie jederzeit die aktuellsten Ausgaben der importierbaren Keys-Dateien.
Skripte|Nein| Sollten Sie eigene angepasste oder selbsterstellte Skripte einsezten, können Sie diese Dateien in der neuen Struktur ablegen.
Vorlagen|Ja| Bitte kopieren Sie alle Unterverzeichnisse unterhalb von `Vorlagen` und legen die Verzeichnisse im gleichnamigen Unterverzeichnis für Magellan 9 ab.

### Auf den Clientrechnern

#### Magellan 9 installieren und lizenzieren

!!! warning "Wichtig"

    Magellan 8 stört dabei nicht, sollte aber nicht dauerhaft auf den Rechnern bleiben, um versehentliche Dateneingaben im verkehrten Programm vorzubeugen - beide Programmversionen arbeiten auf verschiedenen Datenbanken.

Folgen Sie unserer Anleitungen für die Einrichtung und Lizenzierung der [Clients](https://doc.magellan.stueber.de/schulverwaltung/installation/version9/arbeitsplatz.installieren/).

!!! warning "Wichtig"

    Kunden mit einem gültigen Supportvertrag erhalten Ihre neue Lizenz von unserem Office-Team parallel zur Veröffentlichung von Magellan 9, sollten Sie Ihre Lizenz nicht erhalten haben oder möchten Sie eine Lizenz erwerben, schreiben Sie bitte an office@stueber.de.

#### Empfehlung

Wir empfehlen Ihnen Magellan auf einem Clientrechner zu installieren, zu lizenzieren und zu konfigurieren. Die Lizenzdaten und die Konfigurationsdaten können anschließend zentral abgelegt werden. Somit wäre ab dem zweiten Clientrechner nur die Installation notwendig und Sie legen zusätzlich eine Datei ab, die die Pfade enthält, von denen Magellan die Lizenz- und Konfigurationdaten lesen soll.

Nach der Installation auf dem ersten Clientrechner starten Sie bitte Magellan 9 um den Willkommens-Assistenten zu durchlaufen. Im Willkommensassistenten gibt man die Lizenzdaten, die Pfade aus Sicht des Clientrechners zur Datenbank und zu den Datenordnern ein, wählt eine Option für die Region. Diese Eingaben werden in Dateiform gespeichert und können auch für weitere Clients genutzt werden.

Testen Sie anschließend auf dem ersten Clientrechner, ob die Angaben korrekt waren.<br/>
**Test 1 (Datenbankpfad):** Dafür starten Sie Magellan auf dem Rechner, gelingt der Start des Moduls, ist der Pfad zur Datenbank ok.<br/>
**Test 2 (Datenordnerpfade):** In Magellan wechseln Sie in das Menü Schüler, markieren einen Schüler und drücken bitte STRG+P. Werden Schülerberichte zur Auswahl gezeigt, sind die Pfade zu den Datenordnern ok.

Die durch den Willkommens-Assistenten erzeugten Dateien, aus den die Lizenz, die Optionen und die Pfade ausgelesen werden, finden Sie unter `C:\ProgramData\Stueber Systems\Magellan 9`. Diese Dateien können Sie zentral ablegen und von allen Clientrechnern aus nutzen. Damit beim Programmstart von Magellan nicht die lokalen Daten ausgelesen werden, sondern die zentral abgelegten Dateien gelesen werden, muss eine Textdatei mit den Pfaden und einem bestimmten Namen angelegt und an einer bestimmten Stelle abgelegt werden. Bitte folgen Sie hierfür unserer Anleitung unter: [Die Pathsdatei](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei/).

Die erzeugte Datei legen Sie auf allen anderen Clientrechnern (nicht auf dem Server!) nach der Installation bitte unter `C:\Program Files (x86)\Stueber Systems\Magellan 9` ab. Damit entfallen weitere Schritte zur Lizenzierung und Konfiguration.

## Magellan 6-Berichte für 7 oder höher anpassen

Aufgrund technischer Veränderungen in Magellan 7 und 8 müssen Berichte aus Magellan 6 für die neueren Version angepasst werden.

!!! warning "Wichtig"

    Berichte, die für Magellan 6 genutzt wurden, müssen vor der Verwendung in Magellan 7 oder 8 angepasst werden. Berichte, die bereits unter Magellan 7 oder höher verwendet wurden, müssen NICHT für den Einsatz unter Magellan 8 angepasst werden.

Alle mitgelieferten Originalberichte von STÜBER SYSTEMS wurden angepasst und ausgeliefert.
Berichte, die von Schulen verändert worden sind oder selbsterstellte Berichte liegen im Verantwortungsbereich der Schulen. Im Folgenden erläutern wir die Gründe und die notwendigen Anpassungen.

!!! warning "Wichtig"

    Wenn Sie unsere ausgelieferten Magellan 7-Berichte als Vorlage für eigene Anpassungen nutzen möchten, benötigen Sie mindestens die Ausgabe `CRYSTAL REPORTS 2013`. 
    Um Ihre eigenen Berichte für Magellan 7 anzupassen benötigen Sie mindestens `CRYSTAL REPORTS 2011`.

### Beauftragen Sie uns

Sie können Ihre Berichte nach der untenstehenden Anleitung umstellen oder uns beauftragen.
Schreiben Sie uns bitte eine Nachricht unter dem **Stichwort "Angebot: Magellan 6-Berichte umstellen"** an [office@stueber.de](mailto:office@stueber.de), wir erstellen Ihnen gern ein Angebot, schreiben Ihnen die weiteren Schritte und erstellen Ihnen ein Uploadverzeichnis usw.

### Schritte zum Bericht umstellen

#### Magellan unterstützt Unicode

Dies ist grundsätzlich eine erfreuliche Nachricht, da ab Version 7 sämtliche Schriftzeichen in der Magellan-Datenbank gespeichert werden können. Beispielsweise alle Namensschreibweisen sind nun möglich und auch für den Zeugnisdruck ausgebbar.  
Bedingt durch diese Umstellung benötigt Magellan 7 aber einen aktualisierten ODBC-Treiber, der Unicode verarbeiten kann.
Der bisherige ODBC-Treiber ist mittlerweile in die Jahre gekommen und für die neuen Anforderungen nicht geeignet.

!!! info "Hinweis"

    Wir empfehlen für die Änderung der eigenen Berichte sich eine lokale Magellan 7-Installation einzurichten. 

!!! warning "Wichtig"

    Während Tests mit dem neuen ODBC-Treiber und unseren Berichten ist aufgefallen, dass viele Berichte eine Fehlermeldung produzierten, die nach Recherchen auf problematische Datenbank-Abfragen zurückzuführen sind, die ältere Crystal-Reports Versionen produzieren. Der ältere ODBC-Treiber, der in Magellan 6/6.5 Verwendung findet, scheint dahingehend fehlertolerant zu sein, verweigert der neuere Treiber die Verarbeitung und erzeugt einen Fehler.

#### Was ist zu tun - eine Übersicht

Nr.|Was ist zu tun
--|--
1.|[ODBC-Treiber-Einstellungen](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#1-odbc-treiber-einstellungen)
2.|[ggfs. Datenbankverbindung aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#6-datenbankverbindung-aktualisieren)
3.|[Datenquellenpfad festlegen](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#3-datenquellenpfad-festlegen)
4.|[Tabellenverknüpfungen anpassen](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#4-tabellenverknupfungen-anpassen)
5.|[Test](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#5-test)

#### 1. ODBC-Treiber-Einstellungen

Um das Problem beheben zu können, müssen wir fehlerfrei auf die Datenbank zugreifen können. Das funktioniert nur, wenn wir zuvor ein paar Einstellungen an den ODBC-Treiber weitergeben.

!!! info "Hinweis"

    Diese Einstellungen sind nur notwendig um die Anpassungen an Ihren eigenen Berichten vorzunehmen. Für den Druck und die Druckvorschau aus Magellan gibt es andere Voreinstellungen. 
    Die für Magellan notwendigen Druckeinstellungen in der ODBC-Anbindung werden automatisch beim Aufruf der Druckvorschau gesetzt.

|Gehen Sie wie folgt vor:|
|:--|
|1. Starten Sie den ODBC-Datenquellen-Administrator (32-Bit) in Windows.<br>Auf der Registerkarte ```Treiber``` finden Sie den aktuellen mit Magellan 7 installierten Treiber. Da muss mindestens die im Bild angegeben Version stehen.
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/odbc_1_Treiber.png>|
|**Bitte achten Sie darauf, dass Ihr zu ändernder Bericht währenddessen noch nicht in Crystal Reports geladen ist!**|
|2. Wechseln Sie auf die Registerkarte ```Benutzer-DSN``` und wählen Sie den Eintrag ```Magellan-CR``` aus. Dieser wird von Magellan automatisch erstellt. Finden Sie keinen solchen Eintrag, dann starten Sie Magellan 7 und öffnen einen Bericht in der Vorschau. Danach sollte der Eintrag vorhanden sein. Klicken Sie auf ```Konfigurieren```.
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/odbc_2_BenutzerDSN.png>|
|2. Im Konfigurationsfenster geben Sie bei ```Character Set``` den Wert ```NONE``` ein, oder wählen diesen aus. Im Bereich ```Extended identifiert properties``` setzen Sie bitte **alle** Häkchen.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/odbc_3_KonfigurationKorrektur.png>|

!!! info "Hinweis"

     Wenn Sie zwischenzeitlich Magellan auf dem Rechner (Druckvorschau!) verwendet haben, ändert sich diese Einstellung wieder. 
     Bitte kontrollieren Sie vor dem erneuten Start von Crystal Reports diese Einstellungen.

!!! danger "Achtung"

    Ihr Fenster sieht nicht so aus wie in der vorstehenden Abbildung? Dann bitte über den nachstehenden Link das Installationspaket des ODBC-Treibers laden. Anschließende Magellan bitte schließen und die Installation ausführen. 

Downloadseite|Eintrag
--|--
[https://firebirdsql.org/en/odbc-driver/](https://firebirdsql.org/en/odbc-driver/) | Windows 32-bit Full Install

#### 2. Datenbankverbindung aktualisieren

Wenn Sie auf einem Rechner arbeiten, mit dem Sie üblicherweise Ihre Crystal-Reports Berichte bearbeiten, dann legt Crystal-Reports gerne mehrere Datenquellen zur ODBC-Verbindung an. Um da für die Korrektur nicht durcheinander zu kommen, räumen wir an der Stelle auf.

Die vorstehende Meldung taucht allerdings auf, weil in der Datenbankverbindung, mit der Sie gerade angemeldet sind, nicht der korrekte Zeichensatz verwendet wird. 
Per `Rechtsklick > Eigenschaften`auf eine Verbindung können Sie den Unterschied sehen.

Diese Einstellung kann man nicht direkt editieren, letztlich muss eine neue korrekte Verbindung angelegt werden.

![Falscher Zeichensatz in der Verbindung](/assets/images/berichte.anpassen/berichte.anpassen4.png)![Richtiger Zeichensatz in der Verbindung](/assets/images/berichte.anpassen/berichte.anpassen5.png)  

|Gehen Sie wie folgt vor:|
|:--|
|1. Klicken Sie im Menu auf ```Datenbank > Bei Server an-/abmelden...```|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/berichte.anpassen3.png>|
|2. Melden Sie sich zuerst über die ```Abmelden``` Schaltfläche von allen Verbindungen ab. Wenn die Schaltfläche `Abmelden` für alle Verbindungen grau ist, dann sind sie auch nirgends angemeldet. |
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step1_2.png>|
|3. Im Daten-Explorer sollte unter `Meine Verbindungen` nur eine Verbindung stehen.<br>Wenn Sie mehrere Verbindungen finden, löschen Sie alle (bei denen es möglich ist), wie folgt heraus:|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step1_3.png>|
|4. Benennen Sie die verkehrte(n) Datenbankverbindung um (Rechtsklick > Umbenennen), damit keine der bisherigen Verbindungen mehr "Magellan-CR" heißt und legen anschließend eine neue Datenbankverbindung an.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/berichte.anpassen6.png>|
|5. Öffnen Sie die neue Datenbankverbindung, indem Sie auf das Plus vor "Magellan-CR" und anschließend auf das Plus vor "Tabellen" klicken.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/berichte.anpassen7.png>|
|6. Melden Sie sich wieder an und testen die Vorschau, jetzt sollte es klappen!|

#### 3. Datenquellenpfad festlegen

Fehlermeldungen:

![Meldung](/assets/images/berichte.anpassen/cr_error_msg1.png) 

![Meldung](/assets/images/berichte.anpassen/cr_error_msg2.png)

!!! warning "Wichtig"

    Die nachfolgenden Schritte sind **für den Hauptbericht und aus allen Unterberichten heraus** durchzuführen.

|So gehen Sie vor:|
|:--|
|1. Öffnen Sie zusätzlich zum Hauptbericht alle Unterberichte. Starten Sie aus dem Hauptbericht.|
|2. Klicken Sie im Menü auf ```Datenbank > Datenquellenpfad festlegen...```|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_1.png>|
|3. Im Dialogfenster wählen Sie wie im Bild beschrieben zuerst oben die erste Ansicht/Tabelle aus.<br> Dann öffnen Sie unten die bestehende Verbindung und melden sich an.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_2.png>|
|4. Im Beispiel ist das erste Element ```AuswahlZeugnisse``` eine Ansicht.<br> Das heißt, sie öffnen im unteren Bereich ```Ansichten```.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_3.png>|
|5. Wählen die Ansicht auch im unteren Bereich aus. Dann klicken Sie auf ```Aktualisieren```.|
|**ACHTUNG: Ein Doppelklick wird hier von Crystal Reports nicht korrekt verarbeitet, bitte nutzen Sie die Schaltfläche `Aktualisieren` oder die Taste `Enter`.**|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_4.png>|
|5. Den Vorgang wiederholen Sie mit allen Ansichten/Tabellen die in Ihrem Bericht vorhanden sind.<br>Auch mit den Ansichten/Tabellen von Unterberichten.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_5.png>|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_6.png>|
|6. Sonderfall ```SchuelerKlassen```<br>Die SchuelerKlassen haben eine neue Datenstruktur und Crystal-Reports kennt im bestehenden Bericht lediglich die alte Datenstruktur. Damit kann die Tabelle nicht einfach neu verknüpft werden. Sie erhalten deshalb ein weiteres Dialogfenster, dass Sie lediglich mit ```OK``` quittieren.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_7.png>|
|**Wichtig: Wiederholen Sie diese Schritte bitte auch jeweils aus den vorab geöffneten Unterberichten heraus.**|

#### 4. Tabellenverknüpfungen

Außerdem sind ab Magellan 7 einige wichtige Umstellungen in der Datenbankstruktur vorgenommen worden, um neue und verbesserte Funktionalitäten abbilden zu können. Dadurch sind einige Felder entfernt und an anderer Stelle hinzugekommen.

Sie öffnen bitte den Punkt `Datenbank-Assistent..`und rufen die Unterkarte `Verknüpfungen` auf.

!!! info "Hinweis"

    Prüfen Sie, ob die folgenden Tabellen oder Felder **im Bericht oder in einem Unterbericht** genutzt wurden, was dann zu tun ist, wird nachstehend beschrieben. Bitte denken Sie daran, dass der Punkt `Datenbank > Datenbank-Assistent > Unterkarte Verknüpfungen` immer nur die Verknüpfungen für den gerade gewählten Hauptbericht oder den ausgewählten Unterbericht zeigt. Bitte prüfen Sie auch die Verknüpfungen in den Unterberichten.

Tabelle |Feld
--|--
Schueler und SchuelerAusbildung|[Verknüpfungen lösen](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schuelerzeitraeume-und-schuelerausbildung)
Schueler|[ehemalige Felder: SopaedFoerderungen, Foerderschwerpunkt1, Foerderschwerpunkt2 und Behinderung ](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schueler)
SchuelerZeitraeume und SchuelerKlassen|[Neue Verknüpfungen](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schuelerklassen)
SchuelerZeitraeume und SchuelerAusbildung|[Neue Verknüpfungen](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schuelerzeitraeume-und-schuelerausbildung)

!!! info "Hinweis"

    Wenn keine der Tabellen oder keines der Felder genutzt wurde, können Sie speichern und zum Test die Druckvorschau (bei mehrseitigen Berichten bitte auch auf die weiteren Seiten blättern) aufrufen. Klappt alles, ist der Bericht fertig für die Nutzung in späteren Magellan Versionen.

!!! info "Hinweis"

    Die aktuelle Datenstrukturbeschreibung finden Sie als Teil der Dokumentation [Magellan TOOLBOX](https://doc.magellan-toolbox.stueber.de/).

##### "SchuelerZeitraeume" und "SchuelerAusbildung"

Das Feld `Ausbildung` ist in der Tabelle `Schueler` weiterhin vorhanden, bildet aber nicht mehr die aktuelle "Ausbildung" ab.

!!! warning "Wichtig"

     Bitte löschen Sie die Verknüpfungen zwischen der Tabelle "Schueler" und der Tabelle "SchuelerAusbildung". 
     Setzen Sie stattdessen die Verbindungen zwischen der Tabelle "SchuelerZeitraeume" und der Tabelle "SchuelerAusbildung".

Die neue Verknüpfung muss wie folgt aussehen:

Tabelle und Feld|Art der Verbindung|Tabelle und Feld
--|--|--
SchülerZeitraeume| - |SchuelerAusbildung
Mandant|linke äußere Verknüpfung<br/>(left outer join)|Mandant
Ausbildung|linke äußere Verknüpfung<br/>(left outer join)|ID

![SchuelerAusbildung](/assets/images/berichte.anpassen/cr_fix_schuelerAusbildung.png)

##### Schueler

Die Felder folgenden Felder sind nicht mehr in der Tabelle "Schueler" zu finden, sondern wurden in die neue Tabelle "SchuelerFoerderungen" verschoben, da es sich jetzt um eine Liste von Fördermaßnahmen/Behinderung/Schwächen handelt.

* "SopaedFoerderungen"
* "Foerderschwerpunkt1"
* "Foerderschwerpunkt2"
* "Behinderung"

##### SchuelerKlassen

Wenn die Tabelle "SchuelerKlassen" in Berichten verwendet wurde, dann musste Sie mit den Feldern "Schueler", "Klasse", "Zeitraum" verknüpft werden. Diese Felder gibt es in der Tabelle nicht mehr, dafür gibt es das Feld "SchuelerZeitraumID". Die Tabelle wird dann aus der Tabelle "SchuelerZeitraeume" Feld "ID" verknüpft. Folgende Fehlermeldung könnten Sie in der Vorschau erhalten:

![SchuelerKlassen](/assets/images/berichte.anpassen/cr_error_msg3.png)

Die Verknüpfung wird wie folgt korrigiert:

![SchuelerKlassen](/assets/images/berichte.anpassen/cr_fix_schuelerKlassen.png)

Tabelle und Feld|Art der Verbindung|Tabelle und Feld
--|--|--
SchülerZeitraeume|-|SchuelerKlassen
Mandant|linke äußere Verknüpfung<br/>(left outer join)|Mandant
ID|linke äußere Verknüpfung<br/>(left outer join)|SchuelerZeitraumID

##### Empfohlene Verknüpfung

Eine Empfehlung finden Sie im Artikel ["Empfohlene Verknüpfung"](https://doc.kb.stueber.de/cr/verknuepfung.html) in unserer Knowledge-Base.

#### 5. Test

Speichern Sie Ihre Änderungen und wählen Sie anschließend `F5` (oder rufen die Vorschau über das Symbol auf). Wird die Vorschau gefüllt (bei mehrseitigen Berichten bitte auch einmal blättern)? Dann ist der Bericht jetzt für Magellan 7 vorbereitet.

#### Sollte es noch weitere Probleme geben

##### arithmetic exception, numeric overflow

Sie erhalten diese Meldung? Dann folgen Sie bitte dem  Punkt der Anleitung: [2. Datenbankverbindung aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#2-datenbankverbindung-aktualisieren)

![Meldung](/assets/images/berichte.anpassen/berichte.anpassen2.png)

##### Keine Datenbankverbindung möglich

Wir empfehlen für die Änderung der Berichte auf eine lokale Magellan 7-Installation zuzugreifen.

##### Die Vorschau lädt und lädt

Wenn Sie alle vorstehenden Punkte befolgt haben, die Vorschau aber noch immer dauerhaft lädt, ist vermutlich eine vergessene Verknüpfung in einem Unterbericht die Ursache.

Die Übersicht der Verknüpfungen gilt für den jeweils gewählten Bericht oder Unterbericht. Bitte schauen Sie, ob es Unterberichte in Ihrem Bericht gibt und überprüfen Sie bitte die Verknüpfungen unter `Datenbank > Datenbank-Assistent > Unterkarte Verknüpfungen` während der Unterbericht geöffnet ist.

##### Operation noch nicht implementiert

Erscheint die Meldung in der Magellan-Vorschau oder in der Crystal Reports-Vorschau?

Dann handelt es sich vermutlich um einen Bericht, der den Inhalt eines Feldes als Barcode darstellen soll. Für die Darstellung als Barcode wird die Schriftart [Code EAN 13](https://download.stueber.de/bin/de/common/fonts/ean13.ttf) verwendet. Die Schriftart fehlt auf Ihrem Rechner oder ist nicht korrekt installiert, bitte laden Sie sie herunter und installieren Sie diese Schriftart per Doppelklick auf dei Datei neu!

!!! tip "Tipp"

    Klappt die Vorschau von Berichten mit Barcode direkt nach dem MAGELLMA-Update nicht? 
    Bitte starten Sie Ihren Rechner einmal neu, anschließend sollte die Schriftart, die zur Anzeige von Barcodes verwendet wird, verfügbar sein.

##### Die Tabelle wurde nicht gefunden

In Crystal Reports klappt die Vorschau, Magellan meldet aber "Die Tabelle wurde nicht gefunden"?

![Meldung "Die Tabelle wurde nicht gefunden"](/assets/images/berichte.anpassen/berichte.anpassen9.png)

Dann öffnen Sie bitte den Bericht in Crystal Reports und stellen sicher, dass unter `Datei > Berichtsoptionen > Allgemeine Einstellungen` das Häkchen vor `Beim ersten Regenerieren überprüfen` **nicht** aktiviert ist.

!!! danger "Achtung"

    Diese Einstellungen muss bitte für den Bericht **und auch für alle Unterberichte** deaktiviert sein.

![Dieses Häkchen darf NICHT aktiviert sein](/assets/images/berichte.anpassen/berichte.anpassen8.png)

##### Failed to save document

Manche Berichte lassen sich nicht speichern, auch nicht über `Speichern unter`.
Eine mögliche Ursache dafür kann sein, dass ein Unterbericht im Detailbereich eingebunden wurde. Ändert man das, lässt sich der Bericht auch normal speichern.

![Failed to save document](/assets/images/berichte.anpassen/cr.nicht.speicherbar.jpg)

##### Schüler wird wiederholt angezeigt

  Sollten Sie in einem Zeugnis das Problem haben, dass der in Magellan in der Vorschau geladene Schüler beim Test der Vorschau in Crystal Reports immer wieder nacheinander gezeigt wird, kontrollieren Sie bitte die Verknüpfungen der Tabellen `KlassenZeitraeume` und `Klassen`.

![Verknüpfung](/assets/images/berichte.anpassen/berichte.anpassen10.png)

##### Der verkehrte Schüler wird angezeigt

  In einigen alten Berichten wurde die Tabelle `SchuelerKlassen` statt der Tabelle `KlassenZeitraeume` verwendet.
  Das die Verknüpfung nicht stimmt, kann man z.b. daran bemerken, dass ein verkehrter Schüler statt des ausgewählten Schülers angezeigt wird.

Was können Sie tun:

1. Kontrollieren, ob bereits Felder aus `SchuelerKlassen` genutzt wurden.
2. Wenn nicht, dann die Verknüpfungen lösen und `KlassenZeitraeume` einfügen.
3. Verknüpfen wie in der Abbildung.

![KlassenZeitraeume verknüpfen](/assets/images/berichte.anpassen/04.png)

##### Es werden mehr als die ausgewählten Datensätze gezeigt

Problem: Sie wählen in Magellan nur wenige Datensätze aus um die Auswahltabellen zu füllen (Drucken > Vorschau), in der Crystal Reportsvorschau werden aber dennoch immer alle Datensätze aufgerufen.

Eine mögliche Ursache kann folgender Punkt sein:

CR optimiert vor dem Aufruf des Berichtes selbständig (und nicht unterdrückbar) die Abfrage. Gerade bei sehr einfachen Berichten kann das eigenständige Optimieren zu merkwürdigen Nebeneffekten führen. Was hilft, ist ein Feld im oberen Bereich des Berichtes einzufügen und dann zu unterdrücken.

![Feld einfügen und ausblenden](/assets/images/berichte.anpassen/01.png)