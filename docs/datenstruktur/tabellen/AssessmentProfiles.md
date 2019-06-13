#       Tabelle AssessmentProfiles



| Feldname      | Typ | Größe | Funktion | Bemerkung                                |
|---------------|-----|-------|----------|------------------------------------------|
| Mandant       | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID            | I+  | -     | P        | -                                        |
| EnbreaID      | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Code          | A   | 20    | -        | Kürzel für Bewertungsprofil              |
| Name          | A   | 100   | -        | Bezeichnung                              |
| Configuration | S   | -     | -        | Mögliche Werte:<br/>0 = keine Bewertung<br/>1 = Grade<br/>2 = Report<br/>3 = Grade and Report |
| GradeSystem   | I   | -     | V        | Verweis auf Tabelle **GradeSystems**     |
| Description   | A   | 300   | -        | Text                                     |
| InternalCode  | A   | 3     | -        | Interner Code<br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |


