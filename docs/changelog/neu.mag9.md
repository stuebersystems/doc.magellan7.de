# Was ist neu?

[1]:/assets/images/neues/901.png
[2]:/assets/images/neues/902.png
[3]:/assets/images/neues/903.png
[4]:/assets/images/neues/904.png
[5]:/assets/images/neues/905.png
[6]:/assets/images/neues/906.png
[7]:/assets/images/neues/907.png
[8]:/assets/images/neues/908.png
[9]:/assets/images/neues/909.png

**Das Kapitel wird aktuell bearbeitet.**

Die nachfolgenden Abschnitte richten sich an die Nutzer von MAGELLAN 8. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen in MAGELLAN 9 geben.

## Datenstrukturänderungen

Die Neuerungen in der Datenstruktur finden Sie als Zusammenfassung hier:[https://doc.magellan-toolbox.stueber.de/datenstruktur/version9/neuerungen/](https://doc.magellan-toolbox.stueber.de/datenstruktur/version9/neuerungen/).

## MAGELLAN Schulverwaltung

### pausierende Schüler in der Statusleiste

Unter `Schüler > Auswahl` werden in der Statusleiste die pausierenden Schüler berücksichtigt.

[![Summen in der Statusleiste][2]][2]

### Assistenten und Klassenspalte

In sämtlichen Assistenten, in denen die Spalte `Klasse` gezeigt wird, ist die Standardposition der Klasse  geändert worden. Die Spalte `Klasse` wird im vorderen Bereich gezeigt, so dass sie genutzt werden kann ohne nach rechts zu scrollen.

### Schüler > Daten1 > Familie

Im Anzeigefeld unter `Schüler > Daten1 > Familie` wurden die Felder `Seriendruckname1` und `Seriendruckname2` ausgeblendet, damit sind bei mehreren Familienmitgliedern auf einen Blick mehr Informationen erfassbar.

[![Liste der Familienmitglieder][3]][3]

### Schüler > Zeugnis > Fächer

#### Klassenfilter

Im Assistenten zum `Fachtafel zuweisen` kann die Klasse auch mit dem Operator `wie` gefiltert werden.

[![Operator "wie" für Klassenfilterung ergänzt][5]][5]

#### Fachtafeln zuweisen

Der Assistent zum Zuweisen von Fachtafeln wurde vollständig überarbeitet. Bisher konnten bestehende Fächer durch Fächer aus der Fachtafel ersetzt werden oder sie konnten zusätzlich angelegt werden. 
Vor dem Ersetzen der Fächer findet jetzt eine Prüfung statt. Ein bestehendes Fach wird nur gelöscht, wenn dem Fach unter `Schüler > Zeugnis > Leistungen` keine Note zugewiesen wurde. Geprüft werden sämtliche Notenfelder. Wurde dem Fach eine Note zugewiesen, wird diese Fach übersprungen und nicht neu angelegt. Zusätzlich gibt es weitere Optionen, die das mehrfach Zuweisen eines Fachs gestatten oder auch das Löschen von Fächern mit Note erzwingen können.

Für bereits zugewiesene Schülerfächer können zusätzlich zu `Position`, `Faktor`, `Merkmal` und `Lehrer` noch `Unterrichtsart` und `Fachstatus` ergänzt werden.
Die überarbeitete Anleitung hierfür finden Sie unter [https://doc.magellan.stueber.de/schulverwaltung/howto/zeugnisdaten/#fachtafeln-zuweisen-ab-magellan-9](https://doc.magellan.stueber.de/schulverwaltung/howto/zeugnisdaten/#fachtafeln-zuweisen-ab-magellan-9).

[![Neuer Funktionalitäten beim Zuweisen von Fachtafeln][7]][7]

### Schüler > Zeugnis > Details

Das Feld `Anrechendatum` wurde in die Sammelzuweisung übernommen.

[![Sammelzuweisung unter Schüler > Zeugnis > Details][4]][4]

### Bescheinigung zur Rentenversicherung (V0510 - 26.06.2017).rpt

Der Bericht berechnet die Schulbesuchzeiten nach dem 17. Geburtstag anhand des Geburtsdatums des Schülers unter `Schüler > Daten1 > Geburtsdatum` und dem Zugang zur Schule unter `Daten2 > Zugang am`.

### Sorgeberechtigte > Geschlecht

Für Sorgeberechtigte wurde das Feld `Geschlecht` ergänzt. Bei der Anpassung Ihrer Datenbank an die Datenbankstruktur der Version 9 wurde für Sorgeberechtigte, deren Feld `Anrede` befüllt war automatisch das Feld `Geschlecht` vorbefüllt.

### Seriendruck an Betriebe

Für den Seriendruck aus dem Menü `Betriebe` wurde das Feld `«Betrieb_Email»` ergänzt.

### Abitursimulation

Um die Datensicherheit zu gewährleisten und Versehen vorzubeugen wurde unter `Abitur > Qualifikation > Abitur > Simulation` die abschließende Nachfrage, ob die Änderungen aus der Simulation übernommen werden soll unterdrückt. Eintragungen aus der Simulation werden nicht auf die Karten `Qualifikation` oder `Prüfung` übernommen.

### Klassen 

Unter `Klassen > Daten` wurde das Feld `nächste Klasse` ausgeblendet.

### Mandanten

Ein neuer Prüfbericht steht zur Verfügung: `Mandant (ohne Gemeindekennziffer(Sorgeberechtigte, Lehrer, Personen)).rpt`.

### Gruppen

Ein neuer Bericht für die Ausgabe der Mitglieder je Gruppe steht zur Verfügung: `"Mitglieder (Kontaktliste).rpt"`.

### Enbrea-Leistungen

Für die Ansicht unter `Klassen > Zeiträume > Enbrea-Leistungen > Leistungsprofile definieren...` wurde die Spalte `Position` ergänzt. Sie können durch das Erfassen der Positionsnummer an dieser Stelle, den Wert bei der Übernahme der Daten zum einzelnen Schüler mit übergeben.

### Schnittstellen

#### Allgemein

Das Benachrichtigungssystem für den Export ist komplett überarbeitet. Es gibt zwei neue Spalten in den Hinweisen:

* "Klasse" - Enthält Klasseninformationen, sprich den Kürzel der Klasse
* "Person" - Enthält Personeninformationen, üblicherweise Vor-Nachname und ID

[![Neue Spalten in den Meldungen][6]][6]

#### SAXSVS

* Alle Schülermeldungen wurden um die Ausgabe der Klasse erweitert.
* Eine neue Prüfung wurde für die Ausgabe der Statistikfelder `<av_abs_schart>` und `<av_bbs_schart>` integriert. Sind die zugehörigen Felder nicht gefüllt, wird eine Warnung ausgegeben.
* `<sorgeberechtigter><as_beziehung>`: Wenn für den Schülern die Verhältnisse `Eltern`, `Erziehungsberechtigte(r)` oder `Sorgeberechtigte(r)` zugewiesen wurden und den Sorgeberechtigten das Geschlecht (weiblich/männlich) zugeordnet wurden, wird das Verhältnis als Mutter (20) oder Vater (10) ausgespielt. Bitte beachten Sie die geänderte Anleitung unter [https://doc.ls.stueber.de/sachsen/export_saxsvs/#sorgeberechtigte](https://doc.ls.stueber.de/sachsen/export_saxsvs/#sorgeberechtigte).

## MyMAGELLAN

### Übersicht "Kontrolle nach Klassen"

In MyMagellan gibt es die  neue schreibgeschützte Übersicht `Kontrolle nach Klassen`, die Ihnen Ihre erfassten Daten zur Kontrolle je Klasse darstellt. Diese Ansicht kann auch nach Excel exportiert werden.

## MAGELLAN Administrator

### Organisiertes Löschen

Der neue Assistent im MAGELLAN Administrator unterstützt Sie beim Löschen von wahlweise:

*  Schülerdatensätzen
*  Fachdaten von Schülern
*  Passbildern von Schülern

Sie geben als Zeitpunkt dafür eine Monatsanzahl ein, die ausgehend vom aktuellen Tagesdatum die Löschungen für Schüler durchführt, die zu diesem Zeitpunkt nicht mehr Schüler Ihrer Schule waren.  

Die Anleitung hierfür finden Sie unter: [https://doc.magellan.stueber.de/schulverwaltung/admin/datenbankpflege8/#organisisertes-loschen](https://doc.magellan.stueber.de/schulverwaltung/admin/datenbankpflege8/#organisisertes-loschen).

[![Aufruf][8]][8]

[![Assistent][9]][9]

### Mandant vorbelegt

Unter `Datenaustausch > Daten über das Magellan-Importformat importieren` ist im Assistenten der Mandant vorbelegt.

[![Mandant ist vorbelegt][1]][1]

### Haushalt&Inventar und Klassenbuch ausgeblendet

Unter `Benutzerverwaltung > Doppelklick auf einen Benutzer > Rechte` wurden die Aufrufe für Haushalt&Inventar und Klassenbuch ausgeblendet.
