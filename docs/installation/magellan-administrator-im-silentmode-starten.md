
# MAGELLAN ADMINISTRATOR im Silent-Mode starten


## Was ist der Silent-Mode?

Mit Silent-Mode benennt STÜBER SYSTEMS den Aufruf der Anwendung durch Parameter zur Durchführung von bestimmten Funktionalitäten, ohne dass ein Programmfenster geöffnet oder eine Programmeingabe vom Benutzer erwartet wird. Alle wichtigen Informationen zur Durchführung werden durch die Parameter bestimmt.

Zweck des Silent-Mode ist es, die Anwendung durch z.B. den Taskmanager von Windows im Hintergrund wiederkehrende Aufgaben erledigen zu lassen, ohne dass sich ein Benutzer darum kümmern müsste, also zur Automatisierung bestimmter Aufgaben. 

## Übersicht der Silent-Mode Aufgaben

Der Magellan-Administrator erlaubt folgende Aufgaben im Silent-Mode zu erledigen:

*	Datenbank-Anmeldung
*	Benutzerrechte synchronisieren 
*	Import über das Magellan-Importformat

Diese Punkte werden ausführlich in den kommenden Punkten erläutert.

### Datenbank-Anmeldung

Sie haben die Möglichkeit den MAGELLAN ADMIMINISTRATOR direkt ohne Eingabe von Benutzernamen, Passwort und Auswahl der Datenbank zu starten, wenn Sie diese In-formationen einfach als Parameter angeben.

Parameter:

Nr.|Parameter
---|---
1.|/Login=Benutzername
2.|/Keyword=Passwort
3.|/Connection=Datenbank-Alias


> #### warning::Wichtig!
>
> Jegliche weitere Silent-Mode Funktion hängt von diesen Parametern ab. Das bedeutet diese Parameter sind Pflichtangaben für alle weiteren Silent-Mode Aufgaben.
Die Parameter der Datenbank-Anmeldung sind die einzigen Parameter die mit anderen Silent-Mode Funktionen kombinierbar sind.
 
## Benutzerrechte synchronisieren

Eine oft wiederkehrende Aufgabe ist das Synchronisieren der Benutzerrechte. Zusätzlich zu den Parametern der Datenbank-Anmeldung müssen folgende Parameter angegeben werden.

Nr.|Parameter
---|---
1.|/UserSync

## Import über das Magellan-Importformat

Der Import von Daten ist größtenteils ein einmaliger Import zum Hinzufügen von Fremddaten nach Magellan. Für Schüler- und Lehrerdaten gibt es aber die Möglichkeit, die Stammdaten zu aktualisieren.
Voraussetzung für eine solche Aktualisierung ist, dass die Fremddaten mit einer externen GUID importiert wurden und die Aktualisierung anhand dieses Feldes Externe GUID (Feld GUIDExtern) zur nachträglichen Wiedererkennung der Datensätze, aktualisiert werden. Zusätzlich zu den Parametern der Datenbank-Anmeldung müssen folgende Parameter angegeben werden.

## Parameter

Nr.|Parameter
---|---
1.|/Import=Vollständiger Pfad zur Importdatei
2.|/Mandant=ID des Mandanten in den importiert wird

Der Dateiname der Importdatei muss der Importspezifikation entsprechen:
* Schüler-Stammdaten: schueler.import.csv
* Lehrer-Stammdaten: lehrer.import.csv

## Beispiel

Den MAGELLAN ADMIMINISTRATOR  im Silent-Mode aufrufen, zum Import von Schüler-Stammdaten mit dem Firebird Standard SYSDBA und Passwort:


```
C:\Programme\Stüber Systems\MagAdmin.exe /Login=SYSDBA 
/Keyword=masterkey 
/Connection=Magellan /Import=“C:\Import\schueler.import.csv“ /Mandant=1
```


> #### warning::Wichtig!
>
> Achten Sie bitte darauf, dass in Windows ein parametrisierter Aufruf nicht länger als 260 Zeichen sein darf.

