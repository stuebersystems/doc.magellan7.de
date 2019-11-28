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

## 7.1.2 - 710

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE: Änderung der Datenstruktur für die OPAC-Funktion des Moduls MAGELLAN BIBLIOTHEK
* CHANGE: Erneute Zuweisung der SchuelerZeitraumID in der Tabelle SchuelerZeugnisbemerkungen

### MAGELLAN

* FIX: Unter `Schüler > Daten2 > Bereits besuchte Schulen` kann wieder direkt eine neue Schule angelegt werden
* FIX: Eine unter `Schüler > Daten2 > Bereits besuchte Schulen` neu angelegte Schule wird dem Schüler zugewiesen
* FIX: Ein unter `Schüler > Ausbildung` neu angelegter Betrieb wird der Schülerausbildung zugewiesen
* FIX: Beim Aufruf der F3-Suche von einer Schülerunterkarte wird beim Wechsel zum gesuchten Schüler auch der Inhalt der Registerkarte aktualisiert
* FIX: Beim Zusammenführen von Betrieben werden die Auszubildendenzahlen korrekt angezeigt
* FIX: Beim Weiterschalten von einem Schüler der Volljährig ist zu einem Minderjährigen wird das Symbol korrekt aktualisiert
* FIX: Bei der Übergabe von Schüler-Betriebedaten bspsw. für Adressetiketten per Seriendruck, wird nur der aktuelle Ausbildungsbetrieb je Schüler übergeben
* FIX: Eingabe von Noten unter `Schüler > Zeugnis > Leistungen` optimiert
* CHANGE: Testlizenzfenster überarbeitet
* FIX: Beim Wechsel zum Zielschüler (F3-Suche) in der Schülerauswahlliste wechselt auch die Markierung korrekt


### MAGELLAN Administrator

* FIX: Benutzer mit dem Zusatzrecht `Mandanten-Administrator` dürfen für Nutzer ihres Mandanten Benutzer in der `Benutzerverwaltung` verwalten und das MyMAGELLAN CENTER für diese Nutzer verwenden
* FIX: `Datenaustausch > Daten über das MAGELLAN Improtformat importieren` => Problem beim Importieren der schueler_laufbahn.import.csv gelöst

### MAGELLAN Bibliothek

* FIX:

### Skripte

* FIX: Das Skript `Zuweisen von Zugriffsrechten.dws` wurde geändert für das Recht `Mandanten-Administrator`
* CHANGE: Fremdskript `NRW-AS-APO-BK-1999.dws` mit auf 7er Datenstruktur angepasst, bitte beachten Sie die Hinweise unter [https://doc.la.stueber.de/08.nrw/nrw-as-apo-bk-1999/](https://doc.la.stueber.de/08.nrw/nrw-as-apo-bk-1999/)!

### Statistik

* FIX: [BER- SchüDa] Korrektur der Ausgabe des Felds `Geburtsland` und Ausgabe der Dateinamen

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* CHANGE: MVP-FG-FHReife (Bescheinigung 2013).rpt
* CHANGE: MVP-FG-ABI.rpt
* CHANGE: MVP-FG-AZ  (Qualifikationsphase DINA4).rpt
* CHANGE: MVP-FG-AZ (Qualifikationsphase).rpt
* CHANGE: MVP-FG-AZ.rpt
* CHANGE: MVP-FS-JZ.rpt
* CHANGE: MVP-GES-HJZ (nicht versetzt).rpt
* CHANGE: MVP-FO-Fhreife.rpt
* CHANGE: MVP-FO-JZ.rpt
* CHANGE: MVP-FS-AS .rpt
* CHANGE: MVP-FS-AZ.rpt
* CHANGE: MVP-Schullastenausgleich-Vollzeit (nicht im Landkreis Mecklenburgische Seenplatte).rpt
* CHANGE: MVP-Schullastenausgleich-Teilzeit (nicht im Landkreis Mecklenburgische Seenplatte).rpt
* CHANGE: MVP-FS-JZ.rpt
* CHANGE: MVP-GES-HJZ (nicht versetzt).rpt
* CHANGE: MVP-GES-HJZ (versetzt).rpt
* CHANGE: MVP-GES-JZ (nicht versetzt).rpt
* CHANGE: MVP-GES-JZ (versetzt).rpt
* CHANGE: DAS-GY-ABI (DIA)(2019).rpt (Ausgabe der Jahrgangsstufe/Year unter "V. Languages Sprachen" gemäß Vorlage angepasst)
* FIX: BER Abi-1a – Übersichtsplan über die Schullaufbahn ab 2010 – 12jähriger Bildungsgang (VO-GO) (01.12).rpt
* FIX: BER-BF-AS (einjährig).rpt
* FIX: BER-Abi 8 (01.12).rpt
* FIX: BER-Abi 8 (01.12) mit Logo2.rpt
* FIX: BER-Abi 8 (01.12) mit Logo.rpt
* FIX: BER-ABI (Schul II 929-3)(01.09).rpt
* FIX: BER-AbdGy-ABI (Schul Z 325)(02.11).rpt
* FIX: BER-AbdGy (abi_4b_berechnungsbogen_abendgym (03.12.).rpt
* FIX: SAC-BG-HJZ (E.01.03).rpt
* FIX: SAC-BG-JZ (E.01.02).rpt