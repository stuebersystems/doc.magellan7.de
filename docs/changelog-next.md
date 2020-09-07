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

    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

## 7.1.17 - 715

### Datenstruktur

* NEW:

### MAGELLAN SCHULVERWALTUNG

* FIX: `Schüler > Laufbahnprozess` "Schüler in  Mandanten versetzen" 

### MAGELLAN Schnittstellen

#### Statistik NRW

* FIX: SIM.TXT: Schüler einer Klasse ohne Statistikkürzel werden beim Export nicht berücksichtigt
* FIX: SIM.TXT: wenn in Schüler > Extras > Betreuungsarten > Innerschulisch 1 [Betreuungen innerschulisch (Schüler)] kein Eintrag vorhanden ist, ist das das Feld Betreuung leer
* FIX: SIM.TXT: Ausgabe von Foerderschwerp, VOfoerderschwerp, VOschwerstbeh, Foerderschwerp2, VOfoerderschwerp2 ohne Eintrag des BIS Datums. Der Eintrag eines BIS-Datum ist nicht zwingend erforderlich, das VON-Datum muss kleiner oder dem dem Anfangsdatum des jeweiligen Zeitraumes sein.
* CHANGE: ABI.TXT (ABS) um Schüler aus gemischten Jahrgängen G8 und G9 korrekt auszuspielen, ist eine Eintrag unter Klassen > Zeiträume > Klassenstufe (Schlüssel) Q2 notwendig
 

#### Schüler (Berlin) 

* FIX: Schüler (ABS und BBS) bewerber > schueler)_sorgebe.export.csv - bei mehreren eingetragenen Sorgeberechtigten werden auch mehrere Sorgeberechtigte ausgespielt

### MAGELLAN ADMINISTRATOR

* FIX:

### MyMAGELLAN-CENTER

* FIX: 

### MyMAGELLAN

### MAGELLAN Bibliothek

* FIX: 

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* CHANGE: 

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Allgemein

* CHANGE: 