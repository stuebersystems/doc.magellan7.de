# View ClassCourses

Grundlage sind:
* [KlassenZeitraeume](https://doc.magellan7.stueber.de/datenstruktur/tabellen/KlassenZeitraeume/)
* [tblClassCourses](https://doc.magellan7.stueber.de/datenstruktur/tabellen/tblClassCourses/)
* [tblCourses](https://doc.magellan7.stueber.de/datenstruktur/tabellen/tblCourses/)


| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID             | I+  | -     | P        | Verweis auf Tabelle **tblClassCourses**  |
| ClassTerm      | I   | -     | -        | Verweis auf Tabelle **tblClassCourses**  |
| Class          | I   | -     | -        | Verweis auf Tabelle **KlassenZeitraeume** |
| Term           | I   | -     | -        | Verweis auf Tabelle **tblCourses**       |
| Course         | I   | -     | -        | Verweis auf Tabelle **tblClassCourses**  |
| EnbreaID       | I   | -     | -        | EnbreaID                                 |
| Subject        | I   | -     | -        | Verweis auf Tabelle **tblCourses**       |
| SubjectStatus  | -   | -     | -        | Verweis auf Tabelle **tblCourses**       |
| SubjectType    | A   | 10    | -        | Verweis auf Tabelle **tblCourses**       |
| SubjectTeacher | A   | 10    | -        | Verweis auf Tabelle **tblCourses**       |
| Focus          | A   | 10    | -        | Verweis auf Tabelle **tblCourses**       |
| Level          | A   | 10    | -        | Verweis auf Tabelle **tblCourses**       |
| CourseNo       | S   | -     | -        | Verweis auf Tabelle **tblCourses**       |
| Bilingual      | A   | 10    | -        | Verweis auf Tabelle **tblCourses**       |
| Attribute      | A   | 8     | -        | Verweis auf Tabelle **tblCourses**       |

