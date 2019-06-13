# Tabelle Unterrichtseinheiten



| Feldname        | Typ | Größe | Funktion | Bemerkung                                |
|-----------------|-----|-------|----------|------------------------------------------|
| Mandant         | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID              | I+  | -     | P        | -                                        |
| VeranstaltungNr | I   | -     | I        | Veranstaltungsnummer aus daVinci         |
| Klasse          | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Fach            | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Unterrichtsart  | A   | -     | V        | Verweis auf Tabelle **Unterichtsarten**  |
| Fachstatus      | A   | -     | V        | Verweis auf Tabelle **Fachstati**        |
| Schwerpunkt     | A   | -     | V        | Verweis auf Tabelle **Fachschwerpunkte** |
| KursNr          | S   | -     | -        | -                                        |
| Soll            | N   | -     | -        | Sollstunden (=Soll aus daVinci)          |
| Angleichung     | N   | -     | -        | Angleichung (=Angleichung aus daVinci)   |
| Bemerkung       | M   | -     | -        | -                                        |

