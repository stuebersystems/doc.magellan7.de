#      Tabelle KlassenbuchAufgaben



| Feldname                 | Typ | Größe | Funktion | Bemerkung                                |
|--------------------------|-----|-------|----------|------------------------------------------|
| Mandant                  | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                       | I+  | -     | P        | -                                        |
| Klassenbucheintrag       | I   | -     | V        | Verweis auf Tabelle **Klassenbuch**      |
| Stoffverteilung          | I   | -     | V        | Verweis auf Tabelle **Stoffverteilungen** |
| Aufgabentext             | M   | -     | -        | -                                        |
| Bemerkung                | M   | -     | -        | -                                        |
| LogErsteintrag           | DT  | -     | -        | -                                        |
| LogErsteintrag_Benutzer  | A   | 20    | -        | -                                        |
| LetzteAenderung          | DT  | -     | -        | -                                        |
| LetzteAenderung_Benutzer | A   | 20    | -        | -                                        |


