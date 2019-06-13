# Tabelle SchuelerFachdaten


| Feldname               | Typ | Größe | Funktion | Bemerkung                                |
|------------------------|-----|-------|----------|------------------------------------------|
| Mandant                | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                     | I+  | -     | P        | -                                        |
| Schueler               | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Klasse                 | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| Zeitraum               | I   | -     | V        | Verweis auf Tabelle **Zeitraeume**       |
| Fach                   | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Unterrichtsart         | A   | -     | V        | Verweis auf Tabelle **Unterrichtsarten** |
| Fachstatus             | A   | -     | V        | Verweis auf Tabelle **Fachstati**        |
| Schwerpunkt            | A   | -     | V        | Verweis auf Tabelle **Fachschwerpunkte** |
| Niveau                 | A   | -     | V        | Verweis auf Tabelle **Fachniveaus**      |
| KursNr                 | S   | -     | -        | -                                        |
| Beurteilung            | M   | -     | -        | -                                        |
| Note1                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note2                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note3                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note4                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note5                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note6                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note7                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note8                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note9                  | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note10                 | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note11                 | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note12                 | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note13                 | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Note14                 | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Vornote                | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Endnote1               | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Endnote2               | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Faktor                 | N   | -     | -        | -                                        |
| Position               | S   | -     | -        | -                                        |
| Merkmal                | A   | 8     | -        | -                                        |
| Lehrer                 | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| ZusatzKlasse           | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| IstStammkurs           | A   | 1     | -        | -                                        |
| Endnote1Fortschreiben  | A   | 1     | -        | -                                        |
| Mahnung                | S   | -     | -        | Mögliche Werte:<br/>0 = Mahnung<br/>1 = Nachmahnung<br/>2 = Nachprüfung |
| Hauptfach              | I   | -     | V        | Verweis auf Tabelle **Faecher**<br/>Übergeordnetes Fach für das Feld „Fach“ |
| Bilingual              | A   | -     | V        | Verweis auf Tabelle **Kurssprachen**     |
| HausaufgabenVergessen  | S   | -     | -        | -                                        |
| ArbeitsmittelVergessen | S   | -     | -        | -                                        |
| Muendlich              | A   | 1     | -        | -                                        |



