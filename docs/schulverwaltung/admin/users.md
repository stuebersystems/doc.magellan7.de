# Benutzerverwaltung

[1]:/assets/images/magellan.administrator/008.png "Benutzer duplizieren"   

Die Benutzerverwaltung ist das Werkzeug des Administrators, um:

* den Benutzern allgemeinen Zugriffsrechte zuzuweisen,
* Spezielle Rechte zur Nutzung von MYMAGELLAN zuzuweisen und
* das MAGELLAN-Logbuch auszuwerten

!!! info "Hinweis"

	Benutzerdaten werden mit der Datenbankdatei abgespeichert.  Die Passwortdaten der Benutzer werden verschlüsselt in einer zweiten Firebird-Datenbank gespeichert, die bei der Installation von Firebird mit angelegt wurde.

## "sysdba" und "dbadmin"

Standardmäßig sind die Benutzer mit der Kennung "sysdba" und "dbadmin" in der Datenbank hinterlegt. Der "sysdba" hat bis zur Version 9 bei der ersten Installation von Firebird das Passwort "masterkey" hinterlegt. Für den "dbadmin" müssen Sie ein Passwort gezielt vergeben, dazu später mehr.

Mit diesen Standardkennung sind volle Administrationsrechte verbunden mit folgendem Unterschied:

Der Firebird-Datenbankserver kennt zwei Administratoren Benutzer, "sysdba" und "dbadmin". Der sysdba hat für alle Datenbanken, die auf einem Firebird-Server laufen, das höchste Administrationsrecht. Der "dbadmin" hat für eine Datenbank (oder bei mehren Zuweisungen auch mehrmals) die gleichen Rechte wie der "sysdba".

Um den "sysdba" zu verwenden sind keine weiteren Schritte nötig, wir empfehlen nur das Passwort zu ändern. Diese Möglichkeit finden Sie im MAGELLAN Administrator unter `Benutzerverwaltung > Administratoren > Doppelklick auf die Zeile für den "sysdba"`. Vergeben Sie hier bitte ein 8-stelliges Passwort, vermeiden Sie bitte Umlaute und ß.

![Passwort für den sysdba ändern](/assets/images/magellan.administrator/014.png)

### Account "dbadmin" vorbereiten

Möchten Sie den "dbadmin" verwenden sind  zwei Schritte notwendig:

 1. Weisen Sie ein Passwort zu.
 2. Synchronisieren Sie die Zugriffsrechte aus dem Untermenü `Administratoren` heraus.

Um das Passwort zu setzen, rufen Sie MAGELLAN Administrator auf und melden sich bitte als "sysdba" an der Datenbankverbindung an, für die Sie den "dbadmin" einsetzen möchten.
Wechseln auf `Benutzerverwaltung > Administratoren`und Doppelklicken auf die Zeile für den "dbadmin". Vergeben Sie hier bitte ein 8-stelliges Passwort, vermeiden Sie bitte Umlaute und ß.

![Passwort für den dbadmin ändern](/assets/images/magellan.administrator/015.png)

Anschließend müssen dem "dbadmin" die Rechte des "sysdba" für die Datenbank übertragen werden, an der Sie sich angemeldet haben. Das erreichen Sie, indem Sie das Zugriffsrechte synchronisieren von der Unterkarte "Administratoren" aus starten. Es erscheint das nachfolgende Fenster:

![Passworte angeben](/assets/images/magellan.administrator/016.png)

Tragen Sie das Passwort für den "sysdba" und für den "dbadmin" ein und klicken Sie auf "Testen". Stimmen die Passworte, wird die "Weiter" aktiv.

![Testen](/assets/images/magellan.administrator/017.png)

Lösen Sie die Synchronisation mit "Fertigstellen" aus, im Anschluss können Sie den Account verwenden.

![Rechte vom sysdba auf den dbadmin übertragen](/assets/images/magellan.administrator/018.png)

## Registerkarte „Benutzerliste“

In der Benutzerliste ist jeder Benutzer ist durch seine Kennung, den Nachnamen, Vornamen, sein Lehrerkürzel (optional), seinen Mandanten, sein Kennwort und seinen Status definiert. Für jeden Benutzer können Sie seine Rechte in der Schulverwaltung, Bibliotheks & Lernmittel und für MYMAGELLAN, die dezentrale Notenverwaltung, festlegen.

Einen neuen Benutzer können Sie über die Schaltfläche `Hinzufügen` anlegen, einen bestehenden durch Doppelklick auf den Benutzer auf der Karte „MAGELLAN Benutzerliste“ bearbeiten. Für bereits angelegte Benutzer können Rechte exportiert, angepasst und wieder importiert werden. Zum Beispiel, um einer Gruppe von Benutzer schnell und einfach ein neues Recht zu zuweisen oder den Teilnehmern am MYMAGELLAN-Verfahren einen neuen Ablagepfad für die mym-Datei zu hinterlegen.

Dafür stehen in der oberen Menüleiste der Benutzerverwaltung auf der rechten Seite drei Schaltflächen zur Verfügung.
![Dies ist die Liste der Benutzer in der Benutzerverwaltung](/assets/images/users_benutzerliste.png)

## Benutzer exportieren und importieren

Mit Hilfe eines Assistenten werden alle bereits angelegten Benutzer in eine CSV-Datei exportiert. Bitte geben Sie einen Speicherort und einen Dateinamen an, die Endung „.csv“ wird automatisch ergänzt.

![Schaltflächen in der oberen Menüleiste](/assets/images/magellan.administrator/users_benutzer.exportieren.png)

![Die erzeugte Datei kann mit Excel geöffnet und bearbeitet werden.](/assets/images/magellan.administrator/users_benutzer.exportieren1.png)

!!! info "Hinweis"

	Auf diesem Weg können keine Benutzer neu angelegt oder Passworte geändert werden, sondern es können für bereits angelegte Benutzer Werte geändert.

In der Datei sind Kopfzeilen und bereits erfasste Einstellungen. Diese Werte können ergänzt oder verändert werden:

Spaltentitel | Mögliche Werte
-------------------------- | --------------
Kennung | Enthalten ist die Benutzerkennung, dieser Wert ist nicht veränderbar
Status | Für die Teilnahme am MYMAGELLAN-Verfahren: Teilnehmer; (Kein Teilnehmer)
Schulverwaltung | Für den Zugriff auf MAGELLAN: (Kein Zugriff), Schulverwaltung 1, Schulverwaltung 2, Sekretariat 1, Sekretariat 2, Kollegium 1, Kollegium 2, Kollegium 3, Kollegium 4, Gast 1, Gast 2, Statistik-Administrator
Bibliothek/Lernmittel | (Kein Zugriff), Schulleitung, Bibliothekar, Kollegium, Gast
Medienkatalog | <Alle Kataloge> oder selbst im Schlüsselverzeichnis angelegte Kataloge (Modul Bibliothek/Lernmittel > Verzeichnisse > Schlüsselverzeichnis Kataloge)
MYMAGELLAN-Datei | Tragen Sie hier den Speicherpfad und den Dateinamen für die MYMAGELLAN-Datei ein, die später mit dem Modul MYMAGELLANCenter erzeugt wird, zum Beispiel:C:\MAGELLAN 6\MYMAGELLAN\Lehrer1.mym
Haushalt/Inventar | (Kein Zugriff), Schulleitung, Sekretariat, Gast
Verzeichnisse | Für die Editierbarkeit von Schlüsselverzeichnissen in MAGELLAN: Nicht editierbar, Editierbar
Aktiv | Ja, Nein, Kennzeichnung des Benutzers als Aktiv oder Inaktiv
Mandanten | Für das Benutzerrecht Mandanten-Administrator: Ja, Nein
Import/ Export | Für den Im- und Export: Ja, Nein
Drucken | Ja, Nein
Dokumente | Zum Zugriff auf die Dokumentenverwaltung: Ja, Nein
Berufsschule | Ermöglicht den Zugriff des Benutzers auf den Menüpunkt Berufsschule. Mögliche Werte: Editierbar, Nicht editierbar
Berufsschule-Prüfungsnoten | Regelt die Sichtbarkeit der Spalten Prüfungsnote und Prüfungsnote (Kontrolle) im Menüpunkt Berufsschule Unterkarte Matrix. Mögliche Werte sind: Kein Recht, Nur Prüfungsnote (Kontrolle), Prüfungsnote + Prüfungsnote (Kontrolle)

Anschließend: Klicken Sie auf die Schaltfläche `Benutzer importieren` um die veränderte Benutzerliste wieder zu importieren. Bitte führen Sie zum Abschluss den Punkt `Datenbankpflege > Datenbank überprüfen > Zugriffsrechte synchronisieren` aus.

## Export nach Excel/

Über diese Schaltfläche können Sie eine Excelliste oder eine/-Datei mit den Benutzerdaten erzeugen. Bitte beachten Sie, dass diese Dateiformate nicht wieder direkt eingelesen werden können, dafür nutzen Sie bitte die Schaltfläche `Benutzer exportieren`.

## einen neuen Benutzer anlegen

Um Benutzer anzulegen müssen Sie sich mit dem Account des `sysdba` anmelden. 
Einen neuen Benutzer erzeugen Sie über die Schaltfläche `Neuer Datensatz` oben links in der Menüleiste. 

![Einen neuen MAGELLAN-Benutzer anlegen](/assets/images/magellan.administrator/neuer.benutzer.png)

### Registerkarte „Allgemein“

Feld|Anmerkung
--|--
Benutzer aktiv|Der Haken ist beim Neuanlegen automatisch aktiviert. Sie haben über dieses Häkchen die Möglichkeit Benutzer vorübergehend zu deaktivieren, zum Beispiel während der Elternzeit
Mandant|Ist in Ihrer Datenbank nur ein Mandant, wird automatisch dieser Mandant vorbelegt. Die Rechte, die Sie im nachfolgenden gewähren, gelten ausschließlich für den hier gewählten Mandanten.
Lehrer|Ist ein Mandant ausgewählt, wird die Lehrerliste gefüllt. Für Kollegiumsrechte ist es notwendig auf einen Lehrer in der Datenbank zu verweisen. MAGELLAN benötigt diese Information um zum Beispiel die Schüler des Lehrers identifizieren zu können (mit Kollegiumsrechten kann man z.B. nur Zeugnisnoten für eigene Schüler einpflegen), oder auch um die eigene Lehrerzeile im Menü Lehrer einzublenden. Für Benutzer denen andere Rechtegruppen (z.B. Sekretariatsrechte)zugewiesen werden sollen, muss nicht nichts gewählt werden.
Nachname|Ist im Feld Lehrer ein Datensatz gewählt worden, wird das Feld automatisch befüllt, anderenfalls tippen Sie hier bitte den Nachnamen ein.
Vorname|Ist im Feld Lehrer ein Datensatz gewählt worden, wird das Feld automatisch befüllt, anderenfalls tippen Sie hier bitte den Vornamen ein.
E-Mail| Für Benutzer, die keinem Lehrerdatensatz aus MAGELLAN zugeordnet wurden, kann das Feld editiert werden. Für Benutzer, die in MAGELLAN einem Lehrer zugewiesen sind, wird hier die Adresse aus `Lehrer > Daten1 > E-Mail` gezeigt. Die Adresse kann für Umsteiger von Version 9 auf eine höhere Version über einen Assistenten unter `Extras > E-Mail übernehmen` übertragen werden. Wird im Anschluss die Adresse in MAGELLAN verändert, aktualisiert sich die Adresse auf für den verbundenen Benutzer. Die Einträge der E-Mail-Adresse können Sie für alle Benutzer in der Liste der Benutzerverwaltung sehen.
Kennwort ändern|Mit Hilfe dieses Häkchens können Sie für bereits angelegte Benutzer ein neues 8-stelliges Passwort vergeben.
Kennwort|Bitte vergeben Sie ein 8-stelliges Passwort, bitte verzichten Sie auf Umlaute oder ß.
Bestätigung|Tragen Sie zur Bestätigung bitte das Passwort erneut ein.
Kennwort als MYMAGELLAN-Kennwort übernehmen|Das hier vergebene Passwort kann auch später als Passwort für die MYMAGELLAN-Datei des Benutzers übernommen werden.

![Legen Sie hier die Grunddaten des Benutzers fest](/assets/images/magellan.administrator/benutzer.anlegen.png)

!!! info "Hinweis"

	Die Kürzel der Lehrer dürfen keine Umlaute oder „ß“ enthalten. Bitte passen Sie die Kürzel der Kollegen vorab in MAGELLAN an. 
     Sollten Sie bereits einen Benutzerzugang für einen Kollegen mit einem Umlaut im Kürzel angelegt haben, genügt es nicht das Kürzel in MAGELLAN unter Lehrer zu ändern. Löschen Sie bitte den Benutzer unter `MAGELLAN Administrator > Benutzerverwaltung`, ändern anschließend das Kürzel in MAGELLAN unter `Lehrer > Daten1 > Kürzel` und legen abschließend den Benutzerzugang für den Lehrer erneut an.
      Wenn Sie unter Kennwort das Benutzerkennwort eintragen, kann dieses Kennwort gleichzeitig als MYMAGELLAN-Kennwort übernommen werden, wenn Sie das Optionsfeld `Kennwort als MYMAGELLAN-Kennwort übernehmen` markiert haben.Geben Sie bitte ein achtstelliges Passwort ohne Sonderzeichen für den neuen Nutzer an.

## Registerkarte „Rechte“

![Legen Sie die Rechte für den Benutzer fest](/assets/images/magellan.administrator/users_rechtekarte.png)

### Allgemeine Rechte

Rechtegruppe | Rechte
-------------------------- | ------
Mandanten-Administrator | Administratorenrechte, aber kein umfasssender Zugriff auf den MAGELLAN-Administrator, dafür aber Zugriff auf das MYMAGELLAN Center für den jeweiligen Mandanten. Zusätzlich können für bereits angelegte Benutzer des Mandanten die Rechte für MyMAGELLAN (Teilnehmer oder nicht, MyMAGELLAN-Passwort, Ablagepfad für die mym-Datei editiert) werden. <br/>Das Verwenden dieses Rechtes erhöht alle Schulverwaltungsrechte. <br/>Ausnahme: Kann der Nutzer mit seiner zugeordneten Rechtegruppe (z.B. einem Kollegiumsrecht) nur seinen eigenen Datensatz im Lehrermenü betrachten, bleibt diese Einschränkung erhalten.
Import/Export | Zusätzlich zum Schulverwaltungsrecht kann die Möglichkeit des Importes und Exportes (Seriendruck, Excelexport, Schuldatentransferformat) gesteuert werden.
Drucken | Zusätzlich zum Benutzerrecht kann das Drucken ermöglicht werden
Dokumentenverwaltung | Zusätzlich zum Benutzerrecht die Möglichkeit auf die Dokumentenverwaltung zuzugreifen
Verzeichnisse|Je Benutzer kann für die Schulverwaltung  festgelegt werden, ob der Benutzer die Verzeichnisse in MAGELLAN zu editieren. Das Menü `Extras > Schlüsselverzeichnisse` wird für Benutzer in MAGELLAN ausgeblendet. 
Berufsschule | Regelt zusätzlich zum Benutzerrecht den Zugriff des Nutzers auf den Menüpunkt Berufsschule
Berufsschule-Prüfungsnoten | Regelt zusätzlich zum Benutzerrecht die Sichtbarkeit der Spalten Prüfungsnote und Prüfungsnote (Kontrolle) im Menüpunkt Berufsschule auf der Registerkarte Matrix
Administratorenrechte | Keine Zugriffseinschränkungen (Administratorenkennung mit Benutzer: sysdba)

### Rechte für die Schulverwaltung

Rechtegruppe | Rechte
----------------------- | ------
Schulleitung 1 | * Zugriff auf alle Daten außer auf die Datenbankstruktur und die Benutzerverwaltung<br/>* Keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich
Schulleitung 2 | * Wie Schulleitung 1, aber mit der Einschränkung, keine Fächer oder Noten der Schüler zu ändern<br/>* Keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich
Sekretariat 1 | * Zugriff auf alle Daten außer auf die Datenbankstruktur und Benutzerverwaltung<br/>* Keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich
Sekretariat 2 | * Wie Sekretariat 1 aber mit folgenden Einschränkungen: Kein Zugriff auf `Zeugnis > Fächer/Leistungen/Details/Bemerkungen und Formulare/Arbeits- und Sozialverhalten`<br/>keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich
Kollegium 1 | * Stammdaten der Schüler können gelesen, aber nicht verändert werden<br/>* Noten der Schüler, die unterrichtet werden, dürfen als Fachlehrer, Tutor, Klassenleiter1 oder Klassenleiter2 erfasst bzw. geändert werden <br/>* Weitere Zeugnisdaten können als Tutor, Klassenleiter1 oder Klassenleiter2 verändert werden<br/> Ansonsten bestehen nur Leserechte.<<br/>* Menü „Lehrer“ zeigt nur die eigenen Personaldaten<br/>* Kollegiumsrechte müssen zugewiesen sein, damit man MYMAGELLAN-Dateien bearbeiten kann. Welche Voraussetzungen hierfür des Weiteren gegeben sein müssen, erfahren Sie im Abschnitt „Das MYMAGELLAN Center“ unter „Voraussetzungen“.<br/>* keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich<br/>**Voraussetzung:** Der Benutzer muss in MAGELLAN im Menü `Lehrer`angelegt werden, unter `Benutzerverwaltung > Rechte` muss auf den Lehrerdatensatz verwiesen werden.
Kollegium 2 | * Wie Kollegium 1, als Tutor, Klassenleiter1 oder Klassenleiter2 zusätzlich auch Laufbahndaten und Fehlzeiten des Schülers editierbar<br/>**Voraussetzung:** Der Benutzer muss in MAGELLAN im Menü `Lehrer`angelegt werden, unter `Benutzerverwaltung > Rechte` muss auf den Lehrerdatensatz verwiesen werden.
Kollegium 3 | * Wie Kollegium 2, aber keine Zeugnisformulare der Schüler editierbar<br/>**Voraussetzung:** Der Benutzer muss in MAGELLAN im Menü `Lehrer`angelegt werden, unter `Benutzerverwaltung > Rechte` muss auf den Lehrerdatensatz verwiesen werden.
Kollegium 4 | * Wie Kollegium 2, aber keine Zeugnisformulare und Zeugnisbemerkungen editierbar<br/>**Voraussetzung:** Der Benutzer muss in MAGELLAN im Menü `Lehrer`angelegt werden, unter `Benutzerverwaltung > Rechte` muss auf den Lehrerdatensatz verwiesen werden.
Kollegium 5 | * Wie Kollegium 2, als Tutor, Klassenleiter1 oder Klassenleiter2 zusätzlich auch das Abiturmenü für alle Schüler editierbar<br/>**Voraussetzung:** Der Benutzer muss in MAGELLAN im Menü `Lehrer`angelegt werden, unter `Benutzerverwaltung > Rechte` muss auf den Lehrerdatensatz verwiesen werden.
Gast 1 | * Leserechte<br/>*  Schreibzugriff ist nicht möglich <br/>* Menü „Lehrer“ zeigt nur die eigenen Personaldaten<br/>* keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich<br/>**Voraussetzung:** Der Benutzer muss in MAGELLAN im Menü `Lehrer`angelegt werden, unter `Benutzerverwaltung > Rechte` muss auf den Lehrerdatensatz verwiesen werden.
Gast 2 | * Leserechte <br/>* Schreibzugriff ist nicht möglich <br/>* Menü „Lehrer“ zeigt die Personaldaten aller Lehrer<br/>* keine Anmeldung am Modul MAGELLAN ADMINISTRATOR möglich
Statistik-Administrator | Innerhalb der Schulverwaltung wie `Schulleitung 1` zusätzlich können die folgenden Punkte ausgeführt werden: <br/> * im MAGELLAN ADMINISTRATOR „Schlüsselverzeichnisse importieren“<br/> * Abgleich zwischen MAGELLAN und daVinci

### Bibliotheksrechte

Rechtegruppe |	Rechte
------------ | ------
Bibliothekar |	Zugriff auf alle bereits bestehenden Daten der Bibliotheksverwaltung<br/><br/>**Wichtig:**<br/>Soll der Bibliothekar auch das Recht haben Lehrer als Ausleiher hinzufügen, muss dem Nutzer für die Schulverwaltung das Recht `Gast2` gewährt werden.
Schulleitung | wie Bibliothekar, aber kein Zugriff auf die Optionsunterkarten: Ausleihe, Quittung, Mahnwesen und Dokumente
Kollegium | wie Schulleitung
Gast | nur Leserechte

!!! info "Hinweis"

	Beim Anlegen der Kennung bitten wir Sie, auf Abkürzungen wie „Do“ und „If“ zu verzichten, da diese Kürzel gleich lautend mit Programmierbefehlen sind und von Firebird fehl interpretiert werden. Es gibt noch weitere so genannte „reservierte“ Worte, die Sie in der Dokumentation [„MAGELLAN-Scripting“](https://doc.magellan7-toolbox.stueber.de/scripting/) in Kapitel „Die Skriptsprache“ nachschlagen können.
Die Benutzer können ihr Passwort in MAGELLAN unter `Datenbank > Kennwort ändern...` selbst anpassen. Dafür werden mindestens 8 Zeichen erwartet. Sollte die Schaltfläche `Kennwort ändern...` inaktiv bleiben, ist der Benutzer als Datenbankadministrator („sysdba“) angemeldet. Dieses Kennwort kann nur im MAGELLAN-Administrator verändert werden.

## Registerkarte „MYMAGELLAN“

![Sie können auf dieser Karte festlegen, ob der Benutzer Noten mit MYMAGELLAN erfassen darf, ein MYMAGELLAN-Kennwort besitzt und den späteren Speicherort seiner MYMAGELLAN-Datei angeben.](/assets/images/magellan.administrator/users_mymagkarte.png)

Alle Angaben der Benutzer zu MYMAGELLAN werden aus Gründen der Übersichtlichkeit unter dem Reiter `MYMAGELLAN` aufgelistet. Markieren Sie einen der Benutzer, werden für ihn im unteren Bereich zusätzlich die MAGELLAN-Rechte eingeblendet.

![Hier sehen Sie eine Übersichtsliste alle Teilnehmer von MYMAGELLAN.](/assets/images/magellan.administrator/users_mymag.liste.png)

## Passworte gesammelt vergeben und E-Mail-Adressen

### E-Mail-Adressen

Ab Version 10 kann je Benutzerkonto eine E-Mail-Adresse gespeichert werden. Für Benutzer, die mit einem Lehrerdatensatz aus MAGELLAN verknüpft sind, ist die Adresse nicht frei eingebbar, es wird der Eintrag aus `Lehrer > Daten 1 > E-Mail` verwendet.
Für neu angelegte Benutzer wird diese Adresse automatisch übernommen, für bestehende Benutzer kann die Adresse mit dem Assistenten unter `Extras > E-Mail übernehmen` übertragen werden. Ist die Adresse für den Benutzer einmalig übertragen worden, wird auch jede Änderung der Adresse in MAGELLAN übertragen.

![`Extras > E-Mail übernehmen`](/assets/images/magellan.administrator/010.png)

Für Benutzer, die keinem Lehrer in MAGELLAN zugewiesen sind, kann manuell eine E-Mail-Adresse hinterlegt werden. Sie können das E-Mail-Feld unter `Benutzerverwaltung > Doppelklick auf den Benutzer > Allgemein` editieren. Für Benutzer, die einem Lehrerdatensatz zugewiesen sind, ist das Feld nicht auf diesem Weg editierbar.

Alle Einträge sehen Sie in der Benutzerliste in der Spalte `E-Mail`. 

![Spalte E-Mail in der Liste der Benutzer](/assets/images/magellan.administrator/011.png)

## Kennworte erzeugen

Sie können einer Gruppe von in der Liste der Benutzerverwaltung markierten Benutzern mit dem Assistenten unter `Extras > Kennwörter erzeugen` gesammelt ein neues Kennwort zuweisen.
Der Assistent erwartet die Eingabe eines Speicherorts und eines Dateinamens für eine CSV-Datei, die im Moment des Erzeugens der neuen Kennworte, dieses in die Datei speichert. Zusätzlich wird die Kennung des Nutzers und, wenn vorhanden, die E-Mail-Adresse des Nutzers in die Datei gespielt. Diese Datei kann als Grundlage für die Verteilung der Zugangsdaten verwendet werden.
Ein erneuter Durchlauf des Assistenten erzeugt neue Kennworte, sollte ein Nutzer sein Kennwort nicht zur Hand haben, gibt es nicht die Möglichkeit das alte Kennwort erneut zu erzeugen, es kann nur ein neues Kennwort erzeugt werden.
Wenn ein Nutzer sich mit dem neuen Kennwort an MAGELLAN anmeldet, kann er unter `Datenbank > Kennwort ändern` ein eigenes Kennwort vergeben. 

![`Extras > Kennwörter erzeugen`](/assets/images/magellan.administrator/009.png)

## Benutzer duplizieren

Arbeiten mehrere Schulen auf einer Datenbank, kann es notwendig sein, dass Benutzer Zugriff auf mehrere Mandanten haben, beispielsweise wenn Verwaltungsmitarbeiter übergreifend arbeiten.
Ein duplizierter Benutzer kann auf mehr als einen Mandanten die identischen Zugriffsrechte haben und auch aus der MAGELLAN-Oberfläche heraus auf einen anderen Mandanten, für den ihm das Recht gewährt wurde, umschalten. 

### Nicht für Lehreraccounts sinnvoll

Das Duplizieren ist nur für Benutzeraccounts möglich, die nicht Noten erfassen sollen. Wenn Noten für Schüler erfasst werden sollen, wird immer ausgewertet, welcher Lehrer es genau ist - dabei wird auf die Lehrerliste des Mandanten zugegriffen. 
	
Die Lehrer im Menü `Lehrer` haben eine eindeutige ID und sind immer genau einem Mandanten zugeordnet. Legen Sie den Lehrer in einem anderen Mandanten an, kann zwar das gleiche Kürzel verwendet werden, es ist aber technisch gesehen ein anderer Lehrer mit einer anderen ID.

Duplizieren Sie den Account des Lehrers, kann er sich an dem anderen Mandanten anmelden, er kann aber für die Noteneingabe nicht einem Lehrer im Menü ``Lehrer`` zugeordnet werden.

Sollte Sie die Situation haben, dass ein Lehrer in mehr als einem Mandanten Ihrer Datenbank für Schüler Noten vergeben soll, müssen Sie ihn je Mandant anlegen. Sie könnten dafür das identische Kürzel und auch das identische Passwort vergeben, ein Umschalten zwischen den Mandanten ist hier dann aber nicht sinnvoll. Der Lehrer muss sich um im nächsten Mandanten Notenwerte zu ändern an dem anderen Mandanten neu anmelden.

### So geht's

Um eine Account zu duplizieren wählen Sie im MAGELLAN Administrator das Menü ``Benutzerverwaltung`` Unterregister ``Extras`` aus, markieren in der Benutzerliste den gewünschten Benutzer und klicken oben links auf `Benutzer duplizieren`. Wählen Sie im Fenster den gewünschten weiteren Mandanten aus und bestätigen Sie. Die Benutzerzeile wird dupliziert mit einem neuen Eintrag in der Spalte `Mandant`.
Der duplizierte Benutzer kann sich jetzt mit den identischen Rechten am zweiten Mandanten anmelden und auch ggfs. aus der MAGELLAN-Oberfläche im Fenster `aktueller Mandant` zwischen den Mandanten wechseln.
  
[![Benutzer duplizieren][1]][1]


