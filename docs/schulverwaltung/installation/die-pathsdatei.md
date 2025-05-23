# Mehrere Arbeitsplatzrechner einrichten: Die Paths-Datei

Beim Start von Magellan werden Informationen wie zum Beispiel Optionen, Lizenzdaten oder Pfade zur Datenbank, den Datenordnern uws. aus Dateien gelesen. Diese Dateien werden standardmäßig an einem betriebssystemspezifischen Ort pro Magellan-Installation angelegt und dort auch ausgelesen.
Alternativ können diese Dateien auch an einer beliebigen anderen Stelle in Ihrem Netzwerk liegen und Magellan liest den Pfad zu den Dateien aus der Paths-Datei (``Magellan.paths``) aus.

Der Vorteil einer Paths-Datei ist, dass Sie mehreren Nutzern die identischen Einstellungen in einem Arbeitsschritt an einem zentralen Ort zur Verfügung stellen können.

Beispiel:
Die Statistiklizenz wird nur an einer einzigen Stelle im Netzwerk eingespielt, ist aber für alle Kollegen erreichbar.
Auch beim Einrichten einer neuen Arbeitsplatzsituation spart man sich einzelne Schritte: es genügt die Installation durchzuführen und die Magellan.paths im Programmverzeichnis abzulegen.

!!! warning "Wichtig"

    Arbeitsplatzrechner:     
    Die Verbindungsinformationen aus Sicht der Arbeitsplatzrechner sind sicher immer gleich, insofern ist essinnvoll für Ihre Arbeitsplatzrechner Paths-Dateien zum Verweis auf ein Verzeichnis in Ihrem Netzwerk zuverwenden.

    Serverrechner:     
    Wir empfehlen für den Serverrechner nicht auf eine Pathsdatei zu verweisen, hier genügt es die lokalen Dateien zu verwenden.

Folgende Dateien werden beim Programmstart gelesen:

Datei               | Inhalt
------------------- | -------------
Magellan.lic        | enthält die Lizenzierungsdaten
Magellan.opt        | enthält die Magellan-Optionseinstellungen
MagInv.opt          | enthält die Magellan-Haushalt&Inventar-Optionseinstellungen
MagBib.opt          | enthält die Magellan-Bibliothek-Optionseinstellungen
Magellan.evm        | enthält die Pfade zur Datenbank und den Datenordnern

Diese Dateien liegen je nach Betriebssystem an folgenden voreingestellten Speicherorten:

Betriebssystem      | Pfad
------------------- | -------------
Windows Vista       | C:\ProgramData\Stueber Systems\Magellan 8
Windows 7/8         | C:\ProgramData\Stueber Systems\Magellan 8
Windows Server 2008 | C:\ProgramData\Stueber Systems\Magellan 8
Windows 10          | C:\ProgramData\Stueber Systems\Magellan 8

Möchten Sie abweichende Speicherorte für diese Dateien angeben, zum Beispiel damit alle Magellan-Arbeitsplatzinstallationen auf dieselben Dateien zugreifen, sind folgende Schritte nötig:

1. Richten Sie einen Arbeitsplatz vollständig ein, damit Sie von diesem Arbeitsplatz aus die ``Magellan.evm``, die ``Magellan.lic`` und die ``Magellan.opt`` kopieren können. 

2. Wählen Sie einen Speicherort für die Konfigurationsdateien aus. Die Dateien können in einem gemeinsamen Verzeichnis liegen oder Sie wählen für ``Magellan.evm``, ``Magellan.lic`` und die Optionsdateien (``Magellan.opt``, ``MagInv.opt``, ``Mag-Bib.opt``) drei getrennte Verzeichnisse und speichern dort die Dateien.

3. Erstellen Sie mit einem Texteditor eine neue Textdatei und kopieren den nachfolgenden Text in diese Datei. Passen Sie die Pfade bitte auf Ihre angelegten Verzeichnisse an, diese können sich lokal auf dem Rechner oder in Ihrem Netzwerk befinden.

Beispiel:

``` 
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<Preferences>
  <Paths>
    <Entry Name="MagellanEnvironmentFolder" Value="D:\Mein Verzeichnis"/>
    <Entry Name="MagellanOptionsFolder" Value="D:\Mein Verzeichnis"/>
    <Entry Name="MagellanLicenseFolder" Value="D:\Mein Verzeichnis"/>
  </Paths>
</Preferences>
```

Weiter geht's:

1. Speichern Sie diese Textdatei und benennen die Datei anschließend in „Magellan.paths“ um.

2. Legen Sie diese Datei pro Arbeitsplatzinstallation im Programmverzeichnis (parallel zur Magellan.exe) ab. Beim Programmstart von Magellan wird geprüft, ob sich eine Datei mit diesem Namen im Programmverzeichnis befindet und gegebenenfalls ausgelesen.

!!! warning "Wichtig"

    Wenn Sie per Magellan.paths auch auf die Optionsdatei verweisen und wünschen, dass die Benutzer Optionen selbst einstellen dürfen, müssen die Benutzer auch die Rechte haben an der der Ablagestelle der Magellan.opt Änderungen vorzunehmen.

Über Neuerungen im Programm informieren wir im Abschnitt [Was ist neu?](https://doc.magellan.stueber.de/changelog/changelog/)
