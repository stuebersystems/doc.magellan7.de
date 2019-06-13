# View Klassenansicht

Grundlage der Daten sind 
* [Klassen](https://doc.magellan7.stueber.de/datenstruktur/tabellen/Klassen/) 
* [KlassenZeitraeume](https://doc.magellan7.stueber.de/datenstruktur/tabellen/KlassenZeitraeume/).


| Feldname               | Typ | Größe | Funktion | Bemerkung                                |
|------------------------|-----|-------|----------|------------------------------------------|
| Mandant                | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                     | I+  | -     | P        | Verweis auf Tabelle **Klassen**          |
| GUID                   | A   | 32    | V        | Verweis auf Tabelle **Klassen**          |
| IDIntern               | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| IDExtern               | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| GUIDExtern             | A   | 36    | V        | Verweis auf Tabelle **Klassen**          |
| Kuerzel                | V   | 15    | V        | Verweis auf Tabelle **Klassen**          |
| KuerzelStatistik       | A   | 20    | V        | Verweis auf Tabelle **Klassen**          |
| Langname1              | A   | 100   | V        | Verweis auf Tabelle **Klassen**          |
| Langname2              | A   | 100   | V        | Verweis auf Tabelle **Klassen**          |
| Klassenart             | S   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Notenart               | S   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Abteilung              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Schulform              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Schulart               | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Schulstelle            | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Organisation           | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Behinderung            | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Beruf                  | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Bildungsgang           | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Berufsfeld             | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| Einzelintegration      | L   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Laenderuebergreifend   | L   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Schulartuebergreifend  | L   | -     | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalA1              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalA2              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalA3              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalA4              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalA5              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalA6              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalS1              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalS2              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalS3              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalS4              | A   | 10    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalB1              | A   | 15    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalB2              | A   | 15    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalB3              | A   | 15    | V        | Verweis auf Tabelle **Klassen**          |
| MerkmalB4              | A   | 15    | V        | Verweis auf Tabelle **Klassen**          |
| Maske                  | S   | -     | V        | Verweis auf Tabelle **Klassen**          |
| NaechsteKlasse         | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| NaechsteKlasseZeitraum | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| KlassenZeitraumID      | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Zeitraum               | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Jahrgang               | S   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenleiter1         | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenleiter2         | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenraum            | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenstufe           | A   | 10    | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Fachtafel              | A   | 10    | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Unterrichtsform        | A   | 10    | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Unterrichtstage        | S   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassensprecher1       | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassensprecher2       | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenwahlvertreter1  | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenwahlvertreter2  | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenelternsprecher1 | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Klassenelternsprecher2 | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |



