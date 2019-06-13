#        Tabelle GradeSystems




| Feldname     | Typ | Größe | Funktion | Bemerkung                                |
|--------------|-----|-------|----------|------------------------------------------|
| Mandant      | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID           | I+  | -     | P        | -                                        |
| EnbreaID     | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| Code         | A   | 20    | -        | Kürzel für Notensystem                   |
| Name         | A   | 100   | -        | Bezeichnung                              |
| ValueType    | S   | -     | -        | Typ<br/>Mögliche Werte:<br/>0 = Zahlen<br/>1 = Texte |
| Description  | A   | 300   | -        | Beschreibung                             |
| InternalCode | A   | 3     | -        | Interner Code<br/>Mögliche Werte:<br/>werden zukünftig noch festgelegt |


