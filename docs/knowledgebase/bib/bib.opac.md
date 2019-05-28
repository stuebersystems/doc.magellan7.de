# OPAC-Unterstützung

Die bisherige Technik zur Unterstützung von OPAC-Server wurde von keinem Dienst mehr unterstützt, wir haben sie daher in der MAGELLAN BIBLIOTHEK durch eine neue Technik ersetzt. Das bedeutet konkret, das Dialogfenster „Extras > Opac-Server“ wurde ausgeblendet und die Internet-Recherche berücksichtigt die eingetragenen Server nicht mehr. Als Ersatz haben wir eine neue OPAC-Unterstützung entwickelt, die auf der aktuellen SRU-Schnittstelle basiert. Diese wird von vielen Diensten, u.a. der Deutschen Nationalbibliothek verwendet. Diese Technik wurde für die MAGELLAN 7 BIBLIOTHEK entwickelt, in MAGELLAN 6 steht es als eigenständige Anwendung „OPAC-Research“ zu Verfügung.
 
## OPAC-Research

Soweit Sie in den Optionen von MAGELLAN BIBLIOTHEK die Online-Recherche aktiviert haben, wird beim Eintragen neuer Medien über die ISBN-Suche die Anwendung OPAC-Research gestartet. Beim ersten Start der Anwendung müssen entsprechende OPAC-Server eingerichtet werden, über die gesucht werden kann.

## Einrichten von OPAC-Research

![Einrichten von OPAC-Research](images/opac01.png)
 
Beim ersten Start von OPAC-Research landen Sie auf der Registerkarte zum Verwalten der OPAC-Server. Über die Schaltfläche 1 (siehe Bild) können Sie die von uns bereits getesteten OPAC-Server direkt hinzufügen. Aktuell handelt es sich um den Server der Deutschen Nationalbiblio-thek (Weiterhin DNB genannt.). In den meisten Fällen werden Sie eine Anmeldung/Registrierung bei den jeweiligen Serverbetreibern benötigen. Die Deutsche Nationalbibliothek erfordert z. B. eine [Registrierung](https://portal.dnb.de/myAccount/register.htm?method=showRegisterFormExtern&view=redirect%3A%2FmyAccount%2Fregister.htm&dodServiceUrl=https%3A%2F%2Fportal.dnb.de%2Fdod), da neben den kostenfreien Abfragen auf ihre Server auch kostenpflichtige Abfragen möglich sind und diese über das Kundenkonto abgerechnet werden können. Die neue Technik erlaubt uns Anmeldungen an die jeweiligen Server durchzuführen. Im Falle der DNB benötigen Sie einen „Zugriffstoken“, den Sie nach der Registrierung im Portal anfragen können. 
 
![Auf der Registerkarte „Authentifizierung“ können Sie den Zugriffstoken einfügen.](images/opac02.png) 
 
![Speichern Sie danach den Eintrag.](images/opac03.png)    

Sie haben somit erfolgreich den ersten Server eingetragen. Die Serverdaten werden in eine Konfigurationsdatei gespeichert.

![Die Serverdaten werden in eine Konfigurationsdatei gespeichert](images/opac04.png)   
 
Wechseln Sie auf die Registerkarte „Recherche“, um mit der Recherche des Medium fortfahren. Zukünftig wird die Konfigurationsdatei geladen und die vorhandenen Server für die Recherche verwendet. Sie landen dann automatisch auf der Registerkarte „Recherche“ und die Suche wird aufgrund des Einscannens des Barcodes in MAGELLAN BIBLIOTHEK automatisch ausgeführt.
Scannen Sie das Medium beim ersten Mal bitte erneut ein, bzw. geben es über die Tastatur ein und schließen dann mit der Eingabetaste ab. OPAC-Research stellt eine Verbindung zum ersten Server her und sucht nach dem Barcode. Wenn Sie mehrere Server eintragen, dann werden alle Server nacheinander angefragt, bis ein Server einen Eintrag zum Barcode auf dem jeweiligen Server findet. Das Ergebnis wird Ihnen im unteren Bereich dargestellt. In manchen Fällen gibt es mehrere Ergebnisse. Markieren Sie den gewünschten Eintrag und klicken Sie auf die Schaltfläche „Übernehmen und Zurück“, um den Eintrag nach MAGELLAN BIBLIOTHEK zu übertragen und OPAC-Research zu beenden. Wenn Sie auf „Schließen“ klicken, wird der Eintrag nicht übernommen und OPAC-Research beendet.


![Fenster "Neue Medien und Exemplare anlegen"](images/opac05.png)   

 Der ausgewählte Eintrag wird nach MAGELLAN BIBLIOTHEK übertragen und die verwertbaren Informationen noch einmal zur manuellen Bearbeitung dargestellt. Ab hier arbeiten Sie wie gewohnt in MAGELLAN BIBLIOTHEK weiter.
