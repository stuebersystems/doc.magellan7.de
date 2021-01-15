# Was ist neu

Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN 7. Änderungen im Modul MyMAGELLAN CENTER werden hier veröffentlicht, Änderungen im Modul MyMAGELLAN veröffentlichen wir im MyMAGELLAN Handbuch unter [https://doc.mymagellan7.stueber.de/changelog/](https://doc.mymagellan7.stueber.de/changelog/).
Dieses Kapitel gibt ihnen einen Überblick über aktuelle Änderungen in MAGELLAN 6.

* Den Änderungsverlauf aus den vergangenen Jahren finden Sie hier: 

  * [2020](changelog2020.md)
  * [2019](changelog2019.md)

* Was wir für die nächste Ausgabe planen, sehen Sie im Kapitel ["Voraussichtliche Änderungen"](changelog-next.md).

## LEGENDE

Abkürzung | Bedeutung
----------|----------
FIX       | Korrektur bestehender Funktionalität
NEW       | Neue Funktionalität
CHANGE    | Änderung des Ablaufs, Verarbeitung oder Bedienung

!!! danger "Achtung"

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## 7.1.22 - 718 (08.01.2021)

!!! warning "Wichtig"

    Die Datenstruktur von MAGELLAN ist erweitert worden! Bitte aktualisieren Sie als erstes Ihren Serverrechner, anschließend alle Arbeitsplatzrechner! Beim ersten Start von MAGELLAN erfolgt eine automatische Anpassung an die neue Datenstruktur durch einen Assistenten. Bitte befolgen Sie die [Anleitung](https://doc.magellan7.stueber.de/schulverwaltung/update/vorbereitung/#updates-mit-datenstrukturerweiterung)!

### Datenstruktur

* CHANGE: Trigger "Schueler_BD" (Hinzufügen fehlender Tabellen "BewerberVerfahren", "BewerberFachdaten" und
  "BewerberUnterlagen")

### MAGELLAN SCHULVERWALTUNG

* FIX: `Schüler > Zeugnis > Details > Sammelzuweisung > Tutor` =>  die Zuweisung des Tutors für mehrere Schüler ist wieder gegeben.
* FIX: Für den Seriendruck an Nebenschüler werden die Sorgeberechtigtendaten korrekt ausgegeben
* FIX: erneutes Versetzen von Schülern in einen anderen Mandanten korrigiert
* FIX: Versetzen von Schülern in einen anderen Mandanten mit Daten aus den Tabellen "BewerberVerfahren", "BewerberFachdaten" und  "BewerberUnterlagen korrigiert
* FIX: Beim Versetzen von Schülern in einen anderen Mandanten wurde versucht für die Schülerkopie die gleiche ID (mit neuen MandantenID) zu verwenden.
* FIX: Beim Versetzen von Schülern als Vagabund oder Bewerber in einen anderen Mandanten werden die zugewiesenen Sorgeberechtigten im neuen Mandanten stets aktiviert.

### MAGELLAN ADMINISTRATOR

* CHANGE: Lesen der Magellan.paths beim Programmstart korrigiert

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: BER-IBA-HJ-2020.dws - Korrekturen
* FIX: BER-IBA-AS-2020.dws - Berechnung des Abschluss für das 1. HJ, Korrekturen

* NEW: SAR-APO-2018.dws - Basierend auf der Verordnung zur Änderung der Verordnung – Schul-und Prüfungsordnung über die gymnasiale Oberstufe und die Abiturprüfung im Saarland vom 17. April 2018

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: DAS-GY-ABI (DIA)(2020).rpt => Ausgabe der Kurssprachen ( nicht bilingual)
* FIX: Zeugnisliste BBS.rpt (überflüssige Tabellen entfernt, Verknüpfungen optimiert)
* FIX: BER-KO-AS (Schul Z 320a-b)(03.11).rpt (Bemerkungen werden ausgegeben)
* FIX: BER-KO-AS (Schul Z 322)(03.11).rpt (Unterberichtsverknüpfung Geografie korrigiert)
