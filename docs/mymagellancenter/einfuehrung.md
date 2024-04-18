# MyMAGELLAN - dezentrale Notenerfassung

!!! info "Hinweis"

	Die Nutzung von MyMAGELLAN setzt eine gesonderte Lizenzierung voraus. 
	In den nachfolgenden Abschnitten beschreiben wir das MyMAGELLAN CENTER, die Verwendung des Lehrerwerkzeugs MyMAGELLAN beschreiben wir in der Dokumentation [MyMAGELLAN 7](https://doc.mymagellan7.stueber.de/).

## MyMAGELLAN Center starten

Klicken Sie auf Start > Programme > STÜBER SYSTEMS > MAGELLAN ADMINISTRATOR und starten Sie dort den Aufruf "MyMAGELLAN Center". Die MAGELLAN-Datenbank ist grundsätzlich kennwortgeschützt. Wenn Sie MAGELLAN oder MAGELLAN-Administratorstarten, müssen Sie in einem Anmeldedialog Ihre Benutzerkennung und Ihr Kennwort angeben.

![MAGELLAN-Anmeldung](/assets/images/dialog-anmeldung.png)

Der Standardbenutzer lautet „sysdba“ und das dazugehörige Standardkennwort lautet „masterkey“. Mit dieser Standardkennung sind volle Administrationsrechte verbunden. Weitere Informationen zur Anlage und Editierung von Benutzerkennungen und den damit verbundenen Rechten finden Sie im Kapitel „Benutzerverwaltung“.

## Zweck

Aus MAGELLAN heraus können Zeugnisse gedruckt werden. Als Voraussetzung für Zeugnisse müssen Halbjahres- oder Jahresergebnisse (Noten, Punkte oder auch Beurteilungstexte für Grundschüler) und weitere Zeugnisdaten (Zeugnisbemerkungen, Fehlzeiten, Zeugnisdatum usw) in MAGELLAN vorhanden sein.
Das kann direkt über MAGELLAN erfolgen, allerdings müsste dann jeder Kollege während der Notenerfassung auf die Datenbank im Schulverwaltungsnetz zugreifen können.

Alternativ können pro Lehrer, in ihrer jeweiligen Rolle als Fachlehrer, Klassenlehrer und/oder Tutor, Dateien erzeugt werden, die die notwendigen Schülerdaten enthalten.
Beispiel:
Der Biologie-Fachlehrer erhält nur die Bio-Fachzeilen der von ihm unterrichteten Schüler, der Klassenleiter erhält alle Fachzeilen der Schüler seiner Klasse.

Jeder Lehrer füllt seine Datei aus und bringt sie wieder mit in die Schule, dort werden die Daten der Lehrerdateien in die MAGELLAN-Datenbank übergeben.

Für diese Alternative gibt es das zweiteilige Modul MyMAGELLAN, das aus dem **MyMAGELLAN Center** (für die Erzeugung der Lehrerdateien und den Import der später gefüllten Lehrerdateien) und **MyMAGELLAN** (Werkzeug der Lehrer zum Füllen der Lehrerdatei) besteht.

**MyMAGELLAN CENTER**<br/>Administrationstool|**MyMAGELLAN**<br/>Lehrertool
--|--
- Erzeugt aus der Datenbank heraus für Lehrer Dateien, die je nach Rolle des Lehrers (Fachlehrer, Klassenleiter, Tutor) eine unterschiedliche Menge an Daten der Schüler enthält<br/><br/>- zeigt eine Übersicht, wessen Datei erstellt wurde, wessen Datei bereits gefüllt wieder übermittelt wurde, welche Dateien wieder nach MAGELLAN eingelesen wurden<br/><br/>- Liest die von den Lehrern gefüllten Dateien wieder in die Schulverwaltungsdatenbank ein|- Wird von den Lehrern auf dem für die Noteneingabe genutzten Windowsrechner installiert<br/><br/>- Ist das Programm, mit dem der Lehrer seine Notendatei füllt.

## Sicherheit

Die Lehrer erhalten eine Datei, in die Zeugnisdaten in der Regel außerhalb des Verwaltungsnetzes eingegeben werden. Um die sensiblen Daten zu schützen gibt es einen zweistufiges Schutz.

Art des Schutzes|Bemerkungen
--|--
Zugriffsschutz|Die Datei kann mit einem Passwort versehen werden. Hierbei gibt es drei Möglichkeiten: <br/><br/>1. Allen MyMAGELLAN-Dateien wird beim Erzeugen ein Passwort zugewiesen.<br/><br/>2. Es kann dasselbe Passwort wie für die MAGELLAN-Anmeldung der Nutzer verwendet werden.<br/><br/>3. Es kann jedem Nutzer ein individuelles MyMAGELLAN-Passwort zugewiesen werden. 
Schutz der Dateiinhalte| Bis Ausgabe 7.1.8: <br/>Die Daten werden in einer nicht lesbare Binärdatei gespeichert<br/><br/>Seit der Ausgabe 7.1.9: <br/>Die Daten werden in einer XML-Datei verschlüsselt (AES-Verschlüsslung mit 256-Bit-Schlüssellänge).<br/><br/>Unabhängig von der Ausgabe ist das Nutzerpasswort in der Datei mitgespeichert, aber zusätzlch durch eine kryptografische Funktion gegen ein Auslesen gesichert.

## Übersicht der Vorgehensweise

|In den nachfolgenden Kapiteln beschreiben wir die Vorgehensweise:|
|:--|
|[Verteilen](https://doc.magellan.stueber.de/mymagellancenter/verteilen/)|
| [Organisation](https://doc.magellan.stueber.de/mymagellancenter/organisation/)|
| [Importlogik](https://doc.magellan.stueber.de/mymagellancenter/importlogik/)|
| [Einsammeln](https://doc.magellan.stueber.de/mymagellancenter/einsammeln/)|
