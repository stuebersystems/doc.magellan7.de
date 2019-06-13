# Tabelle Buchungen



| Feldname        | Typ | Größe | Funktion | Bemerkung                                |
|-----------------|-----|-------|----------|------------------------------------------|
| Mandant         | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID              | I   | -     | PV       | -                                        |
| Haushaltsstelle | I   | -     | V        | Verweis auf Tabelle **Haushaltsstellen** |
| Buchungsart     | S   | -     | -        | Mögliche Werte:<br/>0 = Ausgabe<br/>1 = Einnahme<br/>2 = Ausgabe-Korrektur<br/>3 = Einnahme-Korrektur<br/>4 = Geplante Ausgabe |
| Bereich         | A   | -     | V        | Verweis auf Tabelle **Buchungsbereiche** |
| Datum           | D   | -     | -        | -                                        |
| Betrag          | N   | -     | -        | -                                        |
| Grund           | M   | -     | -        | -                                        |
| BelegNr         | A   | 15    | -        | -                                        |
| Besteller       | A   | 20    | -        | -                                        |
| BestellNr       | A   | 15    | -        | -                                        |
| BestellDatum    | D   | -     | -        | -                                        |
| RechnungNr      | A   | 15    | -        | -                                        |
| LieferscheinNr  | A   | 15    | -        | -                                        |
| Lieferant       | I   | -     | V        | Verweis auf Tabelle **Lieferanten**      |
| Log_Datum       | D   | -     | -        | -                                        |
| Log_Uhrzeit     | T   | -     | -        | -                                        |
| Log_Benutzer    | A   | 20    | -        | -                                        |

