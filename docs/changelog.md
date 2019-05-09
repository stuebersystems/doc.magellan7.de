# Was ist neu?

Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN 7.

#### Weitere Änderungsverläufe finden Sie wie folgt

* [Geplante Änderungen der nächsten Ausgaben](/changelogs/changelog-next.md)
* [Neuerung zwischen MAGELLAN 6 und 7](/neu.mag7.md)

#### Hilfreiche Dokumentation zur Installation/Update

* [Anleitung zum Einspielen eines Serviceupdate.](/installation/update.md)
* [Probleme beim Einspielen des Updates?](/installation/probleme-beim-update.md)

### LEGENDE

Abkürzung | Bedeutung     
----------|----------
FIX       | Korrektur bestehender Funktionalität              
NEW       | Neue Funktionalität                              
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

---
## 7.0.8 - 703 (07.05.2019)

### SAXSVS

* FIX: Besondere Berücksichtigung von Stamm- und Nebenschülern



## 7.0.7 - 703 (29.04.2019)

### MAGELLAN

* FIX: Seriendruck an Praxisbetriebe in den Menüpunkten `Bewerber` und `Schüler` überarbeitet
* FIX: Problem beim Aktualisieren (F5) einer neuen Eingabe behoben 

### SAXSVS

* FIX: Export von Sorgeberechtigten angepasst


### MAGELLAN Administrator

* CHANGE: Export und Import von Benutzern unter `Benutzerverwaltung > Benutzer importieren/Benutzer exportieren` angepasst

## 7.0.6 - 703 (26.04.2019)

### MAGELLAN

* FIX: "Zuweisen von Zugriffsrechten.dws":  Fehlende Rechte auf "BewerberVerfahren", "BewerberFachdaten" und "BewerberUnterlagen" berücksichtigt , bitte führen Sie im MAGELLAN ADMINISTRATOR das "Zugriffsrechte synchronisieren" im Menüpunkt `Benutzerverwaltung` aus.

![Zugriffsrechte synchronisieren](../assets/images/changelog/7.0.7.01.png)

* FIX: Zeichenlänge auf 20 für die Kürzel der Verzeichnisse Anschluesse Extern und Abschluesse Intern erhöht.
FIX: Die ausführliche Anzeige wurde korrigiert für `Bewerber/Schüler > Daten 4 > Adresse/Förderung`
* FIX: `MAGELLAN > Daten4 > Verkehrsmittel`: Anzeige und Sortierung der Verzeichniswerte
* FIX: Bewerber-Serienmail integriert
* FIX: Schüler-Serienmail korrigiert
* FIX: Schüler- und Lehrerfehlzeitenfunktionalität korrigiert
* NEW: neue Verhältnisse Schüler-/Bewerber-Familien: Onkel, Tante, Bruder, Schwester, Erzieher, Notfall, Gasteltern
* FIX: Alle Kürzel auf 20 Zeichen in den Schlüsselverzeichnissen und in allen Ansichten angepasst
* FIX: Unter `Daten2 > Höchster Abschluss ABS/BBS > Abschluss` wurde jeweils die Anzeige im Verzeichnisfeld auf das Kürzel geändert.

### SAXSVS

* FIX: Problem beim Prüfen des Schülerbetriebes behoben
* CHANGE: In Absprache mit dem LASUB wurde Folgendes geändert: Bei unseren Sorgeberechtigtenprüfungen und beim Erzeugen der XML-Datei werden nur noch Schüler berücksichtigt, die ausgehend vom im Assistenten eingegebenen Stichtag und dem Geburtsdatum nicht volljährig sind. Bitte beachten Sie den Abschnitt [Sorgeberechtigte](https://doc.magellan7.stueber.de/regionales/sachsen/datenpflege.html#sorgeberechtigte--saxsvs-bbsschuelersorgeberechtigte)!
* NEW: Im Statistikassistenten unter `MAGELLAN > Extras > Exporte > Export` wird Ihnen beim Erstellen der XML-Datei für die Meldungen eine neue gesonderte Spalte mit dem jeweiligen Feld oder Bereich gezeigt. Damit können Sie nach dem Export der Meldungen diese sortieren und gezielter die Daten nachpflegen.

> #### warning::Wichtig!
>
> Bitte öffnen Sie `MAGELLAN > Extras > Schlüsselverzeichnisse > Schulformen (Herkunft)`. Wechseln Sie zur Zeile mit dem Schlüssel 115 und schalten den Bearbeitenmodus über das Stiftsymbol am oberen Fensterrand ein. Ändern Sie die Bezeichnung bitte auf das Wort **"Berufsvorbereitungsjahr"** und speichern diese Änderung.

![Bitte die Bezeichnung des Schlüssels 115 anpassen!](../assets/images/changelog/7.0.6.01.png)

### Importe

* CHANGE: Im Verzeichnis der `Abschluesse (Extern)` unter `MAGELLAN > Extras > Schlüsselverzeichnisse` wurde die Bezeichnung für den Schlüssel 115 geändert, korrekt ist die Bezeichnung: Berufsvorbereitungsjahr


### Skripte

* FIX: "Zuweisen von Zugriffsrechten.dws":  Fehlende Rechte auf "BewerberVerfahren", "BewerberFachdaten" und "BewerberUnterlagen" berücksichtigt  


### MAGELLAN Administrator

* NEW: Unter `Datenbankpflege` wurden die Funktionen  `Anrede setzen` und  `Passfoto löschen`ergänzt. Alle Aktionen werden in der [Dokumentation im Abschnitt Datenbankpflege](https://doc.magellan7.stueber.de/admin/datenbankpflege.html) beschrieben.
* FIX: Duplizieren von Benutzern angepasst
* NEW: Neue Funktionalität unter `Datenpflege`. Es können die Einträge im Feld IDIntern geleert werden, wenn der Stammschüler, auf den verwiesen wird nicht mehr existiert. Diese Situation kann in MAGELLAN 7 nicht mehr entstehen, kann aber aus MAGELLAN 6 mit übernommen worden sein. Bitte beachten Sie den Abschnitt [Verwaiste Stammschüler-Verweise entfernen](https://doc.magellan7.stueber.de/admin/datenbankpflege.html#verwaiste-stammsch%C3%BCler-verweise-entfernen)!

### MAGELLAN Bibliothek

* Fix: Datenbankanmeldung beim Druck von Quittungen korrigiert
* CHANGE: die Abfragen beim Aufruf der Menüpunkte `Schüler` und `Vorgänge` wurden optimiert, damit die Daten in den Menüpunkten schneller aufrufbar sind

### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur von MAGELLAN 7 angepasst:

* FIX: Quittung\(DIN A4\).rpt
* FIX: Quittung\(DIN A4\).rpt
* FIX: Zeugnisse\Nordrhein-Westfalen


## 7.0.5 - 703 (11.04.2019)

### MAGELLAN

* FIX: SAXSVS: Problem für `al_abschl_dat` und `al_laufb_kl` behoben
* CHANGE: SAXSVS: Neue Meldungen und in allen Meldungen werden mehr Detailinformationen gezeigt
* CHANGE: SAXSVS: Neue Prüfungen, wenn ein Wert ohne Schlüssel vergeben wurde (Beispiel: Staatsangehörigkeit mit Kürzel D zugeordnet, aber kein Schlüssel im Verzeichnis hinterlegt)
* CHANGE: SAXSVS: XML-Fehlermeldungen werden erst ausgegeben, wenn keine MAGELLAN-Meldungen mehr ausgegeben werden.

Beispiel für eine MAGELLAN-Meldungen:

Art	|Message
--|--
Fehler|	Ina Müller (549): Das Feld "<abs><av_abs_schart>" darf nicht leer sein.
Fehler|	Otto Meyer (549): Das Feld "<bbs><av_bbs_schart>" darf nicht leer sein.
Fehler|	Sebastian Schmidt (2043): Das Feld "<abs><av_abs_schart>" darf nicht leer sein.

Beispiel für eine XML-Meldung:

```
In Zeile "1" an Position "xxx"
Begründung: 
  Fehler beim Analysieren von '' als date-Datentyp.
Analyse des Elements 'al_abschl_dat' mit dem Wert '' fehlgeschlagen.
 
XML-Auszug: ....
```
* FIX: Problem beim Ändern von Staatsangehörigkeiten behoben, bitte synchronisieren Sie die Zugriffsrechte im Modul `MAGELLAN Administrator > Benutzerverwaltung`.
* FIX: Der Aufruf für `Status ändern` wurde in den Menüpunkten `Personen`, `Sorgeberechtigte`, `Betriebe`, `Schulen` unter `Auswahlliste > Datensatz auswählen > Rechtsklick` ergänzt.


### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* NEW:`Berichte\Klassen` Klassenliste mit Schülersummendaten Ausländer.rpt
* NEW:`Berichte > Klassen` Klassenliste mit Schülersummendaten Ausländer.rpt
* NEW: `Berichte > Zeugnisse > Berlin` BER-Schul Z 302 (10.18).rpt

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur von MAGELLAN 7 angepasst:

* CHANGE: `Berichte > Schüler > RLP/NIE/BAW/BER`
* CHANGE: `Berichte > Mandanten > Allgemein`
* CHANGE: `Berichte > Zeugnisse > Auslandsschulen`
* CHANGE: `Berichte > Zeugnisse > Baden-Württemberg`
* CHANGE: `Berichte > Zeugnisse > Demo`
* CHANGE: `Berichte > Zeugnisse > Mecklenburg-Vorpommern`
* CHANGE: `Berichte > Zeugnisse > Hessen`
* CHANGE: `Berichte > Zeugnisse > Niedersachsen`


## 7.0.4 - 703 (01.04.2019)

### MAGELLAN

* FIX: Datenstrukturanpassungsassistent: Eine Sicherung muss vor der Anpassung erstellt werden
* FIX: Datenstrukturanpassungsassistent: Sicherungspfad wird aus den eigenen Einstellungen im Willkommensassistenten oder aus dem MAGELLAN Administrator vorbelegt. Sollte die Sicherung nicht lokal erfolgen, muss der Pfad vorab existieren.
* FIX: Datenstrukturanpassungsassistent: Schaltfläche zum Erstellen der Sicherung eingeblendet.

![Sicherung erstellen](../assets/images/changelog/7.0.4.00.png)

* FIX: Datenstrukturanpassungsassistent: Assistent kann nur als sysdba gestartet werden
* FIX: Problem beim Eintragen von Schülerfehlzeiten korrigiert
* FIX: Anzeige der Statistikmerkmale für Schüler und Bewerber in der Unterkarte `Statistik` behoben.
* FIX: In den Zugriffsrechten der Benutzern wurden die Rechte für die Tabellen `Medienausleiher` (Änderungen bei Lehrerdatensätzen) und `SchuelerAbwesenheiten` korrigiert. Bitte führen Sie im MAGELLAN Administrator einmal den Punkt `Benutzerverwaltung > Zugriffsrechte synchronisieren` aus, das Skriptdatum im Ergebnisfenster müsste den 26.03.2019 zeigen.

![`MAGELLAN Administrator > Benutzerverwaltung > Zugriffsrechte synchronisieren`](../assets/images/changelog/7.0.4.04.png)

* FIX: Mehrfachdarstellung von Schülern beim Fachtafel-zuweisen behoben.
* FIX: Ein neuer Eintrag unter `Bewerber > Ausbildung` wird automatisch als aktueller Ausbildungsdatensatz übernommen. Das gilt nur für den ersten Eintrag, ab dem zweiten Eintrag ändern Sie ggfs. den Eintrag über das Feld `aktuelle Ausbildung` am unteren Menürand.
* FIX: `Mandanten > Daten2 > Schulformen`, hier können auch Werte mit mehr als 8-Zeichen Kürzellänge verwendet werden.
* FIX: Korrektur für den Seriendruck an den Betrieb des Schülers
* CHANGE: Der Eintrag der aktuellen Ausbildung (`Schüler > Ausbildung > Ausbildung`) wird bei Schülerkopien pro Kopie gespeichert. 
* CHANGE: Beim Einschulen wird der `Zugang am` für Schüler oder Schülerkopien wie folgt übernommen:

Feld|Schüler (ohne IDIntern)|Schülerkopie (mit IDIntern)
--|--|--
aktualisiert das Feld `Daten2 > ZugangAm`|Ja|Nein
aktualisiert das Feld `Laufbahn > Zugang`|Ja|Ja
aktualisiert das Feld `Laufbahn > Schulformeintritt`|Ja|Ja

![Zugang am](../assets/images/changelog/7.0.4.02.png)

* NEW: Neue Sammelzuweisungsmöglichkeit zum Aktivieren oder Deaktivieren des Feldes `Schüler > Ausbildung > Ausbildung editieren > Neuanfänger im Bildungsgang`

![Neuanfänger im Bildungsgang](../assets/images/changelog/7.0.4.03.png)

* FIX: Verzeichnisfelder unter ´Schüler > Daten 2` aktualisiert
* CHANGE: Von- und Bis-Datum der Ausbildung auf `Schüler > Daten1` eingeblendet
* CHANGE: Gruppierung im Verzeichnis `Bildungsgänge` entfernt
* FIX: Beim Anlegen eines neuen Schülers wechselt der Auswahllistefilter automatisch auf von `Eingeschult` auf `Vagabunden`.
* FIX: Beim Zuweisen einer neuen Schulform unter `Mandanten > Daten2 > Schulformen` werden Werte mit bis zu 20 Zeichen im Kürzel akzeptiert
* FIX: Editierbarkeit unter `Schüler > Zeugnis > Details > Tutor und Prüfungsvorsitz` korrigiert

### MAGELLAN Bibliothek

* FIX: `Datenbank > Optionen > Quittungen`: es gibt keinen vorbelegten Bericht mehr
* FIX: `Datenbank > Optionen > Quittungen`: `Quittungen/Bestätigungen automatisch drucken` wird korrekt gespeichert
* FIX: Vor dem Anlegen eines Mediums wird geprüft, ob mindestens ein Katalog angelegt und ausgewählt ist


### MAGELLAN Administrator

* NEW: Neue Funktionalität, um Bewerbern, wenn sie nur eine Ausbildung haben, diese als aktuelle Ausbildung zuzuweisen. Hintergrund: die Zuweisung als aktuelle Ausbildung ist die Voraussetzung für den Seriendruck an diesen Betrieb.

![Bewerberausbildung als aktuelle Ausbildung hinterlegen](../assets/images/changelog/7.0.4.01.png)

### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

Folgende Berichtsverzeichnisse wurden auf die Datenstruktur in MAGELLAN 7 angepasst:

* CHANGE: `Berichte > Klassen > allgemeine Berichte`
* CHANGE: `Berichte > Klassen > Baden-Württemberg`
* CHANGE: `Berichte > Klassen > Berlin`
* CHANGE: `Berichte > Klassen > Mecklenburg-Vorpommern`
* CHANGE: `Berichte > Klassen > Nordrhein-Westfalen`
* CHANGE: `Berichte > Klassen > Rheinland-Pfalz`
* CHANGE: `Berichte > Schüler > allgemeine Berichte`
* CHANGE: `Berichte > Schüler > Auslandsschulen`
* CHANGE: `Berichte > Schüler > Baden-Württemberg`
* CHANGE: `Berichte > Schüler > Berlin`
* CHANGE: `Berichte > Schüler > Mecklenburg-Vorpommern`
* CHANGE: `Berichte > Schüler > Niedersachsen`
* CHANGE: `Berichte > Schüler > Nordrhein-Westfalen`
* CHANGE: `Berichte > Schüler > Rheinland-Pfalz`
* CHANGE: `Berichte > Schüler > Schleswig-Holstein` 
* CHANGE: `Berichte > Bewerber > allgemeine Berichte`
* CHANGE: `Berichte > Bewerber > Baden-Württemberg`
* CHANGE: `Berichte > Betriebe > allgemeine Berichte`
* CHANGE: `Berichte > Adressen > allgemeine Berichte`
* CHANGE: `Berichte > Buchungen > allgemeine Berichte`
* CHANGE: `Berichte > Kurslisten > allgemeine Berichte`
* CHANGE: `Berichte > Haushaltsstellen > allgemeine Berichte`
* CHANGE: `Berichte > Inventar > allgemeine Berichte`
* CHANGE: `Berichte > Lehrer > allgemeine Berichte`
* CHANGE: `Berichte > Lehrer > Rheinland-Pfalz`
* CHANGE: `Berichte > Lieferanten > allgemeine Berichte`
* CHANGE: `Berichte > Verlage > allgemeine Berichte`
* CHANGE: `Berichte > Sorgeberechtigte > allgemeine Berichte`
* CHANGE: `Berichte > Schulen > allgemeine Berichte`
* CHANGE: `Berichte > Quittungen > allgemeine Berichte`
* CHANGE: `Berichte > Prüfungslisten > Baden-Württemberg`
* CHANGE: `Berichte > Prüfungslisten > allgemeine Berichte`
* CHANGE: `Berichte > Personen > allgemeine Berichte`
* CHANGE: `Berichte > Medienvorgaenge > allgemeine Berichte`
* CHANGE: `Berichte > Medien > allgemeine Berichte`
* CHANGE: `Berichte > Mandanten > allgemeine Berichte`
* CHANGE: `Berichte > Mandanten > Rheinland-Pfalz`
* CHANGE: `Berichte > Mahnungen > allgemeine Berichte`
* CHANGE: `Berichte > Zeugnisse > allgemeine Berichte`

## 7.0.3 - 703 (15.03.2019)

### MAGELLAN

* NEW: `Schüler/Bewerber > Daten 2 > Aufenthalt > Aufenthaltserlaubnis` - MAGELLAN um Aufenthaltserlaubnis Von- und Bis- Datum erweitert. Im Zuge dessen die Aufteilung der Eingaben auf der Maske angepasst. 
* CHANGE: Unterkarte `Bewerber` ist nur noch in der Sammelzuweisung aus dem Menü `Bewerber` sichtbar
* FIX: Alle Neu-Dialoge der Hauptansichten: Abfrage nach Gast1- und Gast2-Rechten, mit entsprechender Meldung
* FIX: Datenstrukturversion auf 703 angepasst und Skript korrigiert
* FIX: Bewerber/Schueler: Nach Anlegen neuer Herkunftsschule und gesetztem Haken wird jetzt auch die gesetzte Herkunftsschule in der Combobox dargestellt (Aktualisierungsfehler)
* FIX: Sammelzuweisung Bewerber/Schüler : Aus- und Einblenden der Bewerberdaten > Karte im Dialogfenster korrigiert
* FIX: Serienbrief b. Schüler - Ändern der Empfänger (Betrieb/Sorgeberechtigte) hat sich nicht ausgewirkt
* FIX: Beim Wechsel aus der Auswahlliste `Schüler` nach einer Filterung werden auf `Daten 1` die Ausbildungsdaten und Familiendaten des korrekten Schülers gezeigt.
* FIX: Seriendruck aus dem Menü `Bewerber`.
* FIX: Beim Seriendruck aus dem Menü `Schüler` werden die Datenmengen (nur Schüler- und Klassendaten, zusätzlich Sorgeberechtigtendaten oder zusätzlich Betriebedaten) korrekt an Word übergeben.
* FIX: Die Ausgabe der Datenmenge `An den aktuellen Betrieb der markierten Schüler` für den Seriendruck wurde korrigiert
* CHANGE: Unter `Bewerber > Ausbildung` wurde die Eingabe des aktuellen Betriebes ergänzt
* FIX: Aufruf `Drucken > Zeugnisse` wurde im Menü `Berufsschule` eingeblendet


### MAGELLAN Bibliothek

* FIX: Berichte werden in der Vorschau gefüllt
* FIX: Meldung beim Aufruf der Ausleihe behoben (Cannot focus a disabled or invisible window)
* FIX: Ausleihe und Rückgabe angepasst
* FIX: Zuordnung des Berichteverzeichnisses zum Menü `Mahnwesen`


### MAGELLAN Administrator

* NEW: Verbindungen können per Kopieren dupliziert werden (Rechtsklick auf die Verbindung > Verbindung kopieren) 
* NEW: Ansicht `Benutzerverwaltung` > Neue Registerkarte `Administratoren`:  
  * Fehlende Administratoren können nachträglich angelegt werden
  * bei bestehenden Administratoren kann das Passwort geändert werden
  * Aufruf der Funktionalitäten per Doppelklick auf den Administratorendatensatz oder über den Punkt `Extras`
  
![nachträgliches Anlegen eines sysdba-Nutzers](../assets/images/changelog/sysdba.anlegen.png)  

* FIX: `Datenbankpflege > Mandanten kopieren > 6 nach 7`: (Gilt für Umstiege mit MAGELLAN bis zur 7.0.2, für spätere Versionen nicht mehr nötig.) Die IDIntern bei Schülern zu denen das Original nicht mehr existiert, wird entfernt.
* NEW: Unter `Datenbankpflege` finden Sie den neuen Punkt `Korrektur Mandanten kopieren`. Die Korrektur überträgt Ausbildungsdaten eines Nebenschülers in die Liste des Stammschülers. Die gesamte Liste wird für Stamm- und Nebenschüler gezeigt.

 ![Neue Korrekturmöglichkeit im MAGELLAN ADMINISTRATOR](../assets/images/changelog/mandanten.korr.png) 


### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: DAS-GY-ABI (Anlage 7).rpt (Bericht war versehentlich nur für die Darstellung am Bildschirm eingestellt)
* CHANGE: Klassen\Klassenliste (Betriebe mit Auszubildenden nach Gemeinden).rpt
* CHANGE: Klassen\Anwesenheitsliste für den Tag.rpt
* CHANGE: Klassen\Anwesenheitsliste für ganzen Monat.rpt
* CHANGE: Klassen\Jahresnotenliste-BVJ.rpt
* CHANGE: Klassen\Klassen (Fax an Betriebe der Schueler).rpt
* CHANGE: Klassen\Klassenlehrerliste mit Räumen (Variante 2).rpt
* CHANGE: Klassen\Klassenlehrerliste mit Räumen.rpt
* CHANGE: Klassen\Klassenlehrerliste.rpt
* CHANGE: Klassen\Klassenliste (Adressen Schüler und Eltern).rpt
* CHANGE: Klassen\Klassenliste (ausländische Schüler).rpt


## 7.0.2 - 702 (19.02.2019 - 13.30 Uhr) - Achtung erneute Veröffentlichung!!

> #### warning::Wichtig!
>
> Aufgrund von Problemen beim Erstellungsprozess mussten wir die Version erneut veröffentlichen.
> Sollten Sie die Version 7.0.2 bereits installiert haben. Wiederholen Sie bitte den Download und Installation.

## 7.0.2 - 702 (19.02.2019 - 10.00 Uhr)

> #### warning::Wichtig!
>
> Die Datenstruktur von MAGELLAN ist erweitert worden!   
> Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Eine genaue Anleitung zum Serviceupdate finden Sie [**hier**](http://doc.magellan7.stueber.de/installation/update.html). Sollten Probleme auftreten, schauen Sie bitte [**hier**](http://doc.magellan7.stueber.de/installation/troubleshootingupdate.html).


### MAGELLAN

* NEW: `Schüler > Daten 2 > Höchster Abschluss ABS > Schule`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss ABS > Schule`

* NEW: `Schüler > Daten 2 > Höchster Abschluss ABS > Schulform`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss ABS > Schulform`

* NEW: `Schüler > Daten 2 > Höchster Abschluss BBS > Schule`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Schule`

* NEW: `Schüler > Daten 2 > Höchster Abschluss BBS > Schulform`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Schulform`

* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Beruf`
* NEW: `Bewerber > Daten 2 > Höchster Abschluss BBS > Erreicht am`

* CHANGE: `Schüler > Zugang/Abgang` komplett nach `Schüler > Daten 2` verschoben, Registerkarte entfernt
* CHANGE: `Bewerber > Zugang/Abgang` komplett nach `Bewerber > Daten 2` verschoben, Registerkarte entfernt

* NEW: SAXSVS - "Vollständige" Abbildung der Schnittstelle
* NEW: SAXSVS - Schüler zum Löschen (in SAXSVS) vormerken oder 
                Schüler vom Export in die XML-Datei ausschließen                
* CHANGE: SAXSVS - Schlüsselverzeichnisse für die Schnittstelle aktualisiert. Bitte neu einlesen! 


### MAGELLAN Administrator

* FIX: 


### MAGELLAN Bibliothek

* FIX: 


### MAGELLAN Skripteditor

* FIX: 


### Skripte


### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* CHANGE: SAC: Die mitgelieferten Zeugnisse für Sachsen wurden den neuen Gegebenheiten in MAGELLAN 7 angepasst. Zur Anpassung Ihrer eigenen Berichte lesen Sie bitte den Abschnitt <a href="https://doc.magellan7-kb.stueber.de/cr/berichte_fuer_7_anpassen.html" target="_blank">Berichte für MAGELLAN 7 anpassen</a> in unserer Knowledge Base.

---

## 7.0.1 - 701 (04.01.2019)

> #### warning::Wichtig!
>
> Die Datenstruktur von MAGELLAN ist erweitert worden!   
> Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Eine genaue Anleitung zum Serviceupdate finden Sie [**hier**](http://doc.magellan7.stueber.de/installation/update.html). Sollten Probleme auftreten, schauen Sie bitte [**hier**](http://doc.magellan7.stueber.de/installation/troubleshootingupdate.html).

### MAGELLAN

* NEW: Status "Abwesend" mit Speicherung von längerfristigen Abwesenheiten 
       (z.B. Elternzeit, Auslandsjahr, etc.). Gespeichert werden die Daten in 
       der Tabelle "SchuelerFehlzeiten", die über das neue Feld "Art" zwischen 
       Abwesenheit und der bisherigen Fehlzeit unterschieden werden kann. 
       Dargestellt und bearbeitet können die Abwesenheiten unter 
       Schueler > Laufbahn. Weitere Infos können der Dokumentation entommen 
       werden.
* NEW: Anzeige des Schülerstatus auf den Registerkarten. Aktuell nur Daten 1. 
       Wird in den kommenden Serviceupdates auf alle Registerkarten erweitert.      
* FIX: SAXSVS: Auf das neues Schema 2.3 umgestellt. Aktuell wird noch die 
       Minimalanforderung unterstützt. Wir arbeiten an der vollständigen Umsetzung,
       siehe, z.B. die neue Funktion "Abwesenheit", die einen Teil der Umsetzung 
       darstellt, mehr Daten für die Schnittstelle in MAGELLAN erheben zu können.
       

### MAGELLAN Administrator

* FIX: 


### MAGELLAN Bibliothek

* FIX: 


### MAGELLAN Skripteditor

* FIX: 


### Skripte


### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

---

## 7.0.0 - 700 (21.12.2018)

### MAGELLAN

* FIX: Fehlermeldung bei der Installation, wenn kein Crystal Reports installiert ist \#1024921
* FIX: Fehler bei der Sammelzuweisung \#1024899
* FIX: Field Merkmal S1 not found Export SAXSVS \#1024971
* NEW: Die aktuelle Ausbildung des Schülers wird jetzt pro Schulhalbjahr gespeichert
* NEW: \#1019480 - Deutsche Auslandsschule als Region im Willkommensassistent wählbar
* CHANGE: Die bisherige beim Schüler gespeicherte Ausbildung wird nur noch beim Bewerber genutzt und wird bei der Einschulung eines Schülers berücksichtigt.
* CHANGE: Hinzufügen von Datensätzen in den Schlüsselverzeichnissen wieder mit Pfeiltaste unten auf dem letzten Datensatz möglich


### MAGELLAN Administrator

* FIX: Aktualisierte Schlüsselverzeichnisse für Sachsen
* CHANGE: \#1019441 - Neuer Unterordner `\Benutzer` im Importverzeichnis. Benutzer können dort angepasste Importdateien hineinlegen, die von der Installation nicht überschrieben werden.
* NEW: \#1019480 - Deutsche Auslandsschule als Region wählbar
* NEW: Nachträgliches Anmelden an die Datenbank über Menü `Datenbank > Anmelden...` möglich.


### MAGELLAN Bibliothek

* FIX: 


### MAGELLAN Skripteditor

* FIX: 


### Skripte


### Berichte \(NEW oder CHANGE\)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.