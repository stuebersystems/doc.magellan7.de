# Tabelle GroupMembers


| Name               | Typ | Größe | Funkt. | Bemerkung                                |
|--------------------|-----|-------|--------|------------------------------------------|
| Mandant            | I   | -     | PV     | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | P      | -                                        |
| EnbreaID           | A   | 24    | -      | Externer Identifikator aus ENBREA        |
| Group              | I   | -     | V      | Verweis auf Tabelle **Groups**           |
| MemberID           | I   | -     | V      | ID der jeweiligen Tabelle je nach Typ    |
| MemberType         | S   | -     | -      | Mögliche Werte:<br/>1 = Person<br/>2 = Lehrer<br/>3 = Schüler<br/>4 = Sorgeberechtigte |
| StartedAt          | D   | -     | -      | -                                        |
| FinishedAt         | D   | -     | -      | -                                        |
| Contribution       | N   | -     | -      | -                                        |
| ContributionPaidOn | D   | -     | -      | -                                        |
| Function1          | A   | 100   | -      | -                                        |
| Function2          | A   | 100   | -      | -                                        |

