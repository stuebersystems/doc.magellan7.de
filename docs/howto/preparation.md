# Datenbank vorbereiten

Dieses Kapitel beschreibt die grundlegenden vorbereitenden Schritte für die Arbeit mit MAGELLAN.  Weitere Detailinformationen zur Administration von MAGELLAN finden Sie im Kapitel Administration.
Wenn Sie MAGELLAN erstmalig installieren, werden beim Installationstyp `Server- Einzelplatzinstallation` im Verzeichnis `Datenbank` (Standardpfad: C:\Users\Public\Documents\Stueber Systems\MAGELLAN 7\Datenbank) zwei Datenbanken abgelegt. 

| Name                   | Zweck                                                                                                                                                                                                                                                                                                                                                                          |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| MAGELLAN7.fdb          | Diese Datenbank ist leer und für den Start mit MAGELLAN gedacht. Sollten Sie bereits MAGELLAN 6 verwendet haben, ist diese leere Datenbank als Ziel beim Übertrag Ihrer Daten aus der MAGELLAN6.fdb gedacht. Lesen Sie in diesem Fall bitte unseren Abschnitt [Umstieg von MAGELLAN 6 auf MAGELLAN 7](https://doc.MAGELLAN7.stueber.de/installation/umstieg-von-6-auf-7.html)! |
| MAGELLAN7_Beispiel.fdb | Enthält Beispieldaten anhand derer Sie sich die Abläufe in MAGELLAN anschauen können.                                                                                                                                                                                                                                                                                          |

## MAGELLAN starten

Klicken Sie auf `Start > Programme > STÜBER SYSTEMS > MAGELLAN`. Die MAGELLAN-Datenbank ist grundsätzlich kennwortgeschützt. Wenn Sie MAGELLAN bzw. den MAGELLAN-Administrator starten, müssen Sie in einem Anmeldedialog Ihre Benutzerkennung und Ihr Kennwort angeben.
 
![MAGELLAN-Anmeldung](../assets/images/dialog-anmeldung.png)

Der Standardbenutzer lautet „sysdba“ und das dazugehörige Standardkennwort lautet „masterkey“. Mit dieser Standardkennung sind volle Administrationsrechte verbunden. Weitere Informationen zur Anlage und Editierung von Benutzerkennungen und den damit verbundenen Rechten finden Sie im Kapitel [„Benutzerverwaltung“](https://doc.magellan7.stueber.de/admin/users.html).

## Datenbank für den Alltag vorbereiten
 
Richten Sie eine neue Datenbankanbindung zur in der Auslieferung enthaltenen leeren MAGELLAN-Datenbank ein. Eine ausführliche Anleitung finden Sie im Abschnitt [Datenbankverbindungen](https://doc.MAGELLAN7.stueber.de/admin/admin.datenbankverbindungen.html).


## Postleitzahl- und Schlüsselverzeichnisse importieren

Nachdem Sie mit der leeren Datenbank verbunden sind, sollten Sie die bundeslandspezifischen Schlüsselverzeichnisse und das Postleitzahlverzeichnis importieren. Die Schlüsselverzeichnisse beinhalten je nach Bundesland und Schulart die für die Statistik vorgeschriebenen möglichen Schlüssel. Sollten Sie Ihre leere Datenbank bereits für einen Versuch gefüllt haben, erhalten Sie im MAGELLAN ADMINISTRAROR im Unterpunkt `Datenbankpflege > Mandanten kopieren > MAGELLAN 6 nach MAGELLAN 7 ` über folgende Schaltfläche jederzeit eine neue leere Datenbank im aktuellen Format.


  ![Datenbankpflege > Mandanten kopieren > Mag6 nach Mag7](../assets/images/neue.leere.db.png)






!!! info "Hinweis"

  Möchten Sie eigene Werte in Schlüsselverzeichnisse importieren, können Sie die Importdateien auch editieren. Lesen Sie dazu bitte den Abschnitt ["Administration > Importe und Exporte > Eigene oder mitgelieferte Schlüsselverzeichnisse importieren"](https://doc.magellan7.stueber.de/admin/import-export.html/#eigene-oder-mitgelieferte-schlüsselverzeichnisse-importieren)!

Das Postleitzahlverzeichnis beinhaltet alle deutschen Postleitzahlen inkl. der bundesweit eindeutigen Gemeindeschlüssel und dem Bankleitzahlverzeichnis. Wenn Sie das Postleitzahlverzeichnis importieren, können Sie die automatische Zuordnung von Postleitzahl zu einem Ort bzw. Ort zu einer Postleitzahl nutzen. 

1. Klicken Sie auf `Ansicht > Datenaustausch` und dann auf `Kataloge (Schlüsselverzeichnisse) importieren` bzw. auf `Postleitzahlen und Banken importieren`, um das jeweilige Verzeichnis zu importieren. 

2. Wählen Sie für den Import der Schlüsselverzeichnisse Ihr Bundesland, Ihren Mandanten und Ihren Schultyp und klicken auf `Fertigstellen`. Beim Import des Postleitzahlverzeichnisses muss nur die Region (Deutschland, Schweiz oder Berlin (ist wie Deutschland, zusätzlich werden Stadtbezirke für Berlin importiert)) angegeben werden.

3. Anschließend können Sie MAGELLAN starten und mit der Eingabe wichtiger Grunddaten in MAGELLAN beginnen.
  
  ![Importassistent für Schlüsselverzeichnisse](../assets/images/dialog-import-schluesselverz.png)

!!! info "Hinweis"

  Sie können im Assistenten „Importiere Schlüsselverzeichnisse/Kataloge“ im Feld „Importiere folgenden Katalog“ auch einzelne Kataloge zum Import auswählen.

![Importassistent für Postleitzahlen](../assets/images/dialog-import-plz.png)

!!! info "Hinweis"

  Der Assistent liest Postleitzahlen, Bezirke, Kreise, Bundesländer, Gemeindeschlüssel, Banken und für die Auswahl „Berlin“ auch Stadtbezirke ein.

## Bankenverzeichnis importieren

Sie können das Verzeichnis der Banken auch getrennt einlesen. Dazu gehen Sie im MAGELLAN-Administrator wie folgt vor:

1. Klicken Sie auf `Ansicht > Datenaustausch` und dann auf `Postleitzahlen und Banken importieren`. 

2. Treffen Sie unter `Import für folgendes Land` Ihre Auswahl.

3. Wählen Sie unter `Importiere` folgenden Katalog den Wert `Banken` aus und klicken Sie dann auf `Fertigstellen`.

!!! info "Hinweis"

  Im Rahmen der Änderung im Zahlungsverkehr ab 2014 müssen Sie im Bankenverzeichnis auch den BIC-Wert der jeweiligen Bank berücksichtigten. Durch das erneute Einlesen nur des Bankenverzeichnisses können Sie Ihr bisheriges Bankenverzeichnis um den BIC-Wert ergänzen.

## Schlüsselverzeichnisse editieren

In MAGELLAN finden Sie zwei verschiedene Arten von Formularfeldern. Die einen sind frei auszufüllen (z.B. der Name), bei den anderen wurde eine Liste hinterlegt (z.B. Konfessionen), aus der Sie Einträge auswählen müssen. Der Inhalt der Listen stammt aus sogenannten Schlüsselverzeichnissen und sind in MAGELLAN Quellen für viele Eingabefelder auf den Formularen. 
Sie sollen Ihnen die Arbeit bei der Dateneingabe erleichtern. Daten, die nicht in den Schlüsselverzeichnissen hinterlegt wurden, stehen Ihnen für den Eintrag im Formularfeld nicht zur Verfügung. 
Sie sollten also, wenn Sie anfangen mit MAGELLAN zu arbeiten, diese Verzeichnisse editieren und den Datenbestand für Ihre Anforderungen passend gestalten. In den folgenden Abschnitten werden Ihnen die Schlüsselverzeichnisse allgemein und einige Verzeichnisse wie z.B. Noten oder Fächer in den nachfolgenden Kapiteln gesondert erläutert. 

1. Um die Schlüsselverzeichnisse aufzurufen, klicken Sie auf `Extras`und dann auf `Schlüsselverzeichnisse`. 

2. Es öffnet sich das Dialogfenster Schlüsselverzeichnisse.
  
  ![Weitere Schlüsselverzeichnisse](../assets/images/dialog-schluesselverz.png)

3. Im Fenster „Schlüsselverzeichnisse“ sind alle Schlüsselverzeichnisse aufgelistet, die es in MAGELLAN gibt, allerdings sind nicht alle in der Startansicht zu sehen, sondern werden erst mit der Auswahl des jeweiligen Gruppenfilters gezeigt. Den Gruppenfilter finden Sie links oben im Fenster, hier sind Verzeichnisse nach bestimmten Gruppen zusammengefasst, zum Beispiel alle Merkmalsverzeichnisse sind in der Gruppe Merkmale.

4. Wählen Sie das gewünschte Schlüsselverzeichnis aus, z.B. „Dienstbezeichnungen“, und klicken Sie auf das Stiftsymbol um es zu bearbeiten. Das gewünschte Schlüsselverzeichnis kann jetzt editiert werden.
  
  ![Verzeichnis der Dienstbezeichnungen](../assets/images/dialog-dienstbez.png)

5. Wenn nicht schon die einzelnen Schlüssel voreingestellt sind, haben Sie hier die Möglichkeit Schlüssel einzutragen, indem Sie auf das Plus für` Neue Zeile` klicken. Sie können dann direkt in der neu eingefügten Zeile die notwendigen Angaben wie z.B. Kürzel (Mindesteingabe), Schlüssel und Bezeichnung angeben. 

6. Möchten Sie einen Schlüssel verändern, so markieren Sie die entsprechende Spalte in der Zeile des Schlüssels. Verändern Sie den Schlüssel nach Ihren Wünschen. 

Der Schlüssel wird in dem Verzeichnis geändert. Alle Einträge in den Schlüsselverzeichnissen erhalten eine zeitliche Gültigkeit. Geben Sie bei Bedarf, die Von/Bis- Dauer in den entsprechenden Spalten ein. Dies ist für bestimmte Statistik notwendig,  z.B. für E-Stat in Baden-Württemberg. Man kann so z.B. prüfen, ob wirklich die aktuellen Schlüssel verwendet worden sind. Werden Werte aus Verzeichnissen ausgewählt, die eine zeitliche Gültigkeit haben (z.B. Staatsangehörigkeit oder Konfession) so erfolgt die Anzeige nach Gültigkeit gruppiert. Es werden alle gültigen Schlüssel mir einer blauen Raute, gefolgt von den ungültigen mit einer grauen Raute, zur Auswahl angeboten. 

* Möchten Sie einen Schlüssel löschen, so klicken Sie im Verzeichnis auf den zu löschenden Schlüssel und dann auf das Symbol Minus. Nachdem Sie bestätigt haben, wird der Schlüssel aus dem Verzeichnis gelöscht. 

* Möchten Sie ein Schlüsselverzeichnis nach Excel exportieren, so klicken Sie auf das Symbol für den Export nach Excel (schwarzes Kästchen mit einem X). Es öffnet sich das Dialogfenster Liste exportieren nach Excel.

![Schlüsselverzeichnisse exportieren](../assets/images/dialog-schluesselverz-speichern.png)

Wählen Sie eine Pfadangabe nach Ihren Wünschen, vergeben Sie einen Dateinamen und klicken Sie auf Speichern. Excel startet automatisch und öffnet die soeben angelegte Datei. 

!!! info "Hinweis"

  Eventuell sind schon einige Schlüsselverzeichnisse in MAGELLAN über den MAGELLAN-Administrator importiert worden. Wenn Sie mit einem solchen voreingestellten Verzeichnis arbeiten, sollten Sie sich sicherheitshalber vergewissern, ob die Schlüssel und die Kürzel korrekt sind. Kürzel sind von der Bezeichnung her beliebig, die Schlüssel dürfen nicht verändert werden, da sie sonst nicht mehr mit den Statistikschlüsseln übereinstimmen. 

Wenn Sie mit einer mandantenfähigen Version arbeiten, beachten Sie bitte, dass folgende Schlüsselverzeichnisse mandantenabhängig sind:

* Abteilungen
* Abschlussjahrgänge
* Fächer
* Fachtafeln
* Noten
* Merkmale der Lehrer, Klassen und Schüler
* Zeugnisbemerkungen
* Zeugnisbeurteilungen

Alle anderen Schlüsselverzeichnisse gelten für alle Mandanten.

## Mandanten anpassen

In MAGELLAN muss mindestens ein Mandant definiert sein. Wie schon früher erwähnt, ist der Mandant in der Regel Ihre eigene Schule. In der Standardversion von MAGELLAN können Sie nur einen Mandanten eintragen. Dieser Mandant entspricht Ihrer Schule. Besitzen Sie eine SchoolCentral-Lizenz für mehrere Mandanten, können Sie mehr als einen Mandanten in MAGELLAN erfassen. Alle Stammdaten in MAGELLAN sind automatisch einem Mandanten zugeordnet. Alle Betrachtungen in MAGELLAN erfolgen auf Basis des aktuell ausgewählten Mandanten.

![Mandant auswählen](../assets/images/select-mandanten-zeitraeume.png)

Besitzen Sie eine mandantenfähige Version von MAGELLAN, so müssen Sie bei Bedarf zwischen den Mandanten wechseln, um die gewünschten Daten zum jeweiligen Mandanten zu sehen.

!!! info "Hinweis"

  Mandanten sollten grundsätzlich nur durch den Administrator angelegt werden.

Um sich an einer  Datenbank anzumelden, muss mindestens ein Mandant vorhanden, bitte übeschreiben Sie gegebenenfalls die Daten unter `MAGELLAN > Mandanten > Daten` mit den Daten Ihrer Schule überschrieben. 

1. Öffnen Sie MAGELLAN mit der Kennung sysdba und dem Passwort masterkey.
2. Wählen Sie den Menüpunkt `Mandanten`und doppelklicken Sie auf die Zeile des Beispielmandanten.
3. Sie befinden sich automatisch auf der Registerkarte `Daten 1` des Mandanten. Ersetzen Sie nun die erforderlichen Daten in den Feldern durch Ihre eigenen Schuldaten. Fertig!


Auf der Registerkarte `Daten 1` können Sie neben der Anschrift der Schule auch den Schulleiter und den Stellvertreter eintragen. Beide Einträge basieren auf der Auswahl der bisher erfassten Lehrer. Der Eintrag des Schulleiters ist insbesondere für den Ausdruck der Zeugnisse wichtig. Die verschiedenen Schulformen Ihrer Schule können Sie auf der Registerkarte `Daten 2` erfassen. Zusätzlich können Sie mit der Schule bis zu drei Adressen verbinden. Dies kann z.B. das Schulamt oder der Schulträger sein. Diese Adressen müssen zuvor in den Stammdaten der Adressen eingetragen worden sein.

## Zeiträume definieren

Der Zeitraumbezug spielt in MAGELLAN eine wichtige Rolle. Sie müssen daher vor der eigentlichen Eingabe der anderen Daten in MAGELLAN die notwendigen Zeiträume definieren. Ein Zeitraum ist definiert durch ein Anfangs- und ein Enddatum. Zusätzlich sollten noch einige weitere Angaben pro Zeitraum eingetragen werden. In der Regel werden Sie Zeiträume halbjahresweise eingeben (z.B. 1. Halbjahr 2017/2018, 2. Halbjahr 2017/2018). Dieses Intervall empfiehlt sich, wenn halbjahresweise Zeugnisse geschrieben werden.

!!! info "Hinweis"

  Alternativ können Sie auch grundsätzlich in Trimestern arbeiten, allerdings können Halbjahre und Trimester nicht innerhalb einer Datenbank verwaltet werden. Die Datenbank ist standardmäßig auf Halbjahre ausgelegt. Starten Sie mit MAGELLAN, kann die Datenbank auf Trimester über eine Option umschalten. Bitte lesen dazu hier [weiter](https://doc.magellan7.stueber.de/admin/preferences.html/#extras--optionen--einstellungen). Sind bereits Daten in der Datenbank enthalten, wenden Sie sich bitte an uns.


## Zeiträume eingeben

Um einen neuen Zeitraum zu definieren, klicken Sie im Menü `Extras > Schlüsselverzeichnisse` auf `Zeiträume`. 

![Verzeichnis der Zeiträume](../assets/images/dialog-zeitraeume.png)

### Halbjahre

Um einen neuen Zeitraum einzustellen, klicken Sie auf `Schuljahre anlegen` . Der Assistent legt für Sie ein Schuljahr an, bestehend aus zwei Halbjahren, die standardmäßig vom **01.08-31.01 **und von **01.02.-31.07 **dauern. Bitte behalten Sie die Start- und Enddaten für das Kalenderhalbjahr bei, die tatsächliche Dauer ist später über Laufbahndaten der Schüler erkennbar.

### Deutsche Auslandsschulen (Südamerika)

!!! info "Hinweis"

  Auslandsschulen, bei denen das 1.Schulhalbjahr vom 01.01.-31.07. und das 2.Schulhalbjahr vom 01.08.-31.12. läuft, nutzen bitte nicht die Schaltfläche `Schuljahre anlegen`, sondern legen die Schulhalbjahre bitte manuell über die Plus-Schaltfläche an. Nachfolgend die Eintragungen beispielhaft pro Feld:

| Feld           | Eintragungen                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ID             | Wird beim Speichern automatisch besetzt                                                                                                                                                                                                                                                                                                                                                                                  |
| Bezeichnung    | Die Angabe in der Spalte „Bezeichnung“ wird zur Anzeige des aktuell gewählten Zeitraums in MAGELLAN verwendet. (zb. 1. Halbjahr 2018/19)                                                                                                                                                                                                                                                                                 |
| Art            | Bitte jeweils die Zeilen mit den Werten 1. Halbjahr bzw. 2. Halbjahr versehen. Diese Eintragungen sind wichtig um später die Halbjahresergebnisse der Schüler korrekt ins Menü `Abitur` zu synchronisieren.                                                                                                                                                                                                              |
| Von - Bis      | Für Halbjahre wählen Sie bitte standardmäßig:<br />1. Halbjahr 01.01.-31.07.<br />2. Halbjahr 01.08.-31.01.                                                                                                                                                                                                                                                                                                              |
| Ausdruck 1 + 2 | Die unter `Ausdruck 1` und `Ausdruck 2` eingetragenen Daten dienen nur für die Verwendung alternativer Zeitraumbezeichnungen im Ausdruck von Berichten (z.B. bei Zeugnissen). Die standardmäßig mitgelieferten Berichte nutzen dabei den Eintrag unter `Ausdruck 1` für die Halbjahresbezeichnung (z.B. 1. Halbjahr 2008/2009) und den Eintrag unter `Ausdruck 2` als Schuljahresbezeichnung (z.B. Schuljahr 2008/2009). |



### Trimester

Wenn Sie sich entschieden haben mit Trimestern zu arbeiten, steht Ihnen der Assistent leider nicht zur Verfügung. Bitte legen Sie über das Plus in der Menüleiste des Zeiträume-Fensters eine neue Zeile an und füllen die nachstehenden Felder:

| Feld           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ID             | Wird beim Speichern automatisch besetzt                                                                                                                                                                                                                                                                                                                                                                                  |
| Bezeichnung    | Die Angabe in der Spalte „Bezeichnung“ wird zur Anzeige des aktuell gewählten Zeitraums in MAGELLAN verwendet.                                                                                                                                                                                                                                                                                                           |
| Art            | Wenn Sie die Zeiträume als Halbjahr definiert haben (`Extras > Optionen > Einstellungen > Zeiträume`) können Sie in der Spalte Art die Werte 1. Halbjahr bzw. 2. Halbjahr auswählen. Wenn die Zeiträume als Trimester definiert sind, können Sie in der Spalte Art die Werte 1. Trimester, 2. Trimester bzw. 3. Trimester auswählen.                                                                                     |
| Von - Bis      | Für Halbjahre wählen Sie bitte standardmäßig:<br />1. Halbjahr 01.08.-31.01.<br />2. Halbjahr 01.02.-31.07.<br />Für Trimester wählen Sie bitte standardmäßig:<br />1. Trimester 01.08.-31.12.<br />2. Trimester 01.01.-30.04.<br />3. Trimester 01.05.-31.07.                                                                                                                                                           |
| Ausdruck 1 + 2 | Die unter `Ausdruck 1` und `Ausdruck 2` eingetragenen Daten dienen nur für die Verwendung alternativer Zeitraumbezeichnungen im Ausdruck von Berichten (z.B. bei Zeugnissen). Die standardmäßig mitgelieferten Berichte nutzen dabei den Eintrag unter `Ausdruck 1` für die Halbjahresbezeichnung (z.B. 1. Halbjahr 2008/2009) und den Eintrag unter `Ausdruck 2` als Schuljahresbezeichnung (z.B. Schuljahr 2008/2009). |

## Aktuellen Zeitraum definieren

Sie haben die Möglichkeit, sich einen aktuellen Zeitraum zu definieren. Beim Öffnen von MAGELLAN wird standardmäßig der höchste eingegebene Zeitraum geöffnet. Wenn Sie sich einen aktuellen Zeitraum definieren, wird dieser automatisch nach dem Start angezeigt. Klicken Sie dazu auf `Extras` und dann auf `Optionen`. Auf der Registerkarte `Start` können Sie unter `Zeitraum` den aktuellen Zeitraum auswählen.

![Den Startzeitraum in den Optionen einstellen](../assets/images/dialog-optionen-1.png)

## Zeitraum auswählen

Sie können die Zeiträume wechseln, um beispielsweise historische Daten anzusehen oder für das kommende Schuljahr schon mit der Dateneingabe zu beginnen. In der Symbolleiste oben links wird Ihnen der Zeitraum angezeigt, in dem Sie arbeiten.

![Den aktuellen Zeitraum auswählen (hier: 2. Halbjahr 2010/2011)](../assets/images/select-mandanten-zeitraeume.png)

## Daten importieren

Wenn Sie bereits mit einem Schulverwaltungsprogramm gearbeitet haben, dann möchten Sie wahrscheinlich die Daten nach MAGELLAN übernehmenohne alle Daten wieder neu einzugeben. Aus vielen gängigen Schulverwaltungsprogrammen können Sie ohne großen Aufwand den Großteil der Daten übernehmen. 
Die Dokumentation ["MAGELLAN Import"](https://doc.MAGELLAN-import.stueber.de/) sagt Ihnen, aus welchen Programmen MAGELLAN Daten standardmäßig übernehmen kann bzw. wie Sie über das MAGELLAN-Importformat Daten aus Textdateien nach MAGELLAN übernehmen können. Sie finden dort die nötigen Informationen, um den Import aus einem der dort erwähnten Programme erfolgreich durchführen zu können. Lesen Sie sich die entsprechenden Abschnitte sorgfältig durch, um mögliche Fehler zu vermeiden. Wenn Sie ein anderes Programm einsetzen, dann müssen Sie entscheiden, ob Sie die Daten selber übernehmen wollen oder ob Sie STÜBER SYSTEMS mit der Übernahme beauftragen wollen.

Daten selber übernehmen: Mit Hilfe der MAGELLAN-Scripting-Technologie und der Dokumentation der MAGELLAN-Datenstruktur können Sie Daten aus anderen Datenquellen in die entsprechenden Tabellen importieren. Ausführliche Hinweise hierzu finden Sie in den PDF-Dokumenten ["MAGELLAN-Scripting"](https://doc.MAGELLAN-scripting.stueber.de/) und die Dokumentation der "MAGELLAN-Datenstruktur" (bitte unter support@stueber.de anfordern).

Daten von STÜBER SYSTEMS übernehmen lassen: Sie können STÜBER SYSTEMS jederzeit Ihre Daten und die nötigen Informationen zum Programm zuschicken. STÜBER SYSTEMS wird Ihnen dann ein entsprechendes Angebot für die Datenübernahme machen. Dies ist der schnellste Weg für spezielle Importe.
