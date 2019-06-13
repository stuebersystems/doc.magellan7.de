# Tabelle Haushaltstitel



| Feldname              | Typ | Größe  | Funktion | Bemerkung                              |
|-----------------------|-----|--------|----------|----------------------------------------|
| Mandant               | I   | -      | PV       | Verweis auf Tabelle **Mandanten**      |
| ID                    | I+  | -      | P        | -                                      |
| Kuerzel               | A   | 20     | -        | -                                      |
| Bezeichnung           | A   | 50     | -        | -                                      |
| Haushalt              | A   | -      | V        | Verweis auf Tabelle **Haushalte**      |
| Haushaltsjahr         | A   | -      | V        | Verweis auf Tabelle **Haushaltsjahre** |
| Restuebernahme        | L   | -      | -        | -                                      |
| Gesamtbetrag          | N   | 18 , 4 | -        | Über Trigger berechneter Wert          |
| SummeHaushaltsstellen | N   | 18 , 4 | -        | Über Trigger berechneter Wert          |
| SummeBuchungen        | N   | 18 , 4 | -        | Über Trigger berechneter Wert          |


