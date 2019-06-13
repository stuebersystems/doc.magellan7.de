# Tabelle StudentCourseAttendance


| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID             | I+  | -     | P        | -                                        |
| EnbreaID       | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| StudentTerm    | I   | -     | V        | SchülerZeitraum<br/>Verweis auf Tabelle<br/>**SchuelerZeitraeume** |
| Course         | I   | -     | V        | Kurs<br/>Verweis auf Tabelle **tblCourses** |
| ForgotHomework | S   | -     | -        | HausaufgabenVergessen                    |
| ForgotMaterial | S   | -     | -        | ArbeitsmittelVergessen                   |
| Position       | I   | -     | -        | -                                        |


