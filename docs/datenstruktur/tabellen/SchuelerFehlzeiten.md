# Tabelle SchuelerFehlzeiten


| Feldname                    | Typ | Größe | Funktion | Bemerkung                                |
|-----------------------------|-----|-------|----------|------------------------------------------|
| Mandant                     | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                          | I+  | -     | P        | -                                        |
| Klassenbucheintrag          | I   | -     | V        | Verweis auf Tabelle **Klassenbuch**      |
| EintragNrSchueler           | I   | -     | -        | -                                        |
| Klasse                      | I   | -     | V        | Verweis auf Tabelle **KlassenbuchKlassen** |
| Schueler                    | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Von                         | DT  | -     | -        | -                                        |
| Bis                         | DT  | -     | -        | -                                        |
| Fehltext                    | M   | -     | -        | -                                        |
| Entschuldigungsgrund        | A   | -     | V        | Verweise auf Tabelle <br/>**Entschuldigungsgruende** |
| Entschuldigt                | L   | -     | -        | -                                        |
| Versaeumt                   | L   | -     | -        | -                                        |
| AnzahlTage                  | I   | -     | -        | -                                        |
| AnzahlStunden               | N   | -     | -        | -                                        |
| LogErsteintrag              | DT  | -     | -        | -                                        |
| LogErsteintrag_Benutzer     | A   | 20    | -        | -                                        |
| LogLetzteAenderung          | DT  | -     | -        | -                                        |
| LogLetzteAenderung_Benutzer | A   | 20    | -        | -                                        |
| Fehlgrund                   | A   | -     | V        | Verweis auf Tabelle **SchuelerFehlgruende** |
| Art                         | S   | -     | -        | Mögliche Werte: <br/>0 = Fehlzeit<br/>1 = Abwesenheit/Pausiert |
| Bemerkung                   | M   | -     | -        | -                                        |




