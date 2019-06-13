# Tabelle Klassenbuch


| Feldname           | Typ | Größe | Funktion | Bemerkung                                |
|--------------------|-----|-------|----------|------------------------------------------|
| Mandant            | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                 | I+  | -     | P        | -                                        |
| EintragNr          | I   | -     | -        | -                                        |
| BlockNr            | A   | 20    | -        | -                                        |
| Von                | DT  | -     | -        | -                                        |
| Bis                | DT  | -     | -        | -                                        |
| StundeVon          | I   | -     | -        | -                                        |
| StundeBis          | I   | -     | -        | -                                        |
| Fach               | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Unterrichtsart     | A   | -     | V        | Verweis auf Tabelle **Unterrichtsarten** |
| KursNr             | I   | -     | -        | -                                        |
| Ersatzfach         | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Lehrer             | I   | -     | V        | Verweis auf Tabelle **Lehrer**           |
| Ersatzlehrer       | I   | -     | V        | Verweis auf Tabelle **Lehrer**           |
| Vertretungsgrund   | A   | 240   | -        | -                                        |
| Stoffverteilung    | I   | -     | V        | Verweis auf Tabelle **Stoffverteilungen** |
| Unterrichtsausfall | L   | -     | -        | -                                        |
| UnterrichtVerlegt  | I   | -     | V        | Verweis auf Tabelle **Klassenbuch**      |
| Klassen            | A   | 100   | -        | -                                        |
| Thema              | M   | -     | -        | -                                        |
| Bemerkung          | M   | -     | -        | -                                        |


