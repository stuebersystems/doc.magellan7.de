# View StudentAchievements

Grundlage sind die Tabellen:

* [tblStudentAchievements](https://doc.magellan7.stueber.de/datenstruktur/tabellen/tblStudentAchievements/)
* [AchievementsProfiles](https://doc.magellan7.stueber.de/datenstruktur/tabellen/AchievementProfiles/)
* [GradeTypes](https://doc.magellan7.stueber.de/datenstruktur/schlusseltabellen-schlusselverzeichnisse/GradeTypes/)
* [AssessmentProfiles](https://doc.magellan7.stueber.de/datenstruktur/tabellen/AssessmentProfiles/)
* [tblCourses](https://doc.magellan7.stueber.de/datenstruktur/tabellen/tblCourses/)
* [Faecher](https://doc.magellan7.stueber.de/datenstruktur/schlusseltabellen-schlusselverzeichnisse/faecher/)


| Feldname           | Typ | Größe | Funktion | Bemerkung |
|--------------------|-----|-------|----------|-----------|
| Mandant            | I   | -     | -        | -         |
| ID                 | I   | -     | -        | -         |
| EnbreaID           | A   | 24    | -        | -         |
| StudentTerm        | I   | -     | -        | -         |
| AchievementProfile | I   | -     | -        | -         |
| ProfileCode        | A   | 20    | -        | -         |
| ProfileName        | A   | 100   | -        | -         |
| Course             | I   | -     | -        | -         |
| CourseCode         | A   | 10    | -        | -         |
| CourseName         | A   | 200   | -        | -         |
| CourseDisplayName  | A   | -     | -        | -         |
| Configuration      | S   | -     | -        | -         |
| GradeType          | I   | -     | -        | -         |
| GradeTypeCode      | A   | 20    | -        | -         |
| GradeTypeName      | A   | 100   | -        | -         |
| AssessmentProfile  | I   | -     | -        | -         |
| ASPCode            | A   | 20    | -        | -         |
| ASPName            | A   | 100   | -        | -         |
| GradeSystem        | I   | -     | -        | -         |
| Grade              | I   | -     | -        | -         |
| GradeFactor        | N   | -     | -        | -         |
| Report             | M   | -     | -        | -         |
| Position           | S   | -     | -        | -         |


