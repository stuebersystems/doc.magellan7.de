# Server Voraussetzungen \(Hardware\)

Aufgrund häufiger Nachfragen zum Thema Hardware für den Firebird Datenbank-Server haben wir hier für Sie einige Informationen zusammengetragen.

## BENÖTIGTER FESTPLATTENSPEICHER

Das Firebird-System selbst benötigt einen Festplattenspeicher von ca. 25 MB.   
Eine leere MAGELLAN-Datenbank liegt derzeit bei ca. 20 MB und hat bei großen Schulen erfahrungsgemäß eine Größe bis zu 800 MB. Sollten Sie für Ihre Schüler (auch für ehemalige Schüler) oder Lehrer Passfotos in der Datenbank speichern, kann die Datenbankgröße auf mehrere Gibabyte anwachsen. 

> #### success::Tipp
>
> Im MAGELLAN-Administrator (ab Version 6.5.32) können per Assistent Passbilder inaktiver Schüler entfernt werden.

## BENÖTIGTER RAM

Das Firebird-System benötigt laut Eigenangaben ca. 64 MB RAM für den Multi-Client-Betrieb.  
Ein handelsübliches Rechnersystem kommt mit 4, 8 oder 16 GB RAM. Selbst bei 4GB RAM sollten Sie keine Probleme haben.  
Unserer Empfehlung: um sich auch Luft für andere Dienste zu verschaffen, sollten mindestens 8 GB verbaut sein.  

Viele Systeme lassen sich nachrüsten, insofern, wenn die Platine ein Aufrüsten auf mindestens 16 GB erlaubt, dann sollte es auch zukünftig dahingehend kein Problem auftreten

## NETZWERK \(Die Basis\)

Der Wichtigste und vermutlich am meisten unterschätzte Bereich ist das bestehende NETZWERK auf dem gearbeitet wird.  
Üblicherweise arbeiten die Schulen bereits auf einem Netzwerk und selten ist dieses gerade erst neu aufgesetzt und mit aktueller Hardware versehen worden. In diesem Netzwerk werden alle üblichen schulischen Netzwerkaufgaben erledigt.  
Dies bedeutet aber auch, dass die Netzwerklast auf alle diese Aufgaben verteilt werden muss.

Letztlich kommt es darauf an, mit wie vielen Client-Verbindungen sie gleichzeitig auf dem Server zugreifen und wie schnell Ihr bestehendes Netzwerk diese Anfragen verarbeiten kann, bzw. wieviel Netzwerklast es stemmen muss, und wie schnell die Daten dann zwischen Client und Server gesendet werden können.

Genau das ist üblicherweise das Nadelöhr in den Schulen. 

Wenn Sie sich also Gedanken machen, wie alles reibungslos funktioniert könnte, sollte darauf geachtet werden, dass der Netzwerkserver und die verwendeten Komponenten dazwischen möglichst modern, schnell, aktuell und **gut konfiguriert** sind.

## FAZIT

Es kommt also nicht so sehr darauf an, welche Hardware für die Einrichtung eines Firebird-Servers für Ihre MAGELLAN-Datenbank verwendet wird, sondern in welches NETZWERK dieses dann eingebettet ist und wie reibungslos die Daten zwischen dem Client \(MAGELLAN-Anwendung\) und dem Server \(Firbird-Datenbanksystem\) ausgetauscht werden können.

## Quellen

[FirebirdSQL.org Handbuch](https://firebirdsql.org/manual/ufb-about-sysreq.html)

