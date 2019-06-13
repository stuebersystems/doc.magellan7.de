# Tabelle SchuelerSchulen



| Feldname         | Typ | Größe | Funktion | Bemerkung                                |
|------------------|-----|-------|----------|------------------------------------------|
| Mandant          | I   | -     | PV       | Verweis auf Tabelle ** Mandanten**       |
| ID               | I+  | -     | P        | -                                        |
| Schueler         | I   | -     | V        | Verweis auf Tabelle ** Schueler**        |
| Schule           | I   | -     | V        | Verweis auf Tabelle ** Schule**          |
| Schulform        | A   | -     | V        | Verweis auf Tabelle ** SchulformenHerkunft** |
| Schulart         | A   | -     | V        | Verweis auf Tabelle ** SchulartenHerkunft** |
| Von              | D   | -     | -        | -                                        |
| Bis              | D   | -     | -        | -                                        |
| LetzteKlasse     | A   | 15    | -        | -                                        |
| Abschluss        | A   | -     | V        | Verweis auf Tabelle ** AbschluesseExtern** |
| Herkunft         | A   | -     | V        | Verweis auf Tabelle ** Herkunftsarten**  |
| Unterlagen       | A   | -     | V        | Verweis auf Tabelle ** Herkunftsunterlagen** |
| Klassenstufe     | A   | -     | V        | Verweis auf Tabelle ** Klassenstufen**   |
| Sprachfoerderung | L   | -     | -        | -                                        |
| Laufbahn         | S   | -     | -        | Mögliche Werte:<br/>0 = Einschulung in die Primarstufe<br/>1 = Übergang in die SEK I<br/>2 = Übergang in die SEK II<br/>3 = Übergang in BBS<br/>4 = Zuletzt besuchte Schule |


