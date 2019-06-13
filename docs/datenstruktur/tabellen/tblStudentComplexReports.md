# Tabelle tblStudentComplexReports



| Feldname           | Typ | Größe | Funktion | Bemerkung                                |
|--------------------|-----|-------|----------|------------------------------------------|
| Mandant            | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | P        | -                                        |
| EnbreaID           | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| StudentAchievement | I   | -     | V        | Verweis auf Tabelle **tblStudentAchievements** |
| Profile            | I   | -     | V        | Verweis auf Tabelle **AssessmentProfiles** |
| Group              | I   | -     | V        | Verweis auf Tabelle **AssessmentGroups** |
| Entry              | I   | -     | V        | Verweis auf Tabelle **AssesmentEntries** |
| Grade              | I   | -     | V        | Verweis auf Tabelle **GradeEntries**     |
| Report             | M   | -     | -        | Beurteilung                              |

