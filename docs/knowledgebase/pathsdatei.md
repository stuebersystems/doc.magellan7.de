# Mehrere Arbeitsplatzrechner einrichten: Die Paths-Datei

Beim Start von MAGELLAN werden Informationen wie zum Beispiel Optionen, Lizenzdaten oder Pfade zur Datenbank, den Datenordnern uws. aus Dateien gelesen. Diese Dateien werden standardmäßig an einem betriebssystemspezifischen Ort pro MAGELLAN-Installation angelegt und dort auch ausgelesen. 
Alternativ können diese Dateien auch an einer beliebigen anderen Stelle in Ihrem Netzwerk liegen und MAGELLAN liest den Pfad zu den Dateien aus der Paths-Datei (``MAGELLAN.paths``) aus. 

Der Vorteil einer Paths-Datei ist, dass Sie mehreren Nutzern die identischen Einstellungen in einem Arbeitsschritt an einem zentralen Ort zur Verfügung stellen können.

Beispiel: 
Die Statistiklizenz wird nur an einer einzigen Stelle im Netzwerk eingespielt, ist aber für alle Kollegen erreichbar. 
Auch beim Einrichten einer neuen Arbeitsplatzinstallation spart man sich einzelne Schritte: es genügt die Installation durchzuführen und die MAGELLAN.paths im Programmverzeichnis abzulegen.


!!! warning "Wichtig"

     Arbeitsplatzrechner:<br/>  Die Verbindungsinformationen aus Sicht der Arbeitsplatzrechner sind sicher immer gleich, insofern ist es sinnvoll für Ihre Arbeitsplatzrechner Paths-Dateien zum Verweis auf ein Verzeichnis in Ihrem Netzwerk zu verwenden.<br/> <br/>Serverrechner: <br/>  Wir empfehlen für den Serverrechner **nicht** auf eine Pathsdatei zu verweisen, hier genügt es die lokalen Dateien zu verwenden.

Folgende Dateien werden beim Programmstart gelesen:


| Datei        | Inhalt                                   |
|--------------|------------------------------------------|
| MAGELLAN.lic | enthält die Lizenzierungsdaten           |
| MAGELLAN.opt | enthält die MAGELLAN-Optionseinstellungen |
| MagInv.opt   | enthält die MAGELLAN-Haushalt&Inventar-Optionseinstellungen |
| MagBib.opt   | enthält die MAGELLAN-Bibliothek-Optionseinstellungen |
| MAGELLAN.evm | enthält die Pfade zur Datenbank und den Datenordnern |



Diese Dateien liegen je nach Betriebssystem an folgenden voreingestellten Speicherorten:


| Betriebssystem      | Pfad                                     |
|---------------------|------------------------------------------|
| Windows 2000        | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\MAGELLAN 7 |
| Windows XP          | C:\Dokumente und Einstellungen\All Users\Anwendungsdaten\Stueber Systems\MAGELLAN 7 |
| Windows Vista       | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows 7/8         | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows Server 2008 | C:\ProgramData\Stueber Systems\MAGELLAN 7 |
| Windows 10          | C:\ProgramData\Stueber Systems\MAGELLAN 7 |


Möchten Sie abweichende Speicherorte für diese Dateien angeben, zum Beispiel damit alle MAGELLAN-Arbeitsplatzinstallationen auf dieselben Dateien zugreifen, sind folgende Schritte nötig:

1. Richten Sie einen Arbeitsplatz vollständig ein, damit Sie von diesem Arbeitsplatz aus die ``MAGELLAN.evm``, die ``MAGELLAN.lic`` und die ``MAGELLAN.opt`` kopieren können. 

2. Wählen Sie einen Speicherort für die Konfigurationsdateien aus. Die Dateien können in einem gemeinsamen Verzeichnis liegen oder Sie wählen für ``MAGELLAN.evm``, ``MAGELLAN.lic`` und die Optionsdateien (``MAGELLAN.opt``, ``MagInv.opt``, ``Mag-Bib.opt``) drei getrennte Verzeichnisse und speichern dort die Dateien.

3. Erstellen Sie mit einem Texteditor eine neue Textdatei und kopieren den nachfolgenden Text in diese Datei. Passen Sie die Pfade bitte auf Ihre angelegten Verzeichnisse an, diese können sich lokal auf dem Rechner oder in Ihrem Netzwerk befinden. 


!!! warning "Wichtig"

    Bitte denken Sie daran, dass die Nutzer, die auf die Dateien zugreifen sollen auch entsprechende Schreib- und Leserechte benötigen.

Beispiel für die Ablage in Ihrem Netzwerk: 

``` xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<Preferences>
  <Paths>
    <Entry Name="MAGELLANEnvironmentFolder" Value="\\Mein_Server\...\Pathsdateien"/>
    <Entry Name="MAGELLANOptionsFolder" Value="\\Mein_Server\...\Pathsdateien"/>
    <Entry Name="MAGELLANLicenseFolder" Value="\\Mein_Server\...\Pathsdateien"/>
  </Paths>
</Preferences>
```

Weiter geht's:

1. Speichern Sie diese Textdatei und benennen die Datei anschließend in „MAGELLAN.paths“ um.

2. Legen Sie diese Datei pro Arbeitsplatzinstallation im Programmverzeichnis (parallel zur MAGELLAN.exe) ab. Beim Programmstart von MAGELLAN wird geprüft, ob sich eine Datei mit diesem Namen im Programmverzeichnis befindet und gegebenenfalls ausgelesen.


!!! warning "Wichtig"

    Wenn Sie per MAGELLAN.paths auch auf die Optionsdatei verweisen und wünschen, dass die Benutzer Optionen selbst einstellen dürfen, müssen die Benutzer auch die Rechte haben an der der Ablagestelle der MAGELLAN.opt Änderungen vorzunehmen.<br/> Bitte bedenken Sie auch folgenden Punkt: <br/> Startet man MAGELLAN, wird die Optionsdatei geladen. Schließt man MAGELLAN, wird die Optionsdatei gespeichert. Wenn Sie eine Änderung vornehmen, versucht MAGELLAN Ihre Änderung beim Beenden Ihrer Instanz zu speichern. Sind aber parallel noch weitere Instanzen offen, wird beim Beenden dieser Instanzen die Optionsdatei nach Ihnen gespeichert, dann aber ohne Ihre Änderung, weil die Optionsdatei beim Programmstart geladen wird und nicht zwischendrin nachgeladen wird. Ihre Änderung gilt, wenn Sie als letzter MAGELLAN beenden.




