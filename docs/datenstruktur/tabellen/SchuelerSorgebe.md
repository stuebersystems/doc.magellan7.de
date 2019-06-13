# Tabelle SchuelerSorgebe


| Feldname          | Typ | Größe | Funktion | Bemerkung                                |
|-------------------|-----|-------|----------|------------------------------------------|
| Mandant           | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                | I+  | -     | P        | -                                        |
| Schueler          | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Sorgebe           | I   | -     | V        | Verweis auf Tabelle **Sorgeberechtigte** |
| Lehrer            | I   | -     | V        | Verweis auf Ansicht **Lehrer**           |
| Person            | I   | -     | V        | Verweis auf Tabelle **Personen**         |
| Geschwister       | I   | -     | V        | Verweis auf Tabelle **Schueler**         |
| Familiennr        | A   | 50    | -        | -                                        |
| Verhaeltnis       | S   | -     | -        | Wert / Ausgabe in der Oberfläche <br/>  0 = Mutter <br/> 1 = Vater <br/> 2 = Eltern <br/> 3 = Erziehungsberechtigte(r) <br/> 4 = Sorgeberechtigte(r) <br/> 5 = Ansprechpartner(in) <br/> 6 = Vormund <br/> 7 = Großmutter <br/> 8 = Großvater <br/> 9 =Pflegeeltern <br/> 11 = Verhältnis1 <br/> 12 = Verhältnis2 <br/> 13 = Verhältnis3 <br/> 14 = Verhältnis4 <br/> 15 = Verhältnis5 <br/> 16 = Verhältnis6 <br/> 17 = Verhältnis7 <br/> 18 = Verhältnis8 <br/> 19 = Verhältnis9 <br/> 20 = Verhältnis <br/> 10 = "(Werte für die Verhältnis 11 … 20 können über „Bezeichnungen anpassen"" ersetzt werden)" <br/> 21 = Onkel <br/> 22 = Tante <br/> 23 = Bruder <br/> 24 = Schwester <br/> 25 = Erzieher <br/> 26 = Notfall <br/> 27 = Gasteltern       |
| Sorgerecht        | L   | -     | -        | -                                        |
| Benachrichtigung  | S   | -     | -        | Mögliche Werte:<br/>0 = Immer<br/>1 = Nur im Notfall<br/>2 = Nie |
| SeriendruckName1  | A   | 300   | -        | -                                        |
| SereindruckName2  | A   | 300   | -        | -                                        |
| Briefempfaenger   | A   | 300   | -        | -                                        |
| Briefanrede       | A   | 300   | -        | -                                        |
| TelefonPrioritaet | S   | -     | -        | Mögliche Werte:<br/>0 = Telefon privat<br/>1 = Telefon beruf<br/>2 = Mobil |
| Position          | S   | -     | -        | -                                        |
| Bemerkung         | M   | -     | -        | -                                        |


