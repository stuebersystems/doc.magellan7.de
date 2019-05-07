
# Installation von Firebird 2.5

> #### warning::Wichtig!
>
> Diese Installation wird einmalig im Netzwerk auf dem Rechner, auf dem später Ihre MAGELLAN-Datenbank liegen wird ausgeführt. 

Laden Sie bitte das Firebird-Installationspaket von unseren Webseiten oder unter [folgendem Link](https://magellan.stueber.de/download.php). Starten Sie anschließend die Firebird Installation durch einen Doppelklick auf die Datei `Firebird-2.5......Win32.exe`. Bitte übernehmen Sie im daraufhin startenden Installationsassistenten auf der Karte „Komponenten auswählen“ die voreingestellten Optionen.

![Komponenten auswählen](/assets/images/fb-components.png)

Auf der Karte „Zusätzliche Aufgaben auswählen“ übernehmen Sie bitte die Optionen und aktivieren zusätzlich das Häkchen „Die Firebird Client-Bibliothek ins Systemverzeichnis kopieren“.

![Zusätzliche Aufgaben auswählen](/assets/images/fb-tasks.png)

!!! warning "Wichtig"

	Firebird wird nur dem Rechner installiert werden, auf dem zukünftig die Datenbank gespeichert wird. Das kann Ihr Server sein oder auch ein netzwerkunabhängiger Rechner. 
	
	Firebird nutzt für den Datenverkehr den Port 3050, mitunter ist dieser Port durch die Windows Firewall gesperrt. Richten Sie bitte eine Ausnahme \(Eingehende und Ausgehende Regel\) für diesen Port ein und versuchen es bitte erneut.
