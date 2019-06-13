#        Tabelle Medien



| Feldname          | Typ | Größe | Funktion | Bemerkung                                |
|-------------------|-----|-------|----------|------------------------------------------|
| Mandant           | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                | I+  | -     | P        | -                                        |
| Barcode           | A   | 20    | -        | -                                        |
| BarcodePrint      | A   | 20    | -        | -                                        |
| InventarNr        | A   | 15    | -        | -                                        |
| Titel             | A   | 100   | -        | -                                        |
| Untertitel        | A   | 100   | -        | -                                        |
| Medienart         | A   | -     | V        | Verweis auf Tabelle **Medienarten**      |
| Medienkategorie   | A   | -     | V        | Verweis auf Tabelle **Medienkategorien** |
| Standort          | A   | -     | V        | Verweis auf Tabelle **Standorte**        |
| Verlag            | I   | -     | V        | Verweis auf Tabelle **Verlage**          |
| Verlagsname       | A   | 50    | -        | -                                        |
| Verlagsort        | A   | 50    | -        | -                                        |
| Herausgeber       | A   | 50    | -        | -                                        |
| Autor             | A   | 50    | -        | -                                        |
| Signaturvorgabe   | A   | 50    | -        | -                                        |
| Copyright         | A   | 50    | -        | -                                        |
| ISBN              | A   | 20    | -        | -                                        |
| ISSN              | A   | 20    | -        | -                                        |
| Erscheinungsjahr  | S   | -     | -        | -                                        |
| Erscheinungsland  | A   | -     | V        | Verweis auf Tabelle **Staaten**          |
| Erscheinungsweise | A   | -     | V        | Verweis auf Tabelle **Erscheinungsweisen** |
| Sprache           | A   | -     | V        | Verweis auf Tabelle **Sprachen**         |
| Format            | A   | -     | V        | Verweis auf Tabelle **Medienformate**    |
| Umfang            | A   | 100   | -        | -                                        |
| Serie             | A   | 30    | -        | -                                        |
| Band              | A   | 30    | -        | -                                        |
| Heft              | A   | 30    | -        | -                                        |
| Ausgabe           | A   | 30    | -        | -                                        |
| Jahrgang          | S   | -     | -        | -                                        |
| Zusammenfassung   | M   | -     | -        | -                                        |
| Bemerkung         | M   | -     | -        | -                                        |
| Status            | S   | -     | -        | Mögliche Werte:<br/>0 = Ausleihbar<br/>1 = Nicht ausleihbar<br/>2 = Nicht aktuell<br/>3 = Dauerverleih / Teilweise Dauerverleih<br/>4 = Dauerleihgabe / Teilweise Dauerleihgabe |
| Mehrjahresband    | L   | -     | -        | -                                        |
| JahrgangVon       | A   | -     | V        | Verweis auf Tabelle **MedienJahrgaenge** |
| JahrgangBis       | A   | -     | V        | Verweis auf Tabelle **MedienJahrgaenge** |

