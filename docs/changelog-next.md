# Voraussichtliche Änderungen

Sie erhalten hier einen Überblick über die voraussichtlichen Änderungen und Korrekturen für das nächste Serviceupdate. Die nachfolgend gelisteten Änderungen wurden noch nicht veröffentlicht.

## LEGENDE

| Abkürzung | Bedeutung |
| --- | --- |
| FIX | Korrektur bestehender Funktionalität |
| NEW | Neue Funktionalität |
| CHANGE | Änderung des Ablaufs, Verarbeitung oder Bedienung |

---

## 7.0.12 - 705

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### MAGELLAN

* FIX: `Schüler > Laufbahnprozesse > Schüler korrigieren` mit abgestuften Benutzerrechten wurde angepasst
  
!!! info "Hinweis"
  
      Bitte beachten Sie, dass das `Zugriffsrechte synchronisieren` im Modul MAGELLAN ADMINISTRATOR (Menüpunkt Benutzerverwaltung) vorab durchgeführt werden muss!

* FIX: Passfotofunktion unter `Bewerber > Daten1` und unter `Lehrer > Daten1` ergänzt
* FIX: im Lehrermenü kann `Auswahlliste > Lehrer markieren > Rechtsklick` das Fehlzeitenfenster aufgerufen werden
* FIX: Die Funktionalitäten unter `Schüler > Zeugnis > Bemerkungen` wurden überarbeitet
* FIX: `Abitur > Bemerkungen > Sammelzuweisung`: zur Auswahl stehende Schüler werden korrekt gefiltert
* FIX: Unter das Schnittstellenfenster unter `Extras > Export > Export` gibt entsprechende Meldungen aus oder lässt Sie den Assistenten nicht weiterbedienen, wenn keine Schnittstelle oder kein Zeitraum gewählt wurde.
* FIX: Speichern von Schülerfehlzeiten
* FIX: Erste bereits besuchte Schule des Bewerbers (`Bewerber > Daten2`) wird standardmäßig als Herkunftsschule gesetzt
* FIX: Beschriftung des Doublettenprüfungsfensters für Lehrer korrigiert
* FIX: Korrektur der Anzeige des Status (S und N statt H und N für Stamm- und Nebenschüler) unter `Sorgeberechtigte > Kinder`
* FIX: Aufruf der Serienmail aus dem Menü `Bewerber` ergänzt
* FIX: Aufruf `Abitur > Drucken > Zeugnisse` ergänzt
* FIX: `Schüler > Daten2 > Abgangsart` Kürzellänge von 20 Zeichen wird akzeptiert
* FIX: `Schüler > Laufbahnprozesse > Ausschulen > Abgangsart` Kürzellänge von 20 Zeichen wird akzeptiert
* FIX: Geschwindigkeit beim Zuweisen des Status (aktiv, inaktiv, pausierend) in der Schülerauswahlliste optimiert
* FIX: `Klassen > Daten > Abteilung` Problem beim Speichern behoben
* FIX: Unter `Extras > Schlüsselverzeichnisse > Noten` wurden die Spalten `Von` und `Bis` ergänzt.
* FIX: Korrektur der Sammelzuweisung unter `Schüler > Abitur > Zeugnisbemerkung`
* NEW: Auf den Registerkarten im Menü `Schüler` werden jeweils am oberen Rand Symbole für den Status (aktiv, inaktiv, pausierend), ggfs. die Volljährigkeit (Berechnet anhand des Tagesdatums und des Geburtsdatums) und/oder der Status `Geheim` (Häkchen von Daten 3) eingeblendet.

![Symbole auf den Schülerregisterkarten](/assets/images/changelog/7.0.12.02.png)

### SAXSVS

* CHANGE: Wenn bei einem Schüler der Haken unter `Schüler > Daten 2 > NdH` aktiviert/wieder deaktiviert wird, wird entsprechend der Knoten für Migration erzeugt/nicht erzeugt.

### MAGELLAN BIBLIOTHEK

* NEW: Die Ansicht `Schüler` hat keine Zeitraumauswahl mehr und zeigt alle aktiven und inaktiven Ausleiher mit der aktuellen oder zuletzt besuchten Klasse an. Sie können Ihre Liste über die Spalten `Status` und `Zeitraum` individuell filtern.
* CHANGE: neue Symbole in der Medienansicht
* FIX: Verschieben in anderen Katalog korrigiert
* FIX: Text im Assistenten zum manuellen Anlegen eines neuen Mediums korrigiert
* FIX: Assistent zur Übernahme neuer Lehrer korrigiert
* FIX: neue Symbole für die Auswahl der Exemplare in der Ausleihe
* FIX: Rückgabe per eingescanntem Buch korrigiert
* FIX: angezeigte Punkte unter `Extras > Berichte organisieren` und `Extras > Vorlagen organisieren` angepasst
* FIX: Schüler ( = Ausleiher aus Bibliothek) löschen korrigiert
* FIX: Personen hinzufügen korrigiert

### MyMAGELLAN

* NEW:

### MAGELLAN Administrator

* CHANGE: Die Skriptdatei `Zugriffsrechte zuweisen` wurde um neue Bestandteile der Datenbank ergänzt. Bitte synchronisieren Sie die Zugriffsrechte über die Schaltfläche im `MAGELLAN-ADMINISTRATOR > Benutzerverwaltung > Zugriffsrechte` synchronisieren.
  
![Zugriffsrechte synchronisieren](assets/images/changelog/7.0.12.01.png)

* NEW: `Datenbankpflege > Gemeinden synchronisieren` wurde ergänzt um Sorgeberechtigte, damit können nachträglich Gemeindekennziffern für Sorgeberechtigte ergänzt werden, wenn die PLZ und der Ort einem Eintrag im Verzeichnis der Postleitzahlen zugeordnet werden können.
* FIX: Anzeige der Rechtegruppe `Statistikadmin` in der Übersicht der Benutzer
* FIX: Unter `Datenbankverbindung > Wiederherstellen` wird beim Öffnen eines Pfades (Schaltfläche am Ende des Pfadfeldes) direkt der eingestellte Zielpfad geöffnet.

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: 

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur von MAGELLAN 7 angepasst:

* FIX: Klassenliste mit Klassendaten.rpt
* FIX: Klassenliste (Sorgeberechtigte und Geburtsdatum).rpt
* FIX: Klassenliste inkl. ausgeschulter Schüler.rpt
* FIX: Klassenliste mit Eltern2.rpt
* FIX: Klassenliste mit Endnoten.rpt
* FIX: Klassenliste Schüler-Notenmatrix (mit Verhalten und Mitarbeit).rpt
* FIX: Klassenliste Schüler-Notenmatrix (Querformat).rpt
* FIX: Klassenliste Schüler-Notenmatrix.rpt
* FIX: Prüfungsliste.rpt
* FIX: Berichte\Klassen\Klassenliste (Sorgeberechtigte und Geburtsdatum).rpt
* FIX: Berichte\Klassen\Saarland\SAR-Klassen-Notenliste Halbjahr Lernfeld MBK.rpt
* FIX: Berichte\Klassen\Saarland\SAR-Klassen-Notenliste Abgeschlossene Lernfelder MBK.rpt
* FIX: Berichte\Klassen\Rheinland-Pfalz\Klassenliste mit Endnoten.rpt
* FIX: Berichte\Klassen\Nordrhein-Westfalen\Zeugnisliste BBS (nur für Minderjährige).rpt
* FIX: Berichte\Klassen\Nordrhein-Westfalen\Zeugnisliste BBS.rpt
* FIX: Berichte\Schueler\Bescheinigung über Schülerübergabe.rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GY-FHReife (Bescheinigung).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 1-2).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 3-4).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GY-ABI (2014).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-Studienbuch (Qualifikationsphase - zweite Seite).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-ABI-Meldung-MdlAbitur (Profil 2011).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-ABI (2015).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-Abi (Leistungskarte 2011).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AS (Klasse 5-10)(G8).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AS (Klasse 5-10)(G9).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AZ (A3)(2015).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-AZ (A3).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-FHReife (2011).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-FHReife (2015).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-HJZ (2008).rpt
* FIX: Berichte\Zeugnisse\Schleswig-Holstein\SHL-GY-HJZ (Profil).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 3-4).rpt
* FIX: Berichte\Zeugnisse\Niedersachsen\NIE-GS-AS (Klasse 1-2)
* FIX: Berichte\Zeugnisse\Schweiz\CH-Notenausweis-E-Profil-2003.rpt
* FIX: Berichte\Zeugnisse\Auslandsschulen\DAS-GY-ABI-Reifepruefung 2017.rpt
* FIX: Berichte\Zeugnisse\Auslandsschulen\DAS-GY-AZ mit FHR (Anlage 9b).rpt
* FIX: Berichte\Zeugnisse\Auslandsschulen\DAS-GY-AZ mit FHR (Anlage 9b).rpt
* FIX: Berichte\Klassen\Jahresnotenliste-BVJ.rpt
* FIX: Berichte\Schueler\Unfallanzeige (mit Erläuterungen).rpt
* FIX: Berichte\Schueler\Schülerstammblatt (Belegung der Arbeitsgemeinschaften).rpt
* FIX: Berichte\Schueler\Schülerpersonalblatt incl. Schuleintritt (Betriebe -Querformat).rpt
* FIX: Berichte\Schueler\Schülerpersonalblatt (nur mit Eltern und Vorbildung).rpt
* FIX: Berichte\Schueler\Schülerliste (zeitraumübergreifende Fehlzeiten).rpt
* FIX: Berichte\Schueler\Schülerausweis ohne Photo.rpt
* FIX: Berichte\Schueler\Schüler-Abi (Antrag mündliche Prüfung).rpt
* FIX: Berichte\Schueler\Schüler mit Herkunftsschulen.rpt
* FIX: Berichte\Schueler\Schüler mit Herkunftsschulen u. letzte Klasse.rpt
* FIX: Rheinland-Pfalz\RLP-BBS (Bescheinigung Niveaustufen).rpt
* FIX: Rheinland-Pfalz\RLP-BF-AS.rpt
* FIX: Rheinland-Pfalz\RLP-BF-AZ.rpt
* FIX: Rheinland-Pfalz\RLP-BF-HJZ (1. Variante).rpt
* FIX: Rheinland-Pfalz\RLP-BF-HJZ (2. Variante).rpt
* FIX: Rheinland-Pfalz\RLP-BF-HJZ (3. Variante).rpt
* FIX: Rheinland-Pfalz\RLP-BF-JZ (Oberstufe).rpt
* FIX: Rheinland-Pfalz\RLP-BF-JZ (Unterstufe).rpt
* FIX: Rheinland-Pfalz\RLP-BG (Punktekreditkarte-2010).rpt
* FIX: Rheinland-Pfalz\RLP-BG-ABI (2010).rpt
* FIX: Rheinland-Pfalz\RLP-BG-ABI (2010)A4.rpt
* FIX: Rheinland-Pfalz\RLP-BG-AS (Anlage D 48).rpt
* FIX: Rheinland-Pfalz\RLP-BGJ-AS.rpt
* FIX: Rheinland-Pfalz\RLP-BGJ-AZ (mit Zusatzbemerkung).rpt
* FIX: Rheinland-Pfalz\RLP-BGJ-AZ (ohne Zusatzbemerkung).rpt
* FIX: Rheinland-Pfalz\RLP-BGJ-HJZ (Variante 2).rpt
