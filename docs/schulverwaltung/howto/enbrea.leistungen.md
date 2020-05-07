Dieses Kapitel ist im Aufbau!

# ENBREA Leistungen

Dieser Bereich dient als Grundlage zum Erfassen von Daten, die in sogenannten komplexen Zeugnisberichten ausgegeben werden.
Im Unterschied zu einfachen Zeugnissen sind hier auch noch Leistungen je Fach weiter unterteilbar, es sind verschiedene Notensysteme möglich.

!!! warning "Wichtig"

    Bitte schauen Sie vorab im Modul `MAGELLAN BERICHTE` nach, ob diese Ansicht von Ihrem Zeugnis verwendet wird.

## Funktionalitäten aktivieren

Um die Funktionalitäten zu aktivieren, setzen Sie bitte das Häkchen unter `Datenbank > Optionen > ENBREA Funktionen aktivieren`.

![Aktivieren Sie das Häkchen!](/assets/images/enbrea.leistungen/01.png)

## Schlüsselverzeichnisse

Um Fächer und deren Kompetenzbereiche gemäß Zeugnisvorlage in MAGELLAN zu erfassen, müssen die folgenden Schlüsselverzeichnisse entsprechend gefüllt werden.

* Bewertungsprofile
* Notensysteme
* Notentypen

Folgender Auszug einer Zeugnisvorlage für das Fach "Mathematik" soll uns als Beispiel für die Dateneingabe in MAGELLAN dienen:

![Beispiel für eine Zeugnis](/assets/images/enbrea.leistungen/02.png)

### Bewertungsprofile

Öffnen Sie zunächst das `Schlüsselverzeichnis > Bewertungsprofile` . Dieses Verzeichnis ist in folgende Registerkarten unterteilt:

* Bewertungsprofile
* Bewertungsgruppen
* Bewertungseinträge

![Beispiel für `Schlüsselverzeichnis > Bewertungsprofile`](/assets/images/enbrea.leistungen/17.png)

Die Bewertung eines Faches wird wie folgt differenziert:

![Differenzierung des Faches Mathematik](/assets/images/enbrea.leistungen/18.png)

#### Bewertungsprofile > Bewertungsprofile

![Unterkarte Bewertungsprofile](/assets/images/enbrea.leistungen/04.png)

Der Eintrag eines Wertes unter `Schlüsselverzeichnis > Bewertungsprofile > Bewertungsprofile` entspricht im oberen Beispiel dem Eintrag "Mathematik". 

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel einer frei gewählten Kurzform für "Mathematik (01)", also für Mathe in der Klassenstufe 1.
Bezeichnung| freie Wahl
Konfiguration| Legen Sie hier die Beurteilung fest (im Beispiel für die Zeile "Mathematik"). <br/>Mögliche Werte: <br/>- keine Beurteilung <br/>- Note <br/>- Beurteilung <br/>- Note und Beurteilung
Notensystem| zeigt die im Schlüsselverzeichnis `Notensystem` angelegten Werte
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

!!! info "Hinweis"

    Weichen die Bewertungsprofile pro Klassenstufe ab, legen Sie hier für jedes Fach entsprechend der Klassenstufe ein Bewertungsprofil an. Zunächst genügen die Einträge in den Spalten "Kürzel" und "Bezeichnung". Klicken Sie auf das Symbol `Neue Zeile`. Es erscheint eine neue Zeile im Verzeichnis zur direkten Eingabe von Kürzel und Bezeichnung.

#### Bewertungsprofile > Bewertungsgruppen

![Unterkarte Bewertungsgruppen](/assets/images/enbrea.leistungen/05.png)

Der Eintrag eines Wertes unter `Schlüsselverzeichnis > Bewertungsprofile > Bewertungsgruppen` entspricht im oberen Beispiel einem Eintrag unterhalb von "Mathematik", in diesem Beispiel den Einträgen:

* Zahlen und Operationen
* Raum und Form
* Größen und Messen
* Daten, Häufigkeit und Wahrscheinlichkeit

Ein Bewertungsprofil (hier: Mathematik) kann in beliebig viele Bewertungsgruppen unterteilt werden. Es kann auch sein, dass es für ein Bewertungsprofil keine Bewertungsgruppe gibt. (Wie im Beispiel "indische Landeskunde")

!!! tip "Tipp"

    Um eine Bewertungsgruppe anlegen zu können, müssen Sie auf der ersten Karte das Bewertungsprofil markieren, dann auf die Unterkarte Bewertungsgruppen wechseln und einen Eintrag anlegen. Damit werden die Bewertungsgruppen genau einem Bewertungsprofil zugeordnet.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel einer frei gewähltn Kurzform für die "Zahlen und Optionen"
Bezeichnung| der Eintrag entspricht im oberen Beispiel dem Eintrag "Zahlen und Optionen"
Konfiguration| Legen Sie hier die Beurteilung fest (im Beispiel für die Zeile "Mathematik"). <br/>Mögliche Werte: <br/>- keine Beurteilung <br/>- Note <br/>- Beurteilung <br/>- Note und Beurteilung
Notensystem| zeigt die im Schlüsselverzeichnis `Notensystem` angelegten Werte
Position| Zeugnisposition, bitte tragen Sie die Positionen entsprechend der Vorgaben für ihr Zeugins (siehe Modul MAGELLAN Berichte) ein
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

#### Bewertungsprofile > Bewertungseinträge

![Unterkarte Bewertungseinträge](/assets/images/enbrea.leistungen/06.png)

Der Eintrag eines Wertes unter `Schlüsselverzeichnis > Bewertungsprofile > Bewertungseinträge` entspricht im oberen Beispiel einem Eintrag unterhalb von "Zahlen und Optionen". Es kann unterhalb von "Zahlen und Optionen" auch mehrere Einträge geben. Jeder Bewertungseintrag ist einer Bewertungsgruppe zuzuweisen.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, einer frei gewähltn Kurzform für den Bewertungseintrag.
Bezeichnung| freie Wahl
Gruppe| Tragen Sie bitte eine Bewertungsgruppe ein
Notensystem| zeigt die im Schlüsselverzeichnis `Notensystem` angelegten Werte
Position| Zeugnisposition, bitte tragen Sie die Positionen entsprechend der Vorgaben für ihr Zeugins (siehe Modul MAGELLAN Berichte) ein
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

### Notensysteme

![Schlüsselverzeichnis Notensysteme](/assets/images/enbrea.leistungen/07.png)

Öffnen Sie über `Extras > Schlüsselverzeichnisse > Notensysteme` das Verzeichnis der Notensystem. Dieses ist in folgende Registerkarten unterteilt:

* Notensysteme
* Notensystem-Einträge

Innerhalb Ihrer Schule und bei komplexeren Zeugnisberichten kann es unterschiedliche Systeme zur Beurteilung geben: Noten, Punkte, Prozente, Tendenzen...
Diese Arten der Beurteilung (Notensysteme) werden mit den einzelnen Beurteilungswerten (Notensystem-Einträge) in diesem Schlüsselverzeichnis angelegt.

#### Notensysteme > Notensysteme

![Unterkarte Notensysteme](/assets/images/enbrea.leistungen/08.png)

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel zum Beispiel dem Eintrag "Tendenzen"
Bezeichnung| freie Wahl
Wertetyp| Mögliche Werte `Zahlen` oder `Texte`
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

#### Notensysteme > Notensystem-Einträge

![Unterkarte Notensystem-Einträge](/assets/images/enbrea.leistungen/09.png)

Wählen Sie auf der Unterkarte `Notensysteme` einen Wert aus, wechseln Sie anschließend auf die Unterkarte `Notensystem-Einträge` und erfassen die dazugehörigen Einträge. Die vorstehende Abbildung zeigt die Notensystem-Einträge, die zum Notensystem Tendenzen aus unserem Beispiel gehören.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel dem Eintrag "Mathematik"
Bezeichnung| freie Wahl
Wertetyp| Mögliche Werte `Zahlen` oder `Texte`
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

!!! info "Hinweis"
    
    Nachdem die Notensysteme definiert wurden, müssen diese im Schlüsselverzeichnis "Bewertungsprofile" pro definiertem Profil hinterlegt werden.

### Notentypen

![Schlüsselverzeichnis Notentypen](/assets/images/enbrea.leistungen/10.png)

In diesem Verzeichnis wird die Art der Bewertung (z.B. Zeugnisnote, mündliche Note) definiert. Diese Werte können später den Bewertungen der Kurse unter dem Menüpunkt `Klassen > Zeitraum > ENBREA-Leistungen > Leistungsprofile` zugeordnet werden, dazu kommen wir aber später noch.

## Kurse anlegen

Die Kurse legen Sie bitte im Menü `Klassen > Zeiträume > ENBREA Leistungsprofile` über den Aufruf `Kurse definieren...` an.

![Kurse definieren](/assets/images/enbrea.leistungen/13.png)

Es öffnet sich das Dialogfenster zum Definieren der Kurse

![Kurse definieren](/assets/images/enbrea.leistungen/19.png)

Über das `Plus Symbol` kann ein neuer Kurs mit folgenden Informationen angelegt werden.

Spalte | Bedeutung
--|--
Aktion| je nach Aktion werden hier folgende Werte ausgegeben:<br/> - Neu anlegen:  über das `Plus Symbol` <br/>- Bearbeiten: über das `Plus Symbol`<br/> - Duplizieren - Duplizieren eines vorhandenen Kurses über `Kurs duplizieren`<br/> - Duplizieren mit Leistungsprofilen - Duplizieren eines vorhandenen Kurses mit Leistungsprofil über `Kurs mit Leistungsgprofil duplizieren` <br/> - Übergreifend verwenden
Fach| Auswahl aus dem `Schlüsselverzeichnis > Fächer`
Unterrichtsart|Auswahl aus dem `Schlüsselverzeichnis > Unterrichtsart`
Fachstatus|Auswahl aus dem `Schlüsselverzeichnis  > Fachstatus`
Lehrer|Auswahl aus der Menü Lehrer mit dem Status "Aktiv"
Schwerpunkt | Auswahl aus dem `Schlüsselverzeichnis > Fachschwerpunkt`
Niveau | Auswahl aus dem `Schlüsselverzeichnis  > Fachniveaus `
Kursnr.| Eingabe einer Kursnummer
Bilingual|Auswahl aus dem `Schlüsselverzeichnis > Kurssprachen`
Merkmal | Eingabe von Freitext

### Kurs duplizieren

Sie können auch Kurse im Zeitraum über den Aufruf `Kurs duplizieren` als Kurs in ihre gewählte Klasse übernehmen. Wählen Sie zunächst im unteren Bereich des Fenster den gewünschten Kurs und wählen dann in der Menüleiste des Fensters `Kurs duplizieren`.

![Kurse duplizieren](/assets/images/enbrea.leistungen/20.png)

!!! info "Hinweis"
    
    Sie können auch mehrere Kurse in einem Schritt duplizieren. Markieren Sie über `Strg + linke Maustaste` die gewünschte Kurse und wählen Sie dann den Aufruf `Kurs duplizieren`.

### Kurse mit Leistungprofil duplizieren

### Übergreifend verwenden

Findet hier aktuell noch keine Verwendung.

## Leistungsprofile anlegen

Die Leistungsprofile legen Sie bitte im Menü `Klassen > Zeiträume > ENBREA Leistungsprofile` über den Aufruf `Leistungsprofile definieren...` an.

![Aufruf `Leistungsprofile definieren...`](/assets/images/enbrea.leistungen/21.png)

Über das `Plus Symbol` wird eine neue Zeile angelegt werden. Folgende Informationen müssen hinterlegt werden

Spalte | Bedeutung
--|--
Kurs | DropDown-Feld - Wählen Sie aus der Liste der Kurse, die vorab für diese Klasse definiert wurden, einen Kurs aus.
Kürzel | Die Eingabe eines Kürzels ist zwingend erforderlich
Name | Tragen Sie einen beliebigen Namen ein (in Anlehnung an den Kurs)
Konfiguration | DropDown-Feld, wählen Sie hier "komplexer Bericht" aus 
Notensystem | DropDown-Feld, wählen Sie hier "Tendenzen" aus 
Notentyp | 
Bewertungsprofil | DropDown-Feld, wählen Sie das gewünschte vorab 
Bemerkung | Eingabe von Freitext
interner Code | aktuell keine Bedeutung

![`Leistungsprofile definieren...`](/assets/images/enbrea.leistungen/22.png)

Den Fächer "Arbeitsverhalten" und "Sozialverhalten" wird über den Aufruf `Leistungsprofile definieren...` kein Kurs im Feld "Kurs" zugeordnet.

![Leistungsprofil-Einträge mit und ohne Kurszuweisung](/assets/images/enbrea.leistungen/24.png)

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

Weitere Informationen zum Schuljahreswechsel finden Sie [hier](https://doc.magellan7.stueber.de/schulverwaltung/howto/schuljahreswechsel/)




