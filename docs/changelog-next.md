# Voraussichtliche Änderungen

Sie erhalten hier einen Überblick über die voraussichtlichen Änderungen und Korrekturen für das nächste Serviceupdate. Die nachfolgend gelisteten Änderungen wurden noch nicht veröffentlicht.

## LEGENDE

| Abkürzung | Bedeutung |
| --- | --- |
| FIX | Korrektur bestehender Funktionalität |
| NEW | Neue Funktionalität |
| CHANGE | Änderung des Ablaufs, Verarbeitung oder Bedienung |

---

## 7.0.17 - 707

### MAGELLAN

* FIX: Korrektur bei Durchlauf der SAXSVS Statistik
* FIX: Unter `Klassen > Zeiträume` wird die Anzeige der einzublendenen Zusatzklasse beim Weiterschalten aktualisiert
* FIX: Korrektur der Auswahl eines weiteren Mandanten
* FIX: Angezeigte Anzahl der Schüler (gesamt, aktiv, inaktiv) in der Schülerauswahlliste überarbeitet
* FIX: Bezeichnung des Tabs `Datenbank` wird wieder korrekt dargestellt
* FIX: Ablage von PDF-Dokumenten in Schülerunterverzeichnissen parallel zum Druck (oder auch ohne Druck) für Schüler mit Nebenlaufbahn angepasst
* FIX: Die erste dem Schüler unter `Daten2` zugewiesene `Bereits besuchte Schule` wird standardmäßig als `Herkunftsschule` übernommen
* FIX: `Schüler > Daten1` Kontextmenü Passfoto ergänzt um Passfoto aus Digitalquelle
* FIX: für Schüler mit Status N können Zeugnisse, Berichte etc. als PDF Dateien im Dokumente Ordner gespeichert werden

### MAGELLAN Bibliothek

* FIX:

### Skripte  

* FIX: `Exportiere SDTF.dws` und `Importiere SDTF.dws` an neue `MagSDTFSync.exe` angepasst
* FIX: Am Skript `Schüler einschulen.dws` wurde das Einschulen von Schülern korrigiert, die bereits in älteren Halbjahren Schüler der Schule waren

### MAGELLAN Administrator

* FIX: Übernahme MAGELLAN 6 nach MAGELLAN 7: `SchuelerUnfallberichte` und `Beschäftigungsarten`
* FIX: SHL > 00_Klassenstufen.keys

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAR-GEMS-AZ (Klasse 5-10)
* FIX: Lehrerliste mit Geburtstagen.rpt
* FIX: Lehrerliste mit Geburtstagen (ohne Geburtsjahr).rpt
* FIX: Lehrerliste (Email und Funktion 1-8).rpt
* FIX: Schülerpersonalblatt incl. Schuleintritt und -austritt (mit Vorbildung).rpt
* FIX: NRW-BK-JZ (Anlage C14 - 2 Seitig).rpt

