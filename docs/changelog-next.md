# Voraussichtliche Änderungen

Sie erhalten hier einen Überblick über die voraussichtlichen Änderungen und Korrekturen für das nächste Serviceupdate. Die nachfolgend gelisteten Änderungen wurden noch nicht veröffentlicht.

## LEGENDE

Abkürzung | Bedeutung
--------- | ---------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

---

!!! danger "Achtung"

    Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

## 7.0.21 - 709

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### MAGELLAN

* NEW: In allen mit Schlüsselverzeichnissen hinterlegten Eingabefeldern (mit eingeblendeter Bezeichnung) wird hinter der Bezeichnung eine Klammer gezeigt. In der Klammer wird der Wert aus der Spalte Schlüssel gezeigt. Ist im Schlüssel kein Wert enthalten, wird stattdessen ein Strich "(-)" gezeigt. Damit können Sie auch ohne direkt im jeweiligen Schlüsselverzeichnis nachzusehen erkennen, ob ein Schlüsselwert und ob der korrekte Schlüsselwert für ggfs. statistische Auswertungen hinterlegt wurde.
* NEW: Für die Sammelzuzweisung unter `Schüler > Laufbahn > Allgemein und Abschluss` wurden zur einfacheren Auswahl der Schüler die Spalten `Beruf` und `Bildungsgang` eingeblendet.
* NEW: Neues Fenster mit Zusatzinformationen unter `Schüler > Schüler > Weitere Informationen`, über `STRG+I` oder über das schwarze Infosymbol aufrufbar! Dieses Fenster (aus jeder Unterkarte im Menü `Schüler` aufrufbar, auch in der Auswahlliste) enthält Informationen aus der Bewerbungsphase, über die aktuell besuchte Klasse und über die Ausbildung. Bitte beachten Sie die aktualisierte [Dokumentation](https://doc.magellan7.stueber.de/schulverwaltung/howto/schueler/#weitere-informationen)!


* CHANGE: SAXSVS: Für Sorgeberechtigte, die in der Schweiz wohnen, können Sie im Feld `Land` das Kürzel CH eingegeben, MAGELLAN übergibt diese Ausgabe dann als Schlüssel 158 in die Exportdatei.
* CHANGE: Wird beim Schüler die Adresse geändert und für die Sorgeberechtigten soll die Änderung auch übernommen werden, wird auch die Gemeinde des Schülers für die Sorgeberechtigten übernommen.
* CHANGE: Felder, die bislang nur in der Bundeslandauswahl Berlin sichtbar waren, sind in die Standardansichten integriert worden
* CHANGE: Die Karte `Schüler > Statistik` ist zur Karte `Schüler > Merkmale` zusammengefasst worden.
* CHANGE: `Modul MAGELLAN ABITUR` => Pro Halbjahr anlegbare Klassen auf 9 Klassen erhöht.
* CHANGE: Filtern des Feldes `Status` in den Verzeichnisfeldern unter `Schüler > Daten2 > Höchster Abschluss ABS/BBS`  ergänzt.
* CHANGE: Der Style sämtlicher Verzeichnisfelder unter `Schüler > Zeugnis > Fächer/Leistungen` wurde aktualisiert.
* CHANGE: Der Punkt `Schuljahreswechsel` ist vollständig überarbeitet worden und unter der Karte `Laufbahrprozesse > Klassen übernehmen` aufrufbar.   Bitte beachten Sie die aktualisierte [Dokumentation](https://doc.magellan7.stueber.de/schulverwaltung/howto/schuljahreswechsel/#assistent-klassen-ubernehmen-erstellt-neue-klassen)!

* FIX: Leere Fehlermeldung  und Fensterbeschriftung beim Start des Updates direkt auch MAGELLAN heraus behoben.
* FIX: Das Ablegen von Dokumenten beim Seriendruck für Nebenschüler wurde korrigiert.
* FIX: Das Ablegen von Dokumenten beim Druck für Nebenschüler wurde korrigiert.
* FIX: Trägt man eine neue Herkunftsschule unter `Schüler > Daten2 > Bereits besuchte Schulen` ein wird der Speicherung der Eintrag und die Herkunftsschule direkt aktualisiert.
* FIX: Das Feld `Sprache` [Kurssprachen] ist eingebbar unter `Schüler > Zeugnis > Fächer`.
* FIX: Unter `Datenbank > Optionen > Ein- und Ausblenden > Schüler/Bewerber Extras ausblenden` wird bei gesetztem Haken die Karte ausgeblendet
* FIX: Wenn im Menü Sorgeberechtigte die Postleitzahl oder der Ort eingegeben werden und mit TAB oder ENTER bestätigt wird, wird das Feld Gemeinde entsprechend der hinterlegten Schlüssels befüllt.
* FIX: Ist die Postleitzahl oder der Ort beim Sorgeberechtigten nicht eindeutig, wird bei der Wahl eines Wertes aus dem Unterfenster auch die Gemeindekennziffer befüllt.
* FIX: Bei der Übernahme einer Adressänderung eines Schülers oder Sorgeberechtigten, werden die Änderungen für den jeweils anderen korrekt übernommen.
* FIX: Ändern eines Kürzels im Verzeichnis `Unterrichtsart` für bereits verwendete Werte.

### MAGELLAN Administrator

* FIX: Datenübernahme 6 => 7: Die Tabelle `Sponsoren` und das gleichnamige Feld in der Tabelle `Betriebe` wurden ergänzt
* CHANGE: Das MAGELLAN-Importformat ist überarbeitet worden und steht aber dieser Ausgabe wieder zur Verfügung!

### MAGELLAN Bibliothek

* FIX:

### Skripte

* FIX: Schüler wechseln.dws => Beim Wechsel wird die aktuelle Ausbildung korrekt übernommen

### Statistik

* FIX:

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: DAS-Zeugnis Gymnasium - Mittlerer Schulabschluss (Anlage 10)(§23).rpt
* FIX: DAS-HS-MSA-AS (Anlage 8 und 9)(§23).rpt
* FIX: DAS-GY-ABI (DIA)(2019).rpt
* FIX: DAS-GS (Klasse 1-2).rpt
* FIX: DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt (ergänzt um das Feld "Ausbilder" im Bereich der Ausbildung)
* FIX: Schulbescheinigung für die Vergangenheit.rpt
* FIX: Schulbescheinigung (Vergangenheit mit Klasse).rpt