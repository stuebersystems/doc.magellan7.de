# Tabelle tblStudentAchievements



| Feldname           | Typ | Größe | Funktion | Bemerkung                                |
|--------------------|-----|-------|----------|------------------------------------------|
| Mandant            | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | P        | -                                        |
| EnbreaID           | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| StudentTerm        | I   | -     | V        | Verweis auf Tabelle **SchuelerZeitraeume** |
| AchievementProfile | I   | -     | V        | Verweis auf Tabelle **AchievementProfiles** |
| Grade              | I   | -     | V        | Verweis auf Tabelle **GradesEntry**      |
| GradeFactor        | N   | -     | -        | -                                        |
| Report             | M   | -     | -        | Text                                     |
| Position           | I   | -     | V        | Verweis auf Tabelle **AssessmentProfiles** |


