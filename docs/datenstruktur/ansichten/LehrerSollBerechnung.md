# View LehrerSollBerechnung

Grundlage ist die Tabelle [tblLehrerSollBerechnung](https://doc.magellan7.stueber.de/datenstruktur/tabellen/LehrerSollBerechnung/).


| Feldname             | Typ | Größe | Funktion | Bemerkung                                |
|----------------------|-----|-------|----------|------------------------------------------|
| Mandant              | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                   | I   | -     | +P       | -                                        |
| Lehrer               | I   | -     | V        | Verweis auf Tabelle **Lehrer**           |
| Von                  | D   | -     | -        | -                                        |
| Bis                  | D   | -     | -        | -                                        |
| Position             | S   | -     | -        | -                                        |
| Dauer                | N   | -     | -        | -                                        |
| LehrerSollSchluessel | I   | -     | V        | Verweis auf Tabelle **LehrerSollSchluessel** |

