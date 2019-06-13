# Tabelle SchuelerZeitraeume


| Feldname               | Typ | Größe | Funktion | Bemerkung                                |
|------------------------|-----|-------|----------|------------------------------------------|
| Mandant                | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                     | I+  | -     | -        | Eindeutige ID                            |
| KlassenZeitraumID      | I   | -     | V        | Verweis auf Tabelle **KlassenZeitraeume** |
| Schueler               | I   | -     | PV       | Verweis auf Tabelle **Schueler**         |
| Klasse                 | I   | -     | PV       | Verweis auf Tabelle **Klassen**          |
| Zeitraum               | I   | -     | PV       | Verweis auf Tabelle **Zeitraeume**       |
| Gewechselt             | A   | 1     | -        | Mögliche Werte:<br/>N = Hat (noch) nicht gewechselt<br/>J = Hat innerhalb des Zeitraums gewechselt<br/>+ = Hat in den nächsten Zeitraum gewechselt |
| Ausbildungsjahr        | S   | -     | -        | -                                        |
| Schulbesuchsjahr       | S   | -     | -        | -                                        |
| Fachkombination        | A   | 4     | -        | -                                        |
| TeilnahmeZusatzangebot | L   | -     | -        | -                                        |
| SportBefreit           | L   | -     | -        | -                                        |
| Unterrichtstage        | S   | -     | -        | -                                        |
| Fehltage               | S   | -     | -        | -                                        |
| FehltageU              | S   | -     | -        | -                                        |
| Fehlstunden            | N   | -     | -        | -                                        |
| FehlstundenU           | N   | -     | -        | -                                        |
| Versaeumnisse          | S   | -     | -        | -                                        |
| Verhalten              | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| Mitarbeit              | I   | -     | V        | Verweis auf Tabelle **Noten**            |
| ZeugniskonferenzAm     | D   | -     | -        | -                                        |
| ZeugnisausgabeAm       | D   | -     | -        | -                                        |
| Zeugnisausgabe2Am      | D   | -     | -        | -                                        |
| Tutor                  | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Pruefungsvorsitz       | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Verordnung             | A   | -     | V        | Verweis auf Tabelle **Verordnungen**     |
| Anrechnungsdatum       | D   | -     | -        | -                                        |
| Status                 | S   | -     | -        | Mögliche Werte:<br/>0 = Abschluss berechnen<br/>1 = Abschluss erreicht<br/>2 = Abschluss nicht erreicht |
| Meldungen              | M   | -     | -        | -                                        |
| Log_Datum              | D   | -     | -        | -                                        |
| Log_Uhrzeit            | T   | -     | -        | -                                        |
| Log_Benutzer           | A   | 20    | -        | -                                        |
| Ausbildung             | I   | -     | -        | -                                        |
| Zwischenzeugnis        | L   | -     | -        | -                                        |
| Leistungsanforderungen | L   | -     | -        | -                                        |
| Jahrgang               | I   | -     | -        | -                                        |


