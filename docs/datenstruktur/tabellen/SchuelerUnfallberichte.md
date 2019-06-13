# Tabelle SchuelerUnfallberichte



| Feldname                  | Typ | Größe | Funktion | Bemerkung                                |
|---------------------------|-----|-------|----------|------------------------------------------|
| Mandant                   | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                        | I+  | -     | P        | -                                        |
| Schueler                  | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Empfaenger                | I   | -     | V        | Verweis auf Tabelle **Adressen**         |
| Toedlich                  | A   | 1     | -        | Mögliche Werte:<br/>N = Nein<br/>J  = Ja |
| UnfallDatum               | D   | -     | -        | -                                        |
| UnfallZeit                | T   | -     | -        | -                                        |
| UnfallOrt                 | M   | -     | -        | -                                        |
| UnfallHergang             | M   | -     | -        | -                                        |
| SchilderungVersicherter   | A   | 1     | -        | Mögliche Werte:<br/>N = Nein, andere Person<br/>J  = Ja, Versicherter |
| VerletzteKoerperteile     | M   | -     | -        | -                                        |
| Verletzungsart            | M   | -     | -        | -                                        |
| UnterbrechungBesuch       | A   | 1     | -        | Mögliche Werte:<br/>N = Nein<br/>J  = Sofort<br/>S = Später |
| UnterbrechungBesuchAm     | D   | -     | -        | Wenn Feld UnterbrechungBesuch=S, dann ist hier das Datum eingetragen |
| UnterbrechungBesuchStunde | S   | -     | -        | Wenn Feld UnterbrechungBesuch=S, dann ist hier die Stunde eingetragen |
| WiederaufnahmeBesuch      | A   | 1     | -        | Mögliche Werte:<br/>N = Nein<br/>J  = Ja |
| WiederaufnahmeBesuchAm    | D   | -     | -        | Wenn Feld WiederaufnahmeBesuch=J, dann ist hier das Datum eingetragen |
| Zeuge                     | M   | -     | -        | -                                        |
| Augenzeuge                | A   | 1     | -        | Mögliche Werte:<br/>N = Nein<br/>J  = Ja |
| Behandlung                | M   | -     | -        | Name behandelnder Arzt/Krankenhaus       |
| BehandlungUhrzeitVon      | T   | -     | -        | -                                        |
| BehandlungUhrzeitBis      | T   | -     | -        | -                                        |
| Datum                     | D   | -     | -        | Datum des Unfallberichts                 |
| Leiter                    | A   | 300   | -        | Leiter (Beauftragter) der Einrichtung    |
| Telefon                   | A   | 30    | -        | Rufnummer für Rückfragen                 |

