# Die Struktur

Die Datengrundlage von MAGELLAN in der Version 7 ist eine Firebird-Datenbank. Firebird ist eine relationale Client/Server-Datenbank, auf die Sie unter anderem per ODBC direkt zugreifen können. Der standardmäßige Dateiname der Datenbank lautet MAGELLAN6.fdb
Auch Crystal Reports greift über ODBC auf die MAGELLAN-Datenbank zu. Die dafür benötigte Datenquelle wird von MAGELLAN automatisch eingerichtet.

Die aktuelle MAGELLAN-Datenbank besteht aus 298 Tabellen, 58 Ansichten sowie zahlreichen weiteren Datenbankobjekten (Trigger, Prozeduren usw.).

##	Tabellen und Ansichten

Eine Tabelle in einer Datenbank ist der physikalische Speicherort für eine strukturierte Form von Daten. So enthält beispielsweise die Tabelle `tblLehrer `alle in MAGELLAN gespeicherten Lehrer.
Eine Ansicht (der Fachbegriff ist VIEW) definiert mit Hilfe einer SQL-Abfrage eine bestimmte Sichtweise auf eine oder mehrere Tabellen. Die Daten sind weiterhin in den entsprechenden Tabellen gespeichert. So definiert beispielsweise die Ansicht Lehrer eine Sichtweise auf die Tabelle `tblLehrer`.
Wenn Sie sich die Datenstruktur von MAGELLAN näher betrachten, werden Sie feststellen, dass es neben den vielen Tabellen auch eine Reihe von Ansichten gibt. In einigen Fällen ist der Zugriff auf bestimmte Daten einer Tabelle nur über entsprechende Ansichten möglich.

Als Beispiel sei hier das Zusammenspiel zwischen der Tabelle `tblLehrer `und der Ansicht `Lehrer `genannt. Während die Tabelle `tblLehrer` stets alle Lehrer auflistet, sorgt die Ansicht `Lehrer `dafür, dass in den meisten Fällen nur der Lehrer aufgelistet wird, der zum aktuellen Benutzer passt. 

Der Hintergrund hierbei: Ein normaler Lehrer soll nur seine eigenen Personaldaten sehen können und nicht die seiner Kollegen. Der direkte Zugriff auf die Tabelle `tblLehrer `ist somit gesperrt.

Ansichten verhalten sich nach außen hin genauso wie Tabellen, so dass Sie in der Regel nichts weiter beachten müssen.



##	Schlüsseltabellen

Alle Tabellen und Ansichten, die den Feldaufbau „Kürzel“, „Schlüssel“, „Bezeichnung“ bzw. „Kürzel“, „Bezeichnung“ besitzen, sind sogenannte Schlüsseltabellen. Sie dienen dazu, die möglichen Werte bestimmter Felder auf eine vorgegebene Liste einzuschränken. Wenn Sie z.B. beim Schüler die Konfession eintragen wollen, so können Sie nur ein Kürzel eintragen, dass in der Schlüsseltabelle „Konfessionen“ definiert ist. 

Einige Schlüsseltabellen haben einen etwas anderen Aufbau, sie dienen aber dem gleichen Zweck. Hierzu zählen u.a. die Tabellen `Abschlussjahrgaenge`,  `Abteilungen`, `Banken`, `Berufe`, `Bildungsgaenge`, `Bezirke`, `Bundeslaender`, `Faecher`, `Fachtafeln`, `Gemeinden`, `Kreise`, `Noten`, `Sportfeste`, `Wettkämpfe` und `Verordnungen`.

Schlüsseltabellen machen mehr als 50 Prozent aller Tabellen in MAGELLAN aus. 

## 	Mandanten

Mandanten spielen in MAGELLAN eine zentrale Rolle. Sie ermöglichen die Verwaltung mehrerer organisatorisch eigenständigen Einheiten in einer zentralen Datenbank.  So können beispielsweise mehrere Schulen einer Stadt Ihre Daten zentral verwalten. Alle Mandanten sind in der Tabellen `tblMandanten `und `tblMandantenSchulformen ` definiert.

## 	Zeiträume

Zeiträume spielen, ähnlich wie Mandanten, eine zentrale Rolle in MAGELLAN. Sie ermöglichen eine zeitraumbasierte Verwaltung Ihrer Schuldaten. In der Regel handelt es sich bei Zeiträumen um Schulhalbjahre. Durch das Wechseln der Zeiträume können Sie Daten aus dem Blickwinkel unterschiedlicher Halbjahre betrachten. So können Sie die Laufbahnentwicklung einzelner Schüler zurück bis zum Einschulungszeitpunkt betrachten, und das inklusive Fächerzuordnung, Noten und Zeugnisse. Alle Zeiträume sind in der Tabelle Zeitraeume definiert.

##	Lehrerdaten 

Pro Mandant können beliebig viele Lehrer definiert werden. Die Daten der Lehrer finden Sie in den Tabellen `tblLehrer`, `tblLehrerLehraemter`, `tblLehrerFehlzeiten `und `tblLehrerSollBerechnung`.

##	Klassendaten

Pro Mandant können beliebig viele Klassen definiert werden. Jeder Klasse müssen zudem die Zeiträume zugeordnet werden, in denen sie gültig ist. Die Daten der Klassen finden Sie in den Tabellen `tblKlassen` und `tblKlassenZeitraeume`. 
Bitte beachten Sie, dass eine Klasse in der Rolle eines Oberstufenjahrgangs auftreten kann.

##	Schülerdaten

Pro Mandant können beliebig viele Schüler definiert werden.

### Schülerstammdaten

Die Stammdaten der Schüler sind in den Tabellen `tblSchueler`, `tblSchuelerSorgebe`, `tblSchuelerSchulen `und `tblSchuelerAusbildung `definiert. 

### zeitraumbezogene Schülerdaten

Im Lauf der Zeit durchläuft ein Schüler mehrere Klassen und Zeiträume an Ihrer Schule. Diese Angaben werden in den Tabellen `tblSchuelerKlassen`, `tblSchuelerZeitraeume`, `tblSchuelerFachdaten`, `tblSchuelerZeugnisbemerkungen `und `tblSchuelerZeugnisformulare `dokumentiert.

### Schülerdaten fürs Abitur

Daten zum Abitur werden in den Tabellen `tblSchuelerABI`, `tblSchuelerABIDetails`, `tblSchuelerABIZeugnisbemerkungen `und `tblSchuelerABIZeugnisformulare `abgelegt.

### berufsbezogene Schülerdaten

Daten zum Berufsschulabschluss werden in den Tabellen `tblSchuelerBBS`, `tblSchuelerBBSDetails`, `tblSchuelerBBSZeugnisbemerkungen ` und `tblSchuelerBBSZeugnisformulare ` abgelegt.

### Bundesjugendspiele und Sportfeste

Daten für Bundesjugendspiele und Sportfeste werden in den Tabellen `tblSchuelerSPF`, `tblSchuelerSPFDetails` abgelegt.
Bitte beachten Sie, dass ein Bewerber sich syntaktisch nicht von einem Schüler unterscheidet. 

##	Personendaten

Pro Mandant können beliebig viele Personen definiert werden. Die Daten der Personen finden Sie in der Tabelle `tblPersonen`.

##	Sorgeberechtigte

Pro Mandant können beliebig viele Sorgeberechtigte gespeichert werden. Die Daten der Sorgeberechtigten finden Sie in der Tabelle `tblSorgeberechtigte`.

##	Betriebe

Pro Mandant können beliebig viele Betriebe gespeichert werden. Die Daten der Betriebe finden Sie in den Tabellen `tblBetriebe`, `tblBetriebeBerufe`, `tblBetriebeBildungsgaenge` und `tblBetriebeKontakte`.

##	Schulen

Schulen werden unabhängig vom Mandanten gespeichert. Die Daten der Schulen finden Sie in den Tabellen `tblSchulen ` und `tblSchulenKontakte`.

##	Adressen

Pro Mandant können zusätzliche Adressen (z.B. die Adresse des Schulamts) gespeichert werden. Diese Adressen finden Sie in den Tabellen `tblAdressen `und `tblAdressenKontakte`

##	Medien

Medien bilden die Grundlage der Medienverwaltung. Alle Medien werden in der Tabelle `tblMedien `gespeichert und sind ebenfalls mandantenfähig. Die Medienverwaltung bildet jedes physische Exemplar zugehörig zum Medium in der Tabelle `tblMedienExemplare `ab. Detaildaten zu bestimmten Medien finden sich in den Tabellen `Medienarten`, `Medienformate`, `MedienKategorien`, `MedienSchlagworte`, `MedienStichworte `und `MedienZustaende ` wieder. Die Verbindung zu Lehrern, Schülern und Personen wird über die Tabelle `tblMedienAusleiher `definiert. Für die Vorgangsverwaltung stehen `tblMedienVorgaenge ` und `tblMedienVormerker ` zur Verfügung.

##	Inventar

Die Inventarisierung einer Schule wird in der Tabelle `tblInventar ` abgebildet. Detaildaten zum Inventar finden sich in der Tabelle `tblInventarExemplare ` wieder. Auch das Inventar ist mandantenfähig. 

Erwähnenswert ist auch der logische Zusammenhang zwischen Medien und Inventar: Wird die Medienverwaltung eingesetzt, so taucht jedes Medium automatisch auch in der Rolle eines Inventarstücks in Erscheinung.

##	Haushalt

Die Verwaltung des Schulhaushalts wird in den Tabellen Haushaltsjahre, `tblHaushaltstitel`, `tblHaushaltsstellen ` und `tblHaushaltsmittel ` abgebildet. Die registrierten Buchungen finden sich in der Tabelle `tblBuchungen ` wieder. 
