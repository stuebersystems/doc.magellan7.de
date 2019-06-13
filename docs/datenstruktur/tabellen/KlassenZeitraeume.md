# Tabelle KlassenZeitraeume




| Feldname               | Typ | Größe | Funktion | Bemerkung                                |
|------------------------|-----|-------|----------|------------------------------------------|
| Mandant                | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                     | I+  | -     | -        | Eindeutige ID                            |
| Klasse                 | I   | -     | PV       | Verweis auf Tabelle **Klassen**          |
| Zeitraum               | I   | -     | PV       | Verweis auf Tabelle **Zeitraeume**       |
| Jahrgang               | S   | -     | -        | -                                        |
| Klassenleiter1         | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Klassenleiter2         | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Klassenstufe           | A   | -     | V        | Verweis auf Tabelle **Klassenstufen**    |
| Fachtafel              | A   | -     | V        | Verweis auf Tabelle **Fachtafeln**       |
| Unterrichtsform        | A   | -     | V        | Verweis auf Tabelle **Unterrichtsformen** |
| Unterrichtstage        | S   | -     | -        | -                                        |
| Klassensprecher1       | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Klassensprecher2       | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Klassenelternsprecher1 | I   | -     | V        | Verweis auf Tabelle **Sorgeberechtigte** |
| Klassenelternsprecher2 | I   | -     | V        | Verweis auf Tabelle **Sorgeberechtigte** |
| Klassenwahlvertreter1  | I   | -     | V        | Verweis auf Tabelle **Sorgeberechtigte** |
| Klassenwahlvertreter2  | I   | -     | V        | Verweis auf Tabelle **Sorgeberechtigte** |
| Klassenraum            | I   | -     | V        | Verweis auf Tabelle **Raeume**           |


