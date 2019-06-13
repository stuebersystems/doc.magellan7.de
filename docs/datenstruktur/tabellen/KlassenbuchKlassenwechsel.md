#      Tabelle KlassenbuchKlassenwechsel


| Feldname        | Typ | Größe | Funktion | Bemerkung                         |
|-----------------|-----|-------|----------|-----------------------------------|
| Mandant         | I   | -     | PV       | Verweis auf Tabelle **Mandanten** |
| ID              | I+  | -     | P        | -                                 |
| Schueler        | I   | -     | V        | Verweis auf Tabelle **Schueler**  |
| Von             | D   | -     | -        | -                                 |
| Bis             | D   | -     | -        | -                                 |
| KlasseRegulaer  | I   | -     | V        | Verweis auf Tabelle **Klassen**   |
| KlasseTemporaer | I   | -     | V        | Verweis auf Tabelle **Klassen**   |
| Grund           | M   | -     | -        | -                                 |

