# Tabelle KlassenbuchVermerke




| Feldname                 | Typ | Größe | Funktion | Bemerkung                                |
|--------------------------|-----|-------|----------|------------------------------------------|
| Mandant                  | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                       | I+  | -     | P        | -                                        |
| Klassenbucheintrag       | I   | -     | V        | Verweis auf Tabelle **Klassenbuch**      |
| Eintragungsdatum         | D   | -     | -        | -                                        |
| EintragNr                | I   | -     | -        | -                                        |
| EintragNrSchueler        | I   | -     | -        | -                                        |
| Schueler                 | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Eintragungskategorie     | A   | -     | V        | Verweis auf Tabelle **Eintragungskategorien** |
| Eintragungstext          | M   | -     | -        | -                                        |
| Bemerkung                | M   | -     | -        | -                                        |
| Massnahmenkategorie      | A   | -     | V        | Verweis auf Tabelle **Massnahmenkategorien** |
| LogErsteintrag           | DT  | -     | -        | -                                        |
| LogErsteintrag_Benutzer  | A   | 20    | -        | -                                        |
| LetzteAenderung          | DT  | -     | -        | -                                        |
| LetzteAenderung_Benutzer | A   | 20    | -        | -                                        |



