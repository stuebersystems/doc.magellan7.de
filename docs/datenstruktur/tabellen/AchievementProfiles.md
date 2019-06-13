#        Tabelle AchievementProfiles



| Feldname          | Typ | Größe | Funktion | Bemerkung                                |
|-------------------|-----|-------|----------|------------------------------------------|
| Mandant           | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                | I+  | -     | P        | -                                        |
| EnbreaID          | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| ClassTerm         | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Course            | I   | -     | V        | Verweis auf Tabelle **tblCourses**       |
| Code              | A   | 20    | -        | Kürzel für Leistungsprofile              |
| Name              | A   | 100   | -        | Bezeichnung                              |
| Configuration     | S   | -     | -        | Mögliche Werte:<br/>0 = Grade<br/>1 = Report<br/>2 = Grade and Report<br/>3 = ComplexReport |
| GradeSystem       | I   | -     | V        | Verweis auf Tabelle **GradeSystems**     |
| GradeType         | I   | -     | V        | Verweis auf Tabelle **GradeTypes**       |
| AssessmentProfile | I   | -     | V        | Verweis auf Tabelle **AssessmentProfiles** |
| Description       | A   | 300   | -        | Text                                     |
| InternalCode      | A   | 3     | -        | Interner Code <br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |


