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

## 7.1.25 - 719

### Datenstruktur

* CHANGE:

### MAGELLAN SCHULVERWALTUNG

* FIX: Ladeverhalten des Feldes `Verkehrsmittel` im Menü `Bewerber`
* CHANGE: Seriendruck aus dem Menü `Schüler` an deren Sorgeberechtigte auch für inaktive Schüler möglich
* FIX: Tabreihenfolge (Feldwechsel per Tabulatortaste) auf der Karte `Schüler > Zeugnis > Details` korrigiert
* FIX: Unter `Bewerber > Daten1 > Bewerbung` wurden die Felder `2.Wunsch` und `3.Wunsch` wieder eingeblendet, dort kann auf eine Schule aus der Liste Schulen verwiesen werden.

### MYMAGELLAN

* CHANGE:

### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* FIX: SAR-APO-2018.dws = Notenbuffer erhöht
* FIX: Importiere SDTF.dws = Umgang mit nicht gesetzter Fachkursnummer beim Übertrag des Lehrerunterrichts.

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Berlin

* CHANGE: BER-GY-ZAS (Schul II 929-9)(12.08).rpt (Berechnung des Kurshalbjahres für G8 angepasst)

#### Saarland

* NEW:

#### Niedersachsen

* FIX: NIE-GY-ABI (2021).rpt 

#### Auslandsschulen

* FIX: DAS-Prüfungsbogen (Anlage 7 zu DIA-PO)(2018).rpt (Im gesellschaftswiss. Bereich können nun bis zu 4 Fächer angezeigt werden. Da sich üblicherweise die Bilinguale Sprache im Abitur nicht ändert, lesen wir einfach rückwärts von Q4 aus nach den Eintrag aus den zugewiesenen Kurssprachen aus und verwende diese dann im Bericht.)
* NEW: DAS-GY-ABI (DIA)(2021).rpt (Anpassungen gemäß Richtlinien für die Ausweisung der Sprachen auf den Abschlusszeugnissen der Deutschen Schulen im Ausland (Zeugnisse über die Allgemeine Hochschulreife, den Mittleren Schulabschluss und den Hauptschulabschluss)
Beschluss der Kultusministerkonferenz vom 25.09.2019 vorgenommen)
