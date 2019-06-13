# Tabelle tblLehrerLehraemter



| Feldname       | Typ | Größe | Funktion | Bemerkung                                |
|----------------|-----|-------|----------|------------------------------------------|
| Mandant        | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID             | I   | -     | P        | -                                        |
| Lehrer         | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Lehramt        | A   | -     | V        | Verweis auf Tabelle **Lehraemter**       |
| Typ            | S   | -     | -        | Mögliche Werte:<br/>0 = Standard<br/>1 = Lehrbefähigung<br/>2 = Unterrichtserlaubnisg<br/>3 = Unterrichtsauftrag<br/>4 = Unterrichtsbefugnis<br/>5 = Lehrbefähigung kleine Fakultas<br/>6 = Lehrbefähigung große Fakultas |
| Pruefungsbezug | A   | -     | PV       | Verweis auf Tabelle **LehrerPruefungsbezug** |
| JahrgangVon    | S   | -     | -        | -                                        |
| JahrgangBis    | S   | -     | -        | -                                        |
| Bemerkung      | A   | 300   | -        | -                                        |


	
