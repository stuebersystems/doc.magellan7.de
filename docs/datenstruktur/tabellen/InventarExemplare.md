# Tabelle InventarExemplare



| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID             | I+  | -     | P        | -                                        |
| Inventar       | I   | -     | V        | Verweis auf Tabelle **Inventar**         |
| Bewegungsart   | S   | -     | -        | Mögliche Werte:<br/>0 = Zugang<br/>1 = Abgang |
| Bewegungsdatum | D   | -     | -        | -                                        |
| Anzahl         | S   | -     | -        | -                                        |
| Betrag         | N   | -     | -        | -                                        |
| Waehrung       | A   | -     | V        | Verweis auf Tabelle **Waehrungen**       |
| Lieferant      | I   | -     | V        | Verweis auf Tabelle **Lieferanten**      |
| Bemerkung      | M   | -     | -        | -                                        |






