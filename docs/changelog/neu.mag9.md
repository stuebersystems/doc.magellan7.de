# Was ist neu?

[1]:/assets/images/neues/901.png
[2]:/assets/images/neues/902.png
[3]:/assets/images/neues/903.png
[4]:/assets/images/neues/904.png

Die nachfolgenden Abschnitte richten sich an die Nutzer von MAGELLAN 8. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen geben.

## Datenstrukturänderungen

Die Neuerungen in der Datenstruktur finden Sie als Zusammenfassung hier:[https://doc.magellan-toolbox.stueber.de/datenstruktur/version9/neuerungen/](https://doc.magellan-toolbox.stueber.de/datenstruktur/version9/neuerungen/).

## MAGELLAN Schulverwaltung

### pausierende Schüler in der Statusleiste

Unter `Schüler > Auswahl` werden in der Statusleiste die pausierenden Schüler berücksichtigt.

[![Summen in der Statusleiste][2]][2]

### Schüler > Daten1 > Familie

Im Anzeigefeld unter `Schüler > Daten1 > Familie` wurden die Felder `Seriendruckname1` und `Seriendruckname2` ausgeblendet, damit sind bei mehreren Familienmitgliedern auf einen Blick mehr Informationen erfassbar.

[![Liste der Familienmitglieder][3]][3]

### Schüler > Zeugnis > Details

Das Feld `Anrechendatum` wurde in die Sammelzuweisung übernommen.

[![Sammelzuweisung unter Schüler > Zeugnis > Details][4]][4]

### Sorgeberechtigte > Geschlecht

Für Sorgeberechtigte wurde das Feld `Geschlecht` ergänzt. Bei der Anpassung Ihrer Datenbank an die Datenbankstruktur der Version 9 wurde für Sorgeberechtigte, deren Feld `Anrede` befüllt war automatisch das Feld `Geschlecht` vorbefüllt.

### Seriendruck an Betriebe

Für den Seriendruck aus dem Menü `Betriebe` wurde das Feld `«Betrieb_Email»` ergänzt.

### Abitursimulation

Um die Datensicherheit zu gewährleisten und Versehen vorzubeugen wurde unter `Abitur > Qualifikation > Abitur > Simulation` die abschließende Nachfrage, ob die Änderungen aus der Simulation übernommen werden soll unterdrückt. Eintragungen aus der Simulation werden nicht auf die Karten `Qualifikation` oder `Prüfung` übernommen.

### Klassen 

Unter `Klassen > Daten` wurde das Feld `nächste Klasse` ausgeblendet.

### Schnittstellen

#### SAXSVS

* Eine neue Prüfung wurde für die Ausgabe der Statistikfelder `<av_abs_schart>` und `<av_bbs_schart>` integriert. Sind die zugehörigen Felder nicht gefüllt, wird eine Warnung ausgegeben.
* `<sorgeberechtigter><as_beziehung>`: Wenn für den Schülern die Verhältnisse `Eltern`, `Erziehungsberechtigte(r)` oder `Sorgeberechtigte(r)` zugewiesen wurden und den Sorgeberechtigten das Geschlecht (weiblich/männlich) zugeordnet wurden, wird das Verhältnis als Mutter (20) oder Vater (10) ausgespielt. Bitte beachten Sie die geänderte Anleitung unter [https://doc.ls.stueber.de/sachsen/export_saxsvs/#sorgeberechtigte](https://doc.ls.stueber.de/sachsen/export_saxsvs/#sorgeberechtigte).

## MAGELLAN Administrator

### Mandant vorbelegt

Unter `Datenaustausch > Daten über das Magellan-Importformat importieren` ist im Assistenten der Mandant vorbelegt.

[![Mandant ist vorbelegt][1]][1]

### Haushalt&Inventar und Klassenbuch ausgeblendet

Unter `Benutzerverwaltung > Doppelklick auf einen Benutzer > Rechte` wurden die Aufrufe für Haushalt&Inventar und Klassenbuch ausgeblendet.






