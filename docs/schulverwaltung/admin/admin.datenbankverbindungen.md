# Datenbankverbindungen

Das Programm MAGELLAN kann mit mehreren Datenbanken verbunden werden. Bei der Anmeldung an dem Schulverwaltungsmodul wird später eine Verbindung ausgewählt, die auf eine bestimmte Datenbank und Datenordner (Skripte, Berichte, Vorlagen usw.) verweist. Damit könnten auf einem Serverrechner mehrere Datenbanken (zum Beispiel mehrerer Schulen)parallel abgelegt werden, der Nutzer erhält über die Rechtevergabe in der Benutzerverwaltung dann das Recht sich an einer oder an mehreren Verbindungen anzumelden.

Bei der Installation von MAGELLAN werden zwei Datenbanken angelegt: eine leere Datenbank, in die Ihre Schulverwaltungsdaten aus der Version 6 übernommen oder auch neue Daten über das MAGELLAN-Importformat importiert werden können und eine Beispieldatenbank mit Testdaten (Magellan_Beispiel.fdb). 
Eine neue Verbindung können Sie oben links über die Schaltfläche `Neuer Datensatz`anlegen!

![Klicken Sie auf `Neuer Datensatz`!](/assets/images/magellan.administrator/neuer.datensatz.png)

## Unterpunkt Verbindung

Auf dieser Karte wird standardmäßig der Aliasname "Magellan" vorgeschlagen, passen Sie die Bezeichnung nach Wunsch an, gibt es nur eine Verbindung, muss keine Anpassung erfolgen. Der Alias wird bei der Anmeldung an MAGELLAN im Feld Datenbank bezeichnet. 

![Wählen Sie den `Aliasnamen`!](/assets/images/magellan.administrator/neue.verbindung.png)

## Unterpunkt Datenbank

Feld|Anmerkung
--|--
Protokoll|`TCP/IP`: <br/>Wählen Sie diesen Wert, wenn die Datenbank nicht auf dem lokalen Rechner liegt.<br/> `Lokal`:<br/> Wählen Sie diesen Typ, wenn die Datenbank sich auf dem lokalen Rechner befindet. Diese Auswahl ist für die Installationstypen `Server-/Einzelplatz` gedacht.
Server|Wenn Sie für das `Protokoll` `TCP/IP` gewählt haben, tragen Sie bitte den Namen des Servers oder die IP-Adresse des Servers ein. <br/>Haben Sie für das Feld `Protokoll` den Wert `Lokal` gewählt, ist das Feld `Server` ausgegraut.
Dateipfad auf dem Serverrechner|Tragen Sie hier Pfad zur Datenbank und die Bezeichnung der Datenbank ein. <br/>Wichtig ist, dass der Pfad immer aus Sicht des Servers erwartet wird. <br/>In den meisten Fällen steht in diesem Feld in der Verbindung des Servers der identische Pfad wie in der Verbindung des Clientrechners
Region|Bitte wählen Sie Ihre Region aus, zur Verfügung steht:<br/>- Deutschland <br/>- die Bundesländer<br/>- Schweiz<br/>- Deutsche Auslandsschulen

**Beispiel für die Eintragungen für einen Clientrechner:**

![Beispiel für eine Anbindung an eine entfernte Datenbank](/assets/images/magellan.administrator/unterkarte.datenbank.server.png)

**Beispiel für die Eintragungen für einen Server- oder Einzelplatzrechner:**

![Beispiel für eine Anbindung an eine lokale Datenbank](/assets/images/magellan.administrator/unterkarte.datenbank.lokal.png)

## Unterpunkt Datensicherung

Wir empfehlen Ihnen eine tägliche Sicherung Ihrer Datenbank anzulegen. Um nicht für jede Sicherung den Ablagepfad der Sicherung oder den Ablagepfad für eine wiederhergestellte Datenbank eingeben zu müssen, können Ihre Standardpfade mit den Verbindungsinformationen vorab gespeichert werden.

### Vorbereitung

So geht's:

Öffnen Sie im MAGELLAN Administrator unter `Datenbankverbindungen` per Doppelklick auf Ihre Datenbankanbindung die Untereinstellungen. Wählen Sie hier die Karte `Datensicherung` und füllen die Karte entsprechend der nachstehenden Tabelle aus. Die hier gewählten Einstellungen, werden später beim Sichern für Sie vorbelegt.

![Belegen Sie die Pfade für die spätere Sicherung und Wiederherstellung vor!](/assets/images/magellan.administrator/unterkarte.datensicherung.png)

Feld|Anmerkung
--|--
Gemeinsamer Dateipfad|Tragen Sie hier Ihren Wunschpfad für Datenbankbackups ein, der Pfad sollte auf dem Verzeichnis `Datenbank` enden.<br/><br/>Beispiel für den Standardpfad:<br/>`C:\Users\Public\Documents\Stueber Systems\Magellan\Datenbank`<br/><br/>Dieser Vorgabepfad kann über die `blaue Pfeiltaste` am Ende der Zeile als Vorgabe in die Zeilen `Sicherung` und `Wiederherstellung` übernommen werden.<br/>Die Vorgaben werden wie folgt ergänzt:<br/><br/>`Sicherung`: `C:\Users\Public\Documents\Stueber Systems\Magellan\Datenbank\Datensicherung\Backup`<br/><br/>`Wiederherstellung`: `C:\Users\Public\Documents\Stueber Systems\Magellan\Datenbank\Datensicherung\Restore`<br/><br/>**Bitte stellen Sie sicher, dass es diese Unterverzeichnisse im Verzeichnis `Datenbank` gibt, bitte legen Sie sie ggfs. an!**
Namenskonventionen| Wählen Sie die Benennung für die Sicherung oder wiederhergestellte Sicherung:<br/>[Datum, Uhrzeit] Verbindungsalias - Benutzer<br/>[Datum, Uhrzeit] Verbindungsalias
Sicherung|Tragen Sie hier den Pfad ein, an dem die Sicherung später erstellt werden soll. Alternativ können Sie auch die Eintragung aus `Gemeinsamer Dateipfad` übernehmen.
Wiederherstellung|Tragen Sie hier den Pfad ein, an dem die Sicherung später erstellt werden soll. Alternativ können Sie auch die Eintragung aus `Gemeinsamer Dateipfad` übernehmen.

!!! warning "Achtung"

	Eine Sicherung/Wiederherstellung der Datenbank kann ausschließlich auf dem Rechner angelegt werden, auf dem auch die Datenbank selbst gespeichert ist und der Firebird-Server läuft. Sie können zwar die Aktion zum Sichern selbst von einem Clientrechner starten, die Sicherung kann aber nur auf Ihrem Serverrechner abgelegt werden, es sei denn Sie haben Zugriff auf den Serverrechner.

!!! warning "Achtung"

	Beim Wiederherstellen wird eine neue Datenbank aus der Sicherung aufgebaut. Dabei ist es auch, wenn Sie den identischen Pfad verwenden, ausgeschlossen hierbei die Realdatenbank zu überschreiben. Wenn Sie die wiederhergestellte Datenbank im Anschluss verwenden möchten, dann stoppen Sie bitte den Firebird-Dienst (`Systemsteuerung > Verwaltung > Dienste > Firebird Server`), benennen die "alte" Datenbank um, legen die "neue" Datenbank ab und starten den Firebird-Dienst wieder.

### Sichern und Wiederherstellen

Die Sicherung oder Wiederherstellung starten Sie aus der Menüleiste über die Schaltflächen `Backup` oder `Wiederherstellen`. In dem Assistenten werden die zuvor auf der Unterkarte `Datensicherung` Ihrer MAGELLAN Verbindung eingegebenen Werte vorbelegt. Sie tragen nur noch als Benutzer den `sysdba` und dessen Passwort ein und können eine Sicherung erstellen oder aus einer Sicherung eine neue Datenbank wiederherstellen.

![Schaltflächen zum Erstellen eines Backups oder dem Wiederherstellen einer Sicherung](/assets/images/magellan.administrator/ribbon.datenbankverbindungen.png)

## Unterpunkt Datenordner

Feld|Anmerkung
--|--
Gemeinsamer Dateipfad|Tragen Sie hier den Pfad zum Verzeichnis über den Datenordnern Dokumente, Berichte, Skripte, Vorlagen und Importe ein. Möglich ist für Clientinstalltionen ein Netzwerkpfad oder einen Verweis auf ein Netzlaufwerk. Für Server- oder Einzelplatzinstallationen tragen Sie bitte den lokalen Pfad ein. Der Standardpfad für eine Server-/Einzelplatzinstallation wäre:<br/>`C:\Users\Public\Documents\Stueber Systems\Magellan`<br/><br/> Wenn hier einen Pfad eintragen und dieser Pfad für alle Verzeichnisse gilt, können Sie die blaue Pfeiltaste am Ende der Zeile verwenden, um den Eintrag in die weiteren Zeilen zu übernehmen.
Dokumente<br/>Skripte<br/>Berichte<br/>Vorlagen<br/>Importe|Tragen Sie hier den Pfad ein, an dem die Sicherung später erstellt werden soll. Alternativ können Sie auch die Eintragung aus `Gemeinsamer Dateipfad` übernehmen, die Bezeichnung des Verzeichnisses wird automatisch ergänzt.

![Gemeinsamen Dateipfad übernehmen](/assets/images/magellan.administrator/Datenordner.png)

![Ergebnis](/assets/images/magellan.administrator/Datenordner.gefuellt.png)

## Verbindung testen

Ob Ihre eingegebene Verbindung funktionsfähig ist, können Sie testen. Rufen Sie den Assistenten `Verbindung testen`über die Schaltfläche unter dem Punkt `Datenbankverbindungen` auf. Sollte die Ergebnisanzeige Probleme anzeigen, schauen Sie bitte den Abschnitt [Probleme bei der Installation?](https://doc.magellan.stueber.de/schulverwaltung/installation/probleme-bei-der-installation) an.

![Assistent zum Testen der Verbindung](/assets/images/magellan.administrator/verbindung.testen.png)

!!! info "Hinweis"

	 MAGELLAN-Arbeitsplatzrechner und MAGELLAN-Serverrechner werden unterschiedlich eingerichtet. Wenn Sie den ersten Arbeitsplatz fertig eingerichtet und den Aufruf von MAGELLAN (um die Datenbankanbindung zu testen), die Druckvorschau (um den Pfad zum Verzeichnis Berichte zu testen) und zum Beispiel eine Sammelzuweisung (um den Pfad zum Verzeichnis Skripte zu testen) ausgeführt haben, können Sie die Optionen, die Lizenz und die Pfadeinstellungen (Datenbank und Datenordner) für andere Arbeitsplätze nutzen. Bitte lesen Sie dazu den Abschnitt ["Die Pathsdatei"](https://doc.magellan.stueber.de/schulverwaltung/installation/die-pathsdatei)!
