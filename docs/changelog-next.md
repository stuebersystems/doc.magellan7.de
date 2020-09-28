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

## 7.1.18 - 715

### Datenstruktur

* NEW: 

### MAGELLAN SCHULVERWALTUNG

* FIX: Korrekturen beim Versetzen von Schülern in Nachbarmandanten (Herkunfstschule wird übertragen, Prüfung ob Sorgeberechtigte bereits vorhanden sind)
* NEW: Schüler, die in Nachbarmandanten versetzt werden, können optional statt als Vagabunden (Standard) als Bewerber übertragen werden. 

![Schüler als Bewerber in Nachbarmandanten versetzen](/assets/images/changelog/7.1.18.01.png)

### MAGELLAN Schnittstellen

#### SAXSVS

* FIX: erweiterte Fehlerausgabe beim Export, ID und Klasse des betroffenen Schülers werden ausgegeben
* CHANGE: Neue Meldung, wenn das Land des Ausbildungsbetriebs nicht gefüllt ist

Art|Feld|Meldung
--|--|--
Fehler|<aau_ausbetr><staat> (Ausland)|Vorname Nachname (SChülerID): Das Feld "<aau_ausbetr><staat> (Ausland)" darf nicht leer sein.

* NEW: <as_staat> (Land des Sorgeberechtigten): Hier werden bisland die Einträge D, De, Deu, CZ, PL, CH in die richtigen Schlüsselwerte umgesetzt. Ergänzt wurde für Österreich der Wert AT.
* NEW: Neue Prüfung für Sorgeberechtigte (aus Deutschland, also Land D, De oder Deu) ohne Gemeindekennziffer.
* NEW: Neue Betriebeprüfung: Gemeldet werden Betriebe ohne Eintrag im Feld `Land` und `Gemeinde`
* NEW: Hat ein Betrieb nur einen Eintrag im Feld `Gemeinde` und das Feld `Land` leer, wird für SaxSVS das Land automatisch als `De` ausgespielt.


## SHL

* FIX: Ausgabe der Exportdateien

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

* FIX: Schüler > Drucken > Berichte > Schülerliste (Fehlzeiten nach Schüler gruppiert).rpt
* FIX: Abitur > Drucken > Prüfungslisten drucken > Prüfungsliste (Abitur).rpt

#### Berlin

CHANGE: BER-KO-ABI (Schul Z 323)(03.11).rpt (Ausdruck aus MAGELLAN 7 jetzt möglich)
CHANGE: BER-KO-AZ (Schul Z 321)(03.11).rpt (Ausdruck aus MAGELLAN 7 jetzt möglich)
CHANGE: BER-KO-AS (Schul Z 320a-b)(03.11).rpt (Ausdruck aus MAGELLAN 7 jetzt möglich)
NEW: BER-Schul Z 324 (11.19).rpt (Bericht war bereits in MAGELLAN 6 Auslieferung enthalten, nun auch für MAGELLAN 7 verfügbar)