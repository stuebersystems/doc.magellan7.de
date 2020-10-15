# OPAC Unterstützung in MAGELLAN BIBLIOTHEK

## OPAC-Unterstützung

!!! info "Hinweis"

    Diese Dokumentation zur Einrichtung des OPAC Research gilt für die aktuellen Version MAGELLAN 7.

## Einrichten des OPAC-Research

### Aktivieren der Online Suche

Bitte aktivieren Sie in den Optionen von MAGELLAN-BIBLIOTHEK über `Datenbank > Optionen` die Online Suche.

![MAGELLAN Optionen](/assets/images/bibliothek/optionen_online_suche.png)

### Einrichten des OPAC Research

Bitte öffnen Sie über `Extras > Opac` das Verzeichnis der Opac Server. Hier können Sie die von uns bereits getesteten OPAC-Server über die markierte Schaltfläche direkt hinzufügen.
![Opac Server einrichten](/assets/images/bibliothek/opac5.png)

Aktuell handelt es sich um den Server der Deutschen Nationalbibliothek (weiterhin DNB genannt.). In den meisten Fällen werden Sie eine Anmeldung/Registrierung bei den jeweiligen Serverbetreibern benötigen. Die Deutsche Nationalbibliothek erfordert z. B. eine Registrierung (```https://portal.dnb.de/myAccount/register.htm```), da neben den kostenfreien Abfragen auf ihre Server auch kostenpflichtige Abfragen möglich sind und diese über das Kundenkonto abgerechnet werden können.

#### Notwendige Eingaben

Spalte | Eintrag
-|-
Aktiv| bitte den Haken Setzen
Protokoll| bitte wähle Sie Search Retrieve Url (SRU) aus
Name|bitte vergeben Sie hier einen Namen
Host/Url| http://services.dnb.de/sru (Beispiel hier Deutsche Nationalbibliothek, es wird eine Registrierung benötigt)
Port|80
Katalog|dnb

#### Eintragungen Details/ Registerkarte "Autentifizierung"

![Registerkarte "Autentifizierung"](/assets/images/bibliothek/opac6.png)

Spalte | Eintrag
-|-
Art der Authentifizierung| Bitte wählen Sie per **Zugangscode** (Access Token) aus
Benutzername| bleibt leer
Kennwort/Zugangscode| Im Falle der DNB benötigen Sie hier einen `Zugriffstoken`, den Sie nach der Registrierung im Portal der DNB anfragen können.

#### Eintragungen Details/ Registerkarte "Recherche"

![Registerkarte "Recherche"](/assets/images/bibliothek/opac12.png)

Spalte | Eintrag
-|-
Indexname zur Suche| nummer (num)
Maximale Anzahl der Suchergebnisse| 0 (unbegrenzt)
Schema/ Format Kurzform| Auswahl von Dublin-Core-Elementen, DNB-Titeldaten, ZDB-Titeldaten (oai_dc) (bei der Deutschen Nationalbibliothek, da kostenfrei)
Schema Format Langform| XML-Variante von MARC212 / DNB-Titeldaten, ZDB-Titeldaten, Normdaten (MARC21-xml)

Speichern Sie danach den Eintrag. Sie haben somit erfolgreich den ersten Server eingetragen. Die Serverdaten werden in eine Konfigurationsdatei gespeichert.

![Speichern Sie die Daten](/assets/images/bibliothek/opac7.png)

### Recherche

Wechseln Sie in den Bereich `Bücher/Medien > Bearbeiten > Neuer Datensatz`, um mit der Recherche eines Medium zu beginnen. Zukünftig wird die Konfigurationsdatei geladen und die vorhandenen Server für die Recherche verwendet.

Scannen Sie das Medium ein, bzw. geben es über die Tastatur die ISBN Nummer im Feld Barcode ein und schließen dann mit der Eingabetaste ab. OPAC-Research stellt eine Verbindung zum ersten Server her und sucht nach dem Barcode.

Wenn Sie mehrere Server eintragen, dann werden alle Server nacheinander angefragt, bis ein Server einen Eintrag zum Barcode auf dem jeweiligen Server findet.

![Neues Medium erfassen](/assets/images/bibliothek/opac8.png)

!!! info "Hinweis"

    Klappt es nicht? Bitte prüfen Sie, ob unter `Datenbank > Optionen > Online Suche` die Option `Buchdetails im Internet suchen und mit Magellan-Bibliothek synchronisieren` aktiviert ist.

![Online-Suche aktivieren](/assets/images/bibliothek/opac13.png)

### Das Ergebnis

War die Recherche erfolgreich, wechselt der Assistent zur Eingabe neuer Medien direkt auf die nächste Seite. Die gefundenen Informatioanen sind hier bereits vorbelegt, ggf. können Sie weitere Infiormationen für das Medium erfassen.

![Neues Medium erfassen](/assets/images/bibliothek/opac9.png)

Bestätigen Sie die Eingabe mit `Weiter`. Sie gelangen auf die nächste Registerkarte mit den Angaben zur Signatur. Nehmen Sie hier Ihre Eintragungen vor und bestätigen  Sie mit `Weiter`.

![Neues Medium erfassen](/assets/images/bibliothek/opac10.png)

ie gelangen auf die nächste Registerkarte mit den Angaben zu den Exemplardaten. Nehmen Sie hier Ihre Eintragungen vor und bestätigen  Sie mit `Weiter` und dann mit `Fertigstellen`. Das Medium und die Exemplare werden angelegt.

Der ausgewählte Eintrag wird in die MAGELLAN BIBLIOTHEK übertragen und die verwertbaren Informationen sowie die manuell eingegebenen Daten gespeichert.