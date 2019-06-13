# Tabelle Sorgeberechtigte


| Feldname                  | Typ | Größe | Funktion | Bemerkung                                |
|---------------------------|-----|-------|----------|------------------------------------------|
| Mandant                   | I   | -     | PV       | Verweis auf Tabelle<br>**Mandanten**     |
| ID                        | I+  | -     | P        | -                                        |
| EnbreaID                  | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| GUID                      | A   | 32    | -        | -                                        |
| IDIntern                  | I   | -     | P        | -                                        |
| IDExtern                  | I   | -     | P        | -                                        |
| GUIDExtern                | A   | 36    | -        | -                                        |
| Nachname                  | A   | 100   | -        | -                                        |
| NachnameNative            | A   | 100   | -        | -                                        |
| Namenszusatz              | A   | 100   | -        | -                                        |
| NamenszusatzNative        | A   | 100   | -        | -                                        |
| Vorname                   | A   | 100   | -        | -                                        |
| VornameNative             | A   | 100   | -        | -                                        |
| Vorname2                  | A   | 100   | -        | -                                        |
| VornameNative2            | A   | 100   | -        | -                                        |
| Anrede                    | A   | 1     | -        | **Mögliche Werte:**<br>0 = Frau<br>1 = Herr<br>2 = Frau Dr.<br>3 = Herr Dr.<br>4 = Frau Prof.<br>5 = Herr Prof.<br>6 = Frau Prof. Dr.<br>7 = HerrProf. Dr.<br>8 = Familie<br>9 = Herr und Frau<br>: = Ms.<br/>; = Mrs."<br>< = Mr.<br>= = Mr. and Ms.<br>> = Mr. and Mrs.<br>? = Eheleute |
| Geburtsland               | A   | -     | -        | Verweis auf Tabelle<br>**Staatsangehoerigkeiten** |
| Adresszusatz              | A   | 200   | -        | -                                        |
| Strasse                   | A   | 100   | -        | -                                        |
| Land                      | A   | 3     | -        | -                                        |
| PLZ                       | A   | 5     | -        | -                                        |
| Ort                       | A   | 100   | -        | -                                        |
| Ortsteil                  | A   | 100   | -        | -                                        |
| Adressgebiet              | A   | 300   | -        | -                                        |
| Gemeinde                  | A   | -     | -        | Verweis auf Tabelle<br>**Gemeinden**     |
| TelefonPrivat             | A   | 30    | -        | -                                        |
| TelefonBeruf              | A   | 30    | -        | -                                        |
| Mobil                     | A   | 30    | -        | -                                        |
| Email                     | A   | 100   | -        | -                                        |
| Beruf                     | A   | 50    | -        | -                                        |
| Staatsangeh1              | A   | -     | V        | Verweis auf Tabelle<br>**Staatsangehoerigkeiten** |
| Staatsangeh2              | A   | -     | V        | Verweis auf Tabelle<br>**Staatsangehoerigkeiten** |
| Muttersprache             | A   | -     | V        | Verweis auf Tabelle<br>**Muttersprachen**   |
| Verkehrssprache           | A   | -     | V        | Verweis auf Tabelle<br>**Muttersprachen**   |
| Funktion1                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion2                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion3                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion4                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion5                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion6                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion7                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Funktion8                 | A   | -     | V        | Verweis auf Tabelle<br>**SorgebeFunktionen** |
| Status                    | S   | -     | -        | Mögliche Werte:<br>1 = Erreichbar<br>2 = Nicht erreichbar<br>3 = Verstorben |
| Bemerkung                 | M   | -     | -        | -                                        |
| Status2                   | S   | -     | -        | **Mögliche Werte:**<br>0 = Nicht Aktiv<br>1 = Aktiv |
| Auskunft                  | S   | -     | -        | **Mögliche Werte:**<br>0 = Keine Angabe<br>1 = Geheim |
| Bank1                     | I   | -     | V        | Verweis auf Tabelle<br>**Banken**        |
| Bank1Konto                | A   | 20    | -        | Bankkonto 1                              |
| Bank1IBAN                 | A   | 28    | -        | -                                        |
| Bank1Inhaber              | A   | 300   | -        | -                                        |
| Bank1Info                 | A   | 300   | -        | -                                        |
| Bank1Bemerkung            | A   | 300   | -        | -                                        |
| Bank2                     | I   | -     | V        | Verweis auf Tabelle<br>**Banken**        |
| Bank2konto                | A   | 20    | -        | Bankkonto 2                              |
| Bank2IBAN                 | A   | 28    | -        | -                                        |
| Bank2Inhaber              | A   | 300   | -        | -                                        |
| Bank2Info                 | A   | 300   | -        | -                                        |
| Bank2Bemerkung            | A   | 300   | -        | -                                        |
| Rechnung1Name1            | A   | 100   | -        | Rechnungsadresse 1                       |
| Rechnung1Name2            | A   | 100   | -        | -                                        |
| Rechnung1Strasse          | A   | 100   | -        | -                                        |
| Rechnung1Adressgebiet     | A   | 300   | -        | -                                        |
| Rechnung1Land             | A   | 3     | -        | -                                        |
| Rechnung1PLZ              | A   | 5     | -        | -                                        |
| Rechnung1Ort              | A   | 100   | -        | -                                        |
| Rechnung1Ortsteil         | A   | 100   | -        | -                                        |
| Rechnung1Adresszusatz     | A   | 200   | -        | -                                        |
| Rechnung2Name1            | A   | 100   | -        | Rechnungsadresse 2                       |
| Rechnung2Name2            | A   | 100   | -        | -                                        |
| Rechnung2Strasse          | A   | 100   | -        | -                                        |
| Rechnung2Adressgebiet     | A   | 300   | -        | -                                        |
| Rechnung2Land             | A   | 3     | -        | -                                        |
| Rechnung2PLZ              | A   | 5     | -        | -                                        |
| Rechnung2Ort              | A   | 100   | -        | -                                        |
| Rechnung2Ortsteil         | A   | 100   | -        | -                                        |
| Rechnung2Adresszusatz     | A   | 200   | -        | -                                        |
| HeimatName1               | A   | 100   | -        | Heimatadresse                            |
| HeimatName2               | A   | 100   | -        | -                                        |
| HeimatStrasse             | A   | 100   | -        | -                                        |
| HeimatAdressgebiet        | A   | 300   | -        | -                                        |
| HeimatLand                | A   | 3     | -        | -                                        |
| HeimatPLZ                 | A   | 5     | -        | -                                        |
| HeimatOrt                 | A   | 100   | -        | -                                        |
| HeimatOrtsteil            | A   | 100   | -        | -                                        |
| HeimatAdresszusatz        | A   | 200   | -        | -                                        |
| HeimatGemeinde            | A   | -     | V        | Verweis auf Tabelle<br>**Gemeinden**     |
| PassNr                    | A   | 100   | -        | -                                        |
| PassGueltigBis            | D   | -     | -        | -                                        |
| VisumNr                   | A   | 100   | -        | -                                        |
| VisumAblaufAm             | D   | -     | -        | -                                        |
| VisumAusstellungsort      | A   | 300   | -        | -                                        |
| Sozialversicherungsnummer | A   | 100   | -        | -                                        |
| Aufenthaltsbemerkung      | A   | 300   | -        | -                                        |
| ArbeitgeberBetrieb        | -   | -     | -        | Verweis auf Tabelle<br>**Betriebe**      |
| ArbeitgeberKontakt        | -   | -     | -        | Verweis auf Tabelle<br>**BetriebeKontakte** |
| ArbeitgeberAbteilung      | A   | 300   | -        | -                                        |
| ArbeitgeberPosition       | A   | 300   | -        | -                                        |
| SYNC                      | S   | -     | -        | -                                        |