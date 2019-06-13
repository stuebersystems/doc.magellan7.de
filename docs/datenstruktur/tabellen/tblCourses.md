# Tabelle tblCourses



| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID             | I+  | -     | P        | -                                        |
| EnbreaID       | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Term           | I   | -     | V        | Zeitraum<br/>Verweis auf Tabelle **Zeitraeume** |
| Subject        | I   | -     | V        | Fach<br/>Verweis auf Tabelle **Faecher** |
| SubjectStatus  | A   | -     | V        | Fachstatus<br/>Verweis auf Tabelle **Fachstati** |
| SubjectType    | A   | -     | V        | Unterrichtsart<br/>Verweis auf Tabelle **Unterrichtsarten** |
| SubjectTeacher | I   | -     | V        | Lehrer<br/> Verweis auf Ansicht **Lehrer** |
| Focus          | A   | -     | V        | Fachschwerpunkt<br/>Verweis auf Tabelle **Fachschwerpunkte** |
| Level          | A   | -     | V        | Fachniveau<br/> Verweis auf Tabelle **FachNiveaus** |
| CourseNo       | S   | -     | -        | KursNr                                   |
| Bilingual      | A   | -     | V        | Verweis auf Tabelle **Kurssprachen**     |
| Attribute      | A   | 8     | -        | Merkmal                                  |


