# Tabelle UnterrichtseinheitenLehrer



| Feldname           | Typ | Größe | Funktion | Bemerkung                                |
|--------------------|-----|-------|----------|------------------------------------------|
| Mandant            | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | P        | -                                        |
| Unterrichtseinheit | I   | -     | V        | Verweis auf Tabelle **Unterrichtseinheiten** |
| Lehrer             | I   | -     | V        | Verweis auf Tabelle **Lehrer**           |
| Ist                | N   | -     | -        | Iststunden  (=Lehrer-Ist aus daVinci)    |
| Bemerkung          | M   | -     | -        | -                                        |
| Gruppenunterricht  | L   | 1     | -        | Ist nur Unterricht in einer Schülergruppe |


