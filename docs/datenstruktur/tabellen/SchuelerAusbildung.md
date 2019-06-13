# Tabelle SchuelerAusbildung


| Feldname           | Typ | Größe | Funktion | Bemerkung                                |
|--------------------|-----|-------|----------|------------------------------------------|
| Mandant            | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | P        | -                                        |
| Schueler           | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Betrieb            | I   | -     | V        | Verweis auf Tabelle **Betriebe**         |
| AusbilderKontakt   | I   | -     | V        | Verweis auf Tabelle **BetriebeKontakte** |
| PraxisBetrieb      | I   | -     | V        | Verweis auf Tabelle **Betriebe**         |
| PraxisKontakt      | I   | -     | V        | Verweis auf Tabelle **BetriebeKontakte** |
| Beruf              | A   | -     | V        | Verweis auf Tabelle **Berufe**           |
| Bildungsgang       | A   | -     | V        | Verweis auf Tabelle **Bildungsgaenge**   |
| AusbildungVon      | D   | -     | -        | -                                        |
| AusbildungBis      | D   | -     | -        | -                                        |
| Ausbildungsdauer   | N   | -     | -        | -                                        |
| PraxisVon          | D   | -     | -        | -                                        |
| PraxisBis          | D   | -     | -        | -                                        |
| Praxisdauer        | N   | -     | -        | -                                        |
| Vertrag            | L   | -     | -        | -                                        |
| Vertragsart        | A   | -     | V        | Verweis auf Tabelle **Vertragsarten**    |
| Vertragsnr         | A   | 30    | -        | -                                        |
| VertragVorgelegtAm | D   | -     | -        | -                                        |
| Bemerkung          | M   | -     | -        | -                                        |


