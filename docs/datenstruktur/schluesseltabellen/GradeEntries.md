#       Tabelle GradeEntrie



| Feldname      | Typ | Größe | Funktion | Bemerkung                                |
|---------------|-----|-------|----------|------------------------------------------|
| Mandant       | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID            | I+  | -     | P        | -                                        |
| EnbreaID      | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| GradeSystem   | I   | -     | V        | Verweis auf Tabelle **GradeSystems**     |
| Code          | A   | 20    | -        | Kürzel für Notensystemeintrag            |
| Name          | A   | 100   | -        | Bezeichnung der Bewertung/Note           |
| ValueNumber   | N   | -     | -        | Wert                                     |
| ValueText     | A   | 100   | -        | Text                                     |
| Internal Code | A   | 3     | -        | Interner Code<br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |


