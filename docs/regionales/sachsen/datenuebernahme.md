## Inhalte aus der MAGELLAN 6-Datenbank in eine leere MAGELLAN 7-Datenbank übernehmen

Ihre Schulverwaltungsdaten aus MAGELLAN 6 werden in eine leere Datenbank im korrekten Format für MAGELLAN 7 übergeben.

> #### danger::Achtung!
>
> Für die problemlose Übernahme der Datenbank ins neue Zielformat muss sichergestellt sein, dass die Datenbank das korrekte Ausgangsformat hat. 
> Bitte erstellen Sie eine Sicherung Ihrer MAGELLAN 6 Datenbank, stellen sie im Anschluss wieder her und nutzen die wiederhergestellte Datenbank als Datenquelle! 

Öffnen Sie bitte das Modul **MAGELLAN 7 Administrator** und wählen den Unterpunkt `Datenbankpflege > Mandanten kopieren` über die Schaltfläche ``Ausführen`` oder per Doppelklick aus. 

![Magellan 6 nach MAGELLAN 7](/images/magellan.administrator/mandanten.kopieren5.1.png)

Stellen Sie nun die Variante `MAGELLAN 6 nach MAGELLAN 7` ein. Klicken Sie auf `Weiter`!

![Magellan 6 nach MAGELLAN 7](/images/magellan.administrator/mandanten.kopieren5.png)



> ####### warning::Wichtig!
>
> Das Übertragen der MAGELLAN 6-Daten ist nur in eine leere MAGELLAN 7-Datenbank möglich. Bei der Installation von MAGELLAN 7 wird Ihnen im Datenbankverzeichnis eine leere Datenbank mit dem Namen "Magellan7.fdb" angelegt. 
![leere Datenbank im Format für MAGELLAN 7](/images/magellan.administrator/mandanten.kopieren6.png)

![Laden Sie ggfs. eine leere Datenbank herunter!](/images/magellan.administrator/mandanten.kopieren7.png)

Füllen Sie bitte die Felder (siehe untere Tabelle) des Assistenten aus, im oberen Teil verweisen Sie auf die Quelldatenbank (MAGELLAN 6), im unteren Bereich auf die Zieldatenbank (MAGELLAN 7).

![Eintragungen für die Quell- und Zieldatenbank](/images/magellan.administrator/mandanten.kopieren8.png)


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

> #### primary::Hinweis
>
> Sollten Sie den Übertrag bereits einmal durchgeführt haben, können Sie jederzeit eine "frische" leere Datenbank im MAGELLAN 7-Format herunterladen. Alternativ erhalten Sie über diesen [Link](ftp://ftp.stueber.de/pub/bin/de/magellan/v7/database/MAGELLAN7.FDB) eine leere Datenbank.



## Wortersetzungen

Für SaxSVS noch nicht wichtig, aber für den späteren Umstieg: Bei der Übernahme der Daten aus Ihrer MAGELLAN 6-Datenbank in die MAGELLAN 7-Datenbank können Ihre geänderten Feldbezeichnungen aus technischen Gründen nicht übernommen werden. Bitte tragen Sie  unter `MAGELLAN 7 > Extras > Bezeichnungen anpassen > Spalte "durch"` Ihre gewünschten Bezeichnungen neu ein!
