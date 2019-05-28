# MyMAGELLAN - dezentrale Notenerfassung

Aus MAGELLAN heraus können Zeugnisse gedruckt werden. Als Voraussetzung für Zeugnisse müssen Halbjahres- oder Jahresergebnisse (Noten, Punkte oder auch Beurteilungstexte für Grundschüler) und weitere Zeugnisdaten (Zeugnisbemerkungen, Fehlzeiten, Zeugnisdatum usw) in MAGELLAN vorhanden sein.
Das kann direkt über MAGELLAN erfolgen, allerdings müsste dann jeder Kollege während der Notenerfassung auf die Datenbank im Schulverwaltungsnetz zugreifen können.

Alternativ können pro Lehrer, in ihrer jeweiligen Rolle als Fachlehrer, Klassenlehrer und/oder Tutor, Dateien erzeugt werden, die die notwendigen Schülerdaten enthalten. 
Beispiel:
Der Biologie-Fachlehrer erhält nur die Bio-Fachzeilen der von ihm unterrichteten Schüler, der Klassenleiter erhält alle Fachzeilen der Schüler seiner Klasse.

Jeder Lehrer füllt seine Datei aus und bringt sie wieder mit in die Schule, dort werden die Daten der Lehrerdateien in die MAGELLAN-Datenbank übergeben.

Für diese Alternative gibt es das zweiteilige Modul MyMAGELLAN, das aus dem **MyMAGELLAN Center** (für die Erzeugung der Lehrerdateien und den Import der später gefüllten Lehrerdateien) und **MyMAGELLAN** (Werkzeug der Lehrer zum Füllen der Lehrerdatei) besteht.

Modul|Funktion
--|--
**MyMAGELLAN CENTER** |- Erzeugt aus der Datenbank heraus für Lehrer Dateien, die je nach Rolle des Lehrers (Fachlehrer, Klassenleiter, Tutor) eine unterschiedliche Menge an Daten der Schüler enthält<br/>- zeigt eine Übersicht, wessen Datei erstellt wurde, wessen Datei bereits gefüllt wieder übermittelt wurde, welche Dateien wieder nach MAGELLAN eingelesen wurden<br/>- Liest die von den Lehrern gefüllten Dateien wieder in die Schulverwaltungsdatenbank ein
**MyMAGELLAN** |Wird von den Lehrern auf dem für die Noteneingabe genutzten Windowsrechner installiert<br/>Ist das Programm, mit dem der Lehrer seine Notendatei füllt


!!! info "Hinweis"

	Die Nutzung von MyMAGELLAN setzt eine gesonderte Lizenzierung voraus.

Die unten gezeigten Abschnitte beschreiben die Funktionalitäten des MyMAGELLAN CENTERs, die Verwendung des Lehrerwerkzeugs MyMAGELLAN beschreiben wir in der Dokumentation [MyMAGELLAN 7](https://doc.mymagellan7.stueber.de/).

* [Einführung](https://doc.magellan7.stueber.de/schulverwaltung/mymagellancenter/einfuehrung/)
* [Verteilen](https://doc.magellan7.stueber.de/schulverwaltung/mymagellancenter/verteilen/)
* [Organisation](https://doc.magellan7.stueber.de/schulverwaltung/mymagellancenter/organisation/)
* [Importlogik](https://doc.magellan7.stueber.de/schulverwaltung/mymagellancenter/importlogik/)
* [Einsammeln](https://doc.magellan7.stueber.de/schulverwaltung/mymagellancenter/einsammeln/)