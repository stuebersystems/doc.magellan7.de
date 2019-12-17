# Verteilen von Daten

## Voraussetzungen

Voraussetzungen für die Nutzung des MyMAGELLAN CENTERs sind:

Nr.|Voraussetzung
--|--
1. | Definition der MyMAGELLAN-Teilnehmer in der Benutzerverwaltung des MAGELLAN-Administrators
2. | Eingabe der Fachdaten der Schüler
3. | Zuordnung der MyMAGELLAN-Teilnehmer zu den Schülern in MAGELLAN als Fachlehrer, Klassenlehrer und/oder Tutor

### Wer darf die Einstellungen vornehmen

Die Karte MyMAGELLAN CENTER kann vom `sysdba` oder von einem Nutzer mit dem Sonderrecht `Mandantenadministrator` bedient werden.

Der Mandantenadministrator darf Folgendes für:

- Einstellen, wer MyMAGELLAN Teilnehmer sein darf oder nicht (auch per Sammelaktion)
- Passworte vergeben, die für das Öffnen der MyMAGELLAN Dateien verwendet werden (auch per Sammelaktion)
- Den Pfad editieren unter dem die mym-Datei abgelegt werden soll (auch per Sammelaktion)
- Daten verteilen
- Dateien löschen
- Daten einsammeln

Der Mandantenadministrator darf keine neue Nutzer anlegen, Rechte für die Schulverwaltung gewähren oder ändern.

### Einstellungen im MAGELLAN ADMINISTRATOR

Jeder MyMAGELLAN-Teilnehmer muss als Benutzer in der Benutzerverwaltung (MAGELLAN ADMINISTRATOR > Benutzerverwaltung) angelegt sein. Dabei muss er folgende Bedingungen erfüllen:

### 1. Recht zuweisen

Der Benutzer muss unter „Schulverwaltung“ der Benutzergruppe „Schulleitung 1“, „Schulleitung 2“, „Sekretariat 1“, „Kollegium 1“, „Kollegium 2“, „Kollegium 3“ oder „Kollegium 4“ zugeordnet sein.

![Weisen Sie dem Benutzer ein Recht zu](/assets/images/mymagellan/02.png)

### 2. Teilnehmer von MyMAGELLAN

Der Benutzer muss unter „MyMAGELLAN“ den Status „Teilnehmer von MyMAGELLAN“ besitzen. Anderenfalls wird der Benutzer nicht auf der Karte `MyMAGELLAN CENTER` angezeigt.

![Teilnehmer von MyMAGELLAN](/assets/images/mymagellan/03.png)

### 3. Speicherort für die Datei vorbelegen

Dem Benutzer muss unter „MyMAGELLAN“ eine „MyMAGELLAN-Datei“ (Datei mit der Endung .mym7) zugeordnet werden. Die Datei muss lediglich benannt werden, jedoch nicht schon existieren. Es geht hier darum die Stelle für die spätere Sammelerstellung der Lehrerdateien vorzubelegen.
Bitte achten Sie darauf, dass Sie den kompletten Pfad eintragen. Wenn Sie lediglich eine Dateibezeichnung eintragen, führt dies später zu einer Fehlermeldung, da der Speicherort nicht gefunden wird. Nur Benutzer mit diesen Rechten werden im MyMAGELLAN CENTER angezeigt.

![Speicherort vorbelegen](/assets/images/mymagellan/04.png)

!!! info "Hinweis"

	Unter MyMAGELLAN 6 war die Dateiendung "mym", jetzt ist sie "mym7". Sie müssen aber an der Stelle nichts ändern, beim Erstellen wird die korrekte Dateiendung ergänzt.

### Dateipasswort

Die Datei kann mit einem Passwort belegt werden, das beim Öffnen der Datei eingegeben werden muss. Hierfür gibt es vier Möglichkeiten.

1. Sie aktivieren den Haken auf der Unterkarte `Rechte`, damit wird das MAGELLAN-Passwort des Benutzers auch als Passwort für die MyMAGELLAN-Datei verwendet. 

![MAGELLAN Passwort als MyMAGELLAN-Passwort](/assets/images/mymagellan/05.png)

2. Sie vergeben ein gesondertes Passwort für die MyMAGELLAN-Datei auf der Unterkarte `MyMAGELLAN`.

![gesondertes MyMAGELLAN-Passwort](/assets/images/mymagellan/06.png)

3. Sie vergeben ein Passwort für mehrere Dateien, [diese Möglichkeit wird später beim Erstellen der Dateien angeboten](https://doc.magellan7.stueber.de/schulverwaltung/admin/myMAGELLAN-center/#karte-sicherheit-festlegen).
4. Sie verwenden den nachstehend beschriebenen Export und Import von Benutzereinstellungen um somit mehren Benutzern gleichzeitig ein Dateipasswort zuzuweisen.

### Benutzereinstellungen exportieren und importieren

Für bereits angelegte Benutzer können die Passworte für die MyMAGELLAN-Datei und den Ablagepfad gesammelt zugewiesen werden.

#### Export

Starten Sie den Assistenten unter `MAGELLAN ADMINISTRATOR > MYMAGELLAN CENTER > Benutzer exportieren` und geben eine Pfad und einen Dateinamen ein.

![Benutzerdaten exportieren](/assets/images/mymagellan/24.png)

Die entstandene CSV-Datei können Sie beispielsweise mit Excel öffnen.

![Export in Excel öffnen](/assets/images/mymagellan/25.png)

!!! info "Hinweis"

	Ändern Sie bitte nicht den Aufbau der Datei, passen Sie nur die Werte an, die Kennung kann nicht angepasst werden.

Spaltenkopf| Mögliche Werte
--|--
**Kennung**| Keine Änderung möglich
**Passwort**|Tragen Sie hier im Klartext das Passwort ein, es wird chiffriert in der MAGELLAM-Datenbank gespeichert. <br/>Ein bereits erfasstes Passwort wird nicht in die Datei ausgespielt.<br/> Ein leeres Feld wird beim Import kein bestehendes Passwort ändern.
**MyMagellan-Teilnehmer**| Mögliche Werte sind  `Teilnehmer` oder `(Kein Teilnehmer)`. <br/>Das Feld darf nicht leer sein.
**MyMagellan-Datei**| Tragen Sie hier bitte einen existierenden Pfad und den zukünftigen Dateinamen plus Dateiendung ein. <br/>Beispiel: `C:\Users\Public\Documents\Stueber Systems\Magellan 7\MyMag-Exporte\SNAPE.mym7`

#### Import

Speichern Sie Ihre angepasste Datei und rufen Sie den Import über die Schaltfläche unter `MAGELLAN ADMINISTRATOR > MYMAGELLAN CENTER > Benutzer exportieren` auf.

![Benutzereinstellungen importieren](/assets/images/mymagellan/26.png)

### Einstellungen in MAGELLAN

Grundsätzlich gilt: Alle Schüler, deren Noten über MyMAGELLAN erfasst werden sollen, müssen in MAGELLAN erfasst sein. Hierzu zählt neben der eigentlichen Definition des Schülers auch dessen Zuordnung zu einer Klasse. Zusätzlich müssen den Schülern Fächer zugeordnet werden, deren Noten mit MyMAGELLAN erfasst werden sollen, da eine Eingabe der Fächer in MyMAGELLAN nicht möglich ist.

### Verzeichniswerte

Beim Erstellen der MyMAGELLAN-Dateien werden auch Inhalte aus den Schlüsselverzeichnissen übergeben. Stellen Sie vorab sicher, dass in den Verzeichnissen die notwendigen Daten vorhanden sind, die die Kollegen später bei der Eingabe verwenden sollen.

!!! info "Hinweis"

	In die MyMAGELLAN-Dateien werden ausschließlich aktuelle Verzeichniswerte (Noten, Fachstatus, Unterrichtsarten, Abschlüsse usw.) übergeben. Das bedeutet Verzeichniswerte,  deren `Bis-Datum` im MAGELLAN-Verzeichnis (`MAGELLAN > Extras > Schlüsselverzeichnisse`) leer ist oder ein Datum enthält, dass vom Tag der Erstellung aus gesehen in der Zukunft liegt.

### Zuordnung der MyMAGELLAN-Teilnehmer zu den Schülern

Die Zuordnung der MyMAGELLAN-Teilnehmer zu den Schülern erfolgt über die Aufgaben der Teilnehmer in der Schule:

Rolle|Bedeutung
--|--
**Klassenleiter 1** |Der Lehrer ist in mindestens einer Klasse Klassenleiter 1 im aktuellen Zeitraum. In diesem Fall werden alle Schüler mit allen Fachzeilen in die MyMAGELLAN-Datei exportiert. Der Klassenleiter kann auch Zeugnisbemerkungen editieren.
**Fachlehrer** |Der Lehrer ist bei mindestens einem Schüler in einer Fachzeile als Fachlehrer hinterlegt. Für die Rolle als Fachlehrer werden die unterrichteten Fachzeilen der Schüler in seine Datei übertragen, beispielsweise nur die Biofachzeilen der in diesem Fach unterrichteten Schüler.
**Tutor** | Der Lehrer ist bei mindestens einem Schüler als Tutor zugeordnet. Dies ist beispielsweise in der gymnasialen Oberstufe der Fall, wenn der Tutor den Stammkursleiter darstellt. Die Datenmenge, die für den Tutor übertragen wird ist identisch mit der des Klassenleiters: also alle Fachzeilen der Schüler und auch Zeugnisbemerkungen, aber eben nicht für die Schüler einer ganzen Klasse, sondern für alle Schüler, denen er als Tutor zugewiesen wurde.

Zuordnung Klassenleiter unter `Klasse > Zeiträume > Zeitraum > Feld Klassenleiter1`: 
![Zuordnung des Klassenleiters 1 bei einer Klasse auf der Registerkarte „Zeiträume“. Die Zuordnung erfolgt pro Zeitraum.](/assets/images/mymagellan/07.png)

Zuordnung Fachlehrer unter `Schüler > Zeugnis > Fächer > Spalte Lehrer`. 

Die Zuordnung kann auch per Fachtafel verteilt werden oder durch den Abgleich mit DAVINCI als Resulat der Stundenplanung übernommen werden.

![Zuordnung der Fachlehrer bei einem Schüler in der Spalte „Lehrer“ bei den Fächern.](/assets/images/mymagellan/08.png)

Zuordnung des Tutors unter `Schüler > Zeugnis > Details > Feld Tutor`. Dieses Feld kann auch per Sammelzuweisung, Aufruf dazu am oberen Ende der Karte, durchgeführt werden.

![Zuordnung des Tutors auf der Registerkarte „Zeugnis > Details“ des Schülers.](/assets/images/mymagellan/09.png)

Ist ein MyMAGELLAN-Teilnehmer im aktuellen Zeitraum weder Klassenleiter 1, noch Fachlehrer, noch Tutor, wird für ihn keine MyMAGELLAN-Datei durch das MyMAGELLAN CENTER erzeugt.

## MyMAGELLAN-Dateien verteilen

Sind alle Voraussetzungen für die Erstellung der MyMAGELLAN-Dateien erfüllt, werden nach dem Aufruf der Karte `MyMAGELLAN CENTER` alle MyMAGELLAN-Teilnehmer aufgelistet.

!!! info "Hinweis"

	Vor dem eigentlichen Verteilen der MyMAGELLAN-Dateien, sollten Sie nochmals überprüfen, ob für jeden Teilnehmer der Speicherort und der Dateiname für seine MyMAGELLAN-Datei vordefiniert wurde. Wenn dies noch nicht über die Benutzerverwaltung des MAGELLAN ADMINISTRATORs erfolgt ist, können Sie diese Vorgaben auch im MyMAGELLAN CENTER definieren.

![Sind alle Speicherorte vorbelegt?](/assets/images/mymagellan/10.png)

So starten Sie die Verteilung der MyMAGELLAN-Dateien:

1. Markieren Sie die Teilnehmer, deren MyMAGELLAN-Dateien Sie verteilen wollen.

2. Klicken Sie auf die Schaltfläche `Verteilen` im Menüband.

![Dateien verteilen](/assets/images/mymagellan/11.png)

### Karte "Zeitraum auswählen"

3. Wählen Sie das Halbjahr für das die Noten eingegeben werden soll und Ihren Mandanten aus!

![Wählen Sie das Halbjahr und den Mandanten aus!](/assets/images/mymagellan/12.png)

### Karte "Klassen auswählen"

4. Wählen Sie aus, ob für alle Klassen die Noten erfasst werden sollen oder nur für einen Teil. Die Standardauswahl ist für alle Schüler aller Klassen.

![Wählen Sie ggfs. die Klassen aus!](/assets/images/mymagellan/13.png)

### Karte "Teilnehmer auswählen"

5. Wählen Sie aus, aus für welche Rolle oder Rollen Schüler und deren Fachdaten exportiert werden sollen. Bitte beachten Sie hierzu die Abschnitte:

* [Zuordnung der MyMAGELLAN-Teilnehmer zu den Schülern](https://doc.magellan7.stueber.de/schulverwaltung/admin/myMAGELLAN-center/#zuordnung-der-myMAGELLAN-teilnehmer-zu-den-sch%C3%BClern)
* [Organisation des zeitlichen Ablaufs](https://doc.magellan7.stueber.de/schulverwaltung/admin/myMAGELLAN-center/#organisation-des-zeitlichen-ablaufs)
* [Mögliche Konflikte](https://doc.magellan7.stueber.de/schulverwaltung/admin/myMAGELLAN-center/#m%C3%B6gliche-konflikte)

![Für welche Rollen soll exportiert werden?](/assets/images/mymagellan/14.png)

### Karte "Layout und Rechte auswählen"

1. Wählen Sie auf dieser Karte die Spalten für den Export aus und legen Sie fest, welche Einträge editiert werden können. Es werden sämtliche in MyMAGELLAN verfügbaren Felder/Spalten gezeigt.

Feld|Funktion
--|--
**Spalte** | Name der Spalte oder des Feldes in der MAGELLAN-Oberfläche.
**Spaltenüberschrift** |Wählen Sie eine abweichende Bezeichnung für die Anzeige in MyMAGELLAN.<br/><br/> ![](/assets/images/mymagellan/16.png)
**Sichtbar** |Setzen Sie das Häkchen um das Feld in MyMAGELLAN anzuzeigen.
**Editierbar** |Setzen Sie das Häkchen zusammen mit dem Häkchen in der Spalte `Sichtbar`, um eine Eingabe zuzulassen. Bei einigen Spalten bietet es sich an, keinen Eintrag zuzulassen, die Spalte aber dennoch zur besseren Sortierbarkeit in der Datei auszugeben, zum Beispiel für die Unterrichtart oder den Fachstatus.
**Listenspalte** |Diese Option ist fest vorgegeben und soll Ihnen zeigen, welche Einträge später als Liste zur Verfügung stehen (Beispiel Endnote1) und welche als Eingabefelder(Beispiel Versetzungsart oder Abschlussart).

![Layout und Rechte festlegen](/assets/images/mymagellan/15.png)

!!! info "Hinweis"

	Wenn Sie mehrere Zeilen markieren, können Sie per Rechtsklick diese in einer Aktion auf `sichtbar/unsichtbar` oder auf `editierbar/nicht` editierbar setzen.

![Zeilen markieren und per Rechtsklick Werte für mehrere Zeilen zuweisen.](/assets/images/mymagellan/17.png)

Am unteren Rand der Karte `Layout und Rechte festlegen` stellen Sie bitte ein, wie beim späteren Einsammeln der Daten mit den Fehlzeiten verfahren werden soll.

![Einsammeloptionen für Fehlzeiten](/assets/images/mymagellan/18.png)

Option|Bedeutung
--|--
Fehlstunden/-tage in MAGELLAN beim Einsammeln überschrieben|Die Werte der Felder „Fehlstunden“, „Fehlstunden unentschuldigt“, „Fehltage“ und „Fehltage unentschuldigt“ des Schülers in MAGELLAN werden durch Einlesen einer MyMAGELLAN-Datei, mit Daten zu diesem Schüler überschrieben. Ausnahme: Kein Eintrag oder ein Null in MyMAGELLAN überschreiben keinen Wert in MAGELLAN. Eine Korrektur des verkehrten Wertes aus MAGELLAN ist nur im Schulverwaltungsprogramm selbst möglich.
Fehlstunden/-tage in MAGELLAN beim Einsammeln addieren|Die Werte der Felder „Fehlstunden“, „Fehlstunden unentschuldigt“, „Fehltage“ und „Fehltage unentschuldigt“ des Schülers in MAGELLAN werden durch Einlesen einer MyMAGELLAN-Datei, mit Daten zu diesem Schüler addiert. Bitte beachten Sie, dass bei dieser Option im Fall eines erneuten Importes der Datei auch die Fehlzeiten erneut addiert werden.<br/><br/>**Wichtig:**<br/>Bitte beachten Sie den Abschnitt [Fehlzeiten](https://doc.magellan7.stueber.de/schulverwaltung/admin/myMAGELLAN-center/#fehlzeiten) und bedenken bitte auch, dass Sie Dateien in denen das Addieren der Fehlzeiten gewählt wurde, nicht mehrfach importieren dürfen.
Fehlstunden/-tage in MAGELLAN beim Einsammeln nicht aktualisieren| Die Werte der Felder „Fehlstunden“, „Fehlstunden unentschuldigt“, „Fehltage“ und „Fehltage unentschuldigt“ des Schülers in MAGELLAN werden durch Einlesen einer MyMAGELLAN-Datei nicht verändert.

!!! info "Hinweis"

	 Bitte beachten Sie, dass für den Benutzer der MyMAGELLAN-Datei ausgeblendete Felder weiterhin mit Werten versehen sind. Diese Werte werden beim Zurückspielen der MyMAGELLAN-Dateien in die Quelldatenbank übernommen. Zwischenzeitliche Änderungen in der Quelldatenbank werden dabei überschrieben.
Und: Zeugnisbemerkungen werden nur von Klassenleitern und Tutoren nach MAGELLAN übernommen.

### Karte "Sicherheit festlegen"

Sie haben die Möglichkeit ein teilnehmer-individuelles Passwort in der Benutzerverwaltung im MAGELLAN Administrator zu vergeben, die Schritte dafür beschreiben wir im Abschnitt [Dateipasswort](https://doc.magellan7.stueber.de/schulverwaltung/admin/myMAGELLAN-center/#dateipasswort). Alternativ können Sie ein Passwort für mehrere Dateien vergeben, wenn kein Passwort im Administrator angelegt wurde. Tragen Sie für diese Situation hier ein Kennwort ein und wiederholen es.

Im Feld `Bemerkung`, dass dem Nutzer der Datei später in der Startansicht gezeigt wird, können Sie beispielsweise einen Hinweis für die Rückgabe hinterlegen.

![Passwort und Bemerkung erfassen](/assets/images/mymagellan/19.png)

Wechseln Sie auf `Weiter` und `Fertigstellen`!

### Karte "MyMAGELLAN-Daten verteilen"

Der Assistent erstellt die Dateien, füllt sie individuell mit den in MAGELLAN erfassten Daten und legt sie am gewählten Speicherort ab.
Sollte es einen Grund geben, warum keine Datei erzeugt werden kann, wird dieser Hinweis in der Ergebnisliste gezeigt.

Häufige Gründe fürs nicht Erzeugen einer Datei sind beispielsweise:

* Schüler, denen keine Fachdaten zugewiesen wurden
* Lehrer, denen keine Schüler zugeordnet wurden (als Fachlehrer, Tutor oder Klassenleiter)
* im Zielverzeichnis existiert bereits eine gleichnamige Datei, die nicht überschrieben wird

![Beispiel für Ergebnismeldungen](/assets/images/mymagellan/20.png)

Am gewählten Speicherort werden die Dateien erzeugt.

![Erstellte MyMAGELLAN-Dateien](/assets/images/mymagellan/21.png)

!!! info "Hinweis"

	 Die neue Dateiendung `mym7` erzeugt MAGELLAN unabhängig von der Angabe im Speicherpfad, Sie müssen dafür nichts anpassen.

## Übermittlung der Datei an die eingebenden Kollegen

Im nächsten Schritt sind die Dateien an die Kollegen zur Eingabe zur Übermitteln. Die Datei ist als Binärdatei nicht lesbar, das Passwort ist zwar in der Datei enthalten, aber mit einer kryptografischen Funktion so gesichert, dass es nicht ausgelesen werden kann.

Zusätzlich zur Datei brauchen die Kollegen zum Bearbeiten der mym-Datei auch das Programm MyMAGELLAN, dass lizenzfrei auf unserer Webseite geladen werden kann. Die Installation des Programms ist schnell und unkompliziert. Allerdings sollte die verwendete MyMAGELLAN-Version auch der zu lesenden Datei entsprechen, insofern ist es sinnvoll den Kollegen auch die Installationsdatei zur Verfügung zu stellen.

!!! warning "Wichtig"

	Bitte übergeben Sie den Kollegen jeweils die mym-Datei und auch das MyMAGELLAN-Installationspaket. Damit stellen Sie sicher, dass Ihre Kollegen die korrekte Ausgabe von MyMAGELLAN zur Verfügung haben.
	MyMAGELLAN läuft, anders als in vorangegangenen Versionen, immer mit paralleler Versionsnummer zu MAGELLAN. Beispiel: 
	Wird MAGELLAN 7.0.22 veröffentlicht, gibt passend dazu auch MyMAGELLAN 7.0.22.

Für die Übermittlung werden von den Schulen die unterschiedlichsten Wege gewählt, Beispiele:

* Die Kollegen erhalten jeweils einen Stick mit der eigenen mym-Datei, zusätzlich kann man auf dem Stick auch das jeweils aktuelle Installationspaket des Noteneingabeprogrammes MyMAGELLAN mit geben.
* Die Dateien werden in einem passwortgeschützten Bereich der Schulwebseite zum Download angeboten und später gefüllt wieder hochladen.
* Als Anhang einer Mail mit einem Downloadlink zur MyMAGELLAN-Installationspaket auf unserer Webseite oder an einer Ablagestelle Ihrer Wahl.
* Die Eingabe erfolgt innerhalb der Schule, die Dateien werden in Ihrem Netzwerk zu Verfügung gestellt.