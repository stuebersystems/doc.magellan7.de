# Was ist neu?

Die nachfolgenden Abschnitte richten sich an die Nutzer von Magellan 6. Wir möchten Ihnen gern eine Übersicht über die offensichtlichsten Änderungen geben.

## Allgemeines

### UTF8

Für die neue Version von Magellan wird eine leere Datenbank zur Verfügung gestellt, die den Zeichensatz UTF8 unterstützt. In diese Datenbank werden mit einer Funktion des Magellan Administrators Ihre Schulverwaltungsdaten übergeben.
Durch den von der Datenbank und auch von der neuen Oberfläche unterstützten Zeichensatz, können jetzt alle Zeichen in Magellan gespeichert werden und demzufolge auch beispielsweise für den Zeugnisdruck wieder ausgegeben werden.

### Neue Runtime-Version von Crystal Reports integriert

Mit Magellan 7 ist eine neue Schnittstelle zur Runtimeversion von Crystal Reports eingebunden worden, damit können jetzt auch aktuellere Funktionen von Crystal Reports in der Druckvorschau von Magellan angezeigt werden.

!!! warning "Wichtig"

    Wenn Sie unsere ausgelieferten Magellan 7-Berichte als Vorlage für eigene Anpassungen nutzen möchten, benötigen Sie mindestens die Ausgabe Crystal Reports 2013. 

!!! warning "Wichtig"

    Durch die neue implementierte Runtimeversion von Crystal Reports müssen selbst erstellte Berichte angepasst werden. Die Berichte in unserer Auslieferung sind bereits umgestellt worden. Eine Anleitung welche Schritte für Ihre eigenen Berichte notwendig sind, finden Sie im Abschnitt ["Berichte für Magellan 7 anpassen"](/schulverwaltung/update/Berichte_anpassen)

### Neue Nachrichtenfunktion

Die Magellan-Willkommensseite wurde neu gestaltet und enthält jetzt zu den wichtigsten Aufrufen (Dokumentation, Newsletter, Ticketsystem usw.) einen Nachrichtenbereich, über den wir Sie auf dem Laufenden halten werden. Sie erhalten diesen Überblick auch auf beim Aufruf des Magellan ADMINISTRATORs und der Magellan Bibliothek.

![Willkommenseite mit Nachrichten](/assets/images/neues/13.png)
  
## Magellan 7

### Schüler pausiert

Ab Magellan 7 gibt es einen neuen Status um Schüler, die vorübergehend Ihre Schule nicht besuchen (zum Beispiel weil ein Auslandsjahr absolviert wird), markieren zu können.
Tragen Sie als erstes die für Ihre Schule relevanten Gründe unter `Extras > Schlüsselverzeichnisse > Fehlgründe` mit ein. 
Vergeben Sie pro Grund bitte mindestens ein Kürzel und eine Bezeichnung.

In der Schülerauswahlliste markieren Sie den Schüler und wählen `Rechtsklick > Status zuweisen`.
Wählen Sie "Abwesend", einen Abwesenheitsgrund (hier werden Ihre vordefinierten Fehlgründe gezeigt) und ein Startdatum!

![Wählen Sie "Abwesend", einen Abwesenheitsgrund und ein Startdatum!](/assets/images/neues/pausieren01.png)

Alle ausgewählten Schüler erhalten ein neues Statussymbol, damit Sie in der Auswahlliste zwischen den Status aktiv, inaktiv und pausierend unterscheiden können.

| Status                                  | Bedeutung                           |
| --------------------------------------- | ----------------------------------- |
| <img src="/assets/images/neues/pausieren02.png"> | Aktiv, der Schüler besucht aktuell die Schule und wurde nicht ausgeschult |
| <img src="/assets/images/neues/pausieren03.png"> | Inaktiv, der Schüler besucht aktuell nicht mehr die Schule und wurde ausgeschult |
| <img src="/assets/images/neues/pausieren04.png"> | Pausierend, der Schüler besucht vorübergehend nicht die Schule, ist aber nicht ausgeschult |

Auf der Laufbahnkarte gibt es einen neuen Bereich, in dem die Zeiten dieser Abwesenheiten aufgelistet und editiert werden können.

![Die Eintragungen können auf der Laufbahnkarte editiert werden](/assets/images/neues/pausieren05.png)

Kehrt der Schüler zurück an Ihre Schule, können Sie ihn auf zwei Wegen wieder als aktiven Schüler markieren.

Ansicht|Vorgehen
-|-
`Schüler > Auswahlliste`|`pausierend -> aktiv`<br/>Markieren Sie den Schüler und wählen `Rechtsklick > Status zuweisen`. Sie wählen `aktiv` und werden gefragt, ob das aktuelle Datum als Ende der Pause erfasst werden soll. Alternativ können Sie auch ein abweichendes Datum direkt auf der Laufbahnkarte vergeben.<br/> <br/>`pausierend -> inaktiv`<br/>Kehrt der Schüler nach der Pause nicht an Ihre Schule zurück, können Sie auch den Wert `inaktiv` wählen, bitte tragen Sie anschließend noch ein Abgangsdatum ein.
`Schüler > Laufbahn`|`pausierend -> aktiv`<br/>Sie tragen das `Bis-Datum` ein, beim Speichern (Hakensymbol im Abwesenheitsfenster) wird gefragt, ob Sie den Schüler gleich wieder aktivieren möchten.

### Anzeige des Status

Auf den einzelnen Registerkarten werden oben links weitere Informationen in Form von Symbolen eingeblendet. Links wird der Status des Schülers gezeigt (aktiv, inaktiv, pausierend), daneben kann mit einem "V" die Volljährigkeit (berechnet aus dem Tagesdatum und dem Geburtsdatum des Schülers) gezeigt werden. Ein Kreis mit einem Ausrufezeichen soll Sie darauf hinweisen, dass unter `Daten 3` das Häkchen für `Geheim` aktiviert wurde.

| Status                                  | Bedeutung                           |
| --------------------------------------- | ----------------------------------- |
| <img src="/assets/images/neues/09.png"> | Schüler ist volljährig              |
| <img src="/assets/images/neues/10.png"> | Schüler wurde als `geheim` markiert |

![Anzeige des Status auf den Unterregisterkarten der Schüler](/assets/images/neues/08.png)

### Klassen parallel besuchen

Sollte es an Ihrer Schule notwendig sein, dass ein Schüler zeitgleich mehreren Klassen zugeordnet wird, können Sie das jetzt in Magellan darstellen. Es gibt immer eine Stammklasse (S), der die Schüler als erstes zugeordnet werden. Zusätzlich kann ein Schüler weitere Nebenklassen (N) besuchen. Ob die Schülerzeile zur Stamm- oder Nebenlaufbahn gehört, sehen Sie in der neuen Spalte `Laufbahn` in der Auswahlliste `Schüler` Nach diesem Eintrag können Sie auch wie gewohnt Filtern oder Sortieren usw.

Benennung|Was ist gemeint|Kennzeichnung/Menü
--|--|--
**Stammschüler**|Ist der Schüler, der einmalig angelegt wurde<br/>über seine ID werden Schüler- oder Bewerberkopien verknüpft werden|Menü `Schüler`<br/> Laufbahn mit `S` gekennzeichnet 
**Bewerberkopie**|Ist eine Kopie, die über die Funktion `Als Bewerber kopieren` angelegt wurde|befindet sich im Menü `Bewerber`<br/>hat einen Eintrag in der Spalte `IDIntern`
**Schülerkopie**|Ist ein ins Schülermenü übernommener und<br/> parallel zum Stammschüler in eine andere Klasse als zuvor eingeschulter Schüler|Menü `Schüler`<br/> Laufbahn mit `N` gekennzeichnet 

Ein Beispiel:

Die Schülerin Monika Ehrenberg (Stammschüler) besucht aktuell die Klasse BK2017A:

![die Schülerin in ihrer `Stammklasse`](/assets/images/neues/lb01.png)

Zusätzlich soll sie der Klasse Abendschule zugeordnet werden. Dafür wird die Schülerin als Bewerberin ins Menü `Bewerber` kopiert (Bewerberkopie) .

![Schüler als Bewerber kopieren](/assets/images/neues/lb02.png)

Bei diesem Schritt wird eine Kopie der Stammdaten von der Karte `Daten1` bis `Extras` extrahiert und mit einer neuen ID im Menü `Bewerber` angelegt. Zusätzlich wird im Feld `IDIntern` die Schüler-ID des originalen Schülerdatensatzes gespeichert.
Es werden für den Bewerber nicht die Daten des Reiters `Ausbildung` und  `bereits besuchten Schulen` (Reiter `Zugang/Abgang`) übernommen. Für den Bewerber anschließend erfasste Daten des Reiters `Ausbildung` und  `bereits besuchten Schulen`, werden später beim Einschulen des Bewerbers mit den Einträgen des Stammschülers und etwaigen Schülerkopien verbunden.

![Bewerberkopie](/assets/images/neues/lb03.png)

Im nächsten Schritt wird die Bewerberkopie wie gewohnt mit dem Bewerberverfahren `F7` wieder ins Menü `Schüler` übernommen. Schulen Sie die Schülerin in die gewünschte Klasse (aus der Bewerberkopie wird eine Schülerkopie) ein, den Haken `Schüler zusammenführen` gibt es nicht mehr, es wird jetzt generell das Feld `IDIntern` überwacht.

Es kann jetzt zwei Situationen beim Einschulen geben:

Situation|Was passiert
--|--
Stammschüler und Schülerkopie sind im selben Halbjahr|Wenn der Stammschüler bereits in dem Halbjahr indem Sie die Kopie einschulen existiert, werden die beiden Schüler nicht miteinander verbunden, sondern die Schülerkopie wird mit dem Laufbahneintrag `N` für Nebenklasse zusätzlich in der Auswahliste gezeigt. Auf der Laufbahnkarte des Stammschülers ist aber die Nebenlaufbahn mit sichtbar.<br/>![Darstellung in der Auswahlliste](/assets/images/neues/lb05.png)<br/> ![Laufbahnkarte](/assets/images/neues/lb06.png)<br/><br/> Die S- und N-Schüler werden beim Fortschreiben jeweils in ihren Klassen fortgeschrieben oder versetzt. Möchten Sie für die  Schüler Zeugnisse drucken, ist das problemlos möglich, zu jeder Laufbahn hat man eine dazugehörige Zeugniskarte, die individuell pro Zeitraum gefüllt wird. 
Stammschüler und Schülerkopie sind in unterschiedlichen Halbjahren| Der Stammschüler und die Schülerkopie werden miteinander verbunden, es existiert nur eine Zeile in der Schülerliste mit dem Laufbahneintrag `S`

#### Stammdaten

Wer | Wie wird verfahren?
--|--
Stammschüler, Bewerber, Schülerkopie | Mit Stammdaten sind die Einträge des Reiters `Daten1` bis zur Karte `Extras` gemeint, eine Ausnahme bilden die Daten zu den `bereits besuchten Schulen` auf der Karte `Zugang/Abgang`. <br/>Wird beim Stammschüler, bei der Bewerberkopie oder bei der Schülerkopie ein Feld geändert, wird beim Speichern geprüft, ob es den Schüler mehrfach gibt, der geänderte Wert wird dann mit für alle weiteren gefundenen Schüler übernommen. Die Daten sind also bei allen drei Varianten identisch, egal von wem aus etwas geändert wird.

#### Ausbildung, Bereits besuchte Schulen

Wer | Wie wird verfahren?
--|--
Stammschüler, Schülerkopie|Für die Daten in den Bereichen `Ausbildung`, `Bereits besuchte Schulen` und die `Familiendaten` werden für die Schülerkopie immer die Daten es Stammschüler gezeigt. Eine Änderung bei einem der über die ID-Intern miteinander verknüpften Schüler, zeigt also die Änderung immer auch für die anderen Datensätze an. <br/> **Wichtig:**<br/> Eine Ausnahme ist das Feld `Schüler > Ausbildung > Ausbildung`, in dem Feld wird die aktuelle Ausbildung des Schüler hinterlegt, die wird individuell pro Stammschüler oder Schülerkopie gespeichert.
Bewerber | Beim Erstellen einer Bewerberkopie werden nicht die Daten des Reiters `Ausbildung` und die der `bereits besuchten Schulen` übernommen. Pflegen Sie diese Daten im Bewerbungszeitraums für den Bewerber, werden diese Daten dann beim späteren Einschulen des Bewerbers in seine Zielklasse mit den beim Stammschüler gespeicherten Daten ergänzt.

#### Familiendaten

 Wer | Wie wird verfahren?
--|--
 Stammschüler, Bewerber, Schülerkopie |Für die `Familiendaten` werden für den Stammschüler, Schülerkopien und Bewerber immer die Daten es Stammschülers gezeigt. Eine Änderung bei einem der über die ID-Intern miteinander verknüpften Schüler, zeigt also die Änderung immer auch für die anderen Datensätze an.

#### Zeugnisdaten

Wer | Wie wird verfahren?
--|--
Stammschüler, Schülerkopie |Auf sämtlichen Unterkarten unter `Schüler > Zeugnis` sind die Daten pro einzelner Schülerkopie gespeichert, hier hat der Schüler je Klassenzugehörigkeit individuelle Daten.

#### Dokumentenverzeichnis

In Magellan können für Bewerber/Schüler (auch für Lehrer, Klassen, Mandanten, Personen und Sorgeberechtigte) Dateien in eine individuelles Verzeichnis gespeichert werden. Dieses Verzeichnis kann über die Magellan-Oberfläche aufgerufen werden, die Dateien werden aber auf dem Magellan-Serverrechner gespeichert. Wenn man einen Kopie eines Schülers erstellt, dann wird für diese Schülerkopie immer das Dokumentenverzeichnis des Stammschülers gezeigt.

### Schülerlaufbahnkarte

Unter `Schüler > Laufbahn` ist die Spalte mit den Laufbahninformationen in der Breite veränderbar oder kann auch geschlossen werden.

![Eingaben für Mitglieder](/assets/images/neues/lb07.png)

### Vorbelegung der Herkunftsschule beim Kopieren

Im Menü `Schulen` können Schulen als Favoriten markiert werden. Wechseln Sie ins Menü `Schulen`, klicken eine Schule mit rechter Maustaste an und wählen im Kontextmenü `Zu Favoriten hinzufügen`. In der Liste der Schulen werden favorisierte Schulen mit einem gefüllten Herz dargestellt. Die Schulenliste wird standardmäßig nach diesem Merkmal sortiert. 

![Per `Rechtsklick > zu Favoriten hinzufügen` können Schulen als Favoriten hervorgehoben werden](/assets/images/neues/fav01.png)

In der Funktion "Als Bewerber kopieren", die Ihnen aus einem Schüler eine Kopie im Menü `Bewerber` erzeugt, können Herkunftsschulen vorbelegt werden, dabei wird Ihnen die gesamte Schulenliste gezeigt, Ihre favorisierten Schulen werden immer oben angezeigt.

![Der Bewerberkopie wird eine Herkunftsschule zugeordnet](/assets/images/neues/fav02.png)


Beispiel: Ein Schüler Ihrer Schule bewirbt sich auf einen anderen Bildungsgang Ihrer Schule, Sie legen Ihre Schule in der Schulenliste an und favorisieren sie. Dann können Sie beim Erzeugen des Bewerbers Ihre Schule bereits auswählen. Der Bewerber hat dann unter `Bewerber > Zugang > bereits besuchte Schulen` bereits Ihre Schule als Eintrag.

### ehemalige Schüler als Bewerber kopieren

Bislang hat der Assistent immer die Schüler und ehemaligen Schüler des ausgewählten Zeitraums gezeigt, jetzt stehen im Assistentenfenster `als Bewerber kopieren` sämtliche Schüler oder ehemaligen Schüler zur Auswahl, Sie müssen nicht mehr den Zeitraum wechseln.

### Laufbahnsortierung nach Zeiträumen

Bislang waren die Laufbahneinträge der Schüler nach den Zugangs- und Abgangsdaten zur jeweiligen Klasse sortiert, ab der Version 7 ist die Sortierung an die Zeiträume gebunden. Damit werden die Einträge auch korrekt sortiert, wenn verkehrte oder keine Zugangs- und Abgangsdaten hinterlegt wurden.

### Navigationleiste

Sie können sich für die tägliche Arbeit mehr Platz auf Ihrem Bildschirm schaffen, indem Sie die Navigationsleiste minimieren.

![Navigation minimieren](/assets/images/neues/navi01.png)

![Navigation minimiert](/assets/images/neues/navi02.png)

### Spaltensichtbarkeit und Spaltenreihenfolge

In jeder Auswahlliste finden Sie jetzt links vor dem ersten Spaltenkopf ein kleines Listensymbol. Klicken Sie das Listensymbol an, Sie sehen eine Übersicht aller Spalten, die per Häkchen ein- oder ausgeblendet werden können. Die Spaltenposition in der Auswahlliste können Sie hier auch neu vergeben: Ziehen Sie per Maus in der Liste eine Spaltenüberschrift an ihre neue Position.

![Öffnen Sie über das Listensymbol die Organisationsansicht](/assets/images/neues/spalte01.png)

![Ändern Sie per Drag and Drop die Spaltenreihenfolge!](/assets/images/neues/spalte02.png)

### Menüband (Ribbon)

Magellan 7 hat eine neue Aufteilung oder Zusammenstellung der einzelnen Funktionalitäten. 
Wir haben je nach ausgewähltem Menüpunkt die Funktionalitäten zu Gruppen zusammengefasst. Im Bereich Schüler gibt es beispielsweise jetzt die Gruppen `Datenbank`, `Start`, `Extras`, `Hilfe`, `Schüler` und `Laufbahnprozesse`. `Schlüsselverzeichnisse` finden Sie jetzt gesammelt unter in der Gruppe `Extras` im Punkt `Schlüsselverzeichnisse`.
Beispiele:

![Gruppe `Start`](/assets/images/neues/ribbon01.png)

![Gruppe `Datenbank` mit dem Aufruf der `Optionen`](/assets/images/neues/ribbon02.png)

![Gruppe `Extras`](/assets/images/neues/ribbon03.png)

![Gruppe `Hilfe`](/assets/images/neues/ribbon04.png)

![Gruppe `Schüler`](/assets/images/neues/ribbon05.png)

![Gruppe `Laufbahnprozesse`](/assets/images/neues/ribbon06.png)

### Schlüsselverzeichnisse

Alle Schlüsselverzeichnisse finden Sie unter der Gruppe `Extras` unter dem Punkt `Schlüsselverzeichnisse` zusammengefasst. 

![Fenster `Schlüsselverzeichnisse`](/assets/images/neues/sv01.png)

Aufgrund der Vielzahl der Schlüsselverzeichnisse, gibt es auswählbare Untergruppen, die beim Aufruf Ihnen Verzeichnisse zu einem bestimmten Thema zusammengefasst darstellen. In der nachstehenden Abbildung ist die Gruppe `Merkmale` gewählt worden.

 ![Gruppenfilter für die Gruppe `Merkmale` ausgewählt](/assets/images/neues/sv02.png)

Im unteren Bereich des Schlüsselverzeichnisfensters finden Sie zwei Schaltflächen, einmal um alle Datensätze im markierten Verzeichnis auszuwählen und rechts daneben, eine neue Schaltfläche um die optimale Spaltenbreite im Verzeichnis einstellen zu können. Die gewählte Spaltenbreite wird gespeichert und beim Neustart wieder dargestellt.

![Schaltfläche am unteren Rand](/assets/images/neues/sv03.png)

Die Schaltfläche zum Editieren der Inhalte eines Verzeichnisses finden Sie links oben, hier können Sie in den Editiermodus wechseln oder zum Beispiel eine neue Zeile erzeugen. Wenn Sie ein Verzeichnis verlassen, indem Sie beispielsweise auf einen anderen Verzeichnisaufruf klicken, wird gegebenenfalls nachgefragt, ob gespeichert werden soll. Das gilt auch für das Verlassen des Fensters.

![Schaltflächen zum Editieren](/assets/images/neues/sv04.png)

In der Liste der Verzeichnisse und auch im Gruppenfilterfeld können Sie Einträge per inkrementeller Suche finden. Aktivieren Sie die Liste oder das Feld per Klick, tippen Sie anschließend Ihren Suchbegriff ein, es wird der gefundene Eintrag gezeigt.

!!! info "Hinweis"

   Unter dem Gruppenfilter `Allgemein`, der standardmäßig bei Aufruf des Schlüsselverzeichnisfensters gezeigt wird, werden sämtliche in Magellan verfügbaren Schlüsselverzeichnisse aufgelistet.

### Schülerfilter

Wenn Sie die Schülerliste aufrufen, sind erst einmal standardmäßig nur aktive oder inaktive Schüler sichtbar, die einer Klasse zugeordnet wurden. Möchten Sie gern Schüler sehen, die noch keine Klassenzuordnung haben, schalten Sie im Filterfenster von "Eingeschult" auf "Vagabunden". 
Durch die neue Aufteilung reduziert sich die Ladezeit für die Auswahlliste im Menü `Schüler`.

![Auswahl `Eingeschult` ](/assets/images/neues/eingeschult01.png)

![Auswahl `Vagabunden` ](/assets/images/neues/eingeschult02.png)

### Vagabunden korrigieren

Sollte ein Bewerber versehentlich ins Schülermenü übernommen worden sein, können Sie das mit dem Assistenten `Schüler korrigieren` wieder rückgängig machen. Wählen Sie im Menü `Schüler` in der Auswahliste im Filter `Status` den Wert `Vagabunden`. Es werden statt der eingeschulten Schüler alle noch nicht einer Klasse zugeordneten Schüler gezeigt. Rufen Sie anschließend `Laufbahnprozesse > Schüler korrigieren` auf, es werden Ihnen nur die Vagabunden gezeigt. Korrigieren Sie Vagabunden, werden diese wieder als Bewerber im Menü `Bewerber` gezeigt.

![Zeigen Sie über den Auswahlfilter die `Vagabunden` an! ](/assets/images/neues/filter01.png)

!!! info "Hinweis"

  Der Assistent zum `Schüler korrigieren` bietet zum Korrigieren eingeschulte Schüler oder Vagabunden an. Was gezeigt wird, steuert man mit der Auswahl im Filter `Status` in der Schülerauswahlliste.

### Namen in Landessprache

 In den Menüpunkten `Schüler`, `Bewerber`, `Personen`, `Lehrer` und `Sorgeberechtigte` gibt unter `Daten1` die Möglichkeit auf die Unterkarte `Alternativ` zu wechseln um dort Namen in Landessprache einzugeben, zum Beispiel um sie im Zeugnisdruck zu verwenden.

![Unterkarte `Alternativ` unter `Schüler > Daten1` ](/assets/images/neues/s01.png)

### Zusammengefasst: Daten1 und Familie

Es gibt unter `Bewerber` oder unter `Schüler` nicht mehr die Karte `Sorgeberechtigte`/`Familie`, stattdessen sind die Inhalte der alten Karten `Sorgeberechtigte`/`Familie` mit unter `Schüler/Bewerber > Daten1` zu finden.

![neue Daten 1-Karte im Schülermenü](/assets/images/neues/daten01.png)

### Zusammengefasst: Klassen > Zeiträume > Zeitraum und Schüler

Die beiden bislang getrennten Unterkarten unter `Klassen > Zeiträume > Zeitraum und Schüler` sind mit einander verbunden worden.

![neue Karte `Klassen > Zeiträume`](/assets/images/neues/k01.png)

### Zusammengefasst: Schüler > Daten2 und Schüler > Zugang/Abgang

Es gibt unter `Schüler` oder unter `Bewerber` nicht mehr die Karte `Zugang/Abgang` bzw. `Zugang`, stattdessen sind die Inhalte der beiden Karten zusammengefasst unter `Schüler/Bewerber > Daten2` zu finden.

![neue Karte `Schüler/Bewerber > Daten2`](/assets/images/neues/daten2.png)

### Drittes Geschlecht für Bewerber und Schüler

Unter `Bewerber/Schüler > Daten1 > Geschlecht` kann der Wert `divers` gewählt werden. 
  
### Schülerfehlzeiten

Beim Aufruf der Schülerfehlzeiten werden jetzt immer alle bisher erfassten Fehlzeiten gezeigt, den Standardfilter können Sie über die Schaltfläche `Anpassen` weiter eingrenzen.

![Fehlzeitenfenster, aufrufbar in der Schülerauswahlliste mit STRG+F](/assets/images/neues/schueler_36fehlzeiten.png)

### Sorgeberechtigte: Kinder-Karte ohne Zeitraumfilterung

Im Menü `Sorgeberechtigte` werden auf der Unterkarte `Kinder` sämtliche jemals dem Sorgeberechtigten zugeordneten Schüler oder Bewerber gezeigt. Um zwischen den aktuellen Schülern, den Bewerbern und den Schülern, die die Schule inzwischen nicht mehr besuchen unterscheiden zu können, wird der `Status` einblendet. Zusätzlich gibt es eine Spalte `Zeitraum`, die den durch den Schüler zuletzt besuchten Zeitraum einblendet. Bei Bewerbern ist das Feld `Status` und das Feld `Zeitraum` nicht gefüllt.

Per Doppelklick auf eine der Kinderzeilen wechselt Magellan die Ansicht (Menü `Schüler` oder `Bewerber`) und ggfs. auch den Zeitraum.

![](/assets/images/neues/sb.png)

### Neues Modul "Gruppen"

Der neue Bereich `Gruppen` dient der Verwaltung von Gruppen oder Gremien, deren Mitglieder aus den Menüpunkten `Schüler`, `Lehrer`, `Personen` oder `Sorgeberechtigte` bestehen können.
Sie definieren Ihre gewünschten Gruppen, zum Beispiel für den Förderverein, den Elternbeirat, eine Arbeitsgemeinschaft, einen Lehrer-Eltern-Chor usw. Für eine Gruppe sind folgende Angaben möglich:

 ![Eingaben für Gruppen](/assets/images/neues/g01.png)
 
 Anschließend wählen Sie die Mitglieder der Gruppe aus. Einem Mitglied kann auch ein Typ zugewiesen werden, Sie definieren vorab selbst eine Liste von möglichen Typen, beispielsweise: Kassenwart, Leiter, ruhendes Mitglied usw.
 
  ![Eingaben für Mitglieder](/assets/images/neues/g02.png)
  
  Selbstverständlich können Mitglieder auch verschiedenen Gruppen angehören.
  
!!! warning "Wichtig"

    Für die Nutzung dieses Punktes benötigen Sie die Freischaltung per Lizenz.


## Magellan 7 Administrator

Die nachfolgenden Abschnitte richten sich an die Nutzer von Magellan 6, wir möchten gern eine Übersicht über die offensichtlichsten Änderungen geben.

### Aufteilung

Der Magellan Administrator wurde vollständig überarbeitet und neu gestaltet. Nicht mehr verwendete Teile sind entfernt worden, alle Punkte wurden übersichtlich zusammengefasst.

### UTF8

Für die neue Version von Magellan wird eine leere Datenbank zur Verfügung gestellt, die den Zeichensatz UTF8 unterstützt. In diese Datenbank werden mit einer Funktion im Magellan Administrator Ihre Schulverwaltungsdaten übergeben. Durch den von der Datenbank auch von der neuen Oberfläche unterstützten Zeichensatz können jetzt alle Zeichen in Magellan gespeichert werden und demzufolge auch zum Beispiel für den Zeugnisdruck wieder ausgegeben werden.

### Nachträgliches Anmelden

Der Magellan Administrator ist auch ohne Datenbankanmeldung startbar, allerdings sind dann nur die Punkte `Server-Verwaltung` und `Datensicherung` verwendbar. Neu ist, dass man sich jetzt aus der Oberfläche heraus noch nachträglich an einer Datenbank anmelden kann, der Magellan Administrator muss dafür nicht neu gestartet werden.

### Importieren eigener Kataloge

Unter `Datenaustausch > Kataloge (Schlüsselverzeichnisse) importieren` gibt es unter "Importiere für Land/Bundesland" zusätzlich auch die Auswahlen "Benutzer" und "Ausland".

![Datenaustausch > Kataloge (Schlüsselverzeichnisse) importieren](/assets/images/neues/a01.png)

![Datenaustausch > Kataloge (Schlüsselverzeichnisse) importieren](/assets/images/neues/a02.png)

Speicherort des Verzeichnisse ist standardmäßig unter C:\Users\Public\Documents\Stueber Systems\Magellan 7\Importe\Benutzer. Legen Sie in diesem Verzeichnis Ihre editierten Kataloge ab und importieren sie dann in die Datenbank.

### Navigationleiste

Sie können sich für die tägliche Arbeit mehr Platz auf Ihrem Bildschirm schaffen, indem Sie die Navigationsleiste minimieren.

![Navigation minimieren](/assets/images/neues/a03.png)

![Navigation minimiert](/assets/images/neues/a04.png)

### Menüband (Ribbon)

Magellan 7 hat eine neue Aufteilung oder Zusammenstellung der einzelnen Funktionalitäten. 
Wir haben je nach ausgewähltem Menüpunkt die Funktionalitäten zu Gruppen zusammengefasst. Im Bereich Schüler gibt es beispielsweise jetzt die Gruppen `Datenbank`, `Start` und `Hilfe`.

### Verbindungen anlegen

Der Dialog zum Anlegen von Datenbankverbindungen wurde vollständig überarbeitet. Es gibt zusätzlich die Möglichkeit jetzt pro Verbindung die Bundeslandauswahl zu treffen, je Datenbank Angaben für die Datensicherung vorzunehmen, beim Eintrag der Datenordnerpfade sich eine Menge Tipparbeit zu sparen, eine neue Übersicht mit Verbindungsinformationen und die unkomplizierte Möglichkeit in der Übersicht mit einem Häkchen eine neue Standardverbindung auszuwählen. 

![Neuer Dialog zum Anlegen von Verbindungen](/assets/images/neues/a05.png)

![Voreinstellungen zur Datensicherung pro Verbindung](/assets/images/neues/a07.png)

![Neuer Verbindungsübersicht](/assets/images/neues/a06.png)

![Markieren Sie per Häkchen Ihre neue Standardanmeldung](/assets/images/neues/a08.png)

### Verbindungen kopieren

Wenn Sie eine neue Datenbankverbindung aus einer Kopie, einer bereits gespeicherten Verbindung anlegen möchten, dann ist das möglich. Klicken Sie bitte mit der rechten Maustaste auf eine Verbindung und wählen `Verbindung kopieren`, es öffnet sich die Verbindungskopie. Im Anschluss passen Sie die kopierte Verbindung entsprechend an.

![Klicken Sie per rechter Maustaste (oder mit `STRG+C`) auf die zu kopierende Verbindung](/assets/images/verbindung.kopieren.png)

## MyMagellan Center 

Das MyMagellan Center ist Teil des Administrators geworden. Sie finden den Aufruf mit in der Menüleiste.

![Das neue MyMagellan Center](/assets/images/neues/myma.png)

### Verzeichniswerte

Beim Erstellen der MyMagellan-Dateien werden auch Inhalte aus den Schlüsselverzeichnissen übergeben.

!!! info "Hinweis"

	In die MyMagellan-Dateien werden ausschließlich aktuelle Verzeichniswerte (Noten, Fachstatus, Unterrichtsarten, Abschlüsse usw.) übergeben. Das bedeutet Verzeichniswerte,  deren `Bis-Datum` im Magellan-Verzeichnis (`Magellan > Extras > Schlüsselverzeichnisse`) leer ist oder ein Datum enthält, dass vom Tag der Erstellung aus gesehen in der Zukunft liegt.

## MyMagellan

Neue vereinfachte Übersicht nach Schülern und nach Fächern:

![Eingabe nach Fächern](/assets/images/neues/01.png)

![Eingabe nach Schülern](/assets/images/neues/02.png)

![Eingabe von Zeugnisdaten](/assets/images/neues/03.png)

![Eingabe von Zeugnisbemerkungen](/assets/images/neues/05.png)

### Neue Sammelzuweisung

Für die Eingabe der weiteren Zeugnisdaten steht eine Sammelzuweisung für die Unterblöcke `Abschlussdaten` und `Versetzungs- und Zeugnisdaten` zu Verfügung.

![Sammelzuweisung für Zeugnisdaten](/assets/images/neues/04.png)

## Magellan Bibliothek

### Zeitraumbezug entfernt

Die Ansicht `Schüler` hat keine Zeitraumauswahl mehr und zeigt alle aktiven und inaktiven Ausleiher mit der aktuellen oder zuletzt besuchten Klasse an. Sie können Ihre Liste über die Spalten `Status` und `Zeitraum` individuell filtern.

### neuer Status

In der Ansicht `Schüler` wird als dritter Status (zusätzlich zu aktiv und inaktiv) ein roter gefüllter Kreis für Schüler gezeigt, die nur noch in der Bibliothek als Ausleiher existieren, in Magellan aber gelöscht wurden.
Durch diese Anzeige (und auch den Status für inaktive) Schüler, können Sie gezielt nach dem Status und auch nach dem Symbol für Vorgänge filtern und diese Ausleiher aus der Bibliothek entfernen.

!!! info "Hinweis"

  Ausleiher, den noch offene Ausleihvorgänge zugeordnet sind, können nicht gelöscht werden.

![Ansicht `Schüler` in der Bibliothek](/assets/images/neues/07.png)  
