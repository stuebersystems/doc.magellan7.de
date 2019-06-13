# Tabelle Haushaltsstellen



| Feldname       | Typ | Größe  | Funktion | Bemerkung                              |
|----------------|-----|--------|----------|----------------------------------------|
| Mandant        | I   | -      | PV       | Verweis auf Tabelle **Mandanten**      |
| ID             | I+  | -      | P        | -                                      |
| Haushaltstitel | I   | -      | V        | Verweis auf Tabelle **Haushaltstitel** |
| Kuerzel        | A   | 20     | -        | -                                      |
| Bezeichnung    | A   | 50     | -        | -                                      |
| Gewichtung     | N   | -      | -        | -                                      |
| Restuebernahme | L   | -      | -        | -                                      |
| Verwalter      | A   | 20     | -        | -                                      |
| Gesamtbetrag   | N   | 18 , 4 | -        | Über Trigger berechneter Wert          |
| SummeBuchungen | N   | 18 , 4 | -        | Über Trigger berechneter Wert          |


