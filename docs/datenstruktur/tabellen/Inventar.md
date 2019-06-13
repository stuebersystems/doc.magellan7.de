# Tabelle Inventar



| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID             | I+  | -     | P        | -                                        |
| Barcode        | A   | 20    | -        | -                                        |
| InventarNr     | A   | 15    | -        | -                                        |
| GeraeteNr      | A   | 15    | -        | -                                        |
| Bezeichnung    | A   | 50    | -        | -                                        |
| Kategorie      | A   | -     | V        | Verweis auf Tabelle **InventarKategorien** |
| Standort       | A   | -     | V        | Verweis auf Tabelle **Standorte**        |
| Anfangsbestand | S   | -     | -        | -                                        |
| AnzGesamt      | I   | -     | -        | Über Trigger berechneter Wert            |
| Bemerkung      | M   | -     | -        | -                                        |


