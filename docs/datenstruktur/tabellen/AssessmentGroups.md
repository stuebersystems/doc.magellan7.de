#        Tabelle AssessmentGroups



| Feldname      | Typ | Größe | Funktion | Bemerkung                                |
|---------------|-----|-------|----------|------------------------------------------|
| Mandant       | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID            | I+  | -     | P        | -                                        |
| EnbreaID      | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Profile       | I   | -     | V        | Verweis auf Tabelle **AssessmentProfiles** |
| Code          | A   | 20    | -        | Kürzel für Bewertungsgruppen             |
| Name          | A   | 100   | -        | Bezeichnung                              |
| Configuration | S   | -     | -        | Mögliche Werte:<br/>0 = keine Bewertung<br/>1 = Grade<br/>2 = Report<br/>3 = Grade and Report |
| GradeSystem   | I   | -     | V        | Verweis auf Tabelle **GradeSystems**     |
| Position      | I   | -     | -        | -                                        |
| Description   | A   | 300   | -        | Text                                     |
| InternalCode  | A   | 3     | -        | Interner Code<br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |


