# Leistungen eingeben

Für jeden Schüler ist ein Verzeichnis über seine persönlichen Zeugnisdaten hinterlegt. Aus diesem Verzeichnis werden die Daten für den Zeugnisdruck verwendet. Alle diese Daten finden Sie auf den Registerkarten `Laufbahn` und `Zeugnis` des Schülers.

## Noten definieren

Als Voraussetzung für die Eingabe von Noten müssen diese im Verzeichnis `Noten` definiert sein. Wählen Sie dazu `Extras> Schlüsselverzeichnisse` und dann `Noten`. Im Dialogfenster `Verzeichnis der Noten` können Sie eine beliebige Anzahl von Noten definieren.

![ Dialog `Verzeichnis der Noten`](/assets/images/zeugnisdaten/zeugnisdaten14.png)

Für jeden Noteneintrag können Sie dabei in der Spalte `Notenart` zwischen einem `Notenwert`, `Füllwert` (zum Beispiel für "Attest" oder "o.B.") und einem `Punktwert` unterschieden. Zusätzlich können Sie neben der allgemeinen Bezeichnung in der Spalte `Bezeichnung` auch einen alternativen Text in der Spalte `Alternative Bezeichnung` wählen. Wird beim späteren Zeugnisdruck die Bezeichnung der Note ausgegeben, so erfolgt dies im Regelfall über den Wert im Feld `Bezeichnung`. Nur in Ausnahmefällen, wo beispielsweise Abkürzungen für Noten verwendet werden (z.B. bei Allgemeinbildenden Schulen in Baden-Württemberg), wird der Eintrag im Feld `Alternative Bezeichnung` genutzt.

Die angebotene Beurteilungsart unter `Schüler > Zeugnis > Leistungen` richtet sich danach, was der Klasse des Schülers unter `Klassen > Daten > Beurteilungsart` hinterlegt wurde. Zur Auswahl stehen dort die Berurteilungsarten:

* Benotung durch Noten (hierbei steht auch ein Feld für die schriftliche Beurteilung des Fachs zur Verfügung)
* Benotung durch Punkte
* Benotung durch Prozente
* Beurteilungstexte

Je nach Auswahl werden in den Notenfeldern der Schüler Noten, Punkte, Prozente oder auch Eingabemöglichkeiten für Beurteilungstexte eingeblendet.

!!! warning "Sehr wichtig!"

    Bitte wählen Sie die Beurteilungsart der Klasse vor der Vergabe der Zeugnisnoten oder -punkte aus!

![Wählen Sie die Berurteilungsart bei der Klasse aus](/assets/images/zeugnisdaten/zeugnisdaten15.png)

!!! info "Hinweis"

    Um Ausfälle auf einen Blick erkennen zu können, weisen Sie den Noten unter `Extras > Schlüsselverzeichnisse > Noten` in der Spalte `Hintergrundfarbe `eine individuelle Farbe zu. Die Farbe wird unter `Schüler > Zeugnis > Leistungen` und auch in der Notenübersicht gezeigt. Zusätzlich muss bitte unter `Datenbank > Optionen > Einstellungen` die `Hintergrundfarbe für Benotungen` aktiviert werden.

## Noteneingabe

Sie geben Noten für einen Schüler ein, indem Sie auf der Registerkarte `Zeugnis` des Schülers die Registerkarte `Leistungen` wählen. Voraussetzung dafür ist, dass diesem Schüler bereits Fächer zugewiesen wurden.

![Auf der Registerkarte `Leistungen` können Sie jedem Schüler vier schriftliche, eine mündliche Note, eine Endnote und eine Endnote (Gesamt) eintragen](/assets/images/zeugnisdaten/zeugnisdaten16.png)

Je nach der eingestellten Beurteilungsart der Klasse der werden zur Eingabe entweder Noten- oder Punktwerte angeboten. Auf die Eingabe von Beurteilungstexten wird im nachfolgenden Abschnitt näher eingegangen. Aus den schriftlichen und mündlichen Noten berechnet MAGELLAN im Regelfall nicht automatisch die Endnote!
Auf der Registerkarte `Leistungen` werden also im Regelfall nur die Noten eingetragen, die letztendlich auf dem Zeugnis erscheinen und sie besitzt keine Notenbuchfunktionalität. Im Regelfall sollten Sie in der Spalte `Endnote` die Zeugnisnote eintragen.

!!! warning "Sehr wichtig!"

    Wenn Sie innerhalb eines Zeitraums aufgrund der eingetragenen Noten Versetzungen, Abschlüsse bzw. Durchschnittsnoten berechnen wollen, müssen Sie das Optionsfeld `Durchschnitt einblenden` markieren.

### Leistungsarten

Die Angabe der Lesitungsarten wird für bestimmte Berechnungsskripte benötigt. 

Bitte geben Sie die Leistungsarten bei den Schülern unter `Schüler > Zeugnis > Leistungen` für jedes Fach mit der vom Schüler gewählten Leistungsart an. Diese Leistungsart wird je Kurshalbjahr beim Synchronisieren der Daten mit ins Menü `Abitur > Qualifikation` übernommen. Die Leistungsart wird nur für benotete Fächer übernommen. Grundlage ist das Schlüsselverzeichnis `Verzeichnisse > Leistungsarten` mit Arten (Schriftlich, mündlich, praktisch) Sie legen sich hier die Arten der Leistung an (Beispiel Vortrag, Klausur usw.) und Sie markieren diese dann mit der korrekten Art (Beispiel: Klausur = schriftlich).

### Zeitraumübergreifende Notenübersicht Schüler oder Klasse

Wählen Sie den gewünschten Zeitraum und rufen dann `Menü Schüler > Schüler > Notenübersicht` auf. Die Funktionsweisen werden nachfolgend beschrieben. <img src="/assets/images/zeugnisdaten/006.png">

Es werden Ihnen nun entweder alle Fächer und Noten `aktuellen Schülers` oder `aller Schüler der Klasse` mit Angabe des Halbjahres angezeigt. Sie können in der Übersicht wie gewohnt Sortieren und Gruppieren.

![Dies ist die Notenübersicht für den aktuellen Schüler](/assets/images/zeugnisdaten/zeugnisdaten17.png)

!!! warning "Sehr wichtig!"

    Die Registerkarte `Leistungen` und die `zeitraumübergreifende Notenmatrix` können nach Excel oder/ exportiert werden. 
    
    Sie können die zeitraumübergreifende Notenübersicht auch für die gesamte Klasse des ausgewählten Schülers anzeigen lassen. Dafür schalten Sie in der oberen Menüleiste von `Aktueller Schüler` auf `Alle Schüler der Klasse` um.


![Beispiel: Die  Noten der Schüler der Klasse 13 sind nach der Spalte Fach gruppiert.](/assets/images/zeugnisdaten/zeugnisdaten18.png)

## Beurteilungstexte

Haben Sie bei der Klasse die Beurteilungsart `Beurteilungstexte` eingestellt, so haben Sie für die Schüler dieser Klasse ein geändertes Layout auf der Registerkarte `Leistungen`.

![Sie können hier neben dem Fach und der Position in der Spalte `Beurteilung` einen freien Beurteilungstext eintragen.](/assets/images/zeugnisdaten/zeugnisdaten19.png)

Um diesen einzutragen, müssen Sie in der Zeile des Fachs entweder einen Doppelklick auf die Spalte `Beurteilung` ausführen oder auf die entsprechende Schaltfläche `Beurteilung editieren..` klicken. Sie haben zusätzlich über die Schaltfläche `Rechtschreibung prüfen…` die Möglichkeit den Text überprüfen zu lassen. Die Einstellmöglichkeiten für die Rechtschreibprüfung finden Sie unter `Datenbank > Optionen > Rechtschreibung`

![Geben Sie hier einen freien Beurteilungstext ein. Sie können dabei auch auf bereits definierte Textbausteine zurückgreifen, wenn Sie auf `Aus Verzeichnis auswählen` klicken. Klicken Sie anschließend auf OK.](/assets/images/zeugnisdaten/zeugnisdaten21.png)

Bei der Eingabe des Beurteilungstextes können Sie auf bereits definierte Textbausteine zurückgreifen. Diese müssen Sie zuvor unter `Extras > Schlüsselverzeichnisse > Zeugnisbeurteilungen` definiert haben.

![Dies ist das Verzeichnis der Zeugnisbeurteilungen](/assets/images/zeugnisdaten/zeugnisdaten22.png)

!!! warning "Sehr wichtig!"

    Die Beurteilung nach Beurteilungstexten wird häufig in den ersten Klassen der Grundschule verwendet.

## Layout bei Noteneingabe anpassen

Das Layout auf der Registerkarte `Leistungen` kann individuell angepasst werden. Sie können sowohl nicht benötigte Spalten ausblenden als auch die Spaltenbezeichnungen umbenennen. Zur Anpassung des Layouts müssen Sie links oben auf der Registerkarte `Leistungen` auf die Schaltfläche `Layout anpassen…` klicken. Klicken Sie im Dialogfenster `Layout anpassen` auf die Häkchen in der Spalte `Sichtbar`, um die Spalte ein- bzw. auszublenden. Klicken Sie in der Spalte `Bezeichnung` auf den Begriff in der entsprechenden Zeile. Sie können diesen jetzt direkt überschreiben.

!!! warning "Sehr wichtig!"

    Die Einstellungen unter `Layout anpassen...` beziehen sich auf Ihren Arbeitsplatz, nicht auf andere MAGELLAN-Installationen.

![Hier können Sie die Spaltenüberschrift verändern und angeben, ob eine Spalte sichtbar ist.](/assets/images/zeugnisdaten/zeugnisdaten23.png)

## Arbeits- und Sozialverhalten

Unter `Schüler > Zeugnis` können Sie für jeden Schüler das Arbeits- und Sozialverhalten in Kategorien (zum Beispiel `Teamfähigkeit`) erfassen und auch mit einer Bewertung (zum Beispiel `sehr ausgeprägt`) beurteilen. Zusätzlich können auch fachliche Leistungen nach selbst vergebenen Bewertungsmaßstäben beurteilt werden.

### Vorbereitung

Vorab müssen die verwendeten Schlüsselverzeichnisse eingerichtet werden. Folgende Schlüsselverzeichnisse stehen dafür unter `Extras > Schlüsselverzeichnis > Arbeits- und Sozialverhalten` zur Verfügung.

#### Schlüsselverzeichnisse

**Typen:**<br/>Dient als Filter um zwischen `Arbeits- und Sozialverhalten` und `Fachlichen Leistung` zu differenzieren.

![ Verzeichnis `Typen des Arbeits- und Sozialverhalten`](/assets/images/zeugnisdaten/zeugnisdaten24.png)

**Arten:**<br/>
Kann als Übergruppierung für die Kategorien verwendet werden, zum Beispiel um zwischen `Sozialverhalten` und `Arbeitsverhalten` zu unterscheiden. Für fachliche Leistungen entspricht die Art zum Beispiel `Deutsch` oder `Biologie`. Jeder Art wird zusätzlich der entsprechende Typ zugeordnet. Als Hilfe beim Erfassen der Arten kann das Verzeichnis zum Beispiel nach dem Typ gefiltert werden.

![ Verzeichnis `Arten für das Arbeits- und Sozialverhalten`](/assets/images/zeugnisdaten/zeugnisdaten25.png)

**Kategoriegruppen:**<br/>Legen in diesem Verzeichnis die Untergruppen der Arten an. Ein Bespiel für Kategoriegruppen: für die Art `Deutsch` sollen nach `Sprechen und Zuhören` und `Schreiben` getrennte Unterpunkte bewerten werden. Die Kategoriegruppen können Kategorien zugeordnet werden.

![Kategoriegruppen](/assets/images/zeugnisdaten/zeugnisdaten26.png)

**Kategorien:**<br/>Legen Sie in diesem Verzeichnis die an Ihrer Schule zu bewertenden Kategorien an. In der Spalte Art können Sie den einzelnen Kategorien die zuvor angelegten Arten zuordnen. Diese Unterteilung hilft die Kategorien zusätzlich zu den Positionen im Zeugnisdruck korrekt anzuordnen. Jede Kategorie kann einer Kategoriegruppe zugeordnet werden.Der Inhalt des Verzeichnisses kann nach dem Typ gefiltert angezeigt werden. In der nachfolgenden Abbildung ist nach dem Typ `Fachliche Leistung` gefiltert worden.

![Filterung der Kategorien nach der fachlichen Leistung](/assets/images/zeugnisdaten/zeugnisdaten27.png)<br/><br/>![ Filterung der Kategorien nach dem Allgemeinen Lern- und Sozialverhalten](/assets/images/zeugnisdaten/zeugnisdaten28.png)

**Inhaltetafeln:** <br/>Um in Zeugnissen stichpunktartig die im Schuljahr unterrichteten Themen pro Klasse abzubilden, können die Themen in Inhaltetafeln gesammelt werden. Dabei ist es möglich für eine Art (zum Beispiel für Deutsch) verschiedene Inhaltetafeln anzulegen. Die Inhalte unterscheiden sich zwischen den Schuljahren und werden daher in getrennten Inhaltetafeln angelegt.

![Pro Schuljahr werden für die Fächer Inhaltetafeln eingerichtet](/assets/images/zeugnisdaten/zeugnisdaten29.png)

**Inhaltetafel-Kategorien:** <br/>Jede Inhaltetafel enthält Inhaltetafel-Kategorien. Für das Beispiel der Art Deutsch werden in der nachstehenden Abbildung die Themen für das 4. Schuljahr zeilenweise eingerichtet. Über die Position kann die spätere Reihenfolge auf dem Zeugnis gesteuert werden.

![Hier werden die in Deutsch unterrichteten Themen für Klasse 4 aufgeführt](/assets/images/zeugnisdaten/zeugnisdaten30.png)

**Bewertung:**<br/>
Legen Sie in diesem Verzeichnis die möglichen Abstufungen der Bewertungen an. Die Bewertungen können jeweils einem Typ zugeordnet werden. Damit können für das `Arbeits- und Sozialverhalten` andere Bewertungsabstufung als für `Fachliche Leistungen` realisiert werden. Je nach Zeugnisbericht kann für die Bewertungen eine Bezeichnung (zum Beispiel `erkennbar`) oder auch ein Kreuz abgeleitet aus dem Wert der Bewertung ausgegeben werden. 

![Bewertungen können pro Typ differenziert werden](/assets/images/zeugnisdaten/zeugnisdaten31.png)

**Kategorietafeln:** <br/>
Analog zu den Fachtafeln können auch vorbereitete Zusammenstellungen von Kategorien gesammelt den Schülern zugewiesen werden. Legen Sie dazu Kategorietafeln an und füllen sie mit Kategorien. Sie können dabei den Schülern auch die Fachlichen Leistungen und die Bewertungskriterien für das Arbeits- und Sozialverhalten in einem Arbeitsgang zuweisen. 

![Übersicht der Kategorietafeln](/assets/images/zeugnisdaten/zeugnisdaten32.png) 

![Inhalt der markierten Kategorietafeln](/assets/images/zeugnisdaten/zeugnisdaten33.png) 

### Layout anpassen

Über die Schaltfläche `Layout anpassen…` können Sie die Benennung der Spaltenköpfe anpassen oder auch einzelne Spalten ausblenden. Die originale Bezeichnung des umbenannten Spaltenkopfes wird in der Spalte `Spalte` weiterhin angezeigt.

### Kategorietafel extrahieren

Wenn Sie für einen Schüler die Kategorien per Hand angelegt haben, können Sie daraus auch eine Kategorietafel extrahieren.

|So geht's|
|:--|
|1. Wählen Sie den gewünschten Schüler, rufen Sie die Karte `Zeugnis > Arbeits- und Sozialverhalten` auf und klicken auf `Kategorietafel extrahieren…`.|
|2. Geben Sie ein Kürzel und eine Bezeichnung für die neue Kategorietafel ein und klicken auf `OK`.|
|3. Die neue Tafel steht im Anschluss im Assistenten `Kategorietafel zuweisen…`zur Verfügung oder kann unter `Extras > Schlüsselverzeichnisse > Gruppe Arbeits- und Sozialverhalten > Kategorietafeln` editiert werden.|

### Verteilen der Kategorien

Sie können die Kategorien für die Schüler einzeln per Hand zuweisen oder mehrere Kategorien gesammelt für eine Gruppe von Schülern zuweisen. Rufen Sie in beiden Fällen im Menü `Schüler` die Unterkarte `Zeugnis > Arbeits- und Sozialverhalten` auf. Möchten Sie die Sammelzuweisung der Kategorietafeln verwenden, können Sie dabei einen beliebigen Schüler wählen.

#### Zuweisen einer einzelnen Kategorie und Bewertung

|So geht's|
|:--|
|1.  Wählen Sie in der Auswahlliste `Schüler` den gewünschten Schüler und rufen Sie die Registerkarte `Zeugnis > Arbeits- und Sozialverhalten` auf. <br/><br/> ![Dies ist die noch ungefüllte Registerkarte `Arbeits- u. Sozialverhalten`.](/assets/images/zeugnisdaten/zeugnisdaten34.png) |
|2. Um eine neue Zeile zu erzeugen wählen Sie das rote Plus `Neue Kategorie` im rechten Bereich der Ansicht. |
|3. Wählen Sie für die neue Zeile im Feld Kategorie einen Wert aus den zuvor im Schlüsselverzeichnis erfassten Kategorien. |
|4. In der Spalte `Bewertung` können Sie eine Bewertung hinterlegen.|
|5. Bestätigen Sie die Auswahl abschließend mit dem orangen Häkchen für Speichern auf der rechten Seite.|

!!! warning "Sehr wichtig!"

    Die Ansicht kann durch den Typfilter entweder die `Fachlichen Leistungen` oder die Eintragungen zum `Allgemeinen Lern- und Arbeitsverhalten` anzeigen. Aktivieren Sie den Wechsel durch einen Klick auf das Filtersymbol.

![Hier ist die  Ansicht gefiltert nach `Allgemeines Lern- und Arbeitsverhalten`](/assets/images/zeugnisdaten/zeugnisdaten35.png)

#### Sammelzuweisung von Kategorietafeln 

Rufen Sie die Sammelzuweisung bei einem beliebigen Schüler auf der Karte Arbeits- und Sozialverhalten über die Schaltfläche `Kategorietafel zuweisen` auf.
Wählen Sie die Schüler aus, Sie können dabei die Funktionen [`Sortieren`, `Gruppieren` oder auch `Filtern`](https://doc.magellan.stueber.de/schulverwaltung/howto/sort-group-filter-search/) nutzen. Sind die gewünschten Schüler markiert, klicken Sie auf `Weiter`.

Wählen Sie die gewünschte Kategorietafel aus. Mit der Option `Vorhandene Kategorie der Schüler nicht löschen` können Sie steuern, ob die Kategorien der neuen Tafel ergänzt werden sollen oder anstelle der vorhandenen Kategorien zugewiesen werden sollen. Schließen Sie den Assistenten mit `Weiter` und `Fertigstellen` ab.

!!! warning "Sehr wichtig!"

    Mit dem Zuweisen einer Kategorietafel können Einträge für die `Fachliche Leistungen` und das `Allgemeine Lern- und Arbeitsverhalten` für alle Schüler eines Jahrgangs in einem Arbeitsgang zugewiesen werden.

#### Kategorietafeln extrahieren

Haben Sie bei einem Schüler bereits Eintragungen vorgenommen, können Sie daraus auch eine Kategorietafel erzeugen um sie anderen Schülern gesammelt zu zuweisen.
Klicken Sie dafür beim Schüler auf die Schaltfläche `Kategorietafel extrahieren…` und vergeben ein Kürzel und einen aussagekräftigen Langnamen. Anschließend können Sie wie im vorhergehenden Abschnitt beschrieben die Kategorietafel weiteren Schülern zuweisen.

#### Ergänzungen anlegen

Gebunden an eine Inhaltetafel kann zusätzlich eine Ergänzung für einen Schüler frei formuliert werden. Beispielsweise soll auf dem Zeugnisbericht eines Schülers für das Fach Deutsch in der Klasse 4b ein besonderer Hinweis erscheinen. 

|So geht's|
|:--|
|1.  Um einen neue Ergänzung anzulegen, klicken Sie auf die Plusschaltfläche im rechten unteren Bereich |
|2. Wählen Sie eine Inhaltetafel aus und verfassen anschließend im Textfeld `Ergänzungen` die Anmerkung. Speichern Sie bitte über das Häkchen im rechten unteren Bereich. <br/><br/>![Ergänzung für das Fach Deutsch erfasst](/assets/images/zeugnisdaten/zeugnisdaten36.png) |

