Dieses Kapitel ist im Aufbau!

[2]:/assets/images/enbrea.leistungen/02.png
[4]:/assets/images/enbrea.leistungen/04.png
[5]:/assets/images/enbrea.leistungen/05.png
[6]:/assets/images/enbrea.leistungen/06.png
[7]:/assets/images/enbrea.leistungen/07.png
[9]:/assets/images/enbrea.leistungen/09.png
[10]:/assets/images/enbrea.leistungen/10.png
[13]:/assets/images/enbrea.leistungen/13.png
[14]:/assets/images/enbrea.leistungen/14.png
[17]:/assets/images/enbrea.leistungen/17.png
[18]:/assets/images/enbrea.leistungen/18.png
[20]:/assets/images/enbrea.leistungen/20.png
[21]:/assets/images/enbrea.leistungen/21.png
[22]:/assets/images/enbrea.leistungen/22.png
[24]:/assets/images/enbrea.leistungen/24.png
[29]:/assets/images/enbrea.leistungen/29.png
[31]:/assets/images/enbrea.leistungen/31.png
[32]:/assets/images/enbrea.leistungen/32.png
[33]:/assets/images/enbrea.leistungen/33.png
[34]:/assets/images/enbrea.leistungen/34.png
[35]:/assets/images/enbrea.leistungen/35.png
[36]:/assets/images/enbrea.leistungen/36.png

# ENBREA Leistungen

Dieser Bereich dient als Grundlage zum Erfassen von Daten, die in sogenannten komplexen Zeugnisberichten ausgegeben werden.

Im Unterschied zu einfachen Zeugnissen sind hier auch noch Leistungen je Fach weiter unterteilbar, es sind verschiedene Notensysteme möglich.

!!! warning "Wichtig"

    Bitte schauen Sie vorab im Modul `MAGELLAN BERICHTE` nach, ob diese Ansicht von Ihrem Zeugnis verwendet wird.

[![Komplexer Zeugnisbericht, Beispiel][33]][33]

## Funktionalitäten aktivieren

Um die Funktionalitäten zu aktivieren, setzen Sie bitte das Häkchen unter `Datenbank > Optionen > ENBREA Funktionen aktivieren`.

![Aktivieren Sie das Häkchen!](/assets/images/enbrea.leistungen/01.png)

## Schlüsselverzeichnisse

Um Fächer und deren Kompetenzbereiche gemäß Zeugnisvorlage in MAGELLAN zu erfassen, müssen Sie folgende Schlüsselverzeichnisse unter `Extras > Schlüsselverzeichnisse` befüllen.

* `Bewertungsprofile`
* `Notensysteme`
* `Notentypen`

Folgender Auszug einer Zeugnisvorlage für das Fach "Mathematik" soll uns als Beispiel für die Dateneingabe in MAGELLAN dienen:

[![Beispiel für ein Zeugnis][2]][2]

### Bewertungsprofile

Öffnen Sie zunächst das `Schlüsselverzeichnis > Bewertungsprofile` . Dieses Verzeichnis unterteilt sich in die Register:

* Bewertungsprofile
* Bewertungsgruppen
* Bewertungseinträge

[![Beispiel für `Schlüsselverzeichnis > Bewertungsprofile`][17]][17]

Die Bewertung eines Faches wird hier wie folgt differenziert:

[![Differenzierung des Faches Mathematik][18]][18]

#### Bewertungsprofile > Bewertungsprofile

[![Unterkarte Bewertungsprofile][4]][4]

Der Eintrag eines Wertes unter `Extras > Schlüsselverzeichnisse > Bewertungsprofile > Bewertungsprofile` entspricht im oberen Beispiel dem Eintrag "Mathematik". 

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel einer frei gewählten Kurzform für "Mathematik (01)", also für Mathe in der Klassenstufe 1.
Bezeichnung| freie Wahl
Konfiguration| Legen Sie hier die Beurteilung fest (im Beispiel für die Zeile "Mathematik"). <br/>Mögliche Werte: <br/>- keine Bewertung <br/>- Note <br/>- Beurteilung <br/>- Note und Beurteilung
Notensystem| zeigt die im `Schlüsselverzeichnis > Notensystem` angelegten Werte
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

!!! info "Hinweis"

    Weichen die Bewertungsprofile pro Klassenstufe ab, legen Sie hier für jedes Fach entsprechend der Klassenstufe ein Bewertungsprofil an (Mathematik (1), Mathematik (2) etc.). Zunächst genügen die Einträge in den Spalten "Kürzel" und "Bezeichnung". Klicken Sie auf das Symbol `Neue Zeile`. Es erscheint eine neue Zeile im Verzeichnis zur direkten Eingabe von Kürzel und Bezeichnung.

#### Bewertungsprofile > Bewertungsgruppen

[![Unterkarte Bewertungsgruppen][5]][5]

Der Eintrag eines Wertes unter `Extras > Schlüsselverzeichnisse > Bewertungsprofile > Bewertungsgruppen` entspricht im oberen Beispiel einem Eintrag unterhalb von "Mathematik", in diesem Beispiel den Einträgen:

* Zahlen und Operationen
* Raum und Form
* Größen und Messen
* Daten, Häufigkeit und Wahrscheinlichkeit

Ein Bewertungsprofil (hier: Mathematik) kann in beliebig viele Bewertungsgruppen unterteilt werden. 

[![Fach "Mathematik" mit diversen Bewertungsgruppen][35]][35]

Wie im Beispiel "indische Landeskunde" oder "Sport" kann es auch sein, dass es für ein Bewertungsprofil keine Bewertungsgruppe(n) gibt.

[![Fach "Indische Landeskunde" ohne Bewertungsgruppen][34]][34]

!!! tip "Tipp"

    Um für ein Fach eine Bewertungsgruppe anlegen zu können, müssen Sie auf der ersten Registerkarte das Bewertungsprofil (entsprechende Fach) markieren und anschließend auf die Unterkarte Bewertungsgruppen wechseln. Hier können Sie nun neue Einträge hinterlegen. Damit werden die Bewertungsgruppen genau einem Bewertungsprofil zugeordnet.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel einer frei gewähltn Kurzform für die "Zahlen und Optionen"
Bezeichnung| Eintrag entspricht im oberen Beispiel dem Eintrag "Zahlen und Operationen"
Konfiguration| Legen Sie hier die Beurteilung fest (im Beispiel für die Zeile "Mathematik"). <br/>Mögliche Werte: <br/>- keine Bewertung <br/>- Note <br/>- Beurteilung <br/>- Note und Beurteilung
Notensystem| zeigt die im `Schlüsselverzeichnis >  Notensystem` angelegten Werte
Position| gemeint ist die Zeugnisposition, bitte tragen Sie die Positionen entsprechend der Vorgaben/Vorlagen für ihr Zeugnis ein
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

#### Bewertungsprofile > Bewertungseinträge

[![Unterkarte Bewertungseinträge][6]][6]

Der Eintrag eines Wertes unter `Extras > Schlüsselverzeichnisse > Bewertungsprofile > Bewertungseinträge` entspricht im oberen Beispiel einem Eintrag unterhalb von "Zahlen und Optionen". Es kann unterhalb von "Zahlen und Optionen" auch mehrere Einträge geben. Jeder Bewertungseintrag ist einer Bewertungsgruppe zuzuweisen.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, einer frei gewähltn Kurzform für den Bewertungseintrag.
Bezeichnung| freie Wahl
Gruppe| Tragen Sie bitte eine Bewertungsgruppe ein
Notensystem| zeigt die im `Schlüsselverzeichnis > Notensystem` angelegten Werte
Position| gemeint ist die Zeugnisposition, bitte tragen Sie die Positionen entsprechend der Vorgaben für ihr Zeugins ein
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

### Notensysteme

[![`Schlüsselverzeichnis > Notensystem`][7]][7]

Öffnen Sie über `Extras > Schlüsselverzeichnisse > Notensysteme` das Verzeichnis der Notensysteme. Dieses ist in folgende Registerkarten unterteilt:

* Notensysteme
* Notensystem-Einträge

Innerhalb Ihrer Schule und bei komplexeren Zeugnisberichten kann es unterschiedliche Systeme zur Beurteilung geben: Noten, Punkte, Prozente, Tendenzen...
Diese Arten der Beurteilung (Notensysteme) werden mit den einzelnen Beurteilungswerten (Notensystem-Einträge) in diesem Schlüsselverzeichnis angelegt.

#### Notensysteme > Notensysteme

[![`Unterkarte Notensysteme`][7]][7]

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel zum Beispiel dem Eintrag "Tendenzen"
Bezeichnung| freie Wahl
Wertetyp| Mögliche Werte `Zahlen` oder `Texte`
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

#### Notensysteme > Notensystem-Einträge

[![`Unterkarte Notensystem-Einträge`][9]][9]

Wählen Sie auf der Unterkarte `Notensysteme` einen Wert aus, wechseln Sie anschließend auf die Unterkarte `Notensystem-Einträge` und erfassen Sie die dazugehörigen Einträge. Diese Abbildung zeigt die Notensystem-Einträge, die zum Notensystem Tendenzen aus unserem Beispiel gehören.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel dem Eintrag "Mathematik"
Bezeichnung| freie Wahl
Wertetyp| Mögliche Werte `Zahlen` oder `Texte`
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

!!! info "Hinweis"
    
    Nachdem die Notensysteme definiert wurden, müssen diese unter `Extras > Schlüsselverzeichnisse > Bewertungsprofile` pro definiertem Profil nachgepflegt werden.

[![Bewertungsprofile][36]][36]

### Notentypen

[![`Schlüsselverzeichnis > Notentypen`][10]][10]

In diesem Verzeichnis wird die Art der Bewertung (z.B. Zeugnisnote, mündliche Note) definiert. Diese Werte können später den Bewertungen der Kurse im Bereich `Klassen > Zeitraum > ENBREA-Leistungen > Leistungsprofile` zugeordnet werden, dazu kommen wir aber später noch.

## Kurse anlegen

Pro Klassen müssen Sie nun noch die jeweiligen Kurse und je Kurs die Leistungsprofile definieren.

Die Kurse legen Sie bitte im Bereich `Klassen > Zeiträume > ENBREA Leistungsprofile` über den Aufruf `Kurse definieren...` an.

[![Kurse definieren][13]][13]

Es öffnet sich das Dialogfenster zum Definieren der Kurse

[![Kurse definieren][14]][14]

Über das `+` Symbol kann ein neuer Kurs mit folgenden Informationen angelegt werden.

Spalte | Bedeutung
--|--
Aktion| je nach Aktion werden hier folgende Werte ausgegeben:<br/> - Neu anlegen:  über das `Plus` Symbol <br/>- Bearbeiten: über das `Plus` Symbol<br/> - Duplizieren - Duplizieren eines vorhandenen Kurses über `Kurs duplizieren`<br/> - Duplizieren mit Leistungsprofilen - Duplizieren eines vorhandenen Kurses mit Leistungsprofil über `Kurs mit Leistungsgprofil duplizieren` <br/> - Übergreifend verwenden
Fach| Auswahl aus dem `Schlüsselverzeichnis > Fächer`
Unterrichtsart|Auswahl aus dem `Schlüsselverzeichnis > Unterrichtsart`
Fachstatus|Auswahl aus dem `Schlüsselverzeichnis  > Fachstatus`
Lehrer|Auswahl aus der Menü `Lehrer` mit dem Status "Aktiv"
Schwerpunkt | Auswahl aus dem `Schlüsselverzeichnis > Fachschwerpunkt`
Niveau | Auswahl aus dem `Schlüsselverzeichnis  > Fachniveaus `
Kursnr.| Eingabe einer Kursnummer
Bilingual|Auswahl aus dem `Schlüsselverzeichnis > Kurssprachen`
Merkmal | Eingabe von Freitext

### Kurs duplizieren

Sie können auch Kurse im Zeitraum über den Aufruf `Kurs duplizieren` als Kurs in ihre gewählte Klasse übernehmen. Dieser Schritt empfiehlt sich, wenn Sie für eine Klasse 1a bereits Kurse definiert und diese auch für die Klasse 1b benötigen. Wählen Sie zunächst im unteren Bereich des Fenster den gewünschten Kurs und wählen dann in der Menüleiste des Fensters `Kurs duplizieren`.

[![Kurse duplizieren][20]][20]

!!! info "Hinweis"
    
    Sie können auch mehrere Kurse in einem Schritt duplizieren. Markieren Sie über `Strg + linke Maustaste` die gewünschte Kurse und wählen Sie dann den Aufruf `Kurs duplizieren`.

### Kurse mit Leistungprofil duplizieren

### Übergreifend verwenden

Findet hier aktuell noch keine Verwendung.

## Leistungsprofile anlegen

Nachdem Sie die Kurse definiert haben, legen Sie pro Fach die Leistungsprofile an.

Diese legen Sie im Bereich `Klassen > Zeiträume > ENBREA Leistungsprofile` über den Aufruf `Leistungsprofile definieren...` an.

[![Aufruf "Leistungsprofile definieren..."][21]][21]

Über das `Plus Symbol` wird eine neue Zeile angelegt werden. Folgende Informationen müssen hinterlegt werden

Spalte | Bedeutung
--|--
Kurs | DropDown-Feld - Wählen Sie aus der Liste der Kurse, die vorab für diese Klasse definiert wurden, einen Kurs aus.
Kürzel | Die Eingabe eines Kürzels ist zwingend erforderlich, kann beliebig sein
Name | Tragen Sie einen beliebigen Namen ein (in Anlehnung an den Kurs)
Konfiguration | DropDown-Feld, soll das Leistungsprofil benotet werden, wählen Sie hier die gewünschte Konfiguration aus 
Notensystem | DropDown-Feld, wählen Sie hier das benötigte Notensystem für die gewählte Konfiguration aus
Notentyp | 
Bewertungsprofil | DropDown-Feld, wählen Sie das gewünschte Bewertungsprofil aus
Bemerkung | Eingabe von Freitext
interner Code | aktuell keine Bedeutung

[![Leistungsprofile definieren..."][22]][22]

### Leistungsprofile ohne Bewertungsprofil

Es gibt einige Fächer, die auf dem Zeugnis ohne Bewertungsprofile beurteilt werden. Diese erfassen Sie hier ebenfalls, allerdings bleibt die Spalte "Bewertungsprofil" leer. 

![`Leistungsprofile ohne Bewertungsprofile...`](/assets/images/enbrea.leistungen/30.png)

In unserem Beispiel sind das die Fächer "Sprechen und Zuhören", "Lesen - mit Texten und Medien umgehen", "Rechtschreiben" sowie "Sprache und Sprachgebrauch".

[![Leistungsprofile ohne Bewertungsprofile...][29]][29]

Da diese dem Kurs "Deutsch" angehören, müssen Sie diese im Feld "Kurs" mit dem entsprechenden Deutschkurs des Jahrganges verknüpfen.

[![`Klassen > Zeiträume > ENBREA Leistungsprofile`][31]][31]

### Leistungsprofile ohne Kurszuweisung

Es gibt Fächer, die in den Bewertungsgruppen benotet werden. In unserem Beispiel sind das die Fächer "Arbeitsverhalten" und "Sozialverhalten". 

[![Beispiel für Fächer mit Leistungsprofilen ohne Bewertungsprofile...][32]][32]

Diesen Fächern wird über den Aufruf `Leistungsprofile definieren...` kein Kurs im Feld "Kurs" zugeordnet.

[![Leistungsprofil-Einträge mit und ohne Kurszuweisung][24]][24]

## Kurse zuweisen

### Schüler > Zeugnis > ENBREA Kurse

Bitte weisen Sie im Menü `Schüler > Zeugnis > ENBREA Kurse` über das Plus Symbol einem oder mehreren Schülern einer Klasse die Kurse zu.

Es öffnet sich ein Assistent, im Auswahlfenster können Sie im ersten Fenster die gewünschten Schüler markieren.

![Kurse - Schüler auswählen](/assets/images/enbrea.leistungen/25.png)

Bestätigen Sie bitte mit `Weiter`. Hier wählen Sie die gewünschten Kurse aus.

![Kurse - Kurse auswählen](/assets/images/enbrea.leistungen/26.png)

Bestätigen Sie bitte mit `Weiter`. Es werden den gewählten Schülern jeweils noch nicht existierende Kurse zugewiesen, so dass Kurse nicht doppelt belegt werden können. Insofern die Kurse Leistungsprofile enthalten, werden diese automatisch mit den Schülern synchronisert.  

Beenden Sie den Assisten mit `Fertigstellen`.

Im Menü `Schüler > Zeugnis > ENBREA Kurse` ergibt sich nun folgendes Bild:

![Ergbnis der Kurszuweisung](/assets/images/enbrea.leistungen/27.png)

### Schüler > Zeugnis > ENBREA Leistungen

Wechseln Sie in das Menü `Schüler > Zeugnis > ENBREA Leistungen`. Hier finden Sie Ihre Kurse mit und ohne Leistungsprofilen. Die Benotung erfolgt in dieser Ansicht.

![ENBREA Lernlesitungen](/assets/images/enbrea.leistungen/28.png)

## Halbjahreswechsel

1. Schüler in den neuen Zeitraum fortschreiben im Menü `Schüler > Laufbahnprozess > Schüler fortschreiben`. 
Nutzen Sie hier den Assistenten um alle Schüler fortzuschreiben. Weitere Informationen zum Schuljahreswechsel finden Sie [hier](https://doc.magellan7.stueber.de/schulverwaltung/howto/halbjahreswechsel/)


!!! info "Hinweis"
    
    Die ENBREA Leistungen sind aktuell der Klasse im Menü `Klassen > Zeiträume > ENBREA Leistungsprofile` noch nicht zuwiesen. Diese können über den Assistenten `Laufbahnprozess > ENBREA Leistungen übernehmen` in das 2. HJ der Klasse übernommen werden.

2. Bitte wechseln Sie in den Zeitraum des 2. Halbjahres. Öffnen Sie im Menü `Schüler` oder im Menü `Klassen` den `Laufbahnprozess` und wählen hier `ENBREA Leistungen übernehmen`. Wählen Sie die Klasse aus dem vorigen Halbjahr. Die zugewiesenen ENBREA Leistungen des Schülers werden nun aus dem 1. HJ in das 2. HJ übernommen. 

![Klasse auswählen zur Übernahme der ENBREA Leistungen aus dem vorigen Zeitraum](/assets/images/enbrea.leistungen/15.png)

## Schuljahreswechsel

1. Neuen Zeitraum anlegen (`Extras > Schlüsselverzeichnisse > Zeiträume`)

2. Neue Klassen anlegen: Bitte gehen Sie in den Zeitraum des neuen Schuljahres und starten Sie den Asisstenten zur Übernahme neuer Klassen über  `Klassen > Laufbahnprozess > Klassen übernehmen`. Beim Prozess der Klassenübernahme werden auch die jeweiligen Kurse der ENBREA Leistungsprofile `Klassen > Zeiträume > ENBREA Leistungsprofile > Kurse` mit übernommen.

3. Schüler in die neue Klasse versetzen (`Laufbahnprozess > Schüler versetzen`)

4. Den Schülern Kurse zuweisen (Über Menü `Schüler > Zeugnis > ENBREA Kurse` über das `Plus Symbol` einem oder mehreren Schülern die Kurse zuweisen.)

Weitere Informationen zum Schuljahreswechsel finden Sie [hier](https://doc.magellan.stueber.de/schulverwaltung/howto/schuljahreswechsel/)




