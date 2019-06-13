# Tabelle Lehrer


| Feldname                  | Typ | Größe | Funktion | Bemerkung                                |
|---------------------------|-----|-------|----------|------------------------------------------|
| Mandant                   | I   | -     | PV       | Verweis auf Tabelle **Mandanten**        |
| ID                        | I+  | -     | P        | -                                        |
| EnbreaID                  | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| GUID                      | A   | 32    | -        | -                                        |
| IDIntern                  | I   | -     | P        | -                                        |
| IDExtern                  | I   | -     | P        | -                                        |
| GUIDExtern                | A   | 36    | -        | -                                        |
| Barcode                   | A   | 20    | -        | -                                        |
| BarcodePrint              | A   | 20    | -        | -                                        |
| Kuerzel                   | A   | 20    | -        | -                                        |
| Nachname                  | A   | 100   | -        | -                                        |
| NachnameNative            | A   | 100   | -        | -                                        |
| Namenszusatz              | A   | 100   | -        | -                                        |
| NamenszusatzNative        | A   | 100   | -        | -                                        |
| Vorname                   | A   | 100   | -        | -                                        |
| VornameNative             | A   | 100   | -        | -                                        |
| Vorname2                  | A   | 100   | -        | -                                        |
| Vorname2Native            | A   | 100   | -        | -                                        |
| Anrede                    | A   | 1     | -        | Mögliche Werte:<br/>0 = Frau<br/>1 = Herr<br/>2 = Frau Dr.<br/>3 = Herr Dr.<br/>4 = Frau Prof.<br/>5 = Herr Prof.<br/>6 = Frau Prof. Dr.<br/>7 = Herr<br/>Prof. Dr.<br/>:  = Ms.<br/>;  = Mrs.<br/>< = Mr. |
| Geschlecht                | A   | 1     | -        | Mögliche Werte:<br/>W = Weiblich<br/>M = Männlich |
| Geburtsdatum              | D   | -     | -        | -                                        |
| Geburtsname               | A   | 50    | -        | -                                        |
| Geburtsort                | A   | 100   | -        | -                                        |
| Ehestand                  | S   | -     | -        | Mögliche Werte:<br/>0 = Verheiratet<br/>1 = Nicht Verheiratet<br/>2 = Ledig<br/>3 = Geschieden<br/>4 = Verwitwet |
| Kinderzahl                | S   | -     | -        | -                                        |
| Strasse                   | A   | 100   | -        | -                                        |
| Adresszusatz              | A   | 200   | -        | -                                        |
| Land                      | A   | 3     | -        | -                                        |
| PLZ                       | A   | 5     | -        | -                                        |
| Ort                       | A   | 100   | -        | -                                        |
| Ortsteil                  | A   | 100   | -        | -                                        |
| Adressgebiet              | A   | 300   | -        | -                                        |
| Gemeinde                  | A   | 8     | V        | Verweis auf Tabelle **Gemeinden**        |
| Telefon                   | A   | 30    | -        | -                                        |
| Telefax                   | A   | 30    | -        | -                                        |
| Mobil                     | A   | 30    | -        | -                                        |
| Email                     | A   | 100   | -        | -                                        |
| TelefonDienst             | A   | 30    | -        | -                                        |
| TelefaxDienst             | A   | 30    | -        | -                                        |
| KFZ1                      | A   | 15    | -        | -                                        |
| KFZ2                      | A   | 15    | -        | -                                        |
| Kategorie                 | A   | 10    | V        | Verweis auf Tabelle **LehrerKategorien** |
| Staatsangeh               | A   | 10    | V        | Verweis auf Tabelle **Staatsangehoerigkeiten** |
| Staatsangeh2              | A   | 10    | V        | Verweis auf Tabelle **Staatsangehoerigkeiten** |
| Muttersprache             | A   | 10    | V        | Verweis auf Tabelle **Muttersprachen**   |
| Verkehrssprache           | A   | 10    | V        | Verweis auf Tabelle **Muttersprachen**   |
| Konfession                | A   | 10    | V        | Verweis auf Tabelle **Konfessionen**     |
| Bevollmaechtigung         | A   | 10    | V        | Verweis auf Tabelle **Bevollmaechtigungen** |
| Abteilung1                | A   | 10    | V        | Verweis auf Tabelle **Abteilungen**      |
| Abteilung2                | A   | 10    | V        | Verweis auf Tabelle **Abteilungen**      |
| Abteilung3                | A   | 10    | V        | Verweis auf Tabelle **Abteilungen**      |
| Funktion1                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion1Von              | D   | -     | -        | -                                        |
| Funktion1Bis              | D   | -     | -        | -                                        |
| Funktion2                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion2Von              | D   | -     | -        | -                                        |
| Funktion2Bis              | D   | -     | -        | -                                        |
| Funktion3                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion3Von              | D   | -     | -        | -                                        |
| Funktion3Bis              | D   | -     | -        | -                                        |
| Funktion4                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion4Von              | D   | -     | -        | -                                        |
| Funktion4Bis              | D   | -     | -        | -                                        |
| Funktion5                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion5Von              | D   | -     | -        | -                                        |
| Funktion5Bis              | D   | -     | -        | -                                        |
| Funktion6                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion6Von              | D   | -     | -        | -                                        |
| Funktion6Bis              | D   | -     | -        | -                                        |
| Funktion7                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion7Von              | D   | -     | -        | -                                        |
| Funktion7Bis              | D   | -     | -        | -                                        |
| Funktion8                 | A   | 10    | V        | Verweis auf Tabelle **LehrerFunktionen** |
| Funktion8Von              | D   | -     | -        | -                                        |
| Funktion8Bis              | D   | -     | -        | -                                        |
| Krankenkasse              | A   | 10    | V        | Verweis auf Tabelle **Krankenkassen**    |
| Versicherungsart          | A   | 10    | V        | Verweis auf Tabelle **Versicherungsarten** |
| NotfallPerson             | A   | 50    | -        | -                                        |
| NotfallTelefon            | A   | 30    | -        | -                                        |
| Personalnr                | A   | 15    | -        | -                                        |
| Statistiknr               | A   | 15    | -        | -                                        |
| ZugangDatum               | D   | -     | -        | -                                        |
| ZugangGrund               | A   | 10    | V        | Verweis auf Tabelle **LehrerZugaenge**   |
| AbgangDatum               | D   | -     | -        | -                                        |
| AbgangGrund               | A   | 10    | V        | Verweis auf Tabelle **LehrerAbgaenge**   |
| Amtsbez                   | A   | 10    | V        | Verweis auf Tabelle **Amtsbez**          |
| AmtsbezSeit               | D   | -     | -        | -                                        |
| Dienstverh                | A   | 10    | V        | Verweis auf Tabelle **Dienstverh**       |
| Dienstbez                 | A   | 10    | V        | Verweis auf Tabelle **Dienstbez**        |
| Dienstherr                | A   | 10    | V        | Verweis auf Tabelle **Dienstherren**     |
| Dienstalter               | S   | -     | -        | -                                        |
| LetzteUeberpruefung       | D   | -     | -        | -                                        |
| VertragVon                | D   | -     | -        | -                                        |
| VertragBis                | D   | -     | -        | -                                        |
| Beschaeftigungsart        | A   | 10    | V        | Verweis auf Tabelle **Beschaeftigungsarten** |
| Beschaeftigungsverh       | A   | 10    | V        | Verweis auf Tabelle **Beschaeftigungsverh** |
| BeschaeftigungSchulart    | A   | 10    | V        | Verweis auf Tabelle **Schularten**       |
| BeschaeftigungSchulzweig  | A   | 10    | V        | Verweis auf Tabelle **Schulzweige**      |
| Besoldung                 | A   | 10    | V        | Verweis auf Tabelle **Besoldungen**      |
| Ausbildung                | A   | 10    | V        | Verweis auf Tabelle **LehrerAusbildung** |
| Beruf                     | A   | 50    | -        | -                                        |
| BerichtendeSchule         | I   | -     | V        | Verweis auf Tabelle **Schulen**          |
| Abordnung1                | I   | -     | V        | Verweis auf Tabelle **Schulen**          |
| Abordnung1Art             | A   | 10    | V        | Verweis auf Tabelle **Abordnungsarten**  |
| Abordnung2                | I   | -     | V        | Verweis auf Tabelle **Schulen**          |
| Abordnung2Art             | A   | 10    | V        | Verweis auf Tabelle **Abordnungsarten**  |
| Status                    | S   | -     | -        | Mögliche Werte:<br/>0 = Inaktiv<br/>1 = Aktiv |
| Bemerkung                 | M   | -     | -        | -                                        |
| Passfoto                  | B   | -     | -        | -                                        |
| MerkmalA1                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalA2                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalA3                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalA4                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalA5                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalA6                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalS1                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalS2                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalS3                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalS4                 | A   | 10    | -        | Verweis auf Tabelle **LehrerMerkmale**   |
| MerkmalB1                 | A   | 15    | -        | -                                        |
| MerkmalB2                 | A   | 15    | -        | -                                        |
| MerkmalB3                 | A   | 15    | -        | -                                        |
| MerkmalB4                 | A   | 15    | -        | -                                        |
| Bank1                     | I   | -     | V        | Verweis auf Tabelle **Banken**           |
| Bank1Konto                | A   | 20    | -        | Bankkonto 1                              |
| Bank1IBAN                 | A   | 28    | -        | -                                        |
| Bank1Inhaber              | A   | 300   | -        | -                                        |
| Bank1Info                 | A   | 300   | -        | -                                        |
| Bank1Bemerkung            | A   | 300   | -        | -                                        |
| Bank2                     | I   | -     | V        | Verweis auf Tabelle **Banken**           |
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
| HeimatGemeinde            | A   | 8     | V        | Verweis auf Tabelle **Gemeinden**        |
| PassNr                    | A   | 100   | -        | -                                        |
| PassGueltigBis            | D   | -     | -        | -                                        |
| VisumNr                   | A   | 100   | -        | -                                        |
| VisumAblaufAm             | D   | -     | -        | -                                        |
| VisumAusstellungsort      | A   | 300   | -        | -                                        |
| Sozialversicherungsnummer | A   | 100   | -        | -                                        |
| Aufenthaltsbemerkung      | A   | 300   | -        | -                                        |
| SYNC                      | S   | -     | -        | -                                        |

