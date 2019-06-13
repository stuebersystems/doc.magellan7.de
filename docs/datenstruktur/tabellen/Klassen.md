#	Tabelle Klassen



| Feldname               | Typ | Größe | Funktion | Bemerkung                                |
|------------------------|-----|-------|----------|------------------------------------------|
| Mandanten              | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                     | I   | -     | P        | -                                        |
| GUID                   | A   | 32    | -        | -                                        |
| IDIntern               | I   | -     | -        | -                                        |
| IDExtern               | I   | -     | -        | -                                        |
| GUIDExtern             | A   | 36    | -        | -                                        |
| Kuerzel                | A   | 20    | -        | -                                        |
| KuerzelAlpha           | A   | 8     | -        | -                                        |
| KuerzelStatistik       | A   | 20    | -        | -                                        |
| Langname1              | A   | 100   | -        | -                                        |
| Langname2              | A   | 100   | -        | -                                        |
| Klassenart             | S   | -     | -        | Mögliche Werte:<br/>0 = Standardklasse<br/>1 = Ganztagsklasse<br/>2 = Oberstufenjahrgang (Nur Kurse)<br/>3 = Oberstufenjahrgang (Leistungs- u. Grundkurse)<br/>4 = Abschlussklasse<br/>5 = Kombinationsklasse<br/><br/>6 = Schulkindergarten<br/>7 = Standardklasse mit Oberstufensynchronisation |
| Notenart               | S   | -     | -        | Mögliche Werte:<br/>0 = Notenwerte<br/>1 = Punktwerte<br/>2 = Beurteilungen |
| Abteilung              | A   | -     | V        | Verweis auf Tabelle **Abteilungen**      |
| Schulform              | A   | -     | V        | Verweis auf Tabelle **Schulformen**      |
| Schulart               | A   | -     | V        | Verweis auf Tabelle *Schularten*         |
| Organisation           | A   | -     | V        | Verweis auf Tabelle **Organisationen**   |
| Behinderung            | A   | -     | V        | Verweis auf Tabelle **Behinderungsarten** |
| Foerderschwerpunkt1    | A   | -     | V        | Verweis auf Tabelle **FoerderSchwerpunkte** |
| Foerderschwerpunkt2    | A   | -     | V        | Verweis auf Tabelle **FoerderSchwerpunkte** |
| Beruf                  | A   | -     | V        | Verweis auf Tabelle **Berufe**           |
| Bildungsgang           | A   | -     | V        | Verweis auf Tabelle **Bildungsgaenge**   |
| Berufsfeld             | A   | -     | V        | Verweis auf Tabelle **Berufsfelder**     |
| Integration            | A   | -     | V        | Verweis auf Tabelle **Integrationsmerkmale** |
| Einzelintegration      | L   | -     | -        | -                                        |
| Laenderuebergreifend   | L   | -     | -        | -                                        |
| Schulartuebergreifend  | L   | -     | -        | -                                        |
| Schulstelle            | A   | -     | V        | Verweis auf Tabelle **Schulstellen**     |
| Foerderung             | A   | -     | V        | Verweis auf Tabelle **Foerderungen**     |
| Regelbeitrag           | N   | -     | -        | Regelbeitrag für **Lernmittel**          |
| Bemerkung              | M   | -     | -        | -                                        |
| MerkmalA1              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalA2              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalA3              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalA4              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalA5              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalA6              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalS1              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalS2              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalS3              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalS4              | A   | -     | V        | Verweis auf Tabelle **Klassenmerkmale**  |
| MerkmalB1              | A   | 15    | -        | -                                        |
| MerkmalB2              | A   | 15    | -        | -                                        |
| MerkmalB3              | A   | 15    | -        | -                                        |
| MerkmalB4              | A   | 15    | -        | -                                        |
| KBGueltigVon           | D   | -     | -        | Klassenbuch gültig von                   |
| KBGueltigBis           | D   | -     | -        | Klassenbuch gültig bis                   |
| KBFuehrer              | I   | -     | V        | Klassenbuchführer, Verweis auf Ansicht **Lehrer** |
| KBBemerkung            | M   | -     | -        | Klassenbuch Bemerkung                    |
| Klassenorganisation    | A   | 10    | -        | Verweis auf Tabelle **Klassenorganisationen** |
| Maske                  | S   | -     | -        | Standardmaske der Klasse                 |
| Schuelerplan           | L   | -     | -        | Soll bei der Anzeige der Stundenplans der Schüler der Klasse der individuelle Schülerplan anstelle des Klassenplan angezeigt werden |
| NaechsteKlasse         | I   | -     | V        | Verweis auf Tabelle **Klassen**          |
| NaechsteKlasseZeitraum | I   | -     | V        | Verweis auf Tabelle **Zeitraeume**       |
| EnbreaID               | A   | 24    | -        | Externer Identifikator aus ENBREA        |

