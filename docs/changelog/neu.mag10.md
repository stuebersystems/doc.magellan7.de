# Was ist neu?

[1]:/assets/images/neues/10.001.png "Abitur: Fachkategorie, Aufgabenbereich"
[2]:/assets/images/neues/10.002.png "Kurs und Lehrer"
[3]:/assets/images/neues/10.003.png "Bestanden, Leistungsart"
[4]:/assets/images/neues/10.004.png "Aktionsaufrufe in der Gruppe Fächer"
[5]:/assets/images/neues/10.005.png "Fach löschen nach Kursnummer"
[6]:/assets/images/neues/10.006.png "Lehrerserien-E-Mail"
[7]:/assets/images/neues/10.007.png "Endnote fortschreiben"
[8]:/assets/images/neues/10.008.png "Personen-Serien-E-Mail"
[9]:/assets/images/neues/10.009.png "Sorgeberechtigten-Serien-E-Mail"
[10]:/assets/images/neues/10.010.png "Beurteilungsart"

Die nachfolgenden Abschnitte richten sich an die Nutzer von Magellan 9. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen in Magellan 10 geben.

## FIREBIRD

### neue Version

Wir steigen für Magellan 10 auf die aktuelle Firebird-Version 4.0.2 um.
Die Passwortdatenbank von Firebird 2.5.9 (security2.fdb), die die verschlüsselten Passworte der Nutzer enthält, kann nicht für eine höhere Version (3.0 oder höher) aktualisiert werden.
Das bedeutet, dass die Benutzer der Magellan-Datenbank in der neuen Passwortdatenbank (security4.fdb) angelegt werden müssen. Dieses Anlegen ist durch eine neue Vergabe der Passworte möglich.
Hierfür gibt es eine neue Sammelaktion, die für einen Teil oder alle Nutzer neue Passworte generiert und in eine Liste ausgibt. Die Liste enthält Passwort, Kennung und wenn vorhanden, auch Mailadressen (aus Magellan > Lehrer > Daten1 > E-Mail oder für Benutzer, die nicht Lehrer der Schule sind im Administrator erfassbar), die ggfs. für den Versand an die Nutzer genutzt werden können.
Benutzer können Passworte nach der ersten Anmeldung wie gewohnt über die Magellan-Oberfläche auf ein eigenes Passwort abändern.

!!! warning "Wichtig!"

    Bitte berücksichtigen Sie, dass Firebird 4.0.2 und Firebird 2.5.9 können nicht (ohne weitere Anpassungen) parallel genutzt werden.

## Crystal Reports

Für Magellan 10 wird eine höhere Crystal Reports Runtime Version (13_0_33) verwendet.

## Magellan Administrator

### Passworte und E-Mailadresse

Für bereits angelegte Benutzer gibt es neu die Möglichkeit, gesammelt Passworte generieren zu lassen. Für welche Nutzer ein neues Passwort generiert werden soll, legen Sie über die Markierung in der Liste der Benutzer in der Benutzerverwaltung fest.
Um Ihnen die Möglichkeit zu geben diese Daten an die Benutzer zu übermittelt, werden erzeugten Passworte automatisch mit der Benutzerkennung und der E-Mailadresse in eine CSV-Datei gespielt. Diese Datei kann nur beim Ändern oder neu Erzeugen von Passworten erstellt werden, ein späterer Zugriff auf die verschlüsselten Passworte ist nicht möglich.

Als E-Mailadresse wird für Lehrer die E-Mailadresse aus `Magellan > Lehrer > Daten1 > E-Mail` verwendet. Passen Sie die Adresse in Magellan neu an, wird die Adresse auch für diese Funktionalität aktualisiert.
Für Benutzer, die nicht Lehrer der Schule sind, können Sie die zuverwendende Adresse je Benutzer direkt in der Benutzerverwaltung eingeben.
Über eine neue Spalte unter `Benutzerverwaltung > E-Mail` sehen Sie für alle angelegten Benutzer, ob eine Adresse und wenn ja, welche Adresse erfasst wurde.
Um die Emailadressen in bestehenden Datenbanken erstmalig in die Benutzerverwaltung zu übernehmen, steht Ihnen eine Sammelaktion zur Verfügung.

### Sorgeberechtigte ohne aktuelle Schüler inaktivieren

Beim Ausschulen von Schülern kann per Option gewählt werden, ob die verknüpften Sorgeberechtigten gleich auf den Status `inaktiv` gesetzt werden sollen. Magellan prüft, ob es aktive ebenfalls mit dem Sorgeberechtigten verknüpfte Schülerdatensätze (bspw. Geschwister) gibt und würde, wenn das nicht der Fall ist, den Status für den Sorgeberechtigten anpassen.
Sollte diese Aktion nicht konsequent genutzt worden sein, kann mit einer neuen Funktion eine Prüfung erfolgen, die schaut welcher Sorgeberechtigte im aktuellen Zeitraum Schülern zugeordnet ist oder nicht und den Status entsprechend auf `aktiv` oder `inaktiv` setzt. 
Von diesem Status ausgehend können Sie aus der Magellan Oberfläche im Menü `Sorgeberechtigte` die inaktiven Datensätze filtern und ggfs. auch Löschen.

### Oberfläche

Die Oberfläche wurde überarbeitet.

## Magellan Schulverwaltung

### Allgemein

#### Listendarstellung

Die Auswahllisten werden zeilenweise farblich unterschieden (grau, weiß).

![Bezeichnung](/assets/images/neues/011.png)

### Menü Schüler

#### Schüler fortschreiben

Beim Fortschreiben von Schülern ins Folgehalbjahr wird auch, wenn noch nicht vorhanden, ein neuer Klassenzeitraum für die Klassen angefügt. Für den neuen Klassenzeitraum wird beim Anlegen neu auch der Vorhalbjahreswert aus dem Feld `Klassenraum` übernommen.

#### Vagabunden und Seriendruck an Sorgeberechtigte

Der Seriendruck an die Sorgeberechtigten von Vagabunden ist möglich. Bitte markieren Sie im Menü `Schüler` für die Filterung `Vagabunden` die Datensätze, rufen den Seriendruck mit <kbd>Strg</kbd> + <kbd>S</kbd> auf und wählen `An die Sorgeberechtigten der markierten Schüler` aus. Bitte beachten Sie für eigene Vorlagen, dass folgende Seriendruck-Felder logisch nicht für Schreiben an Vagabunden genutzt werden können: Klasse_Kuerzel, Klasse_Langname1, Klasse_Langname2

#### Schüler/Bewerber in Mandanten versetzen

Für den Assistenten unter `Laufbahnprozesse > In Mandanten versetzen` kann für das Versetzen als Vagabund oder Bewerber jeweils eine Herkunftsschule mit zugewiesen werden. Sie können den Start-Mandanten unter `Schulen` erfassen und auch ggfs. als Favorit (Rechtsklick in der Schulenliste > Zu Favoriten hinzufügen) markieren, damit dieser Datensatz in der Auswahl nach oben sortiert wird.

#### Lehrer und Kurs auf der Leistungskarte

Unter `Schüler > Zeugnis > Leistungen` gibt als als Sortierkriterium die Spalten `Lehrer` und `Kurs`, Inhalte in diesen Spalten können Sie wie gewohnt auf der Unterkarte `Fächer` editieren.

[![Kurs und Lehrer][2]][2]

#### Aktionsaufrufe ins Menü verschoben

Die Aktionsaufrufe, die unter `Schüler > Zeugnis > Fächer` angeordnet waren und aber für mehrere Schüler genutzt werden können, wurden zum Aufruf in die Menüleiste unter `Schüler` in die neue Gruppe `Fächer` verschoben.

[![Aktionsaufrufe in der Gruppe Fächer][4]][4]

#### Fach zuweisen

Für das Zuweisen von Fächern (`Schüler > Zeugnis> Fächer`) gibt es zusätzlich zu den vorzubereitenden Fachtafeln einen weiteren Ansatz. Sie markieren einen oder mehrere Schüler und weisen diesen ein Fach zu, dass mit den folgenden Eigenschaften versehen werden kann:

* Unterrichtsart
* Fachstatus
* Kursnummer
* Lehrer
* Schwerpunkt
* Niveau
* Position
* Faktor
* Merkmal
* Sprachen

#### Endnote fortschreiben

Bei den `Optionen zum Verändern bestehender Fachdaten` im Assistenten `Fachtafel zuweisen` ist es zusätzlich möglich nachträglich das Häkchen für `Endnote fortschreiben` je Fachzeile zu setzen.

[![Endnote fortschreiben][7]][7]

#### Fach löschen

Für den Assistenten zum `Fach löschen` gibt es das neue Filterkriterium `Kursnummer`.

[![Fach löschen nach Kursnummer][5]][5]

#### Leistungsart und Bestanden in der Notenübersicht

In der Notenübersicht gibt es die neue Spalten `Leistungsart` und `Bestanden`.

[![Bestanden, Leistungsart][3]][3]

### Menü Bewerber

#### Daten 2

Unter `Bewerber > Daten 2 > Überweisung` kann der Eintrag für  `Einschulantrag/Ausnahme` gesetzt werden.

#### Bewerber > Bewerberstatus

In der Liste der Bewerberstatus gibt es den neuen Wert `Einladung`. Der Wert kann dort manuell erfasst werden oder über den Assistenten `Bewerberverfahren` gesammelt zugewiesen werden.

### Menü Lehrer

#### Lehrer-Serien-E-Mail

Aus dem Menü `Lehrer` heraus können Sie eine Gruppe von Lehrern markieren und per <kbd>Strg</kbd> + <kbd>M</kbd> eine Serienmailfunktion für Lehrer aufrufen. Die Funktion filtert für die markierten Lehrer die Mailadresse aus und übergibt sie an den Standardmailclient Ihres Rechners. Es wird im Standardmailclient einen leere Mail geöffnet, die Mailadressen werden je nach Auswahl im Assistenten in die Zeilen An, CC oder BCC übergeben.

[![Lehrerserien-E-Mail][6]][6]

### Menü Personen

#### Personen-Serien-E-Mail

Aus dem Menü `Personen` heraus können Sie eine Gruppe von Personen markieren und per <kbd>Strg</kbd> + <kbd>M</kbd> eine Serienmailfunktion für Personen aufrufen. Die Funktion filtert für die markierten Personen die Mailadresse aus und übergibt sie an den Standardmailclient Ihres Rechners. Es wird im Standardmailclient einen leere Mail geöffnet, die Mailadressen werden je nach Auswahl im Assistenten in die Zeilen An, CC oder BCC übergeben.

[![Personen-Serien-E-Mail][8]][8]

### Menü Sorgeberechtigte

#### Sorgeberechtigten-Serien-E-Mail

Aus dem Menü `Sorgeberechtigte` heraus können Sie eine Gruppe von Sorgeberechtigten markieren und per <kbd>Strg</kbd> + <kbd>M</kbd> eine Serienmailfunktion für Sorgeberechtigte aufrufen. Die Funktion filtert für die markierten Sorgeberechtigten die Mailadresse aus und übergibt sie an den Standardmailclient Ihres Rechners. Es wird im Standardmailclient einen leere Mail geöffnet, die Mailadressen werden je nach Auswahl im Assistenten in die Zeilen An, CC oder BCC übergeben.

[![Sorgeberechtigten-Serien-E-Mail][9]][9]

### Menü Abitur

#### Fachkategorie und Aufgabenbereich

Auf der Karte `Qualifikation` können über `Layout anpassen` die Spalten `Fachkategorie` und `Aufgabenbereich` aus den Einträgen unter `Extras > Schlüsselverzeichnisse > Fächer` eingeblendet werden. Damit erhalten Sie eine schnelle Übersicht um zu überprüfen, ob Ihren Fächern die korrekten Werte zugewiesen wurden. Die korrekten Eingaben werden je Berechnungsskript in den [Landesanpassungen](https://doc.la.stueber.de/skriptueberblick/) dokumentiert.

[![Abitur: Fachkategorie, Aufgabenbereich][1]][1]

## MyMagellan

### `Bestanden` und `Leistungsart`

Die Felder `Bestanden` und `Leistungsart` aus `Schüler > Zeugnis > Leistungen` können mit in eine MyMagellan-Datei übertragen, dort befüllt und wieder in die Schulverwaltung übertragen werden.

### Beurteilungsart

Die Auswahl der Filterung der Fachzeilen nach der `Beurteilungsart` unter `Fächer anzeigen` ist geändert worden. Die Optionen sind nebeneinander als Schaltflächen angeordnet. Beim Ansichtswechsel innerhalb des Programms bleibt Ihre Auswahl gespeichert, beim Neustart des Programms wird die Standardauswahl auf `Alle (nicht editierbar)` zurückgesetzt.

[![Beurteilungsart][10]][10]