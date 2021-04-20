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

    **OPAC-Anbindung der MAGELLAN Bibliothek**: Durch Änderungen der Schnittstelle durch die Deutsche Nationalbibliothek können aktuell keine Daten ausgelesen werden, die Funktion steht damit aktuell nicht zur Verfügung.
    
    **Umlaute**: Falls Sie das Problem haben, dass beim Druck aus MAGELLAN Umlaute nicht korrekt dargestellt werden, kann die Ursache beim ODBC-Treiber Ihres Betriebssystems liegen. Bitte folgen Sie der [Anleitung](https://doc.kb.stueber.de/magellan/umlaute_druck.html)!

    **MyMAGELLAN**: Bitte beachten Sie, dass mit einer der letzten Versionen das Dateiformat der MyMagellan Dateien geändert wurde. Bitte passen Sie den Pfad im `MAGELLAN Administrator > MyMagellan Center` auf die Dateiendung `.mymx` an.

### 7.1.27 - 720

#### Datenstruktur

* CHANGE: 

#### MAGELLAN SCHULVERWALTUNG

* FIX: `Klassen > Zeiträume > ENBREA Leistungsprofile` beim Anlegen neuer Kurse bleibt der im Zeitraum eingetragene Klassenlehrer sichtbar
* FIX: Für Bewerber mit Nebenlaufbahn (Schülerkopien) kann mit Sekretariatsrechten per Bewerberverfahren den Bewerbungsstatus unter Daten1 angepasst werden.
  
#### Schnittstellen

##### SAXSVS

* CHANGE: 

##### MAGELLAN Bibliothek

* FIX: 

#### Skripte

Alle Anleitungen zu Berechnungsskripten finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW: NRW-APO-BK-2018 Dieses Skript prüft ab, dass nicht mehr als 32 Grundkurse eingebracht werden. Die Beschreibung des Skriptes finden Sie [hier](https://doc.la.stueber.de/08.nrw/nrw-apo-bk-2018/). Sie können es auch vor der Veröffentlichung [hier herunterladen](https://my.hidrive.com/lnk/3qSpCCDo) und auf Ihrem Serverrechner im Verzeichnis `Skripte > Nordrhein-Westfalen` ablegen.

#### Berichte

Alle Anleitungen zu Berichtsdateien finden Sie unter [https://doc.la.stueber.de](https://doc.la.stueber.de).

* NEW:

##### Berlin

* NEW: BER-Schul Z 593 (2019.2020).rpt
* NEW: BER-Schul Z 592 (03.2020).rpt
* NEW: BER-Schul Z 594 (12.19).rpt
* NEW: BER-Schul Z 591 (03.20).rpt
* NEW: DAS-Versetzungszeugnis-GY-MSA (ZKA)(Anlage 11)(§23)_Pandemie.rpt
