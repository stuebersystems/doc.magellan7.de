
# Magellan 6-Berichte für 7 oder höher anpassen

Aufgrund technischer Veränderungen in Magellan 7 und 8 müssen Berichte aus Magellan 6 für die neueren Version angepasst werden.

!!! warning "Wichtig"

    Berichte, die für Magellan 6 genutzt wurden, müssen vor der Verwendung in Magellan 7 oder 8 angepasst werden. Berichte, die bereits unter Magellan 7 oder höher verwendet wurden, müssen NICHT für den Einsatz unter Magellan 8 angepasst werden.

Alle mitgelieferten Originalberichte von STÜBER SYSTEMS wurden angepasst und ausgeliefert.
Berichte, die von Schulen verändert worden sind oder selbsterstellte Berichte liegen im Verantwortungsbereich der Schulen. Im Folgenden erläutern wir die Gründe und die notwendigen Anpassungen.

!!! warning "Wichtig"

    Wenn Sie unsere ausgelieferten Magellan 7-Berichte als Vorlage für eigene Anpassungen nutzen möchten, benötigen Sie mindestens die Ausgabe `CRYSTAL REPORTS 2013`. 
    Um Ihre eigenen Berichte für Magellan 7 anzupassen benötigen Sie mindestens `CRYSTAL REPORTS 2011`.

## Beauftragen Sie uns

Sie können Ihre Berichte nach der untenstehenden Anleitung umstellen oder uns beauftragen.
Schreiben Sie uns bitte eine Nachricht unter dem **Stichwort "Angebot: Magellan 6-Berichte umstellen"** an [office@stueber.de](mailto:office@stueber.de), wir erstellen Ihnen gern ein Angebot, schreiben Ihnen die weiteren Schritte und erstellen Ihnen ein Uploadverzeichnis usw.

## Schritte zum Bericht umstellen

### Magellan unterstützt Unicode

Dies ist grundsätzlich eine erfreuliche Nachricht, da ab Version 7 sämtliche Schriftzeichen in der Magellan-Datenbank gespeichert werden können. Beispielsweise alle Namensschreibweisen sind nun möglich und auch für den Zeugnisdruck ausgebbar.  
Bedingt durch diese Umstellung benötigt Magellan 7 aber einen aktualisierten ODBC-Treiber, der Unicode verarbeiten kann.
Der bisherige ODBC-Treiber ist mittlerweile in die Jahre gekommen und für die neuen Anforderungen nicht geeignet.

!!! info "Hinweis"

    Wir empfehlen für die Änderung der eigenen Berichte sich eine lokale Magellan 7-Installation einzurichten. 

!!! warning "Wichtig"

    Während Tests mit dem neuen ODBC-Treiber und unseren Berichten ist aufgefallen, dass viele Berichte eine Fehlermeldung produzierten, die nach Recherchen auf problematische Datenbank-Abfragen zurückzuführen sind, die ältere Crystal-Reports Versionen produzieren. Der ältere ODBC-Treiber, der in Magellan 6/6.5 Verwendung findet, scheint dahingehend fehlertolerant zu sein, verweigert der neuere Treiber die Verarbeitung und erzeugt einen Fehler.

### Was ist zu tun - eine Übersicht

Nr.|Was ist zu tun
--|--
1.|[ODBC-Treiber-Einstellungen](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#1-odbc-treiber-einstellungen)
2.|[ggfs. Datenbankverbindung aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#6-datenbankverbindung-aktualisieren)
3.|[Datenquellenpfad festlegen](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#3-datenquellenpfad-festlegen)
4.|[Tabellenverknüpfungen anpassen](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#4-tabellenverknupfungen-anpassen)
5.|[Test](https://doc.magellan.stueber.de/schulverwaltung/update/Berichte_anpassen/#5-test)

### 1. ODBC-Treiber-Einstellungen

Um das Problem beheben zu können, müssen wir fehlerfrei auf die Datenbank zugreifen können. Das funktioniert nur, wenn wir zuvor ein paar Einstellungen an den ODBC-Treiber weitergeben.

!!! info "Hinweis"

    Diese Einstellungen sind nur notwendig um die Anpassungen an Ihren eigenen Berichten vorzunehmen. Für den Druck und die Druckvorschau aus Magellan gibt es andere Voreinstellungen. 
    Die für Magellan notwendigen Druckeinstellungen in der ODBC-Anbindung werden automatisch beim Aufruf der Druckvorschau gesetzt.

|Gehen Sie wie folgt vor:|
|:--|
|1. Starten Sie den ODBC-Datenquellen-Administrator (32-Bit) in Windows.<br>Auf der Registerkarte ```Treiber``` finden Sie den aktuellen mit Magellan 7 installierten Treiber. Da muss mindestens die im Bild angegeben Version stehen.
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/odbc_1_Treiber.png>|
|**Bitte achten Sie darauf, dass Ihr zu ändernder Bericht währenddessen noch nicht in Crystal Reports geladen ist!**|
|2. Wechseln Sie auf die Registerkarte ```Benutzer-DSN``` und wählen Sie den Eintrag ```Magellan-CR``` aus. Dieser wird von Magellan automatisch erstellt. Finden Sie keinen solchen Eintrag, dann starten Sie Magellan 7 und öffnen einen Bericht in der Vorschau. Danach sollte der Eintrag vorhanden sein. Klicken Sie auf ```Konfigurieren```.
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/odbc_2_BenutzerDSN.png>|
|2. Im Konfigurationsfenster geben Sie bei ```Character Set``` den Wert ```NONE``` ein, oder wählen diesen aus. Im Bereich ```Extended identifiert properties``` setzen Sie bitte **alle** Häkchen.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/odbc_3_KonfigurationKorrektur.png>|

!!! info "Hinweis"

     Wenn Sie zwischenzeitlich Magellan auf dem Rechner (Druckvorschau!) verwendet haben, ändert sich diese Einstellung wieder. 
     Bitte kontrollieren Sie vor dem erneuten Start von Crystal Reports diese Einstellungen.

!!! danger "Achtung"

    Ihr Fenster sieht nicht so aus wie in der vorstehenden Abbildung? Dann bitte über den nachstehenden Link das Installationspaket des ODBC-Treibers laden. Anschließende Magellan bitte schließen und die Installation ausführen. 

Downloadseite|Eintrag
--|--
[https://firebirdsql.org/en/odbc-driver/](https://firebirdsql.org/en/odbc-driver/) | Windows 32-bit Full Install

### 2. Datenbankverbindung aktualisieren

Wenn Sie auf einem Rechner arbeiten, mit dem Sie üblicherweise Ihre Crystal-Reports Berichte bearbeiten, dann legt Crystal-Reports gerne mehrere Datenquellen zur ODBC-Verbindung an. Um da für die Korrektur nicht durcheinander zu kommen, räumen wir an der Stelle auf.

Die vorstehende Meldung taucht allerdings auf, weil in der Datenbankverbindung, mit der Sie gerade angemeldet sind, nicht der korrekte Zeichensatz verwendet wird. 
Per `Rechtsklick > Eigenschaften`auf eine Verbindung können Sie den Unterschied sehen.

Diese Einstellung kann man nicht direkt editieren, letztlich muss eine neue korrekte Verbindung angelegt werden.

![Falscher Zeichensatz in der Verbindung](/assets/images/berichte.anpassen/berichte.anpassen4.png)![Richtiger Zeichensatz in der Verbindung](/assets/images/berichte.anpassen/berichte.anpassen5.png)  

|Gehen Sie wie folgt vor:|
|:--|
|1. Klicken Sie im Menu auf ```Datenbank > Bei Server an-/abmelden...```|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/berichte.anpassen3.png>|
|2. Melden Sie sich zuerst über die ```Abmelden``` Schaltfläche von allen Verbindungen ab. Wenn die Schaltfläche `Abmelden` für alle Verbindungen grau ist, dann sind sie auch nirgends angemeldet. |
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step1_2.png>|
|3. Im Daten-Explorer sollte unter `Meine Verbindungen` nur eine Verbindung stehen.<br>Wenn Sie mehrere Verbindungen finden, löschen Sie alle (bei denen es möglich ist), wie folgt heraus:|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step1_3.png>|
|4. Benennen Sie die verkehrte(n) Datenbankverbindung um (Rechtsklick > Umbenennen), damit keine der bisherigen Verbindungen mehr "Magellan-CR" heißt und legen anschließend eine neue Datenbankverbindung an.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/berichte.anpassen6.png>|
|5. Öffnen Sie die neue Datenbankverbindung, indem Sie auf das Plus vor "Magellan-CR" und anschließend auf das Plus vor "Tabellen" klicken.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/berichte.anpassen7.png>|
|6. Melden Sie sich wieder an und testen die Vorschau, jetzt sollte es klappen!|

### 3. Datenquellenpfad festlegen

Fehlermeldungen:

![Meldung](/assets/images/berichte.anpassen/cr_error_msg1.png) 

![Meldung](/assets/images/berichte.anpassen/cr_error_msg2.png)

!!! warning "Wichtig"

    Die nachfolgenden Schritte sind **für den Hauptbericht und aus allen Unterberichten heraus** durchzuführen.

|So gehen Sie vor:|
|:--|
|1. Öffnen Sie zusätzlich zum Hauptbericht alle Unterberichte. Starten Sie aus dem Hauptbericht.|
|2. Klicken Sie im Menü auf ```Datenbank > Datenquellenpfad festlegen...```|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_1.png>|
|3. Im Dialogfenster wählen Sie wie im Bild beschrieben zuerst oben die erste Ansicht/Tabelle aus.<br> Dann öffnen Sie unten die bestehende Verbindung und melden sich an.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_2.png>|
|4. Im Beispiel ist das erste Element ```AuswahlZeugnisse``` eine Ansicht.<br> Das heißt, sie öffnen im unteren Bereich ```Ansichten```.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_3.png>|
|5. Wählen die Ansicht auch im unteren Bereich aus. Dann klicken Sie auf ```Aktualisieren```.|
|**ACHTUNG: Ein Doppelklick wird hier von Crystal Reports nicht korrekt verarbeitet, bitte nutzen Sie die Schaltfläche `Aktualisieren` oder die Taste `Enter`.**|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_4.png>|
|5. Den Vorgang wiederholen Sie mit allen Ansichten/Tabellen die in Ihrem Bericht vorhanden sind.<br>Auch mit den Ansichten/Tabellen von Unterberichten.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_5.png>|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_6.png>|
|6. Sonderfall ```SchuelerKlassen```<br>Die SchuelerKlassen haben eine neue Datenstruktur und Crystal-Reports kennt im bestehenden Bericht lediglich die alte Datenstruktur. Damit kann die Tabelle nicht einfach neu verknüpft werden. Sie erhalten deshalb ein weiteres Dialogfenster, dass Sie lediglich mit ```OK``` quittieren.|
| **Abbildung:**<br> <img src=/assets/images/berichte.anpassen/cr_fix_step2_7.png>|
|**Wichtig: Wiederholen Sie diese Schritte bitte auch jeweils aus den vorab geöffneten Unterberichten heraus.**|

### 4. Tabellenverknüpfungen

Außerdem sind ab Magellan 7 einige wichtige Umstellungen in der Datenbankstruktur vorgenommen worden, um neue und verbesserte Funktionalitäten abbilden zu können. Dadurch sind einige Felder entfernt und an anderer Stelle hinzugekommen.

Sie öffnen bitte den Punkt `Datenbank-Assistent..`und rufen die Unterkarte `Verknüpfungen` auf.

!!! info "Hinweis"

    Prüfen Sie, ob die folgenden Tabellen oder Felder **im Bericht oder in einem Unterbericht** genutzt wurden, was dann zu tun ist, wird nachstehend beschrieben. Bitte denken Sie daran, dass der Punkt `Datenbank > Datenbank-Assistent > Unterkarte Verknüpfungen` immer nur die Verknüpfungen für den gerade gewählten Hauptbericht oder den ausgewählten Unterbericht zeigt. Bitte prüfen Sie auch die Verknüpfungen in den Unterberichten.

Tabelle |Feld
--|--
Schueler und SchuelerAusbildung|[Verknüpfungen lösen](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schuelerzeitraeume-und-schuelerausbildung)
Schueler|[ehemalige Felder: SopaedFoerderungen, Foerderschwerpunkt1, Foerderschwerpunkt2 und Behinderung ](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schueler)
SchuelerZeitraeume und SchuelerKlassen|[Neue Verknüpfungen](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schuelerklassen)
SchuelerZeitraeume und SchuelerAusbildung|[Neue Verknüpfungen](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#schuelerzeitraeume-und-schuelerausbildung)

!!! info "Hinweis"

    Wenn keine der Tabellen oder keines der Felder genutzt wurde, können Sie speichern und zum Test die Druckvorschau (bei mehrseitigen Berichten bitte auch auf die weiteren Seiten blättern) aufrufen. Klappt alles, ist der Bericht fertig für die Nutzung in späteren Magellan Versionen.

!!! info "Hinweis"

    Die aktuelle Datenstrukturbeschreibung finden Sie als Teil der Dokumentation [Magellan TOOLBOX](https://doc.magellan-toolbox.stueber.de/).

#### "SchuelerZeitraeume" und "SchuelerAusbildung"

Das Feld `Ausbildung` ist in der Tabelle `Schueler` weiterhin vorhanden, bildet aber nicht mehr die aktuelle "Ausbildung" ab.

!!! warning "Wichtig"

     Bitte löschen Sie die Verknüpfungen zwischen der Tabelle "Schueler" und der Tabelle "SchuelerAusbildung". 
     Setzen Sie stattdessen die Verbindungen zwischen der Tabelle "SchuelerZeitraeume" und der Tabelle "SchuelerAusbildung".

Die neue Verknüpfung muss wie folgt aussehen:

Tabelle und Feld|Art der Verbindung|Tabelle und Feld
--|--|--
SchülerZeitraeume| - |SchuelerAusbildung
Mandant|linke äußere Verknüpfung<br/>(left outer join)|Mandant
Ausbildung|linke äußere Verknüpfung<br/>(left outer join)|ID

![SchuelerAusbildung](/assets/images/berichte.anpassen/cr_fix_schuelerAusbildung.png)

#### Schueler

Die Felder folgenden Felder sind nicht mehr in der Tabelle "Schueler" zu finden, sondern wurden in die neue Tabelle "SchuelerFoerderungen" verschoben, da es sich jetzt um eine Liste von Fördermaßnahmen/Behinderung/Schwächen handelt.

* "SopaedFoerderungen"
* "Foerderschwerpunkt1"
* "Foerderschwerpunkt2"
* "Behinderung"

#### SchuelerKlassen

Wenn die Tabelle "SchuelerKlassen" in Berichten verwendet wurde, dann musste Sie mit den Feldern "Schueler", "Klasse", "Zeitraum" verknüpft werden. Diese Felder gibt es in der Tabelle nicht mehr, dafür gibt es das Feld "SchuelerZeitraumID". Die Tabelle wird dann aus der Tabelle "SchuelerZeitraeume" Feld "ID" verknüpft. Folgende Fehlermeldung könnten Sie in der Vorschau erhalten:

![SchuelerKlassen](/assets/images/berichte.anpassen/cr_error_msg3.png)

Die Verknüpfung wird wie folgt korrigiert:

![SchuelerKlassen](/assets/images/berichte.anpassen/cr_fix_schuelerKlassen.png)

Tabelle und Feld|Art der Verbindung|Tabelle und Feld
--|--|--
SchülerZeitraeume|-|SchuelerKlassen
Mandant|linke äußere Verknüpfung<br/>(left outer join)|Mandant
ID|linke äußere Verknüpfung<br/>(left outer join)|SchuelerZeitraumID

#### Empfohlene Verknüpfung

Eine Empfehlung finden Sie im Artikel ["Empfohlene Verknüpfung"](https://doc.kb.stueber.de/cr/verknuepfung.html) in unserer Knowledge-Base.

### 5. Test

Speichern Sie Ihre Änderungen und wählen Sie anschließend `F5` (oder rufen die Vorschau über das Symbol auf). Wird die Vorschau gefüllt (bei mehrseitigen Berichten bitte auch einmal blättern)? Dann ist der Bericht jetzt für Magellan 7 vorbereitet.

### Sollte es noch weitere Probleme geben

#### arithmetic exception, numeric overflow

Sie erhalten diese Meldung? Dann folgen Sie bitte dem  Punkt der Anleitung: [2. Datenbankverbindung aktualisieren](https://doc.magellan.stueber.de/schulverwaltung/update/berichte_anpassen/#2-datenbankverbindung-aktualisieren)

![Meldung](/assets/images/berichte.anpassen/berichte.anpassen2.png)

#### Keine Datenbankverbindung möglich

Wir empfehlen für die Änderung der Berichte auf eine lokale Magellan 7-Installation zuzugreifen.

#### Die Vorschau lädt und lädt

Wenn Sie alle vorstehenden Punkte befolgt haben, die Vorschau aber noch immer dauerhaft lädt, ist vermutlich eine vergessene Verknüpfung in einem Unterbericht die Ursache.

Die Übersicht der Verknüpfungen gilt für den jeweils gewählten Bericht oder Unterbericht. Bitte schauen Sie, ob es Unterberichte in Ihrem Bericht gibt und überprüfen Sie bitte die Verknüpfungen unter `Datenbank > Datenbank-Assistent > Unterkarte Verknüpfungen` während der Unterbericht geöffnet ist.

#### Operation noch nicht implementiert

Erscheint die Meldung in der Magellan-Vorschau oder in der Crystal Reports-Vorschau?

Dann handelt es sich vermutlich um einen Bericht, der den Inhalt eines Feldes als Barcode darstellen soll. Für die Darstellung als Barcode wird die Schriftart [Code EAN 13](https://download.stueber.de/bin/de/common/fonts/ean13.ttf) verwendet. Die Schriftart fehlt auf Ihrem Rechner oder ist nicht korrekt installiert, bitte laden Sie sie herunter und installieren Sie diese Schriftart per Doppelklick auf dei Datei neu!

!!! tip "Tipp"

    Klappt die Vorschau von Berichten mit Barcode direkt nach dem MAGELLMA-Update nicht? 
    Bitte starten Sie Ihren Rechner einmal neu, anschließend sollte die Schriftart, die zur Anzeige von Barcodes verwendet wird, verfügbar sein.

#### Die Tabelle wurde nicht gefunden

In Crystal Reports klappt die Vorschau, Magellan meldet aber "Die Tabelle wurde nicht gefunden"?

![Meldung "Die Tabelle wurde nicht gefunden"](/assets/images/berichte.anpassen/berichte.anpassen9.png)

Dann öffnen Sie bitte den Bericht in Crystal Reports und stellen sicher, dass unter `Datei > Berichtsoptionen > Allgemeine Einstellungen` das Häkchen vor `Beim ersten Regenerieren überprüfen` **nicht** aktiviert ist.

!!! danger "Achtung"

    Diese Einstellungen muss bitte für den Bericht **und auch für alle Unterberichte** deaktiviert sein.

![Dieses Häkchen darf NICHT aktiviert sein](/assets/images/berichte.anpassen/berichte.anpassen8.png)

#### Failed to save document

Manche Berichte lassen sich nicht speichern, auch nicht über `Speichern unter`.
Eine mögliche Ursache dafür kann sein, dass ein Unterbericht im Detailbereich eingebunden wurde. Ändert man das, lässt sich der Bericht auch normal speichern.

![Failed to save document](/assets/images/berichte.anpassen/cr.nicht.speicherbar.jpg)

#### Schüler wird wiederholt angezeigt

  Sollten Sie in einem Zeugnis das Problem haben, dass der in Magellan in der Vorschau geladene Schüler beim Test der Vorschau in Crystal Reports immer wieder nacheinander gezeigt wird, kontrollieren Sie bitte die Verknüpfungen der Tabellen `KlassenZeitraeume` und `Klassen`.

![Verknüpfung](/assets/images/berichte.anpassen/berichte.anpassen10.png)

#### Der verkehrte Schüler wird angezeigt

  In einigen alten Berichten wurde die Tabelle `SchuelerKlassen` statt der Tabelle `KlassenZeitraeume` verwendet.
  Das die Verknüpfung nicht stimmt, kann man z.b. daran bemerken, dass ein verkehrter Schüler statt des ausgewählten Schülers angezeigt wird.

Was können Sie tun:

1. Kontrollieren, ob bereits Felder aus `SchuelerKlassen` genutzt wurden.
2. Wenn nicht, dann die Verknüpfungen lösen und `KlassenZeitraeume` einfügen.
3. Verknüpfen wie in der Abbildung.

![KlassenZeitraeume verknüpfen](/assets/images/berichte.anpassen/04.png)

#### Es werden mehr als die ausgewählten Datensätze gezeigt

Problem: Sie wählen in Magellan nur wenige Datensätze aus um die Auswahltabellen zu füllen (Drucken > Vorschau), in der Crystal Reportsvorschau werden aber dennoch immer alle Datensätze aufgerufen.

Eine mögliche Ursache kann folgender Punkt sein:

CR optimiert vor dem Aufruf des Berichtes selbständig (und nicht unterdrückbar) die Abfrage. Gerade bei sehr einfachen Berichten kann das eigenständige Optimieren zu merkwürdigen Nebeneffekten führen. Was hilft, ist ein Feld im oberen Bereich des Berichtes einzufügen und dann zu unterdrücken.

![Feld einfügen und ausblenden](/assets/images/berichte.anpassen/01.png)
