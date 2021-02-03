# Umstieg von MAGELLAN 7 auf MAGELLAN 8

Grob zusammengefasst müssen folgende Punkte erledigt werden:

* Stellen Sie bitte sicher, dass Sie jeweils die aktuellste Ausgabe von MAGELLAN 7 und Firebird 2.5.9 einsetzen. Die Installationspakete finden Sie wie gewohnt auf unserer Webseite im [Downloadbereich](https://magellan.stueber.de/download.php).
* Sie installieren sich MAGELLAN 8. Folgen sie hierbei den Anleitungen für den [Server](https://doc.magellan7.stueber.de/schulverwaltung/installation/version8/server.installieren/) und für die [Clients](https://doc.magellan7.stueber.de/schulverwaltung/installation/version8/arbeitsplatz.installieren/).
* Sie stoppen anschließend den Firebird-Dienst, kopieren die MAGELLAN 7-Datenbank ins MAGELLAN 8-Verzeichnis, starten den Firebird-Dienst wieder.
* Benennen Sie die Datenbankkopie im MAGELLAN 8-Verzeichnis von Magellan7.fdb in Magellan8.fdb um.
* Anschließend starten Sie MAGELLAN 8 und lizenzieren das Programm.
* Das Programm aktualisiert die Datenstruktur.
* Haben Sie eigene Berichte, Skripte, Seriendruckvorlagen? Kopieren Sie diese in die neuen Verzeichnisse.
* Sie synchronisieren für Ihre Benutzer abschließend die Zugriffsrechte und los geht es!