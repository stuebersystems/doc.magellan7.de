#       Tabelle GradeTypes


| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID           | I+  | -     | P        | -                                        |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Code         | A   | 20    | -        | Kürzel für Art der Bewertung             |
| Name         | A   | 100   | -        | Bezeichnung                              |
| InternalCode | S   | -     | -        | Interner Code<br/>Mögliche Werte:<br/>ASV = Arbeits- und Sozialverhalten<br/>MN = Mündliche Note<br/>MZN = Mündliche Zeugnisnote<br/>SN = Schriftlich Note<br/>SZN = Schriftliche Zeugnisnote<br/>ZN = Zeugnisnote |

