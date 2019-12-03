# OPAC Unterstützung in MAGELLAN BIBLIOTHEK

## OPAC-Unterstützung

!!! info "Hinweis"

    Diese Dokumentation zur Einricht des OPAC Research gilt für die aktuellen VErsion MAGELLAN 7

## Einrichten des OPAC-Research

### Aktivieren der Online Suche

Bitte aktivieren Sie in den Optionen von MAGELLAN-BIBLIOTHEK über `Datenbank > Optionen` die Online Suche.

![MAGELLAN Optionen](/assets/images/bibliothek/optionen_online_suche.png)

### Einrichten des OPAC Research

Bitte öffnen Sie über `Extras > Opac` das Verzeichnis der Opac Server. Hier können Sie können Sie die von uns bereits getesteten OPAC-Server über die markierte Schaltfläche direkt hinzufügen.
![Opac Server einrichten](/assets/images/bibliothek/opac5.png)

Aktuell handelt es sich um den Server der Deutschen Nationalbibliothek (Weiterhin DNB genannt.). In den meisten Fällen werden Sie eine Anmeldung/Registrierung bei den jeweiligen Serverbetreibern benötigen. Die Deutsche Nationalbibliothek erfordert z. B. eine Registrierung (```https://portal.dnb.de/myAccount/register.htm```), da neben den kostenfreien Abfragen auf ihre Server auch kostenpflichtige Abfragen möglich sind und diese über das Kundenkonto abgerechnet werden können.

#### Notwendige Eingaben

Spalte | Eintrag
-|-
Aktiv| Bitte den Haken Setzen
Protokoll| bitte wähle Sie Search Retrieve Url (SRU) aus
Name|Bitte vergeben Sie hier einen Namen
Host/Url| http://services.dnb.de/sru
Port|80
Katalog|dnb

#### Eintragungen Details/ Registerkarte "Autentifizierung"

![Opac Server einrichten](/assets/images/bibliothek/opac6.png)

Spalte | Eintrag
-|-
Art der Auhthentifizierung| Bitte wählen Sie  per **Zugangscode** (Access Token) aus
Benutzername| bleibt leer
Kennwort/Zugangscode| Im Falle der DNB benötigen Sie hier einen `Zugriffstoken`, den Sie nach der Registrierung im Portal der DNB anfragen können.

#### Eintragungen Details/ Registerkarte "Recherche"

Spalte | Eintrag
-|-
Indexname zur Suche|
Maximale Anzahl der Suchergebnisse| 0
Schema/ Format Kurzform|
Schema Format Langform|

Speichern Sie danach den Eintrag. Sie haben somit erfolgreich den ersten Server eingetragen. Die Serverdaten werden in eine Konfigurationsdatei gespeichert.

![Speichern Sie die Daten](/assets/images/bibliothek/opac7.png)

### Recherche

Wechseln Sie in den Bereich `Bücher/Meidne > Bearbeiten > Neuer Datensatz` um mit der Recherche eines Medium zu beginnen. Zukünftig wird die Konfigurationsdatei geladen und die vorhandenen Server für die Recherche verwendet. Sie landen dann automatisch auf der Registerkarte `Recherche` und die Suche wird aufgrund des Einscannens des Barcodes in MAGELLAN-BIBLIOTHEK automatisch ausgeführt.

Scannen Sie das Medium beim ersten Mal bitte erneut ein, bzw. geben es über die Tastatur ein und schließen dann mit der Eingabetaste ab. OPAC-Research stellt eine Verbindung zum ersten Server her und sucht nach dem Barcode.

Wenn Sie mehrere Server eintragen, dann werden alle Server nacheinander angefragt, bis ein Server einen Eintrag zum Barcode auf dem jeweiligen Server findet.

### Das Ergebnis

In manchen Fällen gibt es mehrere Ergebnisse. Markieren Sie den gewünschten Eintrag und klicken Sie auf die Schaltfläche `Übernehmen und Zurück`, um den Eintrag nach MAGELLAN-BIBLIOTHEK zu übertragen und OPAC-Research zu beenden. Wenn Sie auf `Schließen` klicken, wird der Eintrag nicht übernommen und OPAC-Research beendet.

![Neues Medium](/assets/images/bibliothek/opac4.png)

Der ausgewählte Eintrag wird nach MAGELLAN-BIBLIOTHEK übertragen und die verwertbaren Informationen noch einmal zur manuellen Bearbeitung dargestellt. Ab hier arbeiten Sie wie gewohnt in MAGELLAN-BIBLIOTHEK weiter.
