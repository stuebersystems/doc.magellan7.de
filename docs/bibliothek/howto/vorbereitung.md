# Vorbereitung

[1]:/assets/images/bibliothek/anmeldung.png
[2]:/assets/images/bibliothek/willkommen.png
[3]:/assets/images/bibliothek/optionen_online_suche.png
[4]:/assets/images/bibliothek/opac5.png
[5]:/assets/images/bibliothek/opac6.png
[6]:/assets/images/bibliothek/opac12.png
[7]:/assets/images/bibliothek/opac7.png

Bevor Sie mit der Arbeit in der Magellan Bibliothek beginnen können, müssen drei Startbedingungen erfüllt sein:

1. Die Verbindung zur Magellan-Datenbank ist angelegt.
2. An Ihrem Arbeitsrechner ist ein Barcodescanner installiert.
3. Das Programm ist gestartet.

## Arbeitsplatzinstallation

Bitte richten Sie Ihren Arbeitsplatz mit einer Installation von Magellan , entsprechend der Anleitung [hier](https://doc.magellan.stueber.de/schulverwaltung/installation/version8/arbeitsplatz.installieren/) ein.

## Barcodescanner anschließen

Damit Sie optimal und komfortabel mit der Magellan Bibliothek arbeiten können, sollte an Ihrem Arbeitsplatzrechner ein Barcodescanner installiert sein.

Barcodes bzw. Strichcodes nehmen in Magellan-Bibliothek eine zentrale Rolle bei der Erfassung und Verwaltung sowohl der Nutzer- als auch der Medien ein. Sie ermöglichen eine schnelle Abwicklung der Ausleihvorgänge ebenso wie eine zügige Erfassung neuer Medientitel, indem Medien- und Nutzerdaten nicht umständlich eingetippt, sondern über das Einscannen eines Strichcodes in Sekundenschnelle aufgerufen werden können. So wird in Magellan-Bibliothek z.B. für jedes erfasste Medienexemplar und für jeden angemeldeten Benutzer ein eindeutiger Strichcode erzeugt, auf den später mittels eines Barcodescanner zugegriffen werden kann.

Bei einem Barcodescanner handelt es sich um ein Eingabegerät vergleichbar mit Maus oder Tastatur. Verbinden Sie einfach den USB-Stecker Ihres Barcodescanners mit einem freien USB-Port Ihres Rechners. Die heute handelsüblichen Geräte werden in der Regel von Ihrem Windows-Rechner automatisch erkannt, sobald eine Verbindung hergestellt wurde. Ein Betrieb von Magellan-Bibliothek ohne ein entsprechendes Lesegerät ist aus Gründen der Arbeitseffizienz nicht zu empfehlen.

## Magellan-Bibliothek starten

Um Magellan-Bibliothek das erste Mal zu starten, gehen Sie bitte folgendermaßen vor:

1. Rufen Sie das Startmenü Ihres Windows-Betriebssystems auf und wählen Sie den Aufruf  `Programme` \(XP; 2000\) bzw.  `Alle Programme` \(Vista\).
2. Öffnen Sie den Programmordner  `STÜBER SYSTEMS`.
3. Klicken Sie dort mit der linken Maustaste auf die Programmzeile  `Magellan/Bibliothek`.

Es öffnet sich das Dialogfenster  `Magellan-Anmeldung`, in das Sie einen Benutzernamen und ein Kennwort eintragen müssen. Tragen Sie hier bitte den Benutzernamen sysdba und das Kennwort masterkey \(gilt nur für neuinstallierte Testsysteme\) ein, die als Zugangsdaten bei jeder Installation standardmäßig hinterlegt werden. Außerdem müssen Sie in diesem Anmeldedialog den Namen der Datenbank, die Sie nutzen möchten, angeben. Beim ersten Programmstart steht Ihnen hier nur der Eintrag  `Magellan` zur Verfügung. Unter diesem Namen ist die mitgelieferte Demo-Datenbank für den Zugriff in Magellan registriert.

[![Das Dialogfenster  `Magellan-Anmeldung` erscheint vor jedem Programmstart][1]][1]

Sobald Sie Ihre Angaben mit  `OK` bestätigen, wird Magellan-Bibliothek mit dem  `Willkommensfenster` geöffnet.

[![Das Willkommensfenster begrüßt Sie beim ersten Programmstart von Magellan-Bibliothek und verweist Sie auf weiterführende Informationen und Services.][2]][2]

Wenn Sie sich nicht als sysdba angemeldet hatten, sondern von Ihrem Schuladministrator persönliche Zugangsdaten erhalten hatten, können Sie nach dem Programmstart Ihr persönliches Anmeldekennwort festlegen. Gehen Sie dazu bitte folgendermaßen vor:

1. Führen Sie den Menüpunkt `Datenbank > Kennwort ändern` aus.

2. Geben Sie im Eingabefeld  `Neues Kennwort` Ihr gewünschtes Anmeldekennwort ein.

3. Wiederholen Sie im Eingabefeld  `Bestätigung` das gewählte Kennwort.

4. Bestätigen Sie bitte Ihre Angaben mit `OK`.

## OPAC Unterstützung in Magellan Bibliothek

!!! info "Hinweis"

    Diese Dokumentation zur Einrichtung des OPAC Research gilt für die aktuellen Version Magellan.

### Aktivieren der Online Suche

Bitte aktivieren Sie in den Optionen von Magellan-Bibliothek über `Datenbank > Optionen` die `Online Suche`.

[![Magellan Optionen][3]][3]

### Einrichten des OPAC Research

Bitte öffnen Sie über `Extras > Opac` das Verzeichnis der Opac-Server. Hier können Sie die von uns bereits getesteten OPAC-Server über die markierte Schaltfläche direkt hinzufügen.

[![Opac Server einrichten][4]][4]

Aktuell handelt es sich um den Server der Deutschen Nationalbibliothek (weiterhin DNB genannt.). In den meisten Fällen werden Sie eine Anmeldung/Registrierung bei den jeweiligen Serverbetreibern benötigen. Die Deutsche Nationalbibliothek erfordert aktuell keine Registrierung.

#### Notwendige Eingaben

Spalte | Eintrag
-|-
Aktiv| bitte den Haken Setzen
Protokoll| bitte wähle Sie Search Retrieve Url (SRU) aus
Name|bitte vergeben Sie hier einen Namen
Host/Url| `http://services.dnb.de/sru` (Beispiel hier Deutsche Nationalbibliothek, es wird keine Registrierung benötigt)
Port|80
Katalog|dnb

#### Eintragungen Details/ Registerkarte "Autentifizierung"

[![Opac Server einrichten][5]][5]

Spalte | Eintrag
-|-
Art der Authentifizierung| Bitte wählen Sie für das Beispiel "Deutsche Nationalbibliothek den Wert "`Keine Authentifizierung`
Benutzername``| bleibt leer
Kennwort/Zugangscode| Im Falle der DNB benötigen Sie in der Vergangenheit einen `Zugriffstoken`, den Sie nach der Registrierung im Portal der DNB anfragen konnten. Das Feld kann inzwischen leer bleiben.

#### Eintragungen Details/ Registerkarte "Recherche"

[![Registerkarte "Recherche"][6]][6]

Spalte | Eintrag
-|-
Indexname zur Suche| nummer (num)
Maximale Anzahl der Suchergebnisse| 0 (unbegrenzt)
Schema/ Format Kurzform| Auswahl von Dublin-Core-Elementen, DNB-Titeldaten, ZDB-Titeldaten (oai_dc) (bei der Deutschen Nationalbibliothek, da kostenfrei)
Schema Format Langform| XML-Variante von MARC212 / DNB-Titeldaten, ZDB-Titeldaten, Normdaten (MARC21-xml)

Speichern Sie danach den Eintrag. Sie haben somit erfolgreich den ersten Server eingetragen. Die Serverdaten werden in eine Konfigurationsdatei gespeichert.

[![Speichern Sie die Daten][7]][7]

