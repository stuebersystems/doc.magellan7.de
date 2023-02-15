# Wie kann ein Update verteilt werden

Bei jedem Update müssen der Server und alle Clientrechner aktualisiert werden.
Nachfolgend einige Herangehensweisen:

|**Varianten**|
|-|
|[Variante 1:](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/#variante-1)  Sie laden das Updatepaket von unserer Webseite und starten die Installation  pro Rechner per Doppelklick.|
|[Variante 2:](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/#variante-2)  Die Nutzer starten die Aktualisierung selbst (MAGELLAN > Hilfe > auf Aktualisierung prüfen), laden das Updatepaket von **unserem** Server und führen die Installation durch. Für diese Aktion muss den Benutzern das Recht gewährt werden, den Windows Installer auszuführen.|
|[Variante 3:](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/#variante-3)  Die Nutzer starten die Aktualisierung selbst (MAGELLAN > Hilfe > auf Aktualisierung prüfen), laden das Updatepaket von **Ihrem** Server und führen die Installation durch. Für diese Aktion muss den Benutzern das Recht gewährt werden, den Windows Installer auszuführen.|
|[Variante 4:](https://doc.magellan.stueber.de/schulverwaltung/update/wie-kann-ein-update-verteilt-werden/#variante-4)  Sie nutzen ein Tool zur Softwareverteilung oder die Gruppenrichtlinien in Ihrem Netzwerk.|

## Variante 1

Über ein neues Update können Sie sich von uns per Newsletter informieren lassen oder Sie aktivieren in MAGELLAN unter `Datenbank > Optionen > Update` die folgende Einstellung:

![Die Karte `Update `unter `MAGELLAN > Datenbank > Optionen`](/assets/images/datenbank_optionen_update.png)

Mit dieser Auswahl prüft MAGELLAN bei jedem Programmstart, ob ein neues Update zur Verfügung steht.

Das Installationspaket finden Sie hier: [http://MAGELLAN.stueber.de/download.php](http://MAGELLAN.stueber.de/download.php)

Bitte laden Sie es herunter und führen es per Doppelklick auf allen MAGELLAN-Rechnern in Ihrem Netzwerk aus.

## Variante 2

Wenn Sie diese Variante wählen möchten, stellen Sie sicher, dass bei allen MAGELLAN-Installation die Option `Datenbank > Optionen > Update > Autoupdate aktivieren`gewählt ist. Der Nutzer wird beim Programmstart über das neue Update informiert, kann per Assistent das Updatepaket herunterladen und ausführen.

Vorteil:

* Sie müssen lediglich die Server-Installation selbst aktualisieren, alle weiteren MAGELLAN-Installationen werden von den Anwendern aktualisiert.

Nachteile:

* Sie können nicht sicherstellen, dass alle Nutzer die Aktualisierung durchführen.
* Jeder Anwender lädt einzeln das Updatepaket herunter.
* Die Nutzer müssen über Installationsrechte verfügen.

## Variante 3

Aus Sicht des Anwenders scheint diese Alternative genau wie Variante 2.:

Beim Programmstart wird dem Anwender ein neues Update signalisiert, er kann es mit Hilfe eines Assistenten einspielen.
Was hierbei im Hintergrund verändert wird, ist der Zeitpunkt zu dem das Update signalisiert wird und der Speicherort des Updatepaketes.

Jedes Installationspaket von MAGELLAN besitzt eine korrespondierende Update-Infodatei. Dies ist eine kleine XML-Datei, die es MAGELLAN ermöglicht, eine neuere Version automatisch zu erkennen, herunterzuladen und zu installieren.

### Wozu dient die Update-Infodatei

Beim Programmstart wird die Versionsnummer aus der Registrierungsdatenbank Ihres Rechners mit der Versionsnummer in der Update-Infodatei auf unserem Server abgeglichen. Wird festgestellt, dass ein neueres Update vorliegt, kann das Updatepaket von dem ebenfalls in der Datei gespeicherten Pfad von unserem Server heruntergeladen werden.

### Was können Sie selbst beeinflussen

Sie können steuern wann den Anwendern das neue Update angeboten wird und von welcher Stelle das Updatepaket heruntergeladen wird.

Führen Sie dazu folgende Schritte aus:

1. Erstellen Sie ein Verzeichnis in Ihrem Netzwerk, auf das alle Nutzer zugreifen können.
2. Aktivieren Sie für alle MAGELLAN-Installationen die Option `Datenbank > Optionen > Update > Autoupdate aktivieren` und ändern den Standardpfad auf Ihr Netzwerkverzeichnis.
3. Laden Sie die Update-Infodatei pro Update herunter und speichern Sie die Datei an einem im Netzwerk für alle Anwender freigegebenen Verzeichnis.
4. Laden Sie das Updatepaket herunter und speichern es im selben Verzeichnis.
5. Öffnen Sie die Update-Infodatei mit einem Texteditor und passen den enthaltenen Pfad auf Ihren Speicherort der MAGELLAN6.msi an.

Für alle folgenden Updates führen Sie bitte nur noch die Schritte 4. und 5. aus.

### Anpassen der Clients

Damit MAGELLAN "weiß", dass es nicht auf unseren Internetseiten sondern in Ihrem Netzwerk nach neuen Updates suchen soll, müssen Sie bei allen Clients unter `Datenbank > Optionen > Auto-Update` den Pfad zu Ihrer Update-Infodatei eintragen.

[Update-Infodatei für MAGELLAN-Setup](https://download.stueber.de/bin/de/MAGELLAN/v10/MAGELLAN10.updateinfo)

### Herunterladen des Updatepaketes

Das Installationspaket finden Sie hier: [http://MAGELLAN.stueber.de/download.php](http://MAGELLAN.stueber.de/download.php)
Bitte laden Sie es herunter und speichern es in Ihrem Netzwerkverzeichnis.

### Editieren der Update-Infodatei

Die Update-Infodateien für MAGELLAN finden Sie hier:

* [Update-Infodatei für MAGELLAN-Setup](https://download.stueber.de/bin/de/MAGELLAN/v10/MAGELLAN10.updateinfo)

Update-Infodateien besitzen die Dateiendung `.UPDATEINFO`. Öffnen Sie die Datei per Texteditor.

Ein Beispiel für eine Update-Infodatei:

``` xml
<?xml version="1.0" encoding="utf-8"?>
<UpdateInfo>
<UpdatePackage
Product="MAGELLAN10"
ProductVersion="10.0.1"
SetupFileName="MAGELLAN9.msi"
SetupURL="https://download.stueber.de/bin/de/MAGELLAN/v10/MAGELLAN10.msi"
SetupSize="243156992" />
</UpdateInfo>
```

Passen Sie den Pfad in der Zeile "SetupURL" auf den Speicherort des heruntergeladenen Updatepaktes an und speichern die Änderung. Fertig!

## Variante 4

### Aktualisieren per Gruppenrichtlinien oder Softwareverteilung

MAGELLAN 6 installiert sich in drei Ordner, für diese drei Ordner (und die Registry) müssten Zugriffsrechte gewährt werden:

Was|Pfad am Beispiel Windows 10
--|--
Alle Programmdateien (EXE etc.))|  `C:\Program Files (x86)\Stueber Systems\MAGELLAN 10`
Alle Konfigurationsdaten (LIC, EVM etc.)|`C:\ProgramData\Stueber System\MAGELLAN 10`
Alle Dokumente (Datenbank, Berichte etc.)| `C:\Dokumente und Einstellungen\All Users\Dokumente\Stueber Systems\MAGELLAN 10`

Es wird das Recht benötigt in die Registry zu schreiben!

!!! info "Hinweis"

    Die Angaben variieren je nach Betriebssystem. Im oberen Beispiel beziehen sich die Angaben auf Windows XP (unter Vista wäre der zweite Pfad zum Beispiel: `C:\Users\Public\Documents\Stueber Systems`).

Für die Installation von MAGELLAN  wie auch für das Update von MAGELLAN benötigt der Benutzer Administratorenrechte bzw. er benötigt das Recht in Systemverzeichnisse ("C:\Programme" und "C:\Windows") zu schreiben und in die Registry unter HKEY-LOCAL-MACHINE zur schreiben. Das bedeutet, es könnte auch eine andere Benutzergruppe installieren, sofern diese die oben genannten Zugriffsrechte haben.
Technisch gesehen sind Erstinstallation und Update gleich.
Um die Updates möglichst ohne viel Aufwand auf mehreren Rechnern zu verteilen, gibt es zwei Möglichkeiten:

a. die Gruppenrichtlinien in einem Windows-Domänen-Netzwerk zu nutzen

b. Professionelle Software-Verteilung

* zu a.: Jeder Benutzer in einer Domäne kann bestimmte Rechte erhalten. Durch das Verwenden von Gruppenrichtlinien können diese Benutzer zu Gruppen zusammengefasst werden und dann diesen gesammelt Rechte zuweisen. Zum Beispiel könnten diese Gruppen das Recht haben bestimmte Programme zu installieren.  

* zu b.: Es gibt verschiedene Programme zur automatisierten Softwareverteilung innerhalb eines Netzwerkes. Sie könnten so von zentraler Stelle aus die Installation der Updates anstoßen.

Grundsätzlich basiert unsere Installation auf der MSI-Technologie. Mit dieser MSI-Technologie wird beispielsweise auch MS Office installiert.

Folgenden Parameter sind möglich:

Silent-Setup für MAGELLAN 10:

Installationstyp|Parameter
--|--
Serverinstallation|msiexec /i "C:\MySetup\MAGELLAN10.msi" /q INSTALLMODE="Server" APPDIR="C:\MyFolder\MAGELLAN"
Clientinstallation|msiexec /i "C:\MySetup\MAGELLAN10.msi" /q INSTALLMODE="Client" APPDIR="C:\MyFolder\MAGELLAN"
Deinstallation|msiexec /x "C:\MySetup\MAGELLAN10.msi" /q

!!! info "Hinweis"

    /i bedeutet immer Installation und /x immer Deinstallation. 
    Bitte starten Sie die Kommandozeilenaufrufe mit Administratorenrechten!

![Eingabeaufforderung per Rechtsklick mit administrativen Rechten starten](/assets/images/updates.verteilen/eingabeaufforderung.als.admin.png)

## Weitere Aktionen per Silentmode

Bitte schauen Sie hierzu den Abschnitt ["Aktionen im Silentmode"](/schulverwaltung/installation/magellan-administrator-im-silentmode-starten/) an!
