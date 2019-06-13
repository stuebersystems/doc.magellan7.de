#       Tabelle AssessmentEntries


| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID           | I+  | -     | P        | -                                        |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Profile      | I   | -     | V        | Verweis auf Tabelle **AssessmentProfiles** |
| Group        | I   | -     | V        | Verweis auf Tabelle **AssessmentGroups** |
| Code         | A   | 20    | -        | Kürzel für Bewertungseinträge           |
| Name         | A   | 100   | -        | Bezeichnung                              |
| GradeSystem  | I   | -     | V        | Verweis auf Tabelle **GradeSystems**     |
| Position     | I   | -     | -        | -                                        |
| Description  | A   | 300   | -        | Text                                     |
| InternalCode | A   | 3     | -        | Interner Code<br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |


