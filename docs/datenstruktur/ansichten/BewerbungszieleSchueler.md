# View BewerbungszieleSchueler

Diese Ansicht listet alle Bewerbungsziele pro Schüler auf.  Grundlage ist die Tabelle [Schueler](https://doc.magellan7.stueber.de/datenstruktur/tabellen/Schueler/).


| Feldname       | Typ | Größe | Funktion | Bemerkung                         |
|----------------|-----|-------|----------|-----------------------------------|
| Mandant        | I+  | -     | P        | Verweis auf Tabelle **Mandanten** |
| Schueler       | I   | -     | -        | Verweis auf Tabelle **Schueler**  |
| Bewerbungsziel | A   | 100   | -        | Verweis auf Tabelle **Schueler**  |
| Rangzahl       | N   | -     | -        | Verweis auf Tabelle **Schueler**  |


