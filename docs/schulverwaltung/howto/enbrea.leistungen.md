Dieses Kapitel ist im Aufbau!

# ENBREA Leistungen

Dieser Bereich dient als Grundlage zum Erfassen von Daten, die in sogenannten komplexen Zeugnisberichten ausgegeben werden.
Im Unterschied zu einfachen Zeugnissen sind hier auch noch Leistungen je Fach weiter unterteilbar, es sind verschiedene Notensysteme möglich.

!!! warning "Wichtig"

    Bitte schauen Sie vorab im Modul `MAGELLAN BERICHTE` nach, ob diese Ansicht von Ihrem Zeugnis verwendet wird.

## Funktionalitäten aktivieren

Um die Funktionalitäten zu aktivieren, setzen Sie bitte das Häkchen unter `Datenbank > Optionen > ENBREA Funktionen aktivieren`.

![Aktivieren Sie das Häkchen!](/assets/images/enbrea.leistungen/01.png)

## Schlüsselverzeichnisse vorbereiten

* Bewertungsprofile
* Notensysteme
* Notentypen

Um Fächer und deren Kompetenzbereiche gemäß Zeugnisvorlage in MAGELLAN zu erfassen, müssen die o.g. Schlüsselverzeichnisse entsprechend gefüllt werden. 

Folgender Auszug einer Zeugnisvorlage für das Fach Mathematik soll uns als Beispiel für die Dateneingabe in MAGELLAN dienen:

![Beispiel für eine Zeugnis](/assets/images/enbrea.leistungen/02.png)

### Bewertungsprofile

Öffnen Sie zunächst das `Extras > Schlüsselverzeichnisse > Bewertungsprofile`. Dieses Verzeichnis ist in folgende Registerkarten unterteilt:

* Bewertungsprofil
* Bewertungsprofil-Gruppen
* Bewertungsprofil-Einträge

Die Bewertung eines Faches wird wie folgt differenziert:

![Beispiel für das Schlüsselverzeichnis Bewertungsprofil](/assets/images/enbrea.leistungen/03.png)

#### Unterkarte Bewertungsprofil

![Unterkarte Bewertungsprofile](/assets/images/enbrea.leistungen/04.png)

Der Eintrag eines Wertes auf der Unterkarte Bewertungsprofil entspricht im oberen Beispiel dem Eintrag "Mathematik".

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel einer frei gewähltn Kurzform für "Mathematik(01)", also für Mathe in der Klassenstufe 1.
Bezeichnung| freie Wahl
Konfiguration| Legen Sie hier die Beurteilung fest (im Beispiel für die Zeile "Mathematik"). <br/>Mögliche Werte: <br/>- keine Beurteilung <br/>- Note <br/>- Beurteilung <br/>- Note und Beurteilung
Notensystem| zeigt die im Schlüsselverzeichnis `Notensystem` angelegten Werte
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

!!! info "Hinweis"

    Weichen die Bewertungsprofile pro Klassenstufe ab, legen Sie hier für jedes Fach entsprechend der Klassenstufe ein Bewertungsprofil an. Zunächst genügen die Einträge in den Spalten "Kürzel" und "Bezeichnung". Klicken Sie auf das Symbol `Neue Zeile`. Es erscheint eine neue Zeile im Verzeichnis zur direkten Eingabe von Kürzel und Bezeichnung.

#### Unterkarte Bewertungsgruppen

![Unterkarte Bewertungsgruppen](/assets/images/enbrea.leistungen/05.png)

Der Eintrag eines Wertes auf der Unterkarte Bewertungsgruppen entspricht im oberen Beispiel einem Eintrag unterhalb von "Mathematik", in diesem Beispiel dem Eintrag "Zahlen und Optionen". Es könnte unterhalb von Mathematik auch mehr als eine Unterteilung (mehr als eine Bewertungsgruppe) geben.

!!! tip "Tipp"

    Um eine Bewertungsgruppe anzulegen, müssen Sie auf der ersten Karte das Bewertungsprofil markieren, dann auf die Unterkarte Bewertungsgruppen wechseln und einen Eintrag anlegen. Damit werden die Bewertungsgruppen genau einem Bewertungsprofil zugeordnet.

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel einer frei gewähltn Kurzform für die "Zahlen und Optionen"
Bezeichnung| der Eintrag entspricht im oberen Beispiel dem Eintrag "Zahlen und Optionen"
Konfiguration| Legen Sie hier die Beurteilung fest (im Beispiel für die Zeile "Mathematik"). <br/>Mögliche Werte: <br/>- keine Beurteilung <br/>- Note <br/>- Beurteilung <br/>- Note und Beurteilung
Notensystem| zeigt die im Schlüsselverzeichnis `Notensystem` angelegten Werte
Position| Zeugnisposition, bitte tragen Sie die Positionen entsprechend der Vorgaben für ihr Zeugins (siehe Modul MAGELLAN Berichte) ein
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

#### Unterkarte Bewertungseinträge

![Unterkarte Bewertungseinträge](/assets/images/enbrea.leistungen/06.png)

Der Eintrag eines Wertes auf der Unterkarte `Bewertungseinträge` entspricht im oberen Beispiel einem Eintrag unterhalb von "Zahlen und Optionen". Es kann unterhalb von "Zahlen und Optionen" auch mehrere Einträge geben. Jeder Bewertungseintrag ist einer Bewertungsgruppe zuzuweisen. 

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, einer frei gewähltn Kurzform für den Bewertungseintrag.
Bezeichnung| freie Wahl
Gruppe| Tragen Sie bitte eine Bewertungsgruppe ein
Notensystem| zeigt die im Schlüsselverzeichnis `Notensystem` angelegten Werte
Position| Zeugnisposition, bitte tragen Sie die Positionen entsprechend der Vorgaben für ihr Zeugins (siehe Modul MAGELLAN Berichte) ein
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

## Notensysteme

![Schlüsselverzeichnis Notensysteme](/assets/images/enbrea.leistungen/07.png)

Öffnen Sie zunächst das `Extras > Schlüsselverzeichnisse > Notensysteme`. Dieses Verzeichnis ist in folgende Registerkarten unterteilt:

* Notensysteme
* Notensystem-Einträge

Innerhalb Ihrer Schule und bei komplexeren Zeugnisberichten kann es unterschiedliche Systeme zur Beurteilung geben: Noten, Punkte, Prozente, Tendenzen...
Diese Arten der Beurteilung (Notensysteme) werden mit den einzelnen Beurteilungswerten (Notensystem-Einträge) in diesem Schlüsselverzeichnis angelegt.

### Unterkarte Notensystem

![Unterkarte Notensysteme](/assets/images/enbrea.leistungen/08.png)

Feld|Bedeutung
--|--
Kürzel| Eintrag muss gesetzt werden, der Eintrag entspricht im oberen Beispiel zum Beispiel dem Eintrag "Tendenzen"
Bezeichnung| freie Wahl
Wertetyp| Mögliche Werte `Zahlen` oder `Texte`
Beschreibung|freie Wahl
interner Code| derzeit nicht in Benutzung

### Unterkarte Notensystem-Einträge

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

## Notentypen

![Schlüsselverzeichnis Notentypen](/assets/images/enbrea.leistungen/10.png)

In diesem Verzeichnis wird die Art der Bewertung (z.B. Zeugnisnote, mündliche Note) definiert. Diese Werte können später den Bewertungen der Kurse unter dem Menüpunkt `Klassen > Zeitraum > ENBREA-Leistungen > Leistungsprofile` zugeordnet werden, dazu kommen wir aber später noch.

## Kurse anlegen

## Kurse zuweisen

## Halbjahreswechsel

## Schuljahreswechsel
