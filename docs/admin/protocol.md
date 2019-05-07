# Protokollierung in MAGELLAN


Aus Sicherheits- und Datenschutzgründen sollen Änderungen der Daten in der MAGELLAN-Datenbank mitprotokolliert werden. Jegliche Änderung der Daten und Datenstruktur, das heißt, Erstellen, Ändern oder Löschen von Daten oder Teile der Datenstruktur soll im Nachhinein nachvollzogen werden können. Nachfolgend erklären wir Ihnen, wie Sie die Protokollierung auf einem Windows basierten Rechner einrichten können.


## Bevor Sie beginnen


Diese Informationen sind nur relevant, wenn Sie mindestens MAGELLAN 6 und Firebird 2.5.2 einsetzen. Wenn Sie bereits Firebird 2.5 einsetzen, können Sie problemlos den Firebird Datenbankserver auf die aktuelle Version 2.5.2 oder auf eine höhere Version 2.5.x von Firebird 2.5 aktualisieren.


## Die Technik


Der Firebird Datenbankserver bringt seit Version 2.5 von zu Hause aus die Möglichkeit des sogenannten „Auditing“ mit.


Jede Firebird Datenbank hält interne Systemtabellen zur Verwaltung verschiedenster Aufgaben. Die Monitoring Tabellen sind für die Überwachung der Aktivitäten einer Datenbank zuständig.


Der Datenbankserver erhält Kenntnis zur Überwachung einer oder mehrerer Datenbanken oder des gesamten Firebird-Dienstes über eine Konfigurationsdatei.


Die Protokolle werden in Textdateien gespeichert. Sie haben die Möglichkeit anzugeben, ob die Protokolle in einer oder mehreren Textdateien gespeichert werden sollen.


## Einrichten der Protokollierung


Das „Auditing“ bzw. die Protokollierung in Firebird muss explizit eingestellt werden. Dazu bearbeiten Sie Konfigurationsdateien der Firebird-Installation.


Die Konfigurationsdateien befinden sich nach einer Standardinstallation im Stammverzeichnis der Firebird-Installation, z.B. C:\Programme\Firebird_2_5_2\firebird.conf


Der Vollständigkeit halber sei erwähnt, dass Firebird zwischen einem System Audit und einem User Trace unterscheidet.


Das System Audit wird beim Start des Firebird-Servers automatisch gestartet, es ist keine Benutzerinteraktion notwendig. Das User Trace wird explizit unter Angabe einer Trace-Konfiguration durch einen Benutzer gestartet. Weitere Unterschiede entnehmen Sie bitte der Firebird Dokumentation.


Im weiteren Verlauf beziehen wir uns lediglich auf das System Audit.


### Bearbeiten von Konfigurationsdateien


Konfigurationsdateien in Firebird sind Textdateien und können mit jedem beliebigen Texteditor (z.B. Windows Notepad) bearbeitet werden.


Zeilen die mit # beginnen, sind Kommentare und werden nicht verarbeitet. Auch Zeilen, die eigentlich Optionen und Befehle für die Konfigurationsdatei beinhalten, können mit # voran auskommentiert werden und werden dann nicht verarbeitet.


Möchte man eine Option „aktivieren“, muss lediglich die # entfernt werden.


### Konfigurationsdatei „Firebird.conf“


Dies ist die Hauptkonfigurationsdatei von Firebird. Diese enthält einen Eintrag, in dem die Konfigurationsdatei für eine etwaige Protokollierung eingestellt werden muss. Nach der Installation von Firebird sieht der Abschnitt für die Protokollierung in dieser Datei wie folgt aus:





```
# ----------------------------
# Trace configuration file for system audit
#
# Empty value means that system audit is turned off.
#
# Type: string
#
# AuditTraceConfigFile =

```




Wie Sie sehen gibt es eine kurze Information zur Option, die aber durch die Raute # „deaktiviert“ ist. Die Information gibt an, dass die Option auch dann nicht aktiv ist, wenn nur die Raute entfernt wird, da ein leerer Wert hinter dem Gleichheitszeichen in diesem Falle das gleiche bewirkt.


Zur Aktivierung der Protokollierung müssen folgende Schritte durchlaufen werden:


1. "#" Zeichen entfernen
2. Einen vollständigen Pfad zu einer neuen Konfigurationsdatei eingeben
3. Erstellen der Konfigurationsdatei (Textdatei) im angegebenen Ordner und Dateinamen


> #### primary::Hinweis
>
> Um die "Firebird.conf" bearbeiten zu können und die Änderungen speichern zu können, sollte der Firebirddienst unter `Systemsteuerung > Verwaltung > Dienste` gestoppt werden.


Das Ergebnis der Bearbeitung kann wie folgt aussehen:




```
# ----------------------------
# Trace configuration file for system audit
#
# Empty value means that system audit is turned off.
#
# Type: string
#
AuditTraceConfigFile = “C:\Programme\Stueber Systems\Magellan\Firebird\audit.conf“
```




Damit geben wir an, dass Firebird im entsprechenden Ordner die Datei audit.conf laden soll, um die weiteren Optionen zu einer Protokollierung auszulesen.

An dieser Stelle sei angemerkt, dass STÜBER SYSTEMS bereits eine vorbereitete und ausdokumentierte Konfigurationsdatei audit.conf für Sie bereitstellt. Diese kann an Ihre Wünsche angepasst werden.
Die Konfigurationsdatei befindet sich nach der Magellan-Installation im Verzeichnis

[ProgramFolder]\Stueber Systems\Magellan\Firebird\audit.conf.


> #### warning::Wichtig!
>
> AuditTraceConfigFile = “C:\Programme\Stueber Systems\Magellan\Firebird\audit.conf“
Pfadangaben, die Leerzeichen aufweisen müssen in Anführungszeichen gesetzt werden.


## Einstellen der Konfigurationsdatei audit.conf


Die Verarbeitung der Konfigurationsdatei unterliegt folgenden Regeln:


* Konfiguration wird von oben nach unten abgearbeitet


* gibt zwei Abschnitte für die Konfiguration:


* "database" (Datenbank) und
* "services" (Dienste)


* Die Abschnitte können unterteilt werden in Bereiche für Standardangaben und spezifische Angaben


* Jeder Abschnitt darf lediglich EINEN Bereich für Standardangaben enthalten


* Nach dem der Standardbereich des Abschnittes abgearbeitet wurde, wird nach Abschnitten für spezifischen Angaben gesucht


* Wenn ein Abschnitt mit spezifischen Angaben zur aktuellen Datenbank oder Dienst übereinstimmt, werden die Optionen sofort auf die Datenbank oder den Dienst angewandt und die weitere Verarbeitung beendet.


### Abschnitt "database"

Wenn Sie die Angaben auf alle Datenbanken setzen möchten, müssen Sie folgendes eingeben:

**Beispiel 1:**

`<database></database>`

Wenn Sie die Angaben auf alle Datenbanken setzen möchten, die "Magellan6.fdb" heißen, müssen Sie folgendes eingeben:

**Beispiel 2:**

```
<database %[\\/]Magellan6.FDB>
```
 
Wenn Sie die Angaben auf eine bestimmte Datenbank setzen möchten, müssen Sie den Pfad zur Datenbank angeben.

**Beispiel 3:**

````
<database "C:\\Dokumente und Einstellungen\\All Users\\Dokumente\\Stueber Software\\Magellan 6\\Datenbank\\Magellan6.FDB"></database>
````

> #### success::Tipp
>
> Wir empfehlen die Eintragung wie in **Beispiel 2**.




#### Parameter für Abschnitt "database"



Parameter| Bedeutung| Werte
--|--|--
enabled| aktiv/nicht aktiv |true/false
log_filename| Pfad der Logdatei. Nur für System-Audit relevant |String
max_log_size |Maximale Größe der Logdatei, bevor eine neue Logdatei erzeugt wird (Logrotation). Nur für System-Audit relevant |Integer<br/>0 = stellt die Logrotation aus und schreibt alles in eine Logdatei
include_filter| Nur SQL-Anweisungen protokollieren, die dem regulären Ausdruck entsprechen |String (regulärer Ausdruck)
exclude_filter |SQL-Anweisungen explizit nicht protokollieren, die dem regulären Ausdruck entsprechen |String (regulärer Ausdruck)
log_connections |Protokollierung von Verbindungsaufbau und Verbindungsabbau |true / false
connection_id| Protokollierung nur für bestimmte Verbindungs-ID aktivieren (CURRENT_CONNECTION). |Integer<br/>0 = Alle Verbindungen
log_transactions |Protokollierung von Transaktionsanweisungen (Start, Commit, Rollback) |true / false
log_statement_prepare |Protokollierung, wenn eine Anweisung durch ein Prepare in das BLR-Format übersetzt wurde |true / false
log_statement_free |Protokollierung, wenn eine Anweisung freigegeben wurde | true / false
log_statement_start| Protokollierung, wenn eine Anweisung gestartet wurde | true / false
log_statement_finish |Protokollierung, wenn eine Anweisung beendet wurde | true / false
log_procedure_start |Protokollierung, wenn eine Stored Procedure gestartet wurde | true / false
log_procedure_stop |Protokollierung, wenn die Abarbeitung einer Stored Procedure beendet wurde | true / false
log_trigger_start |Protokollierung, wenn ein Trigger gestartet wurde | true / false
log_trigger_stop |Protokollierung, wenn die Abarbeitung eines Triggers beendet wurde | true / false
log_context |Protokollierung, wenn eine benutzerdefinierte Kontextvariable mit RDB$SET_CONTEXT gesetzt wurde | true / false
log_errors |Protokollierung von Fehlern | true / false
log_sweep |Protokollierung der Sweep Aktivitäten | true / false
time_threshold_| *_finish-Parameter werden nur dann protokolliert, wenn die Ausführungszeit der protokollierten Anweisung diesen Wert überschreitet |Integer (Millisekunden)
print_plan |Ausgabe des Ausführungsplans des Optimizers | true / false
print_perf |Ausgabe von detaillierten Performancestatistiken | true / false
log_blr_requests |Protokollierung von BLR Requests | true / false
print_blr |Ausgabe des BLR-Outputs | true / false
log_dyn_requests |Protokollierung von DYN Requests | true / false
print_dyn |Ausgabe des DYN-Outputs | true / false
max_sql_length |Maximale Länge des protokollierten SQLs. Rest wird im Trace-Output abgeschnitten |Integer (Zeichen)
max_blr_length |Maximale Länge des ausgegebenen BLR-Outputs. Rest wird im Trace-Output abgeschnitten |Integer (Zeichen)
max_dyn_length |Maximale Länge des ausgegebenen DYN Outputs. Rest wird im Trace-Output abgeschnitten |Integer (Zeichen)
max_arg_length| Maximale Länge des ausgegebenen Parameternamens bei parametrisierten Anweisungen |Integer (Zeichen)
max_arg_count |Maximale Anzahl der auszugebenden Parameter bei parametrisierten Anweisungen |Integer

### Abschnitt "services"


Die Angaben für alle Dienste werden innerhalb von <services></services> gesetzt.


#### Parameter für Abschnitt "services"


Parameter |Bedeutung |Werte
--|--|--
enabled |aktiv/nicht aktiv |true/false
log_filename |Pfad der Logdatei. Nur für System-Audit relevant |String
max_log_size |Maximale Größe der Logdatei, bevor eine neue Logdatei erzeugt wird (Logrotation).<br/><br/>Nur für System-Audit relevant |Integer<br/><br/>0 = stellt die Logrotation aus und schreibt alles in eine Logdatei
include_filter| Nur Services Events protokollieren, die dem regulären Ausdruck entsprechen |String (regulärer Ausdruck)
exclude_filter |Services Events explizit nicht protokollieren, die dem regulären Ausdruck entsprechen |String (regulärer Ausdruck)
log_services |Protokollierung von Service-Attach/Detach/Start-Ereignissen |true/false
log_service_query |Protokollierung der Rückgabe von Serviceaufrufen |true/false
log_errors |Protokollierung von Fehlern |true/false


> #### warning::Wichtig!
>
> Die Backslashes ( \ ) in Pfadangaben müssen mit einem weiteren Backslash maskiert werden, Beispiel: <database "C:\\Dokumente und Einstellungen\\All Users\\Dokumente\\Stueber Software\\Magellan 6\\Datenbank\\Magellan6.FDB"></database> Pfadangaben, die Leerzeichen aufweisen müssen in Anführungszeichen gesetzt werden.

