# Voraussichtliche Änderungen

Sie erhalten hier einen Überblick über die voraussichtlichen Änderungen und Korrekturen für das nächste Serviceupdate. Die nachfolgend gelisteten Änderungen wurden noch nicht veröffentlicht.

## LEGENDE

| Abkürzung | Bedeutung |
| --- | --- |
| FIX | Korrektur bestehender Funktionalität |
| NEW | Neue Funktionalität |
| CHANGE | Änderung des Ablaufs, Verarbeitung oder Bedienung |

---

## 7.0.15 - 706

### MAGELLAN

* FIX: Durchblättern der Datensätze funktioniert auch mit PgUp und PageDown
* FIX: Befehl "Änderungen verwerfen" ist aktiv
* FIX: Skalierungsproblem beim Vergrößern und Verkleinern der Ansicht behoben
* FIX: Eingabe eines Leerzeichens unter `Schüler > Daten1 > Straße`
* FIX: Anzeige eines Berufes oder Bildungsgangs ohne Betrieb/Praxisbetriebs auf `Ausbildung` und `Daten1` beim Schüler
* FIX: Abfrage für angezeigte Datensätze unter `Schüler > Auswahl` angepasst
* FIX: Downloadpfad unter `Hilfe > auf Aktualisierung prüfen` angepasst
* FIX: Eingabe der PLZ und des Ortes bei Betrieben
* FIX: Setzen des aktuellen Ausbildungsbetriebes beim Einschulen von Vagabunden

### Skripte

* FIX: Anpassung von `Schueler wechseln`

### MAGELLAN BIBLIOTHEK

* FIX:

### MyMAGELLAN

### MyMAGELLAN CENTER

* NEW:

### MAGELLAN Administrator

* FIX: Restore (Wiederherstellen) einer Sicherungskopie korrigiert
* FIX: Übernahme der Daten von MAGELLAN 6 nach MAGELLAN 7 (Klassenzeitraeume.NaechsteKlasse und Klassenzeitraeume.NaechsteKlasseZeitraum)

### Berichte (NEW oder CHANGE)

Eine Anleitung unserer Berichte finden Sie im Modul MAGELLAN BERICHTE, das Bestandteil der Installation ist und unter `Start > Programme > Stüber Systems > MAGELLAN BERICHTE` aufgerufen werden kann.

* FIX: SAC-BVJ-AS mit HS (A.01.08).rpt (Ausgabe der Klassenmerkmale - Merkmal 1 und Merkmal 2)
* FIX: Schueler\Nordrhein-Westfalen\Schülerstammblatt.rpt
* FIX: Schueler\Nordrhein-Westfalen\NRW-Schülerstammblatt.rpt

Für folgende Berichte wurde die Verknüpfung zwischen SchuelerZeitraeume und SchuelerAusbildung geprüft und ggfs. korrigiert:

* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.05).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-HJI (A.01.02).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-Bescheinigung (F.01.01).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.04).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.04) 2spaltig.rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.03).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (A.02.02).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AZ (2 seitig).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (Vorbereitungsklasse) (A.01.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.05) 2spaltig.rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.02.04).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.01.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (2 seitig).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-HJZ (1 seitig).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-JZ1 (C.01.02).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-JZ2 (C.01.02).rpt
* FIX: Zeugnisse\Sachsen\Zertifikat (F.01.09).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-AZ (C.01.04)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-Fremdsprachenzertifikat (F.01.05).rpt
* FIX: Zeugnisse\Sachsen\SAC-Fremdsprachenzertifikat (F.01.05)(DIN A3)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-Fremdsprachenzertifikat (F.01.05)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-JZ (A.02.01).rpt
* FIX: Zeugnisse\Sachsen\SAC-FOS-FHReife (D.01.04).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-HJI (C.01.01).rpt
* FIX: Zeugnisse\Sachsen\SAC-FS-HJI (C.01.01)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-BVJ-JZ (A.01.08)(2 jähriges BVJ).rpt
* FIX: Zeugnisse\Sachsen\SAC-BVJ-AS mit HS (A.01.08).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.01.07)(Einstiegsqualifizierung).rpt
* FIX: Zeugnisse\Sachsen\SAC-BS-AS (A.01.07)(bis 2018).rpt
* FIX: Zeugnisse\Sachsen\SAC-BG-ABI (E.01.06).rpt
* FIX: Zeugnisse\Sachsen\SAC-BF-AS (A.02.07).rpt
