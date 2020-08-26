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

## 7.1.16 - 715

### Datenstruktur

* NEW:

### MAGELLAN SCHULVERWALTUNG

* FIX: 

### MAGELLAN Schnittstellen

#### NRW

* CHANGE: ABS => für die ABI.txt wurden bislang Schüler ausgegeben, die einen Eintrag unter `Daten2|G8/G9` hatten, MAGELLAN liest jetzt nur noch Schüler aus, die diesen Eintrag haben und im Klassenjahrgang 12 (mit Eintrag G8) oder 13 (mit Eintrag G9) sind. Der Klassenjahrgang wird unter `Klasse > Zeiträume > Jahrgang` erwartet.  
* FIX: ABS + BBS: Ausgabe aus dem Feld `Versetzung` angepasst. Auszug aus der Dokumentation unter [https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/](https://doc.ls.stueber.de/nordrhein-westfalen/schuelerdaten/)

![Feld Versetzung](/assets/images/changelog/7.1.16.01.png)

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

* FIX: SAR-APO-DFG-2014.dws: PreCheckPruefungsbereichFehler

### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

#### Allgemein

* CHANGE: `Klassenliste mit Schülersummendaten.rpt` Jahrgang der Klasse wird mit ausgegeben
