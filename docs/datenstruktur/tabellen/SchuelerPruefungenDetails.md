# Tabelle SchuelerPrüfungenDetails



| Feldname           | Typ | Größe | Funktion | Bemerkung                                |
|--------------------|-----|-------|----------|------------------------------------------|
| Mandant            | I   | -     | V        | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | -        | -                                        |
| SchuelerZeitraumID | I   | -     | V        | Verweis auf Tabelle **SchuelerZeitraeume** |
| Fach               | I   | -     | V        | Verweis auf Tabelle ** Faecher**         |
| ParentSPD          | I   | -     | V        | -                                        |
| Fachstatus         | A   | -     | V        | Verweis auf Tabelle **Fachstati**        |
| Fachgruppe         | S   | -     | -        | -                                        |
| Position           | S   | -     | -        | -                                        |
| HJ1_Lehrer         | I   | -     | V        | Verweis auf Tabelle **tblLehrer**        |
| HJ1_Unterrichtsart | A   | 10    | V        | -                                        |
| HJ1_Note           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| HJ2_Lehrer         | I   | -     | V        | Verweis auf Tabelle **tblLehrer**        |
| HJ2_Unterrichtsart | A   | -     | V        | Verweis auf Tabelle **Unterrichtsarten** |
| HJ2_Note           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| HJ3_Lehrer         | I   | -     | V        | Verweis auf Tabelle **tblLehrer**        |
| HJ3_Unterrichtsart | A   | -     | V        | Verweis auf Tabelle **Unterrichtsarten** |
| HJ3_Note           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| VN_Unterrichtsart  | A   | -     | V        | Verweis auf Tabelle **Unterrichtsarten** |
| VN_Berechnet       | N   | -     | -        | -                                        |
| VN_Note            | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| VN_NoteMarkiert    | S   | -     | -        | -                                        |
| PR_Note1           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| PR_Note2           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| PR_Note3           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| EN_Unterrichtsart1 | A   | 10    | V        | -                                        |
| EN_Note1           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| EN_Note1Markiert   | S   | -     | -        | -                                        |
| EN_Unterrichtsart2 | A   | -     | V        | Verweis auf Tabelle **Unterrichtsarten** |
| EN_Note2           | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Merkmal            | A   | 8     | Flag     | -                                        |


